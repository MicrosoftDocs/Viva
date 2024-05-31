---
title: Import members to a Viva Glint Distribution List
description: Use the import option in Microsoft Viva Glint Distribution Lists to add employees in bulk when they don't share a common attribute value.
ms.author: judithweiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: distribution list import, import users, distribution list, blended distribution list
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 05/31/2024
---

# Import members to a Viva Glint Distribution List 

Use the import option in Microsoft Viva Glint Distribution Lists to add employees in bulk when they don't share a common attribute value.

> [!IMPORTANT]
> Importing members to an existing Distribution List removes any attribute rules from that list.

## Imports members

To import employees to a Distribution List:

1. From the admin dashboard, select **Configuration** and then choose **Distribution Lists**.
2. Select the Distribution List that you need to add employees to.
3. Select **Add/Edit Employees**.
4. From the **Choose a way to add employees** dialog, select **Import**.
   :::image type="content" source="../../media/glint/setup/dl-choose-add-method.png" alt-text="Screenshot of the choose a way to import employees dialog for distribution lists.":::
6. In the **Import employees to distribution list** dialog, select **Download CSV** in the **Download your current employee list to modify section**. 
7. Use the downloaded file as a template and add employee email addresses in the email column. Include the header row, which is labeled differently when there are or aren't users in the list. Both column labels import successfully:
   1. The header row label in the template file is **email** when there are already users in the **Distribution List**.
   2. The header row label in the template file is **Employee Email** when there are no users in the **Distribution List**.
8. After adding all email address values, save the file as .csv or .xlsx.
9. In the **Import employees to distribution list** dialog, drag and drop or browse to choose the file (maximum size 550 MB, maximum row count 10,000).
10. To keep any existing users in the list, select **Preserve the employees already in the distribution list**.
    :::image type="content" source="../../media/glint/setup/dl-import-preserve.png" alt-text="Screenshot of distribution list import dialog with the preserve employees in the list option selected.":::
12. Select **Import File**.
13. The **Confirm your import** window displays. If the correct number of employees to be added and removed are correct, select **Confirm Import**.

> [!TIP]
> [Read this guidance for more information on setting up Distribution Lists in Viva Glint](https://go.microsoft.com/fwlink/?linkid=2246615)


