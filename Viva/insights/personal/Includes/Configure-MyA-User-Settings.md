---

title: Configure Viva Insights user settings
description: Configure Viva Insights settings for new users
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.service: viva
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
ms.subservice: viva-insights
---

You can configure Viva Insights (change its default behavior) for users in your organization by setting the *PrivacyMode* parameter. For information about the values of PrivacyMode, see [User configuration settings](#user-configuration-settings).

You can set this parameter for one user or for many users:  

* [Set Viva Insights access for multiple users](#set-Viva Insights-access-for-multiple-users)
* [Set Viva Insights access for one user](#set-Viva Insights-access-for-one-user)

### User configuration settings

PrivacyMode parameter  | Licensed user  | Unlicensed user
------------- | -------------  | ---------------
Opt-in (This is the default setting)        | <ul><li>Microsoft 365 data is used for aggregated information shown to licensed users.</li><li>Personal dashboard is available.</li><li>User can opt-out.</li></ul>  | <ul><li>Microsoft 365 data is used for aggregated information shown to licensed users.</li><li>Admins can opt-out unlicensed users through the admin PowerShell. </li></ul>  
Opt-out    | <ul><li>Microsoft 365 data is not used for aggregated information shown to licensed users.</li><li> Personal dashboard is not available.</li><li>User can opt-in through the Feature settings menu.</li></ul>   |  <ul><li> Microsoft 365 data is not used for aggregated information shown to licensed users.</li></ul>
Excluded   |<ul><li> Microsoft 365 data is not used for aggregated information shown to licensed users.</li><li>Dashboard is available.</li><li>User cannot opt-in through the Feature settings menu.</li></ul>  |<ul><li> Do not specify _Excluded_ for unlicensed users. Instead, specify _Opt-out_.</li></ul>

>[!Note]  
>
>* _Licensed users_ have Viva Insights automatically enabled for them after a license is assigned to them.
>* _All users_ in your organization, whether or not they have Viva Insights licenses issued to them, are opted-in. If you want a licensed user to be opted _out_ by default, which would give them the choice to opt-in, change the value of the PrivacyMode parameter for that user to "Opt-out."

### Set Viva Insights access for multiple users

You can use PowerShell to change the access to Viva Insights (the value of PrivacyMode) for multiple users at once. To do this, run a PowerShell script that iterates through the users, changing the value one user at a time. Follow these steps:

1. Create a comma-separated value (.csv) text file that contains the UserPrincipalName field and the addresses of the users you want to configure. For example:

```
UserPrincipalName,UsageLocation
ClaudeL@contoso.onmicrosoft.com,FR
LynneB@contoso.onmicrosoft.com,US
ShawnM@contoso.onmicrosoft.com,US
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
3. Run the resulting commands at the PowerShell command prompt. For more information about the Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).

This PowerShell command block does the following:

 * Displays the user principal name of each user.
 * Sets the specified privacy mode for each user.
 * Creates a .csv file with all the users that were processed and shows their status.

### Set Viva Insights access for one user

Configure Viva Insights access settings for a user with the following PowerShell cmdlet:

```powershell
Set-UserAnalyticsConfig –Identity <string> [PrivacyMode <string[]>]
```

Parameter   |   Required   |   Description   | Default value
----------  |  ----------  |  -------------- | -------------
Identity   |   Yes   | User ID for the current user as stored in Azure Active Directory (AD).   |   -
PrivacyMode   |   Yes   | <ul><li>__Excluded:__ Viva Insights will not use the current user's data to compute derived statistics for other users. The current user will not be able to change this from the **Feature settings** menu in Viva Insights, but will still be able to see personalized statistics in their Viva Insights dashboard and the Insights Outlook add-in.</li><li>__Opt-out:__ Viva Insights will not use the current user's data to compute derived statistics for other users. The current user will not see statistics in Viva Insights, but can change this from the Feature settings menu and choose to opt-in.</li><li>__Opt-in:__ Viva Insights will use the current user's data to compute derived statistics for other users. The current user will see statistics in Viva Insights, and can change this from the Feature settings menu to opt out.</li></ul>|  Opt-in
  
### Determine Viva Insights access for one user

To determine the Viva Insights access (the value of PrivacyMode) for one user, use the following cmdlet:

```powershell
Get-UserAnalyticsConfig –Identity <string>
```

Parameter   |   Required   |    Description    |   Default value
----------- | ------------ |  ---------------  | ---------------
Identity    |  Yes         |    User ID for the current user as stored in AAD  | -