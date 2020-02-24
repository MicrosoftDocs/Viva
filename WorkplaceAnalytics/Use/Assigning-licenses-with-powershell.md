---

title: Assigning Workplace Analytics licenses with PowerShell
description: How to assign Workplace Analytics licenses in Azure Active Directory by using PowerShell
author: madehmer
ms.author: madehmer
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Assign Workplace Analytics licenses with PowerShell

Use the following steps to assign Workplace Analytics licenses with PowerShell in Azure Active Directory (Azure AD).

## Installation prerequisites

1. Install the Azure AD PowerShell module by following these steps:

     a) Open an elevated Windows PowerShell command prompt.

     b) Run the following command:

         ``` powershell
         Install-Module *AzureAD*
        ```
2. Run the Azure AD PowerShell module:

    a) Start PowerShell.

    b) Type the following command:

        ``` powershell
        Import-Module *AzureAD*
        ```

## Assigning licenses

Workplace Analytics can only extract data from the accounts of users who have valid Workplace Analytics licenses.

1. To assign a Workplace Analytics license to a user:

    With PowerShell open, start the Import Module, and log in to Azure AD by running the following commands:

       Import-Module *AzureAD*

       Connect-AzureAD

    To log in, you will need credentials with admin privileges.

   ![Azure Active Directory login](../images/WpA/Use/azure-ad-log-in-1.png)

2. Copy and paste the following variable data into the PowerShell command line, and then run it:

      ``` powershell

       $UserToLicense = Get-AzureADUser -SearchString ‘<usertolicense@domain.com>’
       $LicenseSku = Get-AzureADSubscribedSku | Where {$_.SkuPartNumber -eq 'WorkPlace_Analytics'}
       $License = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense
       $License.SkuId = $LicenseSku.SkuId
       $AssignedLicenses = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses

      ```

3. To assign a license, copy and paste the following code into the PowerShell command line, and then run it:

      ``` powershell

       $AssignedLicenses.AddLicenses = $License
       Set-AzureADUserLicense -ObjectId $UserToLicense.ObjectId -AssignedLicenses $AssignedLicenses

      ```

4. To verify that the license has been assigned, copy and paste the following code into the PowerShell command line, and then run it:

      ``` powershell

       Get-AzureADUserLicenseDetail -ObjectId $UserToLicense.ObjectId | Select -Expand ServicePlans | Where {$_.ServicePlanName -eq "Workplace_Analytics"}

      ```

   After you’ve run this last command, you’ll see an entry on the command line. If not, or if an error message displays, the license was not successfully assigned.

## View Available licenses on your tenant

To view available licenses for your tenant and current usage run the following in PowerShell:

```powershell
Connect-MsolService
```

Now that you're connected to the Office 365 tenant, run the following next:

```powershell
Get-MsolAccountSku
```

## Add Workplace Analytics licenses in bulk through Office365 PowerShell

If you need to assign Workplace Analytics licenses to a large number of users, you can use the bulk license script for Office365 PowerShell provided in this section.

### Software Requirements

The Workplace Analytics bulk license script uses the Azure Active Directory PowerShell module to make the necessary licensing changes to your tenant identities. To ensure that the Azure Active Directory PowerShell module is installed:

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
> If the cmdlet fails to execute, you might be running an older version of Windows Management Framework (WMF). In that case, download and install the required sign-in assistant and the Azure Active Directory PowerShell module through MSI. For instructions to install these required packages, see
[Connect to Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell).

## Input Requirements

The Workplace Analytics bulk license script uses a .csv reference file as input. The script references each address listed in the .csv file and attempts to assign Workplace Analytics license to all users.

Each user who is already assigned a license retains all current licensing. New users will receive a Workplace Analytics license. The input .csv must have a single column with the header "Email" that contains all email addresses. The following example shows the correct .csv email format.

|Email|
|---|
|User1@contoso.com|
|User2@contoso.com|

