---

ROBOTS: NOINDEX,NOFOLLOW
title: Insight metrics
description: Describes the data metrics used in Workplace Analytics insights
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
ms.prod: wpa

---
# Metrics used in Workplace Analytics insights

*This experience is only available through private preview at this time.*

The following describes the metrics used in the behavioral percentage and visual insights within each business outcome.

|Metric |Description |Data type |
|------|-----------|----------|---------|------------|
|<a name="after-hours-collaboration-define"></a> After hours collaboration |Number of hours the person spent in calls, instant messages, meetings, and on email outside of working hours. |Hour|
| <a name="attendee-meeting-hours-define"></a> Attendee meeting hours|Total number of adjusted meeting hours for all attendees. |Hour|
| <a name="attendees-define"></a> Attendees|Number of people who attended the meeting.|Count|
|Attendees multitasking|Number of attendees that sent emails during the meeting.<ul><li>In meetings of one hour or less, two or more emails.</li><li>In meetings longer than one hour, two emails per hour. For example: Sending four emails during a two-hour meeting would count as multitasking.</li></ul>|Count|
| <a name="attendees-with-conflicting-meeting-define"></a> Attendees with conflicting meeting |Number of attendees with meetings that overlap with the meeting (includes all non-declined meetings, which include accepted, tentative, and no responses to meeting invites).|Count|
|<a name="collaboration-hours-define"></a> Collaboration hours|Number of hours the person spent in meetings and on email with at least one other person. Collaboration hours include both internal and external hours. |Hour|
|<a name="conflicting-meeting-hours-define"></a> Conflicting meeting hours|Number of meeting hours where the person had overlapping meetings in their calendar. The count includes the entire duration of all overlapping meetings, not just the amount of time that overlaps. (This number includes all non-declined meeting times, which includes accepted, tentative, or no responses to meeting invitations.)|Hour|
|<a name="external-collaboration-define"></a> External collaboration hours |Number of hours the person spent in meetings and on email with at least one person outside the company (as defined by the participant’s email domains).|Hour|
|<a name="external-network-define"></a> External network size |The number of people external to the company with whom the person had at least two meaningful interactions in the last four weeks.|Count|
| <a name="influence-define"></a> Influence |A numeric score that indicates how well connected a person is within the company. A higher score means that the person is better connected and has greater potential to drive change. (A person’s connection score is based on the frequency of collaboration activities, which include emails, [meetings](glossary.md#meeting-define), Teams [calls](glossary.md#call-define), and Teams chats with other people within the company.) |Score |
|Invitees|Number of people invited to the meeting.|Count|
|<a name="low-quality-meeting-hours-define"></a> Low-quality meeting hours |Number of meeting hours in which an attendee multitasked, attended a *conflicting meeting*, or attended a meeting that exhibits *Redundancy (organizational)*. Workplace Analytics admins set the hourly rate of low-quality meeting time; if this value has not been set, the cost defaults to $75 per person hour. **Note**: Calculations for conflicting meeting hours are affected by meeting exclusion rules and adjustments based on the type of meetings that overlap (non-declined work meetings, focus hours, and out-of-office time).|Hour|
|<a name="meeting-hours-define"></a>Meeting hours|Number of hours the person spent in meetings with at least one other person.|Hour|
|Meeting hours during working hours|Number of hours the person spent in meetings, during working hours, with at least one other person.|Hour|
| <a name="meeting-hours-with-manager-define"></a> Meeting hours with manager | Number of meeting hours where attendees included at least the person and their manager.|Hour|
| <a name="meeting-hours-with-manager-1-1-define"></a> Meeting hours with manager 1:1|Number of meeting hours involving only the person and their manager.|Hour|
<a name="multitasking-meeting-hours-define"></a> Multitasking meeting hours|Number of meeting hours where the person sent:<ul><li>Two or more emails sent per meeting hour</li><li>Two or more emails sent per meeting for meetings less than one hour</li></ul>|Hour|
|Networking outside company|The number of distinct external domains outside the company a person has had at least two [meaningful interactions](glossary.md#meaningful-interaction-define) in the last four weeks. |Count|
|Redundant attendees | The number of attendees in a meeting who are redundant, as defined by the _Redundant meeting hours (lower level)_ metric. |Count|
|Redundant meeting hours (lower level) |Number of meeting hours a person spent in a meeting with both their manager and their skip-level manager present in the meeting. <br> <br> This metric is _not_ used in calculating *Low-quality meeting hours*. | Hour|
|<a name="redundant-meeting-hours-define"></a> Redundant meeting hours (organizational) |Number of meeting hours a person spent with attendees from three or more distinct levels within that person’s organization. Used in calculating *Low quality meeting hours*. |Hour|
|Total calls | Total number of calls a person joined through Teams, including scheduled and unscheduled calls during and outside of working hours (as set in Outlook). | Count |
|Total email sent during meeting | Number of emails the person sent during meetings. |Count|
|<a name="focus-define"></a> Total focus hours|Total number of hours with two or more hour blocks of time where the person had no meetings.|Hour|
|Total meeting cost|The total cost of all attendees in a meeting. The meeting cost for each attendee is defined as the product of the attendees' meeting hours multiplied by the attendees' hourly rates. If no hourly rate is available for one or more attendees, the default rate of $75/hr (US dollars) is used to calculate the cost of those attendees.|Currency|
|Total redundant hours|The total number of redundant hours metric for all attendees in a meeting.|Hour|
|Working hours collaboration hours|Number of hours the person spent in meetings and sending emails during working hours.|Hour
|Working hours email hours|Number of hours the person spent in sending email during working hours.|Hour|
|Working hours in calls| Total number of hours a person spent time in scheduled and unscheduled calls with Teams, during working hours. | Hour|
|Working hours instant messages| Total number of hours a person spent time in instant messages through Teams, during working hours. | Hour|
| <a name="workweek-span-define"></a> Workweek span | The time between the person's first sent email, meeting attended, or Teams call or chat, and the last email, meeting, call, or chat for each day of the work week. The total number of hours are based on the person’s work week that is set in Outlook, which the user can change at any time. If a work week is not defined in Outlook (or if Workplace Analytics is unable to access a user's Outlook settings), the totals are based on the default of Monday through Friday, with a minimum of four hours and a maximum of 16 hours per day. If reported for the week, the metric is a sum of the daily values for the week. If reported for the month, the metric is the sum of the daily values for the month. |Hour|

