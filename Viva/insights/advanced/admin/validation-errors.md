---
title: Validation errors
description: View errors and solutions for validation errors in the advanced insights app
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Validation errors

Here are validation errors you might encounter while uploading data to the advanced insights app. In most cases, you'll need to correct the errors and upload your file again. Review our [Prepare organizational data](./prepare-org-data.md) article to learn how to format and get your data ready for upload.

|Category|Related rule| Message|
|---|-----|---|
<a name="files-and-file-extensions"></a>File and file extensions|The data file needs to be in the .csv UTF-8 format, and it can’t be empty.|Your file is empty. Select another file and upload again.
|||This file has an invalid extension of '{0}'. Select a .csv file and upload again.
|||Invalid .csv format. Number of columns in row does not match number of columns in header. Please check for missing or misplaced commas and upload again.
|||Non-UTF-8 character found. Make sure your .csv file uses UTF-8 encoding and upload it again.
<a name="column headers"></a>Column headers|All field header or column names need to be unique.|Two or more column headers in your file are the same. Include unique headers for each column.
||All field header or column names need to contain a value.|Header is missing in column(s) {J}. Include the header name in your selected file and upload again.
||All field header or column names need to have no leading or trailing blank spaces or special characters (non-alphanumeric, such as @, #, %, &).|{Header name} contains unsupported special characters. Remove the special characters and upload again.
||All field header or column names need to contain no reserved keywords.|{header name} is a reserved keyword. Please rename {header name} so that it doesn't use a reserved keyword and upload the file again.
||After you upload your file, you can only map one column header to each Viva Insights data field.|Your file has more than one source column mapped to a data field. Make sure each source column is mapped to a unique field.
|Field values|Field values need to be provided in the correct data type. Refer to [Attribute reference](./prepare-org-data.md#attribute-reference).|Invalid {header name} value. {Header name} should be an email address following the form `employee@contoso.com`.
|||Invalid {header name} value. {Header name} should be a string.
|||Invalid {header name} value. {Header name} should be a date following the form MM/DD/YYYY.
|||Invalid {header name} value. {Header name} should be a double following the form 23.75.
|||Invalid {header name} value. {Header name} should be an integer.
||Required fields need to have a value for every row.|Missing {header name} column or {header name} value. {Header name} is a required field and needs a value for every row. Add {header name} value and upload the file again.
||Each PersonId needs to have a unique ManagerId.|Missing ManagerId value for new PersonId field. ManagerId is a required field. Add the corresponding ManagerId field and upload again.
|||Multiple ManagerIds detected for PersonId in row {row #4}. Each PersonId should have a unique ManagerId. Please fix this error and upload your file again.
||There can't be loops where: <ul><li>Managers and employees report to each other. <li>Managers report back to employees.<li>People report to themselves.|There is a loop in the manager hierarchy in which a manager reports back to an employee. The loop contains the PersonIds and ManagerIds found in rows {rows #3,4,5}. Please fix the loop and upload your file again.
|||This row contains a loop in the manager hierarchy in which managers and employees report to each other. The loop contains {X} people and starts with the PersonId in row {row #3}. Please fix the loop and upload your file again.
|||PersonId in row {row #5} reports to themselves (PersonId and ManagerId is the same). Please correct this loop in the manager hierarchy and upload your file again.
