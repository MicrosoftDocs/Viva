---
# Metadata Sample
# required metadata

title: User roles in Workplace Analytics
description: User roles in Workplace Analytics -- which roles perform which functions and have access to each page of Workplace Analytics
author: paul9955
ms.author: rodonahu
ms.date: 05/02/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# User roles in Workplace Analytics 

Users of Workplace Analytics require the proper level of access to areas of the product to be able to perform their required tasks. This topic describes the roles and responsibilities of users and the levels of access that each role requires.

> [!Note] 
> The administrator of Office 365 or Azure Active Directory grants the levels of access that are described in this topic.  

## Role descriptions and access levels

These are the Workplace Analytics roles and their level of access:

 * **Analyst:** Has full access to all service features, except Administration. This role is used for the analyst who requires the most complete access to data.

 * **Analyst (Limited Access):** Has access to the Home page and to the explore-metrics features. This role is used for the analyst who only needs access to insights generated from our curated set of Explore-the-metrics dashboards.

 * **Administrator:** Has access to the Settings and Data sources features. The responsibilities of the Workplace Analytics administrator are to configure privacy settings and system defaults, and to prepare and upload organizational data to Workplace Analytics and verify it.

 * **Program manager:** Has access to the Home and Explore pages, the Solutions page and its Manage page, where the Program Manager can set up programs. On the Manage page, the Program Manager also has access to its Track page, to track the progress of active or ended programs.

>[!Note]
>User roles are each distinct in their assigned responsibilities and access permissions. Each user role only gives access to actions, pages, dashboards, and data that correspond to that role. Roles are assigned independently, are non-cumulative, and do not roll up.


## Details by user role

The following tables provide more details about Workplace Analytics user roles:

### Access to pages in Workplace Analytics

Each role has access to specific pages of Workplace Analytics as described here:

|  Page  | Page description |  Administrator | Analyst |  Analyst (Limited Access) | Program manager |
| ---- | ---- | ---- | ---- | ---- | ---- |
| **Home** | View highlights from the latest data; optionally explore metrics of team behavior | | <img src="../Images/WpA/check-mark.png"> | <img src="../Images/WpA/check-mark.png"> | <img src="../Images/WpA/check-mark.png"> |
| **Analyze** | 
| | **Explore:** View a series of dashboards that provide insights into the way your organization collaborates | | <img src="../Images/WpA/check-mark.png"> | <img src="../Images/WpA/check-mark.png"> |<img src="../Images/WpA/check-mark.png"> |
| | **Queries:** Perform deeper exploration of the data through custom querying tools | | <img src="../Images/WpA/check-mark.png"> | | |
| **Sources** | Help to verify that the Office 365 data and organizational data have been loaded properly and are available for analysis | <img src="../Images/WpA/check-mark.png"> | <img src="../Images/WpA/check-mark.png"> | | |
| **Queries** | Perform deeper exploration of the data through custom querying tools | | <img src="../Images/WpA/check-mark.png"> | | |
| **Solutions** | Create programs to help participants improve workplace behaviors. | | <img src="../Images/WpA/check-mark.png"> | |  <img src="../Images/WpA/check-mark.png"> |
| **Settings** | Make settings such as: <ol><li>System defaults</li><li>Privacy settings</li><li>Upload organizational data</li></ol> | <img src="../Images/WpA/check-mark.png"> | | | |

### Functions performed

People in these roles perform the following functions in Workplace Analytics:

|  Function |  Administrator |  Analyst |  Analyst (Limited Access) | Program manager |
| ---- | ---- | ---- | ---- | ---- | ---- |
| Configure privacy and system default settings | <img src="../Images/WpA/check-mark.png">| | | |
| Upload organizational data into the system | <img src="../Images/WpA/check-mark.png"> | | | |
| Use the full set of analyst tools on the Sources and Analyze (Explore and Queries) pages to perform analysis | | <img src="../Images/WpA/check-mark.png"> | | |
| Serve as HR data provider and Workplace Analytics tool owner | | | <img src="../Images/WpA/check-mark.png"> | |
| Help coordinate, setup, and manage change programs | | | | <img src="../Images/WpA/check-mark.png"> |

### Levels of responsibility

People who are assigned to any Workplace Analytics user roles should ideally have previous experience in similar roles. Preferably, they should have previously undergone security and privacy training in handling sensitive data.

| Access level | Administrator |  Analyst | Analyst (Limited Access) | Program manager |
| ---- | ---- | ---- | ---- | ---- | ---- |
| Ability to view personally-identifiable, individual-level organizational data (including email addresses and HR fields such as level and organization)| <img src="../Images/WpA/check-mark.png"> | | | |
| Ability to view de-identified, individual-level data:<ol><li>Organization data (HR fields such as level or organization)</li><li>Office 365 data (metrics about collaboration time and relationships)</li></ol> | | <img src="../Images/WpA/check-mark.png"> | | |
| Ability to view aggregated and de-identified Office 365 data (metrics about collaboration time and relationships) | | <img src="../Images/WpA/check-mark.png"> | <img src="../Images/WpA/check-mark.png"> | |
| Can create custom programs to be deployed to groups and can influence the pages that users see in MyAnalytics | | | | <img src="../Images/WpA/check-mark.png"> | 

### Suggested personas

Consider the following personas for each of the Workplace Analytics user roles:

|  Persona |  Administrator |  Analyst |  Analyst (Limited Access) | Program manager |
| ---- | ---- | ---- | ---- | ---- | ---- |
| Executive/business leader | | | <img src="../Images/WpA/check-mark.png"> |   |
| Program manager | <img src="../Images/WpA/check-mark.png"> | <img src="../Images/WpA/check-mark.png"> | <img src="../Images/WpA/check-mark.png"> | <img src="../Images/WpA/check-mark.png"> |
| Analyst/data scientist |   | <img src="../Images/WpA/check-mark.png"> | | |
|  HR data provider / Workplace Analytics tool owner |    <img src="../Images/WpA/check-mark.png"> |   | | |


### Access to resources

In Azure Active Directory, you can assign access rights to users by assigning roles to them. For general information on accessing resources, and for information on the specific methods of role assignment in Azure AD, see **Related topics**.

## Related topics

[What is Azure Active Directory?](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis)

[Managing access to resources with Azure Active Directory groups](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-manage-groups)