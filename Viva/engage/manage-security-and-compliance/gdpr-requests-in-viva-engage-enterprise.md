---
title: "Manage GDPR data subject requests in Viva Engage Enterprise"
f1.keywords:
- NOCSH
ms.author: dmillerdyson
author: cedemaagd
manager: elizapo
ms.date: 08/28/2023
audience: Admin
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: medium
search.appverid:
- MET150
- MOE150
ms.assetid: eae49f12-4661-4ba5-aa72-01248f0709bf
description: "Erase all information about a Viva Engage user to comply with GDPR data subject requests."
---

# Manage GDPR data subject requests in Viva Engage Enterprise

As a verified admin, you can erase a user from Viva Engage to comply with a [General Data Protection Regulation (GDPR) data subject request](/compliance/regulatory/gdpr-dsr-Office365). When you erase a user, personally identifying information about the user is removed, but the user's messages and files remain. You can review a user's messages and files to decide which ones to delete. Content that remains is identified with an ID, not with the user's name.

Choose the approach that makes sense for your situation, and **follow the steps in the order listed**. The order matters: after you erase a user, you can no longer find their data to delete it.

| Approach | Steps |
| :----- | :----- |
|Keep all messages and files created by the user.|Remove the user by using the **Erase the user** option. This removes the user from the home tenant and any external tenants they belong to, but doesn't delete any of their messages or files.|
|Delete all messages created by the user and decide which files to delete|1. Do one per-user export of the user's data for the home tenant, and one for each external tenant they belong to.<br>2. Remove the user from each tenant by using the **Permanently remove this user, and remove their messages** option.<br>3. In the home tenant, use the **Erase the user** option.<br>4. Within 14 days, remove any files stored in Viva Engage in the home tenant as necessary, and any information not included in the per user export.*|
|Review files and messages created by the user and decide which to keep and which to delete|1. Do one per-user export of the user's data for the home tenant, and one for each external tenant they belong to. <br>2. In the home tenant, use the **Erase this user** option. <br>3. Within 14 days, remove any files or messages as necessary from the home tenant, and any information not included in the per user export.*|

 \* If you prefer to have more than 14 days to review and delete files and messages, you can do this prior to erasing the user.

> [!IMPORTANT]
> Closing a Microsoft Entra ID account doesn't delete the user and their information. To delete user information, go the Viva Engage admin center and complete the instructions provided below.

<a name="DeleteMessagesFiles"> </a>

## Delete specific messages or files

Use the Viva Engage file ID from the export to go directly to the file in Viva Engage and delete it.

> [!IMPORTANT]
> For Viva Engage files stored in SharePoint, delete the files from Viva Engage in order to remove the Viva Engage metadata as well as the file.
  
**To locate and delete a specific message:**

1. In the data export, find the URL for the message in the **gdpr_delete_url** column. The URL has this syntax: **https&#58;//www&#46;yammer&#46;com**/*network_name*/**#**/**Threads**/**show?threadId=** *thread_id*. For example, http&#58;//www&#46;yammer&#46;com/contosomkt&#46;onmicrosoft&#46;com/#/threads/show?threadID=135893.
  
2. In the message, select the **More** icon :::image type="icon" source="../../media/d9378a9a-fb0a-4313-96e5-bc6c9f1d5827.png" border="false":::, and then select **GDPR Hard Delete**.

**To locate and delete a specific Viva Engage file stored in Viva Engage or SharePoint:**

  1. Use the **Search** box in Viva Engage. For example, for a file named 12345678.pptx in the export, search for 1235678.pptx. In the search results, select **Go to File**, and then select **Delete this File**.

  1. You can also build the URL for the file. Use **https&#58;//www&#46;yammer&#46;com**/*network_name*/**#**/**files**/*file_number*, for example https&#58;//www&#46;yammer&#46;com/contosomkt&#46;onmicrosoft&#46;com/#/files/12345678. On the Viva Engage page for the file, select **Delete this File**.

