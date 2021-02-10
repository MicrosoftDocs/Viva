---

title: Upload you first organizational data file into Workplace Analytics
description: Learn how to upload organizational data through the new Workplace Analytics onboarding experience 
author: madehmer
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Upload organizational data (first upload)

Administrators must first upload (import) organizational data before you can analyze insights about your company in Workplace Analytics. Complete the following steps after preparing data as described in [Prepare organizational data](Prepare-organizational-data.md).

>[!Important]
>Only use the following steps if this is the **first time** you are uploading organizational data. If this is not your first upload, see [Upload organizational data (subsequent uploads)](upload-organizational-data.md) to update previously uploaded data.

## Import tasks

The task of importing organizational data has three parts:

1. [File upload](#file-upload)
2. [Field mapping](#field-mapping)
3. [Data validation](#data-validation)

After you prepare the source data, you can upload the .csv file and map fields. After you map fields, Workplace Analytics validates the data. When the data successfully validates, the overall data-import task is complete. If the data validation is not successful, you can choose from a few options that are described in [Validation fails](#validation-fails).

### Video: Upload organizational data

<iframe width="640" height="564" src="https://player.vimeo.com/video/282897809" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>

## File upload

After the initial processing of collaboration data is complete, the next time you open Workplace Analytics, the page automatically updates to let you know it's time to upload your organizational data as a .csv file into Workplace Analytics. Use the following steps to do so.

1. In **Upload**, select **Name your upload** and enter a name.
2. Optionally, select **Add an optional description** and type a description.
3. Click **Select a file**, select the .csv file to upload, and then select **Open** after reviewing the following **important upload considerations**:<a name="important-upload-considerations"></a>

   * The .csv file that you upload must be UTF-8 encoded.
   * Confirm the .csv file is not open in a different program when you begin the upload process.
   * After the upload process begins, the process is irreversible.

<!-- THE FOLLOWING SHOULD NOT APPLY FOR THE FIRST UPLOAD OF DATA: 
  > [!Note]
  > If you are uploading new data, go to step 8, _Complete new file upload_. However, if you have uploaded data and then discovered that it contains sensitive, incorrect, or unauthorized data, you must remove the uploaded data and replace it with a new file. To do this, go to step 9, _Append or replace organizational data_.
-->

4. To complete a new upload, select **Next**. This displays the System fields table. Go to [Field mapping](#field-mapping).

## Field Mapping

You need to map the fields (columns) for the source .csv file to the field names that Workplace Analytics recognizes. You map these fields during the Upload step, as indicated in the progress bar on the **Setup** page:

   ![Map data fields option](../images/wpa/setup/onboarding-mapping-2.png)

This page includes tables for System default fields and Custom fields for mapping the data for the upload file. These field types are described in the following sections.

### System default fields

<!-- The following include is for "system default" fields and should remain the correct one for this file (first time upload) and should soon be the correct one for all uploads, including subsequent uploads. -->

<!-- Formerly here: 
[!INCLUDE [System default fields](../includes/org-data-sys-default-fields.md)]
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

### Custom fields

* **Custom fields** are displayed on this page below the optional fields. Custom fields are optional attributes you can create. Select a column from your source.csv file. Name the column, select the data type, and then select the report option.

### Field column details

* **Source column** corresponds to each of the fields in the uploaded file.

* **Workplace Analytics name** is the name of this attribute in your organization's Workplace Analytics data. <!-- VERIFYING THIS NAME WITH PRAMOD. IT MIGHT BE WORKPLACE ANALYTICS ATTRIBUTE -->

* **Data type** is the data type of the fields, such as Email or DateTime.

   >[!Note]
   >If the data type is Boolean, the value for the Boolean field must be TRUE or FALSE.

* **Include in report** lets you decide how to treat sensitive data in the report that will be generated about the import operation. If offers the following options for each of the columns in your source data:

    ![Map data field columns to include](../images/wpa/setup/map-fields-include-column-65-85-1st.png)

  * **Show in report** - Lets the actual data value display in the report just as it was imported in the organizational data file.
  * **Exclude from report** - Prevents the data value from appearing in the report. For data-privacy reasons, some attributes (such as ManagerID) are automatically assigned the value "Exclude from report" and this value cannot be changed.
  * **Hash in report** - De-identifies sensitive data. This option includes the data in the report that it generates about the import operation, but instead of displaying the actual value that was taken from the source file, it shows a hashed version of the value – a format that cannot be read.

#### To map fields

After you complete the steps in [File upload](#file-upload), do the following to map the fields:

1. In **Upload**, map the required fields.

    ![System fields table](../images/wpa/setup/2-orgd-map-fields.png)
  
   1. Determine which of the columns in your .csv file correspond to the second column in the table (Workplace Analytics name).
   2. In **Source column** (the first column in the table), select the name that corresponds with the applicable Workplace Analytics attribute name.
   3. Select or enter the applicable values for the other columns, including the **Data type** and **Report options**.
   4. Repeat these steps for all the required system fields.

   >[!Note]
   >See [Field column details](#field-column-details) for more information.

2. Map the optional and custom fields, as applicable. You only need to map the columns in the source data (.csv) file that your organization considers important for analysis. For example, if **StartDate** is important and your data contains this field, map it.

   1. In **Source column** (the first column in the table), select the applicable names for the data you want to upload.
   2. Select or enter the values for the other columns in the table, such as the data type and report options.
   3. Repeat these steps for all custom fields that are important to your organization.

   <img src="../images/wpa/setup/upload3-map-custom2.png" alt="Custom fields table">

3. In **Submit for validation**, select the check box for **I confirm that these mappings are correct**, and then select **Next**. You'll then see a notice about "your file is uploading."

>[!Important]
>You must stay logged in while the file is uploading or the upload will be canceled. The upload requires this page to be open in your web browser during the upload. If you close the browser (or this browser page), the upload will fail.

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
