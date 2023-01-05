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
- highpri
search.appverid:
- MET150

description: "Learn about the admin roles for Viva Connections, Viva Learning, Viva Topics, and Viva Insights in Microsoft Viva"
---
# Admin roles and tasks in Microsoft Viva
Setup and management of the Microsoft Viva suite starts with the Microsoft 365 admin. The Microsoft 365 admin can then assign additional roles for the management, tasks and maintenance of each Viva app.
Admin options and permissions for each app rely heavily on the environments the apps are available in. For example, most Viva apps are accessed through Microsoft Teams and rely on the Microsoft Teams permissions structure.

In this article, we bring together information on the types and levels of admin roles for each Viva app.

## Admin roles in Microsoft Viva

![Image of the Viva admin roles.](./media/TO COME)

## Roles spanning Microsoft Viva apps

#### Microsoft 365 admin

The Microsoft 365 admin role spans the Viva suite. A Microsoft 365 admin sets up Viva, manages licenses and settings, and can assign the following Azure AD roles, which may be required for some apps and tasks:

- Viva Topics [Knowledge admin](/azure/active-directory/roles/permissions-reference#knowledge-manager)
- Viva Learning [Knowledge manager](/azure/active-directory/roles/permissions-reference#knowledge-administrator)
- Viva Insights [Business Leader](/azure/active-directory/roles/permissions-reference#insights-business-leader), [Administrator](/azure/active-directory/roles/permissions-reference#insights-administrator), and [Analyst](/azure/active-directory/roles/permissions-reference#insights-analyst)
- [SharePoint admin](/azure/active-directory/roles/permissions-reference#sharepoint-administrator)
- [Teams admin](/azure/active-directory/roles/permissions-reference#teams-administrator)

Learn more about [admin roles in the Microsoft 365 admin center](/microsoft-365/admin/add-users/about-admin-roles?view=o365-worldwide)

Learn about [Azure AD roles](/azure/active-directory/roles)

#### Microsoft Teams admin

The Teams admin manages the Teams service and creates and manages Microsoft 365 Groups. Teams admins can access everything in the Microsoft Teams admin center and associated PowerShell controls.

For Viva, the Teams admin manages the [deployment of Viva apps](/microsoftteams/manage-apps) and some settings for the apps.

For more information, see [Use Microsoft Teams administrator roles to manage Teams](/microsoftteams/using-admin-roles)

## Admin and management roles for each app

Deciding who should be assigned roles will partly depend on how much access you want a person to have.

For example, you might want to give someone site owner permissions so they can create and manage your Viva Connections dashboard. This person would also be able to manage permissions for that site, edit the home page and other pages, delete pages and other site contents, and more.

To help you decide who should be assigned which roles, here are overviews of roles for each app and what they do in Viva.<br><br>
[Topics](/viva/microsoft-viva-admin-roles#viva-topics)<br>
[Connections](/viva/microsoft-viva-admin-roles#viva-connections)<br>
[Learning](/viva/microsoft-viva-admin-roles#viva-learning)<br>
[Insights](/viva/microsoft-viva-admin-roles#viva-insights)<br>
[Goals](/viva/microsoft-viva-admin-roles#viva-goals)<br>
[Engage](/viva/microsoft-viva-admin-roles#viva-engage)<br>
[Sales](/viva/microsoft-viva-admin-roles#viva-sales)


#### Viva Topics

You must be a [Microsoft 365 global admin](/microsoft-365/admin/add-users/about-admin-roles) or [SharePoint admin](/sharepoint/sharepoint-admin-role) to set up and manage Topics in the Microsoft 365 admin center. 

| Role         | What this role does in Viva
|--------------|-----------|
|**Viva Topics admin** <br> Must be a Microsoft 365 global administrator or a SharePoint administrator and Groups administrator| <ul><li>Name the topic center</li><li>Select which SharePoint sites will be crawled for topics</li><li>Assign knowledge manager role</li><li>Select which licensed users can view and access topics (topic viewers)</li><li>Select which licensed users can create and edit topics (topic contributors)</li><li>Select which topics will be excluded from being identified</ul>|
|**Knowledge manager**<br> Knowledge managers are users who manage topics in your organization.<br><br>Assigned by Topics admin| On the Manage topics page, knowledge managers can do the following tasks: <ul><li>View AI-suggested topics</li><li>Review topics to confirm that they're valid</li><li>Remove topics that you don’t want visible to users.</li><br>|

For more information on all the roles in Microsoft Viva Topics, see [Roles in Viva Topics](/viva/topics/topic-experiences-roles).

Learn more about planning and administration for Topics in: [Plan for Microsoft Viva Topics](/viva/topics/plan-topic-experiences).

#### Viva Connections

Depending on the task, Viva Connections administration and permissions are managed through SharePoint Online and Microsoft Teams admin centers. The following are the basic requirements and minimum permission levels.

| Role         | What this role does in Viva
|--------------|-----------|
|**SharePoint admin** <br> Manages all aspects of SharePoint<br><br> Assigned by Microsoft 365 admin | <ul><li>Sets up the home site</li><li>Enables global navigation and creates a Dashboard |
|**Teams admin** <br> Manage all aspects of Microsoft Teams<br><br>Assigned by Microsoft 365 admin|Creates and selects settings for customized app
|**Site owner**<br>Manages one or more SharePoint sites<br><br>Assigned by SharePoint admin	| Creates a SharePoint home site to meet technical requirements for Viva Connections
|**Site member**<br>Assigned by site owner|Can author and edit dashboards, news, and other pages|

To learn about setup and administration for Connections, see [Guide to setting up Viva Connections](/viva/connections/guide-to-setting-up-viva-connections), in which required permissions are noted for each step. To learn about SharePoint Online roles and tasks see [Introduction to roles, tasks, and timelines in SharePoint Online](/sharepoint/intranet-roles-tasks). To learn about Teams administration, see [Manage teams in the Microsoft Teams admin center](/microsoftteams/manage-teams-in-modern-portal).

#### Viva Learning
Viva Learning is by default available in Microsoft Teams with some content already available. To set up learning content sources in Viva Learning and manage individual licensing, you'll need these permissions:

| Role         | What this role does in Viva
|--------------|-----------|
|**Knowledge admin** <br> Assigned by Microsoft 365 admin|Manages the organization's learning content sources through the Microsoft 365 admin center.<br><br>Users in this role have full access to all knowledge, learning and intelligent features settings in the Microsoft 365 admin center. <br><br>Knowledge admins can create and manage content, like topics, acronyms and learning resources. Additionally, these users can create content centers, monitor service health, and create service requests.|
|**SharePoint admin** <br> Manages all aspects of SharePoint<br><br> Assigned by Microsoft 365 admin | Manages and stores custom learning content for your organization|
|**Teams admin** <br> Manage all aspects of Microsoft Teams<br><br>Assigned by Microsoft 365 admin|Can turn on or off the Viva Learning app at the organization level. Learn how to manage your apps in the Microsoft Teams admin center.<br><br> Can create custom app permission policies to allow or block specific users from using Viva Learning.

- [Microsoft Teams admin](/microsoftteams/using-admin-roles)
- [Microsoft 365 global admin](/microsoft-365/admin/add-users/about-admin-roles) or [SharePoint admin](/sharepoint/sharepoint-admin-role)
- [Knowledge admin](/azure/active-directory/roles/permissions-reference#knowledge-administrator)

The knowledge admin is an Azure Active Directory (Azure AD) role in the Microsoft 365 admin center that can be assigned to anyone in the organization. This role manages the organization's learning content sources through the Microsoft 365 admin center. For more information, see [Azure AD built-in roles](/azure/active-directory/roles/permissions-reference#knowledge-administrator)  and [Overview of Microsoft Learning](/viva/learning/overview-viva-learning).

### Viva Insights
 The [Insights admin](/azure/active-directory/roles/permissions-reference#insights-administrator) is responsible for configuring the privacy settings and system defaults and for preparing, uploading, and verifying the organizational data for Viva Insights.

The admin has access to data sources, the ability to upload pages within data sources, and has access to analyst settings. While the admin has access to organizational data, they do not have access to Microsoft 365 data. 

The Insights admin role  must be assigned by a Microsoft 365 admin as described in [Assign user roles](/viva/insights/advanced/setup-maint/assign-user-roles). The Insights admin and the legacy Workplace Analytics admin are interchangeable roles. 

For more information on all the roles in Viva Insights see [Roles in Viva Insights](/viva/insights/advanced/setup-maint/user-roles).

### Viva Goals
Viva Goals has several different roles. Included here are roles that require specific permissions:

| Role         | What this role does in Viva
|--------------|-----------|
|**Organization admin** <br> Assigned by Microsoft 365 admin|Manages the setup of the organization and can manage users and teams. An organization can have more than one organization administrator.
|**Organization owner** <br> Assigned by Organization admin<br><br>| Manages members, teams, setup, and billing for the account. By default, they own organization-level OKRs, but organizational objectives can be owned by other members also.|
|**Team admin** <br>Assigned by Organization owner|Manages team members
|**Team owner** <br>Assigned by Team admin|Manages team-level OKRs
|**Managers**|Own their own OKRs and the OKRs of employees who report to them.
|**Teams admin** <br>Manages all aspects of Microsoft Teams<br><br>Assigned by Microsoft 365 admin|Uses the Teams admin center to create setup policies to install the app and assign users.

For more detailed information see [Roles and permissions in Viva Goals](/viva/goals/roles-permissions-in-viva-goals).

For more information about admin settings in the admin dashboard, see [Navigate the admin dashboard](/viva/goals/navigate-admin-dashboard)

### Viva Engage
| Role         | What this role does in Viva
|--------------|-----------|
|**Viva Engage admin** <br> |Sets up the Yammer network and performs tasks such as configuring security settings, monitoring keywords for appropriate use, managing data retention, and exporting  data. Also can view reports showing overall usage. This role maps to the Yammer admin Azure AD role.
|**Yammer community admin** <br> |Manages day-to-day activity within a community to keep the community engaged and productive, including monitoring usage activity. Any Yammer user who creates a community is assigned the Community Admin role.|
|**Teams admin** <br>Assigned by Microsoft 365 admin|Uses the Teams admin center to create setup policies to install the app and assign users.

For more information, see: [Manager Yammer admins](/yammer/manage-yammer-users/manage-yammer-admins)

#### Viva Sales
You need to be a Microsoft 365 administrator to deploy and install the Viva Sales add-in for Outlook. You need to be a Teams administrator to deploy and install Viva Sales for Teams.

| Role         | What this role does in Viva
|--------------|-----------|
|**Microsoft 365 admin** |Deploys and installs the Viva Sales add-in for Outlook.
|**Teams admin** <br>Assigned by Microsoft 365 admin|Uses the Teams admin center to create setup policies to install the app and assign users.
|**CRM security role**|Viva Sales applies your organization's existing CRM access controls and user permissions. Users must have the correct permissions to view, update, and create records in their CRM systems from Viva Sales. Required roles depend on the system you are using.

For more information on these and other roles, see [Install Viva Sales](/Viva/sales/install-viva-sales)

