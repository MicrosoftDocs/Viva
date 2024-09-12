---
title: "Create a dynamic group in Viva Engage"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 09/11/2024
audience: Admin
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 6d2a6ec7-1d65-46bb-b253-1bf441ec80a5
description: "Use dynamic groups in Viva Engage to easily manage group membership through Active Directory."
---

# Create a dynamic group in Viva Engage

When a user's Microsoft Entra attributes are updated within your organization, dynamic groups update automatically. Dynamic groups work well for large organizations where people frequently change teams, roles, and locations. You can create dynamic groups based on various attributes, including role, geography, and department.
  
## Requirements

|**Requirement** <br/> |**Learn more** <br/> |
|:-----|:-----|
|Your organization must be using Microsoft Entra ID P1 or P2 and have a license for each user that's added to a dynamic group.  <br/> |[Microsoft Entra pricing](https://go.microsoft.com/fwlink/?linkId=869572) <br/> |
|The person setting up the groups must have permissions to update Microsoft Entra ID.  <br/> |[Built-in roles for Azure role-based access control](/azure/role-based-access-control/built-in-roles) <br/> |
|Changing the associated Active Directory group to make it dynamic requires PowerShell. <br/> |[Manage Microsoft 365 Groups with PowerShell](https://support.office.com/article/aeb669aa-1770-4537-9de2-a82ac11b0540) <br/> |
|Only Viva Engage groups that are connected to Microsoft 365 can be set up as dynamic groups. This means you must be enforcing Microsoft 365 identity in Viva Engage, and your Viva Engage network must have existing Microsoft 365 connected groups.  <br/> |[Enforce Microsoft 365 identity for Viva Engage users](../configure-your-viva-engage-network/enforce-office-365-identity.md) <br/> [Join a community](https://support.microsoft.com/en-us/topic/join-a-community-in-viva-engage-1ee29da1-5250-4c1e-b773-e7a78cfaf5d4) <br/> |

## Create a dynamic group in Viva Engage

1. Create a Microsoft 365 connected group in Viva Engage.

2. Use PowerShell to change membership management for an Active Directory group to make it dynamic. For instructions, see [Dynamic membership rules for groups in Microsoft Entra ID](/azure/active-directory/enterprise-users/groups-dynamic-membership)

## FAQ

 **Q: Are there limits to the number of members in dynamic groups?**
  
A: Yes. Visit [Limits in Viva Engage](/office365/servicedescriptions/limits-viva-engage) for the current membership limits on dynamic groups.
  
 **Q: Do users experience any differences in Viva Engage when using a dynamic group?**
  
A: Yes. Groups with dynamic membership don't have the **Join** and **Leave** buttons in the top navigation. Instead, users either see **Member** for dynamic groups to which they belong, or **Reserved** if they aren't members of the group.

**Q: What is the difference between a Microsoft 365 connected group and a dynamic group?**
A. For a Microsoft 365 connected group, group membership changes made in any Microsoft 365 app such as Outlook, are available in the group in Viva Engage. For a dynamic group, changes made in the group membership in Microsoft Entra ID are available in the Viva Engage group.

Typically large organizations use dynamic groups if they use Microsoft Entra ID to track department membership, roles, and location, and have Microsoft 365 connected groups for each department, role, and location. Organizations that don't use Microsoft Entra ID in this way typically don't use dynamic groups.
