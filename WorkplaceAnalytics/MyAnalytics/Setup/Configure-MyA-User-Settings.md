---
# Metadata Sample
# required metadata

title: Configure MyAnalytics user settings
description: Configure MyAnalytics settings for new users. 
author: buntus
ms.author: paul9955
ms.date: 12/17/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: mya
---

Use the following options to configure MyAnalytics for each user in your organization. You can change these default behaviors for any user by setting the *PrivacyMode* parameter:

PrivacyMode   | Licensed user  | Unlicensed user
------------- | -------------  | ---------------
Opt-in (This is the default setting)        | <ul><li>Office 365 data is used for aggregated information shown to licensed users.</li><li>Personal dashboard is available.</li><li>User can opt-out.</li></ul>  | <ul><li>Office 365 data is used for aggregated information shown to licensed users.</li><li>Admins can opt-out unlicensed users through the admin PowerShell. <!--Unlicensed users can opt-out through the Feature settings menu. THIS MIGHT BE POSSIBLE THROUGH DELVE. PENDING WORD FROM PATB/MATHEW/PETER BERGEN ABOUT WHETHER THIS IS POSSIBLE IN THE DELVE FEATURE SETTINGS PAGE --></li></ul>  
Opt-out    | <ul><li>Office 365 data is not used for aggregated information shown to licensed users.</li><li> Personal dashboard is not available.</li><li>User can opt-in through the Feature settings menu.</li></ul>   |  <ul><li> Office 365 data is not used for aggregated information shown to licensed users.</li></ul>
Excluded   |<ul><li> Office 365 data is not used for aggregated information shown to licensed users.</li><li>Dashboard is available.</li><li>User cannot opt-in through the Feature settings menu.</li></ul>  |<ul><li> Office 365 data is not used for aggregated information shown to licensed users.</li></ul>

> [!Note]  
> * _All users_ in your organization, whether or not they have MyAnalytics licenses issued to them, are opted-in.
> * _Licensed users_ will have MyAnalytics automatically enabled for them after a license is assigned to them. If you want a licensed user to be opted out by default, which would give them the choice to opt-in, you can change the value of the PrivacyMode for that user to “Opt-out.” (You can change this value for one user or for multiple users at once by using PowerShell. To make a change for multiple users, admins iterate through a list of users in a single PowerShell script.) 

### Use Exchange Online PowerShell to run cmdlets to set or get MyAnalytics user settings

For more information about the Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289(v=exchg.160).aspx).

### Privacy Mode

PrivacyMode has three different settings: Excluded, Opt-in, and Opt-out, as described in the following table. 

Configure MyAnalytics settings for a user with the following cmdlet:

```powershell
Set-UserAnalyticsConfig –Identity <string> [PrivacyMode <string[]>]
```

Parameter   |   Required   |   Description   | Default value
----------  |  ----------  |  -------------- | -------------
Identity   |   Yes   | User ID for the current user as stored in Azure Active Directory (AAD).   |   -
PrivacyMode   |   Yes   | <ul><li>__Excluded:__ MyAnalytics will not use the current user’s data to compute derived statistics for other users. The current user will not be able to change this from the Feature settings menu in MyAnalytics, but will still be able to see personalized statistics in their MyAnalytics dashboards.</li><li>__Opt-out:__ MyAnalytics will not use the current user’s data to compute derived statistics for other users. The current user will not see statistics in MyAnalytics, but can change this from the Feature settings menu and choose to opt-in.</li><li>__Opt-in:__ MyAnalytics will use the current user’s data to compute derived statistics for other users. The current user will see statistics in MyAnalytics, and can change this from the Feature settings menu to opt out.</li></ul>|  Opt-in

Get MyAnalytics settings for a user with the following cmdlet:

```powershell
Get-UserAnalyticsConfig –Identity <string>
```

Parameter   |   Required   |    Description    |   Default value
----------- | ------------ |  ---------------  | ---------------
Identity    |  Yes         |    User ID for the current user as stored in AAD  | -
