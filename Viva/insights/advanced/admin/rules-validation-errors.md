---
ms.date: 02/02/2024
title: File rules and validation errors
description: View errors and solutions for validation errors in the advanced insights app
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights
manager: anirudhbajaj
audience: Admin
---

# File rules and validation errors

In this article, we describe how your upload file needs to be formatted, and provide errors you might encounter while bringing data into the advanced insights app.

## File and field rules

When any data row or column has an invalid value for any attribute, the entire upload will fail until the source file is fixed (or the mapping changes the validation type of the attribute in a way that makes the value valid).

### Rules for the file

The data file needs to be in the .csv UTF-8 format, and it can’t be empty.

### Rules for source and target field headers

All source and target field header or column names need to: 

1. Only contain ASCII alphanumeric characters (letters and numbers, for example, **Date1**), or underscore (_). Special non-alphanumeric characters such as @, #, %, &, or other characters aren’t supported.
2. Contain a value.
3. Be unique. 

### Rules for custom target field headers

 All custom target field headers or column names need to:  
1. Have no leading, middle, or trailing blank spaces.  
2. Contain no system fields, which are: 
    * PeopleHistoricalId
    * StartDate
    * EndDate
    * Domain
    * PopulationType
    * TimeZone
    * StandardTimeZone
    * WorkdayStart
    * WorkDayEnd
    * WeekendDays
    * InferredTeamSize
    * ObjectId
    * IsActive
    * Starting with "Microsoft_"
    


Required fields need to have a value for every row.

After you upload your file, you can only map one column header to each Viva Insights data field.

### Rules for field values

Field values need to be provided in the correct data type. Refer to [Attribute reference](./prepare-org-data.md#attribute-reference).

#### Rules for characters in field values


* The character length of field values in rows can't exceed 128 KB, which is about 1024 x 128 characters.
* “New line” (\n) characters aren't permitted in field values.

>[!Note]
>You can use double-byte characters, such as Japanese characters, in the field values.

#### Rules for values in the ManagerId field

Each PersonId needs to have a unique ManagerId. In other words, there can't be multiple managers for one person.

There can't be loops where:

* Managers and employees report to each other.
* Managers report back to employees.

Let’s say Dylan is Kris’s manager. The organizational data couldn’t show:

* Kris reporting to Dylan and also Dylan reporting back to Kris.
* Dylan reporting to Kris.


Both of the following hierarchies would produce errors in end-user experiences:

:::image type="content" source="../images/admin-mgr-loops-1-a.png" alt-text="Screenshot that shows a manager hierarchy loop between three people.":::


### Example .csv export file

Here's an example snippet of a valid .csv export file:

``PersonId,EffectiveDate,HireDate,ManagerId,LevelDesignation,Organization,Layer,Area Emp1@contoso.com,12/1/2020,1/3/2014,Mgr1@contoso.com,Junior IC,Sales,8,Southeast Emp2@contoso.com,11/1/2020,1/3/2014,Mgr1@contoso.com,Junior IC,Sales,8,Southeast Emp3@contoso.com,12/1/2020,1/3/2014,Mgr2@contoso.com,Manager,Sales,7,Northeast Emp4@contoso.com,10/1/2020,8/15/2015,Mgr3@contoso.com,Support,Sales,9,Midwest Emp5@contoso.com,11/1/2020,8/15/2015,Mgr3@contoso.com,Support,Sales,9,Midwest Emp6@contoso.com,12/1/2020,8/15/2015,Mgr3@contoso.com,Support,Sales,9,Midwest``



## Validation errors

Here are validation errors you might encounter while uploading data to the advanced insights app. In most cases, you'll need to correct the errors and upload your file again. Review our [Prepare organizational data](./prepare-org-data.md) article to learn how to format and get your data ready for upload.

|Category|Related rule| Message|Applies to|
|---|-----|---|---|
File and file extensions|The data file needs to be in the .csv UTF-8 format, and it can’t be empty.|Your file is empty. Select another file and upload again.|.csv upload only
|||This file has an invalid extension of '{0}'. Select a .csv file and upload again.|.csv upload only
|||Invalid .csv format. Number of columns in row does not match number of columns in header. Please check for missing or misplaced commas and upload again.|All
|||Non-UTF-8 character found. Make sure your .csv file uses UTF-8 encoding and upload it again.|All
Column headers|All field header or column names need to be unique.|Two or more column headers in your file are the same. Include unique headers for each column.|All
||All field header or column names need to contain a value.|Header is missing in column(s) {J}. Include the header name in your selected file and upload again.|All
||All field header or column names need to only contain alphanumeric characters (letters and numbers, for example, **Date1**), or the following symbols: ~ ! @ # $ % ^ & * + > : < > [] ?. Other characters aren’t supported|{Header name} contains unsupported special characters. Remove the special characters and upload again.
||All field header or column names need to contain no system fields.|{header name} is a system field. Please rename {header name} so that it doesn't use a system field and upload the file again.|All
||After you upload your file, you can only map one column header to each Viva Insights data field.|Your file has more than one source column mapped to a data field. Make sure each source column is mapped to a unique field.|All
|Field values|Field values need to be provided in the correct data type. Refer to [Attribute reference](./prepare-org-data.md#attribute-reference).|Invalid {header name} value. {Header name} should be an email address following the form `employee@contoso.com`.|All
|||Invalid {header name} value. {Header name} should be a string.|All
|||Invalid {header name} value. {Header name} should be a date following the form MM/DD/YYYY.|All
|||Invalid {header name} value. {Header name} should be a double following the form 23.75.|All
|||Invalid {header name} value. {Header name} should be an integer.|All
||Required fields need to have a value for every row.|Missing {header name} column or {header name} value. {Header name} is a required field and needs a value for every row. Add {header name} value and upload the file again.|All
|||Missing ManagerId value for new PersonId field. ManagerId is a required field. Add the corresponding ManagerId field and upload again.|All
||Each PersonId needs to have a unique ManagerId.|   |All
||There can't be [loops](#rules-for-values-in-the-managerid-field) where: <ul><li>Managers and employees report to each other. <li>Managers report back to employees.|   |All
