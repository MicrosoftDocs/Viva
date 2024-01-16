---
ms.date: 01/blah/2024
title: Blah
ms.reviewer: 
ms.author: v-nstockwell
author: DefinitelyNotNitza
manager: Liz.Pierce
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:  
- Strat_SP_modern
- M365-collaboration
- m365initiative-viva-goals
- vg-integration  
search.appverid:
- MET150
description: "Blah."
---

# Introduction to teams in Viva Goals

Viva Goals lets you create teams for departments or large groups working toward shared goals. Here are some of the benefits of using teams in Viva Goals:

- Assigning an OKR to a team helps the team feel a sense of ownership over that goal and creates a clear record of that goal for other parts of your org.

- Teams have permissions that let you control who can create and view your team's OKRs.

- Team goals are pinned in the left nav of the Viva Goals app so team members can easily find them. Team members also receive email updates for goal statuses and check-ins.

- You can set up OKR rhythms for your team, such as scheduled check-in reminders. This helps your team members and OKR owners be more proactive in communication.

## Capabilities overview  

Here are the three main capabilities that teams in Viva Goals have to help run successful OKR programs:

- **Permissions** - Each team can define its own policies for OKRs and project creation. You can find more information [here](configure-okr-create-permissions.md).

- **Dashboards** - A dashboard is a shared canvas to which team owners can add OKR-specific widgets that help run business review meetings. A team can have multiple dashboards.

- **Analytics** - Surfaces metrics and reports to Helps understand OKR adoption and usage within the team and sub-teams. <!--Editor's Note: What is this saying?-->

## Types of teams in Viva Goals

There are two types of teams in Viva Goals:

- **Microsoft 365 group-connected teams** - In general, the best way to create teams in Viva Goals is from existing Microsoft 365 groups. Teams created this way are called *group-connected teams*. Such teams continue to be synced with their connected group in all aspects, including membership, roles, and properties. Team owners can add members to these teams from Viva Goals or the other relevant Microsoft 365 service.

- **Classic teams** - These are teams created within Viva Goals and not connected to any existing Microsoft 365 groups. Team owners can add members to classic teams only from within Viva Goals.

<!--Editor's Note: Now that I have a more complete understanding of the material, I actually think "native teams" works better.-->

| Characteristic | Microsoft 365 group-connected teams | Classic teams |
|--- | --- | --- |
|Membership | Members can be added within or outside Viva Goals.<br>When adding members to these connected teams, users can search pull members from different types of groups; the members are pulled one time and added to the group. | Members can be added only within Viva Goals. When adding members, multiple groups can be added as members.<!--Editor's Note: These require clarification.--> |
| Expiration policies | Follows expiration policy of connected Microsoft 365 group. | No expiration policies. |
| Administration | Organization owners can remove a team from the organization but cannot add members to the team unless they are owners of the team/group. | Organization owners have full access to the team. |
| Lifecycle | Teams can be archived within Viva Goals, but they cannot be deleted within Viva Goals: the associated groups can be deleted in other Microsoft 365 services. | Teams can be deleted within Viva Goals. |
| Making goals content private to team members | OKRs and related content can be restricted to only team members by setting the team to Private. | This capability does not exist for classic teams. |

## Capabilities

### Permission to create teams

Permission to create teams: Organization owners can control who can create teams within their organization with the help of permissions by visiting Admin -> General -> Who can create teams. By default, all members of an organization can create teams; org owner can change this to only owners (or) specific people or Groups (only mail enabled security groups are allowed)

### Roles within teams

A team has team owner and member role. Team owners have the permission to access the team OKRs, modify team creation permissions, create dashboards. Members can be assigned OKRs and Projects and if they have necessary permissions, they can create OKRs and Projects too.

### Membership of an organization vs team

All Viva Goals teams are hosted within an organization. Whenever a member or group is added to a team, they also get added to the organization that is hosting it.

### Parent vs sub-teams

You can select another team as your parent team in team creation and settings if you want to follow that team's OKR check-in rhythm (or) use that team's OKR creation permissions (or) show up under that team in Team navigation. Typically, your parent team is your organizationally higher up team such as Department/Division and both your teams follow the same rhythm.

### Lifecycle of teams

Teams can be archived and deleted. We recommend you archive teams that are no longer in service so that the collection of teams stay relevant for use. Once a team is archived, you can no longer create OKRs and initiatives under that team, and no users are a part of the team. Additionally, any sub teams become independent teams in Viva Goals. All OKRs that were previously assigned to the archived teams will still be accessible for actions to be performed on them, such as check-ins. Even though you won't be able to see the archived team under All Teams now, you can see the assigned OKRs by expanding the parent OKRs that they're aligned to. You can also view those OKRs/initiatives in the Explorer by applying the type filter and selecting the archived team name.

Activities related to the archived team are halted, including assigning team members and team-level notifications. To resume these activities, you would need to restore the team.
