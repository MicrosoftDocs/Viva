---
ms.date: 04/05/2022
title: Inviting and removing a user
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager: Liz.Pierce
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
- essentials-manage
search.appverid:
- MET150
description: "Inviting and removing a user in Viva Goals"
---

# Invite and remove users in Viva Goals

To onboard your entire organization into Viva Goals, send an invitation to all team members.

Before either of these procedures, you must sign in to Viva Goals using Microsoft Entra ID and create an account for your organization.  

To sign in to Viva Goals, visit https://goals.microsoft.com/.

## Add users via invitation after you create an organization 

1. After you create an organization, select **Continue.**

2. You're taken to the **Invite Members** page, where you can enter the names of the users you want to add to your organization.

   Alternatively, you can also add a Microsoft Entra group with all the users you want to invite.

4. If your organization is public, you have the option of sharing a link to join your organization with users.

> [!Note]
> Ensure that all users are provisioned and the eligible ones are licensed to Viva Goals on your organization's Microsoft Entra account. You can learn more about assigning licenses in [this article](/azure/active-directory/fundamentals/license-users-groups).

## Add members via invitation from Viva Goals

To invite users from the Viva Goals menu, select the **Add members** button.

Or, if you're the organization administrator, you can go to **Settings** and select **Add members** on the Users tab.

:::image type="content" source="../media/goals/2/23/a.jpg" alt-text="Screenshot show the dialog box where an admin uses the Invite Users button." lightbox="../media/goals/2/23/a.jpg":::

Another way to do this is to select **Users** from the menu and then select the **Add members** button.

:::image type="content" source="../media/goals/2/23/b.jpg" alt-text="Screenshot showing another option to add members." lightbox="../media/goals/2/23/b.jpg"::: 

<a name='add-an-azure-ad-group-via-invitation'></a>

## Add a Microsoft Entra group via invitation

To invite a group, you can select the **Add members** button by following any one of the methods mentioned above. Enter the Microsoft Entra group name in the popup that appears. An invitation is sent to the group email address. 

Now, all the members in the group are eligible to sign in. The user record will get added to the **All Users** list after they sign in for the first time.

> [!Note] 
> Every time a user is added to the Microsoft Entra group, that user will automatically become eligible to log into Viva Goals. However, users will need to sign in at least once to appear under the **All Users** list.

## How to add members to a team 

Team owners can set up their team by adding team members. Members can be added to the team either by adding a Microsoft Entra group (Microsoft 365 group, mail enabled security group or distribution group), or by adding individuals in your tenant. 

To add members to your team, follow these steps: 

1. Go to the **Team OKR** page. 
1. Select the **Team Members** tab. 
1. Select the **Add Members** button. 
1. Start typing the name of the Microsoft Entra group or the individual. The search tool returns results directly from Microsoft Entra ID.  
1. Select the group or the individual you want to add. 
1. After selecting the required groups or individuals, select the Add Members button. The groups or individuals are added to the team as a member.

When you set up a team, it's recommended that you add one or more team owners to make sure that the team management isn't dependent on one person. 

To assign team owner permissions to a team member, follow these steps:

Navigate to the **Team Members** tab. Search for the member in the search field. The search tool returns results directly from Microsoft Entra ID. Next to the member you want to assign as the owner, select on the more options dropdown. 

- If the member has already been added to the team as part of a group or individually, the dropdown provides the option to **Make owner**. Clicking on this option assigns this member as the team owner. 
- If the member hasn't been added to the team yet, the more options button provides the option to **Add to team**. After adding the member, repeat the above process to assign this member as the team owner. 

## Remove a user 

To remove a user from your organization, an admin can deactivate or delete their account: Go to **Admin** > **Users**. Find the user you want to remove and select **Actions** > **Deactivate** or **Actions** > **Delete**. In either case, you'll no longer be billed for that user.

If you have invited users using a Microsoft Entra group, you can remove the user from the group to deactivate them in Viva Goals as well.

> [!NOTE]
> When a user is removed/deactivated from the on-prem Active Directory, the information has to be synced to Microsoft Entra ID so that the user is deactivated in Viva Goals as well. If there's a delay in syncing the information between on-prem Active Directory and Microsoft Entra ID, the impacted user will be able to access Viva Goals until they're deactivated.

### Deactivate versus delete a user

