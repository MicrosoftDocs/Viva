---
# Metadata Sample
# required metadata

title: Upload organizational data to Workplace Analytics (first upload)
description: How to upload organizational data by using the pages of the new Workplace Analytics onboarding experience 
author: paul9955
ms.author: v-midehm
ms.date: 02/21/2019
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

1. On the Upload page, select **Name your upload**, and then type the name of your new upload file.
2. Optionally, select **Add an optional description** and type a description of this upload.
3. In the Select file section, click **Select file**. In the dialog box that appears, select the .csv file that you want to import.

  > [!Important] 
  > Make sure the file that you are uploading is not open in a different program when you begin the upload process. 

  > [!Note]
  > If you are uploading new data, go to step 8, _Complete new file upload_. However, if you have uploaded data and then discovered that it contains sensitive, incorrect, or unauthorized data, you must remove the uploaded data and replace it with a new file. To do this, go to step 9, _Append or replace organizational data_.

4. To complete a new-file upload, select **Next**. This displays the System fields table. Go to [Field mapping](#field-mapping).

## Field Mapping

You need to map the fields (columns) for the source .csv file to the field names that Workplace Analytics recognizes. You map these fields during the Upload step, as indicated in the progress bar on the **Setup** page:

   ![Map data fields](../images/wpa/setup/05-map-data-fields.png)

This page includes tables for System default fields and Custom fields for mapping the data for the upload file.

### System default fields table

[!INCLUDE [System default fields table](../includes/org-data-sys-default-fields.md)]

[!INCLUDE [Fields tables](../includes/org-data-fields-tables.md)]

**To map fields**

After you complete the steps in [File upload](#file-upload), the Upload page with the System fields table will appear.

1. Map the required fields.
  
    <img src="../images/wpa/setup/2-orgd-map-fields.png" alt="System fields table">

   <ol type="a"> 
   <li>Determine which of the columns in your .csv file correspond to the second column in the table (Workplace Analytics name).</li>
   <li>Under <b>Source column</b> (the first column in the table), click the down arrow. This displays a list of the column names that were found in the .csv file. From the list, select the correct column name for this data.</li> 
   <li>Fill in appropriate values for the other columns in the table: Workplace Analytics name, Data type, and so on. Repeat these mapping steps for the rest of the required fields and for the optional fields that you choose to map.</li>
   </ol>

   > [!Note]
   > For more information, see [Columns in the fields tables](#columns-in-the-fields-tables).

2. Map the optional and custom fields, as applicable. You only need to map the columns in your source (.csv) file that your organization considers important for analysis. For example, if StartDate is important and your data contains this field, map it. 

   <ol type="a">
   <li>Under <b>Source column</b> (the first column in the table), select the down arrow to display the list of column names that were found in the .csv file. From the list, select the correct column name for the data. In this example, you'd select <b>StartDate</b>.</li>
   <li>Set values for the other columns in the table, such as the data type, the validity threshold, and the hash setting for reports.</li>
   <li>Repeat these steps for all custom fields that are important to your organization.</li>
   </ol>

   <img src="../images/wpa/setup/upload3-map-custom2.png" alt="Custom fields table">

3. In the Submit for validation area, select **I confirm that these mappings are correct**, and then select **Submit**. This uploads the .csv file and starts the validation process.

4. Next step is to go to [Data validation](#data-validation).

## Data validation

After you complete the steps in [Field mapping](#field-mapping), the Upload page displays the _We are validating your upload_ message.

   ![Validating the uploaded data](../images/wpa/setup/06-validating-your-upload.png)

> [!Important]  
> You must stay logged in while the file is uploading or the upload will be canceled. The upload requires this page to be open in your web browser during the upload. If you close the browser (or this browser page), the upload will fail.

## Validation succeeds

If validation succeeds, in the Validation results section, the page displays the _Succeeded_ notification, which reports information about the data that was successfully uploaded and validated:

<img src="../images/wpa/setup/4-orgd-reprocess.png" alt="Validation succeeded">

After successful validation, Workplace Analytics processes your new data.

You can select **Settings** > **Upload** > **Organizational data** to show the **Upload history** page. You can then select **Successes** to see the workflows that were successfully validated (and uploaded).

On this page, you have the following options:

 * Select the **View** (eye) icon to see a summary of the validation results.
 * Select the **Mapping** icon to see the mapping settings for the workflow.
 * Select the **Validation** (download) icon to see a list of validation warnings.

> [!Note]
> Each tenant can have only one upload in progress at a time. Therefore you need to complete the workflow of one data file, which means you either guide it to a successful validation or abandon it, before you begin the workflow of the next data file. The status or stage of the upload workflow is shown on the progress bar across the top of the Upload page.

## Validation fails

The following illustration shows a failed validation.

<img src="../images/wpa/setup/5-orgd-upload-fail.png" alt="Validation failed">

 If a data validation fails, the Data load page shows a failed notification. It also shows details about the validation attempt and presents you with options.

Before you try to address the problem, you can select **Download issues**. This displays a log file that describes the problems in your data that might cause validation errors. Use the log to either fix the source data, change your mapping settings, or abandon the current upload.

> [!Tip]
> If you have a small number of errors, you’ll probably want to fix them. If you have many errors, you might want to select **Abandon**.

### Options upon failed validation

[!INCLUDE [Options upon failed validation](../includes/org-data-failed-validation.md)]

## Tips

[!INCLUDE [Tips](../includes/org-data-upload-tips.md)]


