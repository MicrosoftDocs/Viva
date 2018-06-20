---
# Metadata Sample
# required metadata

title: Workplace Analytics metric definitions 
description: This article describes the metrics for queries that are available in Workplace Analytics, including Person, Meeting, Group-to-group, and Person-to-group metrics. 
author: madehmer
ms.author: paul9955
ms.date: 06/13/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Metric descriptions for Workplace Analytics
You can use the following metrics in Workplace Analytics to customize your queries.

## Person metrics

|Metric|Description|Query type|Data type|Customizable|
|------|-----------|----------|---------|------------|
|After-hours collaboration|Number of hours the person spent in meetings and on email outside of working hours.|Person|Hour|No|
|Collaboration hours|Number of hours the person spent in meetings and on email with at least one other person. Collaboration hours include both internal and external hours. |Person|Hour|Yes|
|Collaboration hours external|Number of hours the person spent in meetings and on email with at least one person outside the company (as defined by the participant’s email domains).|Person|Hour|No|
|Conflicting meeting hours|Number of meeting hours where the person had overlapping meetings in their calendar. The count includes the entire duration of all overlapping meetings, not just the amount of time that overlaps. (This number includes all accepted meeting times.).|Person|Hour|Yes|
|Email hours|Number of hours the person spent sending and receiving emails.|Person|Hour|Yes|
|Emails sent|Number of emails the person sent.|Person|Count|Yes|
|External network size|Number of people external to the company with whom the person had at least two meaningful interactions (a meeting or email between five or fewer people) within the last 28 days (or if reported by month, within the last month).|Person|Count|No|
|Generated workload email hours|Number of email hours the person created for internal recipients by sending emails.|Person|Hour|Yes|
|Generated workload email recipients|Number of internal recipients on all emails sent by the person. (Counts each recipient once for each email received.)|Person|Count|Yes|
|Generated workload meeting attendees|Number of internal attendees in meetings organized by the person. (Counts each attendee once for each meeting.)|Person|Count|Yes|
|Generated workload meeting hours|Number of meeting hours the person created for internal attendees by organizing meetings.|Person|Hour|Yes|
|Generated workload meetings organized|Number of internal meetings organized by the person.|Person|Count|Yes|
|Internal network size|Number of people within the company with whom the person had at least two meaningful interactions (a meeting or email between five or fewer people) within the last 28 days (or if reported by month, within the last month).|Person|Count|No <!-- Changed from Yes 04-25-18 per Daysha -->|
|Low-quality meeting hours|Number of meeting hours where the person multitasked, had a conflicting meeting (any accepted meeting that overlaps), or is redundant (at least three distinct levels from their organization that attended). The current assumed cost of low-quality meeting hours is $75 per person hour. |Person|Hour|Yes|
|Manager coaching hours 1:1|Number of hours that a manager spends in one-on-one meetings with their direct reports. |Person|Hour|Yes|
|Meeting hours|Number of hours the person spent in meetings with at least one other person.|Person|Hour|Yes|
|Meeting hours with manager|Number of meeting hours where attendees included at least the person and their manager.|Person|Hour|Yes|
|Meeting hours with manager 1:1|Number of meeting hours involving only the person and their manager.|Person|Hour|Yes|
|Meetings hours with skip level|Number of meeting hours that the person attends where their manager's manager also attends the meeting.|Person|Hour|Yes|
|Meetings|Number of meetings the person attended.|Person|Count|Yes|
|Meetings with manager|Number of meetings where attendees include at least the person and their manager.|Person|Count|Yes|
|Meetings with manager 1:1|Number of meetings involving only the person and their manager.|Person|Count|Yes|
|Meetings with skip level|Number of meetings where the manager of the person's manager is an attendee.|Person|Count|Yes|
|Multitasking meeting hours|Number of meeting hours where the person sent:<ul><li>Two or more emails sent per meeting hour</li><li>Two or more emails sent per meeting for meetings less than one hour</li></ul>|Person|Hour|Yes|
|Networking outside company|Number of companies outside their own that the person had meaningful interactions with, within the last 28 days (or if reported by month, within the last month).|Person|Count|No <!-- Changed from Yes 04-25-18 per Daysha -->|
|Networking outside department|Number of departments outside their own that the person had meaningful interactions with, within the last 28 days (or if reported by month, within the last month).|Person|Count|No <!-- Changed from Yes 04-25-18 per Daysha -->|
|Open 1-hr blocks|Number of one-hour blocks in the person’s calendar without meetings during the work day.|Person|Count|Yes|
|Open 2-hr blocks|Number of two-hour blocks in the person’s calendar without meetings during the work day.|Person|Count|Yes|
|Redundant meeting hours|Number of meeting hours a person spent with attendees from three or more distinct levels within that person's organization.|Person|Hour|Yes|
|Time in meetings during after hours|Number of hours the person spent in meetings outside of working hours.|Person|Hour|Yes|
|Time in meetings during working hours|Number of hours the person spent in meetings during working hours.|Person |Hour |Yes|
|Time spent on email after hours|Number of hours the person spent sending email outside of working hours.|Person|Hour|No|
|Time spent on email working hours|Number of hours the person spent sending email during working hours.|Person|Hour|No|
|Total emails sent during meetings | Number of emails the person sent during meetings. |Person|Count|Yes|
|Total focus hours|Total number of hours with two or more hour blocks of time where the person had no meetings.|Person|Hour|Yes|
|Working hours collaboration|Number of hours the person spent in meetings and sending emails during working hours.|Person|Hour|No|
|Workweek Span|Time between the person's first sent email or meeting attended and the last email or meeting in a day. (Counted Monday through Friday, with a minimum of four hours and a maximum of 16 hours per day.) If reported for the week, the metric is a sum for the week. If reported for the month, the metric is the weekly average.|Person|Hour|No|

