---
# Metadata Sample
# required metadata

title: Workplace Analytics Glossary
description: This  glossary defines concepts and other terms important for working with Workplace Analytics.
author: LeisaLaDell
ms.author: v-leash
ms.date: 02/20/2018
ms.topic: get-started-article
ms.prod: wpa
---

# Glossary for Workplace Analytics

The glossary defines concepts and other terms (excluding [metric definitions](../use/Metric-definitions.md)) used for working with Workplace Analytics.

|Term|Definition|
|----|----------|
|Adjusted meeting hours|An adjustment is applied so that overlapping time is not double-counted when a person has overlapping meeting hours.<br>For example: A person with non-declined meeting requests from 2:00 -3:00 PM and 2:30 - 3:30 PM would yield 1.5 adjusted meeting hour.|
|Attended|A person is counted as attended for a meeting if they either accepted or did not respond to a meeting request (also referred to as *non-declined meeting request*).|
|Attendee|A person who was invited and *attended* the meeting.|
|Attributes|A defined characteristic about the person, such as team, department, or function. *Required attributes* are the subset of attributes that are required in order to calculate metrics.|
|Calendar fragmentation|When a person does not have blocks of time sufficient to focus on completing complex tasks. This is typified by having only small blocks of time (15, 30, 60 minutes) between meetings.<br>Anything that is not *focus time* (uninterrupted time blocks of two hours or more with no meetings) is considered calendar fragmentation.|
|Collaborator|People that *measured employees* interact with by email or in meetings. Collaborators are identified as internal (within the company) or external (outside of the company).|
|Connection|Two or more *meaningful interactions*.|
|Custom attribute|*Organizational data* attributes that describe the people being analyzed. If supplied by the company, these attributes can be used in grouping of data, and to filter reports and customize metrics. However, they are not reserved for metrics calculations.|
|Focus time|Uninterrupted time blocks of two hours or more with no meetings.|
|Insularity|When collaboration happens only with people from within a person’s team, function, department, and so on.|
|Invitee|A person who is invited to a meeting via a meeting request.|
|Layer|The number of *levels* of reporting in a company, starting from CEO and going down.<br>For example: The CEO equals level 0.|
|Level|A *required attribute* that is a company-specific way of organizing employees by job experience or seniority.   |
|Meaningful interactions|An email or meeting that includes between two and five people.|
|Measured employee|A person about whom Workplace Analytics gathers Office 365 data, and about whom analysts can calculate metrics.|
|Multitasking|The concept of not staying focused on the task at hand. Defined in Workplace Analytics as a person sending two emails or more per meeting hour, and in meetings shorter than an hour, two emails or more per meeting.|
|Non-declined meeting request|In Workplace Analytics, this is synonymous with *attended*.|
|Optional attribute|Optional *organizational data* attributes that describe the people being analyzed. If supplied by the company, these attributes can be used to group in Explore metrics and filter queries and customize metrics. These are reserved for future metric calculations. The optional attributes are FunctionType, Layer, HourlyRate.|
|Organization|A *required attribute* that describes the organizational unit in which the employee resides. The exact value will be determined by the company’s structure, as well as how that structure is captured in within the company’s human resources information system.<br>For example: the organization may also be known as department, function, or could be defined by a specific manager name in the management hierarchy. |
|Organizational data|Attributes about people in the organization or people who collaborate with the organization that Workplace Analytics analyzes. Most organizational data are obtained from a company’s human resources information system.<br>Examples include: job family, job role, organization, line of business, cost center, location, region, layer, level, number of direct reports, manager, and so on. |
|Organizer|The person who organizes a meeting. This person is also counted as an *attendee*.|
|People meeting hours|The sum of adjusted meeting hours for each person in the meeting.<br>For example: If a meeting is one hour long, with three attendees (and no attendees have overlapping meetings), then the people meeting hours for that meeting is three.|
|Person|The *measured employee* for whom the metric is calculated.|
|Recipient|A person included in an email (includes the sender and people included in cc and bcc lines).|
|Redundant|A meeting is considered redundant if at least three attendees are from different *levels* within the same organization.<br>For example: A meeting whose attendees included a General Manager, a Director and an Independent Contributor from the same organization would be considered redundant.|
|Required attribute|Mandatory organizational data attributes that describe the people being analyzed. Required attributes are reserved by Workplace Analytics for calculating metrics and can be used to customize metrics, group in Explore metrics, and filter query results. The two required attributes are LevelDesignation (also referred to as level) and Organization.|
|Sender|The person who sends an email.|
|Span|The number of direct reports per manager.|
|Time zones|Workplace Analytics uses these time zones. Personal metrics (Person query results) are calculated using the person’s time zone. Meeting metrics (Meeting query results) are calculated using the organizer’s time zone.|
|Working hours|Hours representing the typical work week for the company. Workplace Analytics uses M-F from 8:00 AM – 5:00 PM for working hours calculations.|
 

### Related topic
[Metric descriptions for Workplace Analytics](../use/Metric-definitions.md)
