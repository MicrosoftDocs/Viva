---

title: My team in Viva Insights
description: Learn about the My team page in Microsoft Viva Insights in Teams that shows managers their habits and how that impact their team
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-manager
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# My team

As a manager or team lead, you can see insights and suggested actions based on your personal habits in **My team** within the Microsoft Viva Insights app in Microsoft Teams. You can also learn how your habits impact your team while getting suggestions on how to foster team culture.

Viva Insights uses Azure Active Directory (AD) for your initial team, which you can then edit by selecting **Go to settings** in the **Your team** section. See [Admin tasks](#admin-tasks) to learn what's required to see the **My team** page.

![My team page in Viva Insights in Teams.](../images/wpa/use/myteam-2.png)

## Data privacy

When data is processed for Group insights, Microsoft protects employee privacy and fully complies with local regulations, such as the General Data Protection Regulation (GDPR) the same as for personal insights. For information about data privacy and GDPR compliance in Viva Insights, see [Privacy guide](../personal/teams/viva-teams-app-privacy.md).

## Admin tasks

**My team** and its features (as described on this page) are available to managers or team leads who have a Microsoft Viva Insights license with an applicable [service plan](../personal/overview/plans-environments.md). Ask your admin about licensing and to install and set up the Viva Insights app in Teams for the organization. See [Admin tasks](../personal/teams/viva-teams-app-admin-tasks.md) for details.

## Install, pin, and configure the app

Your setup tasks for **My team** are the same as for [Personal insights](../personal/teams/viva-teams-app.md) in the Viva Insights app. See the following to install, pin, and configure the app in Teams:

* [Install and pin the app](../personal/teams/viva-teams-app-install.md)
* [Configure the app](../personal/teams/viva-teams-app-settings.md)

## View My team

1. In the left navigation bar in Teams, select **Viva Insights**.
2. In **Viva Insights Home**, you’ll see an insight about your team. To learn more about an insight, select **Explore more**. You can also use any of the other features on this page, such as **Reflect**, **Praise**, **Stay connected**, and **Protect time**. For more information, see [Viva Insights Home](/insights/viva-insights-home).
3. Alternatively, select **My team** in Viva Insights to see key recommendations, actions, and reflections relating to your team.

## Disable or enable My team

1. In the left navigation bar in Teams, select **Viva Insights** > **My team**.
2. Select the **ellipsis** (**...**) icon > **Settings** at the top right.
3. In **Choose your team members**:

   * To disable it, select **I don't lead a team**.
   * To enable it, select **I lead a team**, select your team members, and then select **Save changes**.

## Manage your team

As a licensed Viva Insights user, you can create a team and view insights about them within the Viva Insights app. With the exception of [Group insights](#group-insights), the team insights you see are based on data that's processed from within your own mailbox for only you to see.

The first time you open **My team**, you are prompted to select or confirm your current team members. The initial list of team members you see is derived from Azure AD. After this initial setup, you can add and remove team members at any time by selecting **Go to settings** in the **Your team** section.

## Recommendations and actions

You'll see a rotating recommendation at the top of your **My team** page that's based on recent activity. You'll also see options to stay connected and send praise in the **Actions for you** section.

In **Reflect**, you might see one or more suggestions to improve your own personal habits as a team member. For example, if you select **Explore more** in [Your habits](#your-habits), you'll see more details about who you collaborated with. It might also suggest you reconnect with members who you haven't collaborated with lately.

You might also see suggestions for your team in the [Plans](#plans) section.

## Your habits

As a manager, you often have a hectic schedule, which makes it tough to stay in close contact with each team member. Viva Insights brings together all the information you need to stay caught up and respond quickly to important requests, such as the following.

* Act on tasks you promised to get done or that team members asked you to complete
* Review important emails and documents from team members that you haven’t read yet
* Schedule [1:1 time](#11-time) with your team members (or reschedule if a conflict comes up)
* View and consider changes for [quiet hours impact](#quiet-hours-impact) and [team meeting habits](#team-meeting-habits)

### 1:1 time

As a people manager, it's likely that one of your many responsibilities is coaching team members to help them build the skills they need for their role. One of the simplest coaching tools you have at your disposal is 1:1 time. [Research by Microsoft](https://insights.office.com/productivity/what-great-managers-do-daily/) has shown that people who get consistent 1:1 time with their manager are more engaged and view the manager's leadership more favorably.

#### How 1:1 time is calculated

Any meeting on your calendar that includes only you and your team member counts as a 1:1. If the calendar invitation also has a meeting room assigned, it still counts as a 1:1.

If you directly call your team member over Teams or Skype for Business outside of a scheduled 1:1 meeting, it does not count as 1:1 time.

### Quiet hours impact

[Research by Microsoft](https://insights.office.com/productivity/multitask-meetings-team-will/) has shown that when managers work after hours, team members take that as a signal that they need to be 'on' too; in one study, every hour that people managers spent after hours translated to 20 minutes of additional direct report time spent after hours. While some team members may actually prefer to do some of their work outside traditional 9-5 working hours, others may struggle to mentally disconnect and recharge for the next day if they receive a late-night message from their manager.

#### How quiet-hours impact is calculated

Quiet-hours impact is based on collaboration activity that you initiate with team members more than one hour outside of their working hours as configured in Outlook. This activity includes emails and chats you send as well as meetings and calls you hold. For example, if a team member's configured working hours are 9 AM to 5 PM and you arrange a meeting with them from 6 to 7 PM, this counts as quiet-hours impact.

For emails and chats, it is not necessary for the team member to have actually read or responded to the message you sent; the insight is simply intended to draw your awareness to activities that might have impacted team members after hours.

>[!Note]
>When you add a member to your team list, your impact on the new member's quiet hours are reflected in next week's data.

### Team meeting habits

Managers are role models when it comes to collaboration habits; team members tend to mimic their manager's behavior. [One study by Microsoft](https://insights.office.com/productivity/multitask-meetings-team-will/) found, for example, that managers who multitask in meetings (defined as reading or sending emails during a scheduled meeting) are more than two times as likely to have team members who also multitask in meetings.

#### How team meetings habits are calculated

A 'team meeting' is any scheduled meeting on your calendar that includes you and at least one of your team members (including 1:1 meetings). The 'habits' shown in this section are defined as follows:

* **<=1 hour** - Team meetings that you scheduled that were no longer than one hour.
* **No overlap with other meetings:** team meetings that you scheduled or were invited to that did not overlap with other meetings on your calendar.
* **Didn't multitask** - Team meetings that you scheduled or were invited to during which you did not read or send emails or chats.
* **RSVP'd** - Team meetings to which you were invited but did not explicitly accept (note that the denominator here excludes meetings that you declined).
* **Joined on time** - Online team meetings (over a Teams or Skype for Business link) that you scheduled or were invited to and joined within a few minutes of the scheduled start time.

>[!Note]
>When you add a member to your team this week, those changes are reflected in next week's data.

## Group insights

Group insights are only available to qualifying managers who are set up as a manager in Workplace Analytics and meet the minimum-group requirements. For more details, see [Group insights](Group-insights.md).

## Plans

This section will also show suggestions for you to consider, such as scheduling a [no-meeting day for your team](#no-meeting-day-for-your-team) or a [shared focus plan](#shared-focus-plan).

### No-meeting day for your team

For **Schedule a no-meeting day for your team** in the **Plans** section, you can select **Get started** to create a plan that schedules a shared recurring time that everyone in your team can use to focus without interruptions. You can select the start date, frequency, status, and meeting title.

![Start a no-meeting day in My team.](../images/wpa/use/no-meeting-day.png)

You're then prompted to confirm the team members to invite, an optional note for the email invitation, and then after you confirm the details, select **Send invitation**. Viva Insights will then invite your team to participate in the plan.

The day before a scheduled no-meeting day, your team members are prompted by Viva Insights to prepare for the no-meeting day by rescheduling or canceling any conflicting meetings:

![Prompt before a no-meeting day.](../images/wpa/use/no-meeting-prompt.png)

They can select **Review schedule** within the notice to help with this task.

![Review schedule before a no-meeting day.](../images/wpa/use/no-meeting-review.png)
<!-->
### Shared focus plan

An enrolled manager can invite their team to book daily, uninterrupted focus time to get their work done. A shared focus plan helps your team build a shared productivity habit. See [Shared focus plan](shared-focus-plan.md) for details.-->

## Briefing and digest emails

As a team manager or lead, you'll also see additional information and suggestions about your team in your Briefing and digest emails from Microsoft Viva. For details, see [digest emails](../personal/Use/email-digests-3.md) and [Catch up with your team](../personal/Briefing/be-manager.md).

>[!Note]
>As you use the Viva Insights app, you can provide feedback about the app to Microsoft. To learn how, see **Q10** in [My team FAQ](my-team-faq.md).

## Related topics

* [Personal insights in Viva Insights](../personal/teams/viva-teams-app.md)
* [Viva Insights introduction](viva-insights-intro.md)
