---
# Metadata Sample
# required metadata

title: Configure MyAnalytics user settings
description: Set user settings. These are part of the MyA setup checklist. 
author: rodonahu
ms.author: v-pascha
ms.date: 01/19/2018
ms.topic: get-started-article
ms.prod: wpa
---

## Configure user settings

Use the following options to configure MyAnalytics for each user in your organization. You can change these default behaviors for any user by setting the *PrivacyMode* parameter:

PrivacyMode   | Licensed user  | Unlicensed user
------------- | -------------  | ---------------
Opt-in (This is the default setting)        | <ul><li>Office 365 data is used for aggregated information shown to licensed users.</li><li>Personal dashboard is available.</li><li>User cannot opt-out. Only the admin can opt the user out.</li></ul>  | <ul><li>Office 365 data is used for aggregated information shown to licensed users.</li><li>User can opt-out through the Feature settings menu.</li></ul>  
Opt-out    | <ul><li>Office 365 data is not used for aggregated information shown to licensed users.</li><li> Personal dashboard is not available.</li><li>User can opt-in through the Feature settings menu.</li></ul>   |  <ul><li> Office 365 data is not used for aggregated information shown to licensed users.</li></ul>
Excluded   |<ul><li> Office 365 data is not used for aggregated information shown to licensed users.</li><li>Dashboard is available.</li><li>User cannot opt-in through the Feature settings menu.</li></ul>  |<ul><li> Office 365 data is not used for aggregated information shown to licensed users.</li></ul>

> [!Note] 
> The following applies when you use the default settings: 
>  
> * _All users_ in your organization, whether or not they have MyAnalytics licenses issued to them, are opted-in.
> * _Licensed users_ will have MyAnalytics automatically enabled for them after a license is assigned to them. If you want your licensed users to instead have the choice to opt-in, you must change the default settings. 

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
