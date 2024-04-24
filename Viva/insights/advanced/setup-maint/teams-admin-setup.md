---
ms.date: 06/16/2023
title: Install the Viva Insights app in Teams
description: Install the Microsoft Viva Insights app available for Microsoft Teams
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.collection: 
- viva-insights-manager
- viva-insights-leader
- essentials-manage
ms.localizationpriority: medium 
ms.service: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Configure Teams app settings

![Teams service admin icon](../images/applies-to-teams-admin.png)*Applies to: Teams Service Administrator, Microsoft 365 global admin, and Exchange Online admin*

:::image type="content" source="../images/setup-teams-1.png" alt-text="Image alt text." lightbox="../../advanced/images/setup-teams-1.png":::

The Viva Insights app is automatically installed in Teams once the admin enables the app on managed apps. As a [Teams Service Administrator](/microsoftteams/using-admin-roles#teams-roles-and-capabilities), you can pin and manage access for the Microsoft Viva Insights app in Microsoft Teams for all the users or for specific groups in your organization [through custom policies](/microsoftteams/teams-app-setup-policies).

>[!Note]
>The steps in this document are optional. We talk about how to limit access to the app and automatically pin it for people in your organization.
>
>To pin or uninstall the app, users can follow the instructions in [Discover and pin the Viva Insights app](https://support.microsoft.com/topic/discover-and-pin-the-viva-insights-app-3b8db3ff-17b7-4d41-b2eb-f593530abfc7).

## Prerequisites

Before people in your organization can use the Viva Insights app, they need to have:

* Access to Microsoft Teams.
* An Exchange Online account.

## Limit access to the app

To limit who can access the app, follow these steps:

1. Confirm users have a [Viva Insights service plan](environment-requirements.md).
1. On the Viva Insights [admin page](https://admin.microsoft.com/Adminportal/Home?source=applauncher#/viva), select **Viva Insights**.
1. Under **Viva Insights in Microsoft 365**, select **Manage availability in the Teams admin center**.

    :::image type="content" source="../../images/mya/setup/mac-teams-admin1.png" alt-text="Screenshot that shows Manage availability in Teams admin center in the Viva Insights admin page.":::

1. Confirm that Viva Insights is turned on for your organization on the [Manage apps](/microsoftteams/manage-apps) page.
2. Create a custom app permission policy and assign it to those users. For details, see [Manage app permission](/microsoftteams/manage-apps) policies in Teams.

## Pin the app

In Teams, you can pin the Viva Insights app in the left app bar for all users in your organization. Learn how to pin apps in [Use app setup policies to pin and auto-install apps for users](/microsoftteams/teams-app-setup-policies#pin-apps).


Users can follow these steps to [Discover and pin the Viva Insights app](https://support.microsoft.com/topic/discover-and-pin-the-viva-insights-app-3b8db3ff-17b7-4d41-b2eb-f593530abfc7).

## Turn on and off specific features

### Turn off Headspace

When the Headspace feature is turned on, users can find it on the [Home](https://support.microsoft.com/topic/viva-insights-home-tab-6e7d28b2-6b0e-4367-9b52-1999a86eb391) page of Viva Insights. As an admin, you can turn off this feature by using PowerShell cmdlets.

The PowerShell commands for working with Viva Insights features are described in [Set-VivaInsightsSettings](/powershell/module/exchange/set-vivainsightssettings). To disable Headspace, see [Example 1](/powershell/module/exchange/set-vivainsightssettings).

### Configure meeting effectiveness surveys

As the admin, you can configure the meeting effectiveness surveys for your organization at the [user](#user-level-configuration) or [tenant level](#tenant-level-configuration). You can enable or disable the survey for a specific user or multiple users with PowerShell, or you can set the default state for all users in your tenant as opted in or opted out in the Microsoft 365 admin center.

#### Prerequisites

Confirm the following before configuring access:

* **Admin role** - You need to have a Global admin or an Exchange Online admin role to configure users for meeting effectiveness surveys in the Microsoft 365 admin center. To configure individual users through PowerShell, you need to have an Exchange Online admin, a Global admin, or an Insights admin role.
* **Understand data privacy** - See the [Privacy guide](../../personal/overview/privacy-guide-admins.md) to understand how privacy is built into meeting effectiveness surveys and to learn what you can configure to address your organization's specific privacy requirements.

#### Tenant-level configuration

As the admin, use the following steps to change the setting for meeting effectiveness surveys at the tenant level. This setting is enabled by default, so that all users will receive the surveys. Users can opt out individually from within their Viva Insights app settings.

>[!IMPORTANT] 
> If you opt out of the meeting effectiveness surveys at the tenant level, people in your organization will be opted-out by default from getting feedback on meetings they organize. However, individuals can override this tenant-level setting. To prevent a person from opting-in and and to disable the feature completely, you need to disable the surveys for that user with PowerShell, like we describe [below](#set-access-for-multiple-users).

##### To configure the default state for a tenant

1. On the Viva Insights [admin page](https://admin.microsoft.com/Adminportal/Home?source=applauncher#/viva), select **Viva Insights**.
1. Under **Viva Insights in Microsoft 365**, select **Manage settings for Viva Insights**.
   :::image type="content" source="../../images/mya/setup/manage-settings-insights.png" alt-text="Screenshot that shows Manage settings for Viva Insights in the Viva Insights admin page.":::
1. In the resulting pane, select or deselect the checkbox for **Meeting effectiveness surveys**, and then select **Save changes**. If you deselect the checkbox, *no user in your organization will receive the surveys*, including those who previously were receiving them. However, individuals can explicitly opt in again within their Viva Insights app.

   :::image type="content" source="../../personal/teams/images/meeting-effectiveness-surveys-admin.png" alt-text="Screenshot that shows the Viva Insights elements pane in the Viva Insights admin collection.":::


>[!Note]
>After you change the survey setting in the admin center, it will take up to 24 hours for the new setting change to take effect.

#### User-level configuration

As the admin, you can use the [Exchange Online PowerShell V2](/powershell/module/exchange/set-vivainsightssettings) module to set access [for one user](#set-access-for-one-user) or [for multiple users](#set-access-for-multiple-users) for meeting effectiveness surveys.

>[!Note]
>The following user-level configuration can only be modified when users have P1 licenses enabled for Viva Insights.

#### To configure survey sampling rate

As the admin, you can configure the percentage of meetings that get surveyed. The default sampling rate is 15%. You can configure this sampling rate to any value between 10% and 70% through the [Set-DefaultTenantMyAnalyticsFeatureConfig](/powershell/module/exchange/set-defaulttenantmyanalyticsfeatureconfig#example-3) PowerShell cmdlet. Run the following command and change the `-SamplingRate` value, which is set at `0.2` in this example:

```powershell
Set-DefaultTenantMyAnalyticsFeatureConfig -Feature Meeting-Effectiveness-Survey-Sampling-Rate -SamplingRate 0.2
```

##### Check a user's access

To check whether a user has access to features in Microsoft Viva Insights in Microsoft Teams, follow the directions in [Get-VivaInsightsSettings](/powershell/module/exchange/get-vivainsightssettings).

##### Set access for one user

To enable or disable meeting effectiveness surveys for a specific user, use the Exchange Online PowerShell V2 module and the following command line, where you replace **roy@contoso.com** with your applicable username and organization:

```powershell
Set-VivaInsightsSettings -Identity roy@contoso.onmicrosoft.com -Enabled $false -Feature MeetingEffectivenessSurvey
```

* If you set the Enabled parameter to `$false`, the meeting effectiveness surveys will be **Off** for that user. The user won't be able to override this setting or opt in to the meeting effectiveness surveys. In other words, you're completely disabling the feature.
* If you set the Enabled parameter to `$true`, the meeting effectiveness surveys will be **On** for that user. Users can then opt out from meeting effectiveness surveys. If no action occurs, this setting applies by default.

>[!Note]
>When Enabled is set as `$true`, people who had previously opted out will continue to be opted out and will not receive any surveys until they opt back in through their Viva Insights app.
>
>**Suggestions for you cards** (How your meetings succeeded and How your meetings can improve) derived from meeting metrics data (outside of surveys)  appear regardless of tenant- and user-level disablements.

##### Set access for multiple users

You can also enable or disable meeting effectiveness surveys for multiple users with a PowerShell script that iterates through the specified users, changing the value one user at a time.

Use the following script to:

* Create a .csv file with all users that were processed with their current status.
* List the user principal name for each user.
* Set the specified Enabled parameter for each user.

1. Create an input .csv text file that contains the **Identity** of the users you want to configure. For example:

   ```powershell
   Identity
   ClaudeL@contoso.com
   LynneB@contoso.com
   ShawnM@contoso.com
   ```

2. Specify the location of the input .csv file, the output .csv file, and the value of Enabled to $true or $false for each user:

   ```powershell
   $inFileName="<path and file name of the input .csv file that contains the users, for example: C:\admin\Users2Opt-in.csv>"
   $outFileName="<path and file name of the output .csv file that records the results, for example: C:\admin\Users2Opt-in-Done.csv>"
   $meetingEffectivenessSurveysMode = $true
   
   $users=Import-Csv $inFileName
   ForEach ($user in $users)
   {
   $user.identity
   $upn=$user.identity
   Set-VivaInsightsSettings –Identity $upn -Enabled $meetingEffectivenessSurveysMode -Feature MeetingEffectivenessSurvey
   }
   ```

3. Run the resulting commands at the [Exchange Online PowerShell V2](/powershell/module/exchange/set-vivainsightssettings) module command prompt.


#### Notification scenarios

People see different notifications and settings in their Viva Insights app in Teams or on the web, depending on which settings scenario you picked above.

**Scenario 1: You didn't change the default setting in the Microsoft admin center, and the meeting effectiveness survey feature is on for all people in your organization.**

The first time people in your organization use the Viva Insights app, they get a notification about meeting effectiveness surveys. On their **Settings > Effective meetings** page, the toggle for **Meeting effectiveness surveys** is switched on. If people want to opt out of the survey, they can switch the toggle off.

   :::image type="content" source="../../personal/teams/images/meeting-effectiveness-notification-on.png" alt-text="Screenshot that shows the notification for users who have the feature default-on.":::

   :::image type="content" source="../../personal/teams/images/settings-effective-meetings-toggle.png" alt-text="Screenshot that shows the Effective meetings tab in Settings with the Meeting effectiveness surveys toggle switched on.":::

**Scenario 2: In the Microsoft admin center, you set the meeting effectiveness survey feature to default-off.**

The first time people in your organization use the Viva Insights app, they get a notification asking whether they want to start using meeting effectiveness surveys. On their **Settings > Effective meetings** page, the toggle for **Meeting effectiveness surveys** is switched off. If people want to start using the surveys, they can switch the settings toggle on, or select **Get started** on the first-use notification.

   :::image type="content" source="../../personal/teams/images/meeting-effectiveness-notification-opt-in.png" alt-text="Screenshot that shows the opt-in notification for users who have the feature default-off.":::

**Scenario 3: You used a PowerShell cmdlet to disable access to the meeting effectiveness survey feature.**

People in your organization don't receive *any* notifications about meeting effectiveness surveys. When they go to their **Settings > Effective meetings** page in the Viva Insights app in Teams or on the web, they don't see a toggle to turn on or off the feature.


## Next steps

> [!div class="nextstepaction"]
> [Customize Viva Insights privacy settings](privacy-settings.md)

*Applies to: Insights Administrator*
