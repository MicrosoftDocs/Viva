---
title: "Manage data in the Viva Engage admin center"
description: "Describes where and how admins can manage data in the Viva Engage admin center."
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: dmillerdyson
ms.date: 05/19/2023
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
localization_priority: Priority
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Manage data in the Viva Engage admin center

## Manage Data

As an Engage admin, you need to export data to manage users and content. This article explains the different options that can help you manage usage, compliance, and discovery.

>[!NOTE]
>To migrate data between Viva Engage tenants [learn about migrating content](/yammer/configure-your-yammer-network/add-basic-domains-to-office-365).

Choose from these data export methods to manage your data.

:::row:::
    :::column span="2":::
        **Export user and admin list**
    :::column-end:::
    :::column:::
        Identify the status of current admins and users. For each user, you get an email address, title, location, and department.
    :::column-end:::
:::row-end:::
:::row:::
    :::column span="2":::
        **Export Engage tenant data by date range and network**
    :::column-end:::
    :::column:::
        View and audit tenant data for all users from your home network for a specific date range. Options let you include attachment files and data from external networks.
    :::column-end:::
:::row-end:::
:::row:::
    :::column span="2":::
        **Export data for one user**
    :::column-end:::
    :::column:::
        Pull all data related to a single user. Use this method to identify data that needs to be deleted to comply with a GDPR data subject request.
    :::column-end:::
:::row-end:::
:::row:::
    :::column span="2":::
      **Automatic data exports**
 :::column-end:::
    :::column:::
        Automate recurring exports for compliance through the Data Export API.
    :::column-end:::
:::row-end:::
:::row:::
    :::column span="2":::
        **Export Engage files through the API**
    :::column-end:::
    :::column:::
        When exporting large volumes of files, use the API. You can specify a date range and include files from external networks. This method is best for archiving data.
    :::column-end:::
:::row-end:::

<br>
<br>

## Access the Data Export options

Use the Data export page in the admin portal to access all data exports.

1. Select the **Governance and compliance** tab.
2. Select **Data Export**. <br>

:::image type="content" source="../media/engage/admin/eac-data-export.png" alt-text="Use the Governance and compliance tab to find your data export options.":::


### Export user and admin list

Use this method to export data from a specific time period.

1. On the Data export page, choose **Export data for all** **users**.
2. Specify a date range and other options.
-  **Date range:**  Specify the date range for which you want data. The current date appears as the end date.
- **Include attachments:**  Leave unselected to get a list of file names. Select to get both a list and a Files folder of all the attachments in their native format.
- **Include external networks:**  Leave unselected to get data from your home network only. Select to get data for each network in a separate folder (folder name is the network ID). Full network names are listed in **Networks.csv**.

3. Select **Download CSV**. The file is saved as a compressed file with a .zip file name extension.
4. Go to the location where you saved the compressed file and expand it.
The data export contains the following files:

| **File** | **Contents** |
|---|---|
| **log.txt** | Summary of the export |
| **request.txt** | Parameters of the export |
| **Admins.csv** | Lists current admins, their email addresses, and corresponding roles <br>For more information on the types of admins in Viva Engage, see [Key admin roles in Viva Engage.](/viva/engage/eac-key-admin-roles-permissions) |
| **Networks.csv** | Information about your home network and any external networks, including name, URL, creation date, number of users, and whether it’s moderated or has a usage policy. |
| **Users.csv** | Lists user data. **Properties include:** ID, name, email, job title, location, department, user ID, deletion status (date, name and ID of the person who performed the deletion), join date, suspension status (date, name and ID of person who performed the deactivation), and the user state (active or soft_delete). A soft_delete is: **Pending**, if accompanied by no other values; **Suspended** (deactivated), if accompanied by a suspended_at and no deleted_at value; or **Deleted**, if accompanied by a deleted_at value. Identify Guests by an email address that doesn't match the home network domain. <br> <br>The **api_url** provides user metadata. For more information about using the data in this field, see the [REST API](https://go.microsoft.com/fwlink/?linkid=874691). |
| **Files folder** | Contains files that are stored in Viva Engage and were created or modified during the specified time period. Files are named with their account ID and are in native format. For example, a PowerPoint presentation might be listed as 127815379.pptx. | 

This data export doesn't include:
- Data available in the user's settings, including:
    - user profile 
    - tenants (networks) of which the user is a member
    - user account activity, applications, notifications, and language preference
    - org chart
- User activity data
- Bookmarked messages
- Group membership
- Followed or following users, or followed articles
- File attachments stored in SharePoint

<br>

### Export tenant data by date range

1. On the Data export page, select **Export tenant data.** 
2. Specify a date range and other options.

