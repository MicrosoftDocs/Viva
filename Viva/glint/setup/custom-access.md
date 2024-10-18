---
title: Custom data access in Viva Glint
description: Microsoft Viva Glint offers custom data access for users who support unique groups of employees in your organization.
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

Microsoft Viva Glint offers custom data access for users who support unique groups of employees in your organization. Users may need to have their default team access modified or are in a role so specific, access needs to be set at the user level. Use the guidance in this article to export, modify, and import custom data access. To make individual updates to users' custom data access, see: [Custom User Role setup in Viva Glint](custom-user-role.md)

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

|Column  |Description   |
|:----------|:-----------|
|user email     | Populated with users' email addresses.       |
|population     | Enter 1 for the first population. Each new population increases in number for each user. |
|access type   | <ul><li>The survey uuid of the program that users have customized access for, or</li> <li>"GOAL" when exporting Focus Area access for users.</li> </ul>      |
|other attributes    | Other columns in the export are based on your organization's attributes and values that are used to grant custom access. To grant new access, add new columns and values. |

### Edit the access file

To prepare your exported custom access file for import to Advanced Configuration:

1. Open the exported .csv file by [importing in Microsoft Excel](https://support.microsoft.com/office/import-data-from-a-csv-html-or-text-file-b62efe49-4d5b-4429-b788-e1211b5e90f6) to retain leading zeros and data formats.
2. Update the columns in the exported file to the following columns:

   |Column  |Change to...   |
   |:----------|:-----------|
   |user email     | manager reference   |
   |population     | `no change` |
   |add or remove     | `insert this as a new column` populate with "ADD" or "REMOVE" |
   |access type   | survey uuid |
   |other attributes    | `no change` To grant new access, add new columns and values based on employee data imported to Glint. |

   > [!NOTE]
   > To prevent upload errors, for attributes based on data uploaded to Glint make sure that column labels match your attribute setup exactly.
 
3. To grant custom access for:
   - **Survey results**:
      - Populate the survey uuid column with the survey programs unique ID that's included in the access export file.
   - **Focus Areas**:
      - Populate the survey uuid column with "GOAL."
   - **Admin permissions**:
      - Populate the survey uuid column with "ADMIN."
4. To grant custom access to: 
   - **Another manager's team that exists in current employee data**:
      - Include an attribute column labeled: Manager Level 1 and list the Employee ID of the manager that another user should have access to. The manager levels automatically calculate based on the manager ID added to the Manager Level 1 column.
   - **Another manager's team that doesn't exist in current employee data**:
      - Include columns for all Manager Level fields populated with manager IDs to build the full manager hierarchy path. To get all levels in this past hierarchy path for an old manager team, [export users from the survey cycle](/viva/glint/setup/glint-data-apps#export_users_from_survey_cycle) and copy Manager Level fields and the manager IDs in them.
   - **A level in a non-Manager hierarchy**:
      - Include all levels above the level the user should have access to. Example: To grant access to Location Hierarchy Level 3 = Dublin, include columns for Region, Country, and City.
5. Save your file in .csv format with a comma separator and UTF-8 encoding.

### Example

An HR business partner, user@contoso.com, oversees European Sales and Marketing teams for Contoso. To grant this user access to the right cut of data to view survey results, a Viva Glint Admin would fill in an access file with their location attribute Region = Europe and their hierarchy Team Level 1 = Marketing and Sales.

:::image type="content" source="../../media/glint/setup/custom-access-export-survey2.png" alt-text="Screenshot of a custom access export for a user with customized survey results access.":::

To apply the same custom access for creating Focus Areas, update the access type column for this user to "GOAL."

:::image type="content" source="../../media/glint/setup/custom-access-export-focus-area2.png" alt-text="Screenshot of a custom access export for a user with customized focus area access.":::

> [!IMPORTANT]
> Save your edited file as **.csv with a comma separator and UTF-8 encoding**.

## Upload custom access in Advanced Configuration

After exporting and preparing a file, go to Advanced Configuration to upload users’ custom data access.

1. From the Glint Admin dashboard, select the **Configuration** symbol and then in **Service Configuration**, choose **Advanced Configuration**.
2. In the **Advanced Configuration** menu, select **Uploads**.
3. In the **Upload type** dropdown menu, select **MANAGERS_UPLOAD**.
4. **Apply to**: Ignore, this setting is for retroactive uploads only.
5. **Incremental**:
   1. Switch on this toggle to append access to users in your file.
   2. Switch off this toggle to overwrite all access for users in your file. Users not included in the file aren't impacted.
6. **Use exact case from the file for First/Last name**: Ignore, this doesn’t apply to access uploads.

   :::image type="content" source="../../media/glint/setup/adv-config-uploads.png" alt-text="Screenshot of the Advanced Configuration Uploads feature.":::

7. Drag and drop your .csv file or browse to choose it in the **Drag and drop to upload** section.
8. In the **Upload Job Details** page that appears, confirm that the **Uploaded Lines Summary** matches the changes in your file.
9. Select **Apply Upload to Database** to upload new values.
10. In the **Load import file into database?** dialog, select Yes.
11. Go to some users' profiles to confirm that customized access appears as expected.
   1. Select the **Configuration** symbol, then in **Employees**, choose **People**.
   2. Search for and select users to spot check.
