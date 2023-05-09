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
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:  
- Strat_SP_modern
- M365-collaboration
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Inviting and removing a user in Viva Goals"
---

# Invite and remove users in Viva Goals

To onboard your entire organization into Viva Goals, send an invitation to all team members.

Before either of these procedures, you must sign in to Viva Goals using Azure Active Directory and create an account for your organization.  

To sign in to Viva Goals, visit https://goals.microsoft.com/.

## Add users via invitation after you create an organization 

1. After you create an organization, select **Continue.**

2. You're taken to the **Invite Members** page, where you can enter the names of the users you want to add to your organization.

   Alternatively, you can also add an Azure Active Directory group with all the users you want to invite.

4. If your organization is public, you have the option of sharing a link to join your organization with users.

> [!Note]
> Ensure that all users are provisioned on your organization's Azure Active Directory account.

## Add members via invitation from Viva Goals

To invite users from the Viva Goals menu, select the **Add members** button.

Or, if you're the organization administrator, you can also go to **Settings** and select **Add members** on the Users tab.

:::image type="content" source="../media/goals/2/23/a.jpg" alt-text="Screenshot show the dialog box where an admin uses the Invite Users button." lightbox="../media/goals/2/23/a.jpg":::

Another way to do this is to select **Users** from the menu and then select the **Add members** button.

:::image type="content" source="../media/goals/2/23/b.jpg" alt-text="Screenshot showing another option to add members." lightbox="../media/goals/2/23/b.jpg"::: 

## Add an Azure AD group via invitation

To invite a group, you can select the **Add members** button by following any one of the methods mentioned above. Enter the Azure AD group name in the popup that appears. An invitation is sent to the group email address. 

Now, all the members in the group are eligible to sign in. The user record will get added to the **All Users** list after they sign in for the first time.

> [!Note] 
> Every time a user is added to the AAD group, they will automatically become eligible to log into Viva Goals. However, they will need to log in, at least once, to appear under the **All Users** list.

## Remove a user 

To remove a user from your organization, an admin can deactivate or delete their account: Go to **Admin** -> **Users**. Find the user you want to remove and select **Actions** -> **Deactivate** or **Actions** -> **Delete**. In either case, you'll no longer be billed for that user.

If you have invited users using an Azure AD group, you can remove the user from the group to deactivate them in Viva Goals as well. 

### Deactivate versus delete a user

A deactivated user remains visible in Viva Goals but won't be able to sign in. The user remains assigned as an owner of any OKRs they had. They won't be searchable in **All Users** and will be listed as deactivated in the **Users** section of the admin tools. 

:::image type="content" source="../media/goals/2/23/c.jpg" alt-text="Screenshot shows deactivated users." lightbox="../media/goals/2/23/c.jpg"::: 

To reactivate a user, go to **Action** -> **Make Active**, which will restore their ability to sign in.

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
    1. There are two user types in Azure AD—members and guests. Only members can be invited/provisioned to access Viva Goals and not guest users. 

1. **Can any group in Azure Active Directory be invited to Viva Goals?**
    1. Any group in Azure Active Directory, Security Groups, Distribution groups, and Microsoft 365 groups can be invited to Viva Goals. 

1. **How many groups can be invited?** 
    1. There's no limit on the number of groups that can be added into Viva Goals. 

1. **If only one group can be added, how can administrators invite an entire organization to Viva Goals?**
    1. To invite an entire organization, we recommend users nest all existing groups or include all members as part of a single group.  

1. **Can I invite a group if I'm not a member of the group?**
    1. Yes, you can invite any group, even if you aren't a member.

1. **Will emails be sent to all users who are part of the invited group list?**
    1. Email won't be sent to individual emails. Instead, email is sent to the group email. And, if the group they're a member of restricts emails by not including Viva Goals as an authorized sender, users won't receive email communications.

1. **Will all users in the invited AAD group appear in the 'All Users' list?**
    1. All the users in the group are eligible to log into Viva Goals but only the users who have logged in at least once will appear in the **All Users** list.

1. **If users are added to or removed from the group, will the list automatically reflect the change with the respective organization in Viva Goals?**
    1. When a user is added to the Azure AD group that was used to invite users to an organization in Viva Goals, the user becomes automatically eligible to sign in but they won't appear in the 'All Users' list until they have logged in at least once. 
    1. When a user who appears in the **All Users** list is removed from the Azure AD group, this change is automatically reflected in Viva Goals as well.

1. **How can I view a deactivated or deleted user?**
    1. Go to **Admin**->**Settings** and under **Users** tab, select the **Status** dropdown and select **Deactivated**.

1. **Manager updates made in Azure AD are not reflected in Viva Goals. Why?**
    1. The changes made in Azure AD are pushed to Viva Goals only after the corresponding users sign out and sign-in to Viva Goals. Until then, the updates won't reflect in Viva Goals. To resolve, sign out and then log back in to Viva Goals.

