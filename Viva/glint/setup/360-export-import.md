---
title: Viva Glint 360 cycle content export and import
description: Export and import translation files for 360 feedback cycles.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: 360 feedback, import 360 content, export 360 content, translations
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 5/24/2024
ROBOTS: NOINDEX, NOFOLLOW
---

# Viva Glint 360 cycle content export and import

> [!NOTE]
> This feature is available to preview customers only. Features described here are subject to change.

After setting up a Microsoft Viva Glint 360 cycle and making all customizations in English, use Export and Import Cycle Content options to apply all updates to translations.

> [!NOTE]
> Standard 360 content includes translations for selected languages.

## Export and edit content from the 360 cycle page

To export 360 content files from the cycle page and edit content to prepare for import:

> [!NOTE]
> New 360 content can't be added to your cycle with the export/import process. This feature only updates translations for content that already exists in your 360 cycle.

1. Select **Actions** and choose **Export Cycle Content**.
1. In the dialog that appears, choose the **Content Details to Include** and select **Languages** to export.
1. Select XLSX or CSV in the **Select Content Type** dropdown menu.
   :::image type="content" source="../../media/glint/setup/export-360-cycle-content.png" alt-text="Screenshot of the Export Cycle Content dialog with content, language, and file format selections..":::
1. Folders (compressed with .zip extension) that contain files for each language download for each type of selected content
1. Double-click each .zip folder to open and view all language files for each content type.
2. Open and edit files in each language where customizations need to be added.
   > [!IMPORTANT]
   > To retain special characters and formatting, always open CSV files by [importing data from csv](https://support.microsoft.com/en-us/office/import-data-from-a-csv-html-or-text-file-b62efe49-4d5b-4429-b788-e1211b5e90f6) in Microsoft Excel.
1. Modify content in columns that contain "translated" in the column label.

> [!IMPORTANT]
> Don’t edit exported **file names** or **header names** in the files to ensure that files import successfully.

## Import edited content to the 360 cycle page

1. After editing and saving exported content files in each language, select **Actions** and choose **Import Cycle Content**.
2. Select a **Content Type** from the dropdown menu.
   :::image type="content" source="../../media/glint/setup/import-360-cycle-content.png" alt-text="Screenshot of the Import Cycle Content dialog with content type and file upload method selections.":::
4. Drag and drop or browse to choose:
   1. A single XLSX or CSV file in one language.
   2. A .zip folder of multiple XLSX or CSV files in more than one language.
5. Select **Next** and then choose **Make changes**.
6. Refresh the cycle page to track the upload's progress or wait for a confirmation email.
