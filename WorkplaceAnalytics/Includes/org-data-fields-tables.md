---

title: Descriptions of the custom fields table and columns in all of the fields tables
description: Information to help you map fields by using the fields tables.   
author: paul9955
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

### Custom fields table

* **Custom fields** are displayed on this page below the optional fields. Custom fields are optional attributes you can create. Select a column from your source.csv file. Name the column, select the data type, set the [validity threshold](#set-validity-threshold-for-custom-fields), and then select the report option.

### Field column details

* **Source column** corresponds to each of the fields in the uploaded file.
* **Workplace Analytics name** is the name of your organization's Workplace Analytics.

* **Data type** is the data type of the fields.

   >[!Note]
   >If the data type is Boolean, the value for the Boolean field must be TRUE or FALSE.

* **Validity threshold** sets the percentage of rows in the uploaded file that must have non-null values (no blanks) for the attribute. The source file might still be valid even if some rows have missing values for some columns. This setting is not intended to check or allow invalid values. A single invalid value, such as an incorrect data type, email address, or TimeZone string will cause the file upload to fail.

   <b>Summary of Validity threshold settings</b>

   * **Required attributes:** Because PersonId and EffectiveDate are required attributes, their Validity threshold value is 100%. This value cannot be changed.

   * **Fields with minimum values:** The Validation threshold for the ManagerId, Organization, and LevelDesignation fields is set to 95% by default, but you can increase this value.

   * **Other system fields:** The Validation threshold for other system fields is set to 95% by default, but you can increase or decrease this value.

   * **Custom fields:** See [Set Validity threshold for custom fields](#set-validity-threshold-for-custom-fields).

* **Include in report** lets you decide how to treat sensitive data in the report that will be generated about the import operation.

    ![Map data fields](../images/wpa/setup/map-fields-include-column-65.png) 

The drop-down menu under **Include in report** offers the following options for each of the columns in your source data:

   * **Show in report:** Let the actual data value display in the report just as it was imported in the organizational data file.

   * **Exclude from report:** Prevent the data value from appearing in the report. For data-privacy reasons, some attributes (such as ManagerID) are automatically assigned the value "Exclude from report" and this value cannot be changed. 

   * **Hash in report** de-identifies sensitive data. This option includes the data in the report that it generates about the import operation, but instead of displaying the actual value that was taken from the source file, it shows a hashed version of the value – a format that cannot be read.
