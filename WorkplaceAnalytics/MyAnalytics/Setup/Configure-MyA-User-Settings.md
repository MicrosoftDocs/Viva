---
# Metadata Sample
# required metadata

title: Configure MyAnalytics user settings
description: Configure MyAnalytics settings for new users. 
author: paul9955
ms.author: paul9955
ms.date: 12/17/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: mya
---

Use the following options to configure MyAnalytics for each user in your organization. You can change these default behaviors for any user by setting the *PrivacyMode* parameter:

PrivacyMode   | Licensed user  | Unlicensed user
------------- | -------------  | ---------------
Opt-in (This is the default setting)        | <ul><li>Office 365 data is used for aggregated information shown to licensed users.</li><li>Personal dashboard is available.</li><li>User can opt-out.</li></ul>  | <ul><li>Office 365 data is used for aggregated information shown to licensed users.</li><li>Admins can opt-out unlicensed users through the admin PowerShell. </li></ul>  
Opt-out    | <ul><li>Office 365 data is not used for aggregated information shown to licensed users.</li><li> Personal dashboard is not available.</li><li>User can opt-in through the Feature settings menu.</li></ul>   |  <ul><li> Office 365 data is not used for aggregated information shown to licensed users.</li></ul>
Excluded   |<ul><li> Office 365 data is not used for aggregated information shown to licensed users.</li><li>Dashboard is available.</li><li>User cannot opt-in through the Feature settings menu.</li></ul>  |<ul><li> Office 365 data is not used for aggregated information shown to licensed users.</li></ul>

> [!Note]  
> * _Licensed users_ have MyAnalytics automatically enabled for them after a license is assigned to them. 
> * _All users_ in your organization, whether or not they have MyAnalytics licenses issued to them, are opted-in. If you want a licensed user to be opted _out_ by default, which would give them the choice to opt-in, change the value of the PrivacyMode parameter for that user to "Opt-out." 

### Setting PrivacyMode

An admin can change the value of PrivacyMode for one user or for multiple users at once, by using PowerShell. To do this for multiple users, run a PowerShell script that iterates through the users, changing the value one user at a time. 

For more information about the Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289(v=exchg.160).aspx).

#### Make settings 
Configure MyAnalytics settings for a user with the following cmdlet:

```powershell
Set-UserAnalyticsConfig –Identity <string> [PrivacyMode <string[]>]
```

Parameter   |   Required   |   Description   | Default value
----------  |  ----------  |  -------------- | -------------
Identity   |   Yes   | User ID for the current user as stored in Azure Active Directory (AAD).   |   -
PrivacyMode   |   Yes   | <ul><li>__Excluded:__ MyAnalytics will not use the current user's data to compute derived statistics for other users. The current user will not be able to change this from the **Feature settings** menu in MyAnalytics, but will still be able to see personalized statistics in their MyAnalytics dashboards.</li><li>__Opt-out:__ MyAnalytics will not use the current user's data to compute derived statistics for other users. The current user will not see statistics in MyAnalytics, but can change this from the Feature settings menu and choose to opt-in.</li><li>__Opt-in:__ MyAnalytics will use the current user's data to compute derived statistics for other users. The current user will see statistics in MyAnalytics, and can change this from the Feature settings menu to opt out.</li></ul>|  Opt-in

> [!Note]  
> After you grant a MyAnalytics license to a user, they have access to the Outlook add-in, regardless of the value that you have assigned to the PrivacyMode parameter. For example, even after you opt-out a licensed user by setting PrivacyMode to **Excluded**, the following holds true:   
> * The user retains access to the Outlook add-in. 
> * MyAnalytics is not uninstalled, but the user loses access to the other surfaces of MyAnalytics (such as the dashboard).
> * They can still choose to opt back in to MyAnalytics.  

#### Get settings 
Get MyAnalytics settings for a user with the following cmdlet:

```powershell
Get-UserAnalyticsConfig –Identity <string>
```

Parameter   |   Required   |    Description    |   Default value
----------- | ------------ |  ---------------  | ---------------
Identity    |  Yes         |    User ID for the current user as stored in AAD  | -
