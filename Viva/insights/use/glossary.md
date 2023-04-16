---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 02/20/2018
title: Advanced insights glossary
description: This glossary defines concepts and other terms important for working with the advanced insights app for Microsoft Viva Insights
author: madehmer
ms.author: helayne
ms.topic: reference
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin

---
# Glossary for Advanced insights

The following are terms and concepts used in the advanced insights app as part of Microsoft Viva Insights. This glossary excludes [query metric definitions](../use/Metric-definitions.md).

|Term|Definition|
|----|----------|
| <a name="active-employees-define"></a> Active employee | An employee who has sent at least one email or instant message during the time period in question (such as a time period that was defined for a query). |
| Adjusted meeting hours |An adjustment is applied so that overlapping time is not double-counted when a person has overlapping meeting hours. For example, a person with non-declined meeting requests from 2:00 to 3:00 PM and 2:30 to 3:30 PM would yield 1.5 adjusted meeting hours.|
| Aggregation | Aggregation means compiling data from multiple individuals or sources. The more individuals or sources whose data is used, the more difficult it is to identify personal data. Aggregation is one means of achieving de-identification. |
| Attended| A person attended a meeting if they did not decline the meeting request. This means that they either accepted the meeting request, accepted it as _tentative_, or did not respond to it. (This meeting request itself is subsequently referred to as a *non-declined meeting request*.) |
| Attendee|A person who was invited and *attended* the meeting.|
| Attributes|A defined characteristic about the person, such as team, department, or function. *Required attributes* are the subset of attributes that are required in order to calculate metrics.|
|Calendar fragmentation|When a person does not have blocks of time sufficient to focus on completing complex tasks. This is typical of those with only small blocks of time (15, 30, or 60 minutes) between meetings. Anything that is not *focus time* (uninterrupted time blocks of two hours or more with no meetings) is considered calendar fragmentation.|
| <a name="call-define"></a> Call | A scheduled or unscheduled audio or video communication between two or more people over Microsoft Teams. If the call is scheduled, it appears on a person's Outlook calendar as a meeting appointment. A user's call duration is based on their join time and their leave time for the call. | 
|Collaborators| Anyone that *measured employees* or *time investors* interact with by email or instant message, in meetings, in unscheduled calls, or with instant messages. Collaborators are identified as internal (within the company) or external (outside of the company) and discovered through the data extracted for measured employees. Internal collaborators have domains internal to your organization, while external collaborators have domains external to your organization. |
|Collaborator group|A group of collaborators that are identified as internal (within the company) or external (outside of the company) that interacts by email, in meetings, in calls, or with instant messages  with a specified *time investor*.|
| <a name="common-network"></a> Common network | A relationship that is based on an overlap between the collaboration networks of two or more people. For example, Megan and Vinod each has their own set of people with whom they work and meet. These sets of people overlap, which creates an indirect bonding or relationship &mdash; a _common network_ &mdash; between Megan and Vinod.  |
| <a name="conflicting-meeting-define"></a> Conflicting meeting | A meeting on a person's calendar that overlaps with another meeting on that person's calendar.  |
|Connected people |Those who have had more than five connections with external people within the same month. |
|Connected groups |Those who spend a large proportion of their overall collaboration with people outside the company. |
|Connections |Two or more [meaningful interactions](#meaningful-interaction-define) during the past four weeks.|
|Coverage|The percentage of measured employees who have a non-blank value for the specified attribute as shown in [Data sources](/viva/insights/use/organizational-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json). If coverage levels are low, it'll be difficult to determine how people collaborate across different characteristics. Additionally, low coverage on required attributes may give skewed (under reported) metric calculations for metrics that rely on those attributes.|
|Custom attribute|*Organizational data* attributes that describe the people being analyzed. If supplied by the company, these attributes can be used in grouping of data, and to filter reports and customize metrics. However, they are not reserved for metrics calculations.|
| <a name="decision-making-meeting-define"></a> Decision-making meeting | A decision-making meeting has a duration of less than or equal to one hour and has between one and eight attendees (inclusive). |
| De-identification | A process that is used to prevent the connection of personal identifiers with information. |
|Uninterrupted focus hours |Uninterrupted time blocks of one or more hours with no meetings, emails, calls, or Teams IMs.|
|Fragmented hours | A person's time after you subtract their meeting hours and their focus hours. |
|Hashing | Hashing is a cryptographic process that converts a piece of data into another in a way that is easy to compute, extremely difficult to reverse, and highly unlikely that two different pieces of data have the same hash. For example, meeting [subject lines](/viva/insights/use/privacy-settings?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#hash-subject-lines) that are hashed would appear not in their original, readable, form but as a meaningless number. |  
|Influence |Indicates a person or group's potential influence on opinions of the network or an estimate of social status. The number and strength of connections between employees and the relative collaboration time between them. |
|Insularity|When collaboration happens only with people from within a person’s team, function, department, and so on.|
|Invitee|A person who is invited to a meeting with a meeting request.|
| <a name="large-meeting-define"></a> Large meeting | A large meeting has a duration of less than or equal to one hour and has nine or more attendees. Also see [Long and large meeting](#long-and-large-meeting-define).|
|Layer|The number of *levels* of reporting in a company, starting from CEO and going down. For example, the CEO equals level 0.|
|Level|A *required optional attribute* that is a company-specific way of organizing employees by job experience or seniority. |
| <a name="long-meeting-define"></a> Long meeting | A long meeting has a duration of greater than one hour and has fewer than nine attendees. Also see [Long and large meeting](#long-and-large-meeting-define). |
| <a name="long-and-large-meeting-define"></a> Long and large meeting | A long and large meeting has a duration of more than one hour and has more than eight attendees. Also see [large meeting](#large-meeting-define) and [long meeting](#long-meeting-define).|
| <a name="meaningful-interaction-define"></a>Meaningful interaction | A meaningful interaction is defined as one of the following types of collaboration: <li>an email</li><li>a meeting</li><li>a call</li><li>three instant messages. These messages could be sent by any of the collaborators in the chat. For example, they could be: (a) three messages sent by one individual to others in Teams, or (b) three distinct messages from distinct senders within the same Teams chat.<p><p>Moreover, every meaningful interaction must have at least two collaborators but at most eight collaborators participating in the interaction.  |
| <a name="measured-employees-define"></a> Measured employees | The employees to whom your Viva Insights admin assigned licenses during setup. After license assignment, Viva Insights extracts Microsoft 365 data about meetings, email, unscheduled calls, and instant messages for these people. If you are an analyst or limited analyst, this is the population that you can analyze within Viva Insights. The number of measured employees can help determine whether you have good data coverage for analysis.|
| <a name="meeting-define"></a> Meeting | An audio or video communication or in-person meeting that has been scheduled -- that is, it appears on a person's Outlook calendar. A meeting must involve two or more people. Outlook calendar events determine the durations of meetings. |
|Multitasking|The concept of not staying focused on the task at hand. Defined in Viva Insights as a person sending two emails or more per meeting hour, and in meetings shorter than an hour, two emails or more per meeting.|
|Multitasking hours |Total number of hours the person spent sending emails or instant messages during a meeting or a Teams call. |
|Non-declined meeting request|In Viva Insights, this is synonymous with *attended*.|
|Optional attribute|Optional *organizational data* attributes that describe the people being analyzed. If supplied by the company, you can use these attributes to explore metrics, filter queries, and customize metrics. These can be reserved for future metric calculations. Optional attributes include FunctionType, HireDate, HourlyRate, Layer, and TimeZone.|
|Organization|A *required attribute* that describes the organizational unit in which the employee resides. The exact value will be determined by the company’s structure, as well as how that structure is captured in within the company’s human resources information system. For example, the organization might also be known as department, function, or defined by a specific manager name in the management hierarchy. |
|Organizational data |Attributes about people in the organization or people who collaborate with the organization that Viva Insights can analyze. Most organizational data is obtained from a company’s human resources (HR) information system. For example, job family, job role, organization, line of business, cost center, location, region, layer, level, number of direct reports, manager, and so on. |
|Organizational network analysis (ONA) |A quantitative method for modeling and analyzing how communications, information, decisions, and resources flow through an organization. It is used in business management and the social and behavioral sciences. |
|Organizer|The person who organizes a meeting. This person is also counted as an *attendee*.|
|People meeting hours|The sum of adjusted meeting hours for each person in the meeting. For example, if a meeting lasts at least one hour with three attendees (and no attendees have overlapping meetings), the people meeting hours for that meeting is three.|
|Person|The *measured employee* for whom the metric is calculated.|
|Personal data  | <!--Personal data is any data that can be used to identify a specific person. Examples of personal data are email addresses, telephone numbers, IP addresses, and digital images. --> Personal data is any data that relates to an identified or identifiable natural person. An identifiable person is one who can be identified (directly or indirectly), in particular through an identifier such as a name, an identification number, location data, online identifier, or through one or more factors specific to the physical, physiological, genetic, mental, economic, cultural, or social identity of that person.|
|Recipient |A person receiving an email (includes people in the to, cc, and bcc lines). |
|Redundancy (organizational)|Organizational redundancy is present if at least three attendees are from different levels within the same organization. For example, a meeting whose attendees included a General Manager, a Director, and an Independent Contributor from the same organization would be a redundant meeting.|
|Redundancy (lower level)|An attendee is considered redundant at the lower level if both the attendee's manager and skip-level manager are present in the meeting.|
|Required attribute|Mandatory organizational data attributes that describe the people being analyzed. Required attributes are used in Viva Insights to explore, calculate, and customize metrics and filter query results. Required attributes include PersonId, EffectiveDate, ManagerId, and Organization.|
|Sender|The person who sends an email.|
|Span|The number of direct reports per manager.|
|Time investor|A *measured employee* who interacts with other collaborators in meetings and with email or instant messages. Time investors allocate their time with the other participants or *collaborators* in the interaction in proportion to how many people are in the collaborator group for that interaction. People who do not have a license for Viva Insights can appear as collaborators, but never as time investors.|
|Time zones|Viva Insights uses these [time zones](/viva/insights/use/timezones-for-workplace-analytics?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json). Personal metrics (person query results) are calculated by using the person’s time zone. Meeting metrics (meeting query results) are calculated by using the organizer’s time zone.|
|Working hours|Hours that represent the typical workweek for the company. The Viva Insights default setting is Monday through Friday from 8:00 AM to 5:00 PM for calculations of working hours. This default is only used for users who have not already set up their working days and hours in Outlook. Your admin can change the default working days and hours in **Analyst settings** > [System defaults](/viva/insights/use/system-defaults?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

### Related topic

[Metric descriptions for Advanced insights](../use/Metric-definitions.md)

