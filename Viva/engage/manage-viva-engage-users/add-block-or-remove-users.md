---
title: "Add, block, or remove Viva Engage users"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 09/30/2024
audience: Admin
ms.topic: article
ms.service: office-online-server
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 0fc72b66-cbf1-4202-bcf0-f2174ea96798
description: "Manage users and guests in Viva Engage."
---

# Add, block, or remove a Viva Engage user

As a verified or network admin, you can add, block, or remove Viva Engage users, and define what fields to include in their profiles.
  
To get to the Viva Engage admin center to manage users:
  
- In Microsoft 365, go to **Admin** \> **Viva Engage**.
    
- Or, in Viva Engage, select the Viva Engage settings icon :::image type="icon" source="../../media/9704ce70-56ce-43f7-96c6-f253b0413d40.png" border="false":::, and then select **Edit Network Admin settings**.
    
## Invite users to Viva Engage
<a name="InviteUsers"> </a>

Use this procedure only to invite employees with a company email to Viva Engage.

- If you enforce Microsoft 365 identity in your network, Microsoft 365 users with a Viva Engage license are created as *pending users* in Viva Engage. 
- If you don't enforce Microsoft 365 identity, users must select the Viva Engage tile from Microsoft 365 or sign in to Viva Engage to join the network.
- If you invite a user to a group who has no Viva Engage license, that user is suspended in Viva Engages and removed from the group member list. They don't receive announcement emails.

**If your Viva Engage network is [in Native Mode](../overview-native-mode.md)**, you must perform this action in the [Microsoft Entra user Management Portal](/azure/active-directory/fundamentals/add-users-azure-active-directory).

**If your Viva Engage network is not in Native Mode**, follow these steps:
  
1. In Viva Engage, from the settings, select **Edit Network admin Settings**. This selection opens the Yammer admin center.

2. In the Yammer admin center, select **Users** > **Invite Users**.

3. Enter individual email addresses, and then select **Invite**. 

4. Additionally, you can select **Import an address book** and import a CSV file exported from an email application, such as Outlook or Apple Mail. The CSV file should include a single email address on each line.
  
> [!NOTE]
> If your organization uses more than one internet domain for email addresses and you want to add users from other domains to your network, consider performing a Viva Engage network consolidation. For more information, go to [Network migration: Consolidate multiple Viva Engage networks](../configure-your-viva-engage-network/consolidate-multiple-networks.md). 
  
<a name="ManagePending"> </a>
## Manage pending users

A *pending user* is someone who was invited to a Viva Engage network but hasn't ever signed in. Pending users can be added to communities and receive announcement notification emails from community admins. As in all Office products, pending users are visible in the community member list.

To stop receiving announcements from a particular community, users can sign in to Viva Engage and leave the community. Or, they can follow the unsubscribe link in the email to unsubscribe from all Viva Engage emails.
 
<a name="InviteGuests"> </a>
## Invite guests

Invite external contacts with email addresses outside of your domain (for example, consultants, contractors, or partners). Guest email domains aren't added to the list of authorized domains for your network.
  
1. In Viva Engage, select the settings icon, and select **Edit Network admin Settings** to go to the Yammer admin center.

2. In the Yammer admin center, select **Users** > **Invite Guests**.
    
3. Enter individual email addresses. Active and pending guests are listed on this page.
    
   :::image type="content" source="../../media/c8573062-7613-4964-bbd3-4393931146af.png" alt-text=" Screenshot of the Pending guests list.":::
  
As with other users, guest names and profiles remain blank until they accept their invitations and complete registration. Guest accounts can be deleted anytime, but their contributions to the network remain.
  
For more information about guests, see [External Messaging FAQ](../work-with-external-users/external-messaging-faq.md).
  
<a name="RemoveUsers"> </a>
## Remove users

You can deactivate or permanently remove active users, pending users, and guests.

