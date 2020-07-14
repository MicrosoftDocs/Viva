---

ROBOTS: NOINDEX,NOFOLLOW
title: Use a script to prepare organizational data in Workplace Analytics
description: How to use a script to prepare data from your organization to upload and use in Workplace Analytics 
author: paul9955
ms.author: v-pausch
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
audience: Admin
---

# Use a script to prepare organizational data

## Introduction 

Whether this is your first time onboarding users to Workplace Analytics or you are creating a new file to update organizational data, this script should help. It uses the [MSOnline service](https://docs.microsoft.com/powershell/azure/active-directory/overview?view=azureadps-1.0) to find user mailboxes within your organization. It then uses your Azure Active Directory data to create a Workplace Analytics organizational-data file for you. A Workplace Analytics admin can upload this file as is or edit it first. For more information, see [Prepare organizational data](prepare-organizational-data.md), [Upload organizational data (first upload)](upload-organizational-data-1st.md), and [Upload organizational data (subsequent uploads)](upload-organizational-data.md). 

## Prerequisites

This script requires the following elements. If you need help while installing these prerequisites, contact Workplace Analytics FastTrack services; see [Get support](../overview/getting-support.md) for more information or contact FastTrack services directly by sending email to <wpasetup@microsoft.com>.

* **PowerShell version 5.0 or higher**. To check the version of PowerShell on your computer:
   
   1.	In Windows, select **Start**, type **PowerShell**, and press **Enter**. 
   2.	In the Windows PowerShell window, type **$PSVersionTable** and press **Enter**. Verify that the value listed for “PSVersion” is at least 5.0. If it is not, see: [Installing Windows PowerShell](https://docs.microsoft.com/powershell/scripting/windows-powershell/install/installing-windows-powershell?view=powershell-7). 
   
    For information about using PowerShell on the Mac, see [Installing PowerShell on macOS](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-macos?view=powershell-7). 
    
    Note that when you install the following modules – AAD and MSOnline – you first need to start PowerShell as an administrator: 

    ![Run as administrator](../images/wpa/setup/run-as-admin.png)
 
* **The Azure Active Directory module**. For installation instructions, see [Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/en-us/powershell/azure/active-directory/install-adv2?view=azureadps-2.0). To install the AAD module, use the PowerShell command:

   ```
   Install-Module AzureAD
   ```

* **The MSOnline module**. This service is used to determine which accounts are real users with mailboxes. For information about installing MSOnline, see [Azure ActiveDirectory (MSOnline)](https://docs.microsoft.com/en-us/powershell/azure/active-directory/install-msonlinev1?view=azureadps-1.0). To install the MSOnline module, use the PowerShell cmdlet:

   ```
   Install-Module MSOnline
   ```

## Run the script

1.	Download the latest version of the script: [Organizational data script](https://aka.ms/WpaOrgFileFromAad). 
2.	Extract the downloaded script zip file and note its folder location.
3.	Open a new instance of Windows PowerShell with administrator privileges.
4.	In PowerShell, navigate to the folder that contains the extracted script files.
   
    _Example:_ 

    cd c:\users\localuser\desktop\orgfilecreation
    
5.	In PowerShell, run the following commands to make sure that the downloaded files are unblocked from execution:
   
    _Run:_ 
    ```
    Unblock-File .\Generate-WpaOrganizationFile.ps1
    ```
    
    _Run:_
    ``` 
    Unblock-File .\helper.psm1
    ```

6.	The script is now ready to run. If this is your first time creating an organizational data file and your organization requires multi-factor authentication, run the script with the default options:
    
    _Run:_ 
    ```
    .\Generate-WpaOrganizationFile.ps1 -RequireCredentialPrompt	
    ```
    
   As it runs, the script prompts you twice for credentials, once to authenticate to the Azure Active Directory service, and once to authenticate to the MSOnline service.

### Examples

The following example command lines create an organizational data file in different ways, with the inclusion of different data. 

#### Example 1

This example does **not** gather the optional properties City, Country, Office, and Title from Active Directory:

   .\Generate-WpaOrganizationFile.ps1 -RequireCredentialPrompt -SkipOptionalProperties

#### Example 2

This example sets the EffectiveDate field in the resulting organizational data file to the current day:

   .\Generate-WpaOrganizationFile.ps1 -RequireCredentialPrompt -EffectiveDateOption Delta

> [!Note] 
> If you do not use this option, the effective date will default to a fixed date in the past, such as 01/01/1970. 

#### Example 3

Use the parameters in the following example if your organization does not enforce multi-factor authentication and you would like to create PSCredential objects and pass them into the script so that the script can run unattended:

   .\Generate-WpaOrganizationFile.ps1 -MSOLCredential $MsolCred -AzureADCredential $AzureADcred

## Parameter reference

You can use the following parameters with the Generate-WpaOrganizationFile.ps1 script. 

|Parameter |Type | Description |
|------|-----------|----------|
|MSOLCredential	|pscredential	|The credential of a user who can authenticate with the MSOnline service and execute the Get-MsolUser cmdlet.  |
|AzureADCredential	|pscredential	|The credential of a user who can authenticate with the Azure AD service and execute read-only cmdlets such as Get-AzureADUser.|
|RequireCredentialPrompt	|switch|	If your organization's IT requires multifactor authentication, this switch lets you authenticate by prompting you for credentials. It uses the built-in prompts that are provided by the Connect-AzureAD and Connect-MsolService cmdlets.|
| EffectiveDateOption|	string|	Used to determine the EffectiveDate.<ul><li>Select the InitialPull option if this is the first time you are generating an organizational data file for Workplace Analytics.</li><li>Use the Delta option if you are creating a subsequent upload of organizational data.</li></ul> |
|SkipOptionalProperties|	switch|	As part of information gathering, there are additional properties available via Azure AD and MSOnline that are not required by Workplace Analytics. If you want to skip gathering those properties, use this switch. The optional properties are Country, City, Title, Office.|
|InjectThrottling|	switch|	This switch is used only for debugging. We recommend that you omit this switch because its use hinders performance.|

## Resulting organizational-data file schema

After you run this script, the resulting schema in the organizational-data file contains the following attributes, or column names (with the exception of LevelDesignation; see its description). The attributes in bold are required attributes. 

|Column name |Type | Description |
|------|-----------|----------|
| **PersonID** 	|String	|A user's primary SMTP address.|
| **EffectiveDate**	|String	|The start date on which this information is current. It must be able to be cast to the .NET type _datetime_.|
| **ManagerID**	|String	|The ID of the user’s manager, assigned in Azure AD. This must be in valid SMTP format.|
| **Organization**	|String|	The user's Azure AD Department field.|
| **LevelDesignation**	|String	|The script generates this required column as it creates the organizational data file. However, the script cannot access actual level designations, so it assigns the default value \_\_novalue\_\_ in each row in the file. To make LevelDesignation usable by analysts, you must edit the organizational data file and update the value of this attribute for each user before you upload the file. (Alternatively, use the Title property. See [Optional properties](#optional-properties).)|
|NumDirectReports	|Integer	|The number of direct reports, found in Azure AD, of this user.|
|SupervisorIndicator	|String	|Indicates whether this user manages no people, is a manager, or is a manager of managers.|
|ManagerIsMissingFlag	|String	|If there was no manager found in AD or if an error occurred during lookup, this value is TRUE; otherwise it is FALSE.|

## Optional properties

If you use the SkipOptionalProperties switch when you run the Generate-WpaOrganizationFile.ps1 script, the following optional properties are left out of the resulting data file. If you omit this switch, these properties are included in the data file. 

|Column name &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp;   |Type | Description |
|------|-----------|----------|
| City  	| String | The City property is obtained in a call to Get-MsolUser. |
|Country |	String	| The Country property is obtained in a call to Get-MsolUser. |
|Title	| String |	The Title property is obtained in a call to Get-MsolUser. It corresponds to a user’s job title. If this property is populated in the organizational data file, analysts can use it in their queries, in place of or in addition to the LevelDesignation property. (See [Resulting organizational-data file schema](#resulting-organizational-data-file-schema).) |
| Office	| String	| The Office property is obtained in a call to Get-MsolUser. |

