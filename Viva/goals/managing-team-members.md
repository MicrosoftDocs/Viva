---
ms.date: 05/22/2023
title: Managing Viva Goals members 
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
- Strat_SP_modern
- M365-collaboration
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Learn how to manage users with the members’and team members pages in Viva Goals."
---

# Overview

Viva Goals allows organization owner admins and team owner admins to view and manage members in their organization and/or teams. From these pages, you can view all the groups and individuals that have been added to an organization and/or team. You can also add or remove members (individuals and groups) and assign permissions from these pages. 

## Prerequisites and things to note 

[**Role and Permission**](roles-permissions-in-viva-goals.md): This page can be accessed by organization owners, organization admins, team owners, team admins and team members.  

**Definitions:**

- **Organizations**: Typically, an organization in Viva Goals represents the company or business unit or a large department within the company.  

- **Teams**: A Team exists within an organization in Viva Goals. It's a group of users working towards a common set of team OKRs.

## Managing members for an Organization

You can view all members of an organization (individual members and groups) by navigating to Admin (in left nav bar) and selecting the Members tab. 

## How to view all members in Viva Goals organization: 

- The members’ page lists both individual members and groups in a single list. 

- If you want to view all the members of a group that has been added to the organization, hover on the group name on this page. This opens the group page that lists all the members of the group for Distribution groups and Microsoft 365 groups.  

- If you want to search for a specific member who has been added to the organization either individually or as part of a group, you can search for the member in the search bar at the top of the page. 

    - When you search for a user, for example, if you search for John, the search tool returns all results for John from Azure Active Directory (individuals and groups). This includes members and groups who are part of the organization and those who aren't.  

    - If you want to know if a user or group listed in the search result is part of the organization or not, select on the more options button (Three dots). The dropdown indicates whether the user or group is a member or a nonmember. 

        - If the user/group is already part of the organization, you'll be able to take more actions pertaining to the user/group.  

        - If the user/group isn't part of the organization, you'll be able to add the user/group to the organization, provided you have the permission to do so.  

## How to manage members/groups who are part of the organization:

### Deactivate a member from the organization:

- Search for the user from the search field in the members’ page 

- Select on the more options button next to the user in the search results. Select on deactivate. 

    - When a member is deactivated from Viva Goals, that member continues to be deactivated even if they are added to another group that is part of the organization. You'll have to manually reactivate this member to resume their access to the organization. 

    - To reactivate a user, you can search for the user, select on more options, and then select on reactivate. 

- Alternately, a member who was added to an organization as part of a group can be deactivated by removing this user from the group in Azure Active Directory.  

> [!NOTE]
> If the user is not part of the organization, clicking on more options button in the search results will only provide the option to add this user to the organization. 

### Delete a member from the organization: 

- Search for the user from the search field in the members’ page 

- Select on the more options button next to the user in the search results. Select on Delete. 

    - Deleting a user from the organization removes their user record from the organization database.  

    - If the user is added again to Viva Goals either individually or via a group, then the system creates a new user record for this user. This user record is delinked from the old user record.  

- It's recommended that the delete member feature is only used when a member has left the company altogether.  

> [!NOTE]
>  If the user is not part of the organization, clicking on more options button in the search results will only provide the option to add this user to the organization. 

### Remove a group that’s part of the organization from Microsoft Azure Active Directory 

- When a group that has been added to an Org is deleted from Azure AD, the users of the group cease to have access to the organization. 

### Change the role of a member in the organization: 

- Search for the user from the search field in the members’ page 

- Select on the more options button next to the user in the search results.  

    - If the user is part of the organization, the more options drop down will list two options: 
        -  Make admin/remove admin 

        - Make observer/regular user 

    - Choose the relevant role for the user. 

> [!NOTE]
> If the user is not part of the organization, clicking on more options button in the search results will only provide the option to add this user to the organization. 

### View or export a member’s profile: 

- Search for the user from the search field in the members’ page 

- Select on the more options button next to the user in the search results.  

    - If the user is part of the organization, the more options button lists two options – View profile and export. 

        - Select on ‘view profile’ to view the user’s profile information 

        - Select on ‘export’ to export the user’s profile information 

> [!NOTE]
> If the user is not part of the organization, clicking on more options button in the search results will only provide the option to add this user to the organization. 

### Remove a group from the organization: 

- Search for the group from the search field in the members’ page 

- Select on the more options button next to the group in the search results.  

    - If the group is part of the organization, the more option button lists the option to remove the group. Clicking on it removes the group from the organization. When removing a group, the admin sees a warning stating “Removing a group from the organization will also remove the group from all the teams as well.” 

> [!NOTE]
>  If the user is not part of the organization, clicking on more options button in the search results will only provide the option to add this group to the organization. 

## Managing members for a team

You can view all members of a team (individual members and groups) by navigating to the team page and selecting team members from the options on the top right corner of the page. 

## How to view all members in Viva Goals team: 

- The members page lists members in two sections: 

    - All the groups that have been added to the team. 

    - All members that have been added to the team in an individual capacity. 

- If you want to search for a specific member who has been added to the team either individually or as part of a group, you can search for the member in the search bar at the top of the page. 

## How to search for a member from the team member’s page: 

You can search for a member who is part of the team from the search bar at the top of the member’s page. 

