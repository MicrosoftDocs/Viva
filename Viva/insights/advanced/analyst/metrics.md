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

The following metrics are available when creating analysis in the Advanced insights app with Microsoft Viva Insights, such as for Person queries and Power BI templates. The descriptions are listed alphabetically within each category.

|Category | Name | Description           | Data type |
|---------|------|-----------------------|-----------|
|**After-hours collaboration** | After hours collaboration hours | Number of hours the person spent outside of working hours in meetings, emails, chats, and calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| | After hours email hours | Number of hours the person spent in meetings, emails, IMs, and calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting), outside of working hours.| Hour |
| | After hours in calls | Number of hours a person spent in scheduled and unscheduled calls through Teams, outside of working hours. For calls that started during working hours, this number only includes the part of the call that occurred outside of that person’s work schedule. | Hour |
| | After hours in unscheduled calls | Number of hours a person spent in unscheduled calls through Teams, outside of working hours. For calls that started during working hours, this number only includes the part of the call that occurred outside of that person’s work schedule. | Hour |
| | After hours instant messages | Number of hours a person spent in instant messages through Teams, outside of working hours. | Hour |
| | After hours meeting hours | Number of hours the person spent in meetings outside of working hours. | Hour |
| **Collaboration activity** | Collaboration hours | Number of hours the person spent in meetings, emails, IMs, and calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Hour |
| | Email hours | Number of hours the person spent sending and receiving emails. | Hour |
| | Meeting hours | Number of hours the person spent in meetings with at least one other person during and outside of working hours. | Hour |
| | Instant message hours | Number of hours that a person spent in instant messages (IMs) through Teams with at least one other person, during and outside of working hours. | Hour |
| | Call hours | Number of hours that a person spent in scheduled and unscheduled calls through Teams with at least one other person, during and outside of working hours. | Hour |
| | Unscheduled call hours | Number of hours that a person spent in unscheduled calls through Teams with at least one other person, during and outside of working hours. | Hour |
| | Multitasking hours | Number of hours the person spent sending emails or instant messages during a meeting or a Teams call. | Hour |
| | Emails sent | Number of emails the person sent. | Count |
| | Meetings | Number of meetings the person attended. | Count |
| | Instant messages sent | Total number of instant messages (IMs) sent by a person through Teams, during and outside of working hours. | Count |
| | Total calls | Total number of calls a person joined through Teams, including scheduled and unscheduled calls during and outside of working hours. | Count |
| | Meeting and call hours | Number of hours the person spent in meetings and calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities. | Hour |
| **Collaboration by day of the week** | Emails sent during weekend | Number of emails the person sent on Saturdays or Sundays. | Hour |
| | IMs sent during weekend | Number of IMs the person sent on Saturdays or Sundays. | Hour |
| | Meetings during weekend | Number of meetings the person attended during Saturdays or Sundays. | Count |
| | Unscheduled calls during weekend | Total number of unscheduled calls a person joined through Teams, during and Saturdays or Sundays. | Count |
| | Collaboration hours [day] <br>(For example, Collaboration hours Monday) | Number of hours the person spent in meetings, emails, IMs, and calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting) during the specified <day> (Monday through Sunday). | Hour |
| **Collaboration by time of day** |  Urgent email hours | Number of hours the person spent in emails where some level of urgency is involved. Urgency is defined by a set of urgent keywords in email subject lines.
| | Urgent meeting hours | Number of hours the person spent in meetings where some level of urgency is involved. Urgency is defined by a set of urgent keywords in meeting subject lines.
a. Emails sent 00 01, Emails sent 01 02 etc till Emails sent 23 24 (24 metrics depicting each hour of the day) | Number of emails the person sent during the defined hour block.
IMs sent 00 01, IMs sent 01 02 etc till IMs sent 23 24 (24 metrics depicting each hour of the day) | Number of IMs the person sent during the defined hour block.
Meetings 00 01, Meetings 01 02 etc till Meetings 23 24 (24 metrics depicting each hour of the day) | Number of meetings the person attended during the defined hour block.
Unscheduled calls [XX] <br>(for example, Unscheduled calls 00)  | Number of unscheduled calls that a person joined through Teams with at least one other person during the defined hour block. The metric name includes the hour block of when it occurred, from 00 to 24 (depicting 24 hours in a day), where 00 is the hour between 12AM and 1AM, which would be "Unscheduled calls 00." | Hour |

| **Collaboration in small groups** | | Number of  | Hour |

| **Collaboration involving manager** | | Number of  | Hour |

| **Collaboration network** | Name |Definition | Type |

| **External collaboration** | Name |Definition | Type |

| **Focus** | Available to focus | Time remaining during working hours after excluding meetings and scheduled calls for focused work. This helps understand how meetings and scheduled calls can impact what time is available for self-directed work. | Hour |
|  | Uninterrupted time | Sum of time where a person did not attend meetings and did not send or read emails, chats, calls, or Teams channel posts for one or more hours. This can help organizations understand if employees have long blocks of uninterrupted time for deep-thinking to solve new problems creatively and fuel innovation. | Hour |
|  |Interrupted time | Time available to focus that was interrupted by emails, chats, unschedule calls, and Teams channel posts. This excludes the one-hour or more blocks of Uninterrupted time for deep work. This helps organizations understand if employees are choosing to use the blocks of time between meetings or scheduled calls for emails, calls, chats, and Teams channel collaboration. | Hour |
| **Hybrid** | Name |Definition | Type |

| **Meeting types** | Conflicting meeting hours|Number of meeting hours where the person had overlapping meetings in their calendar. The count includes just the amount of time that overlaps. (This number includes all non-declined meeting times, which includes accepted, tentative, or no responses to meeting invitations.) | Hour |

| **Working hours collaboration** | Name |Definition | Type |