A deactivated user remains visible in Viva Goals but won't be able to sign in. The user remains assigned as an owner of any OKRs they had. They won't be searchable in **All Users** and will be listed as deactivated in the **Users** section of the admin tools. 

:::image type="content" source="../media/goals/2/23/c.jpg" alt-text="Screenshot shows deactivated users." lightbox="../media/goals/2/23/c.jpg"::: 

To reactivate a user, go to **Action** > **Make Active**, which will restore their ability to sign in.

:::image type="content" source="../media/goals/2/23/d.jpg" alt-text="Screenshot showing where you reactivate a user." lightbox="../media/goals/2/23/d.jpg"::: 

Deleting a user is a permanent action and can't be undone. It removes all their activities in the system.

:::image type="content" source="../media/goals/2/23/e.jpg" alt-text="Screenshot shows deleting a user and a warning." lightbox="../media/goals/2/23/e.jpg"::: 

Admins can’t delete users who currently own any objective. To delete those users, reassign their OKRs first, and then delete the user.

:::image type="content" source="../media/goals/2/23/f.jpg" alt-text="Screenshot of the error dialog you get when you try to delete a user who owns objectives or initiatives." lightbox="../media/goals/2/23/f.jpg"::: 

**Example scenario of when to deactivate a user**

- When an employee moves from one organization to another within a company

**Example scenario on when to delete a user**

- When the organization administrator receives a request from the user to completely delete all data that can be linked back to them as per GDPR DSR regulations

> [!Note] 
> To find deleted or deactivated users, navigate to the **Users** tab and select the **Deactivate** filter option under the **Status** dropdown.

## FAQ (Frequently asked questions)

1. **Who can be invited/granted access to Viva Goals?**
    1. There are two user types in Microsoft Entra ID—members and guests. Only members can be invited/provisioned to access Viva Goals and not guest users. 

1. **Can any group in Microsoft Entra ID be invited to Viva Goals?**
    1. Any group in Microsoft Entra ID, Security Groups, Distribution groups, and Microsoft 365 groups can be invited to Viva Goals. 

1. **How many groups can be invited?** 
    1. There's no limit on the number of groups that can be added into Viva Goals. 

1. **If only one group can be added, how can administrators invite an entire organization to Viva Goals?**
    1. To invite an entire organization, we recommend users nest all existing groups or include all members as part of a single group.  

1. **Can I invite a group if I'm not a member of the group?**
    1. Yes, you can invite any group, even if you aren't a member.

1. **Will emails be sent to all users who are part of the invited group list?**
    1. Email won't be sent to individual emails. Instead, email is sent to the group email. And, if the group they're a member of restricts emails by not including Viva Goals as an authorized sender, users won't receive email communications.

1. **Will all users in the invited Microsoft Entra group appear in the 'All Users' list?**
    1. All the users in the group are eligible to log into Viva Goals but only the users who have logged in at least once will appear in the **All Users** list.

1. **If users are added to or removed from the group, will the list automatically reflect the change with the respective organization in Viva Goals?**
    1. When a user is added to the Microsoft Entra group that was used to invite users to an organization in Viva Goals, the user becomes automatically eligible to sign in but they won't appear in the 'All Users' list until they have logged in at least once. 
    1. When a user who appears in the **All Users** list is removed from the Microsoft Entra group, this change is automatically reflected in Viva Goals as well.

1. **How can I view a deactivated or deleted user?**
    1. Go to **Admin** > **Settings** and under **Users** tab, select the **Status** dropdown and select **Deactivated**.

1. **Manager updates made in Microsoft Entra ID are not reflected in Viva Goals. Why?**
    1. The changes made in Microsoft Entra ID are pushed to Viva Goals only after the corresponding users sign out and sign-in to Viva Goals. Until then, the updates won't reflect in Viva Goals. To resolve, sign out and then log back in to Viva Goals.

1. **If users are added to or removed from the group, will the list automatically reflect the change with the respective organization in Viva Goals?**
    1. When users are deleted from Microsoft Entra ID, they're not deleted/deactivated in Viva Goals immediately. In the Azure portal, when a user is deleted, it is in a soft-deleted phase for a 30-day period. During this period, the admin has the possibility to retrieve the account. If the account isn't retrieved for 30 days, it's then permanently deleted from Azure, and we get an update to delete/deactivate the same in Viva Goals.
