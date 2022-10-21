---
title: Effective meetings in Viva Insights  
description: Effective meetings in Microsoft Viva Insights
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
localization_priority: normal 
ms.collection: viva-insights-personal
ms.service: viva
ms.subservice: viva-insights
manager: anirudhbajaj
audience: user

---

# Effective meetings

*This experience is part of a rolling release set to complete in October 2022. It's available to users with a Viva Insights subscription. Refer to [Plans and environments](../Overview/plans-environments.md) for more information.*

## Meeting category insights

You can use **Meeting category insights** in **Effective meetings** to help understand how you’re allocating time across your Outlook meeting categories.
To set up Outlook meeting categories, refer to [Assign a color category to a calendar appointment, meeting, or event (microsoft.com)](https://support.microsoft.com/office/assign-a-color-category-to-a-calendar-appointment-meeting-or-event-750596d9-707d-4412-8c0e-7fdc0fc52527).
  
**Meeting category insights** shows you how many hours you’re spending in meetings, then breaks down the time you spend in each of your categories.

![Screenshot that shows the Meeting category insights page.](Images/meeting-category-insights.png)

You can customize what you see here. If you want to:

* Analyze a specific category, select it from the checklist to the left.

    ![Screenshot that shows one category selected.](Images/meeting-category-insights-customer-meetings.png)

* Pick a specific timeframe, use the dropdown menu in the top-right. You can choose from **Last 3 months**, **Last 4 weeks**, or **Next 4 weeks**.

    ![Screenshot that shows the time frame dropdown list.](Images/meeting-category-insights-time-frame.png)

>[!Important]
>If you haven’t categorized any meetings between the last three months and next four weeks, these insights won’t be available to you. However, you’ll have access to them after you categorize any meeting within this time period, as long as you have a Viva Insights subscription.
>
> When you make updates to your meeting categories in Teams or Outlook, it can take up to a day for those changes to appear in the **Effective meetings** tab.

## Meeting habits

>[!Note]
> This capability is currently available in the MyAnalytics dashboard, but it's coming to the Viva Insights app in Teams and on the web soon.

The **Meeting habits** section highlights your habits or practices in meetings you organized and accepted. Switch between the **Habits** and **Meetings** views by toggling the control above the graph/table.

* Use percentage data from the **Habits** view to understand how often you organize or attend meetings that apply certain habits. For example, you might notice that 81% of the online meetings you attend end on time. 

    ![Collaboration Meeting Habits View.](../teams/Images/meeting-effectiveness-habits.png)

* For details about all your meetings in the past four weeks, use the **Meetings** view.
    

    ![Collaboration Meeting List View.](../teams/Images/meeting-effectiveness-list-view.png)

    The **Meetings** view classifies meetings by using icons, which we describe in the following table:

   |Icon|Description |
   |--|---|
   |![recur icon.](../../Images/mya/use/recur-icon.png) |  This meeting is recurring |
   | ![check mark icon.](../../Images/mya/use/checkmark.png)| This meeting meets the requirement of the habit in the column header. For example, if the meeting started on time, you'd see a check under **On time**. |
   |![X icon.](../../Images/mya/use/x-icon.png) |This meeting doesn't meet the requirement of the habit in the column header. For example, if the meeting didn't start on time, you'd see an **X** under **On time**. |
   |![dash icon.](../../Images/mya/use/dash-icon.png) |Not applicable. The  habit in the column header doesn't apply to this meeting. For example, **On time** doesn't apply to a canceled meeting, so you'd see a dash instead of a check or an **X**. |

You can sort this table by selecting the column header.

### How meeting habits are calculated

Here's how we calculate the habits shown in this section:

* **<= 1 hour** – Meetings you organized that were one hour or shorter
* **Advanced notice** – Meeting invitations you sent with more than 24 hours' notice before the scheduled start time
* **Added a Teams link** – Meetings you organized that included a Teams link for remote attendees
* **During working hours** – Meetings you organized or accepted during your working hours
* **Ended on time** – Online meetings (on Microsoft Teams) that you ended within one minute of the scheduled end time
* **High attendance** – Meetings you organized or accepted that had a response rate over 50%
* **Joined on time** – Online meetings (on Microsoft Teams) you joined within five minutes of the scheduled start time
* **No overlap with other meetings** – Meetings that didn't overlap with other meetings on your calendar
* **RSVP'd to invite** – Meetings you were invited to and either accepted or declined (that is, you didn't leave your status as **Tentative**)
* **You didn't multitask** – Meetings where you didn't read or send emails or chats

