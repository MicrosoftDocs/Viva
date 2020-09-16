---

title: User roles in Workplace Analytics
description: Which user roles in Workplace Analytics perform which functions and have access to which pages in Workplace Analytics
author: madehmer
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# User roles in Workplace Analytics

Users of Workplace Analytics require the proper level of access to areas of the product to be able to perform their required tasks. This topic describes the roles and responsibilities of users and the levels of access that each role requires.

> [!Note]
> The administrator of Office 365 or Azure Active Directory grants the levels of access that are described in this topic.  

## Role descriptions and access levels

These are the Workplace Analytics roles and their level of access:

[!INCLUDE [Roles](../includes/wpa-roles.md)]

>[!Note]
>User roles are each distinct in their assigned responsibilities and access permissions. Each user role only gives access to actions, pages, dashboards, and data that correspond with that role. Roles are assigned independently, are non-cumulative, and do not roll up.

## User access

The following shows who can access what in Workplace Analytics.

|  Page  | Page description |  Administrator | Analyst |  Analyst (Limited Access) | Program manager | People manager |
| ---- | ---- | ---- | ---- | ---- | ---- |----| ---- |
| **Home** | View highlights from the latest data; see the latest notifications | | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> |<img src="../Images/WpA/check-mark.png" alt="checkmark"> (team only)|
| **Analyze** |
| | **Explore:** View a series of dashboards that provide insights into the way your organization collaborates | | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> |<img src="../Images/WpA/check-mark.png" alt="checkmark"> |
| | **Queries:** Perform deeper exploration of the data through custom querying tools | | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | | | |
| **Plans** | Create programs to help participants improve workplace behaviors. | | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> |<img src="../Images/WpA/check-mark.png" alt="checkmark"> (team only) |
| **Settings** |
| | **Sources:** Help to verify that the Office 365 data and organizational data have been loaded properly and are available for analysis | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | | | |
| | **Upload:** Upload an organizational data file to Workplace Analytics | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | | | | |
| | **Analysis settings:** Exclude meetings from analysis that would otherwise skew your results. The _Analyst (Limited access)_ role has read-only access to this page.| | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | | | |
| | **Admin settings:** Configure system defaults, privacy settings, and manager settings | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | | | | |

### Functions performed

The following shows who can do what in Workplace Analytics.

|  Function |  Administrator |  Analyst |  Analyst (Limited Access) | Program manager |People manager |
| ---- | ---- | ---- | ---- | ---- | ---- |----| ---- |
| Configure system defaults, privacy settings, and manager settings | <img src="../Images/WpA/check-mark.png" alt="checkmark">| | | |
| Upload organizational data into the system | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | | | |
| Use the full set of analyst tools on the Sources and Analyze (Explore and Queries) pages to perform analysis | | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | | |
| Serve as HR data provider and Workplace Analytics tool owner | | | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | |
| Help coordinate, setup, and manage change plans | | | | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> (team only) |

### Levels of responsibility

People with access to Workplace Analytics should ideally have previous experience for their level of access. Preferably, they should have previously undergone security and privacy training in handling sensitive data.

| Access level | Administrator |  Analyst | Analyst (Limited Access) | Program manager | People manager |
| ---- | ---- | ---- | ---- | ---- | ---- |-------| ---- |
| Ability to view personally-identifiable, individual-level organizational data (including email addresses and HR fields such as level and organization)| <img src="../Images/WpA/check-mark.png" alt="checkmark"> | | | |
| Ability to view de-identified, individual-level data:<ol><li>Organization data (HR fields such as level or organization)</li><li>Office 365 data (metrics about collaboration time and relationships)</li></ol> | | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | | |
| Ability to view aggregated and de-identified Office 365 data (metrics about collaboration time and relationships) | | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | |
| Can create custom plans to be deployed to groups and can influence the pages that users see in MyAnalytics | | | | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> (team only)|

### Suggested personas

Consider the following personas when granting the different levels of access to Workplace Analytics.

| Persona | Administrator | Analyst | Analyst (Limited Access) | Program manager |People manager |
| ------ | ----------- | ------- | ------- | ------ | ------ |
| Executive/business leader | | | <img src="../Images/WpA/check-mark.png" alt="checkmark"> |   | |
| Program manager | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | <img src="../Images/WpA/check-mark.png" alt="checkmark"> |
| Analyst/data scientist |   | <img src="../Images/WpA/check-mark.png" alt="checkmark"> | | |
|  HR data provider / Workplace Analytics tool owner |    <img src="../Images/WpA/check-mark.png" alt="checkmark"> | | | |
| Group or team manager | | | | | <img src="../Images/WpA/check-mark.png" alt="checkmark"> |

### Access to resources

In Azure Active Directory, you can assign access rights to users by assigning roles to them. For general information on accessing resources, and for information on the specific methods of role assignment in Azure AD, see **Related topics**.

## Aspects of role assignment

### How many assignees?

The size of your organization and your requirements for managing organizational data determine the number of people to whom you assign the roles of Workplace Analytics admins and analysts. The number of analysts should be as many as your organization requires to perform data analysis. Workplace Analytics imposes no limit on the number of role assignments.

### Multiple roles for one person

You can assign multiple Workplace Analytics roles to one person. It's up to your organization to choose who is assigned which role or roles. Examples:

* One person can be both an Office 365 admin and a Workplace Analytics admin.
* One person can be both a Workplace Analytics admin and a Workplace Analytics analyst. It is best practice, however, to assign the admin and analyst roles to different people to prevent any misuse of or external linking to organizational data with collaboration metrics.

In the Azure Portal, you can assign multiple roles to one account but you can assign only one role at a time. In the Azure portal, add the first role, click **Select**, return to the user list, and then select the same account again to choose the next role for that account. (Note that role assignment in Workplace Analytics is performed in the Azure Portal and not in the Office 365 dashboard.)

### Limiting analyst access

The analyst (limited access) role is for an analyst who needs access only to the insights that are displayed in the Workplace Analytics [Explore](explore-intro.md) dashboards.

## Related topics

* [Manager settings](../use/settings.md#manager-settings)
* [Assign user or group roles in Azure Active Directory](../setup/assign-user-roles.md)
* [What is Azure Active Directory?](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis)
* [Managing access to resources with Azure Active Directory groups](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-manage-groups)