For further information on formatting the input .csv file, see [example .csv export file](https://docs.microsoft.com/workplace-analytics/setup/prepare-organizational-data#example-csv-export-file)

### Script description

The Add-WpALicense.ps1 script is designed to easily allow the assignment of Workplace Analytics licenses to Office365 identities based on .csv email address input. The email address input is used to identify the correct Office365 identity based on the UserPrincipalName and ProxyAddresses attributes of the MSOL object, and attempts to assign a license to the Office365 identity.

### Script Execution

1. Create a folder, C:\Scripts, if it does not already exist.
2. Copy the following script and paste it into a text editor, and then save the script as C:\Scripts\Add-WpALicense.ps1.


``` powershell
<#
.NOTES
	    Title:			Add-WpALicense.ps1
	    Date:			February 21st, 2020
	    Version:		1.0.0
	
.SYNOPSIS
    This script is designed to allow Workplace Analytics licenses to be added to a CSV list of email addresses that correlate to Office365 identities.
.DESCRIPTION
    Add-WpALicense is designed to allow assigning Workplace Analytics licenses easily to Office365 identities based on CSV e-mail address input. The e-mail address input will be used to identify the correct Office365 identity based on the UserPrincipalName and ProxyAddresses attributes of the MSOL object and try to assign a license to the identity.
.PARAMETER CSV
    The CSV input file containing all of the email addresses that will be given the license. Use Email as the header and when save the file with the UTF-8 encoded format.
.PARAMETER LicenseSKU
   The WORKPLACE_ANALYTICS LicenseSKU will be applied to a user if found. The script will try to automatically apply a license sku. If a license sku is provided, the script will try to match it with the domain. When specifying a sku an example would be CONTOSO:WORKPLACE_ANALYTICS.
.EXAMPLE
   .\Add-WpALicense.ps1 -CSV c:\users\user123\desktop\input.csv -LicenseSku CONTOSO:WORKPLACE_ANALYTICS

   The above execution would ingest the CSV file from the location above and attempt to apply the MSOL license SKU of CONTOSO:WORKPLACE_ANALYTICS to all users to be found in the MSOL structure of the tenant.

       #>
       param
       (
       [parameter(Mandatory=$true,Position=0,HelpMessage="Please provide a CSV containing the Email address column header.")]
       [ValidateNotNullorEmpty()]
       [string]$CSV,
       [parameter(Mandatory=$true,Position=1,HelpMessage="Please provide the exact name of the Workplace Analytics MSOL Account Sku license for the tenant to be affected.")]
       [ValidateNotNullorEmpty()]
       [string]$LicenseSKU
       )

       #Simple function to connect to Office365 MSOL PowerShell

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
                   Write-Output "Successfully connected to Office365 MSOL, proceeding..."
               }
               catch {
                   Write-Error "Could not connect to Office365 MSOL due to the following exception.`r`n$($_.Exception.Message)"
                   break
               }
           }
       }

       #Simple function to get to MSOL SKU information.

       Function Get-WorkplaceAnalyticsSku {
           param ($searchString)
           $O365MsolSKUs = Get-MsolAccountSku
           try {
               $wpaSku = $O365MsolSKUs | Where-Object { $_.AccountSkuId -like $searchString }
               if ($wpaSku) {
                   Write-Host "Office365 tenant possesses the correct WorkplaceAnalytics license, proceeding..."
                   [int]$availableLicenses = $wpaSku.ActiveUnits - $wpaSku.ConsumedUnits
                   Write-Host "Using Sku: $($wpaSku.AccountSkuId), Total Licenses: $($wpaSku.ActiveUnits), Used Licenses: $($wpaSku.ConsumedUnits), Available Licenses: $($availableLicenses)"
                   return $wpaSku
               }
               else {
                   Write-Error "Script could not find matching WorkplaceAnalytics license using $searchString on Office365 tenant. Here are the available SKU's for this tenant:"
                   Write-warning ($O365MsolSKUs | out-string)
                   write-warning "Please Rerun script and specify a SKU above with parameter -LicenseSKU {sku} including the appropriate WORKPLACE_ANALYTICS SKU"  
                   exit 1
               }
           }
           catch {
                Write-Error "Failed to determine the Office365 tenant licenses, script cannot proceed!`n$_."
                exit 1
           }
       }

       #Start-Transcript to keep a simple log of all stream output of the successes and failures of the execution and to set StrictMode.

       Start-Transcript
       Set-StrictMode -version 2

       #Simple if block to test the CSV param input and ensure that the path is valid and contains a file.

       if (!(Test-Path $CSV)) {
       Write-Error "CSV file could not be found, please ensure that the location is correct and you have the proper permissions to read the file then try again.`r`n$($_.Exception.Message)"
       break
       }
       Write-Output "CSV file was found, proceeding..."
       try {
            #If the CSV is valid and found an attempt will be made to import the contents into a user's csv array to be used for processing.
            [array]$users = @(Import-Csv $CSV -ErrorAction Stop)
            Write-Output "CSV file was imported to process successfully, proceeding..."
        }
        catch {
                Write-Error "Failed to import CSV for processing due to the following exception.`r`n$($_.Exception.Message)"
                break
            }
       }
       else
       {
           Write-Error "CSV file could not be found, please ensure that the location is correct and try again.`r`n$($_.Exception.Message)"
           break
       }

       #If the user's array contains the Email member which is created by importing of a proper CSV and the object count of the user's array is greater than 0, the processing block will be entered and a foreach loop will be used to process the array contents.

       if(($users | Get-Member Email) -and (($users.Email).count -gt 0))
       {
       Write-Output "CSV file is valid, proceeding..."
       foreach($user in $users)
       {
        #An attempt is made to find the user through the UserPrincipalName parameter. If an error is thrown the catch block will attempt to find the user through a ProxyAddresses attribute regex comparison. An absolute match after the colon of the address in the array must be made to increase the accuracy of the find.
        try
        {
            $msolUser = Get-MsolUser -UserPrincipalName $user.Email -ErrorAction Stop
            Write-Output "Found user $($user.Email) via UPN, proceeding..."
        }
        catch
        {
          Write-Output "Failed to find user through UPN lookup, attempting ProxyAddress attribute..."
          $msolUser = Get-MsolUser -All | Where-Object {$_.ProxyAddresses -match "\:$($user.Email)"}
        }

        #If the msolUser variable is not null the following block will be entered where an attempt will be made to add the LicenseSKU parameter to the MSOL user.
        if($msolUser)
        {
              Write-Output "User $($user.Email) found, attempting to license..."
               try
               {
                  Set-MsolUserLicense -UserPrincipalName $msolUser.UserPrincipalName -AddLicenses $LicenseSKU -ErrorAction Stop | Out-Null
                  Write-Output "Successfully licensed user $($msolUser.UserPrincipalName) with $($LicenseSKU) license."
               }
                catch
               {
                  Write-Error "Failed to license user $($msolUser.UserPrincpalName) due to the following exception.`r`n$($_.Exception.Message)"
               }
           }
           else
           {
                Write-Error "Could not find user $($user.Email), skipping!"
             }
          }
       }
       else
       {
        Write-Error "The CSV provided did not contain the valid header of Email or did not contain any values to be evaluated. Please ensure that the CSV contains the correct header and valid data and try again."
       break
       }

       Stop-Transcript
