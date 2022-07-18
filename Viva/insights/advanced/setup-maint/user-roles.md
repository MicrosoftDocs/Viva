---
ROBOTS: NOINDEX,FOLLOW
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

## Role descriptions and access levels

### Feature access

The following matrix shows which roles can access which features.

| Feature |  |   | Description | Insights Administrator | Insights Analyst | Insights Business Leader | People Manager<sup>1</sup>|
|---|---|---|---|---|---|---|---|
| Viva Insights app in Teams |  |   |   |   |   |   |   |
|   |  | **My team**<sup>2</sup> | View Group insights about your   team in **My team**  |   |   |   | X |
|   |  | **My organization**    | View highlights about your   organization in **My organization**  |   |   | X |   |
| Viva Insights advanced insights app |  |   |   |   |   |     |   |
|   |  | **Analysis** | Landing page for analysts. View recent queries, Power BI templates, and build custom queries.  |   | X |   |   |
|   |  | **Query results** | View query results |   | X |   |   |
|   |  | **Organizational data** | Verify whether organizational data quality is high enough for analysis and upload custom organizational data files | X | X<sup>3</sup>|   |   |
|   |  | **Privacy settings** | Manage privacy settings  | X |   |   |   |
|   |  | **Manager settings** | Turn on/off group insights; select eligible managers for group insights | X |   |   |   |

<sup>1. People manager isn't technically a role that can be assigned. The Insights admin can enable them access to their Group insights through [Manager settings](./manager-settings.md) within the advanced insights app. </sup>

<sup> 2. My team and its features are available to managers or team leads who have a Microsoft Viva Insights license with an applicable [service plan](/viva/insights/personal/overview/plans-environments). Ask your admin about licensing and to install and set up the Viva Insights app in Teams for the organization. See [Admin tasks](/viva/insights/personal/teams/viva-teams-app-admin-tasks) for details. </sup>

<sup>3. Insights Analysts can't upload custom organizational data files.</sup>

### Functional tasks

The following table shows which roles can perform which tasks in Viva Insights.

| Function | Insights Administrator | Insights Analyst | Insights Business Leader | People Manager | |
|---|---|---|---|---|---|
| Configure privacy settings and manager settings | X | | | | |
| Upload organizational data into the system | X | | | | |
| Use the **My organization** page within the Viva Insights app in Teams | | | X | | |
| Use the full set of analyst tools | | X | | | |
| Use **Group insights** on the **My team** page within the Viva Insights app in Teams | | | | X | |

### Levels of responsibility

People who access data with Viva Insights should ideally have previous experience for their level of access. Preferably, they should have previously undergone security and privacy training in handling sensitive data. The following table shows access levels for each role.

| Access level | Administrator | Analyst | Insights Business Leader | People Manager |
|---|---|---|---|---|
| View personally identifiable, individual-level organizational data (including email addresses and HR fields such as level and organization) | X | | | |
| View de-identified, individual-level data: Organizational data (HR fields, such as level or organization) and Microsoft 365 data (metrics about collaboration and relationships) | | X | | |
| View aggregated and de-identified Microsoft 365 data (metrics about collaboration time and relationships) | | X | | X (team only) |

### Suggested personas

Consider the following personas when granting the different levels of access for Viva Insights.


| Persona | Administrator | Analyst | Insights Business Leader | People Manager |
|---|---|---|---|---|
| Administrator | X | | | |
| Executive or business leader | | X | X | |
| Analyst or data scientist | | X | | |
| Group or team manager | | | | X |

### Access to resources

In the Microsoft 365 admin center, you can assign access rights to users by assigning roles to them. For general information on accessing resources, and for information on the specific methods of role assignment in Azure AD, see [Related topics](#related-topics).

## Aspects of role assignment

### How many assignees

The size of your organization and your requirements for managing organizational data determine the number of people to whom you assign specific roles for Viva Insights. The number of analysts should be as many as your organization requires to perform data analysis. Viva Insights imposes no limit on the number of role assignments.

### Multiple roles for one person

You can assign multiple roles to one person. It's up to your organization to choose who is assigned which role or roles. For example:

* One person can be both a **Microsoft 365 admin** and an **Insights Administrator**.
* One person can be both an **Insights Administrator** and an **Insights Analyst**. However, it's a best practice to assign the admin and analyst roles to different people to prevent any misuse of or external linking of organizational data with collaboration metrics.

In the Azure Portal, you can assign multiple roles to one account, but you can assign only one role at a time. In the Azure portal, add the first role, choose **Select**, return to the user list, and then select the same account again to choose the next role for that account. Note that role assignment is performed in the Azure Portal and not in the Microsoft 365 or Office 365 dashboard.

## Related topics

* [Assign user or group roles](../setup-maint/assign-user-roles.md)
* [What is Azure Active Directory](/azure/active-directory/fundamentals/active-directory-whatis)
* [Managing access to resources with Azure Active Directory groups](/azure/active-directory/fundamentals/active-directory-manage-groups)
