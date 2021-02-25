---

ROBOTS: NOINDEX,NOFOLLOW
title: Insights glossary
description: Describes common terms and concepts used in Workplace Analytics insights
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: none 
ms.prod: wpa

---
# Glossary for Workplace Analytics insights

*This experience is only available through private preview at this time.*

The following are terms and concepts used in Workplace Analytics insights. This glossary excludes [business outcome definitions](intro.md#business-outcomes).

|Term|Definition|
|----|----------|
| Adjusted meeting hours |An adjustment is applied so that overlapping time is not double-counted when a person has overlapping meeting hours. For example, a person with non-declined meeting requests from 2:00 to 3:00 PM and 2:30 to 3:30 PM would yield 1.5 adjusted meeting hours.|
| Aggregation | Aggregation means compiling data from multiple individuals or sources. The more individuals or sources whose data is used, the more difficult it is to identify personal data. Aggregation is one means of achieving de-identification. |
| Anonymization | Anonymized data is information that does not relate to a specific individual, that does not increase the likelihood that a specific individual can be identified, or that has been rendered in a way so that it cannot be used to identify a specific individual. |
| Attended| A person attended a meeting if they did not decline the meeting request. This means that they either accepted the meeting request, accepted it as _tentative_, or did not respond to it. (This meeting request itself is subsequently referred to as a *non-declined meeting request*.) |
| Attendee|A person who was invited and *attended* the meeting.|
| Attributes|A defined characteristic about the person, such as team, department, or function. *Required attributes* are the subset of attributes that are required in order to calculate metrics.|
|Calendar fragmentation|When a person does not have blocks of time sufficient to focus on completing complex tasks. This is typical of those with only small blocks of time (15, 30, or 60 minutes) between meetings. Anything that is not *focus time* (uninterrupted time blocks of two hours or more with no meetings) is considered calendar fragmentation.|
| <a name="call-define"></a> Call | A scheduled or unscheduled audio or video communication between two or more people over Microsoft Teams. If the call is scheduled, it appears on a person's Outlook calendar as a meeting appointment. A user's call duration is based on their join time and their leave time for the call. |
|Collaborators| Anyone that *measured employees* or *time investors* interact with by email or instant message, in meetings, in unscheduled calls, or with instant messages. Collaborators are identified as internal (within the company) or external (outside of the company) and discovered through the data extracted for measured employees. Internal collaborators have domains internal to your organization, while external collaborators have domains external to your organization. |
|Collaborator group|A group of collaborators that are identified as internal (within the company) or external (outside of the company) that interacts by email, in meetings, in calls, or with instant messages  with a specified *time investor*.|
| <a name="conflicting-meeting-define"></a> Conflicting meeting | A meeting on a person's calendar that overlaps with another meeting on that person's calendar.  |
|Connected people |Those who have had more than five connections with external people within the same month. |
|Connected groups |Those who spend a large proportion of their overall collaboration with people outside the company. |
|Connection|Two or more [meaningful interactions](#meaningful-interaction-define).|
|Custom attribute|*Organizational data* attributes that describe the people being analyzed. If supplied by the company, these attributes can be used in grouping of data, and to filter reports and customize metrics. However, they are not reserved for metrics calculations.|
|De-identification | A process that is used to prevent the connection of personal identifiers with information. De-identification is achieved through the removal of personal data, which is sometimes replaced with a pseudonymous identifier. |
| <a name="decision-making-meeting-define"></a> Decision-making meeting | A meeting that has between two and eight attendees and lasts less than one hour. |
|Focus time| Uninterrupted time blocks of two hours or more with no meetings.|
|Fragmented hours |A person's time after you subtract their meeting hours and their focus hours. |
|Influence score |The calculations for influence scores use the relative collaboration time between individuals as the strengths of the connections for a person's influence measure, which is how well connected that person is in the company, division, or other group. |
|<a name="influencer-define"></a> Influencers |Beyond an organization’s formal hierarchy, individuals can exert influence within informal networks and between them. Influencers are the best-connected people in the company, who have large personal networks or above-average numbers of relationships with colleagues, which is determined based on their collaboration data.|
|Insularity|When collaboration happens only with people from within a person’s team, function, department, and so on.|
|Invitee|A person who is invited to a meeting with a meeting request.|
| <a name="large-meeting-define"></a> Large meeting |A large meeting  involves more than eight people and lasts less than one hour. Also see [Long and large meeting](#long-and-large-meeting-define).|
|Layer|The number of *levels* of reporting in a company, starting from CEO and going down. For example, the CEO equals level 0.|
|Level|A *required attribute* that is a company-specific way of organizing employees by job experience or seniority. |
| <a name="long-meeting-define"></a> Long meeting | A long meeting is scheduled for more than one hour and has more than one but fewer than nine attendees. |
| <a name="long-and-large-meeting-define"></a> Long and large meeting |A long and large meeting has more than eight attendees and is scheduled for longer than one hour. |
| <a name="meaningful-interaction-define"></a>Meaningful interaction | A meaningful interaction is defined as one of the following types of collaboration: <li>an email</li><li>a meeting</li><li>a call</li><li>three instant messages. These messages could be sent by any of the collaborators in the chat. For example, they could be: (a) three messages sent by one individual to others in Teams, or (b) three distinct messages from distinct senders within the same Teams chat.<p><p>Moreover, every meaningful interaction must have at least two collaborators but at most eight collaborators participating in the interaction.  |
| <a name="measured-employees"></a> Measured employees | The employees to whom your Workplace Analytics administrator assigned licenses during setup. After license assignment, Workplace Analytics extracts Microsoft 365 data about meetings, email, unscheduled calls, and instant messages for these people. If you are an analyst or limited analyst, this is the population that you can analyze within Workplace Analytics. The number of measured employees can help determine whether you have good data coverage for analysis.|
| <a name="meeting-define"></a> Meeting | An audio or video communication or in-person meeting that has been scheduled -- that is, it appears on a person's Outlook calendar. A meeting must involve two or more people. Outlook calendar events determine the durations of meetings. |
|Multitasking |The concept of not staying focused on the task at hand. Defined in Workplace Analytics as a person sending two emails or more per meeting hour, and in meetings shorter than an hour, two emails or more per meeting.|
|Non-declined meeting request |In Workplace Analytics, this is synonymous with *attended*.|
|Optional attribute |Optional *organizational data* attributes that describe the people being analyzed. If supplied by the company, the insights use these attributes in calculations. Optional attributes include FunctionType, HireDate, HourlyRate, Layer, and TimeZone.|
|Organization |A *required attribute* that describes the organizational unit in which the employee resides. The exact value will be determined by the company’s structure, as well as how that structure is captured in within the company’s human resources information system. For example, the organization might also be known as department, function, or defined by a specific manager name in the management hierarchy. |
|Organizational data |Attributes about people in the organization or people who collaborate with the organization that Workplace Analytics can analyze. Most organizational data is obtained from a company’s human resources information system. For example, job family, job role, organization, line of business, cost center, location, region, layer, level, number of direct reports, manager, and so on. |
|<a name="ona-define"></a> Organizational network analysis (ONA) |Studies communication and uses social network theory and dynamic network analysis to create statistical and graphical models of people, tasks, groups, knowledge, and resources within an organization. Beyond an organization’s formal hierarchy, informal networks exist where individuals can exert influence within and between these networks. The most influential people are the ones who have large personal networks or above-average numbers of relationships with co-workers. Network size is just one attribute of a collaborative network. Network connections have other qualities that show the type of working relationship and what benefit it might present to the employee and team. |
|Organizer |The person who organizes a meeting. This person is also counted as an *attendee*.|
|People meeting hours |The sum of adjusted meeting hours for each person in the meeting. For example, if a meeting lasts at least one hour with three attendees (and no attendees have overlapping meetings), the people meeting hours for that meeting is three.|
|Person |The *measured employee* for whom the metric is calculated.|
|Personal data | Personal data is any data that relates to an identified or identifiable natural person. An identifiable person is one who can be identified (directly or indirectly), in particular through an identifier such as a name, an identification number, location data, online identifier, or through one or more factors specific to the physical, physiological, genetic, mental, economic, cultural, or social identity of that person.|
|Pseudonymized | Pseudonymized data is personal data that has undergone processing so that it can no longer be attributed to a specific data subject without the use of additional information, provided that such additional information is kept separately and is subject to technical and organizational measures to ensure that the personal data is not attributed to an identified or identifiable natural person. Pseudonymization is one means of achieving de-identification. |
|Recipient |A person receiving an email (includes people in the to, cc, and bcc lines).|
|Redundancy (organizational) |Organizational redundancy is present if at least three attendees are from different levels within the same organization. For example, a meeting whose attendees included a General Manager, a Director, and an Independent Contributor from the same organization would be a redundant meeting.|
|Redundancy (lower level) |An attendee is considered redundant at the lower level if both the attendee's manager and skip-level manager are present in the meeting.|
|Required attribute |Mandatory organizational data attributes that describe the people being analyzed in the insights. Required attributes include PersonId, EffectiveDate, ManagerId, LevelDesignation (also referred to as level), and Organization.|
|Sender |The person who sends an email.|
|Span |The number of direct reports per manager.|
|Time investor |A *measured employee* who interacts with other collaborators in meetings and with email or instant messages. Time investors allocate their time with the other participants or *collaborators* in the interaction in proportion to how many people are in the collaborator group for that interaction. People who do not have a license for Workplace Analytics can appear as collaborators, but never as time investors.|
|Time zones |Personal metrics are calculated by using the person’s time zone. Meeting metrics are calculated by using the organizer’s time zone.|
|Working hours |Hours that represent the typical workweek for the company. The Workplace Analytics default setting is Monday through Friday from 8:00 AM to 5:00 PM for calculations of working hours. This default is only used for users who have not already set up their working days and hours in Outlook.|
