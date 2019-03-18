---
# Metadata Sample
# required metadata

title: Upload organizational data to Workplace Analytics (first upload)
description: How to upload organizational data by using the pages of the new Workplace Analytics onboarding experience 
author: paul9955
ms.author: v-pascha
ms.date: 03/12/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Upload organizational data (first upload)

This article presents the steps that administrators take to upload (import) organizational data to Workplace Analytics. Complete these steps after preparing data as described in [Prepare organizational data](Prepare-organizational-data.md).

  > [!Important] 
  > Follow the steps in this section if this is the **first time** that you are uploading organizational data. If this is not the first time, follow the steps in [Upload organizational data (subsequent uploads)](upload-organizational-data.md).

## Import tasks

The task of importing organizational data has three parts:

1. [File upload](#file-upload)
2. [Field mapping](#field-mapping)
3. [Data validation](#data-validation)

After you prepare the source data, you can upload the .csv file and map fields. After you map fields, Workplace Analytics validates the data. When the data successfully validates, the overall data-import task is complete. If the data validation is not successful, you can choose from a few options that are described in [Validation fails](#validation-fails).

### Video: Upload organizational data

<iframe width="640" height="564" src="https://player.vimeo.com/video/282897809" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>

## File upload

In the following steps, you specify a .csv file to upload to Workplace Analytics.

**To select the file to upload**

After the initial processing (of collaboration data) is complete, the next time you open Workplace Analytics, the page automatically updates to let you upload your organizational data file.

1. On the **Upload** page, select **Name your upload**, and then type the name of your new upload file.
2. Optionally, select **Add an optional description** and type a description of this upload.
3. In the Select file section, click **Select file**. In the dialog box that appears, select the .csv file that you want to import.

  > [!Important] 
  > <ul><li>Make sure that the file that you are uploading is not open in a different program when you begin the upload process.</li><li>The .csv file that you upload must be UTF-8 encoded.</li> 

<!-- THE FOLLOWING SHOULD NOT APPLY FOR THE FIRST UPLOAD OF DATA: 
  > [!Note]
  > If you are uploading new data, go to step 8, _Complete new file upload_. However, if you have uploaded data and then discovered that it contains sensitive, incorrect, or unauthorized data, you must remove the uploaded data and replace it with a new file. To do this, go to step 9, _Append or replace organizational data_.
-->

4. To complete a new-file upload, select **Next**. This displays the System fields table. Go to [Field mapping](#field-mapping).

## Field Mapping

You need to map the fields (columns) for the source .csv file to the field names that Workplace Analytics recognizes. You map these fields during the Upload step, as indicated in the progress bar on the **Setup** page:

   ![Map data fields](../images/wpa/setup/05-map-data-fields.png)

This page includes tables for System default fields and Custom fields for mapping the data for the upload file. These field types are described in the following sections. 

### System default fields table

<!-- The following include is for "system default" fields and should remain the correct one for this file (first time upload) and should soon be the correct one for all uploads, including subsequent uploads. -->

<!-- Formerly here: 
[!INCLUDE [System default fields table](../includes/org-data-sys-default-fields.md)]
Removed 18 March 2019 per Pramod because it refers to validity threshold.
Replaced with actual text and then removed that term: -->

System default fields represent attributes that are known by Workplace Analytics and are used in specific calculations beyond grouping and filtering. A system default field can be either required or optional.

* **Required fields** are identified in two ways. Their rows have dark shading and show as "Required" under the Source column header. These rows represent data that was found in the uploaded file. For the upload to succeed, you must map the required fields with a column in your .csv file that is the correct data type.

   >[!Important]
   >Every required field must have a valid, non-null value in every row. This means that, even if the names of these attributes are not present in the uploaded .csv file, other columns must be present in the .csv file that are mapped to these attributes.

* **Optional fields** appear below the required fields in rows that have lighter shading. These rows are commonly encountered system fields that Workplace Analytics suggests for use. You don't need to map these fields if your organization doesn't have data for them.

<!-- Formerly here: 
[!INCLUDE [Fields tables](../includes/org-data-fields-tables.md)]
Removed 18 March 2019 per Pramod because it refers to validity threshold.
Replaced with actual text and then removed that term: -->

### Custom fields table

* **Custom fields** are displayed on this page below the optional fields. Custom fields are optional attributes you can create. Select a column from your source.csv file. Name the column, select the data type, and then select the report option.

### Columns in the fields tables

* **Source column** corresponds to each of the fields in the uploaded file.
* **Workplace Analytics name** is the name of your organization's Workplace Analytics.

* **Data type** is the data type of the fields.

   >[!Note]
   >If the data type is Boolean, the value for the Boolean field must be TRUE or FALSE.

* **Include in report** lets you decide how to treat sensitive data in the report that will be generated about the import operation. 

    ![Map data fields](../images/wpa/setup/map-fields-include-column-65-85-1st.png) 

The drop-down menu under **Include in report** offers the following options for each of the columns in your source data:

   * **Show in report:** Let the actual data value display in the report just as it was imported in the organizational data file.

   * **Exclude from report:** Prevent the data value from appearing in the report.

   * **Hash in report** de-identifies sensitive data. This option includes the data in the report that it generates about the import operation, but instead of displaying the actual value that was taken from the source file, it shows a hashed version of the value – a format that cannot be read.

**To map fields**

After you complete the steps in [File upload](#file-upload), the **Upload** page with the System fields table will appear.

1. Map the required fields.
  
    <img src="../images/wpa/setup/2-orgd-map-fields.png" alt="System fields table">

   <ol type="a"> 
   <li>Determine which of the columns in your .csv file correspond to the second column in the table (Workplace Analytics name).</li>
   <li>Under <b>Source column</b> (the first column in the table), click the down arrow. This displays a list of the column names that were found in the .csv file. From the list, select the correct column name for this data.</li> 
   <li>Fill in appropriate values for the other columns in the table: Workplace Analytics name, Data type, and so on. Repeat these mapping steps for the rest of the required fields and for any optional fields that you choose to map.</li>
   </ol>

   > [!Note]
   > For more information, see [Columns in the fields tables](#columns-in-the-fields-tables).

2. Map the optional and custom fields, as applicable. You only need to map the columns in your source (.csv) file that your organization considers important for analysis. For example, if StartDate is important and your data contains this field, map it. 

   <ol type="a">
   <li>Under <b>Source column</b> (the first column in the table), select the down arrow to display the list of column names that were found in the .csv file. From the list, select the correct column name for the data. In this example, you'd select <b>StartDate</b>.</li>
   <li>Set values for the other columns in the table, such as the data type and the hash setting for reports.</li>
   <li>Repeat these steps for all custom fields that are important to your organization.</li>
   </ol>

   <img src="../images/wpa/setup/upload3-map-custom2.png" alt="Custom fields table">

3. In the **Submit for validation** area, select **I confirm that these mappings are correct**, and then select **Next**. You see a notice that states "Your file is uploading."

> [!Important]
> You must stay logged in while the file is uploading or the upload will be canceled. The upload requires this page to be open in your web browser during the upload. If you close the browser (or this browser page), the upload will fail.

The upload of the .csv file starts the validation process. 

4. The next step is [Data validation](#data-validation).

## Data validation

After you complete the steps in [Field mapping](#field-mapping), the **Upload** page displays the _We are validating your upload_ message.

   ![Validating the uploaded data](../images/wpa/setup/06-validating-your-upload.png)

## Validation succeeds

If validation succeeds, in the **Validation results** section, the page displays the _Succeeded_ notification, which reports information about the data that was successfully uploaded and validated:

<img src="../images/wpa/setup/4-orgd-reprocess.png" alt="Validation succeeded">

After successful validation, Workplace Analytics processes your new data.

You can select **Settings** > **Upload** > **Organizational data** to show the **Upload history** page. You can then select **Successes** to see the workflows that were successfully validated (and uploaded).

On this page, you have the following options:

 * Select the **View** (eye) icon to see a summary of the validation results.
 * Select the **Mapping** icon to see the mapping settings for the workflow.
 * Select the **Validation** (download) icon to see a list of validation warnings.

> [!Note]
> Each tenant can have only one upload in progress at a time. Therefore you need to complete the workflow of one data file, which means you either guide it to a successful validation or abandon it, before you begin the workflow of the next data file. The status or stage of the upload workflow is shown on the progress bar across the top of the **Upload** page.

## Validation fails

The following illustration shows a failed validation.

<img src="../images/wpa/setup/5-orgd-upload-fail.png" alt="Validation failed">

 If a data validation fails, the Data load page shows a failed notification. It also shows details about the validation attempt and presents you with options.

Before you try to address the problem, you can select **Download issues**. This displays a log file that describes the problems in your data that might cause validation errors. Use the log to either fix the source data, change your mapping settings, or abandon the current upload.

> [!Tip]
> If you have a small number of errors, you’ll probably want to fix them. If you have many errors, you might want to select **Upload new file**.

### Options upon failed validation

* **Upload new file** restarts the upload-map-validate process with new data rather than retrying the process with the current data. <!-- Select **Abandon** (at the upper right of the page). This option does not retain any of the field mappings. -->
* **Edit mapping** has two options:
  * **Fix the source data** is recommended because it fixes the data in your source .csv file and increases the quality of the data.
  * **Edit mapping** enables you to change an incorrect data type. Select **Edit mapping** to set new mapping values, after which you can retry to validate your data file.

## Tips

### Invalid values or formats

When any data row or column has an invalid value for any attribute, the entire upload will fail until the source file is fixed (or the mapping changes the validation type of the attribute in a way that makes the value valid). 

All field header or column names must:

* Begin with a letter (not a number)
* Only contain alphanumeric characters (letters and numbers, for example Date1)
* Have at least one lower-case letter (Hrbp); all uppercase won’t work (HRBP)
* Have no spaces (Date1)
* Have no special characters (non-alphanumeric, such as @, #, %, &, *)
* Match exactly as listed for Workplace Analytics’ Required and Reserved optional attributes, including for case sensitivity (for example PersonId and HireDate)

The field values in the data row must comply with the following formatting rules:

* The required EffectiveDate and HireDate field values must be in the MM/DD/YYYY format
* The required PersonId and ManagerId field values must be a valid email address (for example, gc@contoso.com). 
* The required TimeZone field values must be in a supported Windows format.
* The required Layer field values must contain numbers only.
* The required HourlyRate field values must contain numbers only, which Workplace Analytics assumes is in US dollars for calculations and data analysis.

>[!Note]
> Workplace Analytics does not currently perform currency conversions for HourlyRate data. All calculations and data analysis in Workplace Analytics assume the data to be in US dollars.

The field values also cannot contain any of the following:

* No accent marks (á)
* No tildes (~)
* No short or long dashes (-, --)
* No commas (,)
* No "new line" characters (\n)
* No double (" ") or single quotes (‘ ‘)
* Limit character length of field values in rows to a maximum of 128 KB, which is about 1024 x 128 characters

### Addition of missing data

Workplace Analytics does not modify or fill in data that is missing from HR uploads, even for EffectiveDate or TimeZone. The administrator is responsible for correcting such errors or omissions.

### Addition of a new data column

Let's say that you've already uploaded at least 13 months of snapshot data, which contained the five required columns (PersonId, EffectiveDate, LevelDesignation, ManagerId, Organization) for all employees. Now, you want to upload one new column of data – for example, an engagement score value for each employee – and you want it to apply to all of the historical data. When you upload to append the new "EngagementScore" data column, remember to reupload all five of the minimum required fields along with the new field. 

