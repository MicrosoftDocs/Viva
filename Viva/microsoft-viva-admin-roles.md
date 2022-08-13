---
title: "Admin roles and tasks in Microsoft Viva"
ms.reviewer: 
ms.author: loreenl
author: LoreenLa
manager: pamgreen
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
localization_priority: Priority
ms.collection:  
- M365initiative-viva
search.appverid:
- MET150

description: "Learn about the admin roles for Viva Connections, Viva Learning, Viva Topics, and Viva Insights in Microsoft Viva"
---
# Admin roles and tasks in Microsoft Viva
Each Microsoft Viva module has its own individual options for setup, permissions, management, and governance. Admin options and permissions rely on the environment the module is built in. For example, Viva Connections relies heavily on the SharePoint admin and permissions model, and in some cases Teams admin management. In this article, we bring together information on the admin roles and management for each module.

#### Setup in the Microsoft 365 admin  center
While each module has its own setup process, you can find all of the setup pages in one location in the Microsoft 365 admin center. For more information see [Set up Microsoft Viva](/viva/setup-microsoft-viva).


### Viva Topics
You must be a [Microsoft 365 global admin](/microsoft-365/admin/add-users/about-admin-roles) or [SharePoint admin](/sharepoint/sharepoint-admin-role) to set up and manage Topics in the Microsoft 365 admin center. During setup, admins can configure Viva Topics to:
- Select which SharePoint sites will be crawled for topics.
- Select which licensed users who can view topics (topic viewers).
- Select which topics will be excluded from being identified.
- Select which licensed users who can create and edit topics (topic contributors).
- Select which licensed users who can manage topics.
- Name the topic center.

Admins need to be able to coordinate with all Viva Topics stakeholders in their organization to know how to configure it. For example, if a new project has sensitive information, the admin needs to be informed so that they can make sure that the SharePoint site is not crawled for topics, or specific topic names need to be excluded.


For more information on all the roles in Microsoft Viva Topics, see [Roles in Viva Topics](/viva/topics/topic-experiences-roles).

Learn more about planning and administration for Topics in: [Plan for Microsoft Viva Topics](/viva/topics/plan-topic-experiences).

### Viva Connections

Depending on the task, Viva Connections administration and permissions are managed through SharePoint Online and Microsoft Teams admin centers. The following are the basic requirements and minimum permission level:

- **Set a home site**:  [SharePoint admin](/sharepoint/sharepoint-admin-role)
- **Enable global navigation and create a Dashboard**: [SharePoint site admin](/sharepoint/manage-site-collection-administrators)
- **Create and select setting for the customized app**: [Teams admin](/microsoftteams/using-admin-roles)

To learn about setup and administration for Connections, see [Guide to setting up Viva Connections](/viva/connections/guide-to-setting-up-viva-connections), in which required permissions are noted for each step. To learn about SharePoint Online roles and tasks see [Introduction to roles, tasks, and timelines in SharePoint Online](/sharepoint/intranet-roles-tasks). To learn about Teams administration, see [Manage teams in the Microsoft Teams admin center](/microsoftteams/manage-teams-in-modern-portal).

### Viva Learning
Viva Learning is by default available in Microsoft Teams with some content already available. To set up learning content sources in Viva Learning and manage individual licensing, you'll need these permissions:

- [Microsoft Teams admin](/microsoftteams/using-admin-roles)
- [Microsoft 365 global admin](/microsoft-365/admin/add-users/about-admin-roles) or [SharePoint admin](/sharepoint/sharepoint-admin-role)
- [Knowledge admin](/azure/active-directory/roles/permissions-reference#knowledge-administrator)

The knowledge admin is an Azure Active Directory (Azure AD) role in the Microsoft 365 admin center that can be assigned to anyone in the organization. This role manages the organization's learning content sources through the Microsoft 365 admin center. For more information, see [Azure AD built-in roles](/azure/active-directory/roles/permissions-reference#knowledge-administrator)  and [Overview of Microsoft Learning](/viva/learning/overview-viva-learning).

### Viva Insights
 The [Insights admin](/azure/active-directory/roles/permissions-reference#insights-administrator) is responsible for configuring the privacy settings and system defaults and for preparing, uploading, and verifying the organizational data for Viva Insights.

The admin has access to data sources, the ability to upload pages within data sources, and has access to analyst settings. While the admin has access to organizational data, they do not have access to Microsoft 365 data. 

The Insights admin role  must be assigned by a Microsoft 365 admin as described in [Assign user roles](/viva/insights/setup/assign-user-roles). The Insights admin and the legacy Workplace Analytics admin are interchangeable roles. 

For more information on all the roles in Viva Insights see [Roles in Viva Insights](/viva/insights/use/user-roles).

### Viva Goals
Organization Admins have a special role within their organization’s OKR program. Organization Admins will help set up the organization, time periods, users and teams in the Viva Goals instance. To complete these actions, please visit the Admin Dashboard in your solution instance. 

To access the Viva Goals Admin Dashboard, navigate toward the bottom of the left side panel and select “Admin” next to the gear icon.

Inside the Admin Dashboard, you will see different tabs where you can make adjustments, including Settings, Users, Teams, Time Periods, Notifications, Integrations, OKR Model Configuration, and OKRs & Projects.

For more information about admin settings in the admin dashboard, see [Navigate the admin dashboard](/viva/goals/navigate-admin-dashboard)

### Viva Engage
See: [Manager Yammer admins](https://docs.microsoft.com/en-us/yammer/manage-yammer-users/manage-yammer-admins)
