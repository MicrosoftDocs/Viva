---
ms.date: 04/05/2022
title: Create and edit teams and subteams
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
search.appverid:
- MET150
description: "Learn how to set up teams and subteams, from divisions to small functional units"
---

# Create and edit teams 

Viva Goals supports multiple levels of hierarchy, from department level down to individual teams and functional units. To achieve this setup, you can use the teams and subteams functionality.

## How to create teams 

1. To create a team, go to **All Teams** > **Create a new team** or alternatively, **Admin** > **Teams** > **Add Team**.

    :::image type="content" source="../media/goals/2/22/a.jpg" alt-text="Screenshot showing where you create a team." lightbox="../media/goals/2/22/a.jpg":::
   
2. In the dialog box that follows, follow these steps:

   - Enter a team name.
   - Designate a team owner from the **Team Owner** dropdown list.
   - If this team is a subteam, division, or department, select a primary team.
   - Enter a team type and more details, if necessary.

In this example, we set up a sales territory "Central Territory" (from the **Team Name** dropdown list), under the overarching Sales Department (from the **Parent Team: (Optional)** dropdown list).

:::image type="content" source="../media/goals/2/22/b.jpg" alt-text="Screenshot showing menu options when you create a team." lightbox="../media/goals/2/22/b.jpg":::

To view all subteams, go to the **Parent Team** page and select the **Sub-teams** tab. Using subteams, you can easily replicate the structure of your organization and view how each department, division, and team contribute to organization goals.

## How to create teams in bulk

1. To import and create multiple teams in Viva Goals at once, go to **All Teams > Create Team** or alternatively, **Admin > Teams > Add Team.**
1. Select on the drop-down next to **Create Team** or **Add Team** and select import teams. 
    
    :::image type="content" source="../media/goals/bulk-teams/bulk-teams-01.png" alt-text="Screenshot of the import teams window." lightbox="../media/goals/bulk-teams/bulk-teams-01.png":::

1. In the window that opens, follow the following steps: 
    1. Download the excel template. 
    1. Update the excel template with information about all the teams that need to be imported. You can update the following information: 
        1. **Team name** – This is a mandatory field. It has to be a unique name. This team shouldn't already exist in Viva Goals. 
        1. **Team owner** – This is a mandatory field. Enter the primary email of the user who is the owner of the team. 
        1. **Team admins** – This is an optional field. You can add up to five admins to the team. Enter the primary email of the users you want to be the team’s admin. 
        1. **Parent team** – This is an optional field. Add the name of the team that needs to be the parent team for this team. Ensure that you're adding the correct name here. 
        1. **Group ID** – This is an optional field. You can add up to five Azure AD groups as members for this team. The groups that are supported include Mail enabled security groups, Mail enabled distribution groups and nested groups. Nonmail enabled security groups and Microsoft 365 groups aren't supported. 
            1.**NOTE:**You can find a Group’s ID by navigating to the group’s page in portal.azure.com and checking in properties.
    1. Once you have filled the above information for all the teams that you want to create, go back to the import teams page in Viva Goals and upload this excel template. 
1. The page displays a snapshot of the teams’ information you have uploaded. Select on ‘Create Teams’ to start the import process. 
1. You'll be taken to the import tracking page. The import can take up to 30 minutes depending on the number of teams to be imported. You can close the window while the import is in progress. You can always track the progress of the import by navigating to **Account settings > Preferences > My imports > My team imports.** 
    
    :::image type="content" source="../media/goals/bulk-teams/bulk-teams-02.png" alt-text="Screenshot of preferences window for bulk importing teams." lightbox="../media/goals/bulk-teams/bulk-teams-02.png":::

1. Once the import is complete, you'll receive an email notification. You can come back to the import tracking page to check how man teams got created and how many teams didn't.  
1. Download the import report to understand why some of teams weren't created. 
1. You can view the created teams by navigating to All Teams or Admin > Teams. 

## How to add members to a team 

Team owners and administrators can set up their team by adding team members.

- To add existing Viva Goals users as team members, follow these steps:

   1. Go to the **Team OKR** page.
   2.  Select the **Team Members** tab.
   3. Select the **Add Members** button.
   4. Start typing the name or email of the existing Viva Goals user. Autocomplete will suggest matching users.
   5. Select the name or email of the user, which is returned as a result.

        :::image type="content" source="../media/goals/2/22/c.jpg" alt-text="Screenshot showing where you add members to a team." lightbox="../media/goals/2/22/c.jpg":::
   
   6. Select the **Add Members** button. The user is added to the team as a member.

