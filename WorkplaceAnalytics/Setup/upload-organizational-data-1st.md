---
# Metadata Sample
# required metadata

title: Upload organizational data to Workplace Analytics (first upload)
description: How to upload organizational data by using the pages of the new Workplace Analytics onboarding experience 
author: paul9955
ms.author: v-pascha
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
  > <ul><li>Make sure that the file that you are uploading is not open in a different program when you begin the upload process.</li><li>The .csv file that you upload must be UTF-8 encoded.</li><li>After the upload process begins, the process is irreversible.</li></ul> 

<!-- THE FOLLOWING SHOULD NOT APPLY FOR THE FIRST UPLOAD OF DATA: 
  > [!Note]
  > If you are uploading new data, go to step 8, _Complete new file upload_. However, if you have uploaded data and then discovered that it contains sensitive, incorrect, or unauthorized data, you must remove the uploaded data and replace it with a new file. To do this, go to step 9, _Append or replace organizational data_.
-->

4. To complete a new-file upload, select **Next**. This displays the System fields table. Go to [Field mapping](#field-mapping).

## Field Mapping

You need to map the fields (columns) for the source .csv file to the field names that Workplace Analytics recognizes. You map these fields during the Upload step, as indicated in the progress bar on the **Setup** page:

   ![Map data fields](../images/wpa/setup/onboarding-mapping-2.png)

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

<!-- NOTE THAT VALIDITY THRESHOLD DOES NOT APPLY TO FIRST UPLOAD! -->

### Custom fields table

* **Custom fields** are displayed on this page below the optional fields. Custom fields are optional attributes you can create. Select a column from your source.csv file. Name the column, select the data type, and then select the report option.

### Columns in the fields tables

* **Source column** corresponds to each of the fields in the uploaded file.

* **Workplace Analytics name** is the name of this attribute in your organization's Workplace Analytics data. <!-- VERIFYING THIS NAME WITH PRAMOD. IT MIGHT BE WORKPLACE ANALYTICS ATTRIBUTE -->

* **Data type** is the data type of the fields.

   >[!Note]
   >If the data type is Boolean, the value for the Boolean field must be TRUE or FALSE.

* **Include in report** lets you decide how to treat sensitive data in the report that will be generated about the import operation. 

    ![Map data fields](../images/wpa/setup/map-fields-include-column-65-85-1st.png) 

The drop-down menu under **Include in report** offers the following options for each of the columns in your source data:

   * **Show in report:** Let the actual data value display in the report just as it was imported in the organizational data file.

   * **Exclude from report:** Prevent the data value from appearing in the report. For data-privacy reasons, some attributes (such as ManagerID) are automatically assigned the value "Exclude from report" and this value cannot be changed. 

   * **Hash in report** de-identifies sensitive data. This option includes the data in the report that it generates about the import operation, but instead of displaying the actual value that was taken from the source file, it shows a hashed version of the value – a format that cannot be read. 

**To map fields**

After you complete the steps in [File upload](#file-upload), the **Upload** page with the System fields table will appear.

1. Map the required fields.

    ![System fields table](../images/wpa/setup/2-orgd-map-fields.png) 
  
   <ol type="a"> 
   <li>Determine which of the columns in your .csv file correspond to the second column in the table (Workplace Analytics name).</li>
   <li>Under <b>Source column</b> (the first column in the table), click the down arrow. This displays a list of the column names that were found in the .csv file. From the list, select the correct column name for this data.</li> 
   <li>Fill in appropriate values for the other columns in the table: Workplace Analytics name, Data type, and so on. Repeat these mapping steps for the rest of the required fields and for any optional fields that you choose to map.</li>
   </ol>

   > [!Note]
   > For more information, see [Columns in the fields tables](#columns-in-the-fields-tables).

2. Map the optional and custom fields, as applicable. You only need to map the columns in the source data (.csv) file that your organization considers important for analysis. For example, if StartDate is important and your data contains this field, map it. 

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

After you complete the steps in [Field mapping](#field-mapping), the **Upload** page shows the following message:

![File is uploading](../images/wpa/setup/up-1-verifying-zoom.png)

After the file has successfully uploaded, file validation starts: 

![Validating now](../images/wpa/setup/validation-full-screen.png) 

In most cases, file validation should complete very quickly. If your organizational data file is very large, validation could take up to one or two minutes. 

During this step, if you decide that the data you are uploading is not the correct data and that you want to upload a different data file instead, select **Cancel**. 

After this phase completes, the file has either passed or failed validation. Go to the appropriate section:

[Validation succeeds](#validation-succeeds)

[Validation fails](#validation-fails)

## Validation succeeds

If validation succeeds, in the **Validation results** section, the page displays the _Succeeded_ notification, which reports information about the data that was successfully uploaded and validated:

![Validation succeeded](../images/wpa/setup/4-orgd-reprocess.png)

After successful validation, Workplace Analytics processes your new data.

You can select **Settings** > **Upload** > **Organizational data** to show the **Upload history** page. You can then select **Successes** to see the workflows that were successfully validated (and uploaded).

On this page, you have the following options:

 * Select the **View** (eye) icon to see a summary of the validation results.
 * Select the **Mapping** icon to see the mapping settings for the workflow.
 * Select the **Validation** (download) icon to see a list of validation warnings.

> [!Note]
> Each tenant can have only one upload in progress at a time. Therefore you need to complete the workflow of one data file, which means you either guide it to a successful validation or abandon it, before you begin the workflow of the next data file. The status or stage of the upload workflow is shown on the progress bar across the top of the **Upload** page.

## Validation fails

If data validation fails, the **Setup** page shows a "could not be validated" notification in the **Upload details** area. This page also presents you with options of how to proceed.

![Validation failed](../images/wpa/setup/onboarding-validation-failed.png)

Before you address the problem, you can select **Download error log**. This log file describes the problems in your data that might have caused the validation errors. Use this information to decide what to do next &mdash; fix the source data or change your mapping settings. The following section describes these options: 

### Options upon failed validation

[!INCLUDE [Options upon failed validation](../includes/org-data-failed-validation-1st.md)]


