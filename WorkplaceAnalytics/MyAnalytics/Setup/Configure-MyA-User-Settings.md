---
# Metadata Sample
# required metadata

title: Configure MyAnalytics user settings
description: Configure MyAnalytics settings for new users. 
author: paul9955
ms.author: paul9955
ms.date: 03/25/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: mya
---

You can configure MyAnalytics (change its default behavior) for users in your organization by setting the *PrivacyMode* parameter. For information about the values of PrivacyMode, see [PrivacyMode options](#privacymode-options). 

To set this parameter for one user or for many users, see the following:  

 * [Set PrivacyMode for one user](#set-privacymode-for-one-user) 
 * [Set PrivacyMode for multiple users](#set-privacymode-for-multiple-users)

## PrivacyMode options

PrivacyMode   | Licensed user  | Unlicensed user
------------- | -------------  | ---------------
Opt-in (This is the default setting)        | <ul><li>Office 365 data is used for aggregated information shown to licensed users.</li><li>Personal dashboard is available.</li><li>User can opt-out.</li></ul>  | <ul><li>Office 365 data is used for aggregated information shown to licensed users.</li><li>Admins can opt-out unlicensed users through the admin PowerShell. </li></ul>  
Opt-out    | <ul><li>Office 365 data is not used for aggregated information shown to licensed users.</li><li> Personal dashboard is not available.</li><li>User can opt-in through the Feature settings menu.</li></ul>   |  <ul><li> Office 365 data is not used for aggregated information shown to licensed users.</li></ul>
Excluded   |<ul><li> Office 365 data is not used for aggregated information shown to licensed users.</li><li>Dashboard is available.</li><li>User cannot opt-in through the Feature settings menu.</li></ul>  |<ul><li> Office 365 data is not used for aggregated information shown to licensed users.</li></ul>

> [!Note]  
> * _Licensed users_ have MyAnalytics automatically enabled for them after a license is assigned to them. 
> * _All users_ in your organization, whether or not they have MyAnalytics licenses issued to them, are opted-in. If you want a licensed user to be opted _out_ by default, which would give them the choice to opt-in, change the value of the PrivacyMode parameter for that user to "Opt-out." 

## Set PrivacyMode for one user 
Configure MyAnalytics settings for a user with the following PowerShell cmdlet:

```powershell
Set-UserAnalyticsConfig –Identity <string> [PrivacyMode <string[]>]
```

Parameter   |   Required   |   Description   | Default value
----------  |  ----------  |  -------------- | -------------
Identity   |   Yes   | User ID for the current user as stored in Azure Active Directory (AAD).   |   -
PrivacyMode   |   Yes   | <ul><li>__Excluded:__ MyAnalytics will not use the current user's data to compute derived statistics for other users. The current user will not be able to change this from the **Feature settings** menu in MyAnalytics, but will still be able to see personalized statistics in their MyAnalytics dashboard and Outlook add-in.</li><li>__Opt-out:__ MyAnalytics will not use the current user's data to compute derived statistics for other users. The current user will not see statistics in MyAnalytics, but can change this from the Feature settings menu and choose to opt-in.</li><li>__Opt-in:__ MyAnalytics will use the current user's data to compute derived statistics for other users. The current user will see statistics in MyAnalytics, and can change this from the Feature settings menu to opt out.</li></ul>|  Opt-in
  
### Get settings 
Get MyAnalytics settings for a user with the following cmdlet:

```powershell
Get-UserAnalyticsConfig –Identity <string>
```

Parameter   |   Required   |    Description    |   Default value
----------- | ------------ |  ---------------  | ---------------
Identity    |  Yes         |    User ID for the current user as stored in AAD  | - 

## Set PrivacyMode for multiple users

You can use PowerShell to change the value of PrivacyMode for multiple users at once. To do this, run a PowerShell script that iterates through the users, changing the value one user at a time. Follow these steps:

1. Create a comma-separated value (.csv) text file that contains the UserPrincipalName field and the addresses of the users you want to configure. For example:

   ![csv file contents](../../images/mya/setup/csv-contents-privacymode.png)

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
3. Run the resulting commands at the PowerShell command prompt.

This PowerShell command block does the following:
 * Displays the user principal name of each user.
 * Sets the specified privacy mode for each user.
 * Creates a .csv file with all the users that were processed and shows their status.

### Related topics

For more information about the Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289(v=exchg.160).aspx).
