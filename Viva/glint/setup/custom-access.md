---
title: Custom data access in Viva Glint
description: Microsoft Viva Glint offers custom data access for users who need to have their default team access overridden or are in a role that is so specific, it needs to be per user rather than at the User Role level.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: custom survey access, custom access, custom data access export, user access, data access export
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 10/15/2024
---

# Custom data access in Viva Glint

Microsoft Viva Glint offers custom data access for users who need to have their default team access overridden or are in a role that is so specific, it needs to be per user rather than at the User Role level. For example, Viva Glint Administrators can use custom access for HR business partners who serve unique combinations of employee groups in your organization. Use the guidance in this article to export, modify, and import custom data access.

## Export custom access

Use the custom access export as a Viva Glint Admin to audit users' data access.

1. From the Glint Admin dashboard, select the **Configuration** symbol and then in **Employees** choose **User Roles**.
2. In the top right corner of the **User Roles** page, select **Export**.
3. In **Export data** dialog that appears, select a survey **Program**, **Role**, and whether to include:
   1. **Focus Area Access**: Turn on to include Focus Area access only. Turn off to include survey results access only.
   2. **Empty Data**: To include users with no data access, turn on.
   3. **Inactive Data**: To include active **and inactive users**, turn on.
  
      :::image type="content" source="../../media/glint/setup/export-access-dialog.png" alt-text="Screenshot of the Export data dialog with program, role, and data selections.":::  
      
4. A new dialog appears prompting you to **rename and save** the data to your device. Dy default, custom access files export to a compressed folder named: **Untitled.zip**.

## Custom access file

The custom data access export includes the following information. Modify or add data to this file to import to Viva Glint for data access updates in bulk.

> [!NOTE]
> Open the exported .csv file by [importing in Microsoft Excel](https://support.microsoft.com/office/import-data-from-a-csv-html-or-text-file-b62efe49-4d5b-4429-b788-e1211b5e90f6) to retain leading zeros and data formats.

- **user email**: Populated with users' email addresses.
- **population**: Enter 1 for the first population. Each additional population increases in number for each user.
- **access type**:
  - The survey uuid of the program that users have customized access for, or
  - "GOAL" when exporting Focus Area access for users.
- **Attribute columns**: Other columns in the export are based on your organization's attributes and values that are used to grant custom access. Add new columns and values to grant new access.

### Example

An HR business partner, user@contoso.com, oversees European Sales and Marketing teams for Contoso. To grant this user access to the right cut of data to view survey results, a Viva Glint Admin would fill in an access file with their location attribute Region = Europe and their hierarchy Team Level 1 = Marketing and Sales.

:::image type="content" source="../../media/glint/setup/custom-access-export-survey.png" alt-text="Screenshot of a custom access export for an HRBP with customized survey results access.":::

To apply the same custom access for creating Focus Areas, update the access type column for this HRBP to "GOAL."

:::image type="content" source="../../media/glint/setup/custom-access-export-focus-area.png" alt-text="Screenshot of a custom access export for an HRBP with customized focus area access.":::

> [!IMPORTANT]
> Save your edited file as **.csv with a comma separator and UTF-8 encoding**.

## Upload custom access in Advanced Configuration

After exporting and preparing a file, go to Advanced Configuration to upload users’ custom data access.

1. From the Glint Admin dashboard, select the **Configuration** symbol and then in **Service Configuration**, choose **Advanced Configuration**.
2. In the **Advanced Configuration** menu, select **Uploads**.
3. In the **Upload type** dropdown menu, select **MANAGERS_UPLOAD**.
4. **Apply to**: Ignore, this is for retroactive uploads only.
5. **Incremental**:
   1. Switch on this toggle to append access to users in your file.
   2. Switch off this toggle to overwrite all access for users in your file. Users not included in the file aren't impacted.
6. **Use exact case from the file for First/Last name**: Ignore, this doesn’t apply to access uploads.

   :::image type="content" source="../../media/glint/setup/adv-config-uploads.png" alt-text="Screenshot of the Advanced Configuration Uploads feature..":::

7. Drag and drop your .csv file or browse to choose it in the **Drag and drop to upload** section.
8. in the **Upload Job Details** page that appears, confirm that the **Uploaded Lines Summary** matches the changes in your file.
9. Select **Apply Upload to Database** to upload new values.
10. In the **Load import file into database?** dialog, select Yes.
11. Got to some users' profiles to confirm that customized access appears as expected.
   1. Select the **Configuration** symbol, then in **Employees**, choose **People**.
   2. Search for and select users to spot check.