- To add people who aren't currently in Viva Goals, you can use the same dialog box. Make sure that the **Send invitations to users who are not in Viva Goals** checkbox is selected.

    :::image type="content" source="../media/goals/2/22/d.jpg" alt-text="Screenshot showing the dialog box where you add new members." lightbox="../media/goals/2/22/d.jpg":::

When you set up a team, it's useful to add a second team administrator to make sure that the team-setup process isn't dependent on one person.

To assign team administrator permissions to a team member, follow these steps:

1. Select the **Team Members** tab. For every user listed, there's an **Actions** dropdown list in the last column.

2. Select the **Actions** dropdown list, and then select **Promote to Team Admin**.

    :::image type="content" source="../media/goals/2/22/e.jpg" alt-text="Screenshot showing where you assign permissions for team administrator." lightbox="../media/goals/2/22/e.jpg":::

## How to promote team owners and administrators

You can promote or remove any team member as a team owner or administrator from the **Admin** menu on the **Admin Dashboard** page.

### How to update team owners

1. To update the team owner, go to the **Teams** section of the **Admin** menu, select the **More Actions** menu of the relevant team, and then select **Edit**.

    :::image type="content" source="../media/goals/2/22/f.jpg" alt-text="Screenshot showing where you update team owners." lightbox="../media/goals/2/22/f.jpg":::

2. From the edit teams dialog, select the **Team Owner** dropdown menu to select and update the team owner.

3. Select **Save**.

### How to update team administrators

1. From the **Teams** section of the **Admin** menu, select the **More Actions** menu of the relevant team, and then select **Manage Members**.

    :::image type="content" source="../media/goals/2/22/g.jpg" alt-text="Screenshot showing where you update team administrators." lightbox="../media/goals/2/22/g.jpg":::

2. Select the **Action** dropdown list to the right of the person's name, and you are able to edit their member status.

   :::image type="content" source="../media/goals/2/22/h.jpg" alt-text="Screenshot showing where you promote team members to team administrators." lightbox="../media/goals/2/22/h.jpg":::
 
## How to archive and delete teams

As an Viva goals administrator, we give you support to manage your teams. Sometimes, teams are dissolved or retired due to an organizational change. In that case, you have the following two options in Viva Goals.
- Delete a team
- Archive a team

### How to delete a team

Deleting a team is permanent. Once the team is deleted, it can't be restored. Delete with caution. 

To delete a team, follow these steps:

1. Select **Admin** > **Teams** tab > **Actions**.
2. Select the **Delete** option corresponding to the team that you want to delete.

Alternately, you can navigate to the team's OKR page and delete the team from the options in the upper-right corner.

> [!NOTE]
> To delete a team from the team's OKR page, you must be an organization administrator or the team owner. Team administrators can't delete a team.

A team can only be deleted if it has no objectives assigned to it. If there are objectives assigned to the team, you can instead archive the team.

### How to archive a team 

We recommend you archive teams that are no longer in service. To archive a team, follow these steps:

1. Select **Admin** > **Teams** tab > **Actions**.
2. Select **Archive** for the team that you want to archive.

    :::image type="content" source="../media/goals/2/22/i.jpg" alt-text="Screenshot showing where you archive a team." lightbox="../media/goals/2/22/i.jpg":::
    
Alternately, you can navigate to the team's OKR page, and archive the team from the options in the upper-right corner.

Once a team has been archived, it is marked as **Archived** on the **Teams** tab in the Admin console. It won't be visible anywhere else. Any objectives that were owned by this team remains unchanged. But you can't assign new objectives to the team.

Archiving a team isn't permanent. You can restore an archived team. To restore an archived team:

1. Select **Admin** > **Teams** tab > **Actions**.
2. Select **Unarchive** for the team you want to restore.

    :::image type="content" source="../media/goals/2/22/j.jpg" alt-text="Screenshot showing where you unarchive a team." lightbox="../media/goals/2/22/j.jpg":::
    
### What happens when I archive a team?

Once a team is archived, you can no longer create OKRs and initiatives under that team, and no users are a part of the team. Additionally, any subteams become independent teams in Viva Goals. All OKRs that were previously assigned to the archived teams will still be accessible for actions to be performed on them, such as check-ins.

Even though you won't be able to see the archived team under **All Teams** now, you can see the assigned OKRs by expanding the parent OKRs that they're aligned to. You can also view those OKRs/initiatives in the Explorer by applying the type filter and selecting the archived team name.

Activities related to the archived team are halted, including assigning team members and team-level notifications. To resume these activities, you would unarchive the team. 

