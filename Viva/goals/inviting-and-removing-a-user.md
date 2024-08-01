---
ms.date: 05/31/2024
title: Invite or remove users in Viva Goals
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager: Liz.Pierce
audience: Admin
f1.keywords:
- NOCSH
ms.topic: how-to
ms.service: viva-goals
ms.localizationpriority: medium
ms.collection:  
- Strat_SP_modern
- M365-collaboration
- m365initiative-viva-goals
- essentials-manage
search.appverid:
- MET150
description: "Inviting and removing a user in Viva Goals"
---

# Invite or remove users in Viva Goals

This article explains how to add members to your organizations and teams in Viva Goals.

## Add users to an organization

### Option 1: Add users via invitation after you create an organization

1. After you create an organization, select **Continue.**

1. You're taken to the **Invite Members** page, where you can enter the names of the users you want to add to your organization.

   Alternatively, you can also add a Microsoft Entra group with all the users you want to invite.

1. If your organization is configured such that all users in the tenant can access it, you have the option of sharing a link to join your organization with users.

> [!Note]
> Ensure that all users are provisioned and the eligible ones are licensed to Viva Goals on your organization's Microsoft Entra account. You can learn more about assigning licenses in [this article](/azure/active-directory/fundamentals/license-users-groups).

### Option 2: Add members via invitation from Viva Goals

To invite users from **Admin** > **Members**, select **Add members**.

:::image type="content" source="../media/goals/2/23/1-add-members-option.png" alt-text="Screenshot that shows how to add members from the Members tab of the Admin section." lightbox="../media/goals/2/23/1-add-members-option.png":::

Alternatively, if you're the organization owner, you can go to **Admin** > **Settings** and select **Add members**.

Another way to do this is to select the **Users** option from the navigation menu on the left side of Viva Goals, then go to the **All Users** tab and select **Add members**.

:::image type="content" source="../media/goals/2/23/2-users-page-option.png" alt-text="Screenshot that shows how to add members from the Users tab." lightbox="../media/goals/2/23/2-users-page-option.png":::

<a name='add-an-azure-ad-group-via-invitation'></a>

### Invite members by adding a Microsoft Entra group

To invite a group, you can select the **Add members** button by following any one of the methods mentioned above. Enter the Microsoft Entra group name in the popup that appears. An invitation is sent to the group email address.

Now, all the members in the group are eligible to sign in. The user record will get added to the **All Users** list after they sign in for the first time.

> [!Note]
> Every time a user is added to the Microsoft Entra group, that user will automatically become eligible to log into Viva Goals. However, users will need to sign in at least once to appear under the **All Users** list.

## Add users to a team

Team owners can set up their team by adding team members. Members can be added to the team either by adding a Microsoft Entra group (Microsoft 365 group, mail enabled security group or distribution group), or by adding individuals in your tenant. You can learn about teams in Viva Goals [here](viva-goals-teams-intro.md).

To add members to your team, follow these steps:

1. Go to the **Team OKR** page.

1. Select the **Team members** option from the dropdown in the top right.

   :::image type="content" source="../media/goals/2/23/3-team-add-members.png" alt-text="Screenshot showing the dropdown expanded to include the Team members option." lightbox="../media/goals/2/23/3-team-add-members.png":::

1. Select the **Add Members** button.

1. Start typing the name of the Microsoft Entra group or the individual. The search tool returns results directly from Microsoft Entra ID.

1. Select the group or the individual you want to add.

1. After selecting the required groups or individuals, select the Add Members button. The groups or individuals are added to the team as a member.

When you set up a team, it's recommended that you add one or more team owners to make sure that the team management isn't dependent on one person.

To assign team owner permissions to a team member, follow these steps:

Navigate to the **Team Members** tab. Search for the member in the search field. The search tool returns results directly from Microsoft Entra ID. Next to the member you want to assign as the owner, select on the more options dropdown.

- If the member has already been added to the team as part of a group or individually, the dropdown provides the option to make a user the owner. Selecting this option assigns this member as the team owner.

  :::image type="content" source="../media/goals/2/23/4-add-team-members.png" alt-text="Screenshot showing how to select different user roles." lightbox="../media/goals/2/23/4-add-team-members.png":::

- If the member hasn't been added to the team yet, the more options button provides the option to **Add to team**. After adding the member, repeat the above process to assign this member as the team owner.

## Remove a user from an organization

To remove a user from your organization, an admin can deactivate or delete their account: Go to **Admin** > **Users**. Find the user you want to remove and select **Actions** > **Deactivate** or **Actions** > **Delete**. In either case, you'll no longer be billed for that user.

