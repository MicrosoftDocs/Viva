---
ms.date: 03/29/2024
title: Roles and permissions in Viva Goals
ms.reviewer: 
ms.author: daisyfeller
author: daisyfell
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: concept-article
ms.service: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals
- highpri
- essentials-manage
search.appverid:
- MET150
description: "Learn about the various roles and permissions in Viva Goals."
---

# Roles and permissions in Viva Goals

## Role types in Viva Goals

|Role  |Description  |Common Activities |
|---------|---------|---------|
|Viva Goals Administrator | Viva Goals Administrators are assigned by user admins from the Microsoft 365 admin center or Microsoft Entra ID. Viva Goals Administrators are users typically from the IT team (IT admins) and manage the policy settings for Viva Goals for the entire company. <br></br> For more information on assigning roles in the [Microsoft 365 admin center](https://go.microsoft.com/fwlink/p/?linkid=2024339), see [Assign admin roles](/microsoft-365/admin/add-users/assign-admin-roles?). <br></br> Related content: [Microsoft Entra roles in the Microsoft 365 admin center](/microsoft-365/admin/add-users/azure-ad-roles-in-the-mac?)   |Some of the tasks managed by Viva Goals Admins are: <br></br>- [Configuring who can create organizations](restrict-organization-creation-permissions.md) within Viva Goals. <br></br>- [Configuring integrations](vg-integrations-administration-overview.md) available for all Viva Goals organizations in the tenant. <br></br>- Controlling the URLs that can be embedded in Viva Goals Dashboards. <br></br>- Raising Product support tickets in the Microsoft 365 admin center to Microsoft's support team.         |
|Organization owner      |Organization owners are generally the executive leader of a department/business unit/company for which the organization was created. Alternatively, they might be members who manage the OKR process rollout for the org, such as OKR champions.<br></br>When a user creates an organization, they become the owner of the organization by default.<br></br>Organization owners manage members and teams. <br></br>Organization owners have access to all OKRs within the org, except the private OKRs that are restricted to specific users. <br></br>Organization owners can configure OKR process properties (such as time periods), add or remove users in the org, and create teams within an organization. An organization can have more than one organization owner. | An organization owner can:<br></br>- Add members to the organization.<br></br>- Set up new time periods.<br></br>- Create teams within the organization. <br></br> - Create organization OKRs. <br></br>- Create OKRs for any team within the organization. <br></br>- Access the [admin settings](navigate-admin-dashboard.md) at the org level.<br></br>- Set policy on who can add members to the org, who can create teams in the org, who can create new tags, and who can export OKRs from their org.<br></br>- Change time period and notification setting options.    |
|Team owner    | Teams are functional units within a Viva Goals organization. Team owners are generally OKR champions at a team level; they manage the setup of a team, which includes adding new members to the team and overseeing settings such as those related to permissions and notifications. A Team can have multiple team owners.<br></br>Team owners are typically managers of their respective teams. They might be managers of people or managers of cross-functional teams.|Some tasks managed by team owners are:<br></br>- Creating teams, if the team creation policy at the org level admin console allows for it.<br></br>- Adding members to the team.<br></br>- Modifying the notification schedule settings of the team. <br></br>- Modifying the OKR and initiative [creation permissions](configure-okr-create-permissions.md) for their team.<br>/br>- Editing and making check-ins for all their team's OKRs.<br></br>- Creating OKRs for their team.<br></br>- Editing their team's OKRs. (This is a default activity.)  |
|Member    |Member is the default role for everyone. Members are typically users within an organization who want to actively participate in the OKR process. Viva Goals recommends all users be added as members.    |Some of the tasks managed by members are:<br></br>- Creating team-level or org-level OKRs and initiatives in teams or orgs, provided they have the necessary permissions. <br></br>- Editing, aligning, and making check-ins on OKRs they've created or been assigned.    |

## Permissions

|Action  |Access  |
|---------|---------|
|Create an OKR or initiative      |By default, any regular user is able to create organization-level OKRs and initiatives unless an organization owner has set explicit permissions against doing so.<br></br>A user can create an OKR or initiative within a team only if they are a member of that team.<br></br> Org owners and team owners who want to control OKR or initiative [creation access](configure-okr-create-permissions.md) for specific users can configure that access in org/team settings.<br></br> The following roles always have the permissions necessary to create OKRs/initiatives in the specified context:<br></br>**Organization-level OKRs**<br><ul>Organization owner</ul><br>**Team-level OKRs**<br><ul>Organization owner<br>Team owner(s)</ul><br>Everyone in an organization can create individual OKRs or initiatives (that is, goals that don't have assigned teams).    |
|Check-in      |<br>The following users get default check-in access for an OKR:<br><ul>1. The OKR owner(s)<br>2. The OKR's creator<br>3. The team owner(s)<br>4. The org admin/org owner<br>5. Any OKR owner's manager<br>6. Any owner of the parent OKR (that is, the OKR under which the relevant OKR is aligned)</ul><br>OKR owners also can grant users [check-in access](https://prod.support.services.microsoft.com/en-us/topic/check-in-with-viva-goals-c0244789-4388-4d2d-9d20-3678900d9b98) by making them check-in owners.         |
|Alignment     |By default, any member in an organization can align to any OKR they have access to view. OKR owners can manage who can check in on an OKR they own by granting users [alignment access](https://prod.support.services.microsoft.com/en-us/topic/collaborate-43673d1c-0dd7-42ba-97aa-6e712db171d1).         |
|Edit     |Users with edit access to an OKR can also perform the following functions on that OKR:<br><ul>1. Delete <br>2. Modify weights and rollups<br>3. Close<br>4. Reopen</ul><br> The following users get default edit access for OKRs: <br><ul>1. The OKR owner(s)<br>2. The OKR's creator<br>3. The team owner(s)<br>4. The org admin/org owner<br>5. Any OKR owner's manager<br>6. Any owner of the parent OKR (that is, the OKR under which the relevant OKR is aligned)</ul><br> In addition, by modifying permissions to OKRs they own, OKR owners can grant users edit access. <br></br>**Note:** A delegate is a user who can perform all the functions of a user with edit access *except* change the owner for an OKR or initiative.         |
|Clone     |A user can clone an OKR into a team for which they have OKR creation access. If the user doesn't have the creation permission, the OKR is cloned as an individual OKR (that is, one not associated with a team).          |
|Comment/Share/Like/Follow      |Any user who is a part of an organization can perform these actions.          |
