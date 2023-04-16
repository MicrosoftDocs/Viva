---
ms.date: 03/03/2023
title: Advanced insights metric descriptions
description: Describes the metrics for analysis data that are available in Microsoft Viva Insights, including query metrics and Power BI template metrics
author: madehmer
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
manager: helayne
audience: Admin
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 

---

# Advanced insights metrics

When you create queries in the Microsoft Viva Insights advanced insights app, you can add these metrics from the **Metrics** pane. We've listed the descriptions alphabetically within each category.

| Category | Name | Description | Data type |
|---|---|---|---|
|<a name="after-hours-collaboration-define"></a> **After-hours collaboration** |  <a name="after-hours-collaboration-define"></a> After-hours collaboration hours | Number of hours a person spent in meetings, emails, Teams chats, and Teams calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting), outside of working hours. | Hour |
| | <a name="after-hours-email-hours-define"></a>  After-hours email hours | Number of hours a person spent sending and receiving emails outside of working hours. | Hour |
| | <a name="after-hours-call-hours-define"></a>  After-hours call hours | Number of hours a person spent in scheduled and unscheduled Teams calls, outside of working hours. For calls that started during working hours, this number only includes the part of the call that occurred outside of that person’s work schedule. | Hour |
| | <a name="after-hours-unscheduled-call-hours-define"></a>  After-hours unscheduled call hours | Number of hours a person spent in unscheduled Teams calls, outside of working hours. For calls that started during working hours, this number only includes the part of the call that occurred outside of that person’s work schedule. | Hour |
| | <a name="after-hours-scheduled-call-hours-define"></a> After-hours scheduled call hours | Number of hours a person spent in scheduled Teams calls, outside of working hours. For calls that started during working hours, this number only includes the part of the call that occurred outside of that person’s work schedule. | Hour |
| | <a name="after-hours-chat-hours-define"></a>  After-hours chat hours | Number of hours a person spent in Teams chats outside of working hours. | Hour |
| | <a name="after-hours-meeting-hours-define"></a>  After-hours meeting hours | Number of hours a person spent in meetings with at least one other person, outside of working hours. | Hour |
| <a name="collaboration-activity-define"></a> **Collaboration activity** | <a name="collaboration-hours-define"></a>  Collaboration hours | Number of hours a person spent in meetings, emails, Teams chats, and Teams calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
|| <a name="collaboration-span-define"></a> Collaboration span| Number of hours a person spent in work sessions, including those before, during, and after working hours as set in Outlook. *During* working hours, a work session is the time between the first and last collaboration activity. *Before* or after working hours, a work session is the time that one activity takes from start to finish, unless another activity starts within one hour. In that case, the session lasts from the beginning of the first to the end of the second activity.|Hour|
| | <a name="email-hours-define"></a>  Email hours | Number of hours a person spent sending and receiving emails. | Hour |
| | <a name="meeting-hours-define"></a>  Meeting hours | Number of hours a person spent in meetings with at least one other person during and outside of working hours. | Hour |
| | <a name="chat-hours-define"></a>  Chat hours | Number of hours a person spent in Teams chats with at least one other person, during and outside of working hours. | Hour |
| | <a name="call-hours-define"></a>  Call hours | Number of hours a person spent in scheduled and unscheduled Teams calls with at least one other person, during and outside of working hours. | Hour |
| | <a name="unscheduled-call-hours-define"></a>  Unscheduled call hours | Number of hours a person spent in unscheduled Teams calls with at least one other person, during and outside of working hours. | Hour |
| | <a name="scheduled-call-hours-define"></a>  Scheduled call hours | Number of hours a person spent in scheduled Teams calls with at least one other person, during and outside of working hours. | Hour |
| | <a name="multitasking-hours-define"></a>  Multitasking hours | Number of hours a person spent sending or reading emails or chats during a meeting or a Teams call. | Hour |
| | <a name="emails-sent-define"></a> Emails sent | Number of emails a person sent. | Count |
| | <a name="meetings-define"></a>  Meetings | Number of meetings a person attended. | Count |
| | <a name="chats-sent-define"></a>  Chats sent | Number of Teams chats a person sent. | Count |
| | <a name="calls-define"></a>  Calls | Number of Teams calls a person joined, including scheduled and unscheduled calls. | Count |
| | <a name="meeting-and-call-hours-define"></a>  Meeting and call hours | Number of hours a person spent in meetings and Teams calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities. | Hour |
|<a name="collaboration-by-day-of-the-week-define"></a> **Collaboration by day of the week** | <a name="weekend-emails-sent-define"></a>  Weekend emails sent | Number of emails a person sent on Saturdays or Sundays. | Hour |
| | <a name="weekend-chats-sent-define"></a>  Weekend chats sent | Number of Teams chats a person sent on Saturdays or Sundays. | Hour |
| | <a name="weekend-meetings-define"></a>  Weekend meetings | Number of meetings a person attended during Saturdays or Sundays. | Count |
| | <a name="unscheduled-weekend-calls-define"></a>  Unscheduled weekend calls | Number of unscheduled Teams calls a person joined, on Saturdays or Sundays. | Count |
| | <a name="collaboration-hours-define"></a>  Collaboration hours on *x* (day) | Number of hours a person spent in meetings, emails, Teams chats, and Teams calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting) during the specified day (Monday through Sunday). | Hour |
|<a name="collaboration-by-time-of-day-define"></a> **Collaboration by time of day** | <a name="urgent-email-hours-define"></a>  Urgent email hours | Number of hours a person spent in emails where some level of urgency is involved. Urgency is defined by a set of urgent keywords in email subject lines. | Hour |
| | <a name="urgent-meeting-hours-define"></a>  Urgent meeting hours | Number of hours a person spent in meetings where some level of urgency is involved. Urgency is defined by a set of urgent keywords in meeting subject lines. | Hour |
| | <a name="emails-sent-x-define"></a>  Emails sent *x* (hour block) | Number of emails a person sent during a defined hour block. The metric name includes when the defined hour block begins and ends, which is written as two numbers from 00 to 24 (depicting 24 hours in a day). For emails sent between 8AM and 9AM, for example, the metric name would be "Emails sent 08 09." | Count |
| | <a name="chats-sent-x-define"></a>  Chats sent *x* (hour block) | Number of Teams chats a person sent during a defined hour block. The metric name includes when the hour block begins and ends, which is written as two numbers from 00 to 24 (depicting 24 hours in a day). For chats sent between 8AM and 9AM, for example, the metric name would be "Chats" sent 08 09." | Count |
| | <a name="meetings-x-define"></a>  Meetings *x* (hour block) | Number of meetings a person attended during a defined hour block. The metric name includes when the hour block begins and ends, which is written as two numbers from 00 to 24 (depicting 24 hours in a day). For meetings between 8AM and 9AM, for example, the metric name would be "Meetings 08 09." | Count |
| | <a name="unscheduled-calls-x-define"></a>  Unscheduled calls *x* (hour block) | Number of unscheduled Teams calls a person joined with at least one other person during a defined hour block. The metric name includes when the hour block begins and ends, which is written as two numbers from 00 to 24 (depicting 24 hours in a day). For unscheduled calls between 8AM and 9AM, for example, the metric name would be "Unscheduled calls 08 09." | Count |
| <a name="collaboration-in-small-groups-define"></a> **Collaboration in small groups** | <a name="small-group-meeting-call-and-chat-hours-define"></a>  Small-group meeting, call, and chat hours | Number of hours a person spent in meetings, Teams chats, and unscheduled Teams calls with between two to eight people, all internal, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| | <a name="small-group-emails-sent-excluding-manager-define"></a>  Small-group emails sent, excluding manager | Number of emails a person sent to an internal group of eight or less people, including the sender and excluding the sender's manager from the recipient group. | Count |
| | <a name="small-group-chats-sent-excluding-manager-define"></a> Small-group chats sent, excluding manager | Number of Teams chats a person sent to an internal group of eight or less people, including the sender and excluding the sender’s manager from the recipient group. | Count |
| | <a name="internal-meeting-hours-without-manager-1-1-define"></a> Internal meeting hours without manager 1:1 | Number of hours a person spent in meetings with only one other person who is not their manager. | Hour |
| | <a name="internal-meeting-hours-with-3-to-8-attendees-define"></a> Internal meeting hours with 3 to 8 attendees | Number of hours a person spent in meetings with at least three and up to eight internal collaborators only and no external collaborators. | Hour |
| <a name="collaboration-involving-manager-define"></a> **Collaboration involving manager** | <a name="unscheduled-call-hours-with-manager-1-1-define"></a> Unscheduled call hours with manager 1:1 | Number of hours a person spent in unscheduled Teams calls involving only the person and their manager. | Hour |
| | <a name="unscheduled-call-hours-with-manager-define"></a> Unscheduled call hours with manager | Number of hours a person spent in unscheduled Teams calls where attendees included the person, their manager, and one or more other people (not a one-on-one meeting). | Hour |
| | <a name="collaboration-hours-with-direct-reports-define"></a> Collaboration hours with direct reports | Number of hours a person spent in meetings, emails, Teams chats, and Teams calls where all participants report directly to the person, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| | <a name="small-group-emails-sent-including-manager-define"></a> Small-group emails sent, including manager | Number of emails a person sent to an internal group of eight or less people, including the sender and the sender's manager in the recipient group. | Count |
| | <a name="small-group-chats-sent-including-manager-define"></a> Small-group chats sent, including manager | Number of Teams chats a person sent to an internal group of eight or less people, including the sender and the sender's manager in the recipient group. | Count |
| | <a name="manager-coaching-hours-1-1-define"></a> Manager coaching hours 1:1 | Number of hours a manager spent in one-on-one meetings with all of the manager's direct reports. | Hour |
| | <a name="meeting-hours-with-manager-define"></a> Meeting hours with manager | Number of meeting hours where attendees included the person, their manager, and one or more other people (not a one-on-one meeting). | Hour |
| | <a name="meeting-hours-with-manager-1-1-define"></a> Meeting hours with manager 1:1 | Number of meeting hours involving only the person and their manager. | Hour |
| | <a name="meeting-hours-with-skip-level-define"></a> Meeting hours with skip level | Number of meeting hours a person attended where their manager's manager also attended the meeting. | Hour |
| | <a name="meetings-with-manager-define"></a> Meetings with manager | Number of meetings a person attended where attendees included a person, their manager, and one or more other people (not a one-on-one meeting). | Count |
| | <a name="meetings-with-manager-1-1-define"></a> Meetings with manager 1:1 | Number of meetings a person attended involving only the person and their manager. | Count |
| | <a name="meetings-with-skip-level-define"></a> Meetings with skip level | Number of meetings a person attended where their manager's manager also attended the meeting. | Count |
|**Collaboration network**|Diverse ties | Number of colleagues who are connected to a person (that is, had a reciprocal interaction with them in the last four weeks) but not connected to many of that person’s other colleagues. Diverse ties offer good sources of new and varied information from across the company. (Interactions are based on emails, meetings, and Teams calls and chats.) | Count
||Strong ties | Number of colleagues who are connected to a person (that is, had a reciprocal interaction with them in the last four weeks) and who are also connected to many of that person’s other colleagues. (Interactions are based on emails, meetings, and Teams calls, and Teams chats.) |Count |
||Internal network size|Number of people within the organization with whom a person has had a reciprocal interaction in the past four weeks.|Count |
| <a name="external-collaboration-define"></a> **External collaboration** | <a name="external-collaboration-hours-define"></a> External collaboration hours | Number of hours a person spent in meetings, emails, Teams chats, and Teams calls with at least one other person outside the company, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| | <a name="external-unscheduled-call-hours-define"></a> External unscheduled call hours | Number of hours a person spent in unscheduled Teams calls with at least one other person outside the company. | Hour |
| | <a name="external-email-hours-define"></a> External email hours | Number of hours a person spent in emails with at least one other person outside the company. | Hour |
| | <a name="external-chat-hours-define"></a>  External chat hours | Number of hours a person spent in Teams chats with at least one other person outside the company. | Hour |
| |  <a name="external-meeting-hours-define"></a> External meeting hours | Number of hours a person spent in meetings with at least one other person outside the company. | Hour |
| <a name="focus-define"></a> **Focus**|  <a name="available-to-focus-hours-define"></a>  Available-to-focus hours | Hours remaining during working hours after excluding meetings and scheduled Teams calls for focused work. This metric helps organizations understand how meetings and scheduled Teams calls can impact what time is available for self-directed work. | Hour |
| | <a name="uninterrupted-hours-define"></a> Uninterrupted hours | Sum of blocks one hour or longer where a person didn’t attend a meeting, read or send emails, read or send Teams chats, or initiate or receive Teams calls. In other words, Uninterrupted hours is the sum of blocks of time one hour or longer for deep thinking with no communication. This metric helps organizations understand whether employees have long blocks of uninterrupted time for deep thinking to solve new problems creatively and to fuel innovation. | Hour |
| | <a name="interrupted-hours-define"></a> Interrupted hours | Available-to-focus hours interrupted by emails, Teams chats, or unscheduled Teams calls. Interrupted hours excludes one-hour or longer blocks of Uninterrupted hours for deep work. This metric helps organizations understand whether employees are choosing to use the blocks of time between meetings or scheduled Teams calls for emails, unscheduled calls, or Teams chats. | Hour |
|**Impact**|Booked focus hours | Number of hours a person booked as [focus time](../../personal/teams/focus.md) in Viva Insights. Other appointments or meetings that employees added to their Outlook calendar without using Viva Insights aren’t counted. | Hour
||Booked focus hours kept |Number of hours a person booked as focus time in Viva Insights that didn’t overlap with meetings, including time booked with and without a focus plan. | Hour
||Booked focus hours kept with plan |Number of hours a person booked in Viva Insights, using a focus plan, that didn’t overlap with meetings. | Hour
||Booked focus hours kept without plan | Number of days a person booked as no-meeting days in Viva Insights.  |Hour
||Booked no-meeting days | Number of days a person booked as [no-meeting days](../../personal/teams/shared-no-meeting-day.md) in Viva Insights.  | Hour
|<a name="meeting-hours-on-time-and-advanced-notice-define"></a> **Meetings on time and with advanced notice**| <a name="meeting-hours-with-12-to-24-hours-of-advanced-notice-define"></a> Meeting hours with 12 to 24 hours of advanced notice | Number of meeting hours that were scheduled more than 12 and less than 24 hours before the meeting start time. | Hour
||<a name="meeting-hours-with-24-or-more-hours-of-advanced-notice-define"></a> Meeting hours with 24 or more hours of advanced notice |Number of meeting hours that were scheduled 24 hours or more before the meeting start time. | Hour|
||<a name="meeting-hours-with-six-or-fewer-hours-of-advanced-notice-define"></a>Meeting hours with six or fewer hours of advanced notice | Number of meeting hours that were scheduled six hours or before the meeting start time. | Hour
||<a name="meeting-hours-with-six-to-12-hours-of-advanced-notice-define"></a>Meeting hours with six to 12 hours of advanced notice | Number of meeting hours that were scheduled more than six and less than or equal to 12 hours before the meeting start time. | Hour|
||<a name="meeting-hours-joined-on-time-define"></a>Meeting hours joined on time| Number of Teams meeting hours that were joined early or within five minutes after the scheduled start time. | Hour
||<a name="meeting-hours-ended-on-time-define"></a> Meeting hours ended on time |Number of Teams meeting hours that were ended early or within one minute after the scheduled end time. | Hour|
||<a name="meeting-hours-not-ended-on-time-define"></a>Meeting hours not ended on time |Number of Teams meetings hours that were ended after one minute past the scheduled end time. |Hour
||<a name="meeting-hours-not-joined-on-time-define"></a>Meeting hours not joined on time |Number of Teams meetings hours that were joined after five minutes past the scheduled start time. | Hour
|<a name="meeting-types-define"></a> **Meeting types** | <a name="conflicting-meeting-hours-define"></a> Conflicting meeting hours | Number of meeting hours where a person had overlapping meetings in their calendar. The count includes just the amount of time that overlaps. | Hour |
| |  <a name="small-and-short-meeting-hours-define"></a>  Small and short meeting hours | Meeting hours with a duration of one hour or less that have at least two and up to eight invitees, including the organizer. | Hour |
| |  <a name="small-and-short-recurring-meeting-hours-define"></a> Small and short recurring meeting hours | Recurring meeting hours with a duration of one hour or less that have at least two and up to eight invitees, including the organizer. | Hour |
| |  <a name="large-and-long-meeting-hours-define"></a>  Large and long meeting hours | Meeting hours with a duration of more than one hour and nine or more invitees, including the organizer. | Hour |
| |  <a name="large-and-long-recurring-meeting-hours-define"></a> Large and long recurring meeting hours | Recurring meeting hours with a duration of more than one hour and nine or more invitees, including the organizer. | Hour |
| |  <a name="large-and-short-meeting-hours-define"></a> Large and short meeting hours | Meeting hours with a duration of one hour or less and nine or more invitees, including the organizer. | Hour |
| | <a name="large-and-short-recurring-meeting-hours-define"></a> Large and short recurring meeting hours | Recurring meeting hours with a duration of one hour or less and nine or more invitees, including the organizer. | Hour |
| | <a name="small-and-long-meeting-hours-define"></a>Small and long meeting hours | Meeting hours with a duration of more than one hour that have at least two and up to eight invitees, including the organizer. | Hour |
| | <a name="small-and-long-recurring-meeting-hours-define"></a> Small and long recurring meeting hours | Recurring meeting hours with a duration of more than one hour that have at least two and up to eight invitees, including the organizer. | Hour |
| | <a name="recurring-meeting-hours-define"></a> Recurring meeting hours | Meeting hours for meetings that are set to recur. | Hour |
|**Meeting quality**|Number of attendees who ended the meeting on time|Number of attendees that left a Teams meeting early or within one minute after the scheduled end time|Count
||Number of attendees who didn’t end the meeting on time|Number of attendees who left a Teams meeting after one minute past the scheduled end time.|Count |
||Number of attendees who joined the meeting on time|Number of attendees who joined a Teams meeting early or within five minutes after the scheduled start time.|Count|
||Number of attendees who didn’t join the meeting on time|Number of attendees who joined a Teams meeting after five minutes past the scheduled start time.|Count|
| <a name="working-hours-collaboration-define"></a> **Working-hours collaboration** | <a name="working-hours-collaboration-hours-define"></a> Working-hours collaboration hours | Number of hours a person spent in meetings, emails, Teams chats, and Teams calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting), during working hours. | Hour |
| | <a name="working-hours-email-hours-define"></a> Working-hours email hours | Number of hours a person spent sending and receiving emails during working hours | Hour |
| | <a name="working-hours-call-hours-define"></a> Working-hours call hours | Number of hours a person spent in scheduled and unscheduled Teams calls, during working hours. | Hour |
| | <a name="working-hours-chat-hours-define"></a> Working-hours chat hours | Number of hours a person spent in Teams chats during working hours. | Hour |
| | <a name="working-hours-meeting-hours-define"></a> Working-hours meeting hours | Number of hours a person spent in meetings with at least one other person, during working hours. | Hour |


## Exported metrics

These metrics aren't selectable within the **Metrics** pane when you build queries, but they're included in query output.

Applies to|Name| Description|
|---|-------|------------|
|Person queries |IsActive | Boolean value of "true" or "false" for each employee. Active employees send at least one email or Teams chat during the unit of time—day, week, or month<sup>1</sup>—defined by the query’s **Group by** setting. 

<sup>1. You might notice differences when comparing metrics summarized by day with metrics summarized by week; a person can be active in a week, but not necessarily active seven days of the week.</sup>

