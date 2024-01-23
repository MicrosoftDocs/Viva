---
title: FAQs in SharePoint
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 01/23/2024
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - highpri
  - Tier1
localization_priority: medium
description: FAQs and error codes in SharePoint.
---

# SharePoint in Viva Learning Frequently Asked Questions

This article outlines error codes and FAQs for SharePoint in Viva Learning.
 
If the ingestion status is showing success and content is still not visible in the Viva Learning app, download export logs:

1. Go to the admin tab in Viva Learning
2. Select **SharePoint**. 
3. Select **More options.** Select **Export logs**.
4. In **Logs,** check the **Sync summary** tab.

In case the `TotalObjectCount` is zero.

1. Check if you added folder URLs in Learning app repository.
2. Go to the admin tab.
3. Select more options for SharePoint.
4. Select edit and copy the URL.
5. Open the site URL and go to site contents, then the Learning app repository.
6. Add the folder URLs.

In case `SuccessfulSyncedObjectsCount` isn't zero and you still can’t see the content in Viva Learning app:

1. Check if you're added as a member of the [applied group](https://admin.microsoft.com/Adminportal/Home#/groups/:/TeamDetails/e813e5d8-d251-4024-a6b0-276bc39eecff/Members).

2. Check if Mail enabled security group is applied to the folder or file. You can check the group type at the [Microsoft Entra admin center](https://entra.microsoft.com).

3. If you added a security group, check if the security group is mail enabled. 
    1. Security groups without main enabled are 'global groups.' To mail enable them, convert them to a [universal group](/previous-versions/windows/it-pro/windows-server-2003/cc755692(v=ws.10)) and then add an email for the group.  

 
In case `FailedObjectsCount` isn't zero check the **Failed Object Details** tab, refer to the following error messages:


|Error code | Error description | Next Steps | 
| - | - | - | 
| `SP_INVALID_FOLDER_URL` | The folder url isn't valid. Only folder-URL are supported. Adding document libraries directly isn't supported. | Add the files in a folder and add the folder URL in the learning app repository. Read the configure SharePoint content source [documentation](/viva/learning/configure-sharepoint-content-source#folder-url-document-library-curation)
|`SP_NO_M365_PERMISSIONS_FOUND` | Every item needs to have Microsoft 365 group or Mail-enabled security group (MESG) to light-up inside Viva Learning. | <br> Apply [Microsoft 365 group](sharepoint-permissions.md) or Mail-enabled security group directly to the folder. <br> Open the folder and for a file check if the Microsoft 365 group or Mail-enabled security group (MESG) group is directly applied on the file items. </br> <br> To check if group is directly applied to the folder/file item: <li> In SharePoint go to the folder or file and select **More options** > **Manage access** > **More options** > **Advanced settings**. <li> Check whether the group you added is listed and has "Domain Group" as its Type. <br> <li> Check the group type at the Microsoft Entra admin center.|
|`SP_ITEM_LIMIT_REACHED`| Only 1000 files or items can be ingested as learning objects | Purchase a Microsoft Viva Suite or Viva Learning license. | 
| `SP_ITEM_INGESTION_FAILED` | | Raise a [support ticket](/services-hub/unified/support/open-support-requests).| 


- **What type of site URLs can be added?** 
    - You can use either a Teams site or a communication site. We recommend using a communication site.

- **Why is the display name is not updated?**
    - Only site owners with the knowledge admin or global admin role can update the display name.
    - The change can take 24 hours to reflect.

- **What is the limit on the number of file items that can be ingested?**
    - Viva Learning ingests up to 1000 files as learning objects. A Viva Suite or Viva Learning license is required to ingest more than 1000 files as learning objects. 

- **In what order are the files ingested?**
    - The first 1000 items with earliest last modified date are ingested.
    - For example: A customer has items A, B, and C, and they created or uploaded them in the sequence A, B, and C. The earliest last modified date belongs to A, followed by B, and then C. Therefore, when restricted to only two items, we only include A and B in our collection and C is discarded.

- **Why am I unable to add a M365 group or mail-enabled security group (MESG)?**
    - A Microsoft 365 group or mail-enabled security group (MESG) group can't be added directly to the file or folder in case the group is found on the folder or file nested in SharePoint groups. If it's already present, remove it and add directly or add a different group.
    - To see if a group is already present, select the folder, then **Manage access** > **Advanced settings** > **Check permission**.

- **What can I do if my content is not visible?**  
    1. Go to the SharePoint site added in the **Admin tab** > **Manage provider** > **SharePoint**.
    2. Go to site contents and in the Learning app repository, check if the folder URLs are present.
    3. Check if the Microsoft 365 or mail-enabled security group is applied directly to the folder.
        1. In SharePoint, go to the folder and select **More options** > **Manage access** > **More options** > **Advanced settings**. Check whether the group you added is listed and has "Domain Group" as its Type. You can check the group type in the [Microsoft Entra admin center](https://entra.microsoft.com).
        1. Check if you're added as a member of the [applied group](https://login.microsoftonline.com/common/oauth2/authorize?client_id=00000006-0000-0ff1-ce00-000000000000&response_type=code+id_token&scope=openid+profile&state=OpenIdConnect.AuthenticationProperties%3dbHvyF-kZif3K7SyNj2ScGHQFpHpoRU_qMKYXtjhNzC6aH1DUWi_7XSuzYQS7JxBVXBvZogIzp3x0DvZWJHC_0Uq6JFHTseAKZT7Na3Gd9eiqaBUgogXajEhSg8zKPAiSKq8sL6CoDhRVLx5JNhS7YnNXt68KdPRtCJIAXGNxJgYsnVCQqXfmtgLyzWEWTG5IMX7_n1YPICQbn9f5qeBo1zyDnQzgfwnB5Ke7A3Z8n96XaRSQ9Zp4LUwApDPVb-qT&response_mode=form_post&nonce=638411368973289679.ZDczYjQyODItYzZhOS00NTg4LTk2NmQtNTYzZmFhYWJjOTNiZjFmOGZlMDAtMDM3Mi00MGMwLWE0NjctNDMxZDE1ZGEwOTgz&redirect_uri=https%3a%2f%2fadmin.microsoft.com%2flanding&ui_locales=en-US&mkt=en-US&client-request-id=dc00ca38-de9f-4ba2-b0d2-e5feda954810&x-client-SKU=ID_NET472&x-client-ver=6.34.0.0&sso_nonce=AwABAAEAAAACAOz_BQD0_54Xy0NptLyMJ2RNuNKBrhlrtk3CdnROqgoPjkuGLWsbcgcUprEEZNjX9hzfnwJF1Ja9c1Ad3FdTxR2V0YzcyoQgAA&mscrid=dc00ca38-de9f-4ba2-b0d2-e5feda954810).
    4. Open the folder and check if Microsoft 365 or mail-enabled security group (MESG) group is directly applied on the file items.  
    
> [!NOTE]
> Check if the permission is propagating to file items present in the folder. A site owner or contributor role is required on the site for the permissions to propagate to the dependent item.

- **How can I make a security group mail-enabled**? 

    - Security groups without mail enabled are global groups. To mail-enable them, convert them to a [universal group](/previous-versions/windows/it-pro/windows-server-2003/cc755692(v=ws.10)) and then add an email for the group. 

- **What can I do if the metadata isn't reflecting properly?**

    1. Check the [column names](/viva/learning/configure-sharepoint-content-source#metadata)
    2. If they're not correct, delete and recreate the column.

- What size do the thumbnails have to be to properly render in Viva Learning?
    The aspect ratio has to be 16:9.

- **What can I do if the content is not playable?** 
    1. If you're using a custom SharePoint Domain (for example, sp.contoso.com), raise a [support ticket](/services-hub/unified/support/open-support-requests) with the Viva Learning team to get the URL allowed.
    2. If the linked objects are added, you need a Microsoft Viva suite or Viva Learning license to consume them.
    3. Hyperlinks, forms, embedded videos in a file work in Viva Learning.
    
|            Object type        |         Word     |         Pdf     |      PowerPoint  |      Excel  |
|--------------------|:----------------:|:---------------:|:----------------:|:-----------:|
|      Forms         |     N/A          |                 |     No           |     N/A     |
|      Embed video  |     No           |                 |     Yes          |     N/A     |
|      Hyperlinks    |     Ctrl+ select  |     Ctrl+select  |     No           |     No      |