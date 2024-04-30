---
title: Roles in Viva Amplify
ms.reviewer:
ms.date: 09/13/2023
ms.author: daisyfeller
author: daisyfell
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-amplify
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-amplify
  - Tier1
  - essentials-manage
ms.localizationpriority: medium
description: Learn about admin and user roles and permissions in Microsoft Viva Amplify.
---
# Roles in Viva Amplify

You can make sure that everyone in your organization has the right permissions by familiarizing yourself with [admin](#admin-roles) and [user](#user-roles) roles in Viva Amplify.
  
## Admin roles

Users with both SharePoint Admin role and Microsoft 365 Groups Admin role can configure the Viva Amplify experience for their end users from within the Viva Amplify admin experience. This role is assigned to users by a Microsoft 365 Global admin.  

The following roles and permissions are required to set up Viva Amplify.

|Admin role |Permissions |
|-----------|------------|
|Microsoft 365 global admin |The Microsoft 365 Global Admin has global access to management features and data across Microsoft 365 online services. For Viva Amplify, the Microsoft 365 Global Admin can install and pin the Viva Amplify app in Microsoft Teams, and manage in-app Viva Amplify settings. |
|SharePoint admin |Users with this role have global permissions within Microsoft SharePoint Online, when the service is present, and the ability to create and manage all Microsoft 365 groups, manage support tickets, and monitor service health. |
|Microsoft 365 Groups admin |Users in this role can create/manage groups and its settings like naming and expiration policies. It's important to understand that assigning a user to this role gives them the ability to manage all groups in the organization across various workloads like Viva Amplify campaigns, Teams, SharePoint, Yammer in addition to Outlook. Also, the user is able to manage the various groups settings across various admin portals like Microsoft admin center, Azure portal, and workload specific ones like Teams and SharePoint admin centers.

[Learn more about Microsoft 365 roles.](/azure/active-directory/roles/permissions-reference)

## User roles

User roles are assigned by the campaign creator in Viva Amplify.

|Campaign role |Description |Permission |Manage campaign members |
|--------------|------------|-----------|------------------------|
|Owner |These users oversee and manage the entire campaign. |Full control |Only owners can manage all campaign members and update all roles. |
|Approver |These users approve campaign publications. They can edit and approve Amplify content, list items, and documents. |Approvers can manage other approvers as needed. |
|Editor |These users create and manage campaign publications. They can manage lists and edit campaign materials. |Editors can view campaign members. |
