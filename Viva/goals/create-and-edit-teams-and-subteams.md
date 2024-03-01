---
ms.date: 02/28/2024
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
description: "Learn how to set up teams and subteams, from divisions to small functional units"
---

# Create and manage native teams in Viva Goals

Native teams are teams created within Viva Goals and not connected to a Microsoft 365 group; they can only be managed in Viva Goals. Organization owners have ownership access to these teams.

## Create a native team in an organization

By default, any member of an organization can create a team in that org. That said, organization owners can restrict team creation permissions to owners and admins or specific users and groups.

1. Go to **All Teams** > **Create team** > **Create Teams from scratch** or **Admin** > **Teams** > **Add Team** > **Create Teams from scratch**.

1. Fill out the following details in the dialog:

    - Team Name: Enter a team name.

    - Team owner: Search for and designate a team owner from the Team Owner dropdown list.

    - If this team is a sub-team, division, or department, select the parent team. (Optional)

    - Add any details you deem necesary. (Optional)

1. Select **Create team**.

### About parent teams

If you want to give your team a parent team, all of the following apply:

- Your team will default to the parent team's OKR settings, such as check-in frequency and creation permissions.

- Your team will show up as a sub-team under your parent team. If you want to view your parent team's other subteams, go to the parent team's page and select the sub-teams tab.

- You cannot select a restricted Microsoft 365 group-backed team as a parent team.

## Create native teams in bulk

You can create native teams in bulk using an Excel template.

1. Go to **All Teams** > **Create Team** or **Admin** > **Teams** > **Add Team**.

1. Select the dropdown next to **Create Team** or **Add Team** and choose **Import teams**. <!--Editor's Note: Formatting unclear. Verify consistency with UI throughout article.-->

1. Download the Excel template from the resulting window.

