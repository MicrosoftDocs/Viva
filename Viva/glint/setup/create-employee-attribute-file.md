---
title: Create your Employee Attribute File for Viva Glint
description: Learn how Viva Glint uses your continuously updated employee data to surface meaningful and insightful reports used to increase employee happiness at work and ultimately improve business results. 
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: file upload, upload format, attribute header row, header row, add attributes, column headings
ms.collection: 
 - M365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
localization_priority: high pri
ms.date: 04/04/2023
---
# Create your Employee Attribute File for Viva Glint

Ensuring your data file is configured and named correctly allows an import without errors. Should any errors occur, you receive an email from Microsoft Viva Glint with the information on what needs to be remedied before the file can be processed.

## Choose your file upload format

When creating your Employee Attribute File, use one of the following two formats:

- .xlsx
- .csv (comma delimited) file 

>[!TIP]
> .csv is the cleanest for file formatting as it can handle foreign characters and avoids wingdings, as you may see in Excel.

### Upload an .xlsx file

- Make sure you use only a single tab that isn't password-protected. 

### Upload a .csv file

- Make sure it's UTF-8 encoded. If the file isn't UTF-8 encoded, it may fail or cause corrupted characters to appear in your data.
- Always use a comma as a delimiter. 

>[!NOTE]
>
> - Use double quotes as text qualifiers for values that contain commas. For example, the Job Title value "Manager, Customer Success" would need to be enclosed in double-quotes to import correctly. 
> - There is a 255 character limit for each data file name. 

## Create your Attribute Header row

On your Employee Attribute Template, you have to set up the first row of your file after discussion with your internal stakeholders. All required and custom attributes, and hierarchies, should appear as you would like them to appear on all reports going forward. This first row is your file blueprint. 

Ensure that attribute labels stay consistent over time in your Employee Data File. For example, if an attribute is set up as “Employee ID,” it will not later be recognized as the same column renamed as “Employee Number.”
To create your Attribute Header row, follow these steps:

1. Create a new file, which contains only a single tab. 
2. Enter your attributes names across the columns, starting with column A. There's a 64-character limit for attribute labels. 

## Populate data into your Employee Attribute File

Now that your header row is set and you have received verification, use the following guidance to add data into your Employee Attribute File.

### Add employee attributes to the file

To add employee data attributes *before* your first file import to Viva Glint, an admin follows this process, beginning on their Viva Glint dashboard:

1. Select the **Configure** symbol.
2. In the **Employees** section, choose **People** and then **Active Employees**.
3. From the dropdown Actions menu, choose **New User Attributes**. 
4. Follow the onscreen guidance for the following actions:
   1. Step 1: Upload dataset; upload finalized attributes in the format you have chosen. This file format will determine the format for all future uploads. Select **Continue**.
   2. Step 2: Preview employee data fields; preview attributes from the file uploaded in Step 1. 
        - Verify:
           - All attributes are present
           - Attribute values for the preview employee record (10 maximum) are accurate and in the correct column
           - The total count of data fields found above the preview matches the number of attributes in your file
        - If dates are included in your file, select **There are date fields** and then the appropriate **date format** from the dropdown menu. 
          >[!NOTE]
          > All date attributes must follow the same format.
        - After previewing, select **Continue**.
   3. Step 3: Attributes setup; map your uploaded and confirmed attributes to the Viva Glint fields. This setup is divided into three sections:
       - Required attributes: Select the desired attribute from the dropdown menu for each required attribute.
       - Hierarchy groups: Select the desired attribute from the dropdown menu for each hierarchy group. 
           - To add more levels to a hierarchy, select **+ Add Level.**
           - To add a new hierarchy group, select **+ Add Hierarchy Group**. 
           - To rename the hierarchy label, select the **pencil** symbol. 
           - To delete a group or level, select the **trash can** symbol.
       - Derived attributes: Fields calculated based on data sent in your employee file. Most organizations choose to include a managerial hierarchy. Select your option and the attribute that should be used to create it. Decide whether to include tenure groups based on hire date or age groups based on birth year.
           1. Select the section with the desired attribute. 
           2. Select the desired attribute from the dropdown menu for each derived attribute.
           3. Select **Continue**.
   4. Step 4: Review; choose between the following two options:
       - Save attributes and import employee data – Recommended if the employee data in your file is complete and finalized (doesn't contain test or partial data). Caution: employee data can't be deleted. This option performs a full employee upload, which applies any changes in the file and marks anyone not in the file as an inactive employee.
       - Save attributes and discard employee data – Recommended to configure attributes based on your header row and then import finalized employee data later.
   5. Step 5: Select the desired option. 
         >[!TIP]
         > When setting up attributes for the first time, Viva Glint recommends choosing the *Save attributes and discard employee data* option. This allows you to set up and map your attributes in the system and complete your first data import as a separate task when your IT/HRIS team has completed Employee Data File work.
   6. Step 6: Select **Save**.

## Add new attributes to the file

After the initial setup, you may find that new attributes need to be added to your employee data file. Use the guidance from [Procedure for adding new attributes](#procedure-for-adding-new-attributes) to update your attribute setup before updating your data files so that they continue to import seamlessly. New attributes and their values will apply to future survey results only.

### Procedure for adding new attributes

From the admin dashboard:

1. Select the **Configure** symbol and then under the **Employees** section, choose **People**.
2. Select **Actions** and then **New User Attributes**.
3. Upload your dataset with all *existing* attributes and the *new* attribute(s).
     >[!NOTE]
     > Your uploaded file must contain the Attribute Header Row and at least one row of employee data that aligns with the current format. 

4. Select **Continue**.
5. If dates are included in your file, select **There are date fields** and then the appropriate date format from the dropdown. 
     >[!NOTE] 
     >This selection should be your existing date format, which is consistently used for employee data.
6. Preview your data and confirm that you see the new attributes. 
7. Select **Continue**.
8. The Attributes Setup page shows current required attributes and hierarchy groups and shouldn't require edits. If this is true, select **Continue**. 
9. Select the desired option. 
     >[!TIP]
     >When adding new attributes, choose the *Save attributes and discard employee data* option to save your setup in preparation for future imports. 
10. Select **Save**.

## Edit attribute column headings

After the initial attribute setup, you may find that attribute header names need to change. Use the following guidance to update your attribute setup before updating your data files so that they continue to import seamlessly. At survey launch, the Viva Glint platform takes a snapshot of employee data, and new attributes and value updated after that point don't affect data tied to active or closed surveys.

### Procedure for editing column headings

From the admin dashboard:

1. Select the **Configure** symbol and then in the **Employees** section, choose **People**.
2. Select **Actions** and then select **Edit User Attributes**.
3. Select the corresponding vertical ellipses to the far right of the attribute in the **Active Attributes** row. 
4. Select **Rename Attribute**.
5. Enter the new name in the **Attribute Name** field and select **Rename**.
6. On the top right of your dashboard, select **Save Changes**.

>[!CAUTION]
> Use this method if the underlying data remains the same, but the field name has changed in your system. Do not repurpose attribute name labels, as this can create issues in reporting. Instead, create a new one.
