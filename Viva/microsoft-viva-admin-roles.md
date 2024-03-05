---
title: "Admin roles and tasks in Microsoft Viva"
ms.reviewer: 
ms.author: elizapo
author: lizap
manager: elizapo
ms.date: 01/08/2024
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-suite
ms.localizationpriority: medium
ms.collection:
  - M365initiative-viva
  - highpri
  - Tier1
  - essentials-manage
search.appverid:
- MET150

description: "Learn about the admin roles for Microsoft Viva"
---
# Admin roles and tasks in Microsoft Viva
Setup and management of the Microsoft Viva suite starts with the Microsoft 365 global admin. The Microsoft 365 global admin can then assign additional roles for the management, tasks, and maintenance of each Viva app.

Admin options and permissions for each app rely heavily on the environments the apps are available in. For example, most Viva apps are accessed through Microsoft Teams and rely on the Microsoft Teams permissions structure.

In this article, we bring together information on the types and levels of admin roles for each Viva app.

## Admin roles in Microsoft Viva

![Image showing admin roles](/Viva/media/admin-roles.png)

## Roles spanning Microsoft Viva apps
The two roles that span Microsoft Viva apps are the Microsoft 365 global admin and the Microsoft Teams admin.

#### Microsoft 365 global admin

The Microsoft 365 global admin role spans the Viva suite. A Microsoft 365 global admin sets up Viva, manages licenses and settings, and can assign admin roles and other required roles for each app.

Learn more about [admin roles in the Microsoft 365 admin center](/microsoft-365/admin/add-users/about-admin-roles).

Learn about [Built-in Microsoft Entra roles](/azure/active-directory/roles/permissions-reference).

#### Microsoft Teams admin

The Teams admin manages the Teams service and creates and manages Microsoft 365 Groups. Teams admins can access everything in the Microsoft Teams admin center and associated PowerShell controls.

For Viva, the Teams admin manages the [deployment of Viva apps](/microsoftteams/manage-apps) and some settings for the apps.

For more information, see [Use Microsoft Teams administrator roles to manage Teams](/microsoftteams/using-admin-roles).

## Admin and management roles for each app

Deciding who should be assigned roles will partly depend on how much access you want a person to have.

For example, you might want to give someone site owner permissions so they can create and manage your Viva Connections dashboard. This person would also be able to manage permissions for that site, edit the home page and other pages, delete pages and other site contents, and more.

To help you decide who should be assigned which roles, here are the overviews of roles for each app and what they do in Viva.<br><br>
Jump to a section:

