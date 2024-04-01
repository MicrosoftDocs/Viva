---
title: "Import files to generate questions-and-answers in Viva Engage communities"
description: "Repurpose your organization's FAQ by importing them as question/answer pairs in Viva Engage."
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 03/15/2024
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Import files to generate questions-and-answers in Viva Engage communities

Community admins can generate question-and-answer pairs by uploading informational documents in Viva Engage. The **Answers Intelligent Importer** uses AI to transform your static documents into dynamic interactive conversations, ensuring that your organization's valuable content is easy to retrieve and reuse.

Generated question-and-answer pairs follow the same rules of visibility as other content in that community. Your uploaded source files are stored on [Microsoft SharePoint](/viva/engage/get-started-with-viva-engage/file-storage) with other files in that community and are viewable by all members of that community.

>[!NOTE]
>Currently this premium feature is only available for communities, but will soon be accessible to Engage admins on the Answers page. Viva Engage premium is included with a _Viva Suite_ or _Employee Communities and Communications_ license.

## Import documents to communities

Community admins can populate their communities with useful information by importing informational documents. The Answers Intelligent Importer is enabled by default.

:::image type="content" source="../media/engage/admin/import-access-points.png" alt-text="Screenshot shows the location on the community page that lets you import a file to generate questions and answers.":::

1. Review the [file requirements](#file-requirements) to ensure a successful import.
1. Go to your community landing page, and select the Answers Intelligent Importer access point.
1. When prompted, select and upload a file from your device.
    If the import was successful, Answers Intelligent Importer generates a list of question-and-answer pairs from the content.

1. Edit or delete items in the list, as needed. You can improve future import results by using the thumbs up and thumbs down icons to provide feedback.

1. Select the pairs you want to import (up to 20) and select **Post**.
If the post is successful, it returns a confirmation message and the question-and-answer pairs appear on the community landing page. 
Content posted through this feature follows the same rules of visibility as other knowledge content posted within that community.

## File requirements

Importer uses AI to generate the question-and-answer pairs, no advanced structuring is required. In fact, files that _aren't_ structured as FAQs generally yield the best results. In addition, your files must meet these requirements:

- .docx, .pdf, or .txt format
- 5 MB maximum file size
- 2-10 pages (smaller documents provide better results)
- Files stored locally

Each file can generate a maximum of 20 question-and-answer pairs. If your document is large and you want to generate more than 20 questions and answers, consider breaking the file up into two or more files.

>[!NOTE]
>Embedded images with no textual metadata will not be processed.

## Control the Answers Intelligent Importer feature

Engage admins can control the Answers Intelligent Importer in their Viva Engage network through these steps. The importer is on by default.

1. Go to [Viva Engage admin center on the web](http://engage.cloud.microsoft/main/admin), and from the gear icon at the top navigation menu, select **Admin center**.
1. On the **Feature management** tab, select the **Answers** button  to open the Answers configuration options.
1. Under **Intelligent Importer availability**, turn on **Premium Communities**.

When this setting is enabled, community admins with access to premium functionalities on Engage can access and use the Intelligent Importer feature in their communities.  