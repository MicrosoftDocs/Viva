---
ms.date: 02/27/2023
title: "Roles and permissions in Viva Goals"
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager: Liz.Pierce
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals
- highpri
search.appverid:
- MET150
description: "Learn about the various roles and permissions in Viva Goals"
---

# Roles and permissions in Viva Goals

## Role types in Viva Goals

|Role  |Description  |Common Activities |
|---------|---------|---------|
|Viva Goals Administrators | Viva Goals Administrators are assigned by Global admins or user admins from the Microsoft 365 Admin center or Azure Active Directory. Viva Goals Administrators are users typically from the IT team (IT admins) and manage the policy settings for Viva Goals for the entire company. <br></br> This role is optional. In the absence of a Viva Goals Admin, the Global admin can manage these Viva Goals policy settings for the company. <br></br> For more information on assigning roles in the [Microsoft 365 admin center](https://go.microsoft.com/fwlink/p/?linkid=2024339), see [Assign admin roles](/microsoft-365/admin/add-users/assign-admin-roles?). <br></br> Related content: [Azure AD roles in the Microsoft 365 admin center](/microsoft-365/admin/add-users/azure-ad-roles-in-the-mac?)   |Some of the tasks managed by Viva Goals Admins are: <br></br>[Configuring who can create organizations](restrict-organization-creation-permissions.md) within Viva Goals. <br></br>- [Configuring integrations](vg-integrations-administration-overview.md) available for all Viva Goals organizations in the tenant. <br></br>- Controlling the URLs that can be embedded in Viva Goals Dashboards. <br></br>- Has the permission to raise Product support tickets via MAC- to Microsoft's support team.         |
|Organization admins      |To understand more about Organizations, see [Understand Organizations and Teams in Viva Goals](understand-orgs-and-teams.md). <br></br> Organization administrators are members who manage the OKR process rollout for the org. In an organization, they're generally the OKR champions. They can configure OKR process properties (such as time period), add or remove users in the org, and create teams within an organization. An organization can have more than one organization administrator.  | Some tasks managed by Organization Admins are<br></br>- Creating OKRs for any team.  <br></br>- Accessing the [admin settings](navigate-admin-dashboard.md) at the org level. <br></br> - Setting policy on who can add members to the org, create teams in the org, create new tags, and export OKRs from their org. <br></br> - Change time-period and notification setting options.    |
|Organization owner      | Organization owners are generally the executive leader of a department/business unit/company for which the organization was created. <br></br> At the time of organization creation in a tenant, the global admin or any user who has permissions to create an organization would become the organization owner of the newly created organization. This ownership can be transferred to another user in that organization in the admin section of the organization. An org can have only one org owner.<br></br>Organizational owners manage members and teams. By default, they own organization-level OKRs, but organizational objectives can be owned by other members also.       |Some of the tasks managed by Organization Owners are <br></br>- Creating OKRs for any team.  <br></br>- Accessing the admin settings at the org level. <br></br>- Setting policy on who can add members to the org, who can create teams in the org, who can create new tags, who can export OKRs from their org. <br></br>- Changing time period and notification setting options.     |
|Team admins      |Team admins are generally OKR champions at a team level, who manage the set-up of a team that includes addition of members to the team, permission settings, notification settings, etc. A Team can have multiple team admins.           |Some tasks managed by Team Admins are <br></br>- Adding members to the team.  <br></br>- Modifying the notification schedule settings of the team. <br></br>- Modifying the OKR and Initiative [creation permission](configure-okr-create-permissions.md) for their team. <br></br>- Creating OKRs for their team.  <br></br>- Editing OKRs of their team. (This is a default activity.)  <br></br>- Creating teams, if the team creation policy at the org level admin console is set so that team admins can create teams.  |
|Team owners      |Teams are functional units within a Viva Goals Organization. <br></br> Team owners are typically managers of a team. Team owners can be managers of people or managers of cross-functional teams. A team can have only one team owner.          |Some tasks managed by Team owners are <br></br>- Adding members to the team. <br></br>- Modifying the notification schedule settings of the team. <br></br>- Modifying the OKR and Initiative creation permission settings for the team. <br></br>- Editing or making check-ins for all OKRs of the team.         |
|Regular Members      |Regular members (the default role for everyone) are typically users within an organization who want to actively participate in the OKR process. Viva Goals recommends all users be added as regular users.         |Some of the tasks managed by Regular members are <br></br>- Creating team-level or org-level OKRs and initiatives in teams or orgs provided they have creation access to the orgs and teams. <br></br>- Editing, aligning, and making check-ins on their OKRs or the OKRs that they've created.        |
|Observers     | Observers, as opposed to Regular members, can't create, edit, or own OKRs. They have only read-only access to the entire organization. Viva Goals recommends adding all users as regular users instead of observers.        | - Observers can't create, edit or align OKRs. <br></br> - Observers can like comments on an OKR, share a summary of an entity page with other users, and comment on OKRs or Initiatives.           |


## Permissions


|Action  |Access  |
|---------|---------|
|Create OKRs or Initiatives      |By default, any regular user is able to create team-level or organization-level OKRs or Initiatives in all levels unless an organization or a team has explicit permissions. <br></br> Org admins or team admins who want to control OKR or initiative [creation access](configure-okr-create-permissions.md) for specific users can configure that access in org/team settings. <br></br> The following roles always have Create OKRs or Initiatives permission: <br></br> **Organization-level OKRs** <br><ul> 1. Organization Administrators <br> 2. Organization Owner </ul><br> **Team-level OKRs** <br><ul> 1. Organization Administrators <br> 2. Organization Owner <br> 3. Team Administrators <br> 4. Team Owner </ul><br>Everyone in an organization can create individual OKRs or Initiatives (OKRs that don't have a team assigned to them) except observers.        |
|Check-in      |The following users get default check-in access for OKRs:<br><ul> 1. OKR owner(s)  <br> 2. Creator of the OKR  <br> 3. Team Admin/Team Owner  <br> 4. Org Admin/Org Owner  <br> 5. Manager of the OKR owner  <br> 6. Owner of the parent OKR (the OKR with which this OKR is aligned) </ul> <br> OKR owners also can grant users [check-in access](https://prod.support.services.microsoft.com/en-us/topic/check-in-with-viva-goals-c0244789-4388-4d2d-9d20-3678900d9b98) by making them check-in owners.         |
|Alignment     |By default, any regular users in an organization can align to any OKR. OKR owners can manage who can check-in on an OKR they own by granting users [alignment access](https://prod.support.services.microsoft.com/en-us/topic/collaborate-43673d1c-0dd7-42ba-97aa-6e712db171d1).         |
|Edit     |Users with edit access to an OKR can also perform the following functions on an OKR: <br><ul> 1. Delete <br> 2. Modify weights and rollups <br> 3. Close <br> 4. Reopen </ul><br> The following users get default edit access for OKRs: <br><ul> 1. OKR owner(s) <br> 2. Creator of the OKR  <br> 3. Team Admin/Team Owner  <br> 4. Org Admin/Org Owner  <br> 5. Manager of the OKR owner:  <br> 6. Owner of the parent O/KR (the OKR with which this OKR is aligned to)  </ul><br> In addition, by modifying permissions to OKRs they own, OKR owners can grant users edit access. <br></br> **Note:** A delegate is a user who can perform all the functions of a user with edit access except change the owner for an OKR or Initiative.         |
|Clone     |Users can clone OKR into a team in which they have access to create OKRs. If the users don't have creation permission access, the OKR is cloned as an individual OKR (not associated with a team).          |
|Comment/Share/Like/Follow      |Any user who is a part of an organization can perform these actions.          |