1. Update the Excel template with the following information about the teams you're importing. <!--Why are we saying "import" instead of "create"?-->

    - Team name – Give your team a name that doesn't already exist in Viva Goals.

    - Team owner – Enter the primary email of the user who will be the team's owner.

    - Team admins – Add the primary email addresses of up to five users you'd like to be admins for the team. (Optional)

    - Parent team – Add the name of the team you'd like to be the parent team for the team you're creating. (Optional)

    - Group  ID – Add up to five Microsoft Entra groups as members for this team. Mail-enabled security groups, mail-enabled distribution groups, and nested groups are supported. Other security groups and Microsoft 365 groups aren't supported. (Optional)

        **Note:** You can find a group's ID by navigating to the group's page in [portal.azure.com](https://portal.azure.com/) and checking under **Properties**. <!--Get the right formatting for "properties."-->

1. Go back to the **Import teams** page in Viva Goals and upload the completed Excel doc. The page wlil display a snapshot of the information for the teams you're importing.

1. Select **Create Teams** to begin the import process and view the import tracking page.

1. The import can take up to 30 minutes depending on the number of teams being imported. Feel free to close the window during this process; you can always check the import's progress by going to **Account settings** > **Preferences** > **My imports** > **My team imports**.

1. Once the import is complete, you will receive an email notification. You can come back to the import tracking page to check how many teams got created and how many teams didn't.

Download the import report to understand why some of teams weren't created.

You can view the created teams by navigating to All Teams or Admin > Teams.

## Add members to a team

For both native teams (i.e. teams which are not connected to Microsoft 365 groups) and teams which are connected to Microsoft 365 groups, team owners can add members from within Viva Goals.  

To add individual users as team members, follow these steps:

Go to the Team OKR page. Click on the three dots (…) button on the top right of the page. A drop down will appear.

Select the Team Members from the drop down.

Select the Add Members button on the top right of the page.

Search for an individual user or group in the search box. You can search for either a Mail enabled security group, a distribution group or a Microsoft 365 group.  

Select the user or group that you want to be added as members.

4_.png

Select the Add Members button.  

There are two scenarios:  

The user or group selected is already a member of the organization: In this case, they get added to the team instantly.  

The user or group selected is not a member of the organization yet: In this case, if you have access to add members to the organization, the user or group will be added to the organization and the team. If you do not have access to add members to the organization, you will NOT be able to add these users or groups to the team. In such a scenario, please contact the organization administrator for access to add members to the organization and try the above steps again.  

To add users who have not tarted using Viva Goals yet, to your team, Use the steps mentioned above. When you click on add members, make sure that the Send invitations to users checkbox is selected. This will send them an invitation to join your team in Viva Goals.

Note: When you set up a team, it's useful to add a second team owner to make sure that team management isn't dependent on a single user. You can also select multiple team owners if required.

To assign team administrator permissions to a team member, follow these steps:

Select the Team Members tab. For every user listed, there's an Actions dropdown list (three dots) next to the user’s name.

Select the Actions dropdown list, and then select Owner or admin.

5_.png

You can promote or remove any team member as a team owner from the Admin menu on the Admin Dashboard page.

Frequently Asked Questions (FAQs):

What happens when you do not have permission to add members to the org?  

If you do not have permissions to add members to the org, you will only be able to add existing organization members as team members, and will not be able to add users who are not members of the organization.  

What happens to Groups added as members in native Teams?

In native teams, you can add a mail-enabled security group, distribution group or Microsoft 365 group as members. Once you do that, the group members would have access to the Viva Goals team and the organization. Within the Viva Goals -> Admin -> Members, you will find these groups displayed as members. Every time, a new user is added or removed from the group, they will get access to the Viva Goals team and the organization. Likewise, when a user is removed from the group, they will lose membership access to the Viva Goals team and the organization (if they have gained access to the organization only through this group).

How to manage roles and delete members in a team:  

To update the role of a member, go to the Teams Members page within a team, click on the action button next to the relevant user. In the drop down, either promote them to a team owner or remove them as a team owner.  

Shape Screenshot showing where you update team owners. 6_.png

To remove members from a team, click on the action button next to the relevant user. In the drop down, click on remove.  

If you want to assign the role to or remove members who are part of a group, search for that user in the search field and click on action button (three dots) to select the relevant action.

Frequently Asked Questions (FAQs):

As a team owner, when I remove a user or group from the native team, what will happen?

When an individual user is removed from the team, they will continue to have access to the organization but lose membership access to the team.  

What will happen when groups attached to native teams are removed from the Viva Goals organization? Once the organization owner removes the group from the organization, the group will be removed from the native teams as well. The members will lose access to the team and the org

Can I make a group which is attached to my native team as owner of the team? No, groups cannot be assigned roles within native teams or the organization.  

Delete, Archive and Restore Teams.  

As an org owner or team owner, we give you support to manage your teams. Sometimes, teams are dissolved or retired due to an organizational change. In that case, you have the following two options in Viva Goals.

Delete a team

Archive a team

How to delete a team

In case of native teams, which are NOT connected to a Microsoft 365 group, an org owner/admin or team owner/admin can delete the team from within Viva Goals. A team can only be deleted from within Viva Goals if it has no OKRs or Projects assigned to it. If there are OKRs or projects assigned to the team, you can instead archive the team.  

To delete a native team from within Viva Goals, follow these steps:

If you are an org owner or administrator:  

Select Admin > Teams tab > Actions.

Select the Delete option corresponding to the team that you want to delete.

If you are a team owner

Go to your Team OKRs page

Visit more actions at the top and select the delete option

7_.png

Frequently Asked Questions:  

1. I want to delete my native team. However, I am not able to delete because there is OKR content? What should I do?  

You can remove the OKRs from the team or un/re-assign the OKRs to another team, before trying to delete the team again.

How to archive a team

We recommend you archive teams that are no longer in service so that the collection of teams stay relevant for use. Once a team is archived, you can no longer create OKRs and initiatives under that team, and no users are a part of the team. Additionally, any sub teams become independent teams in Viva Goals. All OKRs that were previously assigned to the archived teams will still be accessible for actions to be performed on them, such as check-ins.

Even though you won't be able to see the archived team under All Teams now, you can see the assigned OKRs by expanding the parent OKRs that they're aligned to. You can also view those OKRs/initiatives in the Explorer by applying the type filter and selecting the archived team name.

Once a team has been archived, it's marked as Archived on the Teams tab in the Admin console. It won't be visible anywhere else. Any objectives that were owned by this team remains unchanged. But you can't assign new objectives to the team.

Activities related to the archived team are halted, including assigning team members and team-level notifications. To resume these activities, you would need to restore the team.

To archive a team, follow these steps:

Org owner or administrator:  

Select Admin > Teams tab > Actions.

Select Archive for the team that you want to archive.

Both org and team owners and administrators:  

Go to Team OKRs page

Visit more actions at the top and select the archive option

Archiving a team isn't permanent. You can restore an archived team. To restore an archived team:

Select Admin > Teams tab > Actions.

Select restore for the team you want to restore.

Alternately, you can visit the team OKRs page and select restore option in More options.  

8_.png
