---
ROBOTS: NOINDEX,NOFOLLOW
title: Power BI Connector base metrics 
description: Describes the metrics for Viva Insights that you can import into Power BI through the Power BI Connector 
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Power BI Connector metrics

The following base metrics are imported from the advanced insights app for Viva Insights into Power BI through the Power BI Connector. These base metrics are imported when you only enter a Partition Identifier and not any Query Names or Query Identifiers. For details, see [Connect through the Power BI Connector](../use/view-download-and-export-query-results.md#connect-through-the-power-bi-connector). [Customized metrics](/viva/insights/tutorials/customize-a-metric?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) or calculated metrics that are not available in the advanced insights app as base metrics, show as **Not applicable** in that metric column.

|Power BI Connector metric |Viva Insights metric |Definition |Data type |
|---------|--------------|---------------------|-------|
|AfterHoursCollaboration |After hours collaboration |Number of hours the person spent in meetings and on email outside of working hours. |Hour |
|AfterHoursCollaborationCalls |After hours in calls |Number of hours a person spent in scheduled and unscheduled calls through Teams, outside of working hours. For calls that started during working hours, this number only includes the part of the call that occurred outside of that person’s work schedule (as set in Outlook). |Hour |
|AfterHoursCollaborationEmails |After hours email hours |Number of hours the person spent sending email outside of working hours. |Hour |
|AfterHoursCollaborationInstantMessages |After hours instant messages |Number of hours a person spent in instant messages through Teams, outside of working hours. |Hour |
|AfterHoursCollaborationMeetings |After hours meeting hours |Number of hours the person spent in meetings outside of working hours. |Hour |
|AfterHoursMailsSentCount |Not applicable |Number of emails the person sent outside of working hours.|Count |
|CallsCount |Total calls |Total number of calls a person joined through Teams, including scheduled and unscheduled calls during and outside of working hours (as set in Outlook). |Count |
|CollaborationHours |Collaboration hours |Number of hours the person spent in meetings and on email with at least one other person. Collaboration hours include both internal and external hours. |Hour |
|CollaborationHoursAdhocCalls |Not applicable |The number of hours the person spent in unscheduled calls through Teams with at least one other person, during and outside of working hours. |Hour |
|CollaborationHours |Collaboration hours |Number of hours the person spent in meetings and on email with at least one other person. Collaboration hours include both internal and external hours. |Hour |
|CollaborationHoursAdhocCalls |Not applicable |The number of hours the person spent in unscheduled calls through Teams with at least one other person, during and outside of working hours. |Hour |
|CollaborationHoursCalls |Call hours |The number of hours the person spent in scheduled and unscheduled calls through Teams with at least one other person, during and outside of working hours. |Hour |
|CollaborationHoursEmails |Email hours |Number of hours the person spent sending and receiving emails. |Hour |
|CollaborationHoursExternal |Collaboration hours external |Number of hours the person spent in meetings and on email with at least one person outside the company (as defined by the participant’s email domains). |Hour |
|CollaborationHoursInstantMessages |Instant message hours |Number of hours a person spent in instant messages (IMs) through Teams with at least one other person, during and outside of working hours. |Hour |
|CollaborationHoursInternalOutsideOrg |Not applicable |Number of hours the person spent in meetings and on email with internal employees only (as defined by the participant’s email domains) outside their Organization. Calculation uses Organization attribute. |Hour |
|CollaborationHoursMeetings |Meeting hours |Number of hours the person spent in meetings with at least one other person. |Hour |
|CollaborationHoursScheduledCalls |Not applicable |The number of hours the person spent in scheduled calls through Teams with at least one other person, during and outside of working hours. |Hour |
|<a name="conflicting-define"></a>ConflictingMeetingHours |Conflicting meeting hours |Number of meeting hours where the person had overlapping meetings in their calendar. The count includes the entire duration of all overlapping meetings, not just the amount of time that overlaps. (This number includes all non-declined meeting times, which includes accepted, tentative, or no responses to meeting invitations.) |Hour |
|Date |Required HR attribute |Same as [MetricDateMonth](#date-month-define). |Date |
|DecisionMakingMeetingCount |Not applicable |Number of meetings that the person attended where attendee count less than nine and the duration is less than or equal to one hour. |Count |
|<a name="direct-manager-define"></a>DirectManagerMeetingHours |Meeting hours with manager |Number of meeting hours where attendees included at least the person and their manager. |Hour |
|External |Not applicable |Number of hours the person spent in meetings and on email with at least one person outside the company (as defined by the participant’s email domain). |Hour |
|ExternalCollaborationCost |Calculated by Viva Insights |Cost of external collaboration which is calculated as CollaborationHoursExternal multiplied by average Hourly Rate. |USD |
|ExternalNetworkBreadth |Networking outside company |The number of distinct external domains outside the company a person has had at least two meaningful interactions in the last four weeks. |Count |
|ExternalNetworkSize |External network size |The number of people external to the company with whom the person had at least two meaningful interactions in the last four weeks. |Count |
|FragmentedTime |Calculated by Viva Insights |A person's time after you subtract their meeting hours and their focus hours. |Hour |
|HourlyRate |Required HR attribute or calculated by Viva Insights |The employee’s salary represented as an hourly rate in US dollars. If not available in Viva Insights, calculations use $75 USD as the average hourly rate. |String |
|InferredTeamSize |Calculated by Viva Insights |Team size of the person not including themselves. If Individual Contributors equal zero, calculations use the count of both direct and indirect reports for the team size. |String |
|InstantMessagesCountSent |Instant messages sent |Total number of instant messages (IMs) sent by a person through Teams, during and outside of working hours. |Count |
|InternalNetworkBreadth |Networking outside organization |The number of distinct organizational units within the company that the person had at least two meaningful interactions in the last four weeks. Calculation uses Organization attribute. |Count |
|InternalNetworkSize |Internal network size |The number of people within the company with whom the person had at least two meaningful interactions in the last four weeks. |Count |
|InternalOnly |Not applicable |Number of hours the person spent in meetings and on email with internal employees only (as defined by the participant’s email domains). |Hour |
|IsActive |IsActive |True if the employee sent at least one email or one instant message during the specified time period. |Logic |
|LargeNotLongMeetingCount |Not applicable |Number of meetings that the person attended with greater than or equal to nine attendees and the duration is less than or equal to one hour. |Count |
|LevelDesignation |Required optional HR attribute  |The employee’s level is specific to your organization and can represent an employee’s experience or management level, or seniority within the organization. This data is needed to correctly calculate metrics for redundancy and insularity. |String |
|LongAndLargeMeetingCount |Not applicable |Number of meetings that the person attended with greater than or equal to nine attendees and a duration of greater than one hour. |Count |
|LongNotLargeMeetingCount |Not applicable |Number of meetings that the person attended with less than nine attendees and a duration of greater than one hour. |Count |
|LongOrLargeMeetingHours |Not applicable |Number of hours the person spent in meetings with more than nine attendees and a duration of greater than one hour.  |Hour |
|<a name="low-quality-define"></a>LowQualityMeetingHours |Low-quality meeting hours |Number of meeting hours in which an attendee multitasked, attended a conflicting meeting, or attended a meeting that exhibits redundancy (organizational). |Hour |
|LowQualityMeetingsCost |Calculated by Viva Insights |Cost of low-quality meetings that’s calculated as LowQualityMeetingHours multiplied by Hourly Rate. |USD |
|MailHoursLoadOrganizedAfterHours |Not applicable |Number of email hours the person created for internal recipients by sending emails outside of working hours. |Hour |
|MailsSentCount |Emails sent |Number of emails the person sent. |Count |
|ManagerId |Required HR attribute |De-identified ID number for the manager of the person represented in the metric. You can only calculate aggregations, such as counts, of this field. Attempting to return a list of all ManagerIds will result in an error.|String |
|MeetingHours30To60Min |Not applicable |Number of hours the person spent in meetings with at least one other person and a duration of between 30 to 60 minutes. |Hour |
|MeetingHoursLessThan30Min |Not applicable |Number of hours the person spent in meetings less with a duration of 30 minutes with at least one other person. |Hour |
|MeetingHoursLessThan8Attendees |Not applicable |Number of hours the person spent in meetings with less than eight attendees. |Hour |
|MeetingHoursLessThanOneHour |Not applicable |Number of hours the person spent in meetings with a duration of less than or equal to one hour with at least one other person. |Hour |
|MeetingHoursOver4Hours |Not applicable |Number of hours the person spent in meetings with a duration equal to or more than four hours with at least one other person. |Hour |
|MeetingHoursOverOneHour |Not applicable |Number of hours the person spent in meetings with a duration of more than one hour with at least one other person. |Hour |
|Meetings19PlusAttendees |Not applicable |Number of hours the person spent in meetings with 19 or more attendees. |Hour |
|Meetings2Attendees |Not applicable |Number of hours the person spent in meetings with one other person. |Hour |
|Meetings3To4Attendees |Not applicable |Number of hours the person spent in meetings with between three and four attendees. |Hour |
|Meetings5To8Attendees |Not applicable |Number of hours the person spent in meetings with between five and eight attendees. |Hour |
|Meetings9To18Attendees |Not applicable |Number of hours the person spent in meetings with between 9 and 18 attendees. |Hour |
|MeetingsCount |Meetings |Number of meetings the person attended. |Count |
|MeetingsHours1To2Hours |Not applicable |Number of hours the person spent in meetings that were between one to two hours in length with at least one other person. |Hour |
|MeetingsHours2To4Hours |Not applicable |Number of hours the person spent in meetings that were two to three hours in length with at least one other person. |Hour |
|MeetingsHoursLoadOrganizedAfterHours |Not applicable |Number of meeting hours the person created for internal attendees by organizing meetings outside of working hours. |Hour |
|MeetingsLoadOrganizedAfterHours |Not applicable |Number of internal meetings organized by the person outside of working hours. |Count |
|MetricDate |Calculated by Viva Insights |The week start date for the first day of the week that data is being aggregated for. For example, Sunday. |Date |
|<a name="date-month-define"></a>MetricDateMonth |Calculated by Viva Insights |The metric date for the first day of the month that data is being aggregated for. For example, March 1st. |Date |
|<a name="multitasking-define"></a>MultitaskingMeetingHours |Multitasking meeting hours |Number of meeting hours where the person sent two or more emails during a meeting, or two or more emails during a meeting that was less than one hour. |Hour |
|NonConflictingMeetingHours |Not applicable |Total number of meeting hours minus the number of [ConflictingMeetingHours](#conflicting-define). |Hour |
|NonDirectManagerMeetingHours |Not applicable |Total number of meeting hours minus the number of [DirectManagerMeetingHours](#direct-manager-define) metric. |Hour |
|NonLowQualityMeetingHours |Not applicable |Total number of meeting hours minus the number of  [LowQualityMeetingHours](#low-quality-define). |Hour |
|NonMultitaskingMeetingHours |Not applicable |Total number of meeting hours minus the number of [MultitaskingMeetingHours](#multitasking-define). |Hour |
|NonOneOnOneMeetingHours |Not applicable |Total number of meeting hours minus the number of [OneOnOneMeetingHours](#one-on-one-define) metric. |Hour |
|NonRecurringMeetingCount |Not applicable |Total number of meetings the person attended minus the number of recurring meetings. |Count |
|NonRecurringMeetingHours |Not applicable |Number of hours the person spent in non-recurring meetings with at least one other person. |Hour |
|NonRedundantMeetingHours |Not applicable |Total number of meeting hours minus the number of [RedundantMeetingHours](#redundant-define) metric. |Hour |
|NonSkipLevelMeetingHours |Not applicable |Total number of meeting hours minus the number of [SkipLevelMeetingHours](#skip-level-define) metric. |Hour |
|OneOnOneInstantMessagesCountSent |Not applicable |Total number of instant messages (IMs) sent by a person to exactly one recipient through Teams, during and outside of working hours. |Count |
|OneOnOneMailsCountSent |Not applicable |Number of emails the person sent to exactly one recipient. |Count |
|<a name="one-on-one-define"></a>OneOnOneMeetingHours |Meeting hours with manager 1:1 |Number of meeting hours involving only the person and their manager. |Hour |
|OpenOneHourBlocks |Open one-hour block |Number of one-hour blocks in the person’s calendar without meetings during the workday. |Count |
|OpenTwoHourBlocks |Open tow-hour blocks |Number of two-hour blocks in the person’s calendar without meetings during the workday. |Count |
|Organization |Required HR attribute  |The internal organization that the employee belongs to. An employee’s organization will be specific to your individual needs and could be identified by the leader of the organization, or by another naming convention. |String |
|OrganizerGeneratedMailLoadHours |Generated workload email hours |Number of email hours the person created for internal recipients by sending emails. |Hour |
|OrganizerGeneratedMeetingLoadCount |Generated workload meetings organized |Number of internal meetings organized by the person. |Count |
|OrganizerGeneratedMeetingLoadHours |Generated workload meeting hours |Number of meeting hours the person created for internal attendees by organizing meetings. |Hour |
|Person_DirectReports |Required HR attribute  |Number of direct reports, which is a non-zero value for managers. |String |
|Person_IsManager |Required HR attribute |True indicates that the person is a manager. |String |
|Person_RoleType |Required HR attribute  |Indicates one of three possible values, which are IC, Manager, or Manager+. |String |
|PersonId |PersonId |De-identified ID number for the person represented in the metric. You can only calculate aggregations, such as counts, of this field. Attempting to return a list of all PersonIds will result in an error. |String |
|PopulationType |Required HR attribute |Currently all the person metric data that’s imported is for measured employees only. |String |
|RecurringMeetingHours |Not applicable |Number of hours the person spent in recurring meetings with at least one other person. |Hour |
|<a name="redundant-define"></a>RedundantMeetingHours |Redundant meeting hours (organizational) |Number of meeting hours a person spent with attendees from three or more distinct levels within that person’s organization. Used in calculating Low quality meeting hours. |Hour |
|<a name="skip-level-define"></a>SkipLevelMeetingHours |Meetings hours with skip level |Number of meeting hours that the person attends where their manager's manager also attends the meeting. |Hour |
|TimeZone |Required HR attribute  |Time zone in which the employee performs work. |String |
|TotalFocusHours |Total focus hours |Total number of hours with two or more one-hour blocks of time where the person had no meetings. |Hour |
|Utilization |Workweek span |The time between the person's first sent email, meeting attended, or Teams call or chat, and the last email, meeting, call, or chat for each day of the work week. The total number of hours are based on the person’s work week that is set in Outlook, which the user can change at any time. If a work week is not defined in Outlook (or if Viva Insights is unable to access a user's Outlook settings), the totals are based on the default of Monday through Friday, with a minimum of four hours and a maximum of 16 hours each day. If reported for the week, the metric is a sum of the daily values for the week. |Hour |
|WorkingHoursCollaboration |Working hours collaboration hours |Number of hours the person spent in meetings and sending emails during working hours. |Hour |
|WorkingHoursCollaborationCalls |Working hours in calls |Total number of hours a person spent time in scheduled and unscheduled calls with Teams, during working hours. |Hour |
|WorkingHoursCollaborationEmails |Working hours email hours |Number of hours the person spent sending email during working hours. |Hour |
|WorkingHoursCollaborationInstantMessages |Working hours instant messages |Total number of hours a person spent time in instant messages through Teams, during working hours. |Hour |
|WorkingHoursCollaborationMeetings |Meeting hours during working hours |Number of hours the person spent in meetings, during working hours, with at least one other person. |Hour |
