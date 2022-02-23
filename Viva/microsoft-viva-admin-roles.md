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
Each Microsoft Viva module has its own individual options for setup, permissions, management, and governance. Admin options and permissions rely on the environment the module is built in. For example, Viva Connections relies heavily on the SharePoint admin and permissions model. In this article, we bring together information on the admin roles and management for each module.

#### Setup in the Microsoft 365 admin  center
While each module has its own setup process, you can find all of the setup pages in one location in the Microsoft 365 admin center. For more information see [Set up Microsoft Viva](/viva/setup-microsoft-viva).


### Viva Topics
**Knowledge admins**: Knowledge admins are admins who set up and configure Viva Topics in the Microsoft 365 environment. They also manage the Viva Topics settings after setup has completed. The Knowledge admin role requires you to be a Microsoft 365 global or SharePoint admin since setup and management are done in the Microsoft 365 admin center. During setup, knowledge admins can configure Viva Topics to:

- Select which SharePoint sites will be crawled for topics
- Select which licensed users who can view topics (topic viewers)
- Select which topics will be excluded from being identified
- Select which licensed users who can create and edit topics (topic contributors)
- Select which licensed users who can manage topics (knowledge managers)
- Name the topic center

For more information on all the roles in Microsoft Viva Topics, see [Roles in Viva Topics](/viva/topics/topic-experiences-roles).

Learn more about planning and administration for Topics here: [Plan for Microsoft Viva Topics](/viva/topics/plan-topic-experiences).

### Viva Connections
Depending on the task, Viva Connections administration and permissions are managed through SharePoint Online and Teams admin centers.

To learn about setup and administration for Connections, see [Guide to setting up Viva Connections](/viva/connections/guide-to-setting-up-viva-connections), in which required permissions are noted for each step.

To learn about SharePoint Online roles and tasks see [Introduction to roles, tasks, and timelines in SharePoint Online](/sharepoint/intranet-roles-tasks).

To learn about Teams administration, see [Manage teams in the Microsoft Teams admin center](/microsoftteams/manage-teams-in-modern-portal).

### Viva Learning
Viva Learning is by default available in Microsoft Teams with some content already available. To set up learning content sources in Viva Learning and manage individual licensing, you'll need these permissions:

- Microsoft Teams admin
- Microsoft 365 global admin or SharePoint admin
- Knowledge admin

The knowledge admin is a new Azure Active Directory (Azure AD) role in the Microsoft 365 admin center that can be assigned to anyone in the organization. This role manages the organization's learning content sources through the Microsoft 365 admin center. For more information, see [Azure AD built-in roles](/azure/active-directory/roles/permissions-reference#knowledge-administrator)  and [Overview of Microsoft Learning](/viva/learning/overview-viva-learning).

### Viva Insights
The Insights administrator role must be assigned by a Microsoft 365 admin as described in [Assign user roles](/viva/insights/setup/assign-user-roles). The admin is responsible for configuring the privacy settings and system defaults and for preparing, uploading, and verifying the organizational data for Viva Insights.

The administrator has access to data sources, the ability to upload pages within data sources, and has access to analyst settings. The Insights Administrator and the legacy Workplace Analytics admin are interchangeable roles. The admin is responsible for configuring the privacy settings and system defaults and for preparing, uploading, and verifying the organizational data for Viva Insights.

Insights Administrators are not Microsoft 365 admins. Unless they are also assigned the role of Microsoft 365 admin, they only have access to organizational data, not to Microsoft 365 data. 

For more information on all the roles in Viva Insights see [Roles in Viva Insights](/viva/insights/use/user-roles).
