---
title: "Manage data in the Viva Engage admin center"
description: "Describes where and how admins can manage data in the Viva Engage admin center."
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 4/04/2024
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Export and manage Viva Engage data 

Engage administrators often need to export data to manage users and content in the network. This article explains the different options available to help you manage usage, compliance, and discovery.

## Export data

>[!NOTE]
>To migrate data between Viva Engage tenants, [learn about migrating content](/viva/engage/configure-your-viva-engage-network/add-basic-domains-to-office-365).

| Use this data export method | For this purpose |
|---|---|
|  [**Export user and admin list**](#export-user-and-admin-list)  |  Identify the status of current admins and users. For each user, you get an email address, title, location, and department. |
|  [**Export tenant data by date range**](#export-tenant-data-by-date-range) | View and audit tenant data for all users from your home network for a specific date range. Options also let you include attachment files and data from external networks. |
|  [**Export data for one user**](#export-data-for-one-user) | Pull all data related to a single user. Use this method to identify data that needs to be deleted to comply with a GDPR data subject request.|
|  [**Automate data exports**](#automate-data-exports) | Automate recurring exports for compliance through the Data Export API. |
|  [**Export Engage files with the API**](#export-large-volumes-of-files-with-the-api) |  When exporting large volumes of files, use the API. You can specify a date range and include files from external networks. This method is best for archiving data. |


## Access data export options

Access all export options from the Data export page in the Engage admin portal.

1. Select the **Governance and compliance** tab.
2. Select **Data Export**.

   :::image type="content" source="../media/engage/admin/eac-data-export.png" alt-text="Screenshot shows the Governance and compliance tab where you can find your data export options.":::

## Export user and admin list

Use this method to export data from a specific time period.

1. On the Data export page, choose **Export data for all** **users**.
2. Specify a date range and other options.

   - **Date range:**  Specify the date range for which you want data. The current date appears as the end date.
   - **Include attachments:**  Leave unselected to get a list of file names. Select to get both a list and a Files folder of all the attachments in their native format.
   - **Include external networks:**  Leave unselected to get data from your home network only. Select to get data for each network in a separate folder (folder name is the network ID). Full network names are listed in **Networks.csv**.

3. Select **Download CSV**. The file is saved as a compressed file with a .zip file name extension.
4. Go to the location where you saved the compressed file and expand it.
The data export contains the following files:

   | File | Contents |
   |---|---|
   | **log.txt** | Summary of the export |
   | **request.txt** | Parameters of the export |
   | **Admins.csv** | Lists current admins, their email addresses, and corresponding roles <br>For more information on the types of admins in Viva Engage, see [Manage admin roles in Viva Engage.](/viva/engage/eac-key-admin-roles-permissions) |
   | **Answers.csv** | Lists the ID, messageId, networkId, threadId, voterID, createdAt timestamp and updatedAt timestamp of Answer Votes |
   | **Campaigns.csv**| Provides data for campaigns including hashtag, creation date, state and so on. The scope_type attribute distinguishes official (network) campaigns versus community (group) campaigns. The scope_id attribute identifies the network or community that hosted the community campaign. Find more campaign details about the network or community in the networks.csv file or groups.csv file, respectively.|
   | **Networks.csv** | Information about your home network and any external networks, including name, URL, creation date, number of users, and whether it’s moderated or has a usage policy. |
   | **Users.csv** | Lists user data. **Properties include:** ID, name, email, job title, location, department, user ID, deletion status (date, name, and ID of the person who performed the deletion), join date, suspension status (date, name, and ID of person who performed the deactivation), and the user state (active or soft_delete). A soft_delete is: **Pending**, if accompanied by no other values; **Suspended** (deactivated), if accompanied by a suspended_at and no deleted_at value; or **Deleted**, if accompanied by a deleted_at value. Identify Guests by an email address that doesn't match the home network domain. <br> <br>The **api_url** provides user metadata. For more information about using the data in this field, see the [REST API](/rest/api/yammer/rest-api-rate-limits). |
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

## Export tenant data by date range

Use this method to export data for the Viva Engage network.

>[!IMPORTANT]
>If you're on a large network (10,000 or more users) and experience time-out errors when running a network export job, we recommend that you: choose hours outside of standard operating hours to export, and limit the date range to no more than one month.

1. On the Data export page, select **Export tenant data**.
2. Specify a date range and other options.

   :::image type="content" alt-text="Screenshot of export options including date range and other filters." source="../media/engage/admin/eac-tenant-options.png" lightbox="../media/engage/admin/eac-tenant-options.png":::

   - **Date range:**  Includes only data in the specified date range. Today’s date is automatically prepopulated as the end date.
   - **Include attachments:**  If unselected, only a list of files is exported. If selected, a **Files** folder is exported containing all files in their native format.
   - **Include external networks:**  If unselected, only data from your home network is exported. If selected, a separate folder of data from each network is exported. Each network is identified by its ID, and the full network names are listed in **Networks.csv**.

3. Select **Download CSV**.
Data is exported into a .zip file.
4. Go to the location where you saved the compressed file and expand it.

   If you exported more than one network, a separate folder is created for each network.

The data export contains the following files:

| File | Contents |
|---|---|
| **log.txt** | Summary of the export |
| **request.txt** | The parameters of the export |
| **Admins.csv** | A list of admins for each selected network, including the name, email, and admin type |
| **Campaigns.csv**| A list of all campaigns on the network. **Properties include:** creation name, URL, hashtag, creation date, creator ID, and state.|
|**EngageTopicMigrationLog.csv**|A list of topics migrated or not imported from Viva Topics or lightweight topics to Viva Engage. **Properties include:** Cortex_topic_ID, migrated_at, migrated_action|
|**EngageTopicApplicationMigrationLog.csv**|A list of topic applications not imported from Viva Topics or lightweight topics to Viva Engage. **Properties include:** Cortex_topic_id, target_id, target_type, migrated_at, migration_action|
| **Files.csv** | A list of file attachments that were added or modified within the date range. Files.csv doesn’t contain actual files. **Properties include:** account ID, type of file, name, description, and path to the file, and metadata that includes the group it was posted in. <br> <br>If **Include attachments** was selected, only files stored in Viva Engage are exported in native format to the **Files** folder of the zip file. <br> <br>**Note**: To download files from SharePoint, use the **download_url** column. <br>If SharePoint files have no Microsoft Entra tokens, you must [create a Microsoft Entra app](https://go.microsoft.com/fwlink/?linkid=2143320). Alternatively, use [Content search in Microsoft 365](/purview/ediscovery-content-search) to find files in SharePoint for the specified date range. <br>To identify files in the **Files** folder, use **file_ID** and **path** columns. <br> <br>**Important:** When files are stored on Viva Engage and SharePoint, delete them from Viva Engage to remove metadata from both locations.    |
| **Groups.csv** | All groups created or modified during the specified date range. **Properties include:** account ID, name, description, privacy status, whether the group is internal or external, link to the group, who created the group, creation date, and updated date. |
| **Messages.csv** | All messages sent or modified during the specified date range, including messages created from files (using Intelligent Importer). **Properties include:** message ID, thread ID, group ID, group name, GDPR deletion URL (**gdpr_delete_url**), privacy status, sender ID, name and email, the full body of the message, attachments, creation and deletion information, and draft state. |
| **MessageThreadsOutbound.csv** | Includes IDs of external participants in outbound messages. |
| **MessageVersions.csv** | Includes IDs and modification information for messages that have been edited. |
| **Networks.csv** | Lists your home network and all external networks included in the export. |
| **Pages.csv** | Lists IDs, dates, and page owners for any page created or modified during the specified date range. |
| **Topics.csv** | Lists creation information and a link for any article created during the specified date range. |
| **Users.csv** | Lists data for all users who joined, or were deleted or suspended during the specified date range. **Properties include:** email address, job-title, location, department, a link to the user, and information about the user’s current state (active or soft_delete). <br>A soft_delete is: **Pending**, if accompanied by no other values; **Suspended** (deactivated), if accompanied by a suspended_at and no deleted_at value; or **Deleted**, if accompanied by a deleted_at value.<br> <br>Identify Guests by an email address that doesn't match the home network domain. <br> <br>The **api_url** provides user metadata. For more information about using the data in this field, see [the REST API](/rest/api/yammer/rest-api-rate-limits). |
|**VivaTopicApplications.csv** | For any topic applied to a post, lists information about each application for the date range specified (if any). |
|**VivaTopicCurationStateLogs.csv** | Applies to only Answers in Viva. <br><br/>Contains the curation state logs for featured topics.<br><br/>cortex_topic_id can be used with the content of VivaTopics.csv to retrieve other information relevant to the topic. |
|**VivaTopics.csv** | Any topic created or updated is displayed for the date range specified (if any).<br><br/>The ID refers to the Viva Topic identifier.<br><br/>The api_url is the URL used to obtain the topic metadata.|
| **Files folder** | Contains files that are stored in Viva Engage and were created or modified during the specified time period. <br> <br>Files are named with their account ID and are in native format. For example, a PowerPoint presentation might be listed as 127815379.pptx. |

This data export doesn't include:

- Data available in the user's settings, including:
  - user profile
  - tenants (networks) of which the user is a member
  - user account activity, applications, notifications, and language preference
  - org chart
- User activity data
- Bookmarked messages
- Group membership
- Followed or following users, or followed topics
- File attachments stored in SharePoint<br>

## Export data for one user

If the user is a member of multiple networks, you must export their data from each network separately.  

1. On the Data export page, choose **Export data for a single** **user**

2. Enter the user's name, select the user, and select **Export**. <br>     User data is exported into a .zip file that contains these files. <br>
When the user's account activity data is ready, a message with a link to the data appears in your Viva Engage inbox.

3. Select the link to open.


The data export contains the following files:

| File | Contents |
|---|---|
| **log.txt** | Summarizes the number of entries in each .csv file and lists any errors that occur during the export. |
| **request.txt** | Parameters used for the export |
| **Broadcast.csv** | Included if the user posted a live event video. Lists the network ID, group ID and name, title, description, links to the video, and additional information about the video. <br>Video content is excluded from the export. The video is saved in the OneDrive of the user who started the recording. To edit metadata or delete the video, you can open the video in Microsoft Stream admin mode. For more information, see [Admin capabilities in Microsoft Stream](/stream/manage-content-permissions) and [Microsoft 365 Data Subject Requests for the GDPR](/microsoft-365/compliance/gdpr-dsr-office365). |
| **Files.csv** | Lists all files added or modified by the user from Viva Engage. **Properties include:** account ID, type of file, name, description, and path to the file, along with metadata including the group it was posted in. The storage_path column shows whether the file is stored in Viva Engage or SharePoint. <br> Files that are stored in Viva Engage are exported in their native format to the **Files** folder of the zip file. Files that are stored in SharePoint aren't exported. <br> To identify files in the **Files** folder, use the file_ID and path columns. <br> <br>To download files stored in SharePoint, use the download_url column. If SharePoint files have no Microsoft Entra tokens, [you must create a Microsoft Entra app](https://go.microsoft.com/fwlink/?linkid=2143320). Alternatively, find files stored in SharePoint for a specific date range with a [Content Search in Microsoft 365](/office365/securitycompliance/content-search). <br>Always delete stored files from Viva Engage to erase the file and metadata in both SharePoint and Viva Engage. Deleting a file from SharePoint retains the metadata in Viva Engage. |
| **Groups.csv** | Lists all groups created or modified by the user. **Properties include:**  group ID, name, description, privacy status, whether internal or external, creation date, updated date, and a link to the group. <br>Additional information includes the aggregated total number of polls the user voted on, and the polls the user created. |
| **LikedMessages.csv** | Lists all messages liked by the user.**Properties include:**  message ID, thread ID, group ID, group name, privacy status, sender ID, name and email, the full body of the message, attachments*, and creation and deletion information. A list of polls you created are also provided. For announcements, includes the title of the announcement. Along with attachments, this Open Graph Object information is exported: ID, URL, title, and description. |
| **Messages.csv** | Lists all messages sent or modified by the user, including messages generated from files (using Intelligent Importer). **Properties include:** message ID, thread ID, group ID, group name, privacy status, sender ID, name and email, the full body of the message, attachments, creation and deletion information, and draft state. Also provides a list of polls the user created and titles of any posted announcements. <br>Along with attachments, this Open Graph Object (OGO) information is exported: ID, URL, title, and description. |
| **BestReplyMessages.csv** | Lists all messages marked as best reply by the user. **Properties include:** message ID, thread ID, group ID, group name, privacy status, sender ID, name and email address, the full body of the message, IDs for attachments, creation, and deletion information. |
| **Topics.csv** | Lists all topics created by the user during the specified date range, including creation information and a link to the topic. |
|**VivaTopicApplications.csv** | For any topic applied to a post, lists information about each application for the date range specified (if any). |
|**VivaTopicCurationStateLogs.csv** | Applies to only Answers in Viva. <br><br/>Contains the curation state logs for featured topics.<br><br/>cortex_topic_id can be used with the content of VivaTopics.csv to retrieve other information relevant to the topic. |
|**VivaTopics.csv** | Any topic created or updated is displayed for the date range specified (if any).<br><br/>The id refers to the Viva Topic identifier.<br><br/>The api_url is the URL used to obtain the topic metadata.|
| **Files folder** | Contains files stored in Viva Engage created or modified by the user during the specified time period. Engage files stored in SharePoint are excluded. <br> <br>Files are in native format and named with their account ID. For example, a PowerPoint presentation might be listed as 127815379.pptx. |

This data export doesn't include:

- Bookmarked messages
- Group membership or org chart
- Followed users, following users, followed topics
- User notifications from Viva Engage (or in Microsoft Teams or Microsoft Outlook)
- Application and language settings

>[!NOTE]
>Data for the user’s skin tone selection is excluded from exported data. However, you can access the skin tone selection on any post in Viva Engage that includes a reaction by the user. Open the grouped modal dialog box for that specific post or comment, and view the user's skin-tone preference in the list.

## Export topics created in Viva Engage with PowerShell

Using PowerShell, you can export topics created by a user in Viva Engage (also known as Lite Topics) to a .csv file. Topics include those created before enabling integration with Viva Engage. For more information, see [Export topics created in Viva Engage with PowerShell](/viva/topics/export-topics-powershell).

## Troubleshoot data export

If the .zip file is corrupted and can't be unzipped, try again. If the file still doesn't expand, [contact Support](https://support.office.com/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b).

If the log.txt file shows export errors for one category of data, try again. If there are still errors, [contact Support](https://support.office.com/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b).

## Automate data exports

To set up automatic recurring exports, use the API. For more information, see [Data Export API.](/rest/api/yammer/rest-api-rate-limits)<br>

## Export large volumes of files with the API

Verified administrators can use the Data Export API to archive and export files in Viva Engage storage asynchronously. This API is intended for exporting large volumes of files from Viva Engage. For more information, see [Data Export API.](/rest/api/yammer/rest-api-rate-limits)

### See also

[Overview of the Viva Engage admin center](/Viva/engage/eac-overview)

[Manage administrator roles in Viva Engage](/Viva/engage/eac-key-admin-roles-permissions)

[Set up the Viva Engage admin center](/Viva/engage/eac-get-started)
