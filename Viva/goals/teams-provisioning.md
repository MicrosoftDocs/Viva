---
ms.date: 02/21/2023
title: Teams provisioning using groups 
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
search.appverid:
- MET150
description: "Add members to their respective teams using Microsoft Entra group with Viva Goals"
---

# Teams provisioning overview

Viva Goals allows team owners and team admins to add members to their respective teams using Microsoft Entra groups. This feature gives the ability to add many members to a team quickly and easily.

Admins and owners can add up to five groups to a team as members. For example, admins and owners can add mail enabled security groups, mail enabled nested groups, distribution lists, and dynamic Microsoft Entra groups to teams as members. Currently, Microsoft 365 Groups aren't supported for this feature.   For more information, see the [FAQ section](/viva/goals/teams-provisioning#faqs-frequently-asked-questions).

## How to add groups to Viva Goals teams
Members can be added to teams as the team is created or after the team is created by adding members.

**Team creation**

1. Go to the Teams page by clicking ‘Teams’ in the left navigation bar.
1. Select ‘Create Team’ on the top right corner of the page.
1. In the Create team pop-up:
    1. Enter team name.
    1. Search and select a user from Microsoft Entra ID to be the team owner.  
    1. If required, select the parent team from the drop-down.
    1. If required, add a description for the team.
    1. Select Create.
1. The ‘Team created successfully’ page appears. When the user selects Next, they're taken to the add members page.
1. In the team members’ field, search for the groups or individual members you want to add to the team.
6. Select ‘Add’ to add these groups or individual members to the team.


**Team Members page**

1. Go to Team Members’ page. Select Add Members on the top right corner of the page.
1. In the team members’ field, search for the groups or individual members to add to the team.
1. Select ‘Add’ to add these groups or individual members to the team.

> [!NOTE]
> Admins and owners can select up to 20 entries to add to the team in a single session. This can be a combination of groups and individuals. However, only up to five groups can be added to a team.

## FAQs (Frequently Asked Questions)

1. **What types of groups can be added as members to teams?**
    1. Mail enabled security groups, mail enabled nested groups, distribution lists and dynamic Microsoft Entra groups can be added as members.  
    1. At this time, Microsoft 365 Groups aren't supported for this feature.

2. **Who can add groups to a team?**
    1. Organization Owners
    1. Organization Admins
    1. Team Owners
    1. Team Admins
    1. Team Members

3. **What are some common limitations I should be aware of?**
    1. Without the permission to add new members to the organization, owners and admins are only able to add members and groups to a team that are already part of the organization. If individuals or groups that aren't part of the organization are chosen, the user receives an error message stating that these individuals or groups haven't been added.
    1. Admins and owners can add five groups to any team. If the user tries adding more than five groups, the system gives an error message that the group limit is reached.
    1. Any groups that added to a team get added to the organization.

4. **What happens when I add groups with users who do not have a license to access Viva Goals?**
    1. If a user adds a group that contains a subset of members who don't have a license to access Viva Goals, those users won't be able to sign in to Viva Goals. They won't be able to gain access to the teams.

5. **What happens when I remove a group from a team?**
    1. When a group is removed from a team, all members of the group lose access to the team. However, this group continues to be a part of the organization and members of the group continue to have access to the organization. 

6. **What happens when I remove a group, that has been added to a team, from the organization?**
    1. When a group that is added to a team is removed from the organization, the members of that group lose access to this team and any other teams where this group was added and the organization itself.
