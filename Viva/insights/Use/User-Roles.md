---

title: User roles for advanced insights
description: Which user roles perform which functions and have access to which parts of Microsoft Viva Insights
author: madehmer
ms.author: v-pausch
ms.topic: article
ms.localizationpriority: medium 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Advanced insights user roles

People who want to use advanced insights and other analysis tools in Microsoft Viva Insights require the correct level of access. The roles are distinct in their assigned responsibilities and access permissions.

Each role only gives access to actions, pages, dashboards, and data that correspond with that role. Roles are assigned independently, are non-cumulative, and do not roll up.

## Role descriptions and access levels

[!INCLUDE [Roles](../includes/wpa-roles.md)]

## User access

The following shows who can access what with Viva Insights.

| Page        | Description | Administrator | Analyst | Analyst (Limited Access) | Program Manager | People Manager |
| ------------- | ---------------- | ------------- | ------- | ------------------------ | --------------- | -------------- |
| **Home**      | View highlights from the latest data; see the latest notifications | &nbsp;    | <img src="../Images/WpA/check-mark.png" alt="checkmark">    | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> |<img src="../Images/WpA/check-mark.png" alt="checkmark"> (team only) |
| **Analyze**   | &nbsp;                                                             | &nbsp;    | &nbsp;                                                      | &nbsp;   | &nbsp;  | &nbsp; |
| &nbsp;        | **Peer analysis** collaboration data                               | &nbsp;    | <img src="../Images/WpA/check-mark.png" alt="checkmark">    | &nbsp;   | &nbsp;  | &nbsp; |
| &nbsp;        | Analysis with the **Query designer**                             | &nbsp;    | <img src="../Images/WpA/check-mark.png" alt="checkmark">    | &nbsp;   | &nbsp;  | &nbsp; |
| **Explore the stats** | Chart data based on insight recommendations                | &nbsp;    | <img src="../Images/WpA/check-mark.png" alt="checkmark">    | <img src="../Images/WpA/check-mark.png" alt="checkmark"> |<img src="../Images/WpA/check-mark.png" alt="checkmark"> | &nbsp; |
| **Plans**     | Create plans that help participants improve workplace behaviors    | &nbsp;    | <img src="../Images/WpA/check-mark.png" alt="checkmark">    | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> |<img src="../Images/WpA/check-mark.png" alt="checkmark"> (team only) |
| **Settings**  | &nbsp;                                                             | &nbsp;    | &nbsp;                                                      | &nbsp;   | &nbsp;  | &nbsp; |
| &nbsp;        | **Sources** help to verify that the Microsoft 365 data and organizational data have been loaded properly and are available for analysis | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | &nbsp;  | &nbsp; |
| &nbsp;        | **Upload** for importing an organizational (HR) data file into Viva Insights | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | &nbsp;  |  &nbsp; |&nbsp; | &nbsp;  | &nbsp; |
| &nbsp;        | **Analysis settings** to set meeting exclusion rules for analysis  | &nbsp;    | <img src="../Images/WpA/check-mark.png" alt="checkmark">     | <img src="../Images/WpA/check-mark.png" alt="checkmark"> *(read-only access)*| &nbsp; | &nbsp; |
| &nbsp;        | **Admin settings** for system defaults, privacy settings, and manager settings | <img src="../Images/WpA/check-mark.png" alt="checkmark">     | &nbsp;  | &nbsp;  | &nbsp;  |  &nbsp; |

## Functions performed

The following shows who can do what with Viva Insights.

|  Function |  Administrator |  Analyst |  Analyst (Limited Access) | Program Manager |People Manager |
| ---- | ---- | ---- | ---- | ---- | ---- |----| ---- |
| Configure system defaults, privacy settings, and manager settings | <img src="../Images/WpA/check-mark.png" alt="checkmark">|&nbsp; |&nbsp; |&nbsp; |
| Upload organizational data into the system | <img src="../Images/WpA/check-mark.png" alt="checkmark"> |&nbsp; |&nbsp; |&nbsp; |
| Use the full set of analyst tools in Sources and Analyze |&nbsp; | <img src="../Images/WpA/check-mark.png" alt="checkmark"> |&nbsp; |&nbsp; |
| Help coordinate, set up, and manage change plans |&nbsp; | <img src="../Images/WpA/check-mark.png" alt="checkmark">  | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> (team only) |

