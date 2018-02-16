---
# Metadata Sample
# required metadata

title: Configure MyAnalytics user settings
description: Set up user settings. Part of the MyA setup checklist. 
author: rodonahu
ms.author: rodonahu, v-pascha
ms.date: 1/19/2018
ms.topic: get-started-article
ms.prod: wpa
---

# Configure MyAnalytics user settings

You can use the following options to configure MyAnalytics for each user in your organization.

You can decide to change these default behaviors for any user by setting the *PrivacyMode* parameter:

PrivacyMode   | Licensed user   | Unlicensed user
------------- | -------------   | ---------------
Opt-in (This is the default setting)        | * Office 365 data is used for aggregated information shown to licensed users * Personal dashboard is available * User cannot opt-out. Only the admin can opt the user out.  | * Office 365 data is used for aggregated information shown to licensed users * User can opt-out through the Feature settings menu                         
Opt-out    | * Office 365 data is not used for aggregated information shown to licensed users * Personal dashboard is not available * User can opt-in through the Feature settings menu   | * Office 365 data is not used for aggregated information shown to licensed users
Excluded   | * Office 365 data is not used for aggregated information shown to licensed users * Dashboard is available * User can not opt-in through the Feature settings menu  | * Office 365 data is not used for aggregated information shown to licensed users

**Notes:** The following applies when you use the default settings :

* All users in your organization, whether or not they have MyAnalytics licenses issued to them, are opted-in.
* Licensed users will have MyAnalytics automatically enabled for them after a license is assigned to them. If you want your licensed users to instead have the choice to opt-in, you must change the default settings.

### Use Exchange Online PowerShell to run cmdlets to set or get MyAnalytics user settings

For more information about the Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289(v=exchg.160).aspx).

### Privacy Mode

PrivacyMode has three different settings: Excluded, Opted-in, and Opted-out, as described below. Configure MyAnalytics settings for a user with the following cmdlet:

***
Set-UserAnalyticsConfig –Identity <<string>string> [PrivacyMode <string[]>]
***

Parameter   |   Required   |   Description   | Default value
----------  |  ----------  |  -------------- | -------------
Identity   |   Yes   | User ID for the current user as stored in Azure Active Directory (AAD).   |   -
PrivacyMode   |   Yes   | * Excluded: MyAnalytics will not use the current user’s data to compute derived statistics for other users. The current user will not be able to change this from the Feature settings menu in MyAnalytics, but will still be able to see personalized statistics in their MyAnalytics dashboards. * Opt-out: MyAnalytics will not use the current user’s data to compute derived statistics for other users. The current user will not see statistics in MyAnalytics, but can change this from the Feature settings menu and choose to opt-in. * Opt-in: MyAnalytics will use the current user’s data to compute derived statistics for other users. The current user will see statistics in MyAnalytics, and can change this from the Feature settings menu to opt out.  |  Opt-in

Get MyAnalytics settings for a user with the following cmdlet:

***
Get-UserAnalyticsConfig –Identity <<string>string>
***

Parameter   |   Required   |    Description    |   Default value
----------- | ------------ |  ---------------  | ---------------
Identity    |  Yes         |    User ID for the current user as stored in AAD  | -
