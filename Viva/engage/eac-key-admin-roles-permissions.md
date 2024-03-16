---
title: "Manage admin roles in Viva Engage"
description: "Learn about admin roles and permissions in Viva Engage and how to assign them."
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 03/15/2023
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
- essentials-manage
search.appverid:
- MET150
---

# Manage administrator roles in Viva Engage

To perform administrative tasks and facilitate many of the premium features in Viva Engage, users need to be assigned specific roles. The table below describes each of the admin roles in Viva Engage and the business functions they enable.  

**Select the role in the table for more details and instructions.**

|Admin role | Business function |
|------------|-------|
|**[Microsoft 365 Global Administrator](#microsoft-365-global-administrator)** | Manages all aspects of Microsoft 365 Entra and services that use Microsoft 365 Entra identities. This role controls admin role assignment and configuration in Viva Engage. As such, global admins have unlimited access to settings and most of its data, including subscription management.|
| **[Engage Administrator](#engage-admin)**| Configures and manages all aspects of Viva Engage including tenant settings, core and premium features, and compliance. |
| **[Verified Administrator](#verified-admin)** | Configures the Viva Engage network. Performs tasks that have legal implications, such as managing security settings, monitoring keywords for appropriate use, managing data retention, and exporting data. | 
| **[Network Administrator](#network-admin)**| Configures the Viva Engage network.|
| **[Answers Administrator](#answers-admin)**| Configures Answers in Viva Engage, manages topics, and enables badges. |
| **[Corporate Communicator](#corporate-communicator)**| Creates and manages official campaigns, defines leaders, and manages content across the organization. |
| **[Community Administrator](#community-admin)**| Manages day-to-day activity (including usage) within a community to keep it engaged and productive.| Viva Engage community page |

## Who assigns roles and where?

Some admins have more permissions than others and can assign Viva Engage roles to users. The following table lists admins in order of permissions and the roles they can assign.

|Admin role | Can assign these roles |Assigned in|
|------------|-------|--------|
|Admin role |Can assign these roles| Assigned in|
|Microsoft 365 Global Admin|Other global admins, Engage admins, Answers admins (Knowledge manager)|Microsoft Entra ID|
|Engage Admin|Verified admins, Network admins, Corporate communicators|Microsoft Entra ID|
|Verified Admin|Verified admins, Network admins, Corporate communicators|Yammer admin center / Viva Engage admin center|
|Network Admin|Other network admins, Corporate Communicators|Yammer admin center / Viva Engage admin center|
|Community Admin|Other community admins|Viva Engage community|

## Role hierarchy

:::image type="content" source="/viva/media/engage/admin/engage-admin-hierarchy.png" alt-text="Image shows the hierarchy of administrator roles in Viva Engage, with roles having the most power at the top.":::

|Function |Details |
|------------|-----------------|
|**Permissions** |Same as an Engage admin, plus:<br>Assigns or removes the Microsoft 365 Global administrator role and the Office 365 reports reader role.<br>Views report in the Microsoft 365 Usage Reporting dashboard. <br>Manages other Microsoft 365 services.|
|**Who can assign this role**|Microsoft 365 Global administrators|
|**How to assign this role**| See [Assign admin roles in the Microsoft 365 admin center](/microsoft-365/admin/add-users/assign-admin-roles)|

## Engage admin  

Engage admins can set up and configure Engage for your organization. This role manages data, network related settings, and various core and premium features in the application. Yammer administrators in Microsoft Entra ID automatically become Engage admins and have elevated permissions over end users.

A Microsoft 365 Global administrator can assign the Engage admin role in [Microsoft Entra ID](https://techcommunity.microsoft.com/t5/yammer-blog/the-new-viva-engage-administrator-role-is-now-available-in-azure/ba-p/3592577), [PIM](/azure/active-directory/privileged-identity-management/pim-configure), [group based role assignments](/azure/active-directory/roles/groups-concept), or [Microsoft Entra portal and PowerShell](/azure/active-directory/roles/manage-roles-portal).

**Permissions**

The following table shows the range of actions available to the Engage admin and Microsoft 365 Global administrator roles based on their license. Admin permissions require that users have the correct licensing to configure features.

|Permissions for the Engage admin and Microsoft 365 Global administrator roles |Microsoft 365 customer with Viva Engage core |Microsoft Viva suite customer|
|----------------------|:-:|:-:|
|**Manage corporate communicators**: <br> Assigns or removes users as a corporate communicator  |✓|✓|
|**Manage tenant and user permissions** |✓|✓|
|**Manage data and compliance**: <br> Manages network and user data; **GDPR** delete |✓|✓|
|**Manage leaders and their audiences**: <br> Assigns leaders in your organization; identify audiences for the leaders identified | |✓|
|**Configure stories and storylines**: <br>Enables storylines and stories for your organization; configure advanced settings like default notifications; specify who can create storyline posts |✓|✓|
|**Manage sentiment analysis and other feature specific analytics**: <br> Configures level of sentiment to be gathered in the organization; Enable or disable campaign analytics; enable or disable Answers analytics|  |✓|
|**Add, view, and manage campaigns**: <br>Creates and manages campaigns; removes posts that aren't aligned with campaign; accesses campaign analytics dashboard|  |✓|
|**Enable and manage badges**|  |✓|
|**Enable Answers**|  |Microsoft 365 Global administrator only |

## Verified admin
|Function |Details |
|------------|-----------------|
|**Permissions** |See permissions for [Network admins](#network-admin).<br>Assigns verified and network admin roles.<br>Manage content policies. Monitors keywords, data retention, security settings, and reading data in private communities.<br>Exports data and perform integrations with other tools.|
|**Who can assign this role**|A Microsoft 365 Global administrator, Engage admin, or verified admin|
|**How to assign this role**|In the Yammer admin center, select **Admins** and do one of the following:<ul><li>To assign a new admin, find and select the user's name and select **Make this user an admin**.</li><li>To change a network admin to a verified admin, select the user's name from the Current Admins list and select **Grant Verified Admin**.</li><li>To change a verified admin to a network admin, in the Admins section, in the row for the admin select **Revoke Verified Admin**.</li><li>To remove all admin roles from a verified admin, in the Current Admins section, in the row for the admin, select **Remove**.</li>|

## Network admin

|Function |Details |
|------------|-----------------|
|**Permissions** |Configures network settings (including logo and colors), usage policy, and what's included in user profiles.<br>Manages internal users, outside guests, and unlisted groups.<br>Grants and revokes the network admin role.<br>Can view reports in the Microsoft 365 Usage Reporting dashboard.<br>Manages other Microsoft 365 services. |
|**Who can assign this role**|A Microsoft 365 Global administrator, Engage admin, verified admin, or network admin|
|**How to assign this role**|In the Yammer admin center, select **Admins**. In the Admins section, enter the user's name. Select **Make this user an admin** and select **Submit**.|

## Answers admin  

The Answers admin can set up and configure Answers in Viva Engage. 

Only a Microsoft 365 Global administrator can assign (or modify) the Answers admin role. The Answers admin role is assigned by [adding a knowledge manager in Microsoft Entra ID](/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal?context=%2Fazure%2Factive-directory%2Froles%2Fcontext%2Fugr-context). Answers admins have elevated permissions over end users. The link between the Answers admin and the Knowledge Manager Microsoft Entra ID role fits because the Answers experience is optimal when integrated with Topics.  

**Permissions**

The following table shows the actions available to an unlicensed user compared with various admin roles in Viva Engage.

|Answers permissions for an Answers admin, Engage admin, and Microsoft 365 Global Administrator roles |M365/O365 customer with Viva Engage core |Viva Suite and Topics customer|
|----------------------|:-:|:-:|
|**Ask, answer, upvote, and react**|Interact with questions that they're mentioned in|✓|
|**Suggest topics**| |✓|
|**Mark best answer**| |✓|
|**Delete and close posts**| |✓|
|**See global insights**| |✓|
|**Feature topics**| |Answers admin and Microsoft 365 Global administrator only|
|**Approve suggested topics**| |Answers admin and Microsoft 365 Global administrator only|
|**Enable and manage badges**| |Answers admin and Microsoft 365 Global administrator only|
|**Enable Answers**| |Microsoft 365 Global administrator only|

## Corporate communicator

The Corporate communicator role provides more capabilities than the community admin role, but fewer than the Engage admin role. Corporate communicators can create and manage campaigns, define leaders, assign campaign co-organizers, and manage content across the organization.

Roles that can assign, modify, or delete Corporate communicators privileges for users include: the Microsoft 365 Global administrator role, the Engage admin role, and fellow corporate communicators.

**Permissions**

The actions available to the corporate communicator, Engage (Yammer) admin, and Microsoft 365 Global Administrator role based on their license appear in the following table.  

|Permissions for the corporate communicator role, Engage admin role, and Microsoft 365 Global administrator role |Microsoft 365 customer with Viva Engage core |Microsoft Viva Suite customer|
|----------------------|:-:|:-:|
|**Identify leaders**: <br> Defines leaders, manages their audiences and delegates | |✓|
|**Create campaigns**| |✓|
|**Manage campaigns**: <br> Publishes active campaigns; ends active campaigns; republishes ended campaigns; deletes campaigns; removes posts as needed | |✓|
|**View campaign analytics**| |✓|

## Community admin

|Function |Details |
|--------|-----------------|
|**Permissions** |Manages the settings for the community, including name, description, image, and header colors.<br>Manages the conversations and files in the community.<br>Manages members and community admins.<br>Posts announcements.<br>
 |**Who can assign this role**|Any Engage user who creates a community is automatically assigned the community admin role. Community admins can add (up to 100) and remove other community admins.<br>Engage admins<br><br>**Note:** Network admins and verified admins can prevent Engage users from creating communities. In this case, they must assign the initial community admin, who can do all community admin tasks. |
|**How to assign this role**|On the community page, select **Settings** icon > **Manage Members and Admins**. Choose a user and select either **Make Admin** or **Revoke Admin**.|

## Office 365 report reader

|Function |Details |
|--------|-----------------|
|**Permissions** |Views the activity, community, and device usage reports for Viva Engage in the Microsoft 365 Reports dashboard.|
|**Who can assign this role**|Microsoft 365 Global administrator|
|**How to assign this role**|In Microsoft 365, go to **Admin** > **Users** > **Active Users** and select a user.|

## See also

[Assign admin roles in the Microsoft 365 admin center](/microsoft-365/admin/add-users/assign-admin-roles?view=o365-worldwide&redirectSourcePath=%252farticle%252feac4d046-1afd-4f1a-85fc-8219c79e1504&preserve-view=true)

[Access the Viva Engage admin center](/Viva/engage/eac-as-access-eac)

[Answers admin scenarios in Viva](/Viva/engage/eac-answers-admin-scenarios)
	