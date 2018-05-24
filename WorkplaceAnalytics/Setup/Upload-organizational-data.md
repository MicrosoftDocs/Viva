---
# Metadata Sample
# required metadata

title: Upload organizational data in Workplace Analytics
description: How to upload data from your organization to Workplace Analytics. 
author: paul9955
ms.author: v-pascha
ms.date: 04/06/2018
ms.topic: get-started-article
ms.prod: wpa
---

# Upload organizational data

This article presents the steps that administrators take to upload organizational data to Workplace Analytics. Complete these steps after preparing data as described in [Prepare organizational data](Prepare-organizational-data.md).

## Import tasks

The task of importing organizational data has three parts: 

1. [File upload](#file-upload)
2. [Field mapping](#field-mapping)
3. [Data validation](#data-validation)

After you have prepared your source data, you upload your .csv file and map fields. After you map fields, data validation might or might not succeed. If the data successfully validates, the overall data-import task is complete. If the data at first does not validate, you can choose from among further options, which are described in [Validation fails](#validation-fails).

## File upload

In this procedure, you specify a .csv file to upload to Workplace Analytics.

**To select the file to upload**

1.	Navigate to the page for Workplace Analytics. 

     – or – 

    Click the Office 365 waffle menu (
<img src="../Images/upload-org-data-00.png" alt="Waffle menu">) and then click **Workplace Analytics**. 

2.	In the left navigation pane, click **Settings**.
3.	Click **Organizational data**. The Upload history area of this page displays the previous data uploads from your organization.
4.	Click **New upload**. This displays the Organizational data > Upload page. 
5.	Click **Name your upload** and type the name of your new upload. <!--FORMER: A “workflow” is the action of uploading your organization’s data.-->
6.	(Optional) Click **Add an optional description** and type a description of this upload. 
7.	In the Select file area, click **Select file**. In the dialog box that appears, select the .csv file that you want to import. 

  > [!Note] 
  > If you are uploading new data, go to step 8, _Complete new file upload_. However, if you have uploaded data and then discovered that it contains sensitive, incorrect, or unauthorized data, you must remove the uploaded data and replace it with a new file. To do this, go to step 9, _Replace organizational data_. 

8.	<u>Complete new-file upload:</u> Click **Next**. This displays the System fields table. Go to the next procedure, [Field mapping](#field-mapping). 
9.	<u>Replace organizational data:</u> In the Select file area, click **Show advanced options**. This opens the Append or replace area. 
10.	In the Append or replace area, select **Replace all existing organizational data with this file**. Note the warning that states “This option permanently deletes all previously uploaded organizational data.”
11.	In the warning message that is displayed, click **[Continue]**. The data in the .csv file that you specified replaces the previously uploaded data for your organization. 
12.	Go to the next procedure, [Field mapping](#field-mapping).

## Field Mapping

In this procedure, you map the fields (columns) in your source .csv file to field names that Workplace Analytics recognizes. You do this mapping on the Upload page:

<img src="../Images/upload2-map-top.png" alt="Upload page">
 
The UpLoad page displays two tables: System fields and Custom fields. You use these tables to map the data in your uploaded file. 

### System fields table

System fields represent attributes that are known by Workplace Analytics and that are used in specific calculations beyond grouping and filtering. A system field can be either required or optional: 

 * **Required fields** are identified in two ways: They appear in rows that have dark shading; under the Source column header, they are identified by the word “Required.”) These rows represent data that was found in the file that you uploaded. You must map them because the upload would fail if the mapping excluded one or more of these fields. 

  Every required field must have a valid, non-null value in every row. This means that, even if the names of these attributes are not present in the uploaded .csv file, other columns must be present in the .csv file that are mapped to these attributes.

 * **Optional fields** appear below the required fields in rows that have lighter shading. These rows are commonly encountered system fields that Workplace Analytics suggests for use. For example, a field in this section might be called “Layer”; if “Layer” is not used in your organization, do not map this field. 

### Custom fields table

 * **Custom fields** are displayed on this page below the optional fields. Custom fields are not system fields. For the custom fields, you choose a source column from your source.csv, give the column a name, choose the data type for it, set the appropriate [Validity threshold](#set-validity-threshold-for-custom-fields), and finally decide whether to include and whether to hash (obscure) the value in the import report. 

### Columns in the System fields and Custom fields tables

 * **Source column.** Each of these fields corresponds to a column in the file that you uploaded.    
 * **Workplace Analytics name.**  This is the name that will be used in the Workplace Analytics product. 
 * **Data type.**  This is the data type of the field. 
 * **Validity threshold.**  A source file might still be valid even if some rows have invalid or missing values for some columns. When you set the Validity threshold, you state the percentage of rows in the uploaded file that must have a valid, non-null value for this attribute. 

   <u>Example:</u> Your data file updates information about people. Because every row in it is linked to a user, the PersonID field must be valid in every row. In this case, set the value for PersonID to 100%. 

   The Validity threshold for required attributes is always 100%. If an attribute has a threshold lower than 100%, it cannot be required. For more information, see [Set Validity threshold for custom fields](#set-validity-threshold-for-custom-fields).
 * **Include in report.** Use this field to exclude sensitive data from the report that Workplace Analytics generates about the import operation.  
 * **Hash in report.** Use this field to obscure sensitive data. If you selecting this option, Workplace Analytics includes the data in the report that it generates about the import operation, but instead of displaying the actual value that was taken from the source file, it shows a hashed version of the value – a format that cannot be read. 

**To map fields**

After you complete the steps in [File upload](#file-upload), you are on the Upload page with the System fields table displayed.

1. <u>Map system fields:</u>

    <img src="../Images/upload2-map-sys-fields.png" alt="System fields table">
 
  <ol type="a"> 
  <li>Determine which of the columns in your .csv file correspond to the second column in the table (Workplace Analytics name).</li>
  <li>Under Source column (the first column in the table), click the down arrow. This displays a list of the column names that were found in the .csv file. From the list, select the correct column name for this data.</li> 
  <li>Fill in appropriate values for the other columns in the table: Workplace Analytics name, Data type, and so on. (For more information, see [Columns in the System fields and Custom fields tables](#columns-in-the-system-fields-and-custom-fields-tables).) Repeat these mapping steps for the rest of the required fields and for the optional fields that you choose to map.</li>
  </ol>

2. <u>Map custom fields:</u> 
Custom fields are optional: you need not map them all. Select the columns in your source (.csv) file that your organization considers important for the analysis that you want to perform. For example, if StartDate is important and your data contains this field, complete the row for StartDate. 

   <img src="../Images/upload3-map-custom2.png" alt="Custom fields table">
 
  <ol type="a">
  <li>Under Source column (the first column in the table), click the down arrow. This displays a list of the column names that were found in the .csv file. From the list, select the correct column name for this data – in this example, select **StartDate**.</li>
  <li>Set values for the other columns in the table: Select the data type, set a threshold percentage (see [Set Validity threshold for custom fields](#set-validity-threshold-for-custom-fields)), and select whether you want to hash the value in the report.</li>
  <li>Repeat these steps for the rest of the custom fields in your data that are important to your organization.</li>
  </ol>

3. In the Submit for validation area, select **I confirm that these mappings are correct** and click **Submit**. This uploads the .csv file and starts the validation process. 

Go to the next procedure, [Data validation](#data-validation).

## Data validation

After you complete the steps in [Field mapping](#field-mapping), the Upload page displays the _File is being uploaded_ screen:

<img src="../Images/upload4-uploading.png" alt="Upload in progress">
 
> [!Important]  
> Observe the warning “You must stay logged in while the file is uploading or the upload will be cancelled.” This is because the upload takes place via this page in your web browser. Do not close the browser (or this browser page). If you do close it, the upload will fail. 

## Validation succeeds

If validation succeeds, the Upload page indicates that validation succeeded, it shows the size of the upload, and it shows the overall process as complete:
 
<img src="../Images/upload6-validated.png" alt="Validation succeeded">

You can now click **Settings** and then click **Organizational data** to display the Data upload history page under Organizational data. On this page, click **Succeeded** to see the workflows that successfully validated (and uploaded). <!--  Note that this will work only work if you are on a native tenant. Demo is still on Volo. -->

On this page, you have the following options:
 * Click view details (the eye icon) to see a summary of the validation results.
 * Click the hierarchy symbol to see the mapping settings for the workflow. 
 * Click the download symbol to download the validated .csv file. 

> [!Note] 
> Each tenant can have only one upload in progress at a time. This means that you must complete the workflow of one data file – either guide it to a successful validation or abandon it – before you begin the workflow of the next data file. By looking at the Start – Mapping – Validation – Complete bar, you can tell whether any data file is in the upload workflow. 

## Validation fails

The following illustration shows a failed validation:

<img src="../Images/upload9-val-failed-upload-flow.png" alt="Validation failed">
 
After a failed validation, the Data load page shows the Validation failed notification. It also shows details about the validation attempt and it presents you with options.

Before you attempt to address the problem, consider clicking **Download issues**. This displays a log file that describes the problems in your data that can cause validation errors. Examine this file to decide what to do next: fix the source data, change your mapping settings, or abandon the current attempt. 

> [!Tip] 
> If you have a small number of errors, you’ll probably want to fix them. If you have many errors, you might want to choose **Abandon**. 

### Options upon failed validation

* <u>Abandon:</u> To restart the upload-map-validate process with new data rather than retrying the process with the current data, click **Abandon** (in the upper right corner of the page). Clicking Abandon does not retain any field mappings that you have made. 
* <u>Fix:</u> If you decide to fix the errors, you have two options: 
  * <u>Fix the source data.</u> Fixing the data in your source .csv file is recommended, because it will increase the quality of the WPA analysis.
  * <u>Change the mappings.</u> This is the right option if you originally had chosen an incorrect data type. You could also lower the Threshold, but making that change, while getting you past this step, could negatively affect future WPA analysis. Click **Edit mapping** to set new mapping values, after which you can retry to validate your data file. 
* <u>Upload file:</u> The difference between Upload file and Abandon is that your mappings are retained if you click Upload file. After you click **Upload file**, follow the steps in [File upload](#file-upload). 

## Tips

### Invalid values
When any row has an invalid value for any attribute, the entire upload will fail until the source file is fixed (or the mapping changes the validation type of the attribute in way that makes the value valid). Lowering a threshold does not ignore or skip an invalid value.

### Adding missing data
Workplace Analytics does not modify or fill in data that is missing from HR uploads, even for EffectiveDate or TimeZone. The administrator is responsible for correcting such errors or omissions. 

### Set Validity threshold for custom fields

The Threshold depends on the intended use of the custom field: If you intend to use this data in much of your analysis, you should pick a high value. You can pick a lower value if it applies, for example, to only a small subset of people in your organization. 

#### Set a high value

Generally, you should set the Threshold field to a high value. This is especially important if your analysis will focus on that field. 

For example, you might include a ManagerId attribute. You might at first not think that you’re analyzing manager behavior and you might be tempted to omit this attribute. But building the organization hierarchy is used implicitly by many Workplace Analytics analyses – for differentiating different work groups, for determining high- and low-quality meetings based on how many levels attend, and more.

#### Set a lower value

The goal of your analysis might be to determine sales effectiveness. Your data might include an attribute for sales attainment that only makes sense for members of your sales force, who constitute 10% of the company. This number doesn’t apply to engineers or documentation writers, so there is no way to fill it out for them, but it is critical for high-performers in sales.  
