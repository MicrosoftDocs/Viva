---
ms.date: 03/18/2024
title: Create and manage native teams in Viva Goals
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
description: "Learn how to create and manage native teams within Viva Goals."
---

# Create and manage native teams in Viva Goals

Native teams are teams created within Viva Goals and not connected to a Microsoft 365 group; they can only be managed in Viva Goals. Organization owners have ownership access to these teams.

## Create a native team in an organization

By default, any member of an organization can create a team in that org. That said, organization owners can restrict team creation permissions to owners and admins or specific users and groups.

1. Go to **All Teams** > **Create team** > **Create Teams from scratch** or **Admin** > **Teams** > **Add Team** > **Create Teams from scratch**.

1. Fill out the following details in the dialog:

    - Team Name: Enter a team name.

    - Team owner: Search for and designate a team owner from the Team Owner dropdown list.

    - If this team is a subteam, division, or department, select the parent team. (Optional)

    - Add any details you deem necessary. (Optional)

1. Select **Create team**.

### About parent teams

If you want to give your team a parent team, all of the following apply:

- Your team will default to the parent team's OKR settings, such as check-in frequency and creation permissions.

- Your team will show up as a subteam under your parent team. If you want to view your parent team's other subteams, go to the parent team's page and select the sub-teams tab.

- You can't select a restricted Microsoft 365 group-backed team as a parent team.

## Create native teams in bulk

You can create native teams in bulk using an Excel template.

1. Go to **All Teams** > **Create Team** or **Admin** > **Teams** > **Add Team**.

1. Select the dropdown next to **Create Team** or **Add Team** and choose **Import Teams**.

1. Download the Excel template from the resulting window.

1. Update the Excel template with the following information about the teams you're importing.

    - Team name – Give your team a name that doesn't already exist in Viva Goals.

    - Team owner – Enter the primary email of the user who will be the team's owner.

    - Parent team – Add the name of the team you'd like to be the parent team for the team you're creating. (Optional)

    - Group  ID – Add up to five Microsoft Entra groups as members for this team. Mail-enabled security groups, mail-enabled distribution groups, and nested groups are supported. Other security groups and Microsoft 365 groups aren't supported. (Optional)

        **Note:** You can find a group's ID by navigating to the group's page in [portal.azure.com](https://portal.azure.com/) and checking under **Properties**.

1. Go back to the **Import teams** page in Viva Goals and upload the completed Excel doc. The page will display a snapshot of the information for the teams you're importing.

1. Select **Create Teams** to begin the import process and view the import tracking page.

1. The import can take up to 30 minutes depending on the number of teams being imported. Feel free to close the window during this process; you can always check the import's progress by going to **Account settings** > **Preferences** > **My imports** > **My team imports**.

1. Once the import is complete, you'll receive an email notification. You can return to the import tracking page to see which teams were created and which teams weren't. If you want to know why some teams weren't created, download the import report.

1. You can view the created teams by navigating to **All Teams** or by going to **Admin** > **Teams**.

## Add members to a native team

For both native teams and teams connected to Microsoft 365 groups, team owners can add members from within Viva Goals.

1. Go to the team's OKRs page and select the three dots (**...**) at the top right, then choose **Team members**.

1. Select **Add members**.

1. Use the search box to search for and select individual users or groups to add. Mail-enabled security groups, mali-enabled distribution groups, and Microsoft 365 groups are supported.  

1. Select **Add members**.

1. There are three possibilities for what will happen next:

    - If a user or group selected is already a part of the organization, it will be added to the team instantly.  

    - If a user or group selected is not yet a member of the organization but you have the permissions necessary to add members to the org, that user or group will be added to the org and the team.

    - If a user or group selected is not yet a member of the organization and you do not have the permissions necessary to add members to the org, that user or group will not be added to the team. Please contact the organization administrator so you can get the necessary permissions and try the above steps again.

You can use the above steps to add users who are not yet a part of Viva Goals; just make sure the **Send email notification to the added members** checkbox is selected while you're adding members. This will send them an invitation to join your team in Viva Goals.

> [!NOTE]
> When you set up a team, it's useful to add a second team owner to ensure that team management isn't dependent on a single user. You can also add multiple team owners as necessary.

## Make a team member an owner or basic member

1. Go to the team's OKRs page and select the three dots (**...**) at the top right, then choose **Team members**.

1. Each team member listed has a dropdown in the **Role** column. Select this dropdown, then choose **Owner** or **Member** depending on the role you want the team member to have.

## Remove a member from a native team

You can remove team members from teams. Individual users removed from a team lose membership access to that team but remain part of their organization.

1. Go to the team's OKRs page and select the three dots (**...**) at the top right, then choose **Team members**.

1. Each team member listed has a dropdown in the **Role** column. Select the **X** next to that team member's dropdown.

1. Select **Remove** in the resulting dialog.

## Delete, archive, or restore a native team

Org owners and team owners have the authority to manage their teams, which includes deciding what to do when those teams are dissolved or retired due to organizational changes. When that happens, there are two options: deleting the team or archiving the team. A team can only be deleted from within Viva Goals if it has no OKRs or initiatives assigned to it. Otherwise, the team can be archived.

### Delete a native team

To delete a native team from within Viva Goals, follow these steps:

If you are an org owner or administrator:

1. Go to **Admin** > **Teams**.

1. For the team you want to delete, select **Actions** (**...**) > **Delete**.

If you are a team owner:

1. Go to the team's OKRs page.

1. Select the three dots (**...**) at the top right, then choose **Delete this team**.

> [!NOTE]
> If you want to delete a team but can't because it has OKR content, you can remove the OKRs or assign them to other teams first.

### Archive a native team

We recommend you archive teams that are no longer in service so that the collection of teams stay relevant for use. Once a team is archived, you can no longer create OKRs and initiatives under that team, and no users are a part of the team. Furthermore, any subteams become independent teams in Viva Goals. It will still be possible to perform actions (such as check-ins) on OKRs previously assigned to the archived team.

Even though you won't be able to see the archived team under All Teams now, you'll be able to see the assigned OKRs by expanding the parent OKRs they're aligned to. You can also view those OKRs and initiatives in the Explorer by applying the type filter and selecting the archived team's name.

Once a team has been archived, it's marked as **Archived** on the **Teams** tab in the admin dashboard. It won't be visible anywhere else. Any objectives that were owned by this team will remain unchanged, but you can't assign new objectives to the team.

Activities related to the archived team will be halted, including the assigning of team members and any team-level notifications. To resume these activities, you would need to [restore the team](#restore-a-native-team).

To archive a team as an org owner, org administrator, or team owner:

1. Go to the team's OKRs page.

1. Select the three dots (**...**) at the top right, then choose **Archive this team**.

If you are an org owner or administrator, you can do the following instead:

1. Go to **Admin** > **Teams**.

1. For the team you want to archive, select **Actions** (**...**) > **Archive**.

## Restore a native team

Archiving a team isn't permanent. To restore an archived team:

1. Go to **Admin** > **Teams**.

1. For the team you want to restore, select **Actions** (**...**) > **Restore**.

Alternately:

1. Go to the team's OKRs page.

1. Select the three dots (**...**) at the top right, then choose **Restore this team**.
