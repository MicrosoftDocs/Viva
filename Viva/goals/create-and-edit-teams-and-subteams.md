---
title: Create and edit teams and subteams
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
description: "Learn how to set up teams and subteams, from divisions to small functional units"
---

# Create and edit teams and subteams

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Viva Goals supports multiple levels of hierarchy, from department level all the way down to individual teams and functional units. To achieve this setup, you can use the teams and subteams functionality.

## Creating teams

1. Create a team by choosing **All Teams > Create a new team** or alternatively, **Admin > Teams > Add Team**.

   :::image type="content" source="../media/goals/navigation.png" alt-text="Process of creating a team":::
   
2. In the dialog box that follows, perform the following steps:
    1. Enter a team name.
    1. Designate a team owner from the **Team Owner** dropdown list.
    1. If this team is a subteam, division, or department, select a primary team.
    1. Enter a team type and more details, if necessary.

   In this example, we'll set up a sales territory "Central Territory" (from the **Team Name** dropdown list), under the over-arching Sales Department (from the **Parent Team: (Optional)** dropdown list).

   :::image type="content" source="../media/goals/setting-up-a-team.png" alt-text="Setting up a team":::

To view all subteams, navigate to the **Parent Team** page and select the **Sub-teams** tab. Using subteams, you can easily replicate the structure of your organization and view how each department, division, and team contribute to organization goals.

In our sales example, we can view the status of all our sales territories at a glance and also view how they contribute to the Sales Department’s over-arching goals.

:::image type="content" source="../media/goals/sales-territories-contribution.png" alt-text="Sales territories contribution":::

## Promoting to team owners and administrators

You can promote or remove any team member as a team owner or administrator in the **Admin** menu item of the **Admin Dashboard** page.

### Updating team owners

1. To update the team owner, go to the **Teams** section of the **Admin** menu, click **...** and select **Edit**.

:::image type="content" source="../media/goals/updating-team-owner.png" alt-text="Updating the team owner details":::

1. From the edit teams pop-up, click on the Team Owner dropdown menu to select and update the team owner.

1. Click **Save**.

### Updating team administrators

1. From the **Teams** section of the **Admin** menu, click **...** and select **Manage Members**.

   :::image type="content" source="../media/goals/team-admin.png" alt-text="Team admin":::

1. Select the **Action** dropdown list to the right of their name and you'll be able to edit their member status.

   :::image type="content" source="../media/goals/editing-team-member-status.png" alt-text="Promoting a team member to the team administrator role":::

   :::image type="content" source="../media/goals/removing-team-admin.png" alt-text="Removing a team administrator from the role":::
   

## Setting up a team

Team owners/administrators can set up their team by adding team members.

To add existing Viva Goals users as team members, perform the following steps:

1. Navigate to the **Team OKR** page.
1. Select the **Team Members** tab.
1. Select the **Add Members** button.
1. Start typing the name or email of the existing Viva Goals user. The auto-complete will suggest the matching users.
1. Select the name or email of the user, which is returned as a result.

   :::image type="content" source="../media/goals/add-members-to-design.png" alt-text="The page to search users":::
   
1. Select the **Add Members** button. The user is added to the team as a member.

To add people who are currently not in Viva Goals, you can use the same dialog box. Ensure the **Send invitations to users who are not in Viva Goals** checkbox is checked.

:::image type="content" source="../media/goals/sending-invitation-to-non-viva-goals-users.png" alt-text="Option to send invitation to non-Viva Goals users":::

As part of setting up a team, it is useful to have another team administrator to ensure that the team setup process is not dependent on one person.

To assign permissions of a team administrator to a team member, perform the following steps:

1. Select **Team Members** tab

   For every user listed, there is an **Actions** dropdown list in the last column.

1. Select the **Actions** dropdown list and select **Promote to Team Admin**.

   :::image type="content" source="../media/goals/making-team-member-as-team-admin.png" alt-text="Promoting a team member to team administrator":::
   
## Archive and delete teams

As an Viva goals administrator, we give you support to manage your teams. Sometimes, teams are dissolved or due to an organizational change, they're retired. If so, we give you the following two options in Viva Goals 
- [Deleting a team](#deleting-a-team)
- [Archiving a team](#archiving-a-team)

### Deleting a team

Deleting a team is an option whose functionality is permanent in nature; once the team has been deleted, it can't be restored. Delete with caution. 

To delete a team, perform the following steps:

1. Select **Admin > Teams tab > Actions**.
1. Select **Delete** corresponding to the team that you want to delete.

   :::image type="content" source="../media/goals/deleting-a-team.png" alt-text="Deleting a team":::

Alternately, you can navigate to the team's OKR page, and delete the team from the options on the top-right corner.

> [!NOTE]
> *To delete a team from the team's OKR page, you need to be an organization administrator or the team owner. Team adminsistrators cannot delete a team*.

A team can only be deleted if it has no objectives assigned to it. If you have objectives assigned to the team, a better alternative is to archive the team.

### Archiving a team

Archiving a team is what we recommend you to use for teams that are no longer in service. You can archive a team by navigating to the **Admin > Teams  > Actions > Archive** against a specific team you want to archive.

To delete a team, perform the following steps:

1. Select **Admin > Teams tab > Actions**.
1. Select **Archive** corresponding to the team that you want to archive.

   :::image type="content" source="../media/goals/archiving-a-team.png" alt-text="Archiving a team":::

Alternately, you can navigate to the team's OKR page, and archive the team from the options on the top-right corner.

Once a team has been archived, it will be marked as **Archived** under the **Teams** tab within the Admin console, and won't be visible anywhere else. Any objectives that were owned by this team will remain in the same state; however, you will not be able to assign new objectives to this team.

Archiving a team is an option with a functionality that's not permanent in nature; you can restore an archived team.

To restore an archived team, perform the following steps:

1. Select **Admin > Teams tab > Actions**.
1. Select **Unarchive** corresponding to the team you want to restore.

   :::image type="content" source="../media/goals/archived-tag-display-for-a-team.png" alt-text="The display of the Archived tag for a team":::
   
### What happens when I archive a team?

Once a team is archived, you'll no longer be able to create OKRs/projects under that team and users will no longer be a part of the team. Additionally, any subteams will then become independent teams in Viva Goals. All OKRs that were previously assigned to the archived teams will still be accessible for actions to be performed on them, such as, check-ins.

Even though you won't be able to see the team under **All Teams** now, you can see the assigned OKRs on expanding the parent OKRs they’re aligned to. You'll also be able to view these OKRs/projects in the Explorer by applying the type filter and selecting the archived team name.

However, the activities related to the specific team will be halted, for example, assigning team members, team-level notifications, and so on, which can easily be resumed at any point by unarchiving the team, if necessary.
