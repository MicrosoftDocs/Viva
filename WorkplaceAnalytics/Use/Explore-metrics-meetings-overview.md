---
# Metadata Sample
# required metadata

title: Explore meetings overview metrics in Workplace Analytics
description: Overview of meetings metrics on the Workplace Analytics Explore page.
author: madehmer
ms.author: v-midehm
ms.date: 07/31/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---
# Meetings Overview

The **Meetings Overview** page in **Explore** summarizes meeting norms within your organization. You can use this section to gain insight into meeting quality by viewing metrics about specific meeting components that can help determine the efficiency and effectiveness of meetings, such as duration, number of attendees, redundancy, multitasking, and conflicting meeting hours, as shown in the Meetings overview summary in the following image. Employees who sent at least one email during a week are considered active and are included in the Explore metrics for the weeks they are active.

![Meetings overview](../images/WpA/Use/Meetings-overview-explore-metrics.png)

To open the **Meetings overview** page:

1. Open the [Workplace Analytics](https://workplaceanalytics.office.com) Home page. If prompted, enter your Microsoft credentials.
2. In the left navigation pane, select **Explore**.
3. In **Explore**, select the **Meetings overview** tab.

## Low-quality meeting hours

The low-quality meeting hours overview summarizes the number of low-quality meeting hours for the organization and shows the percentage of meetings with any of the three components of low-quality meetings.

**Low-quality meetings hours** are the number of hours a person spent in meetings where they are either redundant, scheduled to be in conflicting meetings, or multitasking. If a person meets any of these conditions during a meeting, the meeting is counted as low-quality.

![Low-quality meeting hours](../images/WpA/Use/low-quality-meeting-hours-explore-metrics.png)

### Why it’s important

* Low-quality meeting hours are a good indicator of meeting culture and can help identify opportunities to make meetings more efficient or engaging. Multitasking may significantly reduce productivity.
* Email multitasking in a meeting means attendees are not contributing at their full potential, hearing only part of the communication and/or failing to contribute their know-how to the task at hand.
* Redundancy is an indication of underlying lack of role clarity, poor delegation, and/or a risk averse culture. Lower level employees attending a high proportion of redundant meetings could potentially feel less empowered. Senior levels may be better off by appropriately delegating meeting attendance. As a sign of career development, redundancy should diminish with tenure.

### Hourly rate
Admins can include an optional HourlyRate column in the organizational data, which they can use to calculate the total cost of low-quality meetings as shown in Meetings overview. If the HourlyRate column is included, cost is calculated as the sum of a person’s default hourly rate for the organization multiplied by low-quality meeting hours.
If no hourly rate is assigned to a meeting participant, a default hourly rate of $75 is used. On the [Settings](https://docs.microsoft.com/workplace-analytics/use/settings) page, admins can change the Hourly Rate field from its default value to any other hourly rate.

## Meetings hours by number of attendees

Each duration segment in the chart shows the time a person spent in meetings with the specified number of attendees.

![Meeting numbers by number of attendees](../images/WpA/Use/meeting-hours-by-attendees-explore-metrics.png)

### Why it’s important

* Large meetings aren’t always bad, but having more attendees can make it more difficult to reach a decision.
* Large meetings leave all but a small minority of actively participating attendees disengaged. An overly collaborative and inclusive culture, which may stem from associating meeting attendance with employee importance, or be the outcome of a consensus-driven culture, may lead to a ‘safe’ invite-all (and accept-all) attitude, creating overly large meetings.
* A high percentage of meeting hours with a large number of people can suggest poor meeting accountability and a lack of empowerment. Applying what is known as the 8-18-1800 rule can help ensure the meeting size matches the goal. The rule is decision-making meetings are best with up to 8 attendees, brainstorming/update meetings can have up to 18 attendees, and informational meetings can have 1800 or more attendees.

## Meetings hours by duration
Each duration segment in the chart shows the total time a person spent in meetings of the specified number of hours.

![Meetings hours by duration](../images//WpA/Use/meeting-hours-by-duration-explore-data.png
)

### Why it’s important

* Like large meetings, long meeting aren’t necessarily bad, but consistently having long meetings can indicate that groups lack direction or focus, aren’t structuring meetings efficiently, or are having trouble coming to a decision.
* Meetings that regularly run over one hour can make it difficult to retain the focus of attendees, unless they are well designed small brain-storming/problem solving sessions.
* A high percentage of meetings greater than an hour in duration suggests poor meeting planning and potential for disengagement.

## Redundant meeting hours
**Redundant meeting hours** is the time a person spent in meetings where at least three distinct levels in the person's organization attended.

![Redundant meeting hours](../images/WpA/Use/redundant-meeting-hours-explore.png)

### Why it’s important

* Redundant meetings are an opportunity to downsize meetings by removing unnecessary attendees. Multiple layers of management are not always needed in the same meeting.
* Functional redundancy can indicate an underlying lack of role clarity, poor delegation, and/or a risk averse culture.
* Lower-level employees attending a high proportion of redundant meetings could potentially feel less empowered.
* Senior-level managers may be better off by delegating meeting attendance.
* As a sign of career development, redundancy should diminish with tenure.

## Multitasking meeting hours

**Multitasking meeting hours** shows the number of meeting hours where the person sent two or more emails per meeting hour, or two or more emails per meeting for meetings less than an hour.

![Multitasking meeting hours](../images/WpA/Use/multitasking-meeting-hours-explore.png)

### Why it’s important

* Multitasking indicates that employees might be overloaded, because they're catching up on email during meetings. It might also suggest that employees are not engaged in the meeting, meaning they are not essential attendees.
* Multitasking can reduce productivity and cause attendees to not contribute at their full potential in a meeting, hearing only part of the communication and/or failing to contribute their know-how to the task at hand.
* Managers who multi-task send a clear signal that the meeting is not important, leading others to follow.
* Multi-tasking can become a cultural norm in organizations exhibiting collaboration overload. Insight can come from investigating norms of managers with high multitasking rates.

## Conflicting meeting hours

**Conflicting meeting hours** shows the number of meeting hours where the person had overlapping meetings in their calendar. The count includes the entire duration of all overlapping meetings, not just the amount of time that overlaps. (This number includes all non-declined meetings, which includes those with accepted, tentative, and no responses to the invites).

![Conflicting meeting hours](../images/WpA/Use/conflicting-meeting-hours-explore.png)

### Why it’s important

* Employees who are double-booked might not be able to fully focus or commit to either meeting.
* Consistently conflicting meetings can result in employees feeling stressed and over-burdened. This can especially be important for managers who are overloaded with meetings and may unintentionally delay or de-prioritize their 1:1 meetings.
* Manager 1:1 meetings with employees are critical for employee development, and if ignored, may lead to employee disengagement and ultimately attrition.