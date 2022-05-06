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

# Invite and remove users in Viva Goals

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Onboarding your entire team into Viva Goals is a very simple process that can be done in two ways: 

1. By sending an invitation to team members 

2. By approving member invites sent via the Join Organizations page 

Before either of these steps, you must sign in to Viva Goals using Azure Active Directory and create an account for your organization.  

## Adding users via invitation after creating an organization 

1. After creating an organization, click 'Continue.'

2. You will be taken to the Invite Members page, where you can enter the names of the users you would like to add to your organization. 

3. Alternatively, you can also add an Azure Active Directory group with all the users you want to invite. 

4. If your organization is public, you have the option of sharing a link to join your organization with users. 

Note: Ensure that all users are provisioned on your organization's Azure Active Directory account. 

## Adding members via invitation from within Viva Goals

1. You can invite users by clicking on the ‘Invite Users’ button from the menu. 

2. If you are the organization administrator, you can also head to Settings, and click on ‘Invite Users’ under the Users tab. 

![adding members from within the app](../media/goals/2/23/a.jpg)

3. Another way to do this is to click on 'All Users' from the menu and select the ‘Invite Users’ button. 

![adding members from within the application](../media/goals/2/23/b.jpg)

[screenshot] 

## Removing a user 

To remove a user from your organization, an Admin can either deactivate or delete their account. 

This can be done by navigating to **Admin -> Users**. Find the user you wish to remove and select **Actions -> Deactivate** or **Actions-> Delete**. You will no longer be billed for the user with both actions.

### Deactivating vs, deleting a user

A deactivated user will remain visible in Viva Goals, but won't be able to sign in. The user will remain assigned as an owner of any OKRs they had. They won't be searchable in **All Users**, and will be listed as deactivated in the **Users** section of the admin tools. 

![deactivated users image](../media/goals/2/23/c.jpg)


You can reactivate a user by choosing **Action-> Make Active** which will restore their ability to sign in.

![reactivating a user image](../media/goals/2/23/d.jpg)

Deleting a user is a permanent action and can't be undone. Deleting a user will delete all of their activities in the system.

![deleting a user warning image](../media/goals/2/23/e.jpg)

Admins can’t delete users if they are the current owners of any objective. To delete these users, reassign their OKRs first and then delete the users.

![error image when attempting to delete users who own objectives or projects](../media/goals/2/23/f.jpg)

**Example scenario on when to deactivate a user**

1. When an employee moves from one organization to another within a company.

**Example scenario on when to delete a user**

1. When the organization administrator receives a request from the user to completely delete all data that can be linked back to them as per GDPR DSR regulations.

### Frequently asked questions

**1. Can any group in Azure Active Directory be invited to Viva Goals?**

Any group in Azure Active Directory, Security Groups, Distribution groups, and Office 365 groups can be invited to Viva Goals. 

**2. How many groups can be invited?** 

As of now, only one group from Azure Active Directory can be invited to Viva Goals. 

**3. If only one group can be added, how can administrators invite an entire organization to Viva Goals?**

To invite an entire organization, we recommend users nest all existing groups or include all members as part of the single group.  

**4. Can I invite a group if I'm not a member of the group?**

Yes, you can invite any group, even if you aren't a member.

**5. Will emails be sent to all users who are part of the invited group list?**

Yes, all users will receive email communication. However, if the group they're a member of restricts emails by not including Viva Goals as an authorized sender, users will not receive email communications.

**If users are removed or added to the group, will the list automatically sync with the respective organization in Viva Goals?**

A: Yes, the Members list in that specific group will automatically sync with the respective organization. 
