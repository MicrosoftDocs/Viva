---
title: Add SharePoint as a learning content source for Microsoft Viva Learning
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 11/01/2023
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
description: Learn how to add SharePoint as a learning content source for Microsoft Viva Learning.
---

# Add SharePoint as a content source for Microsoft Viva Learning

You can configure SharePoint as a learning content source to make your organization's own content available in Viva Learning. 

> [!NOTE]
> Content accessible through Viva Learning is subject to terms other than the Microsoft Product Terms. Any content you add to Viva Learning, such as SharePoint-hosted content, is subject to the privacy and service terms associated with that content.

## Overview

The knowledge admin (or global administrator) provides a site URL to where the [Learning Service](configure-sharepoint-content-source.md#learning-service) can create an empty centralized location in the form of a structured SharePoint list. This list is called the Learning App Content Repository. Your organization can use this list to house links to cross-company SharePoint folders that contain learning content. Admins are responsible for collecting and curating a list of URLs for folders. These folders should only include content that can be made available in Viva Learning.


:::image type="content" alt-text="Diagram that shows the process of getting content from folders to a SharePoint list into Viva Learning." source="../media/learning/sp-dataflow-infographic.png" lightbox="../media/learning/sp-dataflow-infographic.png":::

Viva Learning supports the following document types:

- Word, PowerPoint, Excel, PDF
- Audio (.m4a, .mp3)
- Video (.mov, .mp4, .avi)
- [Linked objects](#add-linked-objects)

For more information, see [SharePoint limits](/office365/servicedescriptions/sharepoint-online-service-description/sharepoint-online-limits?redirectSourcePath=%252farticle%252fSharePoint-Online-limits-8f34ff47-b749-408b-abc0-b605e1f6d498).

> [!NOTE]
> You can use either a Modern or Classic SharePoint site. You can choose whether to use an existing site or create a new SharePoint site based on your organization's needs.

> [!NOTE]
> While either communication and teams sites can be used, we recommend using a communication site. 

> [!NOTE]
> If you are using a custom SharePoint Domain (for example, sp.contoso.com) raise a [**support ticket**](/services-hub/unified/support/open-support-requests) with the Viva Learning team to get the URL allowed. 

> [!NOTE]
> Viva Learning ingests up to 1000 files as learning objects. A Viva Suite or Viva Learning license is required to ingest more than 1000 files as learning objects.


## Learning Service

The Learning Service uses the provided folder URLs to get metadata from all content stored in those folders. Within 24 hours of supplying the folder URL in the centralized repository, employees can search for and use your organization's content within Viva Learning. All changes to content, including updated metadata and permissions, appear in the Learning Service within 24 hours.

## Configure SharePoint as a source

> [!NOTE]
> You must be a Microsoft 365 global administrator or knowledge admin to perform these tasks.

1. Open Viva Learning App in Teams or go to the Viva Learning [web app](https://aka.ms/VivaLearningWeb)

1. Go to the Admin tab in Viva Learning and select Manage Providers on the left menu. Select **Add Provider**.

1. Select **SharePoint** from the Provider list and select **Next**.

1. Under SharePoint, provide the site URL to the SharePoint site where you want Viva Learning to create a centralized repository. If your SharePoint site is new, wait 1 hour after site creation to add it here. You must also be the owner of the SharePoint site.

1. If your organization uses [Microsoft 365 Multi-geo](/microsoft-365/enterprise/microsoft-365-multi-geo), find your region or country at [Microsoft 365 Multi-geo availability](/microsoft-365/enterprise/microsoft-365-multi-geo#microsoft-365-multi-geo-availability). The **Viva Learning** panel also shows this information.

1. Update the display name in configuration flow. The display name is the organization or tenant name by default.  

   > [!NOTE]
   > Only the owner of the added site URL can update the display name.
   
   > [!NOTE]
   > Display names for already ingested learning objects update after 24 hours.
   
   Once configured, configured providers list SharePoint immediately. You can track the sync status and export sync logs.
   
   A SharePoint list is created automatically within the provided SharePoint site.

1. In the left navigation of the SharePoint site, select **Site contents** > **Learning App Content Repository**.

1. On the **Learning App Content Repository** page, populate the SharePoint list with URLs to the learning content folders. Read [Folder URL document library curation](#folder-url-document-library-curation) for details about how to create the content folders.
   
   1. Select **New** to view the **New item** panel.
   
   1. On the **New item** panel, in the **Title** field, add a directory name of your choice. In the **Folder URL** field, add the URL to the learning content folder. Select **Save**. [Learn how to to create the folder URL](#folder-url-document-library-curation).
   
      [![New item panel in SharePoint showing the Title and Folder URL fields.](../media/learning/learning-sharepoint-configure6.png)](../media/learning/learning-sharepoint-configure6-big.png#lightbox)

   1. The **Learning App Content Repository** page is updated with the new learning content.
      
      ![Learning Content Repository page in SharePoint showing the updated information.](../media/learning/learning-sharepoint-configure7.png)
      
      If you encounter issues with content, refer to the [export log file](/viva/learning/use-tabs?view=o365-worldwide#managing-providers&preserve-view=true) for a detailed summary of successful and failed content ingestion.

> [!NOTE]
> To allow for broader access to the Learning App Content Repository, a link to the list is soon available in the Viva Learning interface where users can request access and ultimately help populate the list. Site owners and global administrators are able to grant access to the list. Access is specific to the list only and doesn't apply to the site where the list is stored. For more information, see [Provide your own organization's content](#provide-your-own-organizations-content) later in this article.

> [!NOTE]
> Viva Learning ingests up to 1000 files as learning objects. A Viva Suite or Viva Learning license is required to ingest more than 1000 files as learning objects.

### Folder URL document library curation

Create a folder to store learning content for your organization.

1. Go to your Documents library and select **+ New** and choose **Folder**.

1. Enter a folder name.

1. Select **Create**. The folder displays in your document library.

1. Upload files that you want to publish as learning content in this folder. Apply Microsoft 365 permissions to the folders that contain learning objects and to any items within the folders that have unique permissions. [Learn how to use permissions for learning content](sharepoint-permissions.md).
​
1. To get the folder URL, choose the folder and select **Copy link**.

> [!IMPORTANT]
> Users are able to view content in Viva Learning with the correct permissions. See [Configure permissions for SharePoint content](sharepoint-permissions.md) for information.

#### Add linked objects

Add links to both internal content from SharePoint and external content from sites such as YouTube or Vimeo that Viva Learning includes.

> [!NOTE]
> When users access the content from Viva Learning, they'll be taken to the URL of the content in their browser.

> [!NOTE]
> A Viva Suite or Viva Learning license is required to access linked objects in Viva Learning. Without a license, you can discover linked objects in Viva Learning, but can't consume them.

1. In your folder, select **New** and then choose **Link**.

   :::image type="content" alt-text="Screenshot of the documents library with New and Link selected." source="../media/learning/sp-new-link.png" lightbox="../media/learning/sp-new-link.png":::

1. Add the URL and choose a name.

   ![Screenshot of the new link pane with a URL and name filled in.](../media/learning/sp-linkname.png)

1. Select **Create**.
   - The link appears in your document library with the name you selected.

     ![Screenshot of the documents library with a new file called Azure.url.](../media/learning/sp-linkinlibrary.png)

   - The linked object shows up in the Viva Learning app.


### Metadata

Default metadata (such as modified date, created by, document name, content type, and organization name) is automatically pulled into Viva Learning by the Microsoft Graph API.

Improve overall discovery and search relevance of the content by adding columns for description, thumbnail URL, duration, author, and tags.

If a description column is already present, you can delete it and add a new one by following the steps to add a metadata field.

**To add a metadata field, follow these steps**:

> [!IMPORTANT]
> You'll need to use the column names exactly as they're provided here for the metadata to populate the field. Adding metadata is optional, but if configured incorrectly, you will need to delete the column and create again. 


1. Select the folder from your learning content repository.
1. From the **Documents** page, select **Add column**.

   [![Screenshot of the Documents page with Add column selected.](../media/learning/sp-new-column.png)](../media/learning/sp-new-column-big.png#lightbox)

**To add a description column to the document library page, follow these steps**:

1. Follow the initial steps to create a column.
1. Choose **Multiple lines of text**.
1. Name the column `ContentDescription`.
1. Add custom descriptions for each item. If no description is supplied, Viva Learning provides a default message that highlights the content as being from your own SharePoint library.

**Add the content title**:

1. Follow the initial steps to create a column.
1. Choose **Multiple lines of text**.
1. Name the column `ContentTitle`.
1. Add custom title for each item. If no title is supplied, Viva Learning picks the file name as the title.

**Add the content format**: 

1. Follow the initial steps to create a column.
1. Choose **Multiple lines of text**.
1. Name the column `ContentFormat`.
1. Add format for each item. If no format is supplied, Viva Learning picks the file type from the file extension like xlsx, docx, and so on.

**Provide a thumbnail image**:

> [!NOTE]
> - Only public URLs work for this process.
> - For proper rendering of the image in Viva Learning the minimum aspect ratio should be 16:9.

1. Follow the initial steps to create a column.
1. Choose **Hyperlink**.
1. Name the column `ThumbnailWebUrl`.
1. Add the URLs for each item.


**Language metadata**

1. Follow the initial steps to create a column. 

2. Choose Single line of text. 

3. Name the column ContentLanguage 

3. Add 2 Letter ISO standard Language-Locale code for each item. For example, for French (France) add fr_fr. See the list of [Supported languages](/viva-learning-supported-languages).

4. In case a language isn't provided, Viva Learning sets the language of the course as English (US) or to the default language set for Viva Learning by the admin. Learn more about [language preferences](/viva/learning/language-preferences).

**Add the duration of the content**:

1. Follow the initial steps to create a column.
1. Choose **Number**.
1. Name the column `ContentDuration`.
1. Provide the duration of the content in seconds.

**Add tags**:

1. Follow the initial steps to create a column.
1. Choose **Managed metadata**.
1. Name the column `SkillTags`.
1. Select **More options**.
1. Toggle to allow multiple values.
   
   [![Screenshot of the toggle to allow multiple values](../media/learning/skilltags.png)](../media/learning/skilltags-big.png#lightbox)
   
1. Choose to use a predefined term set or a customized term set.

[Learn more about how to create a Managed Metadata column.](https://support.microsoft.com/office/create-a-managed-metadata-column-8fad9e35-a618-4400-b3c7-46f02785d27f)

**Add the author**:

1. Follow the initial steps to create a column.
1. Choose **Multiple lines of text**.
1. Name the column `ContentAuthor`.
1. Add the author or authors of the content.

### Provide your own organization's content

Knowledge admins can access their organization's Learning App Content Repository in SharePoint where they can provide references to cross-organization document libraries. Content within these libraries are learning content in Viva Learning.

1. In Viva Learning, select the ellipses (**...**), and then select **Settings**.
  
1. Under **Settings**, select **Permissions**.

1. Select **Check access** to connect to your organization's centralized library.

### Delete content

1. Select the content you wish to remove from your Learning App Content Repository.
   
1. Choose **Delete** on the command bar, or select the ellipses and then select **Delete**.

> [!NOTE]
> Viva Learning takes approximately 24 hours to remove content you delete from the Learning App Content Repository.

## Multi-geo

[Microsoft 365 Multi-geo](/microsoft-365/enterprise/microsoft-365-multi-geo) is designed to meet data residency requirements.

The site URL provided by the knowledge admin where the Learning App Content Repository resides needs to belong to the central location where your Microsoft 365 subscription was originally provisioned. 

Linked folders linked in the repository must also belong to the central location. This restriction conforms to data residency requirements. 

If you encounter issues with content, refer to the [Manage Providers Configuration](/viva/learning/use-tabs.md#manage-providers-configuration) export log for detailed summaries of successful and failed content ingestions.

For more information, see [Multi-geo capabilities in SharePoint Online](/microsoft-365/enterprise/multi-geo-capabilities-in-onedrive-and-sharepoint-online-in-microsoft-365).

## Next steps

[Add learning management systems for Viva Learning](configure-lms.md) or [Add other content providers for Microsoft Viva Learning](configure-other-content-sources.md)
