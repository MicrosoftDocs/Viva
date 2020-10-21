---

title: Workplace Analytics metric definitions 
description: Describes the metrics for queries that are available in Workplace Analytics, including Person, Meeting, Group-to-group, and Person-to-group query metrics
author: paul9955
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
ms.prod: wpa

---

# Metric descriptions for Workplace Analytics

You can use the following metrics in Workplace Analytics to customize your queries.

## Person metrics

|Metric |Description |Query type |Data type |Customizable |
|------|-----------|----------|---------|------------|
| <a name="after-hours-collaboration-definition"></a>After hours collaboration |Number of hours the person spent in meetings and on email outside of working hours. **Note**: To target or filter for after-hours collaboration, you can use a filter with the Collaboration hours metric.|Person|Hour|No|
|After hours email hours |Number of hours the person spent sending email outside of working hours.|Person|Hour|Yes|
|After hours in calls |Number of hours a person spent in scheduled and unscheduled calls through Teams, outside of working hours. For calls that started during working hours, this number only includes the part of the call that occurred outside of that person’s work schedule (as set in Outlook). |Person|Hour|Yes|
|After hours instant messages |Number of hours a person spent in instant messages through Teams, outside of working hours. |Person|Hour|Yes|
|After hours meeting hours|Number of hours the person spent in meetings outside of working hours.|Person|Hour|Yes|
|Call hours| The number of hours the person spent in scheduled and unscheduled calls through Teams with at least one other person, during and outside of working hours.| Person| Hours| Yes |
|Collaboration hours|Number of hours the person spent in meetings and on email with at least one other person. Collaboration hours include both internal and external hours. |Person|Hour|Yes|
|Collaboration hours external|Number of hours the person spent in meetings and on email with at least one person outside the company (as defined by the participant’s email domains).|Person|Hour|No|
|Conflicting meeting hours|Number of meeting hours where the person had overlapping meetings in their calendar. The count includes the entire duration of all overlapping meetings, not just the amount of time that overlaps. (This number includes all non-declined meeting times, which includes accepted, tentative, or no responses to meeting invitations.)|Person|Hour|Yes|
|Email hours|Number of hours the person spent sending and receiving emails.|Person|Hour|Yes|
|Emails sent|Number of emails the person sent.|Person|Count|Yes|
|External network size|The number of people external to the company with whom the person had at least two [meaningful interactions](glossary.md#meaningful-interaction-definition) in the last four weeks.  |Person|Count|Yes|  
|Generated workload call hours|Number of hours the person spent calling internal recipients through Teams.|Person|Hour|Yes|
|Generated workload call participants|Number of internal participants of calls organized by the person. (Counts each participant once for each call.)|Person|Count|Yes|
|Generated workload calls organized|Number of calls organized by the person. |Person|Count|Yes|
|Generated workload email hours|Number of email hours the person created for internal recipients by sending emails.|Person|Hour|Yes|
|Generated workload email recipients|Number of internal recipients on emails sent by the person. (Counts each recipient once for each email received.)|Person|Count|Yes|
|Generated workload instant message hours|Number of instant message hours the person created through Teams for internal recipients by sending instant messages.|Person|Hour|Yes|
|Generated workload instant message recipients|Number of internal participants of calls organized by the person. (Counts each participant once for each call.)|Person|Count|Yes|
|Generated workload meeting attendees|Number of internal attendees in meetings organized by the person. (Counts each attendee once for each meeting.)|Person|Count|Yes|
|Generated workload meeting hours|Number of meeting hours the person created for internal attendees by organizing meetings.|Person|Hour|Yes|
|Generated workload meetings organized|Number of internal meetings organized by the person.|Person|Count|Yes|
|Instant message hours | Number of hours a person spent in instant messages (IMs) through Teams with at least one other person, during and outside of working hours.| Person| Hours| Yes |
|Instant messages sent | Total number of instant messages (IMs) sent by a person through Teams, during and outside of working hours. | Person| Count| Yes |
|Internal network size|   The number of people within the company with whom the person had at least two [meaningful interactions](glossary.md#meaningful-interaction-definition) in the last four weeks.  |Person|Count|Yes |
|Low-quality meeting hours|Number of meeting hours in which an attendee multitasked, attended a *conflicting meeting*, or attended a meeting that exhibits *Redundancy (organizational)*. Workplace Analytics admins can [set the hourly rate](settings.md#hourly-rate) of low-quality meeting time; if this value has not been set, the cost defaults to $75 per person hour. |Person|Hour|Yes|
|Manager coaching hours 1:1|Total number of hours that a manager spends in one-on-one meetings with *all* of the manager's direct reports. |Person|Hour|Yes|
|Meeting hours|Number of hours the person spent in meetings with at least one other person.|Person|Hour|Yes|
|Meeting hours during working hours|Number of hours the person spent in meetings, during working hours, with at least one other person.|Person|Hour|Yes|
| <a name="meeting-hours-with-manager-definition"></a>  Meeting hours with manager | Number of meeting hours where attendees included at least the person and their manager.|Person|Hour|Yes|
| <a name="meeting-hours-with-manager-1-1-definition"></a> Meeting hours with manager 1:1|Number of meeting hours involving only the person and their manager.|Person|Hour|Yes|
|Meetings hours with skip level|Number of meeting hours that the person attends where their manager's manager also attends the meeting.|Person|Hour|Yes|
|Meetings|Number of meetings the person attended.|Person|Count|Yes|
|Meetings with manager|Number of meetings where attendees include at least the person and their manager.|Person|Count|Yes|
|Meetings with manager 1:1|Number of meetings involving only the person and their manager.|Person|Count|Yes|
|Meetings with skip level|Number of meetings where the manager of the person's manager is an attendee.|Person|Count|Yes|
|Multitasking meeting hours|Number of meeting hours where the person sent:<ul><li>Two or more emails sent per meeting hour</li><li>Two or more emails sent per meeting for meetings less than one hour</li></ul>|Person|Hour|Yes|
|Networking outside company|The number of distinct external domains outside the company a person has had at least two [meaningful interactions](glossary.md#meaningful-interaction-definition) in the last four weeks. |Person|Count|Yes |
|Networking outside organization| The number of distinct organizational units within the company that the person had at least two [meaningful interactions](glossary.md#meaningful-interaction-definition) in the last four weeks. |Person|Count|Yes |
|Open 1 hour block |Number of one-hour blocks in the person’s calendar without meetings during the work day.|Person|Count|Yes|
|Open 2 hour blocks |Number of two-hour blocks in the person’s calendar without meetings during the work day.|Person|Count|Yes|
|Peer average (customer collaboration) | The total amount (in hours) of customer collaboration for all of the participants in the plan divided by the number of participants in the plan. | Person | Hour | No|
|Peer average (internal collaboration) | The total amount (in hours) of internal collaboration for all of the participants in the plan divided by the number of participants in the plan. | Person | Hour | No|
|Redundant meeting hours (lower level) |Number of meeting hours a person spent in a meeting with both their manager and their skip-level manager present in the meeting. <br> <br> This metric is _not_ used in calculating *Low-quality meeting hours*. Analysts can use this metric only when creating [Person queries](../tutorials/person-queries.md).|Person | Hour| Yes |
|Redundant meeting hours (organizational) |Number of meeting hours a person spent with attendees from three or more distinct levels within that person’s organization. Used in calculating *Low quality meeting hours*.  |Person|Hour|Yes|
|Time in self-organized meetings|Number of hours spent in meetings organized by the person with at least one other person.|Person|Hour|Yes|
|Total calls | Total number of calls a person joined through Teams, including scheduled and unscheduled calls during and outside of working hours (as set in Outlook). | Person| Count | Yes |
|Total email sent during meeting | Number of emails the person sent during meetings. |Person|Count|Yes|
|Total focus hours|Total number of hours with two or more hour blocks of time where the person had no meetings.|Person|Hour|Yes|
|Working hours collaboration hours|Number of hours the person spent in meetings and sending emails during working hours.|Person|Hour|No|
|Working hours email hours|Number of hours the person spent in sending email during working hours.|Person|Hour|Yes|
|Working hours in calls| Total number of hours a person spent time in scheduled and unscheduled calls with Teams, during working hours. | Person| Hour| Yes |
|Working hours instant messages| Total number of hours a person spent time in instant messages through Teams, during working hours. | Person| Hour| Yes |
| <a name="workweek-span-definition"></a> Workweek span | The time between the person's first sent email, meeting attended, or Teams call or chat, and the last email, meeting, call, or chat for each day of the work week. The total number of hours are based on the person’s work week that is set in Outlook, which the user can change at any time. If a work week is not defined in Outlook (or if Workplace Analytics is unable to access a user's Outlook settings), the totals are based on the default of Monday through Friday, with a minimum of four hours and a maximum of 16 hours per day. If reported for the week, the metric is a sum of the daily values for the week. If reported for the month, the metric is the sum of the daily values for the month. |Person|Hour|No|

## Meeting metrics

|Metric|Description|Query type|Data type|Customizable|
|------|-----------|----------|---------|------------|
| <a name="attendee-meeting-hours-definition"></a>  Attendee meeting hours|Total number of adjusted meeting hours for all attendees.<br>A _[meeting query](../Tutorials/meeting-queries.md)_ focuses on the meeting as the main entity and reports on the various meeting attributes; a _[person query](../Tutorials/person-queries.md)_ looks from a person's perspective and aggregates multiple meetings for the selected time period. Because the two query types have different purposes, their output also differs. |Meeting|Hour|Yes|
| <a name="attendees-definition"></a> Attendees|Number of people who attended the meeting.|Meeting|Count|Yes|
|Attendees multitasking|Number of attendees that sent emails during the meeting.<ul><li>In meetings of one hour or less, two or more emails.</li><li>In meetings longer than one hour, two emails per hour. (Example: Sending four emails during a two-hour meeting would count as multitasking.)</li></ul>|Meeting|Count|Yes|
| <a name="attendees-with-conflicting-meeting-definition"></a>   Attendees with conflicting meeting|Number of attendees with meetings that overlap with the meeting (includes all non-declined meetings, which include accepted, tentative, and no responses to meeting invites).|Meeting|Count|Yes|
|Emails sent during meetings|Number of emails the person sent during all meetings.|Meeting|Count|Yes|
|Invitees|Number of people invited to the meeting.|Meeting|Count|Yes|
|Redundant attendees | The number of attendees of a meeting who are redundant, as defined by the _Redundant meeting hours (lower level)_ metric. For more information about _Redundant meeting hours (lower level)_, see the table that lists [Person metrics](#person-metrics).  |Meeting|Count|Yes|
|Total meeting cost|The total cost of all attendees in a meeting. The meeting cost for each attendee is defined as the product of the attendees' meeting hours multiplied by the attendees' hourly rates. If no hourly rate is available for one or more attendees, the default rate of $75/hr (US dollars) is used to calculate the cost of those attendees.|Meeting|Currency|Yes|
|Total redundant hours|The total number of redundant hours metric for all attendees in a meeting.|Meeting|Hour|Yes|

## Group-to-group metrics

|Metric|Description|Query type|Data type|Customizable|
|------|-----------|----------|---------|------------|
|Collaboration hours |Sum of meeting hours and email hours spent between the time investor and collaborator groups.|Group|Hour|No|
|Email hours |Number of hours spent sending and reading emails between the time investor and collaborator groups.|Group|Hour|No|
|Meeting attendee count|Total number of attendees in all meetings from the time investor and collaborator groups.|Group|Count|No|
|Meeting hours |Number of meeting hours the time investor group has spent meeting with the collaborator group.|Group|Hour|No|
|Meeting invitee count|Total number of invitees in all meetings from the time investor and collaborator groups.|Group|Count|No|
|Meetings |Number of distinct meetings with at least one attendee from the time investor and collaborator groups.|Group|Count|No|
|Time investors initiated meeting hours | This calculates the number of meeting hours the time investors created only for *[Internal collaborators](../use/csv-query-output-file.md#internal-collaborators)* or *[Collaborators within group](../use/csv-query-output-file.md#collaborators-within-group)* by organizing meetings. (Does not follow time-allocation logic.)​ |Group|Hour|No|

## Person-to-group metrics

|Metric|Description|Query type|Data type|Customizable|
|------|-----------|----------|---------|------------|
|Collaboration hours|Total number of meeting and email hours for the time investor with one or more people in the collaborator group. This metric uses time allocation logic. |Group|Hour|No|
|Email count|Count of unique email exchanges (sent and received) that the time investor had with one or more people in the collaborator group. |Group|Count|No|
|Email hours|Total number of hours that the time investor spent sending and reading emails with one or more people in the collaborator group. This metric uses time allocation logic. |Group|Hour|No|
|LastTimeContacted |The last date and time that the time investor (measured employee) emailed or attended a meeting with one or more people in the collaborator group for the specified date range. |Group|DateTime|No|
|Meeting hours|Total number of hours that the time investor spent in meetings with one or more people in the collaborator group. This metric uses time allocation logic. |Group|Hour|No|
|Meetings|Number of unique meetings that the time investor attended with one or more people in the collaborator group. |Group|Count|No|
|Network size|Number of people in the collaborator group who had at least two [meaningful interactions](glossary.md#meaningful-interaction-definition) in the last 28 days with the time investor. This counts both licensed and unlicensed employees in the collaborator group. |Group|Count|No|

## Organizational network analysis (ONA) metrics

These metrics are based on the following collaboration activities: emails, meetings, Teams calls, and Teams chats.   

|Metric|Description|Query type|Data type|Customizable|
|------|-----------|----------|---------|------------|
| <a name="diverse-tie-score-definition"></a> Diverse tie score   &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; | A numeric score that indicates how varied and how broad the person's connections are. A person need not have much direct collaboration with their diverse ties, so it’s easy to have more diverse ties than strong ties. Diverse ties present good sources of fresh and varied information from across the company. | ONA  &nbsp; &nbsp; &nbsp; |Score &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; |No &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |
| <a name="diverse-tie-type-definition"></a> Diverse tie type   &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; | A numeric score that indicates the relative diversity of the person's diverse ties. 0 means the tie is not very diverse; 2 means that the tie is somewhat diverse; 1 means that the tie's has significant diversity. | ONA  &nbsp; &nbsp; &nbsp; |Score &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; |No &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |
|Influence   &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |A numeric score that indicates how well connected a person is within the company. A higher score means that the person is better connected and has greater potential to drive change.|ONA  &nbsp; &nbsp; &nbsp; |Score &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; |No &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |
| <a name="strong-tie-score-definition"></a> Strong tie score &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |A numeric score that indicates how many strong and tight engagements the person has had. For example, a "strong tie" between a manager and a direct report reflects the amount of direct collaboration they have over time. Typically, a person has only a few strong ties because such ties take more effort to maintain. | ONA  &nbsp; &nbsp; &nbsp; |Score &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; |No &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |
| <a name="strong-tie-type-definition"></a> Strong tie type &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |A numeric score that indicates the relative strength of the person's strong ties. 0 means the tie is not very strong; 2 means that the tie is somewhat strong; 1 means that the tie's strength is significant. | ONA  &nbsp; &nbsp; &nbsp; |Score &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; |No &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |




