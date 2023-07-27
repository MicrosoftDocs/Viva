---
title: "Add, block, or remove Viva Engage users"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: pamgreen
ms.date: 07/26/2023
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

# Add, block, or remove Viva Engage users

As a verified or network admin, you can add, block, or remove Viva Engage users, and define what fields to include in their profiles. 
  
To get to the Viva Engage admin center to manage users:
  
- In Office 365, go to **Admin** \> **Viva Engage**.
    
- Or, in Viva Engage, select the Viva Engage settings icon :::image type="icon" source="../../media/9704ce70-56ce-43f7-96c6-f253b0413d40.png" border="false":::, and then select **Edit Network Admin settings**.
    
## Invite users to Viva Engage
<a name="InviteUsers"> </a>

If you're enforcing Office 365 identity in your network, all Office 365 users that have a Viva Engage license are created as pending users in Viva Engage. If you aren't enforcing Office 365 identity, users aren't part of the Viva Engage network until they select the Viva Engage tile from Office 365 or sign in to Viva Engage.

> [!NOTE]
> If your Viva Engage network is [in Native Mode](../overview-native-mode.md), this action can be performed only in the [Azure Active Directory User Management Portal](/azure/active-directory/fundamentals/add-users-azure-active-directory) and not within the Viva Engage Admin portal.

Only employees with a company email address can be invited from this screen. 
  
- If you invite a user to a group who isn't licensed to use Viva Engage, that user is suspended in Viva Engage and removed from the group member list. They won't receive announcement emails. 
    
 **Invite users a few at a time**
  
1. In Viva Engage, select the settings icon and select **Edit Network admin Settings**. This selection opens the Yammer admin center.

2. In the Yammer admin center, select **Users** > **Invite Users**.
    
3. Enter individual email addresses, and then select **Invite**. 
    
4. Additionally, you can select **Import an address book** and import a CSV file exported from an email application, such as Outlook or Apple Mail. The CSV file should include a single email address on each line.
  
> [!NOTE]
> If your organization uses more than one internet domain for email addresses and you want to add users from other domains to your network, consider performing a Viva Engage network consolidation. For more information, go to [Network migration: Consolidate multiple Viva Engage networks](../configure-your-viva-engage-network/consolidate-multiple-networks.md). 
  
<a name="ManagePending"> </a>
## Manage pending users

A "pending user" is someone who was invited to a Viva Engage network but hasn't ever signed in. Pending users can be added to communities.

Pending users receive announcement notification emails from community admins. If users don't want to receive announcements from a particular community, they can sign in to their Viva Engage account and leave the community. Or, they can follow the unsubscribe link in the email to unsubscribe from all Viva Engage emails.

As in all Office products, pending users are visible in the community member list even if they have never signed in.
 
<a name="InviteGuests"> </a>
## Invite guests

Invite external contacts with email addresses outside of your domain (for example, consultants, contractors, or partners). Guest email domains aren't added to the list of authorized domains for your network. 
  
1. In Viva Engage, select the settings icon, and select **Edit Network admin Settings** to go to the Yammer admin center.

2. In the Yammer admin center, select **Users** > **Invite Guests**.
    
3. Enter individual email addresses. Guest users, including active and pending, are listed on this page. 
    
   :::image type="content" source="../../media/c8573062-7613-4964-bbd3-4393931146af.png" alt-text=" Screenshot of the Pending guests list.":::
  
As with other users, guest users' names and profiles remain blank until they accept their invitations and complete registration. Guest user accounts can be deleted anytime, but their contributions to the network remain.
  
For more information about guests, see [External Messaging FAQ](../work-with-external-users/external-messaging-faq.md).
  
<a name="RemoveUsers"> </a>
## Remove users

You can deactivate or permanently remove active users, pending users, and guests.

> [!NOTE]
> If your Viva Engage network is [in Native Mode](../overview-native-mode.md), the only reason to use the **Remove Users** page in the Admin portal is to process a [Data Subject Request for GDPR](../manage-security-and-compliance/gdpr-requests-in-viva-engage-enterprise.md). To remove a user from your Viva Engage Network, go to the [Azure AD User Management Portal](/azure/active-directory/fundamentals/add-users-azure-active-directory).

1. In Viva Engage, select the settings icon, and select **Edit Network admin Settings** to go to the Yammer admin center.

2. In the Yammer admin center, select **Users** \> **Remove Users**.
    
2. Enter an existing user's name. 
    
3. Select an action to take:
    
   - **Deactivate this user:**
 
      - If the user isn't using Azure AD credentials, this option blocks the user from signing in until they verify their email address again. Without access to their verified email account, they can't sign back in to Viva Engage. User profile information, messages, and file uploads remain. This can be a useful option for departing contract employees as they can be renewed when they return. Deactivated users can reactivate their account within 90 days by enabling their email account and signing in to Viva Engage, where they receive an email with links to reactivate. After 90 days, the account is permanently deleted.

      - If the user is using Azure AD credentials, first use this action to deactivate the user, and then follow the instructions in [Block users](#block-users).
    
   - **Permanently remove this user and keep messages:** This option lets you remove the user and retain the messages and content they posted. 
    
   - **Permanently remove this user and messages:** This option lets you remove the user and all the messages they posted. This can't be reversed. 
    
   - **Erase this user. Wipe their name and personal information, but leave their messages. (Can't be undone after 14 days):** This deactivates the user for 14 days so the admin can evaluate files and messages before the user is permanently deleted. 
    
   > [!NOTE]
   > This option is typically used for executing a GDPR data subject request. Before using this option, read [Manage GDPR data subject requests in Viva Engage](../manage-security-and-compliance/gdpr-requests-in-viva-engage-enterprise.md). For GDPR information for all of Office 365, see [Office 365 data subject requests for the GDPR.](/compliance/regulatory/gdpr-dsr-Office365). 
  
   All deletion options delete the following data:
    
   - Who the person is following, what conversations and articles they're following, and who's following them
    
   - Bookmarks, language preferences, notification settings, and account activity
    
   - User's profile
    
   - Group memberships
    
   - Org chart
    
   - The list of networks they were a member of
    
   The first three deletion options leave the user's name in stored Viva Engage data. The only way to remove the user's name is with the **Erase this user** option. 
    
4. Select **Submit**.
    
    Deactivated users are listed on the **Remove Users** page. You can reactivate or delete a user from this list. 
  
    :::image type="content" source="../../media/162b43ed-acd1-4085-8073-b43845c30999.png" alt-text="Screenshot of deactivated user list.":::
  
## Monitor account activity and device usage for a single user
<a name="AccountActivity"> </a>

1. In Viva Engage, go to **Users** \> **Account Activity**.
    
2. Type a user's name. You'll see what devices they're currently signed in on, when they last signed in on each device, and which IP address was used. 
    
    You can also sign the user out of the device from this list.
    
To monitor activity and device usage for your entire Viva Engage network, see [Office 365 Reports in the Admin Center - Viva Engage activity report](https://support.office.com/article/C7C9F938-5B8E-4D52-B1A2-C7C32CB2312A) and [Office 365 Reports in the Admin Center - Viva Engage device usage report](https://support.office.com/article/B793FFDD-EFFA-43D0-849A-B1CA2E899F38).
  
<a name="BlockUsers"> </a>
## Block users

 Users with blocked email addresses can't join your Viva Engage network unless you or another admin unblocks those addresses.

> [!NOTE]
> If your Viva Engage network is [in Native Mode](../overview-native-mode.md), this action can be performed only in the [Azure AD User Management Portal](/azure/active-directory/fundamentals/add-users-azure-active-directory) and not within the Viva Engage Admin portal.
  
There are two ways to block users from Viva Engage:
  
- **Block the user in the Yammer admin center:**
    
    1. In Viva Engage, select the settings icon, and select **Edit Network admin Settings** to go to the Yammer admin center.

    2. In the Yammer admin center, select **Users** \> **Block Users**.
    
    3. Enter the email address of the user to block. If you enter multiple email addresses, separate them with commas or line breaks. 

     If the user you select is in a suspended state in Viva Engage, blocking that email address puts the user in a deleted state. 
    
  > [!TIP]
  > Viva Engage is most effective when every post comes from an individual user. Therefore, you might want to block group email addresses. 
  
- **Block a user by removing their license and service plan, and remove the Viva Engage tile from Office 365:**
    
    - In the Microsoft 365 admin center, remove the **Viva Engage** license for the user. For steps, see [Turn off Viva Engage access for Office 365 users](turn-off-user-access.md) and see [Manage Viva Engage licenses in Office 365](manage-licenses-in-office-365.md).
  
## Related articles
  
[Manage a group in Viva Engage](https://support.office.com/article/6e05c6d6-5548-4c88-89cd-e6757a514ef2.aspx)

[Can I unsubscribe myself from Viva Engage?](https://support.office.com/article/981ecaf7-8a7d-4312-a845-bd343e925073)