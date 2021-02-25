---

title: Leadership insights dashboard
description: Leaders use this dashboard to learn about their relationships with team members
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: priority 
ms.prod: Mya

---

# Leadership

_**Applies to:** The Leadership page is currently in preview status. It is in the process of rolling out to all MyAnalytics users who are assigned as people managers in Azure AD<!-- REMOVING (12/4/2020) FOR NOW. REINSTATE PERHAPS IN JANUARY 2021.  or in Workplace Analytics*-->._

If you're a people manager, the MyAnalytics Leadership page gives you insights on your relationships with team members that can help you boost team productivity, wellbeing, and engagement. 

### Who can see this page 

You have access to this page only if you have team members assigned to you in Azure Active Directory<!-- REMOVING (12/4/2020) FOR NOW. REINSTATE PERHAPS IN JANUARY 2021.  or in Workplace Analytics*-->. Contact your Microsoft 365 administrator if you are a people manager but do not see the Leadership page in MyAnalytics. 

### A note on data privacy 

All of the information shown on this page is derived from the manager's personal Exchange Online mailbox. Managers do not see any incremental information from team members' mailboxes that would allow them to track a given team members' activities. For example: a manager can use this page to see if they've sent an email to a team member after hours, but they cannot determine whether the team member opened that email. More information is available in the MyAnalytics [Privacy guide for admins](../overview/privacy-guide.md#assistance-for-people-managers). 

## Leadership insights

The Leadership page offers the following insights:

* [1:1 time](#11-time) 
* [Quiet hours impact](#quiet-hours-impact)
* [Team meeting habits](#team-meeting-habits)

### 1:1 time 

As a people manager, it's likely that one of your many responsibilities is coaching team members to help them build the skills they need for their role. One of the simplest coaching tools you have at your disposal is 1:1 time. [Research by Microsoft](https://insights.office.com/productivity/what-great-managers-do-daily/) has shown that people who get consistent 1:1 time with their manager are more engaged and view the manager's leadership more favorably. 

MyAnalytics helps you track your 1:1 trends and ensure that you have regular 1:1 time scheduled with each team member: 

![Coaching: 1:1 time](../../Images/mya/use/leadership-one-on-one.png)

#### How 1:1 time is calculated 

Any meeting on your calendar that includes only you and your team member counts as a 1:1. If the calendar invitation also has a meeting room assigned, it still counts as a 1:1. 

If you directly call your team member over Teams or Skype for Business outside of a scheduled 1:1 meeting, it does not count as 1:1 time. 

### Quiet hours impact 

[Research by Microsoft](https://insights.office.com/productivity/multitask-meetings-team-will/) has shown that when managers work after hours, team members take that as a signal that they need to be 'on' too; in one study, every hour that people managers spent after hours translated to 20 minutes of additional direct report time spent after hours. While some team members may actually prefer to do some of their work outside traditional 9-5 working hours, others may struggle to mentally disconnect and recharge for the next day if they receive a late-night message from their manager. 

MyAnalytics helps you understand whether you might be impacting team members outside their typical working hours: 

![Wellbeing](../../Images/mya/use/leadership-quiet-hours.png)

#### How quiet-hours impact is calculated 

Quiet-hours impact is based on collaboration activity that you initiate with team members more than one hour outside of their working hours as configured in Outlook. This activity includes emails and chats you send as well as meetings and calls you hold. For example, if a team member's configured working hours are 9 AM to 5 PM and you arrange a meeting with them from 6 to 7 PM, this counts as quiet-hours impact. 

For emails and chats, it is not necessary for the team member to have actually read or responded to the message you sent; the insight is simply intended to draw your awareness to activities that might have impacted team members after hours. 

### Team meeting habits 

Managers are role models when it comes to collaboration habits; team members tend to mimic their manager's behavior. [One study by Microsoft](https://insights.office.com/productivity/multitask-meetings-team-will/) found, for example, that managers who multitask in meetings (defined as reading or sending emails during a scheduled meeting) are more than two times as likely to have team members who also multitask in meetings. 

MyAnalytics helps you track your habits in meetings with team members so that you can be sure to set the right standard: 

![Collaboration](../../Images/mya/use/leadership-team-meetings.png)

#### How team meetings habits are calculated 

A 'team meeting' is any scheduled meeting on your calendar that includes you and at least one of your team members (including 1:1 meetings). The 'habits' shown in this section are defined as follows: 

* **<=1 hour:** team meetings that you scheduled that were no longer than one hour. 

* **No overlap with other meetings:** team meetings that you scheduled or were invited to that did not overlap with other meetings on your calendar. 

* **Didn't multitask:** team meetings that you scheduled or were invited to during which you did not read or send emails or chats. 

* **RSVP'd:** team meetings to which you were invited but did not explicitly accept (note that the denominator here excludes meetings that you declined). 

* **Joined on time:** online team meetings (over a Teams or Skype for Business link) that you scheduled or were invited to and joined within a few minutes of the scheduled start time. 

## Confirming your team  

When you first visit the Leadership page, you are asked to confirm your team members. The initial list of team members you see is derived from Azure Active Directory or from Workplace Analytics*. If you make any changes, they will apply only to your MyAnalytics experience (including the [Insights Outlook add-in](add-in.md)) and will not be synchronized back to Azure AD or to Workplace Analytics*. 

![Confirm your team](../../Images/mya/use/leadership-confirm.png)

If your team list or job function changes, you can select the **Edit team** link at the top of the Leadership page or visit **Configurations** to add/remove team members or to indicate that you are no longer a manager.

> [!Note] 
> If you indicate that you're not a manager, you will not be able to turn the Leadership page back on for yourself in the future. 

### To open Configurations

1. Go to myanalytics.microsoft.com to open your personal MyAnalytics dashboard.

2. In the left navigation pane, select **Config settings**. 

   ![Configurations](../../Images/mya/use/leadership-config.png)

## Leadership tips 

**When you hold 1:1s, don’t make them all about business.** Use the time to learn about the team member as a person and to find areas of common interest outside of work. 

**Build a broad internal network.** [Research by Microsoft](https://insights.office.com/productivity/what-great-managers-do-daily/) has found that managers with relatively large internal networks receive higher team engagement scores, and their team members tend to have larger networks as well.

**Help team members prioritize tasks.** [Research by Microsoft](https://insights.office.com/workplace-analytics/the-new-manager-11-nurturing-employee-resiliency-during-disruption-and-change/) has shown that people who receive prioritization support from managers are better able to maintain productivity levels without working longer hours.

> [!Note]
> The Workplace Analytics organizational hierarchy is used for a tenant only if **Insights and plans** is turned **On** for that tenant in the [Manager settings](../../use/manager-settings.md) of Workplace Analytics.

<!-- For now, we cannot use these links, so keeping them safe here: 

**Focus on team members' strengths.** According to [Gallup](https://www.gallup.com/services/182138/state-american-manager.aspx), people who say their manager focuses on their strengths are 16 times more likely to report being engaged with their work. 

**Help team members prioritize tasks.** Research by [Microsoft](https://insights.office.com/workplace-analytics/the-new-manager-11-nurturing-employee-resiliency-during-disruption-and-change/) has shown that people who receive prioritization support from managers are better able to maintain productivity levels without working longer hours. 

 -->