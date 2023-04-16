---

ms.date: 10/06/2020
title: Transform meeting culture through Viva Insights
description: Learn how to use Microsoft Viva Insights data to analyze and transform your organization's meeting culture
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: 
- m365initiative-viva-insights 
- viva-insights-leader
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Transform meeting culture

Meetings are essential for collaboration, however unnecessary meetings and bad practices can harm engagement and limit productivity. Each of the behaviors listed show how your organization compares with others based on industry research and your specific organizational data.

Microsoft Viva Insights has a **My organization** page that shows leader's collaboration data about their team. The outcomes include data about **Transform meeting culture**.

![Transform meeting culture page.](../images/wpa/use/meeting-culture.png)

## Calculations

The following are the percentage insights, their underlying metrics, and a little about the calculations used for them.

![Transform meetings examine recurring meetings.](../images/wpa/use/meeting-culture-percent.png)

|Behavior |Percentage insight | Metrics |Calculations |
|---------|--------|--------------------|----------------------|
|Optimize meeting hours |Percentage of employees who spend a majority of their meeting time in long or large meetings |[Long meetings](/viva/insights/use/glossary?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#long-meeting-define), [large meetings](/viva/insights/use/glossary?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#large-meeting-define), [decision-making meetings](/viva/insights/use/glossary?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#decision-making-meeting-define), and [meeting hours](/viva/insights/use/metric-definitions?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#meeting-hours-define) |Percentage of employees who spend a majority of their meeting hours in long meetings, which are more than one hour, or large meetings, which have more than eight attendees. This insight is calculated weekly and averaged for the entire time period. |
|Examine recurring meetings |Percentage of employees who spend a majority of their time in recurring meetings | [IsRecurring meeting filter](/viva/insights/tutorials/meeting-queries?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#add-metrics) and [meeting hours](/viva/insights/metric-definitions?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#meeting-hours-define) |Percentage of employees who spend more than 50 percent of their meeting hours in recurring meetings. This insight is calculated weekly and averaged for the entire time period. |
|Promote healthy meeting habits |Percentage of employees who significantly multitask in meetings |[Multitasking meeting hours](/viva/insights/use/metric-definitions?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#multitasking-meeting-hours-define) | Percentage of employees who spend more than 25 percent of their meetings hours multitasking. This insight is calculated weekly and then averaged for the entire time period. |

The following defines the organizational data shown in the visual behavioral insights.

![Transform meetings promote healthy meeting habits.](../images/wpa/use/meeting-culture-visual.png)

|Behavior |Visual insight | Definition |
|---------|--------|----------------------|
|Improve meeting quality |Meetings by duration and number of attendees |Uses [meeting hours](/viva/insights/use/metric-definitions?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#meeting-hours-define) to calculate the following percentages:<ul><li>**Large meetings** - Percentage of meetings that are larger than eight attendees but have a duration of less than one hour. </li><li>**Long meetings** - Percentage of meetings that are longer than one hour but have less than equal to eight attendees. </li><li>**Long and large meetings** - Percentage of meetings that have more than eight attendees and are longer than one hour. </li><li>**Decision-making meetings** - Percentage of meetings that have between two and eight attendees and are less than one hour in duration. </li>|
|Examine recurring meetings | Recurring vs. non-recurring meeting hours |Percentage of total meeting hours spent in recurring and non-recurring meetings. These hours are summed for the entire time period and then the percentages are calculated. These calculations use the [meeting hours](/viva/insights/use/metric-definitions?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#meeting-hours-define) metric and the [IsRecurring meeting filter](/viva/insights/tutorials/meeting-queries?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#add-metrics).|
|Promote healthy meeting habits | Distribution of weekly time spent multitasking | Percentage of employees based on their weekly [multitasking meeting hours](/viva/insights/use/metric-definitions?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#multitasking-meeting-hours-define). They are divided into those who spend between zero and one hour, one and five hours, and more than five hours multitasking in meetings. These percentages are calculated weekly and averaged for the entire time period. |

## Best practices

To take action on an outcome, you can select **View best practices** to see a list of recommendations for it. This section describes why each of the following behaviors matter and the top best practices that can help transform meeting culture.

* [Optimize meeting hours](#optimize-meeting-hours)
* [Examine recurring meetings](#examine-recurring-meetings)
* [Promote healthy meeting habits](#promote-healthy-meeting-habits)

### Optimize meeting hours

Long and large meetings are costly and often considered a waste of time. Shorter meetings with fewer people can enhance individual and team performance.

The [condensed guide to running meetings](https://insights.office.com/collaboration/how-to-run-effective-meetings-and-stop-wasting-time/) explains a few new ideas that can help make your meetings more effective, such as if "you want people to have the opportunity to contribute, you need to limit attendance." Other ways to reduce meeting time:

* Use [Microsoft Teams channels](/microsoftteams/teams-channels-overview) as a way for team members to get questions answered and provide updates without the need for a meeting.  
* Encourage employees to politely say no to meetings that lack an agenda or are misaligned with priorities. The feedback will motivate organizers to plan better meetings.

For more best practices and change strategies, see [Best practices for meetings](../tutorials/gm-meetings.md).

### Examine recurring meetings

Recurring meetings for team updates often consume large amounts of time. Over time they can become bloated with attendees, unproductive and disconnected from original goals.

As described in [How to finally kill the useless, recurring meeting](https://insights.office.com/digital-transformation/how-to-finally-kill-the-useless-recurring-meeting/), we all know how wasteful a "bloated" weekly meeting can be. But there's hope: "To liberate victims from this seemingly inescapable vicious cycle, it’s necessary to kick-start a virtuous cycle in which everyone is empowered to say no, ask why, and identify strategies to allow everyone in an organization to be more effective on a day-to-day basis." Ways to optimize recurring meetings:

* Use [Microsoft Teams channels](/microsoftteams/teams-channels-overview) as a way for team members to get questions answered and provide updates without the need for a meeting.
* Experiment with 15-minute meetings. Short stand-up meetings with focused agendas are common in high-stakes workplaces to debrief or reflect on an event.

For more best practices and change strategies, see [Best practices for meetings](../tutorials/gm-meetings.md).

### Promote healthy meeting habits

Emailing and chatting during meetings can lead to different interpretations of decisions, missed guidance and inconsistent follow-through on action items.

According to [If you multitask during meetings, your team will, too](https://insights.office.com/productivity/multitask-meetings-team-will/): “Managers that frequently send emails during meetings are, according to our analysis, are 2.2 times more likely to have direct reports who also multi-task in meetings.” Ways to improve meetings:

* Use [Viva Insights in Outlook to prepare for meetings](../personal/use/use-the-insights.md#prepare-for-your-meetings), which includes information about the meetings, related documents, and reminders to book preparation time.
* When distracted by a thought to send an email during a meeting, add it quickly to your to-do list instead and move on. This provides satisfaction and can help you regain focus.

For more best practices and change strategies, see [Best practices for meetings](../tutorials/gm-meetings.md).

