---
title: Set up attributes in Viva Glint
description: In preparation for uploading employee data to Microsoft Viva Glint, perform attribute setup and mapping that will establish which attributes should be included in data uploads.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: Attribute setup, edit attribute, data import
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 08/24/2023
---

# Set up attributes in Viva Glint

Before using the guidance on this page, you should have created your Employee Attribute Template. All required and custom attributes, and hierarchies, should appear as you would like them to appear on all reports going forward. This first row is your file blueprint.

> [!TIP]
> Ensure that attribute labels stay consistent over time in your Employee Data File. For example, if an attribute is set up as "Employee ID," it will not later be recognized as the same column renamed as "Employee Number".

Use the following guidance to set up attributes in Viva Glint based on selections you made when putting together your [Employee Attribute Template](https://www.microsoft.com/en-us/download/details.aspx?id=105533). This is your guide for setting up Viva Glint to accept data that you import to the platform long-term.

## Attribute setup in Viva Glint

To set up your attributes in Viva Glint, your uploaded file must contain a finalized attribute header row and at least one row of employee data. Use the in-platform, four-step attribute setup process to prepare the system to import employee data.

> [!IMPORTANT]
> Reporting hierarchies, derivations, file format, and date attribute formats can't be edited after initial setup is complete. Before beginning, confirm that the attribute selections in your Employee Attribute Template are **final**.

1. From the admin dashboard, select the **Configure** symbol.
2. In **Employees,** select **People**.
3. Choose **Get Started** to begin the four-step process.

Follow the onscreen guidance for the following actions.

## Upload dataset

Upload finalized attributes in the format you have chosen. This file format will determine the format for all future uploads. Select **Continue.**

## Preview employee data fields

Check that the attribute names and values appear as expected.

1. Verify that:
     - All attributes are present in the preview.
     - Attribute values shown for preview employee records display in the correct column.
     - The total count of "data fields found" displayed above the preview matches the number of attributes in the file.
2. If dates are included in your file, select the **There are date fields** checkbox and then the appropriate **date format** from the dropdown menu.

     > [!NOTE]
     > All attributes that include dates must follow the same format. Viva Glint will transform incoming dates to Viva Glint's preferred format, yyyy/mm/dd, upon upload.

3. After previewing, select **Continue**.

## Set up attributes

Map your uploaded and confirmed attributes to Viva Glint fields. This setup is divided into three sections:

### Required attributes

Select your attribute from the dropdown for each required attribute:

- First Name
- Last Name
- Email
- Employee ID
- Status

### Hierarchy groups

Select your attributes from the dropdown menu for each hierarchy group.

- To add more levels to a hierarchy, select **+ Add Level**.
- To add a new hierarchy group, select **+ Add Hierarchy Group**.
- To rename the hierarchy label, select the **pencil** symbol.
- To delete a group or level, select the **trash can** symbol.

### Derived attributes

Viva Glint calculates attributes based on data sent in your employee attribute file. Most organizations choose to include a managerial hierarchy. Select your option and the attribute that should be used to create it. Decide whether to include tenure groups based on hire date or age groups based on birth year.

1. Select the section with the desired attribute.
2. Select the desired attribute from the dropdown menu for each derived attribute.
3. Select **Continue**.

## Review uploaded attributes

1. Review your attribute selections, choosing between the following two options:

     - Option 1 - Save attributes and import employee data – Recommended if the employee data in your file is complete and finalized (doesn't contain test or partial data).

     > [!CAUTION]
     > Employee data can't be deleted. This option performs a full employee upload, which applies any changes in the file and marks anyone not in the file as an inactive employee.

     - Option 2 - Save attributes and discard employee data – Recommended to configure attributes based on your header row and then import finalized employee data later.

     > [!TIP]
     > Viva Glint recommends the **Save attributes and discard employee data** option for initial setup. This allows you to set up and map your attributes in the system and complete your first data import as a separate task.

2. Select **Save**.


## Add new attributes to Viva Glint

After initial setup, you may find that new attributes need to be added to your employee data file. New attributes and their values will apply to future survey results only.

### Procedure for adding new attributes

From the admin dashboard:

1. Select the **Configure** symbol and then under the **Employees** section, choose **People**.
2. Select **Actions** and then **New User Attributes**.
3. Upload your dataset with all existing attributes and the new attribute(s).

     > [!NOTE]
     > Your uploaded file must contain the Attribute Header Row and at least one row of employee data that aligns with the current format.

4. Select **Continue**.
5. If dates are included in your file, select **There are date fields** and then the appropriate date format from the dropdown menu.

     > [!NOTE]
     > This selection should be your existing date format, which is consistently used for employee data.

6. Preview your data and confirm that you see the new attributes.
7. Select **Continue**.
8. The Attributes Setup page shows current required attributes and hierarchy groups and can't be edited. Select **Continue**.
9. Choose to **Save attributes and import employee data** or to **Save attributes and discard employee data**.

     > [!TIP]
     > When adding new attributes, choose the Save attributes and discard employee data option to save your setup in preparation for future imports.

10. Select **Save**.

## Edit attribute names

Use the following guidance to rename attributes before updating your data files so that they continue to import seamlessly.

From the admin dashboard:

1. Select the **Configure** symbol and then in the **Employees** section, choose **People**.
2. Select **Actions** and then select **Edit User Attributes**.
3. Select the corresponding vertical ellipses to the far right of the attribute in the Active Attributes row.
4. Select **Rename Attribute**.
5. Enter the new name in the Attribute Name field and select **Rename**.
6. On the top right of your dashboard, select **Save Changes**.

> [!CAUTION]
> Use this method if the underlying data remains the same, but the field name has changed in your system. Don't repurpose attribute name labels, as this can create issues in reporting. Instead, create a new attributes. For example, if Department changes to Team and the values in that column change too, add a new Team attribute and don't rename Department to Team.
