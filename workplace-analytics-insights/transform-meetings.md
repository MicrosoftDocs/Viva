---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 10/06/2020
title: Transform meeting culture with Microsoft Viva Insights
description: Learn how to use the insights data to analyze and transform your organization's meeting culture
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.service: workplace-analytics
manager: scott.ruble
audience: Admin
---

# Transform meeting culture insights

*This experience is only available through private preview.*

Meetings are essential for collaboration, however unnecessary meetings and bad practices can harm engagement and limit productivity. Each of the behaviors listed show how your organization compares with others based on industry research and your specific organizational data.

![Transform meeting culture page.](./images/transform-meetings.png)

## Calculations

The following are the percentage insights, their underlying metrics, and a little about the calculations used for them.

![Transform meetings examine recurring meetings.](./images/transform-meetings-percent.png)

|Behavior |Percentage insight | Metrics |Calculations |
|---------|--------|--------------------|----------------------|
|Optimize meeting hours |Percentage of employees who spend a majority of their meeting time in long or large meetings |[Long meetings](glossary.md#long-meeting-define), [large meetings](glossary.md#large-meeting-define), [decision-making meetings](glossary.md#decision-making-meeting-define), and [meeting hours](metrics.md#meeting-hours-define) |Percentage of employees who spend a majority of their meeting hours in long meetings, which are more than one hour, or large meetings, which have more than eight attendees. This insight is calculated weekly and averaged for the entire time period. |
|Examine recurring meetings |Percentage of employees who spend a majority of their time in recurring meetings | [IsRecurring meeting filter](/viva/insights/tutorials/meeting-queries#add-metrics) and [meeting hours](metrics.md#meeting-hours-define) |Percentage of employees who spend more than 50 percent of their meeting hours in recurring meetings. This insight is calculated weekly and averaged for the entire time period. |
|Promote healthy meeting habits |Percentage of employees who significantly multitask in meetings |[Multitasking meeting hours](metrics.md#multitasking-meeting-hours-define) | Percentage of employees who spend more than 25 percent of their meetings hours multitasking. This insight is calculated weekly and then averaged for the entire time period. |

The following defines the organizational data shown in the visual behavioral insights.

![Transform meetings promote healthy meeting habits.](./images/transform-meetings-visual.png)

|Behavior |Visual insight | Definition |
|---------|--------|----------------------|
|Improve meeting quality |Meetings by duration and number of attendees |Uses [meeting hours](metrics.md#meeting-hours-define) to calculate the following percentages:<ul><li>**Large meetings** - Percentage of meetings that are larger than eight attendees but have a duration of less than one hour. </li><li>**Long meetings** - Percentage of meetings that are longer than one hour but have less than equal to eight attendees. </li><li>**Long and large meetings** - Percentage of meetings that have more than eight attendees and are longer than one hour. </li><li>**Decision-making meetings** - Percentage of meetings that have between two and eight attendees and are less than one hour in duration. </li>|
|Examine recurring meetings | Recurring vs. non-recurring meetings |Percentage of total meeting hours that are recurring and those that are non-recurring. These hours are summed for the entire time period and then the percentages are calculated. These calculations use the [meeting hours](metrics.md#meeting-hours-define) metric and the IsRecurring meeting filter.|
|Promote healthy meeting habits | Distribution of multitasking in meetings  | Percentage of employees based on their weekly [multitasking meeting hours](metrics.md#multitasking-meeting-hours-define). They are divided into those who spend between zero and one hour, one and five hours, and more than five hours multitasking in meetings. These percentages are calculated weekly and averaged for the entire time period. |

## Take action

In the **Take action** section for each insight, select **See your insights** to see the most effective actions you can do now to drive change toward better business outcomes in your organization.

You also might see one or more groups listed who are affected and would benefit the most from these recommendations, which are based on your organizational data and industry research.

## Best practices

This section describes why each of the following behaviors matter and the top best practices that can help transform meeting culture.

* [Optimize meeting hours](#optimize-meeting-hours)
* [Examine recurring meetings](#examine-recurring-meetings)
* [Promote healthy meeting habits](#promote-healthy-meeting-habits)

### Optimize meeting hours

Long and large meetings are costly and often considered a waste of time. Shorter meetings with fewer people can enhance individual and team performance.

The [condensed guide to running meetings](https://insights.office.com/collaboration/how-to-run-effective-meetings-and-stop-wasting-time/) explains a few new ideas that can help make your meetings more effective, such as if "you want people to have the opportunity to contribute, you need to limit attendance." Other ways to reduce meeting time:

* Use [Microsoft Teams channels](/microsoftteams/teams-channels-overview) as a way for team members to get questions answered and provide updates without the need for a meeting.  
* Encourage employees to politely say no to meetings that lack an agenda or are misaligned with priorities. The feedback will motivate organizers to plan better meetings.

For more best practices and change strategies, see [Best practices for meetings](/viva/insights/tutorials/gm-meetings).

### Examine recurring meetings

Recurring meetings for team updates often consume large amounts of time. Over time they can become bloated with attendees, unproductive and disconnected from original goals.

As described in [How to finally kill the useless, recurring meeting](https://insights.office.com/digital-transformation/how-to-finally-kill-the-useless-recurring-meeting/), we all know how wasteful a "bloated" weekly meeting can be. But there's hope: "To liberate victims from this seemingly inescapable vicious cycle, it’s necessary to kick-start a virtuous cycle in which everyone is empowered to say no, ask why, and identify strategies to allow everyone in an organization to be more effective on a day-to-day basis." Ways to optimize recurring meetings:

* Use [Microsoft Teams channels](/microsoftteams/teams-channels-overview) as a way for team members to get questions answered and provide updates without the need for a meeting.
* Experiment with 15-minute meetings. Short stand-up meetings with focused agendas are common in high-stakes workplaces to debrief or reflect on an event.

### Promote healthy meeting habits

Emailing and chatting during meetings can lead to different interpretations of decisions, missed guidance and inconsistent follow-through on action items.

According to [If you multitask during meetings, your team will, too](https://insights.office.com/productivity/multitask-meetings-team-will/): “Managers that frequently send emails during meetings are, according to our analysis, are 2.2 times more likely to have direct reports who also multi-task in meetings.” Ways to improve meetings:

* Use [Viva Insights to prepare for meetings](/viva/insights/personal/use/use-the-insights#prepare-for-your-meetings), which includes information about the meetings, related documents, and reminders to book preparation time.
* When distracted by a thought to send an email during a meeting, add it quickly to your to-do list instead and move on. This provides satisfaction and can help you regain focus.

For more best practices and change strategies, see [Best practices for meetings](/viva/insights/tutorials/gm-meetings).

