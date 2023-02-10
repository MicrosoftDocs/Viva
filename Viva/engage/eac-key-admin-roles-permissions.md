---
title: "Key admin roles and permissions in Viva Engage"
description: "Viva Engage is a new employee experience that connects people across the company—wherever and whenever they work—so that everyone is included and engaged."
ms.reviewer: ethli
ms.author: mamiejohnson
author: mamiepjohnson
manager: dmillerdyson
ms.date: 2/15/2023
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

# Key admin roles and permissions in Viva Engage

The following roles will have access to the Engage admin center within the Viva Engage app:  

- Microsoft 365 Global admin
- Engage admin  
- Answers admin  
- Corporate communicator

## Microsoft 365 Global admin

The Microsoft 365 Global admin has unlimited access to your organization’s settings and most of its data. Naturally, the Global admin has permissions to perform all configurations for Viva Engage in your organization. Navigate [here](/microsoft-365/admin/add-users/about-admin-roles?view=o365-worldwide) to learn more about this role and security guidelines for assigning it.

## Engage admin  

The Engage admin can set up and configure Engage for your organization and manage data, network related settings, and the various core or premium features within the application. The new role of Engage admin will be designated by [adding Yammer administrators in AAD](https://techcommunity.microsoft.com/t5/yammer-blog/the-new-yammer-administrator-role-is-now-available-in-azure/ba-p/3592577). Yammer AAD administrators will automatically become Engage admins and they will have elevated permissions over end users. Tying the Engage admin to the Yammer administrator AAD role was intentional, since Viva Engage as an application is powered by Yammer technology.

>[!NOTE]
> This admin role can be assigned and modified by a Global admin through AAD, [PIM](/azure/active-directory/privileged-identity-management/pim-configure), [group based role assignments](/azure/active-directory/roles/groups-concept), or [Azure portal and PowerShell](/azure/active-directory/roles/manage-roles-portal).

**Permissions**

The table below shows the range of actions available to Engage admin and Global admin based on their license. Admin permissions will be dependent on the users having the right licensing to configure those features.

|Permissions for Engage admin and Global admin |M365/O365 customer with Viva Engage core |Microsoft Viva suite customer|
|------------|-------|-------|
|**Manage corporate communicators**: <br> Assign user(s) as a corporate communicator; Remove user(s) as a corporate communicator  |✓ |✓ |
|**Manage tenant and user permissions** (through Yammer)|✓ |✓ |
|**Manage data and compliance**: <br> Manage network and user data; **GDPR** delete |✓ |✓ |
|**Manage leaders and their audiences**: <br> Assign leaders in your organization; **Identify audiences for the leaders identified** |✓ |✓ |
|**Configure stories and storylines**: <br> Enable storylines and stories for your organization; Configure advanced settings like default notifications, specify who can create storyline posts |✓ |✓ |
|**Manage sentiment analysis and other feature specific analytics**: <br> Configure level of sentiment to be gathered in the organization; Enable or disable campaign analytics; Enable or disable Answers analytics|  |✓ |
|**Add, view, and manage campaigns**: <br> Create and manage campaigns; Access campaign analytics dashboard|  |✓ |
|**Enable and manage badges**|  |✓ |
|**Enable Answers**|  |Global admin only |

## Answers admin  

The Answers admin role can set up and configure Answers within the Viva Engage application. This role can only be assigned or modified by a Global admin and will be designated by [adding Knowledge Managers in AAD](/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal?context=%2Fazure%2Factive-directory%2Froles%2Fcontext%2Fugr-context). All Knowledge Managers will become Answers admins and they will have elevated permissions over end users. Tying the Answers admin to the Knowledge Manager AAD role was intentional, since Answers is best experienced when integrated with Topics.  

**Permissions**

The table below shows the range of actions available to an unlicensed user, Viva Topics licensed user, Answers admin (knowledge manager), Engage (Yammer) admin, and Global admin.

|Answers Permissions for Answers admin, Engage admin, and Global admin |M365/O365 customer with Viva Engage core |Viva Suite and Viva Topics customer|
|----------------|---------|-------|
|**Ask, answer, upvote, and react**|Interact with questions they are mentioned in|✓|
|**Suggest topics**| |✓|
|**Mark Best answer**| |✓|
|**Delete and close posts**| |✓|
|**See global insights**| |✓|
|**Feature topics**| |Answers admin and Global admin only|
|**Approve suggested topics**| |Answers admin and Global admin only|
|**Enable and manage badges**| |Answers admin and Global admin only|
|**Enable Answers**| |Answers admin and Global admin only|

## Corporate communicator

Corporate communicators have privileges such as creating and managing campaigns, defining leaders, and more in Viva Engage. This role was created to address the need for a role catered towards content management in the organization, beyond being attached to a community (Community admin) but not as powerful as the overall Engage admin. Corporate communicators can be assigned, modified, or deleted from users by the following admin roles: Global admin, Engage admin, and fellow corporate communicators.

**Permissions**

The table below shows the range of actions available to a corporate communicator, Engage (Yammer) admin, and Global admin based on their license.  

|Permissions for corporate communicators, Engage admin, and Global admin |M365/O365 customer with Viva Engage core |Microsoft Viva Suite customer|
|----------------|---------|-------|
|**Identify leaders**: <br> Manage their audience; Manage their delegates |✓|✓|
|**Create campaigns**| |✓|
|**Manage campaigns via**: <br> Publishing active campaigns; Ending active campaigns; Republishing ended campaigns; Deleting campaigns | |✓|
|**View campaign analytics**| |✓|

## See also

[Access the Engage admin center](/Viva/engage/eac-as-access-eac)

[Answers admin scenarios in Viva](/Viva/engage/eac-answers-admin-scenarios)