### Levels of responsibility

People with access to Viva Insights should ideally have previous experience for their level of access. Preferably, they should have previously undergone security and privacy training in handling sensitive data.

| Access level | Administrator | Analyst | Analyst (Limited Access) | Program Manager | People Manager |
| ------------ | ------------- | ------- | ------------------------ | --------------- | -------------- |
| View personally identifiable, individual-level organizational data (including email addresses and HR fields such as level and organization)| <img src="../Images/WpA/check-mark.png" alt="checkmark"> |&nbsp; |&nbsp; |&nbsp; |
| View de-identified, individual-level data:<ul><li>Organization data (HR fields, such as level or organization)</li><li>Microsoft 365 data (metrics about collaboration and relationships)</li></ul> |&nbsp; | <img src="../Images/WpA/check-mark.png" alt="checkmark"> |&nbsp; |&nbsp; |
| View aggregated and de-identified Microsoft 365 data (metrics about collaboration time and relationships) |&nbsp; | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> |&nbsp; |
| Create custom plans to be deployed to groups and can influence the pages that users see in personal insights through Viva Insights |&nbsp; | <img src="../Images/WpA/check-mark.png" alt="checkmark">  | <img src="../Images/WpA/check-mark.png" alt="checkmark">| <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> *(team only)*|

## Suggested personas

Consider the following personas when granting the different levels of access to Viva Insights.

| Persona | Administrator | Analyst | Analyst (Limited Access) | Program Manager | People Manager |
| ------- | ------------- | ------- | ------------------------ | --------------- | -------------- |
| Executive or business leader |&nbsp; |&nbsp; | <img src="../Images/WpA/check-mark.png" alt="checkmark"> |&nbsp;   |&nbsp; |
| Program manager | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> |&nbsp; |
| Analyst or Data scientist |&nbsp;   | <img src="../Images/WpA/check-mark.png" alt="checkmark"> |&nbsp; |&nbsp; |&nbsp; |
| Group or team manager |&nbsp; |&nbsp; |&nbsp; |&nbsp; | <img src="../Images/WpA/check-mark.png" alt="checkmark"> |

## Aspects of role assignment

### How many assignees?

The size of your organization and your requirements for managing organizational data determine the number of people to whom you assign the roles of Viva Insights admins and analysts. The number of analysts should be as many as your organization requires to perform data analysis. Viva Insights imposes no limit on the number of role assignments.

### Multiple roles for one person

You can assign multiple Viva Insights roles to one person. It's up to your organization to choose who is assigned which role or roles. Examples:

* One person can be both a Microsoft 365 admin and a Viva Insights admin.
* One person can be both a Viva Insights admin and a Viva Insights analyst. It is best practice, however, to assign the admin and analyst roles to different people to prevent any misuse of or external linking to organizational data with collaboration metrics.

In the Azure Portal, you can assign multiple roles to one account but you can assign only one role at a time. In the Azure portal, add the first role, click **Select**, return to the user list, and then select the same account again to choose the next role for that account. (Note that role assignment in Viva Insights is performed in the Azure Portal and not in the Microsoft 365 dashboard.)

### Limiting analyst access

The analyst (limited access) role is for an analyst who needs access only to advanced insights and analysis shown in [Explore the stats](explore-intro.md).

## Related topics

* [Manager settings](../use/manager-settings.md)
* [Assign roles in Azure AD](../setup/assign-user-roles.md)
* [Managing access to resources with Azure AD groups](/azure/active-directory/fundamentals/active-directory-manage-groups)