[Viva Amplify](/viva/microsoft-viva-admin-roles#viva-amplify)<br>
[Viva Connections](/viva/microsoft-viva-admin-roles#viva-connections)<br>
[Viva Engage](/viva/microsoft-viva-admin-roles#viva-engage)<br>
[Viva Glint](#viva-glint)<br>
[Viva Goals](/viva/microsoft-viva-admin-roles#viva-goals)<br>
[Viva Insights](/viva/microsoft-viva-admin-roles#viva-insights)<br>
[Viva Learning](/viva/microsoft-viva-admin-roles#viva-learning)<br>
[Viva Pulse](/viva/microsoft-viva-admin-roles#viva-pulse)<br>

### Viva Amplify

Users with both SharePoint Admin role and Microsoft 365 Groups Admin role can configure the Viva Amplify experience for their end users from within the Viva Amplify admin experience. This role is assigned to users by a Microsoft 365 Global admin.  


| Role | What this role does in Viva |
|-----------|------------|
|SharePoint admin |Users with this role have global permissions within Microsoft SharePoint Online, when the service is present, and the ability to create and manage all Microsoft 365 groups, manage support tickets, and monitor service health. |
|Microsoft 365 Groups admin |Users in this role can create/manage groups and its settings like naming and expiration policies. It's important to understand that assigning a user to this role gives them the ability to manage all groups in the organization across various workloads like Viva Amplify campaigns, Teams, SharePoint, Yammer in addition to Outlook. Also, the user is able to manage the various groups settings across various admin portals like Microsoft admin center, Azure portal, and workload specific ones like Teams and SharePoint admin centers.

### Viva Connections

Depending on the task, Viva Connections administration and permissions are managed through SharePoint Online and Microsoft Teams admin centers. The following are the basic requirements and minimum permission levels.

| Role         | What this role does in Viva |
|--------------|-----------|
|**SharePoint admin** <br> Manages all aspects of SharePoint<br><br> Assigned by Microsoft 365 global admin | <ul><li>Sets up the home site</li><li>Enables global navigation and creates a Dashboard |
|**Teams admin** <br> Manage all aspects of Microsoft Teams<br><br>Assigned by Microsoft 365 global admin|Creates and selects settings for customized app |
|**Site owner**<br>Manages one or more SharePoint sites<br><br>Assigned by SharePoint admin	| Creates a SharePoint home site to meet technical requirements for Viva Connections |
|**Site member**<br>Assigned by site owner|Can author and edit dashboards, news, and other pages|

To learn about setup and administration for Connections, see [Guide to setting up Viva Connections](/viva/connections/guide-to-setting-up-viva-connections), in which required permissions are noted for each step. To learn about SharePoint Online roles and tasks see [Introduction to roles, tasks, and timelines in SharePoint Online](/sharepoint/intranet-roles-tasks). To learn about Teams administration, see [Manage teams in the Microsoft Teams admin center](/microsoftteams/manage-teams-in-modern-portal).

### Viva Engage
| Role         | What this role does in Viva |
|--------------|-----------|
|**Engage admin** <br> Assigned by Microsoft 365 global admin|Sets up Viva Engage for the organization, manages compliance, privacy and features within the application. This role is designated by adding Viva Engage administrators in Microsoft Entra ID as Viva Engage is powered by Viva Engage technology. |
|**Answers admin** <br> Assigned by Microsoft 365 global admin| Sets up Answers within the Viva Engage application. This role is designated by adding a Knowledge manager role in Microsoft Entra ID. All Knowledge managers have Answers admin privileges. To better align the experiences of Topics management and Answers administration, you can assign the same users that manage Topics to manage Answers. Find more information about assigning an [Microsoft Entra role to a group](/azure/active-directory/roles/groups-pim-eligible) or how to [create a role-assignable group](/azure/active-directory/roles/groups-create-eligible).|
|**Corporate communicator**<br>Assigned by the Engage admin or a fellow corporate communicator.  |Can create or manage campaigns and define leaders and audiences in an organization.|
|**Teams admin** <br>Assigned by Microsoft 365 global admin|Uses the Teams admin center to create setup policies to install the app and assign users. |

For more information, see [Manage Viva Engage admins](/viva/engage/manage-viva-engage-users/manage-viva-engage-admins).

### Viva Glint
To set up and manage Viva Glint, you must be a [Microsoft 365 global admin](#microsoft-365-global-admin). 

| Role         | What this role does in Viva |
|--------------|-----------|
|**Viva Glint admin**|Assign other admin roles to help manage the Viva Glint product. Admins can set up program settings and surveys, distribution lists, and reporting features, and support your managers in all aspects of action taking. Viva Glint recommends no more than five (5) administrators for your Viva Glint instance.|
|**Manager**|Organizational team leader who works directly with a Viva Glint Admin to assist with survey administration and/or has access to view reporting and to develop action plans.|


### Viva Goals
Viva Goals has several different roles. Included here are roles that require specific permissions:

| Role         | What this role does in Viva
|--------------|-----------|
|**Organization admin** <br> Assigned by Microsoft 365 global admin|Manages the setup of the organization and can manage users and teams. An organization can have more than one organization administrator. |
|**Organization owner** <br> Assigned by Organization admin<br><br>| Manages members, teams, setup, and billing for the account. By default, they own organization-level OKRs, but organizational objectives can be owned by other members also.|
|**Team owner** <br>Assigned by Organization admin|Manages team-level OKRs |
|**Team admin** <br>Assigned by Team owner|Manages team members |
|**Managers** <br>Assigned by Organization admin|Own their own OKRs and the OKRs of employees who report to them. |
|**Teams admin** <br>Assigned by Microsoft 365 admin|Manages all aspects of Microsoft Teams<br>Uses the Teams admin center to create setup policies to install the app and assign users. |

For more detailed information see [Roles and permissions in Viva Goals](/viva/goals/roles-permissions-in-viva-goals).

For more information about admin settings in the admin dashboard, see [Navigate the admin dashboard](/viva/goals/navigate-admin-dashboard).

### Viva Insights
In Viva Insights, you can assign multiple roles to one person. For example, one person can be both an Insights Administrator and an Insights Analyst. However, it's a best practice to assign the admin and analyst roles to different people to prevent any misuse of or external linking of organizational data with collaboration metrics.

| Role         | What this role does in Viva |
|--------------|-----------|
|**Insights Administrator** <br>Assigned by Microsoft 365 global admin|Has access to the administrator experience in the advanced insights app, which consists of these pages: Organizational data management, Privacy settings, and Manager settings.<br><br>Responsible for configuring the privacy settings and system defaults and for preparing, uploading, and verifying the organizational data for Viva Insights.<br><br>While the Insights admin has access to organizational data, they do not have access to Microsoft 365 data. |
|**Insights Business Leader** <br>Assigned by Microsoft 365 global admin|Insights Business Leaders can see organizational insights on the Organization trends page within the Viva Insights app. |
|**Insights Analyst**<br>Assigned by Microsoft 365 global admin|Has access to the analyst experience in the advanced insights app, which includes the ability to run custom and Power BI queries, view query results, and view the quality of organizational data.
|**People manager**<br> Access enabled by Insights administrator through the Manager settings page in the advanced insights app|Can view organization trends in the Viva Insights app in Teams and on the web. |

For more information on all the roles in Viva Insights see [Roles in Viva Insights](/viva/insights/advanced/setup-maint/user-roles).


### Viva Learning
Viva Learning is by default available in Microsoft Teams with some content already available. To set up learning content sources in Viva Learning and manage individual licensing, you'll need these permissions:

| Role         | What this role does in Viva |
|--------------|-----------|
|**Knowledge admin** <br>Can create and manage content, like topics, acronyms and learning resources. Can also create content centers, monitor service health, and create service requests.<br><br> Assigned by Microsoft 365 global admin|Manages the organization's learning content sources through the Microsoft 365 admin center.<br><br>Users in this role have full access to all knowledge, learning and intelligent features settings in the Microsoft 365 admin center.|
|**SharePoint admin** <br> Manages all aspects of SharePoint<br><br> Assigned by Microsoft 365 global admin | Manages and stores custom learning content for your organization.|
|**Teams admin** <br> Manage all aspects of Microsoft Teams<br><br>Assigned by Microsoft 365 global admin|Can turn on or off the Viva Learning app at the organization level. Learn how to manage your apps in the Microsoft Teams admin center.<br><br> Can create custom app permission policies to allow or block specific users from using Viva Learning.|

The knowledge admin is a Microsoft Entra role in the Microsoft 365 admin center that can be assigned to anyone in the organization. This role manages the organization's learning content sources through the Microsoft 365 admin center. For more information, see [Microsoft Entra built-in roles](/azure/active-directory/roles/permissions-reference#knowledge-administrator) and [Overview of Microsoft Learning](/viva/learning/overview-viva-learning).

For more information on the roles in Viva Learning, see [Admin roles and permissions](/viva/learning/set-up-viva-learning#admin-roles-and-permissions) in Viva Learning.

### Viva Pulse

Viva Pulse admins must have a license to one of the following: Viva Pulse Standalone, Viva Insights Bundle, Viva Suite, or the Viva Pulse Admin-led trial. For more information, see [Licensing requirements](/viva/pulse/get-started/licensing-requirements). The following roles and permissions are required to set up Viva Pulse.


| Role | What this role does in Viva |
| ----------- | ----------- |
| Viva Pulse Admin | The Viva Pulse Admin is assigned by the Microsoft 365 Global Admin. The Viva Pulse Admin can manage the in-app Viva Pulse settings. |
| Teams admin | The Microsoft Teams Admin can pin and install the Viva Pulse Admin in Teams for a customer tenant, as well as manage teams Teams app policies. |