### Meeting exclusions

These types of meetings are excluded from meeting metrics—that is, they don't factor into the habits you see in this section.

* Meetings that are 24 hours or longer, which include meetings marked as **All day** 
* Meetings marked as **Private**
* Meetings where you're the only participant, like when you block focus time in your calendar or set reminders
* Meetings with a **Show As** status set to one of these:
    * Free
    * Working Elsewhere
    * Tentative
    * Out of Office

>[!Note]
>Viva Insights counts double-booked meetings only one time for metric calculations. For example, if you have two meetings scheduled for 10:00 AM to 11:00 AM on the same day, Viva Insights counts this as only one hour of meeting time.

## Meeting effectiveness surveys

With meeting effectiveness surveys, you can view aggregated feedback from attendees on the meetings you organized. These surveys help you gain insight into what’s going well with your meetings, and what you could improve in future meetings, to promote a healthy meeting culture.

Surveys appear at the end of select Teams meetings with five or more participants. Here are the survey questions and response choices:

* **What made this meeting a success?**
    * Agenda
    * Focused discussions
    * Attendee participation
    * Clear next steps

* **What would've made it better?**
    * Agenda
    * Focused discussions
    * Attendee participation
    * Clear next steps

* **How effective was this meeting at achieving its business goals?**

    * A rating scale of one to five stars

![Screenshot that shows the feedback survey.](images/effective-meetings-share-feedback.png)

### Insights

As an organizer with a [Viva Insights subscription](https://www.microsoft.com/microsoft-viva/insights), you can see aggregated survey results in the Viva Insights app in Teams and on the web. These results include an aggregated view of star ratings and access to individual, anonymous feedback. The **Effective meetings** page also shows insights into how your meetings succeeded and how they could be improved.


:::image type ="content" source="images/effective-meetings-landing.png" alt-text="Screenshot that shows the effective meetings page." lightbox="images/effective-meetings-landing.png":::

### Settings

All users have meeting effectiveness surveys turned on by default. Admins can turn off surveys for their entire organization or [enable them](./viva-teams-app-admin-tasks.md#configure-meeting-effectiveness-surveys) for a specific set of users. You also can opt out of receiving feedback.

#### Opt in or out of surveys

To opt in or out of getting feedback about your meetings, follow these steps:

1. In the Viva Insights app, select **Settings**.
2. For **Meeting effectiveness surveys**, select to turn the setting **On** or **Off**, and then select **Save**. This setting defaults to **On**.

    ![Screenshot that shows Effective meeting settings.](images/meeting-effectiveness-settings.png)

### Privacy by design

The meeting effectiveness surveys are only sent for scheduled meetings that have five or more participants (including the meeting organizer). We also check whether the attendees who get those surveys stay in the meetings for at least five minutes. To help mitigate survey fatigue in survey participants, 10% of qualified meetings get the surveys. Providing meeting feedback is optional for all participants.

As the meeting organizer, you’ll only see aggregated results in Viva Insights. You won't see who sent what suggestions within the aggregated feedback.

### Admin controls

To configure meeting effectiveness surveys for your organization at the user or tenant level, refer to [Admin tasks](./viva-teams-app-admin-tasks.md#configure-meeting-effectiveness-surveys).

## Related topics

[Microsoft Viva Insights overview](viva-teams-app.md)