- When you search for a user, for example, if you search for John, the search tool returns all results for John from Azure AD (individuals and groups). This includes members who are part of the team and those who aren't.  

- You can select on the more options button next to a particular search result to know whether that user/group is part of the team or not.  

    - If the user/group is already part of the team, you'll be able to take more actions pertaining to the user/group.  

    - If the user/group isn't part of the team, you'll be able to add the user/group to the team, provided you have the permission to add a member to the organization. 

## How to manage members who are part of the team: 

### Remove a member from the team: 

- Search for the user from the search field in the members’ page 

- Select on the more options button next to the user in the search results.  

    - If the user was added to the team in an individual capacity, the more options drop down will list the remove button. Clicking it removes the user from the team. Note that removing a member from a team doesn't remove the member from the organization. To remove a member from the organization, an organization owner or admin have to deactivate them or delete them from the Admin >> members page. 

    - If the user was added to the team as part of a group, you won't see the remove option. You'll have to remove this user from the group in Azure AD to remove this user from the team 

> [!NOTE]
> If the user is not part of the team, clicking on more options button in the search results will only provide the option to add this user to the team. If this user is not part of the organization itself, then adding this user to the team will also add them to the organization. 

### Change the role of a member in the team: 

- Search for the user from the search field in the team members’ page 

- Select on the more options button next to the user in the search results.  

    - If the user is part of the team, the more options drop down will list the option to “Make team admin/remove team admin” 

    - Choose the relevant role for the user. 

> [!NOTE]
> If the user is not part of the team, clicking on more options button in the search results will only provide the option to add this user to the team. If this user is not part of the organization itself, then adding this user to the team will also add them to the organization. 

### Remove a group from the team: 

- Search for the group from the search field in the team members’ page 

- Select on the more options button next to the group in the search results.  

    - If the group is part of the team, the more option button lists the option to remove the group. Clicking on it removes the group from the team. Note that removing a group from the team doesn't remove the group from the organization as well. To do this, an Org owner/admin will have to remove the organization from the Admin>Members page. While removing the group from the team. The admin gets a warning saying “This group continues to be part of the Org.” 

> [!NOTE]
> If the user is not part of the team, clicking on more options button in the search results will only provide the option to add this user to the team. If this user is not part of the organization itself, then adding this user to the team will also add them to the organization. 

### Delete a group that’s part of the organization from Azure AD:

- When a group that has been added to a team is deleted from Azure AD, Viva Goals listens for such signals by running a scan once a day. Upon learning that this group has been deleted in Azure AD, the users of the group cease to have access to the team. 

## FAQ (Frequently Asked Questions)

1. **How do I remove organization owners/admins from the organization?**
    1. An organization owner can only be removed by another Organization owner. They have to first reassign the organization owner role to another individual before deactivating or deleting the existing team owner. 
    
    Organization admins can be removed by organization owner/. They can remove an organization admin by clicking on the tree dots next to the member and clicking on deactivate/delete. 
    
    When a user is assigned the role of an organization owner or admin, they start being listed in the individual users section. Even if an admin deactivates or deletes the group that an organization admin belonged to, the admin doesn't get removed. They have to be removed manually one by one. 

2. **What attributes can I see for the listed users and groups?**
    1. For the individuals and groups that are part of the organization, you'll see the following attributes 
        1. Name & designation 
        1. Email 
        1. Member type (Regular/observer for individual members, Security/Distribution for groups) 
        1. Role (Admin, Member for individuals. Groups are listed as Members by default) 

3. **What happens to a member’s OKRs, projects and check-ins when they are deactivated from the organization?**
    1. When a member is deactivated from the organization, any OKRs or projects they owned, or checkins they made are retained as is. 

4. **What happens to a member’s OKRs, projects and check-ins when they are deleted from the organization?**
    1. When a member is deleted from an organization, any OKRs or projects they owned, or check-ins they made are retained as is. However, the member’s name is deleted and replaced with “Deleted user”. 

5. **How do I export users that are part of my organization?**
    1. You can only export information about those users in your organization who were added in an individual capacity. You won't be able to export the list of users who are part of a group. You can, however, export the list of groups that are part of your organization. 
        1. To export the list of individual users and groups, select on the “Export button on the top right of the members’ page. 
        1. Viva Goals will send you the list of individuals and groups in your organization in the .xls format to your registered email. 

6. **Can I filter users in my organization in any way?**
    1. You can filter users in your organization based on their role and their status in the organization. This filter can be applied to the list of individual users and users who are part of a group.  

7. **How do I remove team owners/admins from the team?**
    1. Team owners can only be removed by the Org owner/admins and other team owners. They have to first reassign the team owner role to another individual before removing the existing team owner. 
    
    Team admins can be removed by organization owner/admins and team owners and other team admins. They can remove a team admin by clicking on More options button next to the member and clicking on remove. 
    
    When a user is assigned the role of a team owner or a team admin, they start being listed in the individual users section. Even if an admin removes the group that a team admin belonged to, the team admin doesn't get removed. They have to be removed manually one by one. 

8. **What are groups in AAD?**
    1. Azure Active Directory (Azure AD) provides several ways to manage access to resources, applications, and tasks. With Azure AD groups, you can grant access and permissions to a group of users instead of for each individual user. You can find more information on groups [here](/azure/active-directory/fundamentals/concept-learn-about-groups). 