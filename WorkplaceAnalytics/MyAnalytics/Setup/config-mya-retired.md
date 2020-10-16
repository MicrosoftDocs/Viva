---

title: MyAnalytics configuration for Office 365 administrators
description: Configuration options that Office 365 administrators can make for MyAnalytics users
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: Mya
---

# Configure access at the user level

**Role:** Office 365 admins

> [!Note] 
> This topic describes the use of the PowerShell cmdlets [Get-UserAnalyticsConfig](https://docs.microsoft.com/powershell/module/exchange/get-useranalyticsconfig?view=exchange-ps) and [Set-UserAnalyticsConfig](https://docs.microsoft.com/powershell/module/exchange/set-useranalyticsconfig?view=exchange-ps). By January 25, 2021, these cmdlets will be retired, and replaced by the new cmdlets [Get-MyAnalyticsFeatureConfig](https://docs.microsoft.com/powershell/module/exchange/get-myanalyticsfeatureconfig?view=exchange-ps) and [Set-MyAnalyticsFeatureConfig](https://docs.microsoft.com/powershell/module/exchange/set-myanalyticsfeatureconfig?view=exchange-ps), respectively. Please be sure to update your workflow and scripts to use the new cmdlets (as described in [Configure MyAnalytics](configure-myanalytics.md)) by that date.

Use the information in this section to configure MyAnalytics access for individual users in your organization. At this level, you can opt-out the user completely, which would turn off all MyAnalytics functionality for that user. However, the user can choose to opt back in. <!--To remove this choice from the user so that they cannot opt back in, you remove their MyAnalytics service plan. -->

You can configure MyAnalytics (change its default behavior) for users in your organization by setting the *PrivacyMode* parameter. For information about the values of PrivacyMode, see [User configuration settings](#user-configuration-settings).

You can set this parameter for one or many users:

* [Set MyAnalytics access for one user](#set-myanalytics-access-for-one-user)
* [Set MyAnalytics access for multiple users](#set-myanalytics-access-for-multiple-users)

### User configuration settings

PrivacyMode parameter  | Licensed user  | Unlicensed user
------------- | -------------  | ---------------
Opt-in (default setting)        | <ul><li>Office 365 data is used for aggregated information shown to licensed users</li><li>Dashboard is available</li><li>User can opt out</li></ul>  | <ul><li>Office 365 data is used for aggregated information shown to licensed users</li><li>Admins can opt out unlicensed users through the admin PowerShell </li></ul>  
Opt-out    | <ul><li>Office 365 data is not used for aggregated information shown to licensed users</li><li> Dashboard is not available</li><li>User can opt in through the Feature settings menu</li></ul>   |  <ul><li> Office 365 data is not used for aggregated information shown to licensed users.</li></ul> |

> [!Important] 
> The Excluded value of PrivacyMode is being retired. Users whose privacy mode was previously set to Excluded will now be set to Opt-out.

### Set MyAnalytics access for one user

Configure MyAnalytics access settings for a user with the following PowerShell cmdlet:

```powershell
Set-UserAnalyticsConfig –Identity <string> [PrivacyMode <string[]>]
```

Parameter   |   Required   |   Description   | Default value
----------  |  ----------  |  -------------- | -------------
Identity   |   Yes   | User ID for the current user as stored in Azure Active Directory (AAD)   |   --
PrivacyMode   |   Yes   | <ul><li>**Opt-out**: MyAnalytics won't use the user's data to compute derived statistics for other users. The user won't see statistics in MyAnalytics, but can choose to opt in from the Feature settings menu.</li><li>**Opt-in**: MyAnalytics uses the user's data to compute derived statistics for other users. The user can see statistics in MyAnalytics, but can choose to opt out from the Feature settings menu.</li></ul>|  Opt-in

> [!Important]
> The Excluded value of PrivacyMode is being retired. Users whose privacy mode was previously set to Excluded will now be set to Opt-out.
  
### Confirm MyAnalytics access for a user

Use the following to confirm if a user has access to MyAnalytics (the value for PrivacyMode):

```powershell
Get-UserAnalyticsConfig –Identity <string>
```

Parameter   |   Required   |    Description    |   Default value
----------- | ------------ |  ---------------  | ---------------
Identity    |  Yes         |    User ID for the current user as stored in AAD  | - 

### Set MyAnalytics access for multiple users

Use the following steps in the [Exchange Online PowerShell V2 module](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell-v2/exchange-online-powershell-v2) to change access to MyAnalytics (the value of PrivacyMode) for multiple users by running a PowerShell script that iterates through the users, changing the value one user at a time.

1. Create a comma-separated value (.csv) text file that contains the UserPrincipalName field of the users you want to configure. For example:

   ```
   UserPrincipalName
   ClaudeL@contoso.onmicrosoft.com
   LynneB@contoso.onmicrosoft.com
   ShawnM@contoso.onmicrosoft.com
   ```

2. Specify the location of the input .csv file, the output .csv file, and the value of PrivacyMode that you want to set for each user:

   ```powershell
   $inFileName="<path and file name of the input .csv file that contains the users, example: C:\admin\Users2License..csv>"
   $outFileName="<path and file name of the output .csv file that records the results, example: C:\admin\Users2License-Done..csv>"
   $privacyMode = "Opt-in"

   $users=Import-Csv $inFileName
   ForEach ($user in $users)
   {
   $user.Userprincipalname
   $upn=$user.UserPrincipalName

   Set-UserAnalyticsConfig –Identity $upn -PrivacyMode $privacyMode
   Get-UserAnalyticsConfig –Identity $upn | Export-Csv $outFileName
   }
   ```

3. Run the resulting commands at the Exchange Online PowerShell V2 module command prompt. For more information about the module, see [Exchange Online PowerShell V2 module](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell-v2/exchange-online-powershell-v2).

This PowerShell script:

* Displays the user principal name for each user.
* Sets the specified privacy mode for each user.
* Creates a .csv file with all the users that were processed and shows their status.