## Meeting metrics

|Metric|Description|Query type|Data type|Customizable|
|------|-----------|----------|---------|------------|
|Attendee meeting hours|Total number of adjusted meeting hours for all attendees.|Meeting|Hour|No|
|Attendees|Number of people who attended the meeting.|Meeting|Count|No|
|Attendees multitasking|Number of attendees that sent emails during the meeting.<ul><li>In meetings of one hour or less, two or more emails.</li><li>In meetings longer than one hour, two emails per hour. (Example: Sending four emails during a two-hour meeting would count as multitasking.)</li></ul>|Meeting|Count|No|
|Attendees with conflicting meeting|Number of attendees with meetings that overlap with the meeting (includes all non-declined meetings).|Meeting|Count|No|
|Emails sent during meetings|Number of emails the person sent during all meetings.|Meeting|Count|No|
|Invitees|Number of people invited to the meeting.|Meeting|Count|No|
|Total emails sent during meeting|Number of emails sent during a meeting by all attendees.|Meetings|Count|No|

## Group-to-Group metrics

|Metric|Description|Query type|Data type|Customizable|
|------|-----------|----------|---------|------------|
|Email hours allocated|Number of hours spent sending emails between the user-defined groups.|Group|Hour|No|
|Meeting hours allocated|Number of meeting hours spent between the user-defined groups.|Group|Hour|No|
|Meetings attended together|Number of distinct meetings with at least one attendee from each user-defined group.|Group|Count|No|
|Total attendees|Total number of attendees in all meetings from each user-defined group.|Group|Count|No|
|Total collaboration hours allocated|Total number of collaboration hours between the user-defined groups.|Group|Hour|No|
|Total invitees|Total number of invitees in all meetings from each user-defined group.|Group|Count|No|

## Person-to-Group metrics

|Metric|Description|Query type|Data type|Customizable|
|------|-----------|----------|---------|------------|
|Collaboration hours|Total number of meeting and email hours for the time investor with one or more people in the collaborator group. This metric uses time allocation logic.|Group|Hour|No|
|Email count|Count of unique email exchanges (sent and received) that the time investor had with one or more people in the collaborator group|Group|Count|No|
|Email hours|Total number of hours that the time investor spent sending and reading emails with one or more people in the collaborator group. This metric uses time allocation logic.|Group|Hour|No|
|Meeting hours|Total number of hours that the time investor spent in meetings with one or more people in the collaborator group. This metric uses time allocation logic.|Group|Hour|No|
|Meetings|Number of unique meetings that the time investor attended with one or more people in the collaborator group.|Group|Count|No|
|Network size|Number of people in the collaborator group that the time investor had at least two meaningful interactions with in the last 28 days.|Group|Count|No|