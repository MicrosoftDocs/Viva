---
title: "Key admin roles and permissions in Viva Engage"
description: "Describes roles and permissions for admins in Viva Engage."
ms.reviewer: ethli
ms.author: mamiejohnson
author: Starshine89
manager: dmillerdyson
ms.date: 05/11/2023
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

The following roles have access to the Viva Engage admin center in the Viva Engage app:  

- Microsoft 365 Global admin
- Engage admin  
- Answers admin  
- Corporate communicator

## Microsoft 365 Global admin

The Microsoft 365 Global admin has unlimited access to the organization’s settings and most of its data. Naturally, the Global admin controls configuration for Viva Engage in your organization. To learn more about this role and security guidelines for assigning it, see [About admin roles in the Microsoft 365 admin center](/microsoft-365/admin/add-users/about-admin-roles).

## Engage admin  

The Engage admin can set up and configure Engage for your organization. They also manage data, network related settings, and the various core and premium features in the application. This role is assigned when you [add Viva Engage administrators in Azure Active Directory](https://techcommunity.microsoft.com/t5/yammer-blog/the-new-yammer-administrator-role-is-now-available-in-azure/ba-p/3592577). Viva Engage Azure Active Directory (Azure AD) administrators automatically become Engage admins and have elevated permissions over end users. This connection exists because Viva Engage is powered by Yammer technology.

>[!NOTE]
> This admin role is assigned and modified by a Global admin through Azure AD, [PIM](/azure/active-directory/privileged-identity-management/pim-configure), [group based role assignments](/azure/active-directory/roles/groups-concept), or [Azure portal and PowerShell](/azure/active-directory/roles/manage-roles-portal).

**Permissions**

The following table shows the range of actions available to Engage and Global admins based on their license. Admin permissions depend on those users having the right licensing to configure the features.

|Permissions for Engage admin and Global admin |M365/O365 customer with Viva Engage core |Microsoft Viva suite customer|
|------------|-------|-------|
|**Manage corporate communicators**: <br> Assign or remove users as a corporate communicator  |✓ |✓ |
|**Manage tenant and user permissions** |✓ |✓ |
|**Manage data and compliance**: <br> Manage network and user data; **GDPR** delete |✓ |✓ |
|**Manage leaders and their audiences**: <br> Assign leaders in your organization; identify audiences for the leaders identified | |✓ |
|**Configure stories and storylines**: <br>enable storylines and stories for your organization; configure advanced settings like default notifications; specify who can create storyline posts |✓ |✓ |
|**Manage sentiment analysis and other feature specific analytics**: <br> Configure level of sentiment to be gathered in the organization; Enable or disable campaign analytics; enable or disable Answers analytics|  |✓ |
|**Add, view, and manage campaigns**: <br>create and manage campaigns; access campaign analytics dashboard|  |✓ |
|**Enable and manage badges**|  |✓ |
|**Enable Answers**|  |Global admin only |

## Answers admin  

The Answers admin can set up and configure Answers in Viva Engage. Only a Global admin can assign or modify this role. It's assigned when you [add knowledge managers in Azure AD](/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal?context=%2Fazure%2Factive-directory%2Froles%2Fcontext%2Fugr-context). All knowledge managers become Answers admins. They have elevated permissions over end users. The link between the Answers admin and the Knowledge Manager Azure AD role fits because Answers is best experienced when integrated with topics.  

**Permissions**

The following table shows the actions available to an unlicensed user, Viva Topics licensed user, Answers admin (knowledge manager), Engage (Yammer) admin, and Global admin.

|Answers permissions for Answers admin, Engage admin, and Global admin |M365/O365 customer with Viva Engage core |Viva Suite and Viva Topics customer|
|----------------|---------|-------|
|**Ask, answer, upvote, and react**|Interact with questions that they're mentioned in|✓|
|**Suggest topics**| |✓|
|**Mark best answer**| |✓|
|**Delete and close posts**| |✓|
|**See global insights**| |✓|
|**Feature topics**| |Answers admin and Global admin only|
|**Approve suggested topics**| |Answers admin and Global admin only|
|**Enable and manage badges**| |Answers admin and Global admin only|
|**Enable Answers**| |Answers admin and Global admin only|

## Corporate communicator

Corporate communicators can create and manage campaigns, define leaders, and more in Viva Engage. This role was created to address the need for content management in the organization, beyond being attached to a community, as a Community admin, but not as powerful as the overall Engage admin. Only the following roles can assign, modify, or deleted Corporate communicators privileges for users: Global admin, Engage admin, and fellow corporate communicators.

**Permissions**

The following table shows the actions available to a corporate communicator, Engage (Yammer) admin, and Global admin based on their license.  

|Permissions for corporate communicators, Engage admin, and Global admin |M365/O365 customer with Viva Engage core |Microsoft Viva Suite customer|
|----------------|---------|-------|
|**Identify leaders**: <br> manage their audience and delegates |✓|✓|
|**Create campaigns**| |✓|
|**Manage campaigns via**: <br> publish active campaigns; end active campaigns; republish ended campaigns; delete campaigns | |✓|
|**View campaign analytics**| |✓|

## See also

[Access the Viva Engage admin center](/Viva/engage/eac-as-access-eac)

[Answers admin scenarios in Viva](/Viva/engage/eac-answers-admin-scenarios)
