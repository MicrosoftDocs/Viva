---
title: "Key admin roles and permissions in Viva Engage"
description: "Describes roles and permissions for admins in Viva Engage."
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

# Key admin roles and permissions in Viva Engage

Only users with appropriate roles can perform administrative tasks in Viva Engage. Some roles are managed in Azure Active Directory, and others are managed in Viva Engage.

The following table outlines each of the roles, their purpose, and the actions they can perform. **Select the role name in the table for more details about the role and instructions to add or remove that role.**
>


|Admin role | Business purpose | Where to assign this role |
|------------|-------|----------|
|**[Microsoft 365 Global admin](#microsoft-365-global-admin)** | Manage all aspects of Azure Active Directory (Azure AD) and Microsoft services that use Azure AD identities, including all tasks a Viva Engage Verified Admin and Office 365 report reader can perform. | Azure Active Directory (Azure AD) |
| [**Engage admin**](#engage-admin) (Yammer admin in Azure AD)| Manage all aspects of Viva Engage including tenant settings, features, and compliance needs. | Azure Active Directory |
| **[Verified admin](#verified-admin)** | Configure the Viva Engage network. Perform tasks with legal implications for stored data in Viva Engage, such as configuring security settings, monitoring keywords for appropriate use, managing data retention, and exporting data. | Yammer admin center | 
| **[Network admin](#network-admin)**| Configure the Viva Engage network. | Yammer admin center|
| **[Answers admin](#answers-admin)**| Configure Answers in Viva Engage. Perform tasks such as featuring topics and enabling badges. |Yammer admin center|
| **[Corporate communicator](#corporate-communicator)**| Create and manage campaigns, define leaders, and manage content across the organization. | Viva Engage admin center |
| **[Community admin](#community-admin)**| Manage day-to-day activity (including usage) within a community to keep it engaged and productive.| Viva Engage community page |
| **[Office 365 report reader](#office-365-report-reader)**| View reports showing overall Viva Engage usage. This role is helpful for anyone assigned to improve and monitor Viva Engage adoption. | Office 365 |

## Microsoft 365 Global admin
The Global administrator role has administrative access to all features in, and services that use, Azure Active Directory identities. They also have the ability to manage subscriptions.
The Global admin controls configuration for Viva Engage in your organization and has unlimited access to the settings and most of its data. To learn more about this role and security guidelines for assigning it, see About admin roles in the [Microsoft 365 admin center](/microsoft-365/admin/add-users/about-admin-roles).

## Engage admin  

The Engage admin can set up and configure Engage for your organization. They also manage data, network related settings, and various core and premium features in the application. Viva Engage Azure Active Directory (Azure AD) administrators automatically become Engage admins and have elevated permissions over end users.

A Global admin can assign the Engage admin role in [Azure AD](https://techcommunity.microsoft.com/t5/yammer-blog/the-new-viva-engage-administrator-role-is-now-available-in-azure/ba-p/3592577), [PIM](/azure/active-directory/privileged-identity-management/pim-configure), [group based role assignments](/azure/active-directory/roles/groups-concept), or [Azure portal and PowerShell](/azure/active-directory/roles/manage-roles-portal).

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

## Verified admin
Verified admins can perform all the tasks a Network admin can do and assign verified and network admin roles. They manage content policies  in addition to monitoring keywords, data retention, security settings, and reading data in private groups. They can export data and perform integrations with other tools.
A Global admin, Engage admin, or Verified admin can assign a Verified Admin using these steps:
1. In the Yammer admin center, select **Admins**. 
1. Search for and select the user's name, and then select **Make this user an admin**. 
1. Select ** Submit**.

To promote an existing Network Admin to Verified Admin:
- In the Yammer admin center, select **Admins**. If the user is already a network admin, their name appears in the **Current Admins list**. Select  **Grant Verified Admin**.

To change a Verified Admin to Network Admin:
- In the Yammer admin center, select  **Admins**. In the **Admins section**, in the row for the admin, select **Revoke Verified Admin**.

To remove all admin roles from a Verified Admin:
- In the Yammer admin center, select **Admins**. In the **Current Admins section**, in the row for the admin, select **Remove**.

## Answers admin  

The Answers admin can set up and configure Answers in Viva Engage. 

Only Global admins can assign (or modify) the Answers admin role by [adding a knowledge manager in Azure AD](/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal?context=%2Fazure%2Factive-directory%2Froles%2Fcontext%2Fugr-context). Answers admins have elevated permissions over end users. The link between the Answers admin and the Knowledge Manager Azure AD role fits because Answers is best experienced when integrated with topics.  

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
|**Enable Answers**| |Global admin only|

## Corporate communicator

Corporate communicators can create and manage campaigns, define leaders, and manage content across the organization. This role provides more capabilities than Community admins, but is less powerful than the overall Engage admin.

Roles that can assign, modify, or delete Corporate communicators privileges for users include: Global admin, Engage admin, and fellow corporate communicators.

**Permissions**

Actions available to a corporate communicator, Engage (Yammer) admin, and Global admin based on their license are shown in the following table.  

|Permissions for corporate communicators, Engage admin, and Global admin |M365/O365 customer with Viva Engage core |Microsoft Viva Suite customer|
|----------------|---------|-------|
|**Identify leaders**: <br> manage their audience and delegates | |✓|
|**Create campaigns**| |✓|
|**Manage campaigns via**: <br> publish active campaigns; end active campaigns; republish ended campaigns; delete campaigns | |✓|
|**View campaign analytics**| |✓|

## See also

[Access the Viva Engage admin center](/Viva/engage/eac-as-access-eac)

[Answers admin scenarios in Viva](/Viva/engage/eac-answers-admin-scenarios)
