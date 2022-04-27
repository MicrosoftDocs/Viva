---
title: "Roles and permissions in Viva Goals"
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: 
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
localization_priority: Priority
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Learn about the various roles and permissions in Viva Goals"
---

# Roles and permissions in Viva Goals

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## Role types in Viva Goals

In Viva Goals, a creator is a user who has created an objective. An owner is a user who has been assigned an objective. 

For example, if a Sales team member wants to suggest an objective to a Marketing team member, the Sales team member (creator) can add the objective and assign it the Marketing team member (owner). 

Viva Goals supports the following roles within an organization:

|Role  |Description  |
|---------|---------|
|Members    |    Members (the default role for everyone) can set up and manage their individual OKRs, and view all OKRs within the organization.     |
|Observers     |   Observers, as opposed to members, can't create, edit, or own OKRs. They can view all OKRs like members.      |
|Managers     |    Managers are members who own their OKRs and the OKRs of those who report to them.     |
|Team Owners     |    Team owners are members who own their team members' OKRs.     |
|Team Admins     |   Team administrators are members who can manage team members.      |
|Organization Admins     |   Organizational administrators are members who manage the setup of the organization and can manage users and teams. An organization can have more than one organization administrator.      |
|Organization Owner  |    Organizational owners manage members, teams, set up, and billing for the account. By default, they own organization-level OKRs, but organizational objectives can be owned by other members also.     |

## Permission levels on individual OKRs

The permission levels on individual OKRs are described in the following table:

:::image type="content" source="../media/goals/permission-levels-on-individual-okrs.png" alt-text="Permission levels on individual OKRs":::

## Permission levels on team OKRs

The permission levels on team OKRs are described in the following tables:

:::image type="content" source="../media/goals/permission-levels-on-team-okrs.png" alt-text="Permission levels on team OKRs":::

:::image type="content" source="../media/goals/permission-levels-on-team-okrs-2.png" alt-text="Levels of permissions on team OKRs":::

## Permissions for objectives and key results

Organization administrators and the organization owners in Viva Goals have access to all OKR permissions, for example, creating, editing, and deleting any objectives or check-ins.

### Viewing objectives and key results

One of the tenets of a successful OKR strategy is transparency; Viva Goals enables all OKRs to be viewed by all members in the organization.

:::image type="content" source="../media/goals/okrs-permissions-entities.png" alt-text="Matrix describing entities that can view all OKRs":::

### Creating objectives or key results

By default, all members in the organization can create OKRs for themselves, other members, teams, or the organization. This privilege reduces the friction in setting up OKRs and facilitates bottoms-up and lateral alignment of OKRs.  

For example, a team member can propose a team-level objective just by adding an objective of type **Team** and can assign it to the primary team manager. The manager can accept the suggestion by executing either of the following tasks:
- Doing nothing
- Changing it to an individual's objective
- Deleting it

The information regarding the entities entitled to create objectives or key results is described in the below table:

:::image type="content" source="../media/goals/creating-objectives-key-results.png" alt-text="Matrix describing the entities that can create an objective or a key result":::

### Managing objectives or key results

The privileges for each role in Viva Goals are detailed in the following table.

:::image type="content" source="../media/goals/managing-objectives-key-results.png" alt-text="Matrix describing the privileges for each role":::

Creators are by default provided with the ability to edit and delete objectives. These privileges allow them to correct any errors during creation, like an incorrect assignment.

## Check-ins

The permissions related to a check-in and the entities entitled to those permissions are described in the following table:

:::image type="content" source="../media/goals/check-ins.png" alt-text="Permissions and entities in the case of a check-in":::

While the checking-in process is largely restricted to those entities involved in the objective, Viva Goals encourages cross-team collaboration by letting anyone in the organization engage with check-ins. This extension of the privileges for a check-in to all entities is described in the following table:

:::image type="content" source="../media/goals/check-ins-entities.png" alt-text="Coverage of a check-in's privileges to all entities":::

## Administrative Privileges

