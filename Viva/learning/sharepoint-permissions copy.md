---
title: FAQs in SharePoint
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 01/04/2024
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

This topic outlines error codes and FAQs for SharePoint in Viva Learning.


|Error code | Error description | Next Steps | 
| - | - | - | 
| `SP_INVALID_FOLDER_URL` | Folder-URL is not valid, only folder-URL are supported. Adding document libraries directly are not supported | 1. Add the files in a folder and add the folder URL in the learning app repository. Read the configure SharePoint content source [documentation](/viva/learning/configure-sharepoint-content-source#folder-url-document-library-curation)
|`SP_NO_M365_PERMISSIONS_FOUND` | Every item needs to have [Microsoft 365 group permission](sharepoint-permissions.md) to light-up inside Viva Learning.| <br> Check if the folder has M365 /MESG group added directly. </br> <br> If you have added a security group check if the security group is mail enabled. Steps to make a security group as mail-enabled: </br>  <br> Check whether the group you added has "Domain Group" as its Type. </br> <br> Select **Manage access** > **More options** > **Advanced settings.**  <ul> <li> Open the folder  and for a file check if M365 / MESG group is directly applied on the file items. **NOTE:** Check that if permission is propagating to file items, for this owner /contributor access is required </li>  <li> A M365 group or MESG group cant be added directly to the file /folder in-case the group is found on the folder/file nested in SharePoint groups. </li> <li> To see if group is already present, click on the folder, Manage access > advanced setting> check permisisons. </li> <li> If it is already present , remove it and add directly or add a different group </li>
|`SP_ITEM_LIMIT_REACHED`| Only 1000 files or items can be ingested as learning objects | Purchase a Microsoft Viva Suite or Viva Learning license. | 
| `SP_ITEM_INGESTION_FAILED` | | | 



> [!NOTE]
> If the ingestion is showing success and total items ingested are zero check if the folder URLs are added in learning app repository. 

- **Site URL being added** 

    Either Teams site or communication site can be used. It is recommended to use a communication site. 

- **Why is the display name is not getting updated** 
    Only the owner can update 
    Knowledge admin and global admins can only update  [???]
    The change takes 24 hours to reflect  

- **What is the limit on the number of file items that can be ingested?**

    - Viva Learning ingests up to 1000 files as learning objects. A Viva Suite or Viva Learning license is required to ingest more than 1000 files as learning objects. 
    - The order in which files are ingested: 
        - The first 1000 items with earliest last modified date will be ingested 
        - For example, if a customer has items A, B, and C, and they created or uploaded them in the sequence A, B, and C, then the earliest last modified date will belong to A, followed by B, and then C. Therefore, when restricted to only two items, we would have only included A and B in our collection and C would be discarded. 

- **What can I do if my content is not visible?**  
    1. Go to the SharePoint site added in the **Admin tab** > **Manage provider** > **SharePoint**.
    2. Go to site contents and in the Learning app repository, check if the folder URLs are present.
    3. Check if the folder has M365 or MESG group added directly.
        a. If you have added a security group check if the security group is mail enabled. Steps to make a security group as mail-enabled:  
        b. Check whether the group you added has "Domain Group" as its Type. 
        Select **Manage access**> **More options** > **Advanced settings.** 
    4. Open the folder and for a file check if M365 or MESG group is directly applied on the file items.
    **NOTE:** Check that if permission is propagating to file items, for this owner or contributor access is required.
    5. A M365 group or MESG group can't be added directly to the file or folder incase the group is found on the folder or file nested in SharePoint groups.
    6. If it is already present, remove it and add directly or add a different group.

- **What can I do if the metadata isn't reflecting properly?**

    1. Check the [column names](/viva/learning/configure-sharepoint-content-source#metadata)
    2. If not correct, delete and recreate the column.
    3. For thumbnails to render properly, the aspect ratio has to be 16:9 
    4. For images stored on SharePoint the path has to be copied 

- **What can I do if the content is not playable?** 
    1. Check if you are using custom SharePoint URl. Custom URL will not be in the tenantname.sharepoint.com format.
    2. If you are using custom URL, the URL will need to be whitelisted 
    3. If the inked objects are added, then you need a Microsoft Viva suite or Viva Learning license to consume them.
    4. If there are hyperlinks in the document. 
    
|                    |         Word     |         Pdf     |      PowerPoint  |      Excel  |
|--------------------|:----------------:|:---------------:|:----------------:|:-----------:|
|      Forms         |     N/A          |                 |     No           |     N/A     |
|      Embedd video  |     No           |                 |     Yes          |     N/A     |
|      Hyperlinks    |     Ctrl+ click  |     Ctrl+click  |     No           |     No      |