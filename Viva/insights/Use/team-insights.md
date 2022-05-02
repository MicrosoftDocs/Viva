---
title: Team insights in Viva Insights
description: Learn about the Team insights page in Microsoft Viva Insights that shows managers their team collaboration patterns
author: madehmer
ms.author: loreenl
ms.topic: article
ms.localizationpriority: medium 
ms.collection: 
- m365initiative-viva-insights 
- viva-insights-manager
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Team insights

As a manager or team lead, Microsoft Viva Insights shows you insights to learn how your habits impact your team and suggestions to improve and foster team culture.

**To view team insights**: Go to [insights.viva.office.com](https://insights.viva.office.com)

![Team insights in Viva Insights.](../images/wpa/use/team-insights-2.png)

## Data privacy

All of the information shown on this page is derived from a manager's personal Exchange Online mailbox. Managers do not see any incremental information from team members' mailboxes that would allow them to track team member activities. For example, a manager can use this page to see if they've sent an email to a team member after hours, but they cannot determine whether the team member opened the email.

When data is processed for team insights, Microsoft protects employee privacy and fully complies with local regulations, such as the General Data Protection Regulation (GDPR) the same as for personal insights. For information about data privacy and GDPR compliance in Viva Insights, see [Privacy guide](../personal/teams/viva-teams-app-privacy.md).

## Admin tasks

**Team insights** are available to teams who have a Microsoft Viva Insights license with an applicable [service plan](../personal/overview/plans-environments.md). Ask your admin about licensing and to install and set up the Viva Insights app in Teams for the organization. See [Admin tasks](../personal/teams/viva-teams-app-admin-tasks.md) for details.

## Set up your team

As a manager or team lead, you can create a team and view insights about them within Viva Insights. With the exception of **Group insights**, the team insights you see are based on data that's processed from within your own mailbox for only you to see. When you select or confirm your current team members for the first time, the initial list of team members you see is derived from Azure Active Directory. After this initial setup, you can add and remove team members at any time through **Config settings**.

>[!Note]
>After you make changes, the automatic sync from your organization’s directory will stop and you will be responsible for keeping the list up to date.

## Recommendations and actions

As a manager, you often have a hectic schedule, which makes it tough to stay in close contact with your team. Viva Insights brings together all the information you need to stay caught up and respond quickly to important requests, such as:

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
>When you add a member to your team this week, your impact on the new member's quiet hours are reflected in next week's data.

### Team meeting habits

Managers are role models when it comes to collaboration habits; team members tend to mimic their manager's behavior. [One study by Microsoft](https://insights.office.com/productivity/multitask-meetings-team-will/) found, for example, that managers who multitask in meetings (defined as reading or sending emails during a scheduled meeting) are more than two times as likely to have team members who also multitask in meetings.

#### How team meetings habits are calculated

A 'team meeting' is any scheduled meeting on your calendar that includes you and at least one of your team members (including 1:1 meetings). The 'habits' shown in this section are defined as follows:

* **<=1 hour** - Team meetings that you scheduled that were no longer than one hour.
* **No overlap with other meetings:** team meetings that you scheduled or were invited to that did not overlap with other meetings on your calendar.
* **Didn't multitask** - Team meetings that you scheduled or were invited to during which you did not read or send emails or chats.
* **RSVP'd** - Team meetings to which you were invited but did not explicitly accept (note that the denominator here excludes meetings that you declined).
* **Joined on time** - Online team meetings (over a Teams or Skype for Business link) that you scheduled or were invited to and joined within a few minutes of the scheduled start time.

## Group insights

As a qualifying manager, you'll see a top insight with a **Learn more** link to see more in-depth data about your team's employee experience and effectiveness within Viva Insights in Teams. This section is only available to those who are set up as a manager and meet the minimum-group requirements. <!--See [Group insights](group-insights.md) for details.-->

>[!Note]
>When you add a member to your team this week, those changes are reflected in next week's data.

## Briefing and digest emails

As a team manager or lead, you'll also see additional information and suggestions in your Viva digest email and Briefing emails about your team. For details, see [Viva digest emails](../personal/use/email-digests-3.md) and [Catch up with your team](../personal/Briefing/be-manager.md).

## Related topics

* [Personal insights in Viva Insights](../personal/MyA-landing-page.md)
