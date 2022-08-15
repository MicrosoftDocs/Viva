---
ROBOTS: NOINDEX,NOFOLLOW
title: Effective meetings in Viva Insights  
description: Effective meetings in Microsoft Viva Insights
author: madehmer
ms.author: v-lilyolason
ms.topic: article
localization_priority: normal 
ms.collection: viva-insights-personal
ms.service: viva
ms.subservice: viva-insights
manager: helayne
audience: user

---

# Effective meetings

*This experience is only available through private preview at this time.*

The journey to transforming an organization’s meeting culture starts with measuring how people are doing in their meetings. Microsoft Viva Insights can help you you improve your meeting effectiveness, build a feedback culture within your team and company by using meeting effectiveness surveys.

If you're opted in, Viva Insights will automatically send meeting participants a survey asking for feedback about your meetings. This feedback is aggregated into a meeting rating in Effective meetings. You’ll also see personalized insights about what you’re doing well and opportunities to make any improvements.

This feedback is designed to help you improve your individual meeting habits over time, as well as your team and company’s collective meeting habits.

![Effective meeting surveys](images/e-meetings.png)

## Privacy by design

The Meeting effectiveness surveys are only sent for scheduled meetings that have five or more participants (including the meeting organizer). Providing meeting feedback is optional for all participants.

As the meeting organizer, you’ll only see aggregated results in Viva Insights. You will not see who sent what suggestions within the aggregated feedback.

![Meeting survey example](images/meeting-survey.png)

## Opt in or out of surveys

You can do the following to opt in or out of getting feedback about your meetings.

1. In the Viva Insights app, select **Settings**.
2. For **Meeting effectiveness surveys**, select to turn the setting **On** or **Off**, and then select **Save**.

   ![Meeting feedback setting](images/meeting-feedback.png)

## Admin controls

As the admin, you can configure the meeting effectiveness surveys for your organization at the [user](#user-level-configuration) or [tenant level](#tenant-level-configuration). You can set the default state for all users in your tenant as opted in or opted out in the Microsoft 365 admin center, or you can enable or disable the survey for a specific user or multiple users with PowerShell.

## Prerequisites

Confirm the following before configuring access:

* **Admin role** - You must have a Global admin or an Exchange Online admin role to configure users for meeting effectiveness surveys in the Microsoft 365 admin center. To configure individual users through PowerShell, you must have an Exchange Online admin, a Global admin, or an Insights admin role.
* **Understand data privacy** - See the [Privacy guide](./viva-teams-app-privacy.md) to understand how privacy is built into meeting effectiveness surveys and to learn what you can configure to address your organization's specific privacy requirements.

## User-level configuration

As the admin, you can use the [Exchange Online PowerShell V2](https://docs.microsoft.com/powershell/module/exchange/set-vivainsightssettings) module to set access [for one user](#set-access-for-one-user) or [for multiple users](#set-access-for-multiple-users) for meeting effectiveness surveys.

### Set access for one user

To enable or disable meeting effectiveness surveys for a specific user, use the Exchange Online PowerShell V2 module and the following command line, where you replace **roy@contoso.com** with your applicable username and organization:

```powershell
Set-VivaInsightsSettings -Identity roy@contoso.onmicrosoft.com -Enabled $false -Feature MeetingEffectivenessSurvey
```

* If you set the Enabled parameter to **$false**, the meeting effectiveness surveys will be **Off** for that user. The user will not be able to override this setting or opt-in to the meeting effectiveness surveys.
* If you set the Enabled parameter to **$true**, the meeting effectiveness surveys will be **On** for that user. Users can then opt-out from Viva Insights. If no action occurs, this setting applies by default.

>[!Note]
>When Enabled is set as $true, people who had previously opted out will continue to be opted out and will not receive any surveys until they opt back in through their Viva Insights app.

### Set access for multiple users

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

>[!Note]
>Individuals can opt out or back in at any time within their personal Viva Insights app. After the admin changes the survey setting in the admin center, it will take up to 24 hours for the new setting change to take effect.

## Tenant-level configuration

As the admin, use the following steps to change the setting for meeting effectiveness surveys at the tenant level. This setting is enabled by default, so that all users will receive the surveys.

Users can opt out individually from within their Viva Insights app settings. If you opt out of the meeting effectiveness surveys at the tenant level, people in your organization will not receive the surveys, but individuals can override this tenant-level setting. To completely prevent a person from receiving the surveys, you need to disable the surveys for that user with PowerShell.

### To configure access for a tenant

1. Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal).
2. Make sure you're using the new admin center. To do this, if the switch in the upper right of the page reads **Try the new admin center**, select it so that it reads **The new admin center**.
3. In the left pane, expand **Settings**, and then select **Org Settings**.
4. Under **Org Settings**, select **Viva Insights**.
5. Select or deselect the checkbox for **Meeting effectiveness surveys**, and then select **Save changes**. If you deselect the checkbox, all users in your organization will not receive the surveys, including all those who were receiving the surveys. However, individuals can explicitly opt-in again within their Viva Insights app.

## Related topics

[Microsoft Viva Insights overview](viva-teams-app.md)
