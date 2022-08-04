---
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

The following metrics are available when creating analysis in the Advanced insights app with Microsoft Viva Insights, such as for custom Person queries and Power BI templates. The descriptions are listed alphabetically within each category.

| Category | Name | Description | Data type |
|---|---|---|---|
| **After-hours collaboration** | After-hours collaboration hours | Number of hours a person spent in meetings, emails, Teams chats, and Teams calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting), outside of working hours. | Hour |
| | After-hours email hours | Number of hours a person spent sending and receiving emails outside of working hours. | Hour |
| | After-hours call hours | Number of hours a person spent in scheduled and unscheduled Teams calls, outside of working hours. For calls that started during working hours, this number only includes the part of the call that occurred outside of that person’s work schedule. | Hour |
| | After-hours unscheduled call hours | Number of hours a person spent in unscheduled Teams calls, outside of working hours. For calls that started during working hours, this number only includes the part of the call that occurred outside of that person’s work schedule. | Hour |
| | After-hours scheduled call hours | Number of hours a person spent in scheduled Teams calls, outside of working hours. For calls that started during working hours, this number only includes the part of the call that occurred outside of that person’s work schedule. | Hour |
| | After-hours chat hours | Number of hours a person spent in Teams chats outside of working hours. | Hour |
| | After-hours meeting hours | Number of hours a person spent in meetings with at least one other person, outside of working hours. | Hour |
| **Collaboration activity** | Collaboration hours | Number of hours a person spent in meetings, emails, Teams chats, and Teams calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| | Email hours | Number of hours a person spent sending and receiving emails. | Hour |
| | Meeting hours | Number of hours a person spent in meetings with at least one other person during and outside of working hours. | Hour |
| | Chat hours | Number of hours a person spent in Teams chats with at least one other person, during and outside of working hours. | Hour |
| | Call hours | Number of hours a person spent in scheduled and unscheduled Teams calls with at least one other person, during and outside of working hours. | Hour |
| | Unscheduled call hours | Number of hours a person spent in unscheduled Teams calls with at least one other person, during and outside of working hours. | Hour |
| | Scheduled call hours | Number of hours a person spent in scheduled Teams calls with at least one other person, during and outside of working hours. | Hour |
| | Multitasking hours | Number of hours a person spent sending or reading emails or chats during a meeting or a Teams call. | Hour |
| | Emails sent | Number of emails a person sent. | Count |
| | Meetings | Number of meetings a person attended. | Count |
| | Chats sent | Number of Teams chats a person sent. | Count |
| | Calls | Number of Teams calls a person joined, including scheduled and unscheduled calls. | Count |
| | Meeting and call hours | Number of hours a person spent in meetings and Teams calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities. | Hour |
| **Collaboration by day of the week** | Weekend emails sent | Number of emails a person sent on Saturdays or Sundays. | Hour |
| | Weekend chats sent | Number of Teams chats a person sent on Saturdays or Sundays. | Hour |
| | Weekend meetings | Number of meetings a person attended during Saturdays or Sundays. | Count |
| | Unscheduled weekend calls | Number of unscheduled Teams calls a person joined, on Saturdays or Sundays. | Count |
| | Collaboration hours on *x* (day) | Number of hours a person spent in meetings, emails, Teams chats, and Teams calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting) during the specified day (Monday through Sunday). | Hour |
| **Collaboration by time of day** | Urgent email hours | Number of hours a person spent in emails where some level of urgency is involved. Urgency is defined by a set of urgent keywords in email subject lines. | Hour |
| | Urgent meeting hours | Number of hours a person spent in meetings where some level of urgency is involved. Urgency is defined by a set of urgent keywords in meeting subject lines. | Hour |
| | Emails sent *x* (hour block) | Number of emails a person sent during a defined hour block. The metric name includes when the defined hour block begins and ends, which is written as two numbers from 00 to 24 (depicting 24 hours in a day). For emails sent between 8AM and 9AM, for example, the metric name would be "Emails sent 08 09." | Count |
| | Chats sent *x* (hour block) | Number of Teams chats a person sent during a defined hour block. The metric name includes when the hour block begins and ends, which is written as two numbers from 00 to 24 (depicting 24 hours in a day). For chats sent between 8AM and 9AM, for example, the metric name would be "Chats" sent 08 09." | Count |
| | Meetings *x* (hour block) | Number of meetings a person attended during a defined hour block. The metric name includes when the hour block begins and ends, which is written as two numbers from 00 to 24 (depicting 24 hours in a day). For meetings between 8AM and 9AM, for example, the metric name would be "Meetings 08 09." | Count |
| | Unscheduled calls *x* (hour block) | Number of unscheduled Teams calls a person joined with at least one other person during a defined hour block. The metric name includes when the hour block begins and ends, which is written as two numbers from 00 to 24 (depicting 24 hours in a day). For unscheduled calls between 8AM and 9AM, for example, the metric name would be "Unscheduled calls 08 09." | Count |
| **Collaboration in small groups** | Small-group meeting, call, and chat hours | Number of hours a person spent in meetings, Teams chats, and unscheduled Teams calls with between two to eight people, all internal, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| | Small-group emails sent, excluding manager | Number of emails a person sent to an internal group of eight or less people, including the sender and excluding the sender's manager from the recipient group. | Count |
| | Small-group chats sent, excluding manager | Number of Teams chats a person sent to an internal group of eight or less people, including the sender and excluding the sender’s manager from the recipient group. | Count |
| | Internal meeting hours without manager 1:1 | Number of hours a person spent in meetings with only one other person who is not their manager. | Hour |
| | Internal meeting hours with 3 to 8 attendees | Number of hours a person spent in meetings with at least three and up to eight internal collaborators only and no external collaborators. | Hour |
| **Collaboration involving manager** | Unscheduled call hours with manager 1:1 | Number of hours a person spent in unscheduled Teams calls involving only the person and their manager. | Hour |
| | Unscheduled call hours with manager | Number of hours a person spent in unscheduled Teams calls where attendees included the person, their manager, and one or more other people (not a one-on-one meeting). | Hour |
| | Collaboration hours with direct reports | Number of hours a person spent in meetings, emails, Teams chats, and Teams calls where all participants report directly to the person, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| | Small-group emails sent, including manager | Number of emails a person sent to an internal group of eight or less people, including the sender and the sender's manager in the recipient group. | Count |
| | Small-group chats sent, including manager | Number of Teams chats a person sent to an internal group of eight or less people, including the sender and the sender's manager in the recipient group. | Count |
| | Manager coaching hours 1:1 | Number of hours a manager spent in one-on-one meetings with all of the manager's direct reports. | Hour |
| | Meeting hours with manager | Number of meeting hours where attendees included the person, their manager, and one or more other people (not a one-on-one meeting). | Hour |
| | Meeting hours with manager 1:1 | Number of meeting hours involving only the person and their manager. | Hour |
| | Meeting hours with skip level | Number of meeting hours a person attended where their manager's manager also attended the meeting. | Hour |
| | Meetings with manager | Number of meetings a person attended where attendees included a person, their manager, and one or more other people (not a one-on-one meeting). | Count |
| | Meetings with manager 1:1 | Number of meetings a person attended involving only the person and their manager. | Count |
| | Meetings with skip level | Number of meetings a person attended where their manager's manager also attended the meeting. | Count |
| **Collaboration network** | Internal network size | Number of people within the company with whom a person had at least two meaningful interactions in the month. | Count |
| **External collaboration** | External collaboration hours | Number of hours a person spent in meetings, emails, Teams chats, and Teams calls with at least one other person outside the company, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| | External unscheduled call hours | Number of hours a person spent in unscheduled Teams calls with at least one other person outside the company. | Hour |
| | External email hours | Number of hours a person spent in emails with at least one other person outside the company. | Hour |
| | External chat hours | Number of hours a person spent in Teams chats with at least one other person outside the company. | Hour |
| | External meeting hours | Number of hours a person spent in meetings with at least one other person outside the company. | Hour |
| **Focus**| Available-to-focus hours | Hours remaining during working hours after excluding meetings and scheduled Teams calls for focused work. This metric helps organizations understand how meetings and scheduled Teams calls can impact what time is available for self-directed work. | Hour |
| | Uninterrupted hours | Sum of blocks one hour or longer where a person didn’t attend a meeting, read or send emails, read or send Teams chats, or initiate or receive Teams calls. In other words, Uninterrupted hours is the sum of blocks of time one hour or longer for deep thinking with no communication. This metric helps organizations understand whether employees have long blocks of uninterrupted time for deep thinking to solve new problems creatively and to fuel innovation. | Hour |
| | Interrupted hours | Available-to-focus hours interrupted by emails, Teams chats, or unscheduled Teams calls. Interrupted hours excludes one-hour or longer blocks of Uninterrupted hours for deep work. This metric helps organizations understand whether employees are choosing to use the blocks of time between meetings or scheduled Teams calls for emails, unscheduled calls, or Teams chats. | Hour |
| **Meeting types** | Conflicting meeting hours | Number of meeting hours where a person had overlapping meetings in their calendar. The count includes just the amount of time that overlaps. | Hour |
| | Small and short meeting hours | Meeting hours with a duration of one hour or less that have at least two and up to eight invitees, including the organizer. | Hour |
| | Small and short recurring meeting hours | Recurring meeting hours with a duration of one hour or less that have at least two and up to eight invitees, including the organizer. | Hour |
| | Large and long meeting hours | Meeting hours with a duration of more than one hour and nine or more invitees, including the organizer. | Hour |
| | Large and long recurring meeting hours | Recurring meeting hours with a duration of more than one hour and nine or more invitees, including the organizer. | Hour |
| | Large and short meeting hours | Meeting hours with a duration of one hour or less and nine or more invitees, including the organizer. | Hour |
| | Large and short recurring meeting hours | Recurring meeting hours with a duration of one hour or less and nine or more invitees, including the organizer. | Hour |
| | Small and long meeting hours | Meeting hours with a duration of more than one hour that have at least two and up to eight invitees, including the organizer. | Hour |
| | Small and long recurring meeting hours | Recurring meeting hours with a duration of more than one hour that have at least two and up to eight invitees, including the organizer. | Hour |
| | Recurring meeting hours | Meeting hours for meetings that are set to recur. | Hour |
| **Working-hours collaboration** | Working-hours collaboration hours | Number of hours a person spent in meetings, emails, Teams chats, and Teams calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting), during working hours. | Hour |
| | Working-hours email hours | Number of hours a person spent sending and receiving emails during working hours | Hour |
| | Working-hours call hours | Number of hours a person spent in scheduled and unscheduled Teams calls, during working hours. | Hour |
| | Working-hours chat hours | Number of hours a person spent in Teams chats during working hours. | Hour |
| | Working-hours meeting hours | Number of hours a person spent in meetings with at least one other person, during working hours. | Hour |
