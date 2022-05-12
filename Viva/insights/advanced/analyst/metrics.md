---
ROBOTS: NOINDEX,FOLLOW
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

The following metrics are available when creating analysis in the Advanced insights app with Microsoft Viva Insights, such as for Person queries and Power BI templates. The descriptions are listed alphabetically within each category.

|Category | Name | Description           | Data type |
|---------|------|-----------------------|-----------|
|**After-hours collaboration** | After hours collaboration hours | Number of hours the person spent outside of working hours in meetings, emails, chats (instant messages or IMs), and calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| | After hours email hours | Number of hours the person spent in meetings, emails, IMs, and calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting), outside of working hours.| Hour |
| | After hours in calls | Number of hours a person spent in scheduled and unscheduled calls through Teams, outside of working hours. For calls that started during working hours, this number only includes the part of the call that occurred outside of that person’s work schedule. | Hour |
| | After hours in unscheduled calls | Number of hours a person spent in unscheduled calls through Teams, outside of working hours. For calls that started during working hours, this number only includes the part of the call that occurred outside of that person’s work schedule. | Hour |
| | After hours instant messages | Number of hours a person spent in chats (IMs) through Teams, outside of working hours. | Hour |
| | After hours meeting hours | Number of hours the person spent in meetings outside of working hours. | Hour |
| **Collaboration activity** | Collaboration hours | Number of hours the person spent in meetings, emails, IMs, and calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| | Email hours | Number of hours the person spent sending and receiving emails. | Hour |
| | Meeting hours | Number of hours the person spent in meetings with at least one other person during and outside of working hours. | Hour |
| | Instant message hours | Number of hours that a person spent in IMs through Teams with at least one other person, during and outside of working hours. | Hour |
| | Call hours | Number of hours that a person spent in scheduled and unscheduled calls through Teams with at least one other person, during and outside of working hours. | Hour |
| | Unscheduled call hours | Number of hours that a person spent in unscheduled calls through Teams with at least one other person, during and outside of working hours. | Hour |
| | Multitasking hours | Number of hours the person spent sending emails or IMs during a meeting or a Teams call. | Hour |
| | Emails sent | Number of emails the person sent. | Count |
| | Meetings | Number of meetings the person attended. | Count |
| | Instant messages sent | Total number of IMs (chats) sent by a person through Teams, during and outside of working hours. | Count |
| | Total calls | Total number of calls a person joined through Teams, including scheduled and unscheduled calls during and outside of working hours. | Count |
| | Meeting and call hours | Number of hours the person spent in meetings and calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities. | Hour |
| **Collaboration by day of the week** | Emails sent during weekend | Number of emails the person sent on Saturdays or Sundays. | Hour |
| | IMs sent during weekend | Number of IMs the person sent on Saturdays or Sundays. | Hour |
| | Meetings during weekend | Number of meetings the person attended during Saturdays or Sundays. | Count |
| | Unscheduled calls during weekend | Total number of unscheduled calls a person joined through Teams, during and Saturdays or Sundays. | Count |
| | Collaboration hours _x_ (day)  | Number of hours the person spent in meetings, emails, IMs, and calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting) during the specified _day_ (Monday through Sunday). | Hour |
| **Collaboration by time of day** |  Urgent email hours | Number of hours the person spent in emails where some level of urgency is involved. Urgency is defined by a set of urgent keywords in email subject lines.
| | Urgent meeting hours | Number of hours the person spent in meetings where some level of urgency is involved. Urgency is defined by a set of urgent keywords in meeting subject lines.
| | Emails sent _x_ (hour block) | Number of emails the person sent during the defined hour block. The metric name includes the hour block of when it occurred, from 00 to 24 (depicting 24 hours in a day), where 08 is the hour between 8AM and 9AM, which would be "Emails sent 08." | Count |
| | IMs sent  _x_ (hour block) | Number of IMs the person sent during the defined hour block. The metric name includes the hour block of when it occurred, from 00 to 24 (depicting 24 hours in a day), where 08 is the hour between 8AM and 9AM, which would be "IMs sent 08." | Count |
| | Meetings  _x_ (hour block) | Number of meetings the person attended during the defined hour block. The metric name includes the hour block of when it occurred, from 00 to 24 (depicting 24 hours in a day), where 08 is the hour between 8AM and 9AM, which would be "Meetings 08." | Count |
| | Unscheduled calls _x_ (hour block) | Number of unscheduled calls that a person joined through Teams with at least one other person during the defined hour block. The metric name includes the hour block of when it occurred, from 00 to 24 (depicting 24 hours in a day), where 08 is the hour between 8AM and 9AM, which would be "Unscheduled calls 08." | Count |
| **Collaboration in small groups** | Collaboration hours in small groups | Number of hours the person spent in meetings, IMs, and unscheduled calls with between two to eight people, all internal, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| | Emails sent to small group without manager | Number of emails the person sent to an internal group of eight or less people, including the sender and excluding the sender's manager from the recipient group. | Count |
| | IMs sent to small group without manager | Number of IMs the person sent to an internal group of eight or less people, including the sender and excluding the sender's manager from the recipient group. | Count |
| | Internal meeting hours without manager one on one | Number of hours the person spent in meetings with only one other person who is not their manager. | Hour |
| | Internal meeting hours 3 to 8 attendees | Number of hours the person spent in meetings with at least three up to eight internal collaborators only and no external collaborators. | Hour |
| **Collaboration involving manager** | Unscheduled call hours with manager one on one | Number of hours that a person spent in unscheduled calls through Teams involving only the person and their manager. | Hour |
| | Unscheduled call hours with manager | Number of hours that a person spent in unscheduled calls through Teams where attendees included at least the person and their manager. | Hour |
| | Collaboration hours with direct reports | Number of hours the person spent in meetings, emails, IMs, and calls where all participants report directly to the person, after deduplication of time due to overlapping activities (for example, calls during a meeting).| Hour |
| | Emails sent to small group with manager | Number of emails the person sent to an internal group of eight or less people, including the sender and the sender's manager in the recipient group. | Count |
| | IMs sent to small group with manager | Number of IMs the person sent to an internal group of eight or less people, including the sender and the sender's manager in the recipient group. | Count |
| | Manager coaching hours one on one | Total number of hours the manager spends in one-on-one meetings with all of the manager's direct reports. | Hour |
| | Meeting hours with manager | Number of meeting hours where attendees included the person, their manager, and one or more other people (not one-on-one meetings). | Hour |
| | Meeting hours with manager one on one | Number of meeting hours involving only the person and their manager. | Hour |
| | Meeting hours with skip level | Number of meeting hours the person attends where their manager's manager also attends the meeting. | Hour |
| | Meetings with manager | Number of meetings where attendees include at least the person and their manager. | Count |
| | Meetings with manager one on one | Number of meetings involving only the person and their manager. | Count |
| | Meetings with skip level | Number of meetings where the manager of the person's manager is an attendee. | Count |
| **Collaboration network** | Internal network size | The number of people within the company with whom the person had at least two meaningful interactions in the last four weeks. | Count  |
| **External collaboration** | External unscheduled call hours | Number of hours the person spent in unscheduled calls through Teams with at least one other person outside the company, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| | External collaboration hours | Number of hours the person spent in meetings, emails, IMs, and calls with at least one other person outside the company, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| | External email hours | Number of hours the person spent in emails with at least one other person outside the company, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| | External instant message hours | Number of hours the person spent in IMs with at least one other person outside the company, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| | External meeting hours | Number of hours the person spent in meetings with at least one other person outside the company, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| **Focus** | Available to focus | Time remaining during working hours after excluding meetings and scheduled calls for focused work. This helps understand how meetings and scheduled calls can impact what time is available for self-directed work. | Hour |
| | Uninterrupted time | Sum of time where a person did not attend meetings and did not send or read emails, chats, calls, or Teams channel posts for one or more hours. This can help organizations understand if employees have long blocks of uninterrupted time for deep-thinking to solve new problems creatively and fuel innovation. | Hour |
| |Interrupted time | Time available to focus that was interrupted by emails, chats, unscheduled calls, and Teams channel posts. This excludes the one-hour or more blocks of Uninterrupted time for deep work. This helps organizations understand if employees are choosing to use the blocks of time between meetings or scheduled calls for emails, calls, chats, and Teams channel collaboration. | Hour |
| **Hybrid** | Remote days | Number of days per week a person spent working remote (not on the company's corporate network). | Count |
| | Manager remote days | Number of days per week a person's direct manager spent working remote (not on the company's corporate network). | Count |
| | Onsite days | Number of days per week a person spent working onsite (on the company's corporate network). | Count |
| | Manager onsite days | Number of days per week a person's direct manager spent working onsite (on the company's corporate network). | Count |
| **Meeting types** | Conflicting meeting hours|Number of meeting hours where the person had overlapping meetings in their calendar. The count includes just the amount of time that overlaps. (This number includes all non-declined meeting times, which includes accepted, tentative, or no responses to meeting invitations.) | Hour |
| | Decision making meeting hours | Meeting hours with a duration of one hour or less and at least three up to eight participants. | Hour |
| | Decision making recurring meeting hours | Recurring meeting hours with a duration of one hour or less and at least three up to eight participants. | Hour |
| | Large and long meeting hours | Meeting hours with a duration of more than one hour and nine or more participants. | Hour |
| | Large and long recurring meeting hours | Recurring meeting hours with a duration of more than one hour and nine or more participants. | Hour |
| | Large meeting hours | Meeting hours with a duration of one hour or less and nine or more participants. | Hour |
| | Large recurring meeting hours | Recurring meeting hours with a duration of one hour or less and nine or more participants. | Hour |
| | Long meeting hours | Meeting hours with a duration of more than one hour and at least three up to eight participants. | Hour |
| | Long recurring meeting hours | Recurring meeting hours with a duration of more than one hour and at least three up to eight participants. | Hour |
| | One on one meeting hours | Meeting hours with a duration of one hour or less and two participants. | Hour |
| | One on one recurring meeting hours | Recurring meeting hours with a duration of one hour or less and two participants. | Hour |
| | Recurring meeting hours | Meeting hours for meetings that are set to recur. | Hour |
| **Working hours collaboration** | Working hours collaboration hours | Number of hours the person spent in meetings, emails, IMs, and calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting), during working hours.  | Hour |
| | Working hours email hours | Number of hours the person spent sending and receiving emails during working hours | Hour |
| | Working hours in calls | Total number of hours a person spent time in scheduled and unscheduled calls with Teams, during working hours. | Hour |
| | Working hours instant messages | Total number of hours a person spent time in instant messages through Teams, during working hours. | Hour |
| | Working hours meeting hours | Number of hours the person spent in meetings, during working hours, with at least one other person. | Hour |
