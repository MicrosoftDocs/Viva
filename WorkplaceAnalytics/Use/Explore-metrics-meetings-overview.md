---

title: Explore meetings overview data in Workplace Analytics
description: Overview of meetings data in Workplace Analytics
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Meetings overview

**Meetings overview** summarizes meeting norms within your organization. You can use this section to gain insight into meeting quality by viewing metrics about specific meeting components that can help determine the efficiency and effectiveness of meetings, such as duration, number of attendees, redundancy, multitasking, and conflicting meeting hours, as shown in the Meetings overview summary in the following image. Employees who sent at least one email or instant message during a week are considered active and are included in the data for the weeks they are active.

![Meetings overview](../images/wpa/use/meetings-overview.png)

## Access to Meetings overview

**Meetings overview** data is available through the recommendations within **See your insights** in the **Take action** section of a related insight. However, you can also go to [Meetings overview](https://workplaceanalytics.office.com/Home/Agility/MeetingsOverview) to view it in Workplace Analytics.

## Low-quality meeting hours

The low-quality meeting hours overview summarizes the number of low-quality meeting hours for the organization and shows the percentage of meetings with any of the three components of low-quality meetings.

**Low-quality meetings hours** are the number of hours a person spent in meetings where they qualify as redundant, are scheduled to be in conflicting meetings, or are multitasking. If a person meets one or more of these conditions during a meeting, the meeting is counted as low-quality.

![Low-quality meeting hours](../images/wpa/use/06-low-quality-meeting-hours.png)

### Why it’s important

* Low-quality meeting hours are a good indicator of meeting culture and can help identify opportunities to make meetings more efficient or engaging. Multitasking may significantly reduce productivity.
* Email multitasking in a meeting means attendees are not contributing at their full potential, hearing only part of the communication and/or failing to contribute their know-how to the task at hand.
* Redundancy is an indication of underlying lack of role clarity, poor delegation, and/or a risk averse culture. Lower level employees attending a high proportion of redundant meetings could potentially feel less empowered. Senior levels may be better off by appropriately delegating meeting attendance. As a sign of career development, redundancy should diminish with tenure.

### Hourly rate

Admins can include an optional HourlyRate column in the organizational data, which they can use to calculate the total cost of low-quality meetings as shown in Meetings overview. If the HourlyRate column is included, cost is calculated as the sum of a person's default hourly rate for the organization multiplied by low-quality meeting hours.

If no hourly rate is assigned to a meeting participant, a default hourly rate of $75 is used. On the [Admin settings](https://docs.microsoft.com/workplace-analytics/use/settings) page, admins can change the Hourly Rate field from its default value to any other hourly rate.

## Meetings hours by number of attendees

Each duration segment in the chart shows the time a person spent in meetings with the specified number of attendees.

![Meeting numbers by number of attendees](../images/wpa/use/07-meeting-hours-by-number-of-attendees.png)

### Why it’s important

* Large meetings aren’t always bad, but having more attendees can make it more difficult to reach a decision.
* Large meetings leave all but a small minority of actively participating attendees disengaged. An overly collaborative and inclusive culture, which may stem from associating meeting attendance with employee importance, or be the outcome of a consensus-driven culture, may lead to a 'safe' invite-all (and accept-all) attitude, creating overly large meetings.
* A high percentage of meeting hours with a large number of people can suggest poor meeting accountability and a lack of empowerment. Applying what is known as the 8-18-1800 rule can help ensure the meeting size matches the goal. The rule is decision-making meetings are best with up to 8 attendees, brainstorming/update meetings can have up to 18 attendees, and informational meetings can have 1800 or more attendees.

## Meetings hours by duration

Each duration segment in the chart shows the total time a person spent in meetings of the specified number of hours.

![Meetings hours by duration](../images/wpa/use/08-meeting-hours-by-duration.png)

### Why it’s important

* Like large meetings, long meeting aren’t necessarily bad, but consistently having long meetings can indicate that groups lack direction or focus, are not structuring meetings efficiently, or are having trouble coming to a decision.
* Meetings that regularly run over one hour can make it difficult to retain the focus of attendees, unless they are well designed small brain-storming/problem-solving sessions.
* A high percentage of meetings greater than an hour in length suggests poor meeting planning and potential for disengagement.

## Redundant meeting hours

**Redundant meeting hours** is the time a person spent in meetings where at least three distinct levels in the person's organization attended.

![Redundant meeting hours](../images/wpa/use/09-redundant-meeting-hours.png)

### Why it’s important

* Redundant meetings are an opportunity to downsize meetings by removing unnecessary attendees. Multiple layers of management are not always needed in the same meeting.
* Functional redundancy can indicate an underlying lack of role clarity, poor delegation, and/or a risk-averse culture.
* Lower-level employees attending a high proportion of redundant meetings could potentially feel less empowered.
* Senior-level managers may be better off by delegating meeting attendance.
* As a sign of career development, redundancy should diminish with tenure.

## Multitasking meeting hours

**Multitasking meeting hours** shows the number of meeting hours where the person sent two or more emails per meeting hour, or two or more emails per meeting for meetings less than an hour.

![Multitasking meeting hours](../images/wpa/use/10-multitasking-meeting-hours.png)

### Why it’s important

* Multitasking indicates that employees might be overloaded, because they're catching up on email during meetings. It might also suggest that employees are not engaged in the meeting, meaning they are not essential attendees.
* Multitasking can reduce productivity and cause attendees to not contribute at their full potential in a meeting, hearing only part of the communication and/or failing to contribute their know-how to the task at hand.
* Managers who multi-task send a clear signal that the meeting is not important, leading others to follow.
* Multi-tasking can become a cultural norm in organizations exhibiting collaboration overload. Insight can come from investigating norms of managers with high multitasking rates.

## Conflicting meeting hours

**Conflicting meeting hours** shows the number of meeting hours where the person had overlapping meetings in their calendar. The count includes the entire duration of all overlapping meetings, not just the amount of time that overlaps. (This number includes all non-declined meetings, which includes those with accepted, tentative, and no responses to the invites).

![Conflicting meeting hours](../images/wpa/use/11-conflicting-meeting-hours.png)

### Why it’s important

* Employees who are double-booked might not be able to fully focus or commit to either meeting.
* Consistently conflicting meetings can result in employees feeling stressed and over-burdened. This can especially be important for managers who are overloaded with meetings and may unintentionally delay or de-prioritize their 1:1 meetings.
* Manager 1:1 meetings with employees are critical for employee development, and if ignored, may lead to employee disengagement and ultimately attrition.
* Consistently conflicting meeting hours could indicate a cultural issue with potentially significant implications for agility, innovation, engagement, and ultimately, performance.

## Calculation variables

You might expect the total number of redundant, conflicting, and multitasking meeting hours to equal the total number of low-quality meeting hours in a query. However, sometimes the hours won’t exactly match up because of how conflicting meeting hours are calculated, the set meeting exclusion rules, and the type of meeting.

* **Double-booked meetings** – For any double-booked meeting time in a weekly data upload, the meeting duration calculation is adjusted for low-quality meeting hours.
* **Conflicting meetings** – Calculates the total meeting time where two or more meetings overlap on the calendar for work meetings that comply with the set meeting exclusion rules.

For example, the following scenarios of conflicting meetings are counted differently based on the meeting exclusion rules and the meeting type:

* Jill has a one-hour work meeting scheduled at 1PM and a different one-hour work meeting scheduled at 1:30PM on the same day. These two overlapping meetings add 1.5 hours to conflicting meeting hours and 1.5 hours to low-quality meeting hours for the week.
* John has a one-hour work meeting scheduled at 1PM and a one-hour dentist appointment scheduled at 1:30PM (filtered out by a meeting exclusion rule) on the same day. Based on the meeting exclusion rules and calculation adjustments, this adds 0.5 hour to low-quality meeting hours and 0 (zero) conflicting meeting hours for the week because the personal meeting is filtered out.
* Sara has a dentist appointment scheduled at 1PM to 1:30PM (excluded with a meeting exclusion rule), a work meeting scheduled at 1PM to 2PM, and a different work meeting scheduled at 1:30PM to 2:30PM on the same day. Based on meeting exclusion rules and adjusted calculations, these three meetings add 1 hour (1:30PM to 2:30PM) to low-quality meeting hours and 1.5 hours (1PM to 2:30PM) to conflicting meeting hours for the week.

## Related topics

* [Page settings](../use/explore-page-settings.md)
* [Workplace Analytics Charts](../use/chart-types.md)
