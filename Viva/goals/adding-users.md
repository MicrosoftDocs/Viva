---
title: Add users to Viva Goals
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
description: "Learn how to add a user to Viva Goals"
---

# Add users to Viva Goals

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Feeling a little lonely in your Viva Goals workspace? Teammates are crucial to unlocking the full potential of the OKR process!

Once you've established your team/subteam hierarchy in Viva Goals, it's time to start populating those teams with users. With Viva Goals, you have the following ways of adding users as team members:

1. Using the **Invite Users** button
1. Through the Admin Dashboard
1. Auto-Joining and Bulk Invites

> [!NOTE]
> Only administrators can invite users and create teams.

## Invite Users button (basic invite)

The first, and arguably easiest, way to invite users to your instance of Viva Goals is to use the **Invite Users** button. This button is located in a few places, but is most readily available in the navigation bar on the left side.

:::image type="content" source="../media/goals/invite-users.png" alt-text="Invite Users button":::

On selecting the **Invite Users** button, you'll be presented with a dialog box that contains fields described in the following table:


|Field Name  |Description  |
|---------|---------|
|Email Addresses   |     In this field, you can enter the email address of the individual you would like to invite to Viva Goals. You can invite more than one person by separating the email addresses with a semicolon or a space    |
|Teams (Optional)     | This field is a dropdown list containing a list of all of the teams that have been created for your Viva Goals account. If you want your new user(s) to be added to an existing team, select one team from the dropdown list. For more information on Teams, see [Creating and Editing Teams and Subteams](https://help.ally.io/en/articles/2631919-creating-and-editing-teams-and-sub-teams).        |
|Manager (Optional)     |   This field is a dropdown list containing a list of all of the users who have been designated as "managers". If you want your new user(s) to fall under an existing manager, select one user from the dropdown list.      |

The fields specified in the preceding table are depicted in the following image:

:::image type="content" source="../media/goals/setting-users-to-send-invitation.png" alt-text="Deciding on the users to send invitation to":::

After filling in the desired user information, select **Send Invites** to have an email sent with a link to Viva Goals.

## Admin dashboard

You can add users to Viva Goals from the Admin dashboard in the following ways:

- [Users Tab (Invite)](#users-tab-invite)
- [Teams Tab (Invite optional)](#teams-tab-invite-optional)

### Users tab (Invite)

The first method to add users from the Admin Dashboard is sending the users an email inviting them to your company's instance of Viva Goal. This option is best if you want your user to be notified they've been added to Viva Goal, and be provided with a link that will let them access the site.

To send an invitation through email to users, perform the following steps:

1. Navigate to the Admin panel from the left-hand navigation menu.
1. Select the **Users** tab.
1. Select **Invite Users** from the upper-right side of the page.
1. Fill out the available fields.
1. Select **Send Invites**.

   :::image type="content" source="../media/goals/send-invitation-email.png" alt-text="Sending an invitation email to users":::

### Teams tab (Invite optional)

The second way to add a user from the Admin Dashboard is to add a user directly to an established team.

To add a user directly to an established team, perform the following steps:

1. Navigate to the Admin panel from the left-hand navigation menu.
1. Select the **Teams** tab.
1. Scroll to the team you would like to add a member to.
1. Select the **Actions** dropdown list from the right-hand side of the screen select **Manager Members**. A new screen opens up.
1. Select **Add Members**.
1. Enter the email address of the user you would like to add.
1. Check the **Skip Invitation Email** option if you don't want to send an invite link to the user. 
> [!NOTE]
> This option might be used if you wish to set up the structure of your teams before rolling out Viva Goals to your business.

1. Select **Send Invites**.

## Auto-joining and bulk invites

If your company is larger, manually sending invites and organizing people into team groups may be more time consuming than your rollout plan is prepared for. In these instances, we can streamline the user addition process in the following ways:

- [Auto-joining users](#auto-joining-users)
- [Bulk invites](#bulk-invites)

### Auto-joining users

Auto-join allows users from your work domain to auto-join your Viva Goals organization when they sign up for an account. This option works well for mid-sized teams.

Enable this setting by selecting **Admin > Settings > Signup Mode**.

:::image type="content" source="../media/goals/auto-join-users.png" alt-text="Auto-joining users":::

When you enter more than one domain, separate them with a comma.

### Bulk invites

If you have a large team or are trying to add multiple teams and departments, a bulk-invite may be more suitable. Email us at **support@ally.com** with your request.

## FAQs:

### Q: Unable to invite user; it says "This account has been suspended"

**A**: The error **This account has been suspended** occurs when you try to invite deactivated users to your Viva Goals instance. Instead of inviting them fresh, you need to look for the deactivated profiles, activate them, and resend the invites, if necessary.

### Q: How do I remove, suspend, or delete a user?

**A**: If you need to remove a user from your organization, an administrator can suspend or delete their account by selecting **Admin > Users**. Find the user you wish to remove and select **Actions > Deactivate** or **Actions > Delete**.

:::image type="content" source="../media/goals/deactivating-or-deleting-a-user.png" alt-text="Deactivating or deleting a user":::

**Suspending Vs deleting a user**

A suspended user will remain visible in Viva Goals, but won't be able to sign in. They'll remain assigned as an owner of any OKRs they had. They'll not be searchable in **All Users** page, and will be listed as **deactivated** in the **Users** section of the admin tools. You can reactivate a user by selecting **Action > Make Active** which will restore their ability to sign in.

:::image type="content" source="../media/goals/making-active-a-user.png" alt-text="Making active a user":::

Deleting a user is an action that can't be undone. Administrators can't delete a user if they're the current owner of any objective. They'll be met with an error message.

:::image type="content" source="../media/goals/error-while-trying-to-delete-a-user.png" alt-text="Error message displayed when trying to delete a user":::

Deleting a user will delete all of their activities in the system. After a user is deleted, it will appear as though they never existed.

:::image type="content" source="../media/goals/prompt-to-delete-a-user.png" alt-text="The dialog box prompting confirmation to delete a user":::

**Removing a team member**

If you're just trying to remove a user from a team,  perform the following steps:

1. Navigate to the team page, select **Actions > Manage Members**.

   :::image type="content" source="../media/goals/removing-a-team-member-step-1.png" alt-text="First step in the process of removing a team member":::
    
2. Select **Actions > Remove**.
   
   :::image type="content" source="../media/goals/removing-a-team-member-step-2.png" alt-text="Second step in the process of removing a team member":::
 
### Q: How do I grant/remove Admin privileges?

**A**: An administrator can grant admin privileges to another user by selecting **Admin > Users** and selecting **Make Admin** from the **Actions** dropdown list next to the user’s name. You can remove privileges here too.

:::image type="content" source="../media/goals/grant-admin-privileges.png" alt-text="Granting admin privileges":::

### Q: Why is an Org Admin of my organization, not a Dashboard Owner?

**A**: The Dashboard permissions list is locked after the creation of the dashboard.

The new organization administrators can't be added to the Viva Goals instance after the dashboard was visited because the permissions get locked.
