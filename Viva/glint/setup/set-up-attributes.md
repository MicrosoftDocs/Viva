---
title: Set up attributes in Viva Glint
description: In preparation for uploading employee data to Microsoft Viva Glint, perform attribute setup and mapping that will establish which attributes should be included in data uploads. 
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
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
ms.localizationpriority: high pri
ms.date: 04/21/2023
---

# Set up attributes in Viva Glint

In preparation for uploading employee data to Microsoft Viva Glint, complete attribute setup and mapping to establish which attributes should be included in all data uploads. Effective setup and maintenance of attributes in Viva Glint surfaces data for reporting, role setup, and distribution lists for seamless surveying and results analysis.

## Set up employee data attributes

In Viva Glint, use the in-platform guided, four-step attribute setup process to prepare the system to import employee data.

### Upload attributes

To set up your attributes in Viva Glint, your uploaded file must contain a finalized attribute header row and one row of employee data (ideally, test data). Ensure that values in the employee record align with the format that Viva Glint will receive in the future. Format all date fields in your expected format, such as mm/dd/yyyy.

1. From the admin dashboard, select the **Configure** symbol.
2. In *Employees*, select **People**.
3. Select **Get Started**.
4. Upload your finalized attributes in .csv (UTF-8 encoded) or .xlsx (single tab, no password, or formulas) format.
5. Select **Continue**.

### Preview employee data fields

Preview the attributes from the file uploaded. Check that the attribute names and values appear as expected.

1. Verify that:
   - All attributes are present in the preview.
   - Attribute values shown for preview employee records display in the correct column.
   - The total count of "data fields found" displayed above the preview matches the number of attributes in the file.
2. For date fields, select the " **There are date fields...**" checkbox and then the appropriate **date format** from the dropdown menu.

   > [!NOTE]
   > All attributes that include dates must follow the same format. Viva Glint will transform incoming dates to Viva Glint's preferred format, yyyy/mm/dd, upon upload.

3. After reviewing, select **Continue**.

### Set up attributes

Map the attributes from the uploaded file to Viva Glint required, hierarchy, and derived attributes.

### Required attributes

Select your attribute from the dropdown for each Viva Glint required attribute:

- First Name
- Last Name
- Email
- Employee ID
- Status

### Hierarchy groups

Select your attributes from the dropdown menu for each hierarchy group.

- To add additional levels to a hierarchy, select **+ Add Level**.
- To add a new hierarchy group, select **+ Add Hierarchy Group**.
- To rename the hierarchy label, select the **pencil** symbol.
- To delete a group or level, select the **trash can** symbol.

> [!NOTE]
> Hierarchy groups cannot be edited after setup. Confirm that all groups and hierarchies contain accurate attributes before saving.

### Derived attributes

Viva Glint calculates attributes based on data sent in your file. In this section, select which attributes should be calculated and the attributes that Viva Glint should use to create Manager Hierarchy, Tenure Groups, and Age Groups.

1. Select the checkbox for the desired calculated attributes: Manager Hierarchy, Tenure Groups, and Age Groups.
2. Select the attribute from the dropdown menu used to calculate each derived attribute. For example, Manager ID, Hire Date, and Birth Year.
3. Select **Continue**.

### Review uploaded attributes

Review your attribute selections before you finalize your setup.

1. Select a method to complete your Viva Glint attribute setup:

   - **Save attributes and import employee data** : Save the attributes in your upload file header row and import any employee data included in the upload.
   - **Save attributes and discard employee data:** Save the attributes in your upload file header row - only -and discard any employee data included in the upload.

   > [!TIP]
   > Viva Glint recommends the "Save attributes and discard employee data" option for initial setup to prevent the upload of any unwanted test data and to allow you to set up your attributes in preparation for uploading finalized employee data via SFTP or a manual import.

2. Select **Save**.

## Edit employee data attributes

Use the guidance below to update your attribute setup to accept any attribute header row changes in your data files so that they continue to import.

### Edit attribute names

> [!CAUTION]
> Use this method if underlying data remains the same, but the field name has changed in your system. Do not repurpose attributes name labels, as this can create issues in reporting. Instead, create a new attribute.

1. Select **Configure**.
2. In **Employees** , select **People**.
3. Select **Actions** and then **Edit User Attributes**.
4. Select the corresponding vertical ellipses to the far right of the attribute in **Active Attributes**.
5. Select **Rename Attribute**.
6. Enter the new name in the **Attribute Name** field.
7. Select **Rename**.
8. Select **Save Changes**.

### Add new attributes

Use the guidance below to update your attribute setup to accept any attribute header row changes in your data files so that they continue to import.

1. Select **Configure**.
2. In **Employees** , select **People**.
3. Select **Actions** and then select **Edit User Attributes**.
4. Upload your dataset with all current and new attributes and at least one row of employee data that aligns with your current formatting.
5. Select **Continue**.
6. For dates, select the " **There are date fields...**" box and select your current date format **date format** from the dropdown menu.
7. Preview your data and confirm new attributes shaded in green and marked as new.
8. Select **Continue**.
9. The **Attributes Setup** page will show current attributes and doesn't require edits. Select **Continue**.
10. Review and select the desired option:
    - **Save attributes and import employee data** : Save the attributes in your upload file header row and import any employee data included in the upload.
    - **Save attributes and discard employee data:** Save the attributes in your upload file header row only and discard any employee data included in the upload.
11. Select **Save**.