All administrative privileges are restricted to members with an organization administrator or organization owner role, by default.

### User management

The user management activities and the entities to execute those activities are described in the following table:

:::image type="content" source="../media/goals/user-management.png" alt-text="User management activities and entities":::

*Available on request; [contact Microsoft support](https://help.ally.io/en/).

Viva Goals allows profile updates if the member was invited or added directly via Viva Goals. If your account has SSO enabled, a profile update should be done at the source. 

The details of entities who can update a profile are described in the following table:

:::image type="content" source="../media/goals/profile-updates-conditions.png" alt-text="Entities who can update a profile":::

### Team management

*Available on request; [contact Viva Goals support](https://help.ally.io/en/).

The activities, privileges and entities (who can avail such privileges) are described in the following table:

:::image type="content" source="../media/goals/team-management.png" alt-text="Team management-related activities, privileges, and entities":::

### Admin management

The information regarding the activities and the entities who have the privileges to execute such activities are described in the following table:

:::image type="content" source="../media/goals/admin-management.png" alt-text="The activities and entities related to admin management":::

### Other permissions

The other permissions in Viva Goals are described in the following table:

:::image type="content" source="../media/goals/other-permissions.png" alt-text="Other permissions in Viva Goals":::

## Observer user type

Viva Goals supports two kinds of accounts:
- **Regular Users**: Regular users can access all of Viva Goals' functionality, including creating, updating, and owning OKRs. They can take up additional responsibilities in Viva Goals such as an administrator, team administrator, manager, and so on.

- **Observers**: As opposed to regular users, Observers can't create, edit, or own OKRs. However, they can view all entities and OKRs like regular users.

Using Viva Goals with Observer privileges is described in the following image:

:::image type="content" source="../media/goals/using-viva-goals-as-observer.png" alt-text="Using Viva Goals as an Observer":::

### Privileges of an Observer

An Observer is entitled to the following privileges:

- **Seeing all entities' OKRs**: This privilege enables an Observer to be aware of, and aligned to, organization’s, teams’, and users’ priorities, progress, and updates.
- **Following entities**: This privilege enables an Observer to receive updates for any entities and stay updated to latest developments.
- **Liking and commenting**: This privilege enables an Observer to like and comment on OKRs, check-in, and activity feed updates to engage with leadership team.

> [!NOTE]
> Observers can’t be an OKR owner, administrator, or Team owner/administrator. However, they can be team members, managers, and can have a Manager.

### Adding users as an Observer

You can set a default user type for new users from **Admin Dashboard > Setting**. 

:::image type="content" source="../media/goals/setting-account-type-to-observer.png" alt-text="Setting Account Type for a new user to Observer":::

If the value is set to **Observer**, users will take up account type as **Observer** when added through file upload/slack or when they join without invitations (if allowed).

Users will have the option to choose between Observer and Regular privileges when inviting.

:::image type="content" source="../media/goals/inviting-people-to-assign-observer-privileges.gif" alt-text="Inviting people to assign privileges of an Observer":::

### Identifying an Observer

If the users have **Observer** tag against their names, they're an Observer. The process of identifying a person with Observer privileges is depicted in the following image:

:::image type="content" source="../media/goals/identifying-an-observer.png" alt-text="Identifying an Observer":::

If you're an administrator, you can also look at user type from **Admin Dashboard > Users > User Type column**, as depicted in the following image:

:::image type="content" source="../media/goals/checking-for-observer-setting.png" alt-text="Alternative method of identifying an entity with Observer privileges":::

### Changing account type of users

Administrators can change the user type from **Observer** to **Regular** and from **Regular** to **Observer** through **Admin Dashboard > Users Tab > User listing > Three dot Menu**, as shown in image below:

:::image type="content" source="../media/goals/changing-account-type-from-observer-to-regular-vice-versa.gif" alt-text="Changing account type from Observer to Regular and vice versa":::

## Inviting other users as Observers

An Observer can invite others as Observers if the Invite Policy in **Admin > Settings** is set to **Anyone in the organization**.
