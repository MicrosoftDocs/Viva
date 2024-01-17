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
ms.date: 01/17/2024
---

# Set up attributes in Viva Glint

Before using the guidance on this page, you should have created your Employee Attribute Template. All required and custom attributes, and hierarchies, should appear as you would like them to appear on all reports going forward. This first row is your file blueprint.

> [!TIP]
> Ensure that attribute labels stay consistent over time in your Employee Data File. For example, if an attribute is set up as "Employee ID," it will not later be recognized as the same column renamed as "Employee Number".

Use the guidance in this article to set up attributes in Viva Glint based on selections you made when putting together your [Employee Attribute Template](https://www.microsoft.com/en-us/download/details.aspx?id=105533). This is your guide for setting up Viva Glint to accept data that you import to the platform long-term.

## Attribute setup in Viva Glint

To set up your attributes in Viva Glint, your uploaded file must contain a finalized attribute header row and at least one row of employee data. Use the in-platform, four-step attribute setup process to prepare the system to import employee data.

> [!IMPORTANT]
> Reporting hierarchies, file format, and date attribute formats can't be edited after initial setup is complete. Before beginning, confirm that the attribute selections in your Employee Attribute Template are **final**.

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

### Derived attributes

Viva Glint calculates attributes based on data sent in your employee attribute file. Most organizations choose to include a managerial hierarchy. Select your option and the attribute that should be used to create it. Decide whether to include tenure groups based on hire date or age groups based on birth year.

1. Select the section with the desired attribute.
2. Select the desired attribute from the dropdown menu for each derived attribute.
3. Select **Continue**.

### Optional System Attributes

Map attributes in your employee data to Viva Glint language, time zone, and personal email fields to indicate how and when to communicate with employees. Choose to enable any of the following fields by selecting the checkbox and choosing a field from your file in the **Sync From** dropdown menu:

|Viva Glint Field   |Description  |
|----------|-----------|
|Survey Language     |The language in which employees receive surveys and emails.      |
|Dashboard Language|The language in which users view dashboards.  |
|User Timezone|The time zone in which survey communications are sent.  |
|Personal Email|Users' personal email addresses that can be used to survey exiting employees. Select Company and Personal Email in the Communications section of your survey program.  |

> [!IMPORTANT]
> Send language and time zone values exactly as they appear in related tabs in the [Employee Attribute Template](https://www.microsoft.com/en-us/download/details.aspx?id=105533). Users with blank or invalid values will receive and access surveys/emails/dashboards in your organization's default selection in General Settings.

### Hierarchy groups

Select your attributes from the dropdown menu for each hierarchy group.

- To add more levels to a hierarchy, select **+ Add Level**.
- To add a new hierarchy group, select **+ Add Hierarchy Group**.
- To rename the hierarchy label, select the **pencil** symbol.
- To delete a group or level, select the **trash can** symbol.

## Review

Review a summary of all selections made in attribute setup and use the **Go Back** option to make any corrections before moving forward. The review step includes the following sections:

- Summary
- User Attributes
- Removed User Attributes
- Required Attributes Mapping
- Derived Attributes Mapping
- Optional System Attributes Mapping
- Hierarchy Groups Mapping

## Choose how you want to import data

1. Choose between the following two options:

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
2. Select **Actions** and then **Manage User Attributes**.
3. Select **Update dataset** at the top of the page.
4. Upload your dataset with all existing attributes and the new attribute(s).

     > [!NOTE]
     > Your uploaded file must contain the Attribute Header Row and at least one row of employee data that aligns with the current format.

5. Select **Continue**.
6. If dates are included in your file, select **There are date fields** and then the appropriate date format from the dropdown menu.

     > [!NOTE]
     > This selection should be your existing date format, which is consistently used for employee data.

7. Preview your data and confirm that you see the new attributes.
8. Select **Continue**.
9. The Attributes Setup page shows current required, derived, optional system, and hierarchy attributes. If the newly added field is required, derived, or an optional system attribute, make your selection in the appropriate section. Select **Continue**.
  
     > [!NOTE]
     > Derived Manager Hierarchy and Hierarchy Groups can't be edited after initial setup.
  
10. Review newly added attributes and select **Continue**.
11. Choose to **Save attributes and import employee data** or to **Save attributes and discard employee data**.

     > [!TIP]
     > When adding new attributes, choose the Save attributes and discard employee data option to save your setup in preparation for future imports.

12. Select **Save** or **Go Back** to make additional edits.

## Edit attribute names

Use the following guidance to rename attributes before updating your data files so that they continue to import seamlessly.

From the admin dashboard:

1. Select the **Configure** symbol and then in the **Employees** section, choose **People**.
2. Select **Actions** and then select **Manage User Attributes**.
3. Select the corresponding horizonal ellipses to the far right of the attribute in the Active Attributes row.
4. Select **Rename Attribute**.
5. Enter the new name in the Attribute Name field and select **Rename**.

> [!CAUTION]
> Use this method if the underlying data remains the same, but the field name has changed in your system. Don't repurpose attribute name labels, as this can create issues in reporting. Instead, create a new attributes. For example, if Department changes to Team and the values in that column change too, add a new Team attribute and don't rename Department to Team.

## Manage Derived Attributes

Viva Glint calculates attributes based on data sent in your employee attribute file. 

To edit derived fields after your initial setup:

1. Select the **Configure** symbol and then under the **Employees** section, choose **People**.
2. Select **Actions** and then **Manage User Attributes**.
3. In the **Derived Attributes** section, select **Manage Derived Attributes**.
4. Select the checkbox next to the Derived Attribute that you want to edit.
   1. To disable a Derived Attribute: Deselect the checkbox next to the desired field.
   1. To enable a Derived Attribute: Select the checkbox next to the desired field and choose a field from your data in the Calculate From dropdown menu.
   1. To update the field used to create the Derived Attribute: Select the checkbox next to the desired field and choose a new field in the Calculate From dropdown menu. 

> [!NOTE]
> Manager Hierarchy is not editable after initial setup.

## Manage Optional System Attributes

Choose how and when Viva Glint communicates with employees by mapping language, time zone, and personal emails to Viva Glint fields.

To edit optional system fields after your initial setup:

1. Select the **Configure** symbol and then under the **Employees** section, choose **People**.
2. Select **Actions** and then **Manage User Attributes**.
3. In the **Optional System Attributes** section, select **Manage Optional System Attributes**.
   1. To disable an Optional System Attribute: Deselect the checkbox next to the desired field.
   1. To enable a Optional System Attribute: Select the checkbox next to the desired field and choose a field from your data in the Sync From dropdown menu.
   1. To update the field mapped to an Optional System Attribute: Select the checkbox next to the desired field and choose a new field in the Sync From dropdown menu.
