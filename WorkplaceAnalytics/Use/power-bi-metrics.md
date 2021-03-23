---

title: Power BI Connector metrics 
description: Describes the metrics for Workplace Analytics that you can import into Power BI through the Power BI Connector 
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
ms.prod: wpa
manager: scott.ruble
audience: Admin

---

# Power BI Connector metrics

The following person metrics are imported from Workplace Analytics into Power BI through the Power BI Connector. These base metrics are imported when you only enter a Partition Identifier and not any Query Names or Query Identifiers. For details, see [Connect through the Power BI Connector](View-download-and-export-query-results.md#connect-through-the-power-bi-connector). Metrics that are only available through the Power BI Connector and not in Workplace Analytics show as **Not applicable** in the Workplace Analytics metric column.

|Power BI Connector metric |Workplace Analytics metric |Data type |Definition |
|--------------|--------------|-------|---------------|
|AfterHoursCollaboration |After hours collaboration |Hour |Number of hours the person spent in meetings and on email outside of working hours. |
|AfterHoursCollaborationCalls |After hours in calls |Hour |Number of hours a person spent in scheduled and unscheduled calls through Teams, outside of working hours. For calls that started during working hours, this number only includes the part of the call that occurred outside of that person’s work schedule (as set in Outlook). |
|AfterHoursCollaborationEmails |After hours email hours |Hour |Number of hours the person spent sending email outside of working hours. |
|AfterHoursCollaborationInstantMessages |After hours instant messages |Hour |Number of hours a person spent in instant messages through Teams, outside of working hours. |
|AfterHoursCollaborationMeetings |After hours meeting hours |Hour |Number of hours the person spent in meetings outside of working hours. |
|AfterHoursMailsSentCount |Not applicable |Count |Number of emails the person sent outside of working hours.
|CallsCount |Total calls |Count |Total number of calls a person joined through Teams, including scheduled and unscheduled calls during and outside of working hours (as set in Outlook). |
|CollaborationHours |Collaboration hours |Hour |Number of hours the person spent in meetings and on email with at least one other person. Collaboration hours include both internal and external hours. |
|CollaborationHoursAdhocCalls |Not applicable |Hour |The number of hours the person spent in unscheduled calls through Teams with at least one other person, during and outside of working hours. |
|CollaborationHours |Collaboration hours |Hour |Number of hours the person spent in meetings and on email with at least one other person. Collaboration hours include both internal and external hours. |
|CollaborationHoursAdhocCalls |Not applicable |Hour |The number of hours the person spent in unscheduled calls through Teams with at least one other person, during and outside of working hours. |
|CollaborationHoursCalls |Call hours |Hours |The number of hours the person spent in scheduled and unscheduled calls through Teams with at least one other person, during and outside of working hours. |
|CollaborationHoursEmails |Email hours |Hour |Number of hours the person spent sending and receiving emails. |
|CollaborationHoursExternal |Collaboration hours external |Hour |Number of hours the person spent in meetings and on email with at least one person outside the company (as defined by the participant’s email domains). |
|CollaborationHoursInstantMessages |Instant message hours |Hours |Number of hours a person spent in instant messages (IMs) through Teams with at least one other person, during and outside of working hours.
|CollaborationHoursInternalOutsideOrg |Not applicable |Hour |Number of hours the person spent in meetings and on email with internal employees only (as defined by the participant’s email domains) outside their Organization. Calculation uses Organization attribute. |
|CollaborationHoursMeetings |Meeting hours |Hour |Number of hours the person spent in meetings with at least one other person. |
|CollaborationHoursScheduledCalls |Not applicable |Hour |The number of hours the person spent in scheduled calls through Teams with at least one other person, during and outside of working hours. |
|<a name="conflicting-define"></a>ConflictingMeetingHours |Conflicting meeting hours |Hour |Number of meeting hours where the person had overlapping meetings in their calendar. The count includes the entire duration of all overlapping meetings, not just the amount of time that overlaps. (This number includes all non-declined meeting times, which includes accepted, tentative, or no responses to meeting invitations.) |
|Date |Required HR attribute |Date |Same as MetricDateMonth. |
|DecisionMakingMeetingCount |Not applicable |Count |Number of meetings that the person attended where attendee count less than nine and the duration is less than or equal to one hour. |
|<a name="direct-manager-define"></a> DirectManagerMeetingHours |Meeting hours with manager |Hour |Number of meeting hours where attendees included at least the person and their manager. |
|External |Not applicable |Hour |Number of hours the person spent in meetings and on email with at least one person outside the company (as defined by the participant’s email domain). |
|ExternalCollaborationCost |Calculated by Workplace Analytics |USD |Cost of external collaboration which is calculated as CollaborationHoursExternal multiplied by average Hourly Rate. |
|ExternalNetworkBreadth |Networking outside company |Count |The number of distinct external domains outside the company a person has had at least two meaningful interactions in the last four weeks. |
|ExternalNetworkSize |External network size |Count |The number of people external to the company with whom the person had at least two meaningful interactions in the last four weeks. |
|FragmentedTime |Calculated by Workplace Analytics |Hour |A person's time after you subtract their meeting hours and their focus hours. |
|HourlyRate |Required HR attribute or calculated by Workplace Analytics |String |The employee’s salary represented as an hourly rate in US dollars. If not available in Workplace Analytics, calculations use $75 USD as the average hourly rate. |
|InferredTeamSize |Calculated by Workplace Analytics |String |Team size of the person not including themselves. If Individual Contributors equal zero, calculations use the count of both direct and indirect reports for the team size. |
|InstantMessagesCountSent |Instant messages sent |Count |Total number of instant messages (IMs) sent by a person through Teams, during and outside of working hours. |
|InternalNetworkBreadth |Networking outside organization |Count |The number of distinct organizational units within the company that the person had at least two meaningful interactions in the last four weeks. Calculation uses Organization attribute. |
|InternalNetworkSize |Internal network size |Count |The number of people within the company with whom the person had at least two meaningful interactions in the last four weeks. |
|InternalOnly |Not applicable |Hour |Number of hours the person spent in meetings and on email with internal employees only (as defined by the participant’s email domains). |
|IsActive |IsActive |Logic |True if the employee sent at least one email or one instant message during the specified time period. |
|LargeNotLongMeetingCount |Not applicable |Count |Number of meetings that the person attended with greater than or equal to nine attendees and the duration is less than or equal to one hour. |
|LevelDesignation |Required HR attribute  |String |The employee’s level is specific to your organization and can represent an employee’s experience or management level, or seniority within the organization. This data is needed to correctly calculate metrics for redundancy and insularity. |
|LongAndLargeMeetingCount |Not applicable |Count |Number of meetings that the person attended with greater than or equal to nine attendees and a duration of greater than one hour. |
|LongNotLargeMeetingCount |Not applicable |Count |Number of meetings that the person attended with less than nine attendees and a duration of greater than one hour. |
|LongOrLargeMeetingHours |Not applicable |Hour |Number of hours the person spent in meetings with more than nine attendees and a duration of greater than one hour.  |
|LowQualityMeetingHours |Low-quality meeting hours |Hour |Number of meeting hours in which an attendee multitasked, attended a conflicting meeting, or attended a meeting that exhibits redundancy (organizational). |
|LowQualityMeetingsCost |Calculated by Workplace Analytics |USD |Cost of low-quality meetings that’s calculated as LowQualityMeetingHours multiplied by Hourly Rate. |
|MailHoursLoadOrganizedAfterHours |Not applicable |Hour |Number of email hours the person created for internal recipients by sending emails outside of working hours. |
|MailsSentCount |Emails sent |Count |Number of emails the person sent. |
|ManagerId |Required HR attribute  |String |De-identified ID number for the manager of the person represented in the metric. |
|MeetingHours30To60Min |Not applicable |Hour |Number of hours the person spent in meetings with at least one other person and a duration of between 30 to 60 minutes. |
|MeetingHoursLessThan30Min |Not applicable |Hour |Number of hours the person spent in meetings less with a duration of 30 minutes with at least one other person. |
|MeetingHoursLessThan8Attendees |Not applicable |Hour |Number of hours the person spent in meetings with less than eight attendees. |
|MeetingHoursLessThanOneHour |Not applicable |Hour |Number of hours the person spent in meetings with a duration of less than or equal to one hour with at least one other person. |
|MeetingHoursOver4Hours |Not applicable |Hour |Number of hours the person spent in meetings with a duration equal to or more than four hours with at least one other person. |
|MeetingHoursOverOneHour |Not applicable |Hour |Number of hours the person spent in meetings with a duration of more than one hour with at least one other person. |
|Meetings19PlusAttendees |Not applicable |Hour |Number of hours the person spent in meetings with 19 or more attendees. |
|Meetings2Attendees |Not applicable |Hour |Number of hours the person spent in meetings with one other person.
|Meetings3To4Attendees |Not applicable |Hour |Number of hours the person spent in meetings with between three and four attendees. |
|Meetings5To8Attendees |Not applicable |Hour |Number of hours the person spent in meetings with between five and eight attendees. |
|Meetings9To18Attendees |Not applicable |Hour |Number of hours the person spent in meetings with between 9 and 18 attendees. |
|MeetingsCount |Meetings |Count |Number of meetings the person attended. |
|MeetingsHours1To2Hours |Not applicable |Hour |Number of hours the person spent in meetings that were between one to two hours in length with at least one other person. |
|MeetingsHours2To4Hours |Not applicable |Hour |Number of hours the person spent in meetings that were two to three hours in length with at least one other person. |
|MeetingsHoursLoadOrganizedAfterHours |Not applicable |Hour |Number of meeting hours the person created for internal attendees by organizing meetings outside of working hours. |
|MeetingsLoadOrganizedAfterHours |Not applicable |Count |Number of internal meetings organized by the person outside of working hours. |
|MetricDate |Calculated by Workplace Analytics |Date |The week start date for the first day of the week that data is being aggregated for. For example, Sunday. |
|MetricDateMonth |Calculated by Workplace Analytics |Date |The metric date for the first day of the month that data is being aggregated for. For example, March 1st. |
|MultitaskingMeetingHours |Multitasking meeting hours |Hour |Number of meeting hours where the person sent two or more emails during a meeting, or two or more emails during a meeting that was less than one hour. |
|NonConflictingMeetingHours |Not applicable |Hour |Total number of meeting hours minus the number of [ConflictingMeetingHours](#conflicting-define). |
|NonDirectManagerMeetingHours |Not applicable |Hour |Total number of meeting hours minus the number of [DirectManagerMeetingHours](#direct-manager-define) metric. |
|NonLowQualityMeetingHours |Not applicable |Hour |Total number of meeting hours minus the number of  LowQualityMeetingHours. |
|NonMultitaskingMeetingHours |Not applicable |Hour |Total number of meeting hours minus the number of MultitaskingMeetingHours. |
|NonOneOnOneMeetingHours |Not applicable |Hour |Total number of meeting hours minus the number of OneOnOneMeetingHours metric. |
|NonRecurringMeetingCount |Not applicable |Count |The number of meetings the person attended that were not recurring meetings. |
|NonRecurringMeetingHours |Not applicable |Hour |Number of hours the person spent in non-recurring meetings with at least one other person. |
|NonRedundantMeetingHours |Not applicable |Hour |Total number of meeting hours minus the number of RedundantMeetingHours metric. |
|NonSkipLevelMeetingHours |Not applicable |Hour |Total number of meeting hours minus the number of SkipLevelMeetingHours metric. |
|OneOnOneInstantMessagesCountSent |Not applicable |Count |Total number of instant messages (IMs) sent by a person to exactly one recipient through Teams, during and outside of working hours. |
|OneOnOneMailsCountSent |Not applicable |Count |Number of emails the person sent to exactly one recipient.
|OneOnOneMeetingHours |Meeting hours with manager 1:1 |Hour |Number of meeting hours involving only the person and their manager. |
|OpenOneHourBlocks |Open one-hour block |Count |Number of one-hour blocks in the person’s calendar without meetings during the workday. |
|OpenTwoHourBlocks |Open tow-hour blocks |Count |Number of two-hour blocks in the person’s calendar without meetings during the workday. |
|Organization |Required HR attribute  |String |The internal organization that the employee belongs to. An employee’s organization will be specific to your individual needs and could be identified by the leader of the organization, or by another naming convention. |
|OrganizerGeneratedMailLoadHours |Generated workload email hours |Hour |Number of email hours the person created for internal recipients by sending emails. |
|OrganizerGeneratedMeetingLoadCount |Generated workload meetings organized |Count |Number of internal meetings organized by the person. |
|OrganizerGeneratedMeetingLoadHours |Generated workload meeting hours |Hour |Number of meeting hours the person created for internal attendees by organizing meetings. |
|Person_DirectReports |Required HR attribute  |String |Number of direct reports, which is a non-zero value for managers. |
|Person_IsManager |Required HR attribute |String |True indicates that the person is a manager. |
|Person_RoleType |Required HR attribute  |String |Indicates one of three possible values, which are IC, Manager, or Manager+. |
|PersonId |PersonId |String |De-identified ID number for the person represented in the metric. |
|PopulationType |Required HR attribute |String |Currently all the person metric data that’s imported is for measured employees only. |
|RecurringMeetingHours |Not applicable |Hour |Number of hours the person spent in recurring meetings with at least one other person. |
|RedundantMeetingHours |Redundant meeting hours (organizational) |Hour |Number of meeting hours a person spent with attendees from three or more distinct levels within that person’s organization. Used in calculating Low quality meeting hours. |
|SkipLevelMeetingHours |Meetings hours with skip level |Hour |Number of meeting hours that the person attends where their manager's manager also attends the meeting. |
|TimeZone |Required HR attribute  |String |Time zone in which the employee performs work. |
|TotalFocusHours |Total focus hours |Hour |Total number of hours with two or more one-hour blocks of time where the person had no meetings. |
|Utilization |Workweek span |Hour |The time between the person's first sent email, meeting attended, or Teams call or chat, and the last email, meeting, call, or chat for each day of the work week. The total number of hours are based on the person’s work week that is set in Outlook, which the user can change at any time. If a work week is not defined in Outlook (or if Workplace Analytics is unable to access a user's Outlook settings), the totals are based on the default of Monday through Friday, with a minimum of four hours and a maximum of 16 hours each day. If reported for the week, the metric is a sum of the daily values for the week. |
|WorkingHoursCollaboration |Working hours collaboration hours |Hour |Number of hours the person spent in meetings and sending emails during working hours. |
|WorkingHoursCollaborationCalls |Working hours in calls |Hour |Total number of hours a person spent time in scheduled and unscheduled calls with Teams, during working hours. |
|WorkingHoursCollaborationEmails |Working hours email hours |Hour |Number of hours the person spent sending email during working hours. |
|WorkingHoursCollaborationInstantMessages |Working hours instant messages |Hour |Total number of hours a person spent time in instant messages through Teams, during working hours. |
|WorkingHoursCollaborationMeetings |Meeting hours during working hours |Hour |Number of hours the person spent in meetings, during working hours, with at least one other person. |
