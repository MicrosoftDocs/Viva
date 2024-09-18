---
ms.date: 02/28/2024
title: Introduction to teams in Viva Goals
ms.reviewer: 
ms.author: daisyfeller
author: daisyfell
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-goals
ms.localizationpriority: medium
ms.collection:  
- Strat_SP_modern
- M365-collaboration
- m365initiative-viva-goals
- vg-integration  
search.appverid:
- MET150
description: "Learn about the benefits of creating teams in Viva Goals, as well as the different types of teams and their capabilities."
---

# Introduction to teams in Viva Goals

Viva Goals lets you create teams for departments or large groups working toward shared goals. Here are some of the benefits of using teams in Viva Goals:

- Assigning an OKR to a team helps the team feel a sense of ownership over that goal and creates a clear record of that goal for other parts of your org.

- Teams has permissions that let you control who can create and view your team's OKRs.

- Team goals are pinned in the left nav of the Viva Goals app so team members can easily find them. Team members also receive email updates for goal statuses and check-ins.

- You can set up OKR rhythms for your team, such as scheduled check-in reminders. This helps your team members and OKR owners be more proactive in communication.

## Capabilities overview  

Here are the three main capabilities that teams in Viva Goals have to help run successful OKR programs:

- **Permissions** - Each team can define its own policies for OKRs and initiative creation. You can find more information [here](configure-okr-create-permissions.md).

- **Dashboards** - A dashboard is a shared canvas to which team owners can add OKR-specific widgets that help run business review meetings. A team can have multiple dashboards.

- **Analytics** - Surfaces metrics and reports to help understand OKR adoption and usage within the team and subteams.

## Types of teams in Viva Goals

There are two types of teams in Viva Goals:

- **Microsoft 365 group-connected teams** - In general, the best way to create teams in Viva Goals is from existing Microsoft 365 groups. Teams created this way are called *group-connected teams*. Such teams continue to be synced with their connected group in all aspects, including membership, roles, and properties. Team owners can add members to these teams from Viva Goals or the other relevant Microsoft 365 service.

- **Native teams** - These are teams created within Viva Goals and not connected to any existing Microsoft 365 groups. Team owners can add members to native teams only from within Viva Goals.

| Characteristic | Microsoft 365 group-connected teams | Native teams |
|--- | --- | --- |
|Membership | Members can be added within or outside Viva Goals.<br>When adding members to these connected teams, users can pull members from different types of groups; the members are pulled one time and added to the group. | Members can only be added within Viva Goals. When adding members, multiple groups can be added as members. |
| Expiration policies | Follows expiration policy of connected Microsoft 365 group. | No expiration policies. |
| Administration | Organization owners can remove a team from the organization but can't add members to the team unless they're owners of the team/group. | Organization owners have full access to the team. |
| Lifecycle | Teams can be archived within Viva Goals, but they can't be deleted within Viva Goals: the associated groups can be deleted in other Microsoft 365 services. | Teams can be deleted within Viva Goals. |
| Making goals content private to team members | OKRs and related content can be restricted to team members by setting the team to Private. | This capability doesn't exist for native teams. |

## Capabilities

### Permission to create teams

Organization owners can use permissions to control who can create teams within their organization. Simply go to **Admin** > **General** > **Who can create teams**. By default, all members of an organization can create teams the org owner can change this to only owners or specific people/groups. Note that only mail-enabled security groups are valid group choices.

### Roles within teams

Each user on a team has one of two roles: *team owner* or *team member*. Team owners can access team OKRs, modify team creation permissions, and create dashboards. Members can be assigned OKRs and initiatives; if they have the necessary permissions, they can create OKRs and initiatives, too.

### How being on a team affects being part of an org

All Viva Goals teams are hosted within an organization. Whenever a member or group is added to a team, that member or group is also added to the organization that hosts the team.

### Parent vs subteams

You can select another team as your parent team during team creation or in settings. This lets you follow that team's OKR check-in rhythm, use that team's OKR creation permissions, and/or show up under that team in Team navigation. Typically, your parent team is the team directly above you in the organization (such as your department or division), and both teams follow the same rhythm.

### Lifecycle of teams

Teams can be archived and deleted. We recommend you archive teams that are no longer in service so that only relevant and useful teams remain active. Once a team is archived, you can no longer create OKRs and initiatives under that team, and no users are part of the team. Additionally, any subteams become independent teams in Viva Goals. Any OKRs previously assigned to the archived team will still be available to have actions performed on them, such as check-ins. Even though you won't be able to see the archived team under All Teams, you can see the assigned OKRs by expanding the parent OKRs they're aligned to. You can also view those OKRs/initiatives in the Explorer by applying the **Type** filter and selecting the archived team's name.

Activities related to the archived team are halted: this includes the assigning of new team members and any ongoing team-level notifications. To resume these activities, you would need to restore the team.
