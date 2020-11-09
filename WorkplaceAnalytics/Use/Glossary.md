---

title: Workplace Analytics Glossary
description: This glossary defines concepts and other terms important for working with Workplace Analytics
author: paul9955
ms.author: v-mideh
ms.topic: reference
localization_priority: normal 
ms.prod: wpa

---

# Glossary for Workplace Analytics

The following are terms and concepts used in Workplace Analytics. This glossary excludes [query metric definitions](../use/Metric-definitions.md).

|Term|Definition|
|----|----------|
| Adjusted meeting hours |An adjustment is applied so that overlapping time is not double-counted when a person has overlapping meeting hours. For example, a person with non-declined meeting requests from 2:00 to 3:00 PM and 2:30 to 3:30 PM would yield 1.5 adjusted meeting hours.|
| Aggregation | Aggregation means compiling data from multiple individuals or sources. The more individuals or sources whose data is used, the more difficult it is to identify personal data. Aggregation is one means of achieving de-identification. |
| Anonymization | Anonymized data is information that does not relate to a specific individual, that does not increase the likelihood that a specific individual can be identified, or that has been rendered in a way so that it cannot be used to identify a specific individual. |
| Attended| A person attended a meeting if they did not decline the meeting request. This means that they either accepted the meeting request, accepted it as _tentative_, or did not respond to it. (This meeting request itself is subsequently referred to as a *non-declined meeting request*.) |
| Attendee|A person who was invited and *attended* the meeting.|
| Attributes|A defined characteristic about the person, such as team, department, or function. *Required attributes* are the subset of attributes that are required in order to calculate metrics.|
|Calendar fragmentation|When a person does not have blocks of time sufficient to focus on completing complex tasks. This is typical of those with only small blocks of time (15, 30, or 60 minutes) between meetings. Anything that is not *focus time* (uninterrupted time blocks of two hours or more with no meetings) is considered calendar fragmentation.|
| <a name="call-define"></a> Call | A scheduled or unscheduled audio or video communication between two or more people over Microsoft Teams. If the call is scheduled, it appears on a person's Outlook calendar as a meeting appointment. The call duration for a user is based on the join and leave time of the user for that call. <!-- EDIT THIS --> This is because we do processing logic in Collaboration hours metric to prevent double counting of a Teams call with a Meeting, but the standalone Meeting and Call metrics show scheduled meetings that are on Teams independently unless user applies a filter. We should also add another sentence “ Call duration is based on join and leave time of the user” as we often get customer question on how it’s calculated. |
|Collaborators| Anyone that *measured employees* or *time investors* interact with by email or instant message, in meetings, in unscheduled calls, or with instant messages. Collaborators are identified as internal (within the company) or external (outside of the company) and discovered through the data extracted for measured employees. Internal collaborators have domains internal to your organization, while external collaborators have domains external to your organization. |
|Collaborator group|A group of collaborators that are identified as internal (within the company) or external (outside of the company) that interacts by email, in meetings, in calls, or with instant messages  with a specified *time investor*.|
| <a name="common-network"></a> Common network | A relationship that is based on an overlap between the collaboration networks of two or more people. For example, Megan and Vinod each has their own set of people with whom they work and meet. These sets of people overlap, which creates an indirect bonding or relationship &mdash; a _common network_ &mdash; between Megan and Vinod.  |
| <a name="conflicting-meeting-define"></a> Conflicting meeting | A meeting on a person's calendar that overlaps with another meeting on that person's calendar.  |
|Connected people |Those who have had more than five connections with external people within the same month. |
|Connected groups |Those who spend a large proportion of their overall collaboration with people outside the company. |
|Connection|Two or more [meaningful interactions](#meaningful-interaction-define).|
|Coverage|The percentage of measured employees who have a non-blank value for the specified attribute as shown in [Data sources](../use/organizational-data.md). If coverage levels are low, it'll be difficult to determine how people collaborate across different characteristics. Additionally, low coverage on required attributes may give skewed (under reported) metric calculations for metrics that rely on those attributes.|
|Custom attribute|*Organizational data* attributes that describe the people being analyzed. If supplied by the company, these attributes can be used in grouping of data, and to filter reports and customize metrics. However, they are not reserved for metrics calculations.|
| <a name="decision-making-meeting-define"></a> Decision-making meeting | A meeting that has between two and eight attendees and lasts less than one hour. |
| De-identification | A process that is used to prevent the connection of personal identifiers with information. De-identification is achieved through the removal of personal data, which is sometimes replaced with a pseudonymous identifier. | 
|Focus time|Uninterrupted time blocks of two hours or more with no meetings.|
|Fragmented hours | A person's time after you subtract their meeting hours and their focus hours. |
| Hashing | Hashing is a cryptographic process that converts a piece of data into another in a way that is easy to compute, extremely difficult to reverse, and highly unlikely that two different pieces of data have the same hash. For example, meeting [subject lines](settings.md#hash-subject-lines) that are hashed would appear not in their original, readable, form but as a meaningless number. |  
|Insularity|When collaboration happens only with people from within a person’s team, function, department, and so on.|
|Invitee|A person who is invited to a meeting with a meeting request.|
| <a name="large-meeting-define"></a> Large meeting |A large meeting  involves more than eight people<!-- ADDED THIS 23 OCT:--> and lasts less than one hour. Also see [Long and large meeting](#long-and-large-meeting-define).|
|Layer|The number of *levels* of reporting in a company, starting from CEO and going down. For example, the CEO equals level 0.|
|Level|A *required attribute* that is a company-specific way of organizing employees by job experience or seniority. |
| <a name="long-meeting-define"></a> Long meeting | A long meeting is scheduled for more than one hour and has more than one but fewer than nine attendees<!-- ADDED 'fewer than nine' 23 OCT-->. Also see [Long and large meeting](#long-and-large-meeting-define). |
| <a name="long-and-large-meeting-define"></a> Long and large meeting |A long and large meeting has more than eight attendees and is scheduled for longer than one hour. |
| <a name="meaningful-interaction-define"></a>Meaningful interaction | A meaningful interaction is defined as one of the following types of collaboration: <li>an email</li><li>a meeting</li><li>a call</li><li>three instant messages. These messages could be sent by any of the collaborators in the chat. For example, they could be: (a) three messages sent by one individual to others in Teams, or (b) three distinct messages from distinct senders within the same Teams chat.<p><p>Moreover, every meaningful interaction must have at least two collaborators but at most eight collaborators participating in the interaction.  |
| <a name="measured-employees"></a> Measured employees | The employees to whom your Workplace Analytics administrator assigned licenses during setup. After license assignment, Workplace Analytics extracts Office 365 data about meetings, email, unscheduled calls, and instant messages for these people. If you are an analyst or limited analyst, this is the population that you can analyze within Workplace Analytics. The number of measured employees can help determine whether you have good data coverage for analysis.|
| <a name="meeting-define"></a> Meeting | An audio or video communication or in-person meeting that has been scheduled -- that is, it appears on a person's Outlook calendar. A meeting must involve two or more people. Its duration is based on the Outlook calendar event. <!--EDIT HERE --> It may not be exactly be the time shown on Outlook calendar event as we apply post processing logic to remove overlapping meetings, meeting exclusions which impacts the duration from the exact time shown on Outlook. |
|Multitasking|The concept of not staying focused on the task at hand. Defined in Workplace Analytics as a person sending two emails or more per meeting hour, and in meetings shorter than an hour, two emails or more per meeting.|
|Non-declined meeting request|In Workplace Analytics, this is synonymous with *attended*.|
|Optional attribute|Optional *organizational data* attributes that describe the people being analyzed. If supplied by the company, you can use these attributes to explore metrics, filter queries, and customize metrics. These can be reserved for future metric calculations. Optional attributes include FunctionType, HireDate, HourlyRate, Layer, and TimeZone.|
|Organization|A *required attribute* that describes the organizational unit in which the employee resides. The exact value will be determined by the company’s structure, as well as how that structure is captured in within the company’s human resources information system. For example, the organization might also be known as department, function, or defined by a specific manager name in the management hierarchy. |
|Organizational data |Attributes about people in the organization or people who collaborate with the organization that Workplace Analytics can analyze. Most organizational data is obtained from a company’s human resources information system. For example, job family, job role, organization, line of business, cost center, location, region, layer, level, number of direct reports, manager, and so on. |
|Organizer|The person who organizes a meeting. This person is also counted as an *attendee*.|
|People meeting hours|The sum of adjusted meeting hours for each person in the meeting. For example, if a meeting lasts at least one hour with three attendees (and no attendees have overlapping meetings), the people meeting hours for that meeting is three.|
|Person|The *measured employee* for whom the metric is calculated.|
|Personal data  | <!--Personal data is any data that can be used to identify a specific person. Examples of personal data are email addresses, telephone numbers, IP addresses, and digital images. --> Personal data is any data that relates to an identified or identifiable natural person. An identifiable person is one who can be identified (directly or indirectly), in particular through an identifier such as a name, an identification number, location data, online identifier, or through one or more factors specific to the physical, physiological, genetic, mental, economic, cultural, or social identity of that person.|
|Pseudonymized | Pseudonymized data is personal data that has undergone processing so that it can no longer be attributed to a specific [data subject](https://review.docs.microsoft.com/en-us/workplace-analytics/privacy/data-protection-considerations?branch=pas-jt-definitions#data-subject-and-personal-data) without the use of additional information, provided that such additional information is kept separately and is subject to technical and organizational measures to ensure that the personal data is not attributed to an identified or identifiable natural person. Pseudonymization is one means of achieving de-identification. |
|Recipient|A person included in an email (includes the sender and people included in the cc and bcc lines).|
|Redundancy (organizational)|Organizational redundancy is present if at least three attendees are from different levels within the same organization. For example, a meeting whose attendees included a General Manager, a Director, and an Independent Contributor from the same organization would be a redundant meeting.|
|Redundancy (lower level)|An attendee is considered redundant at the lower level if both the attendee's manager and skip-level manager are present in the meeting.|
|Required attribute|Mandatory organizational data attributes that describe the people being analyzed. Required attributes are used in Workplace Analytics to explore, calculate, and customize metrics and filter query results. Required attributes include PersonId, EffectiveDate, ManagerId, LevelDesignation (also referred to as level), and Organization.|
|Sender|The person who sends an email.|
|Span|The number of direct reports per manager.|
|Time investor|A *measured employee* who interacts with other collaborators in meetings and with email or instant messages. Time investors allocate their time with the other participants or *collaborators* in the interaction in proportion to how many people are in the collaborator group for that interaction. People who do not have a license for Workplace Analytics can appear as collaborators, but never as time investors.|
|Time zones|Workplace Analytics uses these [time zones](../use/timezones-for-workplace-analytics.md). Personal metrics (person query results) are calculated by using the person’s time zone. Meeting metrics (meeting query results) are calculated by using the organizer’s time zone.|
|Working hours|Hours that represent the typical workweek for the company. The Workplace Analytics default setting is Monday through Friday from 8:00 AM to 5:00 PM for calculations of working hours. This default is only used for users who have not already set up their working days and hours in Outlook. Your admin can change the default working days and hours in **Admin settings** on the [System defaults](../use/settings.md#system-defaults) page.

### Related topic

[Metric descriptions for Workplace Analytics](../use/Metric-definitions.md)