```

   With the PowerShell environment now prepared, and the input file constructed, the script can now execute.

3. Start Windows PowerShell and run the following command:

    C:\Scripts\Add-WpALicense.ps1 -CSV <CSVLocation>

    Note that the \<CSVLocation> should contain the full path to the .csv input file such as C:\Scripts\InputFile.csv.

4. When prompted, enter the Office365 global administrator credentials for the tenant where the licenses are to be added.

   If all the required inputs are satisfied, the script now executes against the .csv list and licenses are then assigned to users. During the script execution, all successes and failures are shown on the command line.

## FAQ

**It appears something went wrong during the script execution. Is there a log of the script actions?**

Yes, you can find a script transcript for each execution in the Documents folder of the person who executed the script.

**Will an email address input work if it is not the UserPrincipalName of any MSOL identity?** 

The script logic first attempts to find the MSOL identity through the UserPrincipalName by using the email address from the .csv file. If this attempt fails, the script tries to to find any MSOL object that contains the email address from the .csv file within the ProxyAddresses property. If a user still cannot be found, the email is deemed not to exist and is skipped.

**Does this work with Multi-Factor Authentication (MFA)?**

This script works with Multi-Factor Authentication because the Connect-MsolService cmdlet supports Azure Active Directory Authentication Library (ADAL).

## Related topics

[Assign licenses with PowerShell](https://aka.ms/Instructions_AssignLicenseUsingPowerShell)
