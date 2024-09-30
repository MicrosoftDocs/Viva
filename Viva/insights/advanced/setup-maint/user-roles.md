---
ms.date: 09/30/2024
title: Roles in Viva Insights
description: Learn which roles can access which features in Viva Insights
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva-insights
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Roles in Viva Insights

Certain roles need the correct level of access to specific product areas to perform tasks. The roles are distinct in their assigned responsibilities and access permissions.

Each role only gives access to actions, pages, reports, and data that correspond with that role. Roles are assigned independently, are non-cumulative, and don't roll up.

>[!Important]
>Early next year, the **Business Leader** role will no longer be available. At that point, people who previously had this role won’t be able to access organizational insights. Employees with delegate access, however, will be able to view organizational insights. [Learn more about how delegate access works](..//..//org-team-insights/delegate-access.md). 

## Inherited roles

Users with the **Microsoft 365 Global Administrator** role in Microsoft Entra ID automatically inherit Insights Administrator privileges.

## Role descriptions and access levels

### Feature access

The following matrix shows which roles can access which features.

| Feature |  Page  | Description | Insights Administrator | Insights Analyst | Insights Business Leader | Manager<sup>1</sup>|
|---|-----|---|---|---|---|---|
| Viva Insights app – organization insights|  |   |   |   |   |   | 
|   |  (throughout the app) | Depending on your role<sup>2</sup>, view group insights about your team or highlights about your company.  |   |   |  X | X |
| Viva Insights advanced insights app |  |   |   |   |   |     | 
|   |  **Analysis** | Landing page for analysts. View recent queries, Power BI templates, and build custom queries.  |   | X |   |   |
|   |  **Query results** | View query results |   | X |   |   |
|   |  **Organizational data** | Verify whether organizational data quality is high enough for analysis and upload custom organizational data files | X | X<sup>3</sup>|   |   |
|   |  **Privacy settings** | Manage privacy settings  | X |   |   |   |
|   |  **Partitions** | Create and manage partitions  | X |   |   |   |
|   |  **Manager settings** | Turn on/off organization insights that appear in the Viva Insights app in Teams and on the web; select eligible managers for group insights | X |   |   |   |

1. Manager isn't technically a role that can be assigned. The Insights Administrator can enable managers access to their organization insights through [Manager settings](./manager-settings.md) within the advanced insights app. 

2. Managers can access aggregated insights about their team. Insights Business Leaders can access insights about their company. People assigned both roles can access insights about their team and their company.

3. Insights Analysts can't upload custom organizational data files.

### Tasks

The following table shows which roles can perform which tasks in Viva Insights.

| Function | Insights Administrator | Insights Analyst | Insights Business Leader | Manager | 
|---|---|---|---|---|
| Configure privacy settings, partitions, and manager settings | X | | | |
| Upload organizational data into the system | X | | | |
| Access organization insights within the Viva Insights app  | | | X | X|
| Use the full set of analyst tools | | X | | |

### Levels of responsibility

People who access data with Viva Insights should ideally have previous experience for their level of access. Preferably, they should have undergone security and privacy training in handling sensitive data. The following table shows access levels for each role.

| Access level | Insights Administrator | Insights Analyst | Insights Business Leader | Manager |
|---|---|---|---|---|
| View personally identifiable, individual-level organizational data (including email addresses and HR fields such as level and organization) | X | | | |
| View de-identified, individual-level data: Organizational data (HR fields, such as level or organization) and Microsoft 365 data (metrics about collaboration and relationships) | | X | | |
| View aggregated and de-identified Microsoft 365 data (metrics about collaboration time and relationships) | | X | X | X (team only) |

### Suggested personas

Consider the following personas when granting the different levels of access for Viva Insights.


| Persona | Insights Administrator | Insights Analyst | Insights Business Leader | Manager |
|---|---|---|---|---|
| Administrator | X | | | |
| Executive or business leader | | X | X | X|
| Analyst or data scientist | | X | | |
| Group or team manager | | | | X |

### How to assign roles and enable feature access

So users can access Viva Insights features, [assign them roles](assign-user-roles.md) in the Microsoft 365 admin center.
