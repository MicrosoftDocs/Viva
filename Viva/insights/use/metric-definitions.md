---

title: Metric definitions for Advanced insights
description: Describes the metrics for queries that are available in Microsoft Viva Insights, including Person, Meeting, Group-to-group, Person-to-group, and Network query metrics 
author: madehmer
ms.author: helayne
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

# Advanced insights metric descriptions

To customize [queries](/viva/insights/tutorials/query-basics?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json), you can use the metrics that are defined on this page. They are organized by query type:

* [Person metrics](#person-metrics)
* [Peer comparison metrics](#peer-comparison-metrics)
* [Meeting metrics](#meeting-metrics)
* [Group-to-group metrics](#group-to-group-metrics)
* [Person-to-group metrics](#person-to-group-metrics)
* [Network metrics](#network-metrics)

## Person metrics

The metrics in this table are used both in [person queries](/viva/insights/tutorials/person-queries?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) and in [peer-comparison](/viva/insights/tutorials/comparison-query?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) queries.

>[!Note]
>In Microsoft Teams, teamwork and communication happen in channels. Viva Insights includes several "channel metrics," which measure aspects of team communication over channels (both public channels and private channels) in Teams. These metrics are defined in the following table. When these metrics first become available in the advanced insights app in August, 2021, they will reflect a baseline of only 30 days of historical data; this historical data will increase as time progresses. This differs from other metrics, which usually have 13 months of historical baseline data.

<!-- BE SURE TO REMOVE THIS NOTE AT SOME POINT. ASK RADHIKA HOW LONG IT SHOULD BE RETAINED. 13 MONTHS FROM AUGUST 2021? -->

|Metric |Description |Query type |Data type |Customizable |
|------|-----------|----------|---------|------------|
| After hours channel message hours | The number of hours that a person spent sending and reading posts and replies in Teams channels, outside of work hours. | Person | Hour | Yes |
|<a name="after-hours-collaboration-define"></a>After hours collaboration | Number of hours the person spent in meetings, emails, IMs, and calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting), outside of working hours.  <!-- Number of hours the person spent in meetings and on email outside of working hours. **Note**: To target or filter for after-hours collaboration, you can use a filter with the Collaboration hours metric. --> | Person | Hour | No |
|After hours email hours |Number of hours the person spent sending and receiving emails outside of working hours.|Person|Hour|Yes|
|After hours in calls |Number of hours a person spent in scheduled and unscheduled calls through Teams, outside of working hours. For calls that started during working hours, this number only includes the part of the call that occurred outside of that person’s work schedule (as set in Outlook). |Person|Hour|Yes|
|After hours instant messages |Number of hours a person spent in instant messages through Teams, outside of working hours. |Person|Hour|Yes|
|After hours meeting hours|Number of hours the person spent in meetings outside of working hours.|Person|Hour|Yes|
|Call hours| The number of hours that a person spent in scheduled and unscheduled calls through Teams with at least one other person, during and outside of working hours.| Person| Hour | Yes |
| Channel message hours | The number of hours that a person spent sending and reading posts and reply messages in Teams channels, during and after work hours. | Person | Hour | Yes |
| Channel messages sent | The total number of posts and replies sent per person in Teams channels, during and after work hours. | Person | Count | Yes |
| Channel reactions | The total number of reactions to posts and replies on Teams channels, during and after work hours. | Person | Count | Yes |
| Channel visits | The total number of visits per person to Teams channels, during and after work hours. | Person | Count | Yes |
| Channels with active engagement | The number of distinct channels in which a person posted, replied, visited, or reacted to a message during the aggregation period of the query. |Person | Count | Yes |
|<a name="collaboration-hours-define"></a>Collaboration hours | Number of hours the person spent in meetings, emails, IMs, and calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting). | Person | Hour | Yes |
|<a name="collaboration-hours-external-define"></a> Collaboration hours external | Number of hours the person spent in meetings, emails, IMs, and calls with at least one other person outside the company, after deduplication of time due to overlapping activities (for example, calls during a meeting).  | Person | Hour | No |
|<a name="conflicting-meeting-hours-define"></a>Conflicting meeting hours|Number of meeting hours where the person had overlapping meetings in their calendar. The count includes the entire duration of all overlapping meetings, not just the amount of time that overlaps. (This number includes all non-declined meeting times, which includes accepted, tentative, or no responses to meeting invitations.)|Person|Hour|Yes|
|Email hours | Number of hours the person spent sending and receiving emails. |Person|Hour|Yes|
| <a name="emails-sent-define"></a> Emails sent|Number of emails the person sent.|Person|Count|Yes|
|External network size|The number of people external to the company with whom the person had at least two [meaningful interactions](/viva/insights/use/glossary?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#meaningful-interaction-define) in the last four weeks. |Person|Count|Yes|  
| <a name="generated-reactions-to-posts-define"></a> Generated reactions to posts | The total number of reactions generated to posts sent by the person on Teams channels. |Person|Count|No|
| <a name="generated-replies-to-posts-define"></a> Generated replies to posts | The total number of replies generated to posts sent by the person on Teams channels. |Person|Count|No|
| <a name="generated-workload-call-hours-define"></a> Generated workload call hours|Number of hours that the person spent calling internal recipients through Teams.|Person|Hour|Yes|
| <a name="generated-workload-call-participants-define"></a> Generated workload call participants|Number of internal participants of calls that were organized by the person. (Counts each participant once for each call.)|Person|Count|Yes|
| <a name="generated-workload-calls-organized-define"></a> Generated workload calls organized|Number of calls that were organized by the person. |Person|Count|Yes|
| <a name="generated-workload-email-hours-define"></a> Generated workload email hours| Number of email hours that the person created for internal recipients by sending emails. |Person|Hour|Yes|
| <a name="generated-workload-email-recipients-define"></a> Generated workload email recipients|Number of internal recipients on emails that were sent by the person. (Counts each recipient once for each email received.)|Person|Count|Yes|
| <a name="generated-workload-instant-message-hours-define"></a> Generated workload instant message hours|Number of instant message hours that the person created through Teams for internal recipients by sending instant messages.|Person|Hour|Yes|
| <a name="generated-workload-instant-message-recipients-define"></a> Generated workload instant message recipients|Number of internal participants of calls that were organized by the person. (Counts each participant once for each call.)|Person|Count|Yes|
| <a name="generated-workload-meeting-attendees-define"></a> Generated workload meeting attendees|Number of internal attendees in meetings that were organized by the person. (Counts each attendee once for each meeting.)|Person|Count|Yes|
| <a name="generated-workload-meeting-hours-define"></a> Generated workload meeting hours|Number of meeting hours that the person created for internal attendees by organizing meetings.|Person|Hour|Yes|
| <a name="generated-workload-meetings-organized-define"></a> Generated workload meetings organized|Number of internal meetings that were organized by the person.|Person|Count|Yes|
|Instant message hours | Number of hours that a person spent in instant messages (IMs) through Teams with at least one other person, during and outside of working hours.| Person| Hours| Yes |
|Instant messages sent | Total number of instant messages (IMs) sent by a person through Teams, during and outside of working hours. | Person| Count| Yes |
|Internal network size|   The number of people within the company with whom the person had at least two [meaningful interactions](/viva/insights/use/glossary?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#meaningful-interaction-define) in the last four weeks.  |Person|Count|Yes |
|  <a name="low-quality-meeting-hours-define"></a> Low-quality meeting hours |Number of meeting hours in which an attendee was multitasking, attended a *conflicting meeting*, or attended a meeting that exhibits *Redundancy (organizational)*. Viva Insights admins can [set the hourly rate](/viva/insights/use/system-defaults?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#hourly-rate) of low-quality meeting time; if this value has not been set, the cost defaults to $75 per person hour. **Note**: Calculations for conflicting meeting hours are affected by meeting exclusion rules and adjustments based on the type of meetings that overlap (non-declined work meetings, focus hours, and out-of-office time).|Person|Hour|Yes|
|Manager coaching hours 1:1|Total number of hours that a manager spends in one-on-one meetings with *all* of the manager's direct reports. |Person|Hour|Yes|
|<a name="meeting-hours-define"></a>Meeting hours|Number of hours the person spent in meetings with at least one other person during and outside of working hours.|Person|Hour|Yes|
|Meeting hours during working hours|Number of hours the person spent in meetings, during working hours, with at least one other person.|Person|Hour|Yes|
| <a name="meeting-hours-with-manager-define"></a>  Meeting hours with manager | Number of meeting hours where attendees included at least the person and their manager.|Person|Hour|Yes|
| <a name="meeting-hours-with-manager-1-1-define"></a> Meeting hours with manager 1:1|Number of meeting hours involving only the person and their manager.|Person|Hour|Yes|
| Meetings hours with skip level|Number of meeting hours that the person attends where their manager's manager also attends the meeting.|Person|Hour|Yes|
| Meetings|Number of meetings the person attended.|Person|Count|Yes|
| Meetings with manager|Number of meetings where attendees include at least the person and their manager.|Person|Count|Yes|
| Meetings with manager 1:1|Number of meetings involving only the person and their manager.|Person|Count|Yes|
| Meetings with skip level|Number of meetings where the manager of the person's manager is an attendee.|Person|Count|Yes|
| <a name="multitasking-hours-define"></a>Multitasking hours |Number of hours the person spent sending emails or instant messages during a meeting or a Teams call.|Person|Hour|No|
| <a name="multitasking-meeting-hours-define"></a>Multitasking meeting hours|Number of meeting hours where the person sent two or more emails per meeting hour. If less than an hour in length, the calculation is two emails or more sent per meeting. New options are available for measuring multitasking volume and frequency that also reflect Teams activity. To measure how frequently meetings or Teams calls are interrupted by emails or instant messages, add the "Included multitasking" filter to the "Meetings" metric or "Calls" metric. To measure the volume of time spent sending emails or instant messages during a meeting or Teams call, check out [Multitasking hours](/viva/insights/use/metric-definitions?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#multitasking-hours-define). |Person|Hour|Yes|
| Networking outside company|The number of distinct external domains outside the company a person has had at least two [meaningful interactions](/viva/insights/use/glossary?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#meaningful-interaction-define) in the last four weeks. |Person|Count|Yes |
| Networking outside organization| The number of distinct organizational units within the company that the person had at least two [meaningful interactions](/viva/insights/use/glossary?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#meaningful-interaction-define) in the last four weeks. |Person|Count|Yes |
|Open 1 hour block |Number of one-hour blocks in the person’s calendar without meetings during the workday.|Person|Count|Yes|
|Open 2 hour blocks |Number of two-hour blocks in the person’s calendar without meetings during the workday.|Person|Count|Yes|
|Peer average (customer collaboration) | The total amount (in hours) of customer collaboration for all of the participants in the plan divided by the number of participants in the plan. | Person | Hour | No|
|Peer average (internal collaboration) | The total amount (in hours) of internal collaboration for all of the participants in the plan divided by the number of participants in the plan. | Person | Hour | No|
|Redundant meeting hours (lower level) |Number of meeting hours a person spent in a meeting with both their manager and their skip-level manager present in the meeting. <br> <br> This metric is _not_ used in calculating *Low-quality meeting hours*. Analysts can use this metric only when creating [Person queries](/viva/insights/tutorials/person-queries?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).|Person | Hour| Yes |
|<a name="redundant-meeting-hours-define"></a> Redundant meeting hours (organizational) |Number of meeting hours a person spent with attendees from three or more distinct levels within that person’s organization. Used in calculating *Low quality meeting hours*.  |Person|Hour|Yes|
|Teams with active engagement | The number of distinct teams in which a person posted, replied, visited, or reacted to a message during the aggregation period of the query.  | Person | Count | Yes|
|Time in self-organized meetings|Number of hours spent in meetings organized by the person with at least one other person.|Person|Hour|Yes|
|Total calls | Total number of calls a person joined through Teams, including scheduled and unscheduled calls during and outside of working hours (as set in Outlook). |Person |Count |Yes |
|Total emails sent during meeting | By the end of August 2021, this metric will be discontinued and unavailable for any future query data. Alternatively, for the same query results, use [Emails sent](/viva/insights/use/metric-definitions?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#emails-sent-define) and add the “Is sent during meeting” filter to customize that metric. |Person |Count |Yes |
|<a name="focus-define"></a> Total focus hours|Total number of hours made up of two-hour or more blocks of time where the person had no meetings. The new "Uninterrupted focus hours" metric is now available. It measures the total number of hours where a person has more than or equal to a one-hour block of uninterrupted time to focus on work during their set working hours. Uninterrupted time is when the person has no collaboration activity, including attending a meeting or an unscheduled Teams call, sending emails, or replying or sending an instant message or Teams chat. |Person|Hour|No|
| Working hours channel message hours | The number of hours that a person spent sending and reading posts and replies in Teams channels, during work hours. | Person | Hour | Yes |
|Uninterrupted focus hours |Total number of hours where a person has more than or equal to a one-hour block of uninterrupted time to focus on work during their set working hours. It's only counted as uninterrupted time when the person has no collaboration activity, including attending a meeting or an unscheduled Teams call, sending an email, or sending a Teams instant message.	|Person|Hour|No|
|<a name="working-hours-collaboration-hours-define"></a> Working hours collaboration hours | Number of hours the person spent in meetings, emails, IMs, and calls with at least one other person, either internal or external, after deduplication of time due to overlapping activities (for example, calls during a meeting), during working hours. | Person | Hour | No |
|<a name="working-hours-email-hours-define"></a> Working hours email hours| Number of hours the person spent sending and receiving emails during working hours. |Person|Hour|Yes|
|Working hours in calls| Total number of hours a person spent time in scheduled and unscheduled calls with Teams, during working hours. | Person| Hour| Yes |
|Working hours instant messages| Total number of hours a person spent time in instant messages through Teams, during working hours. | Person| Hour| Yes |
| <a name="workweek-span-define"></a> Workweek span | The time between the person's first sent email, meeting attended, or Teams call or chat, and the last email, meeting, call, or chat for each day of the work week. The total number of hours are based on the person’s work week that is set in Outlook, which the user can change at any time. If a work week is not defined in Outlook (or if the advanced insights app is unable to access a user's Outlook settings), the totals are based on the default of Monday through Friday, with a minimum of four hours and a maximum of 16 hours per day. If reported for the week, the metric is a sum of the daily values for the week. If reported for the month, the metric is the sum of the daily values for the month. |Person|Hour|No|

## Peer-comparison metrics
  
Peer-comparison queries use the same metrics as person queries. See [Person metrics](#person-metrics).
  
## Meeting metrics

|Metric|Description|Query type|Data type|Customizable|
|------|-----------|----------|---------|------------|
| <a name="attendee-meeting-hours-define"></a> Attendee meeting hours|Total number of adjusted meeting hours for all attendees.<br>A _[meeting query](/viva/insights/Tutorials/meeting-queries?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)_ focuses on the meeting as the main entity and reports on the various meeting attributes; a _[person query](/viva/insights/Tutorials/person-queries?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)_ looks from a person's perspective and aggregates multiple meetings for the selected time period. Because the two query types have different purposes, their output also differs. |Meeting|Hour|Yes|
| <a name="attendees-define"></a> Attendees|Number of people who attended the meeting.|Meeting|Count|Yes|
|Attendees multitasking |Number of attendees that sent emails or instant messages during a meeting. |Meeting|Count|Yes|
| <a name="attendees-with-conflicting-meeting-define"></a> Attendees with conflicting meeting|Number of attendees with meetings that overlap with the meeting (includes all non-declined meetings, which include accepted, tentative, and no responses to meeting invites).|Meeting|Count|Yes|
|Emails sent during meetings|Number of emails the person sent during all meetings.|Meeting|Count|Yes|
|Instant messages sent during meetings |Number of instant messages sent by attendees during the scheduled meeting time. |Meeting|Count|Yes|
|Invitees|Number of people invited to the meeting.|Meeting|Count|Yes|
|Redundant attendees | The number of attendees of a meeting who are redundant, as defined by the _Redundant meeting hours (lower level)_ metric. For more information about _Redundant meeting hours (lower level)_, see the table that lists [Person metrics](#person-metrics).  |Meeting|Count|Yes|
|Total meeting cost|The total cost of all attendees in a meeting. The meeting cost for each attendee is defined as the product of the attendees' meeting hours multiplied by the attendees' hourly rates. If no hourly rate is available for one or more attendees, the default rate of $75/hr (US dollars) is used to calculate the cost of those attendees.|Meeting|Currency|Yes|
|Total redundant hours|The total number of redundant hours metric for all attendees in a meeting.|Meeting|Hour|Yes|

## Group-to-group metrics

|Metric|Description|Query type|Data type|Customizable|
|------|-----------|----------|---------|------------|
| Channel messages sent | The total number of channel posts and replies sent on Teams channels by the time investor to one or more people in the collaborator group. | Group | Count | Yes |
| <a name="collaboration-hours-define"></a> Collaboration hours | Number of hours spent in meetings, emails, IMs, and calls, after deduplication of time due to overlapping activities (for example, calls during a meeting) between the time investor and collaborator groups.  |Group|Hour|No|
| <a name="email-hours-define"></a> Email hours | Number of hours spent sending and receiving emails between the time investor and collaborator groups.  |Group|Hour|No|
|Meeting attendee count|Total number of attendees in all meetings from the time investor and collaborator groups.|Group|Count|No|
|Meeting hours |Number of meeting hours the time investor group has spent meeting with the collaborator group.|Group|Hour|No|
|Meeting invitee count|Total number of invitees in all meetings from the time investor and collaborator groups.|Group|Count|No|
|Meetings |Number of distinct meetings with at least one attendee from the time investor and collaborator groups.|Group|Count|No|
|Time investors initiated meeting hours | This calculates the number of meeting hours the time investors created only for *[Internal collaborators](/viva/insights/use/csv-query-output-file?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#internal-collaborators)* or *[Collaborators within group](/viva/insights/use/csv-query-output-file?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#collaborators-within-group)* by organizing meetings. (Does not follow time-allocation logic.)​ |Group|Hour|No|

## Person-to-group metrics

|Metric|Description|Query type|Data type|Customizable|
|------|-----------|----------|---------|------------|
| Channel messages sent | The total number of channel posts and replies sent on Teams channels by the time investor to one or more people in the collaborator group. | Group | Count | Yes |
| <a name="diverse-tie-score-define"></a> Collaboration hours | Number of hours that the time investor spent in meetings, emails, IMs, and calls with one or more people in the collaborator group, after deduplication of time due to overlapping activities (for example, calls during a meeting). |Group|Hour|No|
|Email count|Count of unique email exchanges (sent and received) that the time investor had with one or more people in the collaborator group. |Group|Count|No|
| <a name="email-hours-define"></a> Email hours| Number of hours that the time investor spent sending and receiving emails with one or more people in the collaborator group.  |Group|Hour|No|
| <a name="lasttimecontacted-define"></a> Last time contacted |The last date and time that the time investor (a measured employee) emailed or attended a meeting with one or more people in the collaborator group for the specified date range. Note that this metric refers only to interactions that were initiated by the time investor. |Group|DateTime|No|
|Meeting hours|Total number of hours that the time investor spent in meetings with one or more people in the collaborator group. This metric uses time allocation logic. |Group|Hour|No|
|Meetings|Number of unique meetings that the time investor attended with one or more people in the collaborator group. |Group|Count|No|
|Network size|Number of people in the collaborator group who had at least two [meaningful interactions](/viva/insights/use/glossary?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#meaningful-interaction-define) in the last 28 days with the time investor. This counts both licensed and unlicensed employees in the collaborator group. |Group|Count|No|

## Network metrics

The following network metrics are based on the collaboration activities, including: emails, meetings, Teams calls, and Teams chats.

|Metric|Description|Query type|Data type|Customizable|
|------|-----------|----------|---------|------------|
| <a name="diverse-tie-score-define"></a> Diverse tie score | A numeric score that indicates how varied and how broad a person's connections are. This is based on both the infrequent direct collaboration between two people and on the differences in the common network they share between themselves. (Collaboration activities consist of emails, [meetings](/viva/insights/use/glossary?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#meeting-define), Teams [calls](/viva/insights/use/glossary?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#call-define), and Teams chats.) <br>A person need not have much direct collaboration with their diverse ties, so it’s easy to have more diverse ties than [strong ties](#strong-tie-score-define). Diverse ties present good sources of fresh and varied information from across the company. | ONA | Score | No |
| <a name="diverse-tie-type-define"></a> Diverse tie type | A value that indicates the relative diversity of the person's diverse ties. 0 means that the tie is not diverse; 1 means that the tie is diverse; 2 is an intermediate value that means more diverse than 0 but less diverse than 1. (The Diverse tie type metric is derived from the [Diverse tie score](#diverse-tie-score-define) metric, which in turn is based on the thresholds that are described in [The last columns give the results](/viva/insights/tutorials/ona-person-to-person-query?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#the-last-columns-give-the-results).) | ONA | Score | No |
| <a name="diverse-ties-define"></a> Diverse ties | The number of diverse ties that the person has, that is, the number of ties whose [Diverse tie type](#diverse-tie-type-define) is 1. | ONA | Count | No |
| <a name="influence-define"></a> Influence |A numeric score that indicates how well connected a person is within the company. A higher score means that the person is better connected and has greater potential to drive change. (A person’s connection score is based on the frequency of collaboration activities, which include emails, [meetings](/viva/insights/use/glossary?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#meeting-define), Teams [calls](/viva/insights/use/glossary?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#call-define), and Teams chats with other people within the company.) | ONA | Score | No |
| <a name="influence-rank-define"></a> Influence rank | One of a sequence of numbers that starts with 1. A rank of 1 represents the person with the greatest [Influence](#influence-define) score; a rank of 2 represents the person with the next greatest Influence score, and so on. If two people have the same Influence score, they also have the same influence rank. | ONA | Score | No |
| <a name="manager-overlapping-strong-ties-define"></a> Manager overlapping strong ties | The number of strong ties that are in common between a manager and their direct reports. If a manager shares a significant number of strong ties with their directs, this can indicate that they are on the same page and executing on a well known, well understood, common plan. This metric reflects the manager's ability to ensure that the team is working toward progress and team members are up to speed. | ONA | Count | No |
| <a name="manager-unique-strong-ties-define"></a> Manager unique strong ties | The number of strong ties that are unique in the manager's network when contrasted with the strong ties of their direct reports. This metric helps answer the question: "What is the potential of this manager to bring fresh connections and fresh ideas to their team?" | ONA | Count | No |
| <a name="strong-tie-score-define"></a> Strong tie score | A numeric score that indicates how strong and tight a person’s engagements are. It is based on both direct collaboration between two people and on the common network they share. (Collaboration activities consist of emails, [meetings](/viva/insights/use/glossary?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#meeting-define), Teams [calls](/viva/insights/use/glossary?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#call-define), and Teams chats.) <br>For example, a "strong tie" between a manager and a direct report reflects both the amount of direct collaboration they have with each other and the time they both invest in connections that are common to both of them. Typically, a person has only a few strong ties because such ties take more effort to maintain. | ONA | Score | No |
| <a name="strong-tie-type-define"></a> Strong tie type | A value that indicates the relative strength of the person's strong ties. 0 means that the tie is not strong; 1 means that the tie is strong; 2 is an intermediate value that means stronger than 0 but weaker than 1. (The Strong tie type metric is derived from the [Strong tie score](#strong-tie-score-define) metric, which in turn is based on the thresholds that are described in [The last columns give the results](/viva/insights/tutorials/ona-person-to-person-query?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#the-last-columns-give-the-results).) | ONA | Score | No |
| <a name="strong-ties-define"></a> Strong ties | The number of strong ties that the person has; that is, the number of ties whose [Strong tie type](#strong-tie-type-define) is 1. | ONA | Count | No |
