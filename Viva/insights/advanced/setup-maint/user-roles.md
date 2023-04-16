---
ms.date: 07/15/2022
title: Roles in Viva Insights
description: Learn which roles can access which features in Viva Insights
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Roles in Viva Insights

Certain roles need the correct level of access to specific product areas to perform their required tasks. The roles are distinct in their assigned responsibilities and access permissions.

Each role only gives access to actions, pages, reports, and data that correspond with that role. Roles are assigned independently, are non-cumulative, and don't roll up.

## Inherited roles

Users with the **Global Admin** role in Azure Active Directory automatically inherit Insights Administrator privileges.

## Role descriptions and access levels

### Feature access

The following matrix shows which roles can access which features.

| Feature |  Page  | Description | Insights Administrator | Insights Analyst | Insights Business Leader | People Manager<sup>1</sup>|
|---|-----|---|---|---|---|---|
| Viva Insights app – organization insights|  |   |   |   |   |   | 
|   |  (throughout the app) | Depending on your role<sup>2</sup>, view group insights about your team or highlights about your company.  |   |   |  X | X |
| Viva Insights advanced insights app |  |   |   |   |   |     | 
|   |  **Analysis** | Landing page for analysts. View recent queries, Power BI templates, and build custom queries.  |   | X |   |   |
|   |  **Query results** | View query results |   | X |   |   |
|   |  **Organizational data** | Verify whether organizational data quality is high enough for analysis and upload custom organizational data files | X | X<sup>3</sup>|   |   |
|   |  **Privacy settings** | Manage privacy settings  | X |   |   |   |
|   |  **Manager settings** | Turn on/off organization insights that appear in the Viva Insights app in Teams and on the web; select eligible managers for group insights | X |   |   |   |

<sup>1. People Manager isn't technically a role that can be assigned. The Insights admin can enable them access to their Group insights through [Manager settings](./manager-settings.md) within the advanced insights app. </sup>

<sup>2. People Managers can access group insights about their team. Insights Business Leaders can access insights about their company. People assigned both roles can access insights about their team and their company. </sup>

<sup>3. Insights Analysts can't upload custom organizational data files.</sup>

### Functional tasks

The following table shows which roles can perform which tasks in Viva Insights.

| Function | Insights Administrator | Insights Analyst | Insights Business Leader | People Manager | 
|---|---|---|---|---|
| Configure privacy settings and manager settings | X | | | |
| Upload organizational data into the system | X | | | |
| Access organization insights within the Viva Insights app  | | | X | X|
| Use the full set of analyst tools | | X | | |

### Levels of responsibility

People who access data with Viva Insights should ideally have previous experience for their level of access. Preferably, they should have previously undergone security and privacy training in handling sensitive data. The following table shows access levels for each role.

| Access level | Administrator | Analyst | Insights Business Leader | People Manager |
|---|---|---|---|---|
| View personally identifiable, individual-level organizational data (including email addresses and HR fields such as level and organization) | X | | | |
| View de-identified, individual-level data: Organizational data (HR fields, such as level or organization) and Microsoft 365 data (metrics about collaboration and relationships) | | X | | |
| View aggregated and de-identified Microsoft 365 data (metrics about collaboration time and relationships) | | X | X | X (team only) |

### Suggested personas

Consider the following personas when granting the different levels of access for Viva Insights.


| Persona | Administrator | Analyst | Insights Business Leader | People Manager |
|---|---|---|---|---|
| Administrator | X | | | |
| Executive or business leader | | X | X | X|
| Analyst or data scientist | | X | | |
| Group or team manager | | | | X |

### Access to resources

In the Microsoft 365 admin center, you can assign access rights to users by [assigning roles to them](assign-user-roles.md). For general information on accessing resources, and for information on the specific methods of role assignment in Azure AD, see [Related topics](#related-topics).

## Aspects of role assignment

### How many assignees

The size of your organization and your requirements for managing organizational data determine the number of people to whom you assign specific roles for Viva Insights. The number of analysts should be as many as your organization requires to perform data analysis. Viva Insights imposes no limit on the number of role assignments.

### Multiple roles for one person

You can assign multiple roles to one person. It's up to your organization to choose who is assigned which role or roles. For example, one person can be both an **Insights Administrator** and an **Insights Analyst**. However, it's a best practice to assign the admin and analyst roles to different people to prevent any misuse of or external linking of organizational data with collaboration metrics.

In the Azure portal, you can assign multiple roles to one account, but you can assign only one role at a time. In the Azure portal, add the first role, choose **Select**, return to the user list, and then select the same account again to choose the next role for that account. 

## Related topics

* [Assign user or group roles](../setup-maint/assign-user-roles.md)
* [What is Azure Active Directory](/azure/active-directory/fundamentals/active-directory-whatis)
* [Managing access to resources with Azure Active Directory groups](/azure/active-directory/fundamentals/active-directory-manage-groups)

