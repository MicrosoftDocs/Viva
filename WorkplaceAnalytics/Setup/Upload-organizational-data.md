---

title: Subsequent uploads of organizational data into Workplace Analytics
description: Steps for subsequent organizational (HR) data uploads into Workplace Analytics assuming this is not your first data upload
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

# Subsequent uploads of organizational data

Administrators can use the following steps for a subsequent upload (import) of organizational data into Workplace Analytics. Complete the steps after preparing the data as described in [Prepare organizational data](Prepare-organizational-data.md).

  > [!Important]
  > Only follow these steps if this is **not** the first time you have uploaded organizational data to Workplace Analytics. If this **is** the first time, follow the steps in [Upload organizational data (first upload)](upload-organizational-data-1st.md).

## Import tasks

The task of importing organizational data has three parts:

1. [File upload](#file-upload)
2. [Field mapping](#field-mapping)
3. [Data validation](#data-validation)

After you prepare the source data, you can upload the .csv file and map fields. After you map fields, Workplace Analytics validates the data. When the data successfully validates, the overall data-import task is complete. If the data validation is not successful, you can choose from a few options that are described in [Validation fails](#validation-fails).

### Video: Upload organizational data

The following video might not represent your exact upload experience that is based on your unique environment and organizational data.

<iframe width="640" height="564" src="https://player.vimeo.com/video/282897809" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>

## File upload

In the following steps, you specify a .csv file to upload to Workplace Analytics.

**To select the file to upload**

1. Open [Workplace Analytics](https://workplaceanalytics.office.com). If prompted, enter your organizational credentials.
2. In the left navigation pane, select **Settings**.
3. Select **Organizational data**. The **Upload history** area of this page shows the previous data uploads from your organization.
4. Select **New upload**.
5. In **Upload**, select **Name your upload**, and then enter a name, and then optionally, select **Add an optional description** and enter a description.
6. Select one of the following:

   * **Add employees** - Adds new employees to your existing organizational data that's already been uploaded into Workplace Analytics.
   * **Edit employee data** - Enables you to add, edit, or delete data (attributes) for existing employees within the organizational data that you've already uploaded into Workplace Analytics.
   * **Select here to upload a new organizational data file** - Deletes the existing file and uploads a new file.

     >[!Important]
     >If you discover that an existing data upload has sensitive, incorrect, or unauthorized data, use **Select here to upload a new organizational data file** to remove the existing uploaded data and replace it with new employee data.

7. If adding employees, skip to **Step x**. If editing employee data, in **Edit**, select **Add attributes**, select the .csv file with the new employee data you want to upload, and then select **Open** after reviewing the following important considerations:

   * The .csv file that you upload must be UTF-8 encoded.
   * Confirm the .csv file is not open in a different program when you begin the upload process.
   * After the upload process begins, the process is irreversible.

8. Select **Confirm** for the warning message.
9. In **Source column in file**, map the names in the .csv file that correspond with the **Workplace Analytics attributes**:

    <img src="../images/wpa/setup/upload2-map-sys-fields.png" alt="System fields table">

10. Enter values for the other columns in the table as applicable, such as for **Data type** and **Report options**.

    >[!Note]
    >For details about column options, see [Columns in the fields tables](#columns-in-the-fields-tables).

11. Map the optional and custom fields, as applicable. You only need to map the columns in the .csv file that your organization considers important for analysis. For example, if "Region" is important and your data contains this field, map it.

    <img src="../images/wpa/setup/upload3-map-custom2.png" alt="Custom fields table">

12. In **Submit for validation**, select the check box for **I confirm that these mappings are correct**, and then select **Submit** to start the upload and validation process.

13. After you select **Submit**, the following can cause a warning message:

    * **Omitted columns** - If (a) You chose the **Replace** option for uploading organizational data, and (b) while mapping fields, you have chosen to omit one or more columns that are present in the existing organizational-data schema, and (c) at least one auto-refresh query depends on those (omitted) columns.

    * **Excluded columns** - If (a) While setting the **Report options** for attributes on the **Mapping** page, you have chosen to exclude one or more columns from query results, and (b) at least one auto-refresh query depends on those (excluded) columns.

    If you see a warning message about either of these issues, go to [If expected columns are missing or excluded](#if-expected-columns-are-missing-or-excluded). If you do not see a warning message, go to [Data validation](#data-validation).

## Field mapping

You need to map the fields (columns) for the source .csv file to the field names that Workplace Analytics recognizes. You map these on the **Organizational data > Upload** page.

<img src="../images/wpa/setup/upload2-map-top.png" alt="Upload page">

The **Upload** page includes tables for System fields and Custom fields for mapping the data for the upload file.

When appending new attributes to an existing upload, you need to select all the same required and optional attributes that you mapped before in previous uploads, in addition to the new attributes you want to add (append).

<!-- TWO OF THE FOLLOWING THREE SECTIONS (system fields tabLe, custom fields table, columns in the fields tables) ARE LONG AND THIS MAKES THE TOPIC HARDER TO NAVIGATE. CONSIDER PRESENTING THEM IN TABS, RATHER THAN CONSECUTIVELY. -->

### System fields

<!-- The following include is for "system" fields and is meant only for subsequent uploads, and only temporarily. After the UI changes, switch to the "system default" include file. -->
[!INCLUDE [System fields table](../includes/org-data-sys-fields.md)]

### Custom fields

**Custom fields** are optional attributes you can create. Select a column from the .csv file. Name the column, select the data type, set the [validity threshold](#set-validity-threshold-for-custom-fields), and then select the report option.

### Field table columns

* **Source column** corresponds to each of the fields in the uploaded file.
* **Workplace Analytics name** is the name of your organization's Workplace Analytics.

* **Data type** is the data type of the fields.

   >[!Note]
   >If the data type is Boolean, the value for the Boolean field must be TRUE or FALSE.

* **Validity threshold** sets the percentage of rows in the uploaded file that must have non-null values (no blanks) for the attribute. The source file might still be valid even if some rows have missing values for some columns. This setting is not intended to check or allow invalid values. A single invalid value, such as an incorrect data type, email address, or TimeZone string will cause the file upload to fail.

   <b>Summary of Validity threshold settings</b>

   * **Required attributes:** Because PersonId and EffectiveDate are required attributes, their Validity threshold value is 100%. This value cannot be changed.

   * **Fields with minimum values:** The threshold for the ManagerId, Organization, and LevelDesignation fields is set to 95% by default.

   * **Other system fields:** The Validation threshold for other system fields is set to 95% by default, but you can increase or decrease this value.

   * **Custom fields:** See [Set Validity threshold for custom fields](#set-validity-threshold-for-custom-fields).

* **Include in report** lets you decide how to treat sensitive data in the report that will be generated about the import operation.

    ![Map data fields](../images/wpa/setup/map-fields-include-column-65.png) 

The drop-down menu under **Include in report** offers the following options for each of the columns in your source data:

   * **Show in report.** Let the actual data value appear in the report just as it was imported in the organizational data file.

   * **Hash in report.** De-identify sensitive data. If you choose this option, the report will include data that was generated about the import operation, but instead of showing actual values that were taken from the source file, it shows a hashed version of the value – a format that cannot be read.

   * **Exclude from report:** Prevent the data value from appearing in the report. You can select this option for any attribute that you consider highly sensitive. However, for data-privacy reasons, Workplace Analytics _automatically_ assigns **Exclude from report** to particular attributes, such as ManagerID. In those cases, you cannot change this value.

     > [!Note]
     > The visibility of one or more attributes (columns) might be set to **Show in report** or **Hash in report** for previously uploaded data. If you change this setting to **Exclude from report**, any auto-refresh query that depends on the data in that column will experience a schema violation.
     >
     > In this case, after you finish mapping fields, Workplace Analytics shows a warning message that reads "Your upload has certain issues that may affect execution of the auto refresh queries." If you see this message, go to [If expected columns are missing or excluded](#if-expected-columns-are-missing-or-excluded).

### If expected columns are missing or excluded

For a query to run successfully, it requires particular attributes (columns) to be present in the organizational data. This is also true for queries for which the [auto-refresh option](../tutorials/query-auto-refresh.md) is turned on. If expected columns are missing, or if visibility settings (which you set by using the **Report options** on the **Mapping** page) exclude expected columns, Workplace Analytics shows a warning message: 

   ![auto-refresh query warning](../images/wpa/setup/auto-refresh-warning.png)

Below this message, a table in the **Warning details** area lists the affected auto-refresh queries and provides details about issues that were encountered. This information is for review only. You cannot change data or mapping settings on this page. 

After you review the issues, if you decide not to continue with the data replacement, select **Back.** This returns you to the field mapping page; continue with the steps in [To map fields](#to-map-fields). 
        
To continue with data upload despite the issues, select **Next**. Note that this choice will turn auto-refresh off for queries that were listed in the **Warning Details** area. The results of the last runs of these queries remain available. 

## Data validation

After you complete the steps in [Field mapping](#field-mapping), the organizational data file is uploaded and validated, and the **Upload** page shows the _File is being uploaded_ screen:

![Upload in progress](../images/wpa/setup/upload4-uploading.png)

In most cases, file validation should complete very quickly. If your organizational data file is very large, validation could take up to one or two minutes.

After this phase completes, the file has either passed or failed validation. Go to the applicable section for details:

* [Validation succeeds](#validation-succeeds)
* [Validation fails](#validation-fails)

> [!Note]
> Each tenant can have only one upload in progress at a time. Therefore you need to complete the workflow of one data file, which means you either guide it to a successful validation or abandon it, before you begin the workflow of the next data file. The status or stage of the upload workflow is shown on the progress bar across the top of the **Upload** page.

> [!Important]
> You must stay logged in while the file is uploading or the upload will be canceled. The upload requires this page to be open in your web browser during the upload. If you close the browser (or this browser page), the upload will fail.

## Validation succeeds

If validation succeeds, the **Upload** page will indicate it and show the size of the upload and that the overall process is complete. After successful validation, Workplace Analytics processes your new data. 
 
<img src="../images/wpa/setup/upload6-validated.png" alt="Validation succeeded">

You can select **Settings** > **Upload** > **Organizational data** to see **Upload history**. You can then select **Successes** to see the workflows that were successfully validated (and uploaded).

You can do the following for an upload:

 * Select the **View** (eye) icon to see a summary of the validation results.
 * Select the **Mapping** icon to see the mapping settings for the workflow.
 * Select the **Download log** icon to see the log.

> [!Note]
> Each tenant can have only one upload in progress at a time. Therefore you need to complete the workflow of one data file, which means you either guide it to a successful validation or abandon it, before you begin the workflow of the next data file. The status or stage of the upload workflow is shown on the progress bar across the top of the **Upload** page.

## Validation fails

If data validation fails, the **Validation** page shows a "Validation failed" notification. It also shows details about the validation attempt and presents you with options:

<img src="../images/wpa/setup/upload9-val-failed-upload-flow.png" alt="Validation failed">

After a failed validation, it's best to first gain an understanding of the errors by scanning the error summary table. You can also select **Download issues** to examine the error log.

This information about the errors helps you decide which path to choose next &mdash; whether to fix the source data, change the mapping, or abandon the current upload. The following describes these options:

### Options for a failed validation

[!INCLUDE [Options upon failed validation](../includes/org-data-failed-validation.md)]

### Addition of a new data column

Let's say that you've already uploaded at least 13 months of snapshot data, which contained the five required columns (PersonId, EffectiveDate, LevelDesignation, ManagerId, Organization) for all employees. Now, you want to upload one new column of data – for example, an engagement score value for each employee – and you want it to apply to all of the historical data. When you upload to append the new "EngagementScore" data column, remember to reupload all five of the minimum required fields along with the new field.

### Set Validity threshold for custom fields

The threshold checks for non-null values, so it depends on the intended use of the custom field. If you intend to use this data in much of your analysis, consider setting it to a high percentage. You can set a lower threshold for data that applies, for example, to only a small subset of people in your organization.

#### Set a high value

Generally, you should set the Validity threshold to a high value. This is especially important if your analysis will focus on that field.

For example, you might include a "SupervisorIndicator" attribute. At first, you might not think that you're analyzing manager behavior and you might be tempted to omit this attribute. But the organization hierarchy is used implicitly by many Workplace Analytics analyses – for differentiating different work groups, for determining high- and low-quality meetings based on how many levels attend, and more.

#### Set a lower value

The goal of your analysis might be to determine sales effectiveness. Your data might include an attribute for sales attainment that only makes sense for members of your sales force, who constitute about 10% of the company. This number doesn't apply to engineers or program managers, but it is critical for high-performers in sales.  