:::image type="content" source="../media/engage/admin/eac-tenant-options.png" alt-text="Export options let you choose a date range and other filters.":::
- **Date range:**  Includes only data in the specified date range. Today’s date is automatically prepopulated as the end date. 
- **Include attachments:**  If unselected, only a list of files is exported. If selected, a **Files** folder is exported containing all files in their native format. 
- **Include external networks:**  If unselected, only data from your home network is exported. If selected, a separate folder of data from each network is exported. Each network is identified by its ID, and the full network names are listed in **Networks.csv**. 

3. Select **Download CSV**.
Data is exported into a .zip file.
4. Go to the location where you saved the compressed file and expand it.<br>
If you exported more than one network, a separate folder is created for each network. <br>


The data export contains the following files:

| **File** | **Contents** |
|---|---|
| **log.txt** | Summary of the export |
| **request.txt** | The parameters of the export |
| **Admins.csv** | A list of admins for each selected network, including the name, email, and admin type |
| **Files.csv** | A list of file attachments that were added or modified within the date range. Files.csv doesn’t contain actual files. **Properties include:** account ID, type of file, name, description, and path to the file, and metadata that includes the group it was posted in. <br> <br>If **Include attachments** was selected, only files stored in Viva Engage are exported in native format to the **Files** folder of the zip file. <br> <br>**Note**: To download files from SharePoint, use the **download_url** column. <br>If SharePoint files have no Azure AD tokens, you must [create an Azure AD app](https://go.microsoft.com/fwlink/?linkid=2143320). Alternatively, use [Content Search in Office 365](/office365/securitycompliance/content-search) to find files in SharePoint for the specified date range. <br>To identify files in the **Files** folder, use **file_ID** and **path** columns. To access a specific file, see [Find and delete specific messages or files](/yammer/manage-security-and-compliance/export-yammer-enterprise-data). <br> <br>**Important:** When files are stored on Viva Engage and SharePoint, delete them from Viva Engage to remove metadata from both locations.    |
| **Groups.csv** | All groups created or modified during the specified date range. **Properties include:** account ID, name, description, privacy status, whether the group is internal or external, link to the group, who created the group, creation date, and updated date. |
| **Messages.csv** | All messages sent or modified during the specified date range. **Properties include:** message ID, thread ID, group ID, group name, GDPR deletion URL (**gdpr_delete_url**), privacy status, sender ID, name and email, the full body of the message, attachments, and creation and deletion information. <br>See [Find specific Viva Engage messages or files](/yammer/manage-security-and-compliance/export-yammer-enterprise-data). <br> |
| **MessageThreadsOutbound.csv** | Includes IDs of external participants in outbound messages. |
| **MessageVersions.csv** | Includes IDs and modification information for messages that have been edited. <br> |
| **Networks.csv** | Lists your home network and all external networks included in the export. <br> |
| **Pages.csv** | Lists IDs, dates, and page owners for any page created or modified during the specified date range. <br> |
| **Topics.csv** | Lists creation information and a link for any article created during the specified date range. |
| **Users.csv** | Lists data for all users who joined, or were deleted or suspended during the specified date range. **Properties include:** email address, job-title, location, department, a link to the user, and information about the user’s current state (active or soft_delete). <br>A soft_delete is: **Pending**, if accompanied by no other values; **Suspended** (deactivated), if accompanied by a suspended_at and no deleted_at value; or **Deleted**, if accompanied by a deleted_at value.<br> <br>Identify Guests by an email address that doesn't match the home network domain. <br> <br>The **api_url** provides user metadata. For more information about using the data in this field, see the [REST API](https://go.microsoft.com/fwlink/?linkid=874691). |
| **Files folder** | Contains files that are stored in Viva Engage and were created or modified during the specified time period. <br> <br>Files are named with their account ID and are in native format. For example, a PowerPoint presentation might be listed as 127815379.pptx. |

This data export doesn't include:
- Data in the user's settings (including profile, the tenants (networks) of which they're members, their account activity, applications, notifications, and language preferences, and their org chart)
- User activity data
- Bookmarked messages, group membership, followed or following users, or followed topics
- File attachments stored in SharePoint<br>

<br>

### Export data for one user

If the user is a member of multiple networks, you must export their data from each network separately.  

1. On the Data export page, choose **Export data for a single** **user** 

2. Enter the user's name, select the user, and select **Export**. <br>     User data is exported into a .zip file that contains these files. <br>
When the user's account activity data is ready, a message with a link to the data appears in your Viva Engage inbox.

3. Select the link to open it.

<br>

The data export contains the following files:

