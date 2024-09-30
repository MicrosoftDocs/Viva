---
title: Managing exported interest files
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 09/30/2024
audience: admin
ms.topic: article
ms.service: viva-learning
search.appverid: MET150
ms.collection: 
    - enabler-strategic
    - m365initiative-viva-learning
ms.localizationpriority: medium
description: Learn how to open and edit an exported interest file. 
---

# Manage exported interest files

1. Download the exported interest file.

2. Open the CSV file: 
    1. If your CSV file is opening as expected, you can proceed editing without further action.
    1. If you see that all the columns in the file are displayed in one column, then follow the below steps to view or edit the exported CSV file.

3. Open a blank Excel workbook

4. Import the exported CSV file into your workbook with the following steps:

    1. Choose file Origin 65001: Unicode (UTF-8) and Delimiter Comma, then press load.

    2. Remove the Header row (by unchecking the Header Row option) and delete the blank row on top.

    3. Delete the Sheet 1 created by Excel.

    4. Add, delete, or edit interests as needed. Column A needs a unique identifier.

    5. When ready save the file as CSV UTF-8 (Comma delimited) (*.csv).

5. Import the saved file import into **Manage interests**. Before importing the file, check the delimiter in the CSV file and provide the same value in **Specify delimiter for the CSV file** field in the import window.

> [!NOTE]
> To find out what is the delimiter used, open the CSV file in notepad. The delimiter is the separator used in the file, such as `,` or `;`.
> While importing the CSV file, provide the same delimiter, so that Viva Learning can use the same delimiter while processing the imported file.
