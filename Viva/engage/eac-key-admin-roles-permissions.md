---
title: "Manage admin roles in Viva Engage"
description: "Learn about admin roles and permissions in Viva Engage and how to assign them."
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: pamgreen
ms.date: 07/28/2023
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
localization_priority: Priority
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Manage admin roles in Viva Engage

To perform administrative tasks in Viva Engage, a user must be assigned an administrator role. Each role is a collection of permissions. The following table summarizes the permissions for each role in Viva Engage. Some Viva Engage roles are managed in Azure Active Directory, and others are managed in Viva Engage.

**Select the role in the table for more details and instructions.**

|Admin role | Business purpose | Where to assign this role |
|------------|-------|----------|
|**[Microsoft 365 Global Administrator](#microsoft-365-global-administrator)** | Manages all aspects of Azure Active Directory (Azure AD) and Microsoft services that use Azure AD identities, including all tasks a Viva Engage Verified Admin and Office 365 report reader can perform. | Azure Active Directory |
| **[Engage admin](#engage-admin) (Yammer admin in Azure AD)**| Manages all aspects of Viva Engage including tenant settings, features, and compliance needs. | Azure Active Directory |
| **[Verified admin](#verified-admin)** | Configures the Viva Engage network. Performs tasks with legal implications for stored data in Viva Engage, such as configuring security settings, monitoring keywords for appropriate use, managing data retention, and exporting data. | Yammer admin center | 
| **[Network admin](#network-admin)**| Configures the Viva Engage network. | Yammer admin center|
| **[Answers admin](#answers-admin)**| Configures Answers in Viva Engage. Performs tasks such as featuring topics and enabling badges. |Azure Active Directory |
| **[Corporate communicator](#corporate-communicator)**| Creates and manages campaigns, define leaders, and manages content across the organization. | Viva Engage admin center |
| **[Community administrator](#community-admin)**| Manages day-to-day activity (including usage) within a community to keep it engaged and productive.| Viva Engage community page |
| **[Office 365 report reader](#office-365-report-reader)**| Views reports showing overall Viva Engage usage. This role is helpful for anyone assigned to improve and monitor Viva Engage adoption. | Office 365 |

## Microsoft 365 Global Administrator
The Global Administrator role has administrative access to all features for Azure Active Directory identities and services that use those identities.
This role controls configuration for Viva Engage in your organization. As such, it has unlimited access to the settings and most of its data, including subscription management. To learn more about this role and security guidelines for assigning it, see [About admin roles in the Microsoft 365 admin center](/microsoft-365/admin/add-users/about-admin-roles).

|Function |Details |
|--------|-----------------|
|**Permissions** |Same as an Engage admin, plus:<br>Assigns or removes the Global Administrator role and the Office 365 reports reader role.<br>Views reports in the Office 365 Usage Reporting dashboard. <br>Manages other Microsoft 365 services.|
|**Who can assign this role**|global admins|
|**How to assign this role**|[Assign Azure AD roles to users](/azure/active-directory/roles/manage-roles-portal)|

## Engage admin  

The Engage admin can set up and configure Engage for your organization. This role manages data, network related settings, and various core and premium features in the application. Viva Engage Azure Active Directory (Azure AD) administrators automatically become Engage admins and have elevated permissions over end users.

A global admin can assign the Engage admin role in [Azure AD](https://techcommunity.microsoft.com/t5/yammer-blog/the-new-viva-engage-administrator-role-is-now-available-in-azure/ba-p/3592577), [PIM](/azure/active-directory/privileged-identity-management/pim-configure), [group based role assignments](/azure/active-directory/roles/groups-concept), or [Azure portal and PowerShell](/azure/active-directory/roles/manage-roles-portal).

**Permissions**

The following table shows the range of actions available to the Engage admin and Global Administrator roles based on their license. Admin permissions require that users have the correct licensing to configure the features.

|Permissions for the Engage admin and Global Administrator roles |M365/O365 customer with Viva Engage core |Microsoft Viva suite customer|
|------------|-------|-------|
|**Manage corporate communicators**: <br> Assigns or removes users as a corporate communicator  | ✓ | ✓ |
|**Manage tenant and user permissions** | ✓ | ✓ |
|**Manage data and compliance**: <br> Manages network and user data; **GDPR** delete | ✓ | ✓ |
|**Manage leaders and their audiences**: <br> Assigns leaders in your organization; identify audiences for the leaders identified | | ✓ |
|**Configure stories and storylines**: <br>Enables storylines and stories for your organization; configure advanced settings like default notifications; specify who can create storyline posts | ✓ | ✓ |
|**Manage sentiment analysis and other feature specific analytics**: <br> Configures level of sentiment to be gathered in the organization; Enable or disable campaign analytics; enable or disable Answers analytics|  |  ✓ |
|**Add, view, and manage campaigns**: <br>Creates and manages campaigns; accesses campaign analytics dashboard|  | ✓ |
|**Enable and manage badges**|  | ✓ |
|**Enable Answers**|  |Global admin only |

## Verified admin
|Function |Details |
|--------|-----------------|
|**Permissions** |See permissions for [Network admins](#network-admin).<br>Assigns verified and network admin roles.<br>Manage content policies. Monitors keywords, data retention, security settings, and reading data in private communities.<br>Exports data and perform integrations with other tools.|
|**Who can assign this role**|A global admin, Engage admin, or verified admin|
|**How to assign this role**|In the Yammer admin center, select **Admins** and do one of the following:<br><li>_To assign a new admin_, find and select the user's name and select **Make this user an admin**. <br><li>_To change a network admin to a verified admin_, select the user's name from the Current Admins list and select **Grant Verified Admin**. <br><li>_To change a Verified admin to a Network admin_, in the Admins section, in the row for the admin select **Revoke Verified Admin**.<br><li>_To remove all admin roles from a Verified admin_, in the Current Admins section, in the row for the admin, select **Remove**.|

## Network admin
|Function |Details |
|--------|-----------------|
|**Permissions** |Configures network settings (including logo and colors), usage policy, and what's included in user profiles.<br>Manages internal users, outside guests, and unlisted groups.<br>Grants and revokes the network admin role.<br>Views reports in the Office 365 Usage Reporting dashboard.<br>Manages other Microsoft 365 services. |
|**Who can assign this role**|A global admin, Engage admin, verified admin, or network admin|
|**How to assign this role**|In the Yammer admin center, select **Admins**. In the Admins section, enter the user's name. Select **Make this user an admin** and select **Submit**.|

## Answers admin  

The Answers admin can set up and configure Answers in Viva Engage. 

Only a global admin can assign (or modify) the Answers admin role. This role is assigned by [adding a knowledge manager in Azure AD](/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal?context=%2Fazure%2Factive-directory%2Froles%2Fcontext%2Fugr-context). Answers admins have elevated permissions over end users. The link between the Answers admin and the Knowledge Manager Azure AD role fits because Answers is best experienced when integrated with topics.  

**Permissions**

The following table shows the actions available to an unlicensed user compared with various admin roles in Viva Engage.

|Answers permissions for an Answers admin, Engage admin, and Global Administrator roles |M365/O365 customer with Viva Engage core |Viva Suite and Viva Topics customer|
|----------------|---------|-------|
|**Ask, answer, upvote, and react**|Interact with questions that they're mentioned in|✓|
|**Suggest topics**| |✓|
|**Mark best answer**| |✓|
|**Delete and close posts**| |✓|
|**See global insights**| |✓|
|**Feature topics**| |Answers admin and Global Administrator only|
|**Approve suggested topics**| |Answers admin and Global Administrator only|
|**Enable and manage badges**| |Answers admin and Global Administrator only|
|**Enable Answers**| |Global Administrator only|

## Corporate communicator

Corporate communicators can create and manage campaigns, define leaders, and manage content across the organization. This role provides more capabilities than the Community admin role, but is less powerful than the overall Engage admin role.

Roles that can assign, modify, or delete Corporate communicators privileges for users include: the Global Administrator role, the Engage admin role, and fellow corporate communicators.

**Permissions**

The actions available to the Corporate Communicator, Engage (Yammer) admin, and Global Administrator role based on their license appear in the following table.  

|Permissions for the Corporate communicator role, Engage admin role, and Global Administrator role |M365/O365 customer with Viva Engage core |Microsoft Viva Suite customer|
|----------------|---------|-------|
|**Identify leaders**: <br> Manages their audience and delegates | |✓|
|**Create campaigns**| |✓|
|**Manage campaigns via**: <br> Publishes active campaigns; ends active campaigns; republishes ended campaigns; deletes campaigns | |✓|
|**View campaign analytics**| |✓|

## Community admin
|Function |Details |
|--------|-----------------|
|**Permissions** |Manages the settings for the community, including name, description, image, and header colors.<br>Manages the conversations and files in the community.<br>Manages members and community admins.<br>Posts announcements.<br>For instructions for typical tasks, see [Manage a community in Viva Engage](https://support.microsoft.com/en-us/topic/manage-community-members-in-viva-engage-3e75fbe9-1b3e-48b5-8e4b-af2716b7873aa).
 |**Who can assign this role**|Any Viva Engage user who creates a community is automatically assigned the community admin role, and can add or remove community admins (up to 100 per community).<br>Engage admins<br><br>**Note:** Network admins and verified admins can prevent Viva Engage users from creating communities. In this case, they must assign the initial community admin, who can do all community admin tasks, including adding more community admins. |
|**How to assign this role**|On the community page, select **Settings** icon > **Manage Members and Admins**. Choose a user and select either **Make Admin** or **Revoke Admin**.|

## Office 365 report reader
|Function |Details |
|--------|-----------------|
|**Permissions** |View [activity](/microsoft-365/admin/activity-reports/viva-engage-activity-report-ww?view=o365-worldwide), [community](/microsoft-365/admin/activity-reports/viva-engage-groups-activity-report-ww?view=o365-worldwide), and [device usage](/microsoft-365/admin/activity-reports/viva-engage-device-usage-report-ww?view=o365-worldwide) reports for Viva Engage in the Microsoft 365 Reports dashboard.|
|**Who can assign this role**|Global Administrator|
|**How to assign this role**|In Microsoft 365, go to **Admin** > **Users** > **Active Users** and select a user.|

## See also
[Assign admin roles in the Microsoft 365 admin center](/microsoft-365/admin/add-users/assign-admin-roles?view=o365-worldwide&redirectSourcePath=%252farticle%252feac4d046-1afd-4f1a-85fc-8219c79e1504)

[Access the Viva Engage admin center](/Viva/engage/eac-as-access-eac)

[Answers admin scenarios in Viva](/Viva/engage/eac-answers-admin-scenarios)
