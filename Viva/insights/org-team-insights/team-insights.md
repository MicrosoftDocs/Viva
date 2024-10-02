---
ms.date: 09/30/2024
title: Team insights
description: Learn about team insights and where to find them in Viva Insights in Teams and on the web
author: zachminers
ms.author: v-zachminers
ms.topic: how-to
ms.localizationpriority: medium 
ms.collection: 
- viva-insights-manager
- viva-insights-leader
- essentials-manage
ms.service: viva-insights
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin, user

---

# Team insights

*Applies to: people with a premium Viva Insights subscription and one or more people directly reporting to them*

Find insights and suggested actions based on your personal habits as a manager throughout the Microsoft Viva Insights app in Teams and on the web. In addition to providing information about how teams are built, this article gives a quick overview about insights you'll find about team meeting habits on the [Productivity](../personal/teams/productivity.md) tab.

Throughout this document, we'll link to more detailed information.

## About team data and data privacy

Team insights use collaboration data from Microsoft 365. Depending on your setup, team insights might also use organizational data that your admin has uploaded in the advanced insights app, or that's available from Microsoft Entra ID, to determine who should be included in your "team."  

With team insights, you can't see individual team members' personal collaboration habits. Team insights are generated entirely from activity data from only a user’s own account, and computed from their email, meetings, chats, and calls. All of the same privacy protections and considerations apply to team insights as to other personal insights. 

Microsoft protects employee privacy and fully complies with local regulations, such as the General Data Protection Regulation (GDPR), the same as for personal insights. For information about data privacy and GDPR compliance in Viva Insights, refer to the [Privacy guide](../personal/teams/privacy.md).

## Permissions and app setup

### Admin tasks

Team insights and its features (as described on this page) are available users who have a [Viva Insights subscription with an applicable service plan](../personal/overview/plans-environments.md). Ask your admin about licensing and to install and set up the Viva Insights app for the organization. Refer to [Install the Viva Insights app in Teams](../advanced/setup-maint/teams-admin-setup.md) for details.

### Install, pin, and configure the app

Refer to these articles to install, pin, and configure the app in Teams:

* [Install and pin the app](../personal/teams/viva-teams-app-install.md)
* [Configure the app](../personal/teams/settings.md)

## About teams

### How teams are built

Viva Insights automatically builds teams based on organizational data uploaded or connected to the advanced insights app. If your organization uses Microsoft Entra ID to populate Viva Insights—which is the default setting—then we use that directory’s information to build your team. However, if your admin uploads an HR file to the advanced insights app, we use the data provided in that file to create your team. Specifically: 
* The HR file influences the team composition only for users who have entries in the HR data file.
* For other users who do not appear in the HR file, we fall back to using Microsoft Entra ID.


Your team only includes people reporting directly to you as presented in Microsoft Entra ID or the file your admin uploads. This structure means three things:

* To keep teams accurate, your organization needs to regularly update Microsoft Entra ID or upload new HR files.
* If you don’t have at least one person reporting directly to you, as presented in the organizational data file, you won’t have access to Team insights.
* Because teams come directly from organizational data, you’re not able to edit members. People who don't have direct reports won't be able to access team insights.

>[!Note]
>When your direct-reports list changes, your team meeting habits will reflect these changes in next week’s data.

### How to turn on or turn off team insights

To turn on or off team insights:

1. Select the ellipsis (...) icon > **Settings** at the top right.

1. Select **Team insights** on the left pane.

1. To:
    * Turn off team insights, select **Opt out**.
    * To turn on team insights, select **Opt in**.

1. Select **Save changes**.

## Available insights

### Team meeting habits

As a manager, you're a role model when it comes to collaboration habits, especially in meetings. Team members tend to mimic their manager's behavior. One study by Microsoft found, for example, that managers who multitask in meetings (defined as reading or sending emails during a scheduled meeting) are more than two times as likely to have team members who also multitask in meetings.

You'll find insights about your team meeting habits on the **Productivity** tab. Refer to [Meeting habits](../personal/teams/meeting-habits.md) to learn which habits we calculate and how we calculate them.

### Shared plans

To create healthy team norms, you and your team might consider using shared plans. You can find and start [shared no-meeting day](../personal/teams/shared-no-meeting-day.md) and focus plans on the **Wellbeing** tab. To start a [shared meeting plan](../personal/teams/shared-meeting-plan.md), visit the **Productivity** tab.

### 1:1 time with direct reports

>[!Note]
>This card provides insights regardless of your minimum group size setting, even if you only have one direct report. This card's insights are based on data from Microsoft Entra ID, and do *not* reflect data from any organizational data file uploads.

Learn when your last 1:1 was and when the next one is scheduled. You can also easily schedule 1:1 time if there isn’t an upcoming block.

### Quiet hours impact

Learn about your collaboration activities with your team during their non-working hours. For example, these insights let you know how often you had meetings or sent chats and emails during your team's non-working hours. [Learn more about quiet time in Viva Insights](https://support.microsoft.com/topic/quiet-time-in-viva-insights-ec70888d-8840-4f20-9819-af6bfc17e143).

## FAQ

**Can a manager have access to both personal insights for the manager and organizational insights for the manager?**

Yes.

**How are direct reports determined?**

Depending on your setup, team insights might also use organizational data that your admin has uploaded in the advanced insights app, or that's available from Azure Active Directory, to determine who should be included in your "team."