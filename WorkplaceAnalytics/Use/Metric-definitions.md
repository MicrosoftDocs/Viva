---
# Metadata Sample
# required metadata

title: Workplace Analytics metric definitions 
description: This articles describes and defines each of the metrics available within Workplace Analytics.
author: LeisaLaDell
ms.author: v-leash
ms.date: 02/20/2018
ms.topic: get-started-article
ms.prod: wpa
---
# Metric descriptions for Workplace Analytics
These terms describe the metrics calculated by Workplace Analytics that you can use in your queries. There are three types of metrics: Person metrics, Meeting metrics, and Group metrics.

## Person metrics
|Metric|Description|Query type|Data type|Customizable|
|------|-----------|----------|---------|------------|
|After hours collaboration|Number of hours spent in meetings and sending email outside of working hours.|Person|Hour|No|
|Collaboration hours|Number of hours the person spent in meetings and email with at least one other person. Collaboration hours include both internal and external hours. |Person|Hour|Yes|
|Collaboration hours external|Number of hours the person spent in meetings and on email with at least one person outside the company (as defined by the participant’s email domains).|Person|Hour|No|
|Conflicting meeting hours|Number of meeting hours where the person had overlapping meetings in their calendar. The count includes the entire duration of all overlapping meetings, not just the amount of time that overlaps. (This number includes all non-declined meetings).|Person|Hour|Yes|
|Email hours|Number of hours the person spent sending and reading email.|Person|Hour|Yes|
|Emails sent|Number of emails the person sent.|Person|Count|Yes|
|External network size|Number of people external to the company with whom the person had at least two meaningful interactions (a meeting or email between five or fewer people) within the last 28 days (or if reported by month, within the last month).|Person|Count|No|
|Generated workload email hours|Number of email hours the person created for internal recipients by sending emails.|Person|Hour|Yes|
|Generated workload email recipients|Number of internal recipients on all emails sent by the person. (Counts each recipient once for each email received.)|Person|Count|Yes|
|Generated workload meeting attendees|Number of internal attendees of meetings organized by the person. (Counts each attendee once for each meeting.)|Person|Count|Yes|
|Generated workload meeting hours|Number of meeting hours the person created for internal attendees by organizing meetings.|Person|Hour|Yes|
|Generated workload meetings organized|Number of internal meetings organized by the person.|Person|Count|Yes|
|Internal network size|Number of people within the company with whom the person had at least two meaningful interactions (a meeting or email between five or fewer people) within the last 28 days (or if reported by month, within the last month).|Person|Count|No <!-- Changed from Yes 04-25-18 per Daysha -->|
|Low-quality meeting hours|Number of meeting hours where the person multitasked, had a conflicting meeting (any non-declined meeting that overlaps), or is redundant (at least three distinct levels from their organization attended). The current assumed cost of low-quality meeting hours is $75 per person hour. |Person|Hour|Yes|
|Manager coaching hours 1:1|The number of hours that a manager spends in one-on-one meetings with their direct reports. |Person|Hour|Yes|
|Meeting hours|Number of hours the person spent in meetings with at least one other person.|Person|Hour|Yes|
|Meeting hours with manager|Number of meeting hours involving at least the person and their manager.|Person|Hour|Yes|
|Meeting hours with manager 1:1|Number of meeting hours involving only the person and their manager.|Person|Hour|Yes|
|Meetings hours with skip level|Number of meeting hours where the manager of the person's manager is an attendee.|Person|Hour|Yes|
|Meetings|Number of meetings the person attended.|Person|Count|Yes|
|Meetings with manager|Number of meetings where attendees include at least the person and their manager.|Person|Count|Yes|
|Meetings with manager 1:1|Number of meetings involving only the person and their manager.|Person|Count|Yes|
|Meetings with skip level|Number of meetings where the manager of the person's manager is an attendee.|Person|Count|Yes|
|Multitasking meeting hours|Number of meeting hours where the person sent:<ul><li>Two emails or more per meeting hour</li><li>Two emails or more per meeting for meetings less than an hour</li></ul>|Person|Hour|Yes|
|Networking outside company|Number of companies outside their own that the person had meaningful interactions with, within the last 28 days (or if reported by month, within the last month).|Person|Count|No <!-- Changed from Yes 04-25-18 per Daysha -->|
|Networking outside department|Number of departments outside their own that the person had meaningful interactions with, within the last 28 days (or if reported by month, within the last month).|Person|Count|No <!-- Changed from Yes 04-25-18 per Daysha -->|
|Open 1 hr blocks|Number of one-hour blocks in the person’s calendar during the work day where there are no meetings.|Person|Count|Yes|
|Open 2 hr blocks|Number of two-hour blocks in the person’s calendar without meetings during the work day.|Person|Count|Yes|
|Redundant meeting hours|Number of meeting hours where at least three distinct levels in the person's organization attended.|Person|Hour|Yes|
|Time in meetings during after hours|Number of hours the person spent in meetings outside of working hours.|Person|Hour|Yes|
|Time in meetings during working hours|Number of hours the person spent in meetings during working hours.|Person |Hour |Yes|
|Time spent in mails after hours|Number of hours the person spent sending email outside of working hours.|Person|Hour|No|
|Time spent in mails working hours|Number of hours the person spent sending email during working hours.|Person|Hour|No|
|Total emails sent during meeting | Total emails sent during meeting |Person|Count|Yes|
|Total focus hours|The total number of hours made up of two-hour or greater blocks of time where the person had no meetings.|Person|Hour|Yes|
|Working hours collaboration|Number of hours the person spent in meetings and sending email during working hours.|Person|Hour|No|
|Workweek Span|Time between the person's first email or meeting and the last email or meeting in a day. (Counted Monday – Friday, with a minimum of 4 hours and a maximum of 16 hours per day.) If reported for the week, the metric is a sum for the week. If reported for the month, the metric is the weekly average.|Person|Hour|No|

## Meeting metrics
|Metric|Description|Query type|Data type|Customizable|
|------|-----------|----------|---------|------------|
|Attendee meeting hours|Sum of the total adjusted meeting hours for all attendees.|Meeting|Hour|No|
|Attendees|Number of people who attended the meeting.|Meeting|Count|No|
|Attendees multitasking|Number of attendees that sent emails during the meeting.<ul><li>In meetings of one hour or less, two or more emails.</li><li>In meetings longer than one hour, two emails per hour. (Example: Sending four emails during a two-hour meeting would count as multitasking.)</li></ul>|Meeting|Count|No|
|Attendees with conflicting meeting|Number of attendees with meetings that overlap with the meeting (includes all non-declined meetings).|Meeting|Count|No|
|Emails sent during meeting|Number of emails the person sent during all meetings.|Meeting|Count|No|
|Invitees|Number of people invited to the meeting.|Meeting|Count|No|
|Total emails sent during meeting|Number of emails sent during the meeting by all attendees.|Meetings|Count|No|
## Group metrics
|Metric|Description|Query type|Data type|Customizable|
|------|-----------|----------|---------|------------|
|Email hours allocated|Number of email hours between the user-defined groups.|Group|Hour|No|
|Meeting hours allocated|Number of meeting hours between the user-defined groups.|Group|Hour|No|
|Meetings attended together|Number of distinct meetings with at least one attendee from each user-defined group.|Group|Count|No|
|Total attendees|Total number of attendees in all meetings from each user-defined group.|Group|Count|No|
|Total collaboration hours allocated|Total number of collaboration hours between the user-defined groups.|Group|Hour|No|
|Total invitees|Total number of invitees in all meetings from each user-defined group.|Group|Count|No|