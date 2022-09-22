---

ROBOTS: NOINDEX,NOFOLLOW
title: Use a script to prepare organizational data
description: How to use a script to prepare data from your organization to upload for Viva Insights 
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Use a script to prepare organizational data

## Introduction

This script can help you to onboard people for the first time or create a new file to update organizational data. It uses the [Mainline service](/powershell/azure/active-directory/overview) to find their mailboxes within your organization. It then uses your Azure Active Directory data to create an organizational-data file. A Viva Insights Administrator can upload this file as is or edit it first. For more information, see [Prepare organizational data](/viva/insights/prepare-organizational-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json), [Upload organizational data (first upload)](/viva/insights/setup/upload-organizational-data-1st?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json), and [Upload organizational data (subsequent uploads)](/viva/insights/setup/upload-organizational-data2?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

## Prerequisites

This script requires the following elements. If you need help with these prerequisites, contact Support. See [Get support](../overview/getting-support.md) for details or send email to <wpasetup@microsoft.com>.

* **PowerShell version 5.0 or higher** - To check the version of PowerShell on your computer:

   1. In Windows, select **Start**, type **PowerShell**, and press **Enter**.
   2. In the Windows PowerShell window, type **$PSVersionTable** and press **Enter**. Verify that the value listed for “PSVersion” is at least 5.0. For values less than 5.0, see: [Installing Windows PowerShell](/powershell/scripting/windows-powershell/install/installing-windows-powershell).

    For information about using PowerShell on the Mac, see [Installing PowerShell on macOS](/powershell/scripting/install/installing-powershell-core-on-macos).

    When you install the following modules – AAD and MSOnline – you first need to start PowerShell as an administrator:

    ![Run as administrator.](../images/wpa/setup/run-as-admin.png)

* **The Azure Active Directory module** - For installation instructions, see [Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2). To install the AAD module, use the PowerShell command:

   ```PowerShell
   Install-Module AzureAD
   ```

* **The Microsoft Online module** - This service is used to determine which accounts are real people with mailboxes. For information about installing MSOnline, see [Azure ActiveDirectory (MSOnline)](/powershell/azure/active-directory/install-msonlinev1). To install the MSOnline module, use the PowerShell cmdlet:

   ```PowerShell
   Install-Module MSOnline
   ```

## Run the script

1. Download the latest version of the script at [Organizational data script](https://aka.ms/WpaOrgFileFromAad).
2. Extract the downloaded script zip file and note its folder location.
3. Open a new instance of Windows PowerShell with administrator privileges.
4. In PowerShell, navigate to the folder that contains the extracted script files.

    _Example:_

    cd c:\users\localuser\desktop\orgfilecreation

5. In PowerShell, run the following commands to make sure that the downloaded files are unblocked from execution:
  
    _Run:_

    ```PowerShell
    Unblock-File .\Generate-WpaOrganizationFile.ps1
    ```

    _Run:_

    ```PowerShell
    Unblock-File .\helper.psm1
    ```

6. The script is now ready to run. If you're creating an organizational data file for the first time and your organization requires multi-factor authentication, run the script with the default options:

    _Run:_

    ```PowerShell
    .\Generate-WpaOrganizationFile.ps1 -RequireCredentialPrompt
    ```

   As it runs, the script prompts you twice for credentials, once to authenticate to the Azure Active Directory service, and once to authenticate to the MSOnline service.

## Examples

The following example command lines create an organizational data file in different ways, with the inclusion of different data.

### Example 1

 This example does **not** gather the optional properties City, Country, Office, and Title from Active Directory:

 ```PowerShell
 .\Generate-WpaOrganizationFile.ps1 -RequireCredentialPrompt -SkipOptionalProperties
 ```

### Example 2

This example sets the EffectiveDate field in the resulting organizational data file to the current day:

```PowerShell
.\Generate-WpaOrganizationFile.ps1 -RequireCredentialPrompt -EffectiveDateOption Delta
```

>[!Note]
>If you do not use this option, the effective date will default to a fixed date in the past, such as 01/01/1970.

### Example 3

Use the parameters in the following example if your organization doesn't enforce multi-factor authentication and you want to create PSCredential objects and pass them into the script so that the script can run unattended:

```PowerShell
.\Generate-WpaOrganizationFile.ps1 -MSOLCredential $MsolCred -AzureADCredential $AzureADcred
```

## Parameter reference

You can use the following parameters with the Generate-WpaOrganizationFile.ps1 script.

|Parameter |Type | Description |
|------|-----------|----------|
|MSOLCredential |pscredential |The credential of a person who can authenticate with the MSOnline service and execute the _Get-MsolUser_ cmdlet.  |
|AzureADCredential |pscredential |The credential of a person who can authenticate with the Azure AD service and execute read-only cmdlets such as _Get-AzureADUser_.|
|RequireCredentialPrompt |switch| If your organization's IT requires multifactor authentication, this switch lets you authenticate by prompting you for credentials. It uses the built-in prompts that are provided by the _Connect-AzureAD_ and _Connect-MsolService_ cmdlets.|
| EffectiveDateOption| string | Used to determine the EffectiveDate.<ul><li>Select the **InitialPull** option if you're generating an organizational data file for the first time for Viva Insights.</li><li>Use the **Delta** option if you're creating a later upload of organizational data.</li></ul> |
|SkipOptionalProperties| switch | As part of information gathering, there are extra properties available via Azure AD and MSOnline that are not required by Viva Insights. If you want to skip gathering those properties, use this switch. The optional properties are Country, City, Title, Office.|
|InjectThrottling| switch | This switch is used only for debugging. We recommend that you omit this switch because its use hinders performance.|

## Resulting organizational-data file schema

After you run this script, the resulting schema in the organizational-data file contains the following attributes, or column names (except **LevelDesignation**. See its description in the following table). The attributes that are shown in bold are required attributes.

| Column name          | Type   | Description |
| -------------------- | ------ | ----------- |
| **PersonID**         | String | A person's primary SMTP address.|
| **EffectiveDate**    | String | The start date on which this information is current. It must be able to be cast to the .NET type _datetime_.|
| **ManagerID**        | String | The ID of the person’s manager, assigned in Azure AD. This must be in valid SMTP format.|
| **Organization**     | String | The person's Azure AD Department field.|
| **LevelDesignation** | String | The script generates this optionally required column as it creates the organizational data file. However, the script can't access actual level designations, so it assigns the default value \_\_novalue\_\_ in each row in the file. To make **LevelDesignation** usable by analysts, you must edit the organizational data file and update the value of this attribute for each person before you upload the file. (Optionally, use the Title property instead. See [Optional properties](#optional-properties).) |
| NumDirectReports     | Integer | The number of direct reports, found in Azure AD, of this person.|
| SupervisorIndicator  | String  | Indicates whether the person doesn't manage other people, is a manager, or is a manager of managers.|
| ManagerIsMissingFlag | String  | If there was no manager found in AD or if an error occurred during lookup, this value is _TRUE_; otherwise it is _FALSE_.|

## Optional properties

If you use the SkipOptionalProperties switch when you run the Generate-WpaOrganizationFile.ps1 script, the following optional properties are left out of the resulting data file. If you omit this switch, these properties are included in the data file.

| Column name &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; |Type | Description |
| ------- | -----------|----------|
| City    | String | The City property is obtained in a call to _Get-MsolUser_. |
| Country | String | The Country property is obtained in a call to _Get-MsolUser_. |
| Title   | String | The Title property is obtained in a call to _Get-MsolUser_. It corresponds to a person’s job title. If this property is populated in the organizational data file, analysts can use it in their queries, in place of or in addition to the **LevelDesignation** property. (See [Resulting organizational-data file schema](#resulting-organizational-data-file-schema).) |
| Office  | String | The Office property is obtained in a call to _Get-MsolUser_. |

## Related topics

#### To set up prerequisite software

* [Installing Windows PowerShell](/powershell/scripting/windows-powershell/install/installing-windows-powershell?view=powershell-7&preserve-view=true)
* [Installing PowerShell on macOS](/powershell/scripting/install/installing-powershell-core-on-macos?view=powershell-7&preserve-view=true)
* [MSOnline service](/powershell/azure/active-directory/overview?view=azureadps-1.0&preserve-view=true)
* [Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2?view=azureadps-2.0&preserve-view=true)
* [Get support](../overview/getting-support.md)

#### About organizational data

* [Prepare organizational data](/viva/insights/setup/prepare-organizational-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)
* [Upload organizational data (first upload)](/viva/insights/setup/upload-organizational-data-1st?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)
* [Upload organizational data (subsequent uploads)](/viva/insights/setup/upload-organizational-data2?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)
