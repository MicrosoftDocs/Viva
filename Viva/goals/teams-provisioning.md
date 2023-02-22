---
ms.date: 02/21/2023
title: Teams provisioning using groups 
ms.reviewer: 
ms.author: rasanders
author: rasanders
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
search.appverid:
- MET150
description: "Add members to their respective teams using AAD Group with Viva Goals"
---

# Teams provisioning overview

Viva Goals allows team owners and team admins to add members to their respective teams using AAD Groups. This feature allows you to add a large number of members to your teams quickly and with ease.  

To log in to Viva Goals, visit: https://goals.microsoft.com/

## Prerequisites and things to note 

**Max number of groups: You can add up to 5 groups to a team as members.** 

Group types: You can add mail enabled security groups, mail enabled nested groups, distribution lists and dynamic AAD groups to your teams as members. M365 Groups are not supported for this feature at this time. 

**Role and Permission:** 

- Team owners, team admins and team members can add team members using groups 
- If the user adding groups to a team does not have permission to add members to an org, she can only add those groups that have already been added to the Org. 

## How to Add Groups to Viva Goals teams

**During Team Creation:**

1. Go to Teams page by clicking on ‘Teams’ in the left navigation bar. 
1. Click on ‘Create Team’ on the top right corner of the page 
1. In the create team pop-up: 
    1. Enter team name 
    1. Search and select a user from AAD to be the team owner.  
    1. If required, select the parent team from the drop down. 
    1. If required, add a description for the team. 
    1. Click on Create. 
1. You will see a ‘Team created successfully’ page. On clicking next, you will be taken to the add members’ page. 
1. In the team members’ field, search for the groups or individual members you want to add to the team. 

> [!NOTE]
> You can select up to 20 entries to add to the team in a single session. This can be a combination of groups and individuals. However, you can only add up to 5 groups to a team.

6. Click on ‘Add’ to add these groups or individual members to the team. 

**From Team Members page:**

1. Go to Team Members’ page. Click on Add Members on the top right corner of the page. 
1. In the team members’ field, search for the groups or individual members you want to add to the team. 

> [!NOTE]
> You can select up to 20 entries to add to the team in a single session. This can be a combination of groups and individuals. However, you can only add up to 5 groups to a team. 

3. Click on ‘Add’ to add these groups or individual members to the team.

## FAQs (Frequently Asked Questions)

1. **What types of groups can be added as members to teams?**
    1. You can add You can add mail enabled security groups, mail enabled nested groups, distribution lists and dynamic AAD groups to your teams as members.  
    1. M365 Groups are not supported for this feature at this time. 

2. **Who can add groups to a team?**
    1. Organisation Owners 
    1. Organisation Admins 
    1. Team Owners 
    1. Team Admins 
    1. Team Members 

3. **Any limitations that users need to be aware of?**
    1. If you do not have the permission to add new members to the organization, you will only be able to add members and groups to a team that are already part of the organization. If you choose individuals or groups that are not part of the organization, you will see a message stating that these individuals or groups have not been added. 
    1. You can add up to 5 groups to any team. If you try adding more than 5 groups, the system will give you an error message informing you that the groups limit has been reached.  
    1. Any groups that are added to a team will also get added to the organisation. 

4. **What happens when I add groups with users who do not have a license to access Viva Goals?**
    1. If you add a group that contains a subset of members who do not have a license to access Viva Goals, those users will not be able to log in to Viva Goals and hence will not be able to gain access to the teams.

5. **What happens when I remove a group from a team?**
    1. When you remove a group from a team, all members of the group will lose access to the team. However, this group will continue to be a part of the organization. Thus, the members of the group will continue to have access to the organization.

6. **What happens when I remove a group, that has been added to a team, from the organization?**
    1. When you remove a group, that has been added to a team, from the organization, the members of that group will lose access to this team, any other teams where this group was added, as well as the organization itself. 