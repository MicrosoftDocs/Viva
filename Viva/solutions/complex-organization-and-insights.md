---

title: Complex organization and insights
description: Learn about a complex organization and its associated Viva insights
author: v-smandalika
ms.author: v-smandalika
ms.topic: article
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: dansimp
audience: Admin
---

# What is a complex organization?

Complex organizations are Microsoft Azure Active Directory (AAD) customers who use multiple Office365 tenants. There are primarily two reasons for this type of configuration:

- [Mergers and acquisitions](#mergers-and-acquisitions)
- [Conglomerates](#conglomerates)

## Mergers and acquisitions

A business merger between two companies resulting in an organization made up with multiple Office365 tenants and separate AADs. The tenants either choose to remain separate and collaborate together or merge into a single tenant (For example, M&A: Bayer & Monsanto).

## Conglomerates

A conglomerate is a corporation made up of several independent subsidiaries. The subsidiaries are tenants that have separate AAD and will collaborate together and remain separate (For example, The Walt Disney Company, Honeywell).

## What is the purpose of this article?

Complex organizations represent challenges for deriving insights. Often, the task falls to analyzing each of the tenants that make up the complex organization independently and comparing them manually. The process can be highly manual in nature. This article provides a growing number of examples that explain how to overcome manual processes. These examples also include those that lead to output visualizations.

## Complex organizations and Viva insights

Microsoft Viva insights provide information and research-based behavioral insights into:

- the tasks an organization has to execute to get work done. For example:
    - how to enhance organizational agility
    - how to boost employee engagement
    - how to improve agility
    - how to foster innovation

Advanced analytics for organizations comprised of multiple Viva Insights tenants can be enabled by:

- combining the data in a central location, and
- combining that data with additional data sources.

A few starter use cases that would be enabled by this data combination strategy are:

- Identify collaboration patterns between two distinct business groups (tenants)
- Distinguish collaboration patterns between cross business groups (tenants) VS true external interactions.
- Data combined from Viva Insights with external sources to address headcount planning, employee well-being, permanent remote work, inclusion and diversity, and so on.

There are different methods and data storage locations possible as storage accounts, sql databases and synapse to name a few. An example leveraging Azure Data Factory, Viva Insights organizational data, and azure blob storage will be described below using the [Business Continuity](../insights/Tutorials/power-bi-bc.md) use case.

## Requirements

The following requirements to be fulfilled, prior to continuing with its analytical process using Microsoft Viva Insights:

### Organizational data

Organizational data is a key requirement for Viva Insights and further advanced analysis. It can be used to enable joins with additional data sources (as sales data), and more granular person attribute analysis, to name a couple.

General required organizational data is further described in [Viva Insights prepare organizational data](../insights/Use/organizational-data.md). For an insight into advanced analysis, the following example can be uploaded into Viva Insights.


|Attribute Name  |Attribute Description  |
|---------|---------|
|EffectiveDate     |      Date for which the given attribute value applies for the employee. The attribute applies until another record for the same attribute with a different effective date is specified.   |
|PersonId    | Unique identifier for the employee record. This identifier can be the employee's primary SMTP address or email alias. It must be in a simplified format that contains no spaces. For example,  the format **person.name@xyz.com** is allowed; however, the format **<Name, Person> (person.name@xyz.com)** is not allowed.     |
|ManagerId    |  Unique identifier for the employee’s manager, which is needed to correctly calculate metrics for time spent with managers and their direct reports.
This identifier can be the manager's primary SMTP address or email alias. It must be in a simplified format that contains no spaces. For example,  the format **person.name@xyz.com** is allowed; however, the format **<Name, Person> (person.name@xyz.com)** is not allowed.      |
|Organization    |    The internal organization that the employee belongs to. An employee’s organization will be specific to the individual needs and could be identified by the leader of the organization, or by another naming convention. This data is needed to correctly calculate metrics for redundancy and insularity.     |
|FunctionType  |    The job function that the employee performs. This job function is specific to the organization. This data is used to filter and group reports, and for grouping of data in [Explore the stats](../insights/Use/explore-intro.md) features.     |
|LevelDesignation    |      The employee’s level, which is represented as a string. This level is specific to the organization and can represent an employee’s experience or management level, or seniority within the organization. This data is needed to correctly calculate metrics for redundancy and insularity.   |
|Layer     |      The place where the employee is within the organizational hierarchy. Layer is represented as an integer and expressed as the distance the employee is from the top leader of the organization. For example, the CEO is at layer 0. This data is used to filter and group reports, and for grouping of data in [Explore the stats](../insights/Use/explore-intro.md) features.   |
|SupervisorIndicator     |    The attribute used to view the habits of people managers or influencers in the organization in Power BI visualizations. This attribute powers the Overview table, the Generated Workload charts that are generated when you use a template that requires it.
This attribute indicates the manager status of each employee as IC (individual contributor), Mngr (manager), or Mngr+ (manager of managers); however, if a different nomenclature is used in the file, you must update the Power BI chart filters accordingly. If you include SupervisorIndicator, you must also include the values **IC**, **Mngr**, or **Mngr+** in the organizational data.
     |
|TimeZone     |    Time zone in which the employee works. This attribute must be one of the time zones in [Time zones for Workplace Analytics](../insights/Use/Timezones-for-workplace-analytics.md). If no time zone is mapped to for an employee, the system will use the default time zone, which is Pacific Standard Time.     |
|TenantInd     |    Unique name for the Tenant. For example, TenantA, TenantB, TenantC, and so on.     |
|Location   |     Geographic region or other location detail.    |
|HashId    |      Unique Hashed identifier for the employee. This attribute enables further advanced analysis on the Viva insights query results.   |