**To delete the cover images for a user:**
> [!NOTE]
> In cases where the admin or the user are not premium licensed, and/or the user no longer has their own storyline, previously uploaded photos will need to be deleted via API.

 1. Via API: Engage Admins or verified admins can delete cover images for any user in their tenant via an API call. The URL has this syntax: www&#46;yammer&#46;com/api/public/v1/user-profiles/*user_id*/cover-image.

      For example, to delete the cover images of a user with ID 1234567890, the URL would look like: www&#46;yammer&#46;com/api/public/v1/user-profiles/1234567890/cover-image.

 2. Via UI: Engage Admins with premium Viva licenses can upload or delete cover photos for any user who has the premium Viva license and has storyline enabled by:

     1. Visiting the profile page of the user.
     2. Hovering your mouse over the profile header and selecting **"Upload cover photo"**.
     3. Deleting or uploading a new cover image, as needed.

<a name="OtherData"> </a>
## Find and delete user data not included in the per-user export

There's some user data that isn't included in an export.

To find this data for a user, go to Viva Engage settings :::image type="icon" source="../../media/9704ce70-56ce-43f7-96c6-f253b0413d40.png" border="false"::: \> **People**, and select the name of the user.
  
The following table shows how to change or delete this data if needed.
  
****

| Type of data | How to change or delete it |
|:-----|:-----|
|Bookmarked messages, group membership, followed or following users, and followed topics |When you [erase a user from the Viva Engage home tenant and external tenants](gdpr-requests-in-viva-engage-enterprise.md#RemoveUser), this information is deleted after the 14-day suspension period. <br><br> A user can change or delete this information. For steps, see [Tips for staying organized in Viva Engage](https://support.office.com/article/40ae9666-75c0-4254-a84c-d87a9542f380.aspx). |
|User settings, including notification, application, and language settings |When you [erase a user from your Viva Engage home tenant and external tenants](gdpr-requests-in-viva-engage-enterprise.md#RemoveUser), this information is deleted after the 14-day suspension period. As an admin, you can't change this information for a user.<br><br>However, a user can change their own settings. For steps, see [Change my Viva Engage profile and settings](https://support.office.com/article/a3aeca0e-de34-4897-9b59-de6516542851.aspx). |
|User profile | If the user has a Viva Engage identity, there are two options to remove the user: <ul><li>When you [erase a user from your Viva Engage home tenant and external tenants](gdpr-requests-in-viva-engage-enterprise.md#RemoveUser), this information is deleted in Viva Engage after the 14-day suspension period.</li><li>The user has full control of their own profile and can modify the values. For information, see [Edit the user's profile and settings (done by user)](gdpr-requests-in-viva-engage-enterprise.md#EditProfile).</li></ul> If the user has a Microsoft 365 identity, the Viva Engage user profile is pulled from Microsoft 365, which gets the information from Microsoft Entra ID. Viva Engage users can temporarily change their profiles in Viva Engage. If a change occurs in Microsoft Entra ID, their changes are overwritten. To permanently change or delete a user's profile, you must change or delete directory data in Microsoft 365 and Microsoft Entra ID. See [Manage Viva Engage users across their lifecycle from Microsoft 365](https://support.office.com/article/365-6c4c8fff-6444-404a-bffc-f9da0bcc3039.aspx) and [Add or change profile information for a user in Microsoft Entra ID](/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal). |

<a name="EditProfile"> </a>
## Edit the user's profile and settings (done by user)

A user can edit their own profile. Administrators can't change the user profile or settings.
  
- The user can select the Viva Engage settings icon :::image type="icon" source="../../media/9704ce70-56ce-43f7-96c6-f253b0413d40.png" border="false":::, and then select **Edit Settings**.

- Select the tab for the change you want to make:

  - To change your profile, select **Profile**.

  - To change your password, select **Password**.

  - To edit your notifications, select **Networks**.

  - To see your account activity, select **Account Activity**.

  - To see what applications you installed, select **My Applications**.

  - To set preferences, select **Preferences**.

<a name="RemoveGroup"> </a>
## Remove a user from a group including an external group

1. In the group, select **Members**.

2. Select the Settings icon :::image type="icon" source="../../media/9704ce70-56ce-43f7-96c6-f253b0413d40.png" border="false"::: next to the user's name.

3. Select **Remove from group**.

## Remove an external participant from a conversation
<a name="RemoveThread"> </a>

- In the Viva Engage conversation, select **Remove Participants**.

<a name="RemoveUser"> </a>

## Erase a user from your Viva Engage home tenant and external tenants

> [!IMPORTANT]
> When you erase a user, there is a 14-day window for you to decide which files and messages to save or delete in the home tenant before the user-identifying data is completely erased. If you want to review and delete some or all of the user's messages and files, be sure to export user data and do the deletions before erasing the user's account, or within 14 days after selecting **Erase this user**. After the 14-day window, files and messages will continue to exist but will be marked as belonging to a former user.<br><br>After a user's account transitions from deactivated to removed, you can't associate user data with that user, which means you can no longer export and review their data.

> [!IMPORTANT]
> If you want to review and delete messages and files in external groups, external threads, and tenants that the user is a guest member in, follow the instructions in [Delete specific messages or Viva Engage files stored in Viva Engage or SharePoint](gdpr-requests-in-viva-engage-enterprise.md#DeleteMessagesFiles) *before*  erasing the user. After you select **Erase this user**, you can no longer associate the user with these messages and files.

> [!IMPORTANT]
> Removing a user from their home Viva Engage tenant removes them from all external tenants. You must remove guest users separately in each external tenant they're a member of.
  
When you erase a user, the following user data is deleted:
  
- Who the person is following, the connection to conversations and topics they were following, and the connection to users who were following them

- Bookmarks, language preferences, notification settings, and account activity

- Profile

- Group memberships

- The list of tenants they were a member of

As an admin, you can erase a user from your home tenant and from any external tenants they belong to.
  
**Remove a user (done by admin)**
  
1. In the Viva Engage admin center, go to **Users** \> **Remove Users**.

2. Enter an existing user's name. After you select the user, the options for removal are displayed.

    :::image type="content" source="../../media/a48da79c-7f5f-479b-8b75-a3e67285c141.png" alt-text="Screenshot that shows how selecting a name presents options to remove the user.":::

    - If you want to delete all of a user's messages before you erase the user:

      1. Select **Permanently remove this user and remove their messages**, and then select **Submit**.
      2. When that completes, select **Erase this user**. This removes the user's name and activity data.

    - If you want to keep all the user's files and messages, select **Erase this user**.

    - If you want to review the user's messages and files (and you've already deleted messages and files in external groups, threads, or tenants the user is a guest member in) then do these steps:

      1. Deactivate the user for 14 days to export their user data and evaluate their home tenant files and messages by selecting **Erase this user. Wipe their name and personal information, but leave their messages. (Can't be undone after 14 days):** 

         The user is marked as deactivated and is listed on the **Remove Users** page. Within 14 days, you can reactivate the user.

         :::image type="content" source="../../media/162b43ed-acd1-4085-8073-b43845c30999.png" alt-text="Screenshot of deactivated user list.":::

         After 14 days, a message is sent to all the tenant admins and verified admins informing them the user has been deleted.

      2. Select **Submit**.

      3. In the confirmation dialog, select **Yes, Permanently Delete Account**.

      4. Within the 14 days, follow the directions in [Delete specific messages or files](gdpr-requests-in-viva-engage-enterprise.md#DeleteMessagesFiles).

<a name="Reactivate"> </a>

## Reactivate a deactivated account after using Erase this user

When a user's account is deactivated using the **Erase this user** option, you have 14 days to reactivate the user.
  
1. Go to the Viva Engage Admin center.

2. Select **Remove Users**.

3. Go to the **Deactivated Users** section. This section is only visible when there's at least one deactivated user account.

4. Select **Reactivate** for each user you want to reactivate.

   After 14 days, the user cannot be reactivated.

## See also

[Manage Viva Engage data compliance](manage-data-compliance.md)
  
[Export data from the Viva Engage admin center](/viva/engage/eac-as-manage-data)