:::image type="content" source="../media/goals/2/23/5-deactivate-and-delete-user-option.png" alt-text="Screenshot showing an expansion of the More options menu for a specific member." lightbox="../media/goals/2/23/5-deactivate-and-delete-user-option.png":::

If you have invited users using a Microsoft Entra group, you can remove the user from the group to deactivate them in Viva Goals as well.

> [!NOTE]
> When a user is removed/deactivated from the on-prem Active Directory, the information has to be synced to Microsoft Entra ID so that the user is deactivated in Viva Goals as well. If there's a delay in syncing the information between on-prem Active Directory and Microsoft Entra ID, the impacted user will be able to access Viva Goals until they're deactivated.

### Deactivate versus delete a user

A deactivated user remains visible in Viva Goals but won't be able to sign in. The user remains assigned as an owner of any OKRs they had. They won't be searchable in **All Users** and will be listed as deactivated in the **Users** section of the admin tools.

To reactivate a user, go to **Action** > **Make Active**, which will restore their ability to sign in.

:::image type="content" source="../media/goals/2/23/6-reactivate-user.png" alt-text="Screenshot showing the More options menu for a specific deactivated member." lightbox="../media/goals/2/23/6-reactivate-user.png":::

Deleting a user is a permanent action and can't be undone. It removes all their activities in the system.

:::image type="content" source="../media/goals/2/23/7-user-deletion-confirmation.png" alt-text="Screenshot showing the user deletion confirmation dialog." lightbox="../media/goals/2/23/7-user-deletion-confirmation.png":::

An admin can’t delete a user who currently owns any objective. To delete such a user, reassign their OKRs first, then delete the user.

:::image type="content" source="../media/goals/2/23/8-cannot-delete-user.png" alt-text="Screenshot showing the dialog that results when a user cannot be deleted." lightbox="../media/goals/2/23/8-cannot-delete-user.png":::

> [!Note]
> To find deleted or deactivated users, navigate to the **Users** tab and select the **Deactivate** filter option under the **Status** dropdown.

## Frequently asked questions

### Who can be invited/granted access to Viva Goals?

There are two user types in Microsoft Entra ID—members and guests. Only members can be invited/provisioned to access Viva Goals and not guest users.

### Can any group in Microsoft Entra ID be invited to Viva Goals?

Any group in Microsoft Entra ID, Security Groups, Distribution groups, and Microsoft 365 groups can be invited to Viva Goals.

### How many groups can be invited?

There's no limit on the number of groups that can be added into Viva Goals.

### If only one group can be added, how can administrators invite an entire organization to Viva Goals?

To invite an entire organization, we recommend users nest all existing groups or include all members as part of a single group.  

### Can I invite a group if I'm not a member of the group?

Yes, you can invite any group, even if you aren't a member.

### Will emails be sent to all users who are part of the invited group list?

Email won't be sent to individual emails. Instead, email is sent to the group email. And, if the group they're a member of restricts emails by not including Viva Goals as an authorized sender, users won't receive email communications.

### Will all users in the invited Microsoft Entra group appear in the 'All Users' list?

All the users in the group are eligible to log into Viva Goals but only the users who have logged in at least once will appear in the **All Users** list.

### If users are added to or removed from the group, will the list automatically reflect the change with the respective organization in Viva Goals?

When a user is added to the Microsoft Entra group that was used to invite users to an organization in Viva Goals, the user becomes automatically eligible to sign in but they won't appear in the 'All Users' list until they have logged in at least once.
    1. When a user who appears in the **All Users** list is removed from the Microsoft Entra group, this change is automatically reflected in Viva Goals as well.

### How can I view a deactivated or deleted user?

Go to **Admin** > **Settings** and under **Users** tab, select the **Status** dropdown and select **Deactivated**.

### Manager updates made in Microsoft Entra ID are not reflected in Viva Goals. Why?

The changes made in Microsoft Entra ID are pushed to Viva Goals only after the corresponding users sign out and sign-in to Viva Goals. Until then, the updates won't reflect in Viva Goals. To resolve, sign out and then log back in to Viva Goals.

### What happens when a Viva Goals users is deleted fro the Microsoft Entra ID?

When users are deleted from Microsoft Entra ID, they're not deleted/deactivated in Viva Goals immediately. In the Azure portal, when a user is deleted, it is in a soft-deleted phase for a 30-day period. During this period, the admin has the possibility to retrieve the account. If the account isn't retrieved for 30 days, it's then permanently deleted from Azure, and we get an update to delete/deactivate the same in Viva Goals.
