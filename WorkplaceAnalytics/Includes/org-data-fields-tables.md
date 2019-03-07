---
# Metadata Sample
# required metadata

title: Descriptions of the custom fields table and columns in all of the fields tables
description: Information to help you map fields by using the fields tables.   
author: paul9955
ms.author: v-pascha
ms.date: 02/21/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

### Custom fields table

* **Custom fields** are displayed on this page below the optional fields. Custom fields are optional attributes you can create. Select a column from your source.csv file. Name the column, select the data type, set the [validity threshold](#set-validity-threshold-for-custom-fields), and then select the report option.

### Columns in the fields tables

* **Source column** corresponds to each of the fields in the uploaded file.
* **Workplace Analytics name** is the name of your organization's Workplace Analytics.

* **Data type** is the data type of the fields.

   >[!Note]
   >If the data type is Boolean, the value for the Boolean field must be TRUE or FALSE.

* **Validity threshold** sets the percentage of rows in the uploaded file that must have a valid, non-null value for the attribute. The source file might still be valid even if some rows have invalid or missing values for some columns.

   <b>Summary of Validity threshold settings</b>

   * **Required attributes.** Because PersonId and EffectiveDate are required attributes, their Validity threshold value is 100%. This value cannot be changed.

   * **Fields with minimum values.** The Validation threshold for the ManagerId, Organization, and LevelDesignation fields is set to 95% by default, but you can raise this value.

   * **Other system fields.** The Validation threshold for other system fields is set to 95% by default, but you can raise or lower this value.

   * **Custom fields.** See [Set Validity threshold for custom fields](#set-validity-threshold-for-custom-fields). 

* **Include in report** excludes sensitive data from the report that Workplace Analytics generates about the import operation.  

* **Hash in report** de-identifies sensitive data. If you select this option, Workplace Analytics includes the data in the report that it generates about the import operation, but instead of displaying the actual value that was taken from the source file, it shows a hashed version of the value – a format that cannot be read.