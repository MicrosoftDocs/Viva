---
ms.date: 1/17/2024
title: Advanced insights metric descriptions
description: Describes the metrics for analysis data that are available in Microsoft Viva Insights, including query metrics and Power BI template metrics
author: zachminers
ms.author: v-zachminers
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
|<a name="after-hours-collaboration-define"></a> **After-hours collaboration** |  <a name="after-hours-channel-message-hours-define"></a> After-hours channel message hours | Number of hours a person spent posting, replying to, or reading Teams channels messages outside of working hours. | Hour |
| | <a name="after-hours-collaboration-hours-define"></a>  After-hours collaboration hours | Number of hours a person spent in meetings, emails, Teams chats, Teams calls, and Teams channels with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting), outside of working hours. | Hour |
| | <a name="after-hours-email-hours-define"></a>  After-hours email hours | Number of hours a person spent sending and receiving emails outside of working hours. | Hour |
| | <a name="after-hours-call-hours-define"></a>  After-hours call hours | Number of hours a person spent in scheduled and unscheduled Teams calls, outside of working hours. For calls that started during working hours, this number only includes the part of the call that occurred outside of that person’s work schedule. | Hour |
| | <a name="after-hours-unscheduled-call-hours-define"></a>  After-hours unscheduled call hours | Number of hours a person spent in unscheduled Teams calls, outside of working hours. For calls that started during working hours, this number only includes the part of the call that occurred outside of that person’s work schedule. | Hour |
| | <a name="after-hours-scheduled-call-hours-define"></a> After-hours scheduled call hours | Number of hours a person spent in scheduled Teams calls, outside of working hours. For calls that started during working hours, this number only includes the part of the call that occurred outside of that person’s work schedule. | Hour |
| | <a name="after-hours-chat-hours-define"></a>  After-hours chat hours | Number of hours a person spent in Teams chats outside of working hours. | Hour |
| | <a name="after-hours-meeting-hours-define"></a>  After-hours meeting hours | Number of hours a person spent in meetings with at least one other person, outside of working hours. | Hour |
| <a name="collaboration-activity-define"></a> **Collaboration activity** |<a name="active-connected-hours-define"></a>Active connected hours| Sum of half-hour blocks where a person remains active. An active block is defined as having at least one meeting or Teams call, email sent, Teams chat sent, or Teams channel message post or reply with at least one other person, either internal or external, during that block.| Hour| 
||<a name="channel-message-hours-define"></a> Channel message hours | Number of hours a person spent posting, replying to, or reading Teams channels messages. | Hour |
||<a name="channel-message-posts-define"></a> Channel message posts | Number of messages posted on Teams channels. | Count |
||<a name="channel-message-reactions-define"></a> Channel message reactions | Number of reactions to posts and replies to messages on Teams channels. | Count |
||<a name="channel-message-replies-define"></a> Channel message replies | Number of replies to messages on Teams channels. | Count |
||<a name="channel-visits-define"></a> Channel visits | Number of visits to Teams channels. | Count |
||<a name="collaboration-hours-define"></a> Collaboration hours | Number of hours a person spent in meetings, emails, Teams chats, Teams calls, and Teams channels with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting).| Hour |
|| <a name="collaboration-span-define"></a> Collaboration span| Number of hours a person spent in work sessions, including those before, during, and after working hours as set in Outlook. *During* working hours, a work session is the time between the first and last collaboration activity. *Before* or after working hours, a work session is the time that one activity takes from start to finish, unless another activity starts within one hour. In that case, the session lasts from the beginning of the first to the end of the second activity.|Hour|
| | <a name="email-hours-define"></a>  Email hours | Number of hours a person spent sending and receiving emails. | Hour |
| | <a name="meeting-hours-define"></a>  Meeting hours | Number of hours a person spent in meetings with at least one other person during and outside of working hours. | Hour |
| | <a name="chat-hours-define"></a>  Chat hours | Number of hours a person spent in Teams chats with at least one other person, during and outside of working hours. | Hour |
| | <a name="call-hours-define"></a>  Call hours | Number of hours a person spent in scheduled and unscheduled Teams calls with at least one other person, during and outside of working hours. | Hour |
| | <a name="unscheduled-call-hours-define"></a> Unscheduled call hours | Number of hours a person spent in unscheduled Teams calls with at least one other person, during and outside of working hours. | Hour |
| | <a name="scheduled-call-hours-define"></a>  Scheduled call hours | Number of hours a person spent in scheduled Teams calls with at least one other person, during and outside of working hours. | Hour |
| | <a name="multitasking-hours-define"></a> Multitasking hours | Number of hours a person spent sending or reading emails or chats, posting or replying to Teams channels messages, or visiting Teams channels during a meeting or a Teams call. | Hour |
| | <a name="emails-sent-define"></a> Emails sent | Number of emails a person sent. | Count |
| | <a name="meetings-define"></a>  Meetings | Number of meetings a person attended. | Count |
| | <a name="chats-sent-define"></a>  Chats sent | Number of Teams chats a person sent. | Count |
| | <a name="calls-define"></a>  Calls | Number of Teams calls a person joined, including scheduled and unscheduled calls. | Count |
| | <a name="meeting-and-call-hours-define"></a>  Meeting and call hours | Number of hours a person spent in meetings and Teams calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities. | Hour |
| | <a name="time-with-leadership-define"></a> Time with leadership | Number of hours a person spent in meetings, emails, Teams chats, Teams calls, and Teams channels with people who are skip level or above up to six levels in the organization chart. | Hour |
| | <a name="urgent-email-hours-define"></a>  Urgent email hours | Number of hours a person spent in emails where some level of urgency is involved. Urgency is defined by a set of urgent keywords in email subject lines. | Hour |
| | <a name="urgent-meeting-hours-define"></a> Urgent meeting hours | Number of hours a person spent in meetings where some level of urgency is involved. Urgency is defined by a set of urgent keywords in meeting subject lines. | Hour |
|<a name="collaboration-by-day-of-the-week-define"></a> **Collaboration by day of the week** | <a name="meeting-hours-on-x-define"></a>  Meeting hours on *x* (day) | Number of hours a person spent in meetings with at least one other person during and outside of working hours on the specified day (Monday through Sunday). | Hour |
| | <a name="weekend-emails-sent-define"></a>  Weekend emails sent | Number of emails a person sent on Saturdays or Sundays. | Count |
| | <a name="weekend-channel-message-posts-define"></a>  Weekend channel message posts | Number of messages a person posted on Teams channels during Saturdays or Sundays. | Count |
| | <a name="weekend-channel-message-replies-define"></a>  Weekend channel message replies | Number of messages a person replied to on Teams channels during Saturdays or Sundays. | Count |
| | <a name="weekend-chats-sent-define"></a>  Weekend chats sent | Number of Teams chats a person sent on Saturdays or Sundays. | Hour |
| | <a name="weekend-collaboration-hours-define"></a>  Weekend collaboration hours | Number of hours a person spent in meetings, emails, Teams chats, Teams calls, and Teams channels on Saturdays and Sundays. | Hour |
| | <a name="weekend-meetings-define"></a>  Weekend meetings | Number of meetings a person attended during Saturdays or Sundays. | Count |
| | <a name="unscheduled-weekend-calls-define"></a>  Unscheduled weekend calls | Number of unscheduled Teams calls a person joined, on Saturdays or Sundays. | Count |
| | <a name="collaboration-hours-define"></a>  Collaboration hours on *x* (day) | Number of hours a person spent in meetings, emails, Teams chats, Teams calls, and Teams channels with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting) during the specified day (Monday through Sunday). | Hour |
|<a name="collaboration-by-time-of-day-define"></a> **Collaboration by time of day** | <a name="emails-sent-x-define"></a>  Emails sent *x* (hour block) | Number of emails a person sent during a defined hour block. The metric name includes when the defined hour block begins and ends, which is written as two numbers from 00 to 24 (depicting 24 hours in a day). For emails sent between 8AM and 9AM, for example, the metric name would be "Emails sent 08 09." | Count |
| | <a name="chats-sent-x-define"></a>  Chats sent *x* (hour block) | Number of Teams chats a person sent during a defined hour block. The metric name includes when the hour block begins and ends, which is written as two numbers from 00 to 24 (depicting 24 hours in a day). For chats sent between 8AM and 9AM, for example, the metric name would be "Chats" sent 08 09." | Count |
| | <a name="meetings-x-define"></a>  Meetings *x* (hour block) | Number of meetings a person attended during a defined hour block. The metric name includes when the hour block begins and ends, which is written as two numbers from 00 to 24 (depicting 24 hours in a day). For meetings between 8AM and 9AM, for example, the metric name would be "Meetings 08 09." | Count |
| | <a name="unscheduled-calls-x-define"></a>  Unscheduled calls *x* (hour block) | Number of unscheduled Teams calls a person joined with at least one other person during a defined hour block. The metric name includes when the hour block begins and ends, which is written as two numbers from 00 to 24 (depicting 24 hours in a day). For unscheduled calls between 8AM and 9AM, for example, the metric name would be "Unscheduled calls 08 09." | Count |
| <a name="collaboration-in-small-groups-define"></a> **Collaboration in small groups** | <a name="small-group-meeting-call-and-chat-hours-define"></a>  Small-group meeting, call, and chat hours | Number of hours a person spent in meetings, Teams chats, and unscheduled Teams calls with between two to eight people, all internal, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| | <a name="small-group-emails-sent-excluding-manager-define"></a>  Small-group emails sent, excluding manager | Number of emails a person sent to an internal group of eight or less people, including the sender and excluding the sender's manager from the recipient group. | Count |
| | <a name="small-group-chats-sent-excluding-manager-define"></a> Small-group chats sent, excluding manager | Number of Teams chats a person sent to an internal group of eight or less people, including the sender and excluding the sender’s manager from the recipient group. | Count |
| | <a name="internal-meeting-hours-without-manager-1-1-define"></a> Internal meeting hours without manager 1:1 | Number of hours a person spent in meetings with only one other person who is not their manager. | Hour |
| | <a name="internal-meeting-hours-with-3-to-8-attendees-define"></a> Internal meeting hours with 3 to 8 attendees | Number of hours a person spent in meetings with at least three and up to eight internal collaborators only and no external collaborators. | Hour |
| <a name="collaboration-involving-manager-define"></a> **Collaboration involving manager** | <a name="meeting-and-call-hours-with-manager-define"></a>Meeting and call hours with manager<a name="meeting-and-call-hours-with-manager-define"></a>|Number of hours a person spent in meetings and Teams calls where attendees included the person, their manager, and one or more other people (not a one-on-one meeting or call), after deduplication of time due to overlapping activities. |Hour
| | <a name="meeting-and-call-hours-with-manager-1-1-define"></a> Meeting and call hours with manager 1:1 | Number of hours a person spent in meetings and Teams calls involving only the person and their manager, after deduplication of time due to overlapping activities. | Hour |
| | <a name="meeting-and-call-hours-with-skip-level-define"></a> Meeting and call hours with skip level | Number of hours a person spent in meetings and Teams calls where their manager's manager also attended the meeting or joined the call, after deduplication of time due to overlapping activities. | Hour |
| | <a name="meeting-and-call-hours-with-skip-level-1-1-define"></a> Meeting and call hours with skip level 1:1 | Number of hours a person spent in meetings and Teams calls involving only the person and their skip manager, after deduplication of time due to overlapping activities. | Hour |
| | <a name="redundant-meeting-hours-lower-level-define"></a> Redundant meeting hours (lower level) | Number of meeting hours a person spent in a meeting with both their manager and their skip-level manager present in the meeting. | Hour |
| | <a name="recurring-meeting-hours-with-manager-1-1-define"></a> Recurring meeting hours with manager 1:1 | Number of hours a person spent in recurring meetings involving only the person and their manager. | Hour |
|| Unscheduled call hours with manager 1:1 | Number of hours a person spent in unscheduled Teams calls involving only the person and their manager. | Hour |
| | <a name="unscheduled-call-hours-with-manager-define"></a> Unscheduled call hours with manager | Number of hours a person spent in unscheduled Teams calls where attendees included the person, their manager, and one or more other people (not a one-on-one meeting). | Hour |
| | <a name="unscheduled-call-hours-with-skip-level-define"></a> Unscheduled call hours with skip level | Number of hours a person spent in unscheduled Teams calls where their manager's manager also joined the call. | Hour |
| | <a name="collaboration-hours-with-direct-reports-define"></a> Collaboration hours with direct reports | Number of hours a person spent in meetings, emails, Teams chats, and Teams calls where all participants report directly to the person, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| | <a name="small-group-emails-sent-including-manager-define"></a> Small-group emails sent, including manager | Number of emails a person sent to an internal group of eight or less people, including the sender and the sender's manager in the recipient group. | Count |
| | <a name="small-group-chats-sent-including-manager-define"></a> Small-group chats sent, including manager | Number of Teams chats a person sent to an internal group of eight or less people, including the sender and the sender's manager in the recipient group. | Count |
| | <a name="manager-coaching-hours-1-1-define"></a> Manager coaching hours 1:1 | Number of hours a manager spent in one-on-one meetings with all of the manager's direct reports. | Hour |
| | <a name="meeting-hours-with-manager-define"></a> Meeting hours with manager | Number of meeting hours where attendees included the person, their manager, and one or more other people (not a one-on-one meeting). | Hour |
| | <a name="meeting-hours-with-manager-1-1-define"></a> Meeting hours with manager 1:1 | Number of meeting hours involving only the person and their manager. | Hour |
| | <a name="meeting-hours-with-skip-level-define"></a> Meeting hours with skip level | Number of meeting hours a person attended where their manager's manager also attended the meeting. | Hour |
| | <a name="meetings-with-manager-define"></a> Meetings with manager | Number of meetings a person attended where attendees included a person, their manager, and one or more other people (not a one-on-one meeting). | Count |
| | <a name="meetings-including-manager-and-skip-level-leadership-define"></a> Meetings including manager and skip-level leadership | Number of meetings where a person's manager and skip manager or skip manager's peers also attended. | Count |
| | <a name="meetings-with-manager-1-1-define"></a> Meetings with manager 1:1 | Number of meetings a person attended involving only the person and their manager. | Count |
| | <a name="meetings-with-skip-level-define"></a> Meetings with skip level | Number of meetings a person attended where their manager's manager also attended the meeting. | Count |
|**Collaboration network**|Diverse ties | Number of colleagues who are connected to a person (that is, had a reciprocal interaction with them in the last four weeks) but not connected to many of that person’s other colleagues. Diverse ties offer good sources of new and varied information from across the company. (Interactions are based on emails, meetings, and Teams calls and chats.) | Count
|| Diverse ties score|Diverse ties represent connections with colleagues who are connected to the person but not connected to many of the person’s other colleagues. Diverse ties score measures the relative diversity of a connection between two individuals. (Interactions are based on emails, meetings, Teams calls and chats.) | Score
|| Diverse tie type|A value that indicates the relative diversity of the person's diverse ties. 0 means that the tie is not diverse; 1 means that the tie is diverse; 2 is an intermediate value that means more diverse than 0 but less diverse than 1. (The Diverse tie type metric is derived from the Diverse tie score metric.) | Score
|| External network size|The number of people external to the company with whom a person had a reciprocal interaction in a four-week span. A reciprocal interaction occurs between A & B when both A has reached out to B and B has reached out to A.|Score
|| Influence rank| An employee’s potential influence on opinions of the network. It measures how well connected a person is to other well-connected individuals. The closer the rank is to 1, the higher the person’s rank or network influence score. If two people have the same influence score, they also have the same influence rank. (A person’s influence score is based on the frequency of collaboration activities, which include emails, meetings, Teams calls, and Teams chats with other people within the company.)
||Influence score|A numeric score that indicates how well connected a person is within the company. A higher score means that the person is better connected and has greater potential to drive change. (A person’s connection score is based on the frequency of collaboration activities, which include emails, meetings, Teams calls, and Teams chats with other people within the company.)|Rank
||Internal network size|Number of people within the organization with whom a person has had a reciprocal interaction in the past four weeks.|Count |
||Network outside company|The number of distinct external domains outside the company with at least one individual a person has had a reciprocal interaction with.|Count |
||Network outside organization|The number of distinct internal organizational units within the company with at least one individual a person has had a reciprocal interaction with.|Count |
||Strong ties | Number of colleagues who are connected to a person (that is, had a reciprocal interaction with them in the last four weeks) and who are also connected to many of that person’s other colleagues. (Interactions are based on emails, meetings, and Teams calls, and Teams chats.) |Count 
||Strong ties score | Strong ties represent connections with people that are part of a person’s inner working group who work together regularly. Strong ties score measures the relative strength of a connection between two individuals. (Interactions are based on emails, meetings, Teams calls and chats.) |Score
||Strong tie type | A value that indicates the relative strength of the person's strong ties. 0 means that the tie is not strong; 1 means that the tie is strong; 2 is an intermediate value that means stronger than 0 but weaker than 1. (The Strong tie type metric is derived from the Strong tie score metric.) | Score |
|**Group-to-Group**|Group collaboration time invested | Sum of time spent by each member of group A collaborating with any member of group B | Minutes
|| % Group collaboration time invested | % of a group A’s total collaboration time that is spent with any member of group B | Percentage
|| Group meeting time invested | Sum of time spent by each member of group A in a meeting with any member of group B | Minutes
|| Group mail time invested | Sum of time spent by each member of group A in sending mails to or reading mails from any member of group B | Minutes
|**Person-to-Group**|Collaboration time invested | Time spent by a person collaborating with any member of a collaborator group | Minutes
|| Meeting time invested | Time spent by a person in a meeting with any member of a collaborator group | Minutes
|| Mail time invested | Time spent by a person sending mails to or reading mails from any member of a collaborator group | Minutes
| <a name="external-collaboration-define"></a> **External collaboration** | <a name="external-channel-message-hours-define"></a> External channel message hours | Number of hours a person spent posting, replying to or reading messages in Teams channels with at least one other person outside the company. | Hour |
| | <a name="external-collaboration-hours-define"></a> External collaboration hours | Number of hours a person spent in meetings, emails, Teams chats, Teams calls, and Teams channels with at least one other person outside the company, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| | <a name="external-unscheduled-call-hours-define"></a> External unscheduled call hours | Number of hours a person spent in unscheduled Teams calls with at least one other person outside the company. | Hour |
| | <a name="external-email-hours-define"></a> External email hours | Number of hours a person spent in emails with at least one other person outside the company. | Hour |
| | <a name="external-chat-hours-define"></a>  External chat hours | Number of hours a person spent in Teams chats with at least one other person outside the company. | Hour |
| |  <a name="external-meeting-hours-define"></a> External meeting hours | Number of hours a person spent in meetings with at least one other person outside the company. | Hour |
| |  <a name="external-1-1-meeting-hours-define"></a> External 1:1 meeting hours | Number of hours a person spent in meetings where the only other participant was an external person. | Hour |
| |  <a name="external-meetings-including-manager-define"></a> External meetings including manager | Number of meetings where a person and their manager met with at least one person outside of the company. | Count |
| <a name="focus-define"></a> **Focus**|  <a name="available-to-focus-hours-define"></a>  Available-to-focus hours | Hours remaining during working hours after excluding meetings and scheduled Teams calls for focused work. This metric helps organizations understand how meetings and scheduled Teams calls can impact what time is available for self-directed work. | Hour |
| | <a name="uninterrupted-hours-define"></a> Uninterrupted hours | Sum of blocks one hour or longer where a person didn't attend a meeting, read or send emails, read or send Teams chats, joined Teams calls, posted or replied to Teams channels messages, or visited Teams channels. In other words, Uninterrupted time is the sum of blocks of time one hour or longer for deep thinking with no communication. This metric helps organizations understand whether employees have long blocks of uninterrupted time for deep thinking to solve new problems creatively and to fuel innovation. | Hour |
| | <a name="interrupted-hours-define"></a> Interrupted hours | Time available to focus that was interrupted by emails, Teams chats, unscheduled Teams calls, or Teams channels activity. Interrupted time excludes one-hour or longer blocks of uninterrupted time for deep work. This metric helps organizations understand whether employees are choosing to use the blocks of time between meetings or scheduled Teams calls for emails, unscheduled calls, or Teams chats. | Hour |
||<a name="open-1-hour-block-define"></a> Open 1-hour block | <a name="weekend-emails-sent-define"></a>  Number of open one-hour blocks in a person’s calendar without any scheduled meetings during the workday. | Count |
| <a name="generated-load-define"></a> **Generated load**|  <a name="generated-load-call-hours-define"></a>  Generated load - Call hours | Number of Teams calls hours that the person created for internal participants by initiating Teams calls. | Hour |
| | <a name="generated-load-call-participants-define"></a> Generated load – Call participants | Number of internal participants of Teams calls that were initiated by a person. | Count |
| | <a name="generated-load-calls-organized-define"></a> Generated load – Calls organized | Number of internal Teams calls that were initiated by a person. | Count |
| | <a name="generated-load-channel-message-reactions-define"></a> Generated load – Channel message reactions | Number of reactions to messages posted or replies to messages by the person on Teams channels. | Count |
| | <a name="generated-load-channel-message-replies-define"></a> Generated load – Channel message replies | Number of replies to messages posted by the person on Teams channels. | Count |
| | <a name="generated-load-chat-recipients-define"></a> Generated load – Chat recipients | Number of internal recipients who read Teams chats sent by a person. | Count |
| | <a name="generated-load-chats-read-hours-define"></a> Generated load – Chats-read hours | Number of hours that internal recipients spent reading Teams chats sent by a person. | Hour |
| | <a name="generated-load-email-recipients-define"></a> Generated load – Email recipients | Number of internal recipients who read emails sent by a person. | Count |
| | <a name="generated-load-emails-read-hours-define"></a> Generated load – Emails-read hours | Number of hours that internal recipients spent reading emails sent by a person. | Hour |
| | <a name="generated-load-meeting-attendees-define"></a> Generated load – Meeting attendees | Number of internal attendees in meetings that were organized by a person. | Count |
| | <a name="generated-load-meeting-hours-define"></a> Generated load – Meeting hours | Number of meeting hours that a person created for internal attendees by organizing meetings. | Hour |
| | <a name="generated-load-meetings-organized-define"></a> Generated load – Meetings organized | Number of internal meetings that were organized by a person. | Count |
|**Impact**|Booked focus hours | Number of hours a person booked as [focus time](../../personal/teams/focus.md) in Viva Insights. Other appointments or meetings that employees added to their Outlook calendar without using Viva Insights aren’t counted. | Hour
||Booked focus hours kept |Number of hours a person booked as focus time in Viva Insights that didn’t overlap with meetings, including time booked with and without a focus plan. | Hour
||Booked focus hours kept with plan |Number of hours a person booked in Viva Insights, using a focus plan, that didn’t overlap with meetings. | Hour
||Booked focus hours kept without plan | Number of focus hours a person booked in Viva Insights, without using a focus plan, that didn’t overlap with meetings.  |Hour
||Booked no-meeting days | Number of days a person booked as [no-meeting days](../../personal/teams/shared-no-meeting-day.md) in Viva Insights.  | Day
|**Learning time**| Calendared learning time | Number of hours blocked in a person’s calendar for learning activities. An appointment or meeting is considered a learning activity based on keywords that appear in the subject line. | Hour
|<a name="meeting-types-define"></a> **Meeting types** | <a name="30-to-59-minutes-long-meeting-hours-define"></a> 30 to 59 minutes long meeting hours | Hours of meetings with a duration of 30 to 59 minutes. | Hour |
| |  <a name="30-to-59-minutes-long-meetings-define"></a> 30 to 59 minutes long meetings | Number of meetings with a duration of at least 30 minutes and less than one hour.​ | Count |
| |  <a name="60-minutes-or-longer-meeting-hours-define"></a> 60 minutes or longer meeting hours | Hours of meetings with a duration of 60 minutes or longer. | Hour |
| |  <a name="60-minutes-or-longer-meetings-define"></a> 60 minutes or longer meetings | Number of meetings with a duration of 60 minutes or longer. | Count |
| |  <a name="conflicting-meeting-hours-define"></a> Conflicting meeting hours | Number of meeting hours where a person had overlapping meetings in their calendar. The count includes just the amount of time that overlaps.  | Hour |
| |  <a name="small-and-short-meeting-hours-define"></a>  Small and short meeting hours | Meeting hours with a duration of one hour or less that have at least two and up to eight invitees, including the organizer. | Hour |
| |  <a name="small-and-short-recurring-meeting-hours-define"></a> Small and short recurring meeting hours | Recurring meeting hours with a duration of one hour or less that have at least two and up to eight invitees, including the organizer. | Hour |
| |  <a name="large-and-long-meeting-hours-define"></a>  Large and long meeting hours | Meeting hours with a duration of more than one hour and nine or more invitees, including the organizer. | Hour |
| |  <a name="large-and-long-recurring-meeting-hours-define"></a> Large and long recurring meeting hours | Recurring meeting hours with a duration of more than one hour and nine or more invitees, including the organizer. | Hour |
| |  <a name="large-and-long-recurring-meetings-define"></a> Large and long recurring meetings | Number of recurring meetings that are more than one hour and include nine or more attendees, including the organizer. | Count |
| |  <a name="large-and-short-meeting-hours-define"></a> Large and short meeting hours | Meeting hours with a duration of one hour or less and nine or more invitees, including the organizer. | Hour |
| | <a name="large-and-short-recurring-meeting-hours-define"></a> Large and short recurring meeting hours | Recurring meeting hours with a duration of one hour or less and nine or more invitees, including the organizer. | Hour |
| |<a name="meeting-hours-ended-on-time-define"></a> Meeting hours ended on time |Number of Teams meeting hours that were ended early or within one minute after the scheduled end time. | Hour|
| |<a name="meeting-hours-not-ended-on-time-define"></a>Meeting hours not ended on time |Number of Teams meetings hours that were ended after one minute past the scheduled end time. |Hour|
| |<a name="meeting-hours-joined-on-time-define"></a>Meeting hours joined on time| Number of Teams meeting hours that were joined early or within five minutes after the scheduled start time. | Hour |
| |<a name="meeting-hours-not-joined-on-time-define"></a>Meeting hours not joined on time |Number of Teams meetings hours that were joined after five minutes past the scheduled start time. | Hour |
| | <a name="meeting-hours-with-12-to-24-hours-of-advanced-notice-define"></a> Meeting hours with 12 to 24 hours of advanced notice | Number of meeting hours that were scheduled more than 12 and less than 24 hours before the meeting start time. | Hour |
| |<a name="meeting-hours-with-24-or-more-hours-of-advanced-notice-define"></a> Meeting hours with 24 or more hours of advanced notice |Number of meeting hours that were scheduled 24 hours or more before the meeting start time. | Hour|
| |<a name="meeting-hours-with-six-or-fewer-hours-of-advanced-notice-define"></a>Meeting hours with six or fewer hours of advanced notice | Number of meeting hours that were scheduled six hours or before the meeting start time. | Hour |
| |<a name="meeting-hours-with-six-to-12-hours-of-advanced-notice-define"></a>Meeting hours with six to 12 hours of advanced notice | Number of meeting hours that were scheduled more than six and less than or equal to 12 hours before the meeting start time. | Hour|
| | <a name="small-and-long-meeting-hours-define"></a>Small and long meeting hours | Meeting hours with a duration of more than one hour that have at least two and up to eight invitees, including the organizer. | Hour |
| | <a name="small-and-long-recurring-meeting-hours-define"></a> Small and long recurring meeting hours | Recurring meeting hours with a duration of more than one hour that have at least two and up to eight invitees, including the organizer. | Hour |
| | <a name="recurring-meeting-hours-define"></a> Recurring meeting hours | Meeting hours for meetings that are set to recur. | Hour |
||<a name="time-in-self-organized-meetings-define"></a>Time in self-organized meetings | Number of hours spent in meetings organized by the person with at least one other person. | Hour |
|**Meeting quality**|Number of attendees who ended the meeting on time|Number of attendees that left a Teams meeting early or within one minute after the scheduled end time|Count
||Number of attendees who didn’t end the meeting on time|Number of attendees who left a Teams meeting after one minute past the scheduled end time.|Count |
||Number of attendees who joined the meeting on time|Number of attendees who joined a Teams meeting early or within five minutes after the scheduled start time.|Count|
||Number of attendees who didn’t join the meeting on time|Number of attendees who joined a Teams meeting after five minutes past the scheduled start time.|Count|
| <a name="working-hours-collaboration-define"></a> **Working-hours collaboration** | <a name="working-hours-channel-message-hours-define"></a> Working-hours channel message hours | Number of hours a person spent posting, replying to, or reading Teams channels messages during working hours. | Hour |
| | <a name="working-hours-collaboration-hours-define"></a> Working-hours collaboration hours | Number of hours a person spent in meetings, emails, Teams chats, Teams calls, and Teams channels with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting), during working hours. | Hour |
| | <a name="working-hours-email-hours-define"></a> Working-hours email hours | Number of hours a person spent sending and receiving emails during working hours | Hour |
| | <a name="working-hours-call-hours-define"></a> Working-hours call hours | Number of hours a person spent in scheduled and unscheduled Teams calls, during working hours. | Hour |
| | <a name="working-hours-chat-hours-define"></a> Working-hours chat hours | Number of hours a person spent in Teams chats during working hours. | Hour |
| | <a name="working-hours-meeting-hours-define"></a> Working-hours meeting hours | Number of hours a person spent in meetings with at least one other person, during working hours. | Hour |
| | <a name="working-hours-scheduled-call-hours-define"></a> Working-hours scheduled call hours | Number of hours a person spent in scheduled Teams calls, during working hours. | Hour |
| | <a name="working-hours-unscheduled-call-hours-define"></a> Working-hours unscheduled call hours | Number of hours a person spent in unscheduled Teams calls, during working hours. | Hour |



> [!NOTE]
> In Microsoft Teams, teamwork and communication happen in channels. Viva Insights includes several metrics which measure aspects of team communication over channels in Teams. When these metrics first become available in the Advanced insights app, they will reflect a baseline of only 14 days of historical data; this historical data will increase as time progresses. This differs from other metrics, which usually have 13 months of historical baseline data.


## Exported metrics

These metrics aren't selectable within the **Metrics** pane when you build queries, but they're included in query output.

Applies to|Name| Description|
|---|-------|------------|
|Person queries |IsActive | Boolean value of "true" or "false" for each employee. Active employees send at least one email or Teams chat during the unit of time—day, week, or month<sup>1</sup>—defined by the query’s **Group by** setting. 

<sup>1. You might notice differences when comparing metrics summarized by day with metrics summarized by week; a person can be active in a week, but not necessarily active seven days of the week.</sup>