| **File** | **Contents** |
|---|---|
| **log.txt** | Summarizes the number of entries in each .csv file and lists any errors that occur during the export. |
| **request.txt** | Parameters used for the export |
| **Broadcast.csv** | Included if the user posted a live event video. Lists the network ID, group ID and name, title, description, links to the video, and additional information about the video. <br>Video content is excluded from the export. The video is saved in the OneDrive of the user who started the recording. To edit metadata or delete the video, you can open the video in Microsoft Stream admin mode. For more information,, see [Admin capabilities in Microsoft Stream](/stream/manage-content-permissions) and [Office 365 Data Subject Requests for the GDPR, Stream](/microsoft-365/compliance/gdpr-dsr-office365) |
| **Files.csv** | Lists all files added or modified by the user from Viva Engage. **Properties include:** account ID, type of file, name, description, and path to the file, along with metadata including the group it was posted in. The storage_path column shows whether the file is stored in Viva Engage or SharePoint. <br> Files that are stored in Viva Engage are exported in their native format to the **Files** folder of the zip file. Files that are stored in SharePoint aren't exported. <br> To identify files in the **Files** folder, use the file_ID and path columns. To go directly to a file, see [Delete specific messages or files](/yammer/manage-security-and-compliance/export-yammer-enterprise-data). <br> <br>To download files stored in SharePoint, use the download_url column. If SharePoint files have no Azure AD tokens, [you must create an Azure AD app](https://go.microsoft.com/fwlink/?linkid=2143320). Alternatively, find files stored in SharePoint for a specific date range with a [Content Search in Office 365](/office365/securitycompliance/content-search). <br>Always delete stored files from Viva Engage to erase the file and metadata in both SharePoint and Viva Engage. Deleting a file from SharePoint retains the metadata in Viva Engage. |
| **Groups.csv** | Lists all groups created or modified by the user. **Properties include:**  group ID, name, description, privacy status, whether internal or external, creation date, updated date, and a link to the group. <br>Additional information includes the aggregated total number of polls the user voted on, and the polls the user created. |
| **LikedMessages.csv** | Lists all messages liked by the user.**Properties include:**  message ID, thread ID, group ID, group name, privacy status, sender ID, name and email, the full body of the message, attachments*, and creation and deletion information. A list of polls you created are also provided. For announcements, includes the title of the announcement. Along with attachments, this Open Graph Object information is exported: ID, URL, title, and description. |
| **Messages.csv** | Lists all messages sent or modified by the user. **Properties include:** message ID, thread ID, group ID, group name, privacy status, sender ID, name and email, the full body of the message, attachments*, creation and deletion information. Also provides a list of polls the user created and titles of any posted announcements. <br>\*Along with attachments, this Open Graph Object (OGO) information is exported: ID, URL, title, and description. |
| **BestReplyMessages.csv** | Lists all messages marked as best reply by the user. **Properties include:** message ID, thread ID, group ID, group name, privacy status, sender ID, name and email address, the full body of the message, IDs for attachments, creation and deletion information. |
| **Topics.csv** | Lists all topics created by the user during the specified date range, including creation information and a link to the topic. |
| **Files folder** | Contains files stored in Viva Engage created or modified by the user during the specified time period. Engage files stored in SharePoint are excluded. <br> <br>Files are in native format and named with their account ID. For example, a PowerPoint presentation might be listed as 127815379.pptx. |

This data export doesn't include:<br>
- Bookmarked messages
- Group membership or org chart
- Followed users, following users, followed topics
- User notifications from Viva Engage (or in Microsoft Teams or Microsoft Outlook)
- Application and language settings<br>  

>[!NOTE] 
>Data for the user’s skin tone selection is excluded from exported data. However, you can access the skin tone selection on any post in Viva Engage that includes a reaction by the user. Open the grouped modal dialog box for that specific post or comment, and view the user's skin-tone preference in the list.

### Troubleshoot data export

If the .zip file is corrupted and can't be unzipped, try again. If the file still doesn't expand, [contact Support](https://support.office.com/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b). 

If the log.txt file shows export errors for one category of data, try again. If there are still errors, [contact Support](https://support.office.com/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b). 

### Automate your data exports

To set up automatic recurring exports, use the API. For more information, see [Data Export API. ](/rest/api/yammer/yammer-files-export-api)<br>

### Export large file volumes with the API

Verified administrators can use the Data Export API to archive and export files in Viva Engage storage asynchronously. This API is intended for exporting large volumes of files from Viva Engage. For more information, see [Data Export API. ](/rest/api/yammer/yammer-files-export-api)

### See also

[Access the Viva Engage admin center](/Viva/engage/eac-as-access-eac)

[Key admin roles and permissions in Viva Engage](/Viva/engage/eac-key-admin-roles-permissions)

[Set up the Viva Engage admin center](/Viva/engage/eac-get-started)
