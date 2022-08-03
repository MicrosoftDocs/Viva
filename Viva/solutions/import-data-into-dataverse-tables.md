---
title: Step 4-Import data into Dataverse tables
description: Learn how to import data into the Dataverse tables
author: v-smandalika
ms.author: v-smandalika
ms.topic: article
ms.localizationpriority: medium 
search.appverid:
- MET150
ms.service: viva 
ms.subservice: viva-insights
ms.collection: 
- M365-analytics
- viva-insights
manager: dansimp
audience: Admin
---

# Step 4 - Import data into Dataverse tables

To import data into the Dataverse tables, perform the following steps:
1. Download the Yume Card Data V3 initial content CSV file from the VivaSolutions GitHub repository if not already downloaded as part of the prerequisites.
1. Sign in to https://powerapps.microsoft.com and select the environment to which you'll be deploying the CSV file.
1. On the left navigation pane, select **Dataverse > Tables**.

   :::image type="content" source="../media/dataverse-tables-options-selection.png" alt-text="The page on which we select Dataverse and Tables options":::

   The page listing the Dataverse tables is displayed.

   :::image type="content" source="../media/importdataverse1a.png" alt-text="The page listing the Dataverse tables" lightbox="../media/importdataverse1a.png":::

1. Find the Yume Cards table using the **search** box as shown in the following screenshot.

   :::image type="content" source="../media/importdataverse1b.png" alt-text="The search box using which the user can find the Yume table" lightbox="../media/importdataverse1b.png":::
 
   The Yume Cards table is displayed.

1. Open the Yume Cards table by selecting the three-dotted option and then selecting **Open**.

   :::image type="content" source="../media/importdataverse1c.png" alt-text="The page from which the user can launch the information of the Yume Cards table":::

   The screen containing information of Yume Cards is displayed.

   :::image type="content" source="../media/import-data-from-excel-option.png" alt-text="The page from which we can select Import > Import data from Excel":::

1. Select **Import > Import data from Excel**. The page as shown in the following screenshot is displayed.

   :::image type="content" source="../media/importdataverse2b.png" alt-text="The Import data pane" lightbox="../media/importdataverse2b.png":::

1. Select **Upload**. A dialog box listing files and folders are displayed.

   :::image type="content" source="../media/importdataverse2c.png" alt-text="The dialog box listing files and folders that the user can select to upload" lightbox="../media/importdataverse2c.png":::

1. Select the *YumeCardDataV3_initialcontent.csv* file. This selected file is displayed in the **File** box as shown in the following screenshot.

   :::image type="content" source="../media/importdataverse2d.png" alt-text="The page on which the file to be uploaded is displayed in the File box" lightbox="../media/importdataverse2d.png":::

1. Select **Map columns** on the far-right side of the page. The column mapping page is displayed, as shown in the following screenshot.

   :::image type="content" source="../media/column-mapping.png" alt-text="Column mapping" lightbox="../media/column-mapping.png":::

1. Select **Save changes** on the top right. You return to the Import data pane, as shown in the following screenshot.

   :::image type="content" source="../media/dataimport.png" alt-text="The Import data pane on the right side of the page" lightbox="../media/dataimport.png":::

1. Select **Import** on the top right. A notification message denoting a successful import is displayed, for example, the following screenshot.

   :::image type="content" source="../media/import-completed-successfully.png" alt-text="The notification that the import has been completed successfully":::