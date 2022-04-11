---
title: Inviting and removing a user
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
- Strat_SP_modern
- M365-collaboration
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Inviting and removing a user in Viva Goals"
---

# Inviting and removing a user in Viva Goals

> [!IMPORTANT] 
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Onboarding your entire team into Viva Goals is a very simple process that can be done in two ways: 

1. By sending an invitation to the members 

1. Approving member invites sent via the Join Organizations page 

But before doing that, you must sign into Viva Goals using Azure Active Directory and create an account for your organization.  

## Adding users via invitation after creating an organization 

1. After creating an organization, click on continue. 

[screenshot] 

1. You will be taken to the invite members page where you can enter the names of the users you would like to add to your organization. 

[screenshot] 

1. Alternatively, you can also add an Azure Active Directory group with all the users you want to invite. 

[screenshot] 

1. Additionally, if your organization is public, you have the option of sharing with users a link to join your organization. 

Note: Ensure that all the users are provisioned to Azure Active Directory. 

## Adding members via invitation from within the app 

1. You can invite users by clicking on the ‘Invite Users’ button from the menu. 

[screenshot] 

1. If you’re the organization administrator, you can also head to settings, and click on ‘Invite Users’ under the Users tab. 

[screenshot] 

1. Apart from this, you can also click on All Users from the menu and select the ‘Invite Users’ button. 

[screenshot] 

## Removing a user 

To remove a user from your organization, an Admin can either deactivate or delete their account. This can be done by navigating to **Admin -> Users**. Find the user you wish to remove and select **Actions -> Deactivate** or **Actions-> Delete**. You'll no longer be billed for the user with both actions.

### Deactivating Vs deleting a user

A deactivated user will remain visible in Viva Goals, but won't be able to sign in. The user will remain assigned as an owner of any OKRs they had. They won't be searchable in **All Users**, and be listed as deactivated in the **Users** section of the admin tools. 

:::image type="content" source="../media/goals/Goals-deactivate-user.png" alt-text="Image of deactivate a user.":::

You can reactivate a user by choosing **Action-> Make Active** which will restore their ability to sign in.

:::image type="content" source="../media/goals/Goals-make-user-active.png" alt-text="Image of the make a user active":::

Deleting a user is a permanent action and can't be undone. Deleting a user will delete all of their activities in the system.

:::image type="content" source="../media/goals/Goals-delete-user-warning.png" alt-text="Image of the delete a user warning":::

Admins can’t delete users if they’re the current owners of any objective. To delete these users, reassign their OKRs first and then delete the users.

:::image type="content" source="../media/goals/Goals-delete-use-admin-message.png" alt-text="Image of the admins message":::

### Frequently asked questions

1. Can any group in Azure Active Directory be invited to Viva Goals? 

A: Any group in Azure Active Directory, Security Groups, Distribution groups, Office 365 groups can be invited onto Viva Goals 

2. How many groups can be invited? 

A: As of now, only one group from Azure Active Directory can be invited to Viva Goals. 

3. If only one group can be added, how can administrators invite an entire organization to Viva Goals? 

A: To invite an entire organization, we recommend users to nest all the existing groups or include all the members as part of the single group.  
