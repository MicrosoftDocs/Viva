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

:::image type="content" source="../../media/glint/setup/glint-get-started.png" alt-text="Screenshot of the Get Started button for attribute setup on the People page.":::

Follow the onscreen guidance for the following actions.

## Upload dataset

Upload finalized attributes in the format you have chosen. This file format will determine the format for all future uploads. Select **Continue.**

:::image type="content" source="../../media/glint/setup/setup-step1.png" alt-text="Screenshot of attribute setup step 1 to upload your attributes in a finalized file layout.":::

## Preview employee data fields

Check that the attribute names and values appear as expected.

:::image type="content" source="../../media/glint/setup/setup-step2.png" alt-text="Screenshot of attribute setup step 2 to preview uploaded attributes.":::

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

:::image type="content" source="../../media/glint/setup/setup-step3-required.png" alt-text="Screenshot of attribute setup step 3 to map required attributes.":::

### Derived attributes

Viva Glint calculates attributes based on data sent in your employee attribute file. Most organizations choose to include a managerial hierarchy. Select your option and the attribute that should be used to create it. Decide whether to include tenure groups based on hire date or age groups based on birth year.

|Derived Field   |Based On   |Derived Values|
|----------|-----------|------------|
|Manager Hierarchy|Employee ID and Manager ID data relationship  |Up to 25 manager levels, starting with the CEO/top-level leader|
|Tenure* |Hire Date   |<1 Year, 1-2 Years, 2-4 Years, 4-6 Years, 6-10 Years, 10-15 Years, 15-20 Years, 20+ Years|
|Age Grouping     |Birth Year       |<25, 25-29, 30-34, 35-39, 40-44, 45-49, 50-54, 55-59, 60-64, 65-69, 70+       |

*Tenure values for new Viva Glint customers after January 13, 2024. Prior to this date: 0-1 Year, 1-2 Years, 2-3 Years, 3-4 Years, 4-5 Years, 5-7 Years, 7+ Years.

> [!IMPORTANT]
> Don’t include derived attributes in your employee data file, Viva Glint creates these fields.

1. Select the section with the desired attribute.
2. Select the desired attribute from the dropdown menu for each derived attribute.
3. Select **Continue**.

:::image type="content" source="../../media/glint/setup/setup-step3-derived.png" alt-text="Screenshot of attribute setup step 3 to map derived attributes.":::

### Optional System Attributes

Map attributes in your employee data to Viva Glint language, time zone, and personal email fields to indicate how and when to communicate with employees. Choose to enable any of the following fields by selecting the checkbox and choosing a field from your file in the **Sync From** dropdown menu:

|Viva Glint Field   |Description  |
|----------|-----------|
|Survey Language     |The language in which employees receive surveys and emails.      |
|Dashboard Language|The language in which users view dashboards.  |
|User Timezone|The time zone in which survey communications are sent.  |
|Personal Email|Users' personal email addresses that can be used to survey exiting employees. Select Company and Personal Email in the Communications section of your survey program.  |

:::image type="content" source="../../media/glint/setup/setup-step3-optional.png" alt-text="Screenshot of attribute setup step 3 to map optional system attributes.":::

> [!IMPORTANT]
> Send language and time zone values exactly as they appear in related tabs in the [Employee Attribute Template](https://www.microsoft.com/en-us/download/details.aspx?id=105533). Users with blank or invalid values will receive and access surveys/emails/dashboards in your organization's default selection in General Settings.

> [!NOTE]
> Optional system attributes aren't included in raw response data exported from Viva Glint survey programs.

### Hierarchy groups

Select your attributes from the dropdown menu for each hierarchy group.

- To add more levels to a hierarchy, select **+ Add Level**.
- To add a new hierarchy group, select **+ Add Hierarchy Group**.
- To rename the hierarchy label, select the **pencil** symbol.
- To delete a group or level, select the **trash can** symbol.

:::image type="content" source="../../media/glint/setup/setup-step3-hierarchies.png" alt-text="Screenshot of attribute setup step 3 to map hierarchy group attributes.":::

## Review

Review a summary of all selections made in attribute setup and use the **Go Back** option to make any corrections before moving forward. The review step includes the following sections:

- Summary
- User Attributes
- Removed User Attributes
- Required Attributes Mapping
- Derived Attributes Mapping
- Optional System Attributes Mapping
- Hierarchy Groups Mapping

:::image type="content" source="../../media/glint/setup/setup-step4-review.png" alt-text="Screenshot of attribute setup step 4 to review uploaded attribute mapping.":::

> [!NOTE]
> Viva Glint allows for up to 100 User Attributes. Required, optional system, and hierarchy attributes don't count toward this limit.

## Choose how you want to import data

1. Choose between the following two options:

:::image type="content" source="../../media/glint/setup/setup-step5-choose-import.png" alt-text="Screenshot of attribute setup step 5 to confirm attribute and data import options.":::

- Option 1 - Save attributes and import employee data – Recommended if the employee data in your file is complete and finalized (doesn't contain test or partial data).

     > [!CAUTION]
     > Employee data can't be deleted. This option performs a full employee upload, which applies any changes in the file and marks anyone not in the file as an inactive employee.

- Option 2 - Save attributes and discard employee data – Recommended to configure attributes based on your header row and then import finalized employee data later.

     > [!TIP]
     > Viva Glint recommends the **Save attributes and discard employee data** option for initial setup. This allows you to set up and map your attributes in the system and complete your first data import as a separate task.

2. Select **Save**.

## Update attributes after initial setup

To add new attributes or rename attributes after your initial setup, use [Update attributes in Viva Glint](update-attributes.md) guidance.