**If your Viva Engage network is in Native Mode**, only use the **Remove Users** page in the Admin portal to process a  data subject request for GDPR. Before you proceed, review [GDPR requests](../manage-security-and-compliance/gdpr-requests-in-viva-engage-enterprise.md) or [GDPR requests for all of Office 365](/compliance/regulatory/gdpr-dsr-Office365). To remove a user from your Viva Engage Network, go to the [Microsoft Entra user Management Portal](/azure/active-directory/fundamentals/add-users-azure-active-directory).

**If your Viva Engage network is not in Native Mode**, follow these steps:

1. In Viva Engage, select the settings icon, and select **Edit Network admin Settings** to go to the Yammer admin center.

2. In the Yammer admin center, select **Users** \> **Remove Users**.
    
2. Enter an existing user's name. 
    
3. Select an action to take:
    
   **Deactivate this user:**

   - If the user has Microsoft Entra credentials, first use this action to deactivate the user, and then follow the instructions in [Block users](#block-users).
 
   - If the user has no Microsoft Entra credentials, deactivation blocks the user from signing in until the user verifies their email address again. Without access to their verified email account, they can't sign back in to Viva Engage. User profile information, messages, and file uploads remain for 90 days.

   >[!NOTE] 
   > Even though deactivated users are visible for 90 days, their accounts can only be reactivated up to 30 days after deactivation. After 90 days, the account is permanently deleted.
    
   **Permanently remove this user and keep messages:** Removes the user and retains the messages and content they posted.

   **Permanently remove this user and messages:** Removes the user and all the messages they posted. This can't be reversed.

   **Erase this user. Wipe their name and personal information, but leave their messages. (Can't be undone after 14 days):** Deactivates the user for 14 days to give the admin time to evaluate files and messages before the user is permanently deleted.
    
   **All deletion options delete the following data:**

   - Who the person is following, what conversations and articles they're following, and who's following them
   - Bookmarks, language preferences, notification settings, and account activity
   - User's profile
   - Group memberships
   - Org chart
   - The list of networks they were a member of

   The first three deletion options preserve the user's name in Viva Engage stored data and list deactivated users on the **Remove Users** page, from which you can reactivate or delete a user. Only the **Erase this user** option removes the user's name.
  
   :::image type="content" source="../../media/162b43ed-acd1-4085-8073-b43845c30999.png" alt-text="Screenshot of deactivated user list.":::
  
<a name="BlockUsers"> </a>
## Block users

A user with a blocked email address can't join your Viva Engage network unless an admin unblocks the address.

**If your Viva Engage network is [in Native Mode](../overview-native-mode.md)**, you must block users from the [Microsoft Entra user Management Portal](/azure/active-directory/fundamentals/add-users-azure-active-directory).
  
**If your Viva Engage network is not in Native Mode**, block users using one of the following options:
  
- **Block the user in the Yammer admin center:**
    
   1. In Viva Engage, select the settings icon, and select **Edit Network admin Settings** to go to the Yammer admin center.

   2. In the Yammer admin center, select **Users** \> **Block Users**.
    
   3. Enter the email address of the user to block. If you enter multiple email addresses, separate them with commas or line breaks. 

   If the user you select is in a suspended state in Viva Engage, blocking that email address puts the user in a deleted state. 
    
  > [!TIP]
  > Because Viva Engage is most effective when every post comes from an individual user, you might consider blocking group email addresses. 
  
-  **Block the user by removing their license and service plan, and removing the Viva Engage tile from Office 365:**
    
    - In the Microsoft 365 admin center, remove the **Viva Engage** license for the user. For steps, see [Turn off Viva Engage access for Microsoft 365 users](turn-off-user-access.md) and [Manage Viva Engage licenses in Microsoft 365](manage-licenses-in-office-365.md).
  
## Related articles
  
[Manage a community in Viva Engage](https://support.microsoft.com/en-gb/topic/manage-a-community-in-viva-engage-3e75fbe9-1b3e-48b5-8e4b-af2716b7873a)
