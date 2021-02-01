---
ROBOTS: NOINDEX,NOFOLLOW
title: Assign licenses with PowerShell for insights
description: Learn how to assign licenses with PowerShell to people who want to use Workplace Analytics insights
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: none 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Assign licenses with PowerShell

You must be able to sign in as a global admin to Azure Active Directory (Azure AD) to assign licenses with PowerShell to one or more users who subscribe to a Microsoft or Office 365 E5 or E3 plan whose [geo location is North America](https://docs.microsoft.com/microsoft-365/enterprise/microsoft-365-multi-geo#microsoft-365-multi-geo-availability).

Alternatively, you can [use the Microsoft admin center to assign licenses](assign-licenses-admin-c.md).

## Assign licenses to individual users

Confirm the prerequisites and then follow the steps to assign licenses with Azure AD PowerShell.

### Prerequisites

1. Install the Azure AD PowerShell module by following these steps:

   1. Open an elevated Windows PowerShell command prompt.

   2. Enter the following command:

      ``` powershell
      Install-Module *AzureAD*
      ```

2. Run the Azure AD PowerShell module:

   1. Start PowerShell.

   2. Enter the following command:

      ``` powershell
      Import-Module *AzureAD*
      ```

### To assign licenses with Azure AD PowerShell

1. To assign an insights license to a user:

   With PowerShell open, start the Import Module, and log in to Azure AD:

     ``` powershell
    Import-Module *AzureAD*
     ```

     ```powershell
    Connect-AzureAD
      ```

   Log in with admin credentials:

    ![Azure Active Directory login](./images/azure-ad-log-in-1.png)

2. Run the following from the command line:

      ``` powershell
       $UserToLicense = Get-AzureADUser -SearchString '<usertolicense@domain.com>'
       $LicenseSku = Get-AzureADSubscribedSku | Where {$_.SkuPartNumber -eq 'WorkPlace_Analytics'}
       $License = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense
       $License.SkuId = $LicenseSku.SkuId
       $AssignedLicenses = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses
      ```

3. To assign a license:

      ``` powershell
       $AssignedLicenses.AddLicenses = $License
       Set-AzureADUserLicense -ObjectId $UserToLicense.ObjectId -AssignedLicenses $AssignedLicenses
      ```

4. To verify that the license is assigned:

      ``` powershell
       Get-AzureADUserLicenseDetail -ObjectId $UserToLicense.ObjectId | Select -Expand ServicePlans | Where {$_.ServicePlanName -eq "Workplace_Analytics_insights"}
      ```

   After the license is assigned, you'll see an entry on the command line. If not, or if an error message shows, the license was not successfully assigned.

## View Available licenses on your tenant

To view available licenses for your tenant and current usage run the following in PowerShell:

```powershell
Connect-MsolService
```

Now that you're connected to the Microsoft 365 tenant, run the following next:

```powershell
Get-MsolAccountSku
```

## Assign licenses to a large group

If you need to assign licenses for insights to a large number of users, you can use the bulk license script with Azure AD PowerShell. Confirm the prerequisites, input requirements, and then use the following steps to do so.

### Prerequisites

The Insights bulk license script uses the Azure AD PowerShell module to make the necessary licensing changes to your tenant identities. To ensure that the Azure AD PowerShell module is installed:

1. Open Windows PowerShell as an administrator and run the following command:

   ```powershell
   Set-ExecutionPolicy RemoteSigned
   ```

2. When a confirmation message appears, accept the change in order to allow local PowerShell scripts to run.

3. After the execution policy is set correctly on the machine, run the following cmdlet:

   ```powershell
    Install-Module -Name MSOnline -Repository PSGallery
   ```

> [!Note]
> If the cmdlet fails to execute, you might be running an older version of Windows Management Framework (WMF). In that case, download and install the required sign-in assistant and the Azure Active Directory PowerShell module through MSI. For instructions to install these, see
[Connect to Microsoft 365 PowerShell](https://docs.microsoft.com/microsoft-365/enterprise/connect-to-microsoft-365-powershell).

### Input requirements

The Insights bulk license script uses a .csv reference file as input. The script references each address listed in the .csv file and attempts to assign Insights license to all users.

Each user who is already assigned a license retains all current licensing. New users will receive a Insights license. The .csv input must have a single column with the header "Email" that contains all email addresses.

#### Example .csv export file

Here's a partial example of a valid .csv export file:

PersonId,EffectiveDate,HireDate,ManagerId,TimeZone,LevelDesignation,Organization,Layer,Area
Emp1@contoso.com,10/1/2020,1/3/2014,Mgr1@contoso.com,Pacific Standard Time,5,Sales,8,Southeast
Emp2@contoso.com,11/1/2020,1/3/2014,Mgr1@contoso.com,Pacific Standard Time,5,Sales,8,Southeast
Emp3@contoso.com,12/1/2020,1/3/2014,Mgr2@contoso.com,Pacific Standard Time,4,Sales,7,Northeast
Emp4@contoso.com,10/1/2020,8/15/2015,Mgr3@contoso.com,Pacific Standard Time,6,Sales,9,Midwest
Emp5@contoso.com,11/1/2020,8/15/2015,Mgr3@contoso.com,Pacific Standard Time,6,Sales,9,Midwest
Emp6@contoso.com,12/1/2020,8/15/2015,Mgr3@contoso.com,Pacific Standard Time,6,Sales,9,Midwest

### To run the script

The Add-WpAInsightsLicense.ps1 script is designed to assign Insights licenses to Microsoft 365 identities based on the .csv email address input. The email address input is used to identify the correct Microsoft 365 identity based on the **UserPrincipalName** and **ProxyAddresses** attributes of the MSOL (Microsoft Online) object, and then tries to assign a license to the Microsoft 365 identity.

1. Create a **C:\Scripts** folder if it does not already exist.
2. Copy the following script and paste it into a text editor, and then save the script as **C:\Scripts\Add-WpAInsightsLicense.ps1**.

   ```powershell
   <#
   .NOTES
    Title:    Add-WpAInsightsLicense.ps1
    Date:     February 2021
    Version:  1.0
   .SYNOPSIS
    This script is designed to add Insights licenses to a CSV list of email addresses that correlate to Microsoft 365 identities.
   .DESCRIPTION
    Add-WpAInsightsLicense is designed to assign Insights licenses to Microsoft 365 identities based on CSV e-mail address input. The e-mail address input will be used to identify the correct Microsoft365 identity based on the UserPrincipalName and ProxyAddresses attributes of the MSOL object and try to assign a license to the identity.
   .PARAMETER CSV
    The CSV input file contains all of the email addresses that are given a license. Use Email as the header and when save the file with the UTF-8 encoded format.
   .PARAMETER LicenseSKU
    The WORKPLACE_ANALYTICS_Insights LicenseSKU will be applied to a user that's found. The script tries to automatically apply a license SKU. If a license SKU is provided, the script tries to match it with the domain. An example SKU is CONTOSO:WORKPLACE_ANALYTICS_INSIGHTS.
    .EXAMPLE
    .\Add-WpAInsightsLicense.ps1 -CSV c:\users\user123\desktop\inputCSV -LicenseSku CONTOSO:WORKPLACE_ANALYTICS_INSIGHTS

    The script would ingest the CSV file from the specified location in this example and try to apply the MSOL license SKU of CONTOSO:WORKPLACE_ANALYTICS to all users that are found in the MSOL structure of the tenant.
       #>
       param
       (
       [parameter(Mandatory=$true,Position=0,HelpMessage="Please provide a CSV file that has the Email column header.")]
       [ValidateNotNullorEmpty()]
       [string]$CSV,
       [parameter(Mandatory=$true,Position=1,HelpMessage="Please provide the exact name of the Workplace Analytics Insights MSOL Account SKU license for the applicable tenant.")]
       [ValidateNotNullorEmpty()]
       [string]$LicenseSKU
       )
       #Simple function to connect to Microsoft 365 MSOL PowerShell.
       Function Connect-O365PowerShell {
           try {
               Import-Module MSOnline -ErrorAction Stop
               Write-Output "Successfully imported the Azure Active Directory PowerShell module, proceeding..."
           }
           catch {
               Write-Error -Message "Windows Azure Active Directory PowerShell module could not be found, please install the module and run this script again!"
               break
           }
           if(Get-Module -Name MSOnline) {
               try {
                   Connect-MsolService -ErrorAction Stop
                   Write-Output "Successfully connected to Microsoft 365 MSOL, proceeding..."
               }
               catch {
                   Write-Error "Could not connect to Microsoft 365 MSOL due to the following exception.`r`n$($_.Exception.Message)"
                   break
               }
           }
       }
       #Simple function to get to MSOL SKU information.
       Function Get-WorkplaceAnalyticsInsightsSku {
           param ($searchString)
           $O365MsolSKUs = Get-MsolAccountSku
           try {
               $wpaSku = $O365MsolSKUs | Where-Object { $_.AccountSkuId -like $searchString }
               if ($wpaSku) {
                   Write-Host "Microsoft365 tenant possesses the correct WorkplaceAnalytics license, proceeding..."
                   [int]$availableLicenses = $wpaSku.ActiveUnits - $wpaSku.ConsumedUnits
                   Write-Host "Using Sku: $($wpaSku.AccountSkuId), Total Licenses: $($wpaSku.ActiveUnits), Used Licenses: $($wpaSku.ConsumedUnits), Available Licenses: $($availableLicenses)"
                   return $wpaSku
               }
               else {
                   Write-Error "Script could not find matching WorkplaceAnalytics license using $searchString on Microsoft365 tenant. Here are the available SKU's for this tenant:"
                   Write-warning ($O365MsolSKUs | out-string)
                   write-warning "Please Rerun script and specify a SKU above with parameter -LicenseSKU {sku} including the appropriate WORKPLACE_ANALYTICS SKU"  
                   exit 1
               }
           }
           catch {
                Write-Error "Failed to determine the Microsoft365 tenant licenses, script cannot proceed!`n$_."
                exit 1
           }
       }
       #Start-Transcript to keep a simple log of all stream output of the successes and failures of the execution and to set StrictMode.
       Start-Transcript
       Set-StrictMode -version 2
       #Simple if block to test the CSV parameter input and confirm the path is valid and contains a file.
       if (!(Test-Path $CSV)) {
         Write-Error "CSV file could not be found, please ensure that the location is correct and you have the proper permissions to read the file then try again.`r`n$($_.Exception.Message)"
       break
       }
       Write-Output "CSV file was found, proceeding..."
       try {
          #If the CSV is valid, this tries to import the contents into a user's CSV array that's used for processing.
          [array]$users = @(Import-Csv $CSV -ErrorAction Stop)
           Write-Output "CSV file was imported to process successfully, proceeding..."
        }
        catch {
           Write-Error "Failed to import CSV for processing due to the following exception.`r`n$($_.Exception.Message)"
           break
        }
       #After CSV formatting is verified, check for Email values in the file.
       if(($users.count) -le 0) {
          Write-Error "The CSV provided did not contain any valid SMTP data. Please check the CSV file and try again."
          break
       }
       Write-Host "Found $($users.count) items in the CSV to process"
       #Check the CSV contains the proper Email header.
       if ($users | Get-Member Email) {
          Write-Host "CSV file is valid, proceeding..."
       }
       else {
          Write-Warning "CSV is missing Email header. Please check the CSV file specified and update the CSV to include the header: Email"
          break
        }
        #Calling Connect-O365PowerShell function to establish connection.
        try {
            Connect-O365PowerShell -ErrorAction Stop
        }
        catch {
           Write-Error "Failed to successfully connect to Azure Active Directory PowerShell due to the following exception.`r`n$($_.Exception.Message)"
           break
        }
        #Try to pull MSOL SKUs.
        if ([string]::isnullorempty($LicenseSku)) {
           $wpaSearch = "*:WORKPLACE_ANALYTICS_INSIGHTS"
        }
        else {
           $wpaSearch = "*$LicenseSku*"
        }
        $LicenseSku = Get-WorkplaceAnalyticsInsightsSku -searchString $wpaSearch
        $NumofSuccessfullyLicensed = 0
        $NumofErrorLicensed = 0
        $NumOfAlreadyLicensed = 0
        $NumOfUsersNotFound = 0
        [System.Collections.ArrayList]$UsersNotFound =@()
        [System.Collections.ArrayList]$UsersFailedtoLicense =@()
        #If the user's array contains the Email member who is created by importing a CSV and the object count of the user's array is greater than zero (0), the processing block is entered and a foreach loop is used to process the array contents.
        Foreach($user in $users) {
           #An attempt is made to find the user through the UserPrincipalName parameter. If an error occurs, the catch block will try to find the user through a ProxyAddresses attribute regex comparison. An absolute match after the colon of the address in the array is required to increase the accuracy of the find.
           $userIndex = $users.Indexof($user)
           Write-Progress -Activity "Assigning Workplace Analytics Insights Licenses, currently on $($userIndex + 1) of $($users.Count) Currently searching for user $($user.Email)" -PercentComplete ($userIndex / $users.Count * 100) -Id 1
           try {
               $msolUser = Get-MsolUser -UserPrincipalName $user.Email -ErrorAction Stop
            }
            catch {
               Write-Warning "Failed to find user $($user.Email) through UPN lookup, attempting ProxyAddress attribute...`n$_"
               $msolUser = Get-MsolUser -All | Where-Object {$_.ProxyAddresses -match "\:$($user.Email)"}
            }
            if($msolUser) {
                #If the msolUser variable is not null, the following block will be entered where an attempt is made to add the LicenseSKU parameter to the MSOL user.
                if ($msolUser.Licenses.AccountSkuId -contains $LicenseSKU.AccountSkuId) {
                   Write-Warning "User $($msolUser.UserPrincipalName) was found but is already licensed for WorkplaceAnalytics, skipping licensing."
                   $NumOfAlreadyLicensed++
                }
                else {
                   Write-Output "User $($user.Email) found, attempting to license..."
                   try {
                      Set-MsolUserLicense -UserPrincipalName $msolUser.UserPrincipalName -AddLicenses $LicenseSKU.AccountSkuId -ErrorAction Stop | Out-Null
                      Write-Output "Successfully licensed user $($msolUser.UserPrincipalName) with $($LicenseSKU.AccountSkuId) license."
                      $NumofSuccessfullyLicensed++
                    }
                    catch {
                       Write-Error "Failed to license user $($msolUser.UserPrincpalName) due to the following exception.`r`n$($_.Exception.Message)"
                       $NumofErrorLicensed++
                       $UsersFailedtoLicense.Add($user.Email) | Out-Null
                    }
                }
            }
            else {
               $NumOfUsersNotFound++
               $NumofErrorLicensed++
               $UsersNotFound.Add($user.Email) | Out-Null
               Write-Error "Could not find user $($user.Email), skipping!"
               continue
            }
        }
        if ($UsersFailedtoLicense.count -ne 0) {
            Write-Output "`nThe following $($UsersFailedtoLicense.count) failed to License:`n"
            Write-Output $UsersFailedtoLicense
        }
        if ($UsersNotFound.Count -ne 0) {
            Write-Output "`nThe following $($UsersNotFound.count) users were not found:`n"
            Write-Output $UsersNotFound
        }
        $finaloutput = "`nScript completed, Total number of users licensed:$NumofSuccessfullyLicensed"
        $finaloutput += "`nTotal number of users that were already licensed:$NumOfAlreadyLicensed"
        $finaloutput += "`nErrors encountered:$NumofErrorLicensed"
        $finaloutput += "`nTotal users not found:$NumOfUsersNotFound"

        Write-Output $finaloutput
      Stop-Transcript
   ```

   After the PowerShell environment is prepared and the input file constructed, confirm that the CSV user file is in the same directory as the script, and then you can execute the script.

3. Start Windows PowerShell and run the following command:

   ``` powershell
    C:\Scripts\Add-WpAInsightsLicense.ps1 -CSV <CSVLocation>
   ```

   > [!Note]
   > That the \<CSVLocation> should contain the full path to the .csv input file, such as **C:\Scripts\InputFile.csv**.

4. When prompted, enter the Microsoft 365 global administrator credentials for the tenant where the licenses are to be added.

   If all the required inputs are satisfied, the script executes now against the .csv list, and then licenses are assigned to users. During the script execution, all successes and failures are shown on the command line and a transcript is saved in the Documents folder.

## FAQ

**Something went wrong during the script execution. Is there a log of the script actions?**

Yes, you can find a script transcript for each execution in the Documents folder for the person who executed the script.

**Will an email address input work if it is not the UserPrincipalName of any MSOL identity?**

The script logic first attempts to find the MSOL identity through the UserPrincipalName by using the email address from the CSV file. If this attempt fails, the script tries to find any MSOL object that contains the email address from the .csv file within the ProxyAddresses property. If a user still cannot be found, the email is deemed not to exist and is skipped.

**Does this work with Multi-Factor Authentication (MFA)?**

This script works with Multi-Factor Authentication because the Connect-MsolService cmdlet supports Azure Active Directory Authentication Library (ADAL).

## Troubleshooting

**Error: The CSV provided did not contain any valid SMTP data. Please check the CSV file and try again.**

Check the CSV file contains the proper header and valid email addresses to parse

**Error: Could not find user user1@contoso.com, skipping!**

Check that the email properly resolves.

**Error: The property 'AccountSkuId' cannot be found on this object. Verify that the property exists.**

Check that the user has the proper EXO license.

**Error: The CSV file could not be found ...**

Confirm the correct file is specified when defining the `-CSV` and that the user running the script has permissions to read the file.

**If the script is successful but the output reports: Script completed, but the total number of users licensed is zero (0).**

1. Confirm the user is not already licensed.
2. Confirm the user is subscribed to a Microsoft or Office 365 E5 or E3 plan.
3. Confirm the users UPN or proxy email address resolves in the environment.

## Related topics

* [Assign roles](assign-roles.md)
* [Setup overview](./setup.md)
