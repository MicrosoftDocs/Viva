---

ROBOTS: NOINDEX,NOFOLLOW
ms.date: 08/29/2019
title: Format data for uploading in Viva Insights 
description: How to format .xlsx files and .csv files for uploading in Microsoft Viva Insights  
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Format organizational data for upload

Microsoft Viva Insights admins upload files that contain organizational (HR) data as part of setup and as a regular data-refresh task.

<!-- THIS IS THE HEADER AND INTRO PARAGRAPH TO USE WHEN THIS TOPIC APPLIES TO UPLOAD OF ALL/VARIOUS DATA TO WPA. 
FOR NOW (AUGUST 2019), MENTION ONLY ORG DATA. 

# Format data for upload

Various setup and usage tasks require admins to upload data to Viva Insights. Admins can upload files that contain organizational (HR) data as part of setup or as a regular data-refresh task. Analysts can upload files that specify groups of employees when they define queries of particular types. 
END OF EVENTUAL HEADER & INTRO PARAGRAPH
-->

For these uploads, you can choose from among two file formats. The following sections describe how to format these files so that Viva Insights can parse and use their data.

* [Format .xlsx files](#format-xlsx-files)
* [Format UTF-8 encoded .csv files](#format-utf-8-encoded-csv-files)

### Which format to use

**Recommended: Use the .xlsx format** because it is usually easier to use. But for some cases, you could use either format, if it complies with the following:

1. **Use .xlsx if outside of the United States** - Files in the UTF-8 encoded .csv format are subject to United-States data formatting, so if your organization is based outside of the United States and uses non-U.S. formatting for dates, times, or numbers, use the .xlsx format.
2. **Encode .csv files properly** - Only choose the .csv-file option if you can format it as required: UTF-8 encoded, and with all data (dates, times, numbers) in United-States format. Files in the .xlsx format do not have these restrictions.
3. **Stay under the size limit** - The upper limit of .xlsx files for upload is 1.0 GB. If your upload file is larger than 1.0 GB, use the .csv format instead.

>[!Note]
>
>* For more information about selecting and arranging the _contents_ of these files (as opposed to adhering to their _formatting_ rules), see [Prepare organizational data](/viva/insights/setup/prepare-organizational-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).
>* If you've uploaded data by using one file format and would like to upload data in a different file format in the future, you can do so, as long as you format the data according to the rules in the following sections.

<!-- PER PRAMOD (23 AUGUST 2019) REMOVE THIS. "For now, CRM will continue to support upload only through CSV."
> * CRM data: [Prepare the CRM source data](crm-data-upload.md#prepare-the-crm-source-data)
-->
<!-- 
> * Upload groups for use in Plans: [Use a .csv file](../tutorials/solutions-conceptual.md#use-a-csv-file)  **[This link is a placeholder for now. This section will need to be rewritten.]**
-->

## Format .xlsx files

Viva Insights can accept organizational data in .xlsx files produced by Microsoft Excel or by other spreadsheet applications.

### Rules for .xlsx files

Acceptable .xlsx files must adhere to the following:  

* **File extension** - Must be _.xlsx_. It cannot be any other extension (such as .xls, .xlsb, or .xlsm) that is supported by Microsoft Excel or another spreadsheet application.
* **Size limit** - The limit is 1.0 GB for .xlsx upload files. If your upload file is larger than 1.0 GB, use the .csv format instead.  
* **No formulas or macros** - None can be in cells in the .xlsx file.  
* **No special objects** - Do not include charts, images, pivot tables, or other such entities in the file.
* **Accepted number and date formats** - While .csv files require U.S. delimiter and date format, this restriction does _not_ apply to .xslx files. You can use the formats for other locales in .xlsx files. For more information, see [Apply the correct data type](#apply-the-correct-data-type).
* **Internal structure** - See [Structure an .xlsx file](#structure-an-xlsx-file) to learn how to structure the columns and rows in an .xlsx file for a successful upload.

### Structure an .xlsx file

#### Sheets

* **First sheet only** - Viva Insights will read only the first sheet of the .xlsx file. You can have data on other sheets, but it will be ignored. To confirm which sheet is the first sheet, open the file in Excel and locate the tab farthest to the left.

  In the following example, only the data in the sheet labeled "DataSheet" will be used:

   ![First data sheet only.](../images/wpa/setup/first-sheet-only.png)

#### Columns and rows

* **The first row contains column headers only** - In the first sheet, the values in the first row are considered to be column headers.

   Column headers in an .xlsx file are used the same as column headers in a .csv file. You use them on the [Mapping](/viva/insights/setup/upload-organizational-data-1st?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#field-mapping) page of the organizational-data upload sequence to identify columns. The names they are given on that page can later be used by analysts when they build [queries](/viva/insights/tutorials/query-basics?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

* **No duplicate column headers** - Every column header must be unique.
* **No blank or repetitive cells** - Viva Insights checks all cells in the first row to verify that there are no blank cells and no repetitions.
* **Strings only in column headers** - Column headers must be strings. In Microsoft Excel, use either the _General_ or _Text_ formatting option. To format a cell, see [Apply the correct data type](#apply-the-correct-data-type).
* **Only _column span_ data is used** - The _column span_ is the set of contiguous columns in the worksheet that starts with column A and ends with the final column that has a header. In the column-header row, between the first and the last column (inclusive), every cell must contain data and be unique.

  **Example 1:** In this example, the columns span A through H:

   ![Column span A.](../images/wpa/setup/column-span-simple.png)

   **Example 2:** In this example, the column-header cell G1 is missing:

   ![Column span G1.](../images/wpa/setup/column-span-simple-w-blank.png)

   In this case, the column span still consists of columns A through H because cell H1 is the last non-blank cell in the first row. However, cell G1 is reported as having an error ("blank header value").

   **Example 3:** In this example, the values in cells J3 and J4 are ignored because they lie outside the column span. (The column span extends only to column H, so any data in the columns after H is ignored.)

   ![Column span J3 and J4.](../images/wpa/setup/column-span.png)

* **How _row-span_ data is used** - After Viva Insights calculates the column span, it calculates the _row span_. These calculations are ordered because the row span can be determined only after the column span is known.  

  The row span is the set of rows in the worksheet that starts with row 2 (the first row after the column header row) and extends to the last row (the row numbered the highest) that contains data in columns within the column span.

   **Example 4:** In this example, the row spans from 2 through 11:

   ![Row span 2 through 11.](../images/wpa/setup/row-span.png)

  Viva Insights considers the rows in this example as follows:

  * Rows 2, 3, and 4 are valid rows.
  * Rows 5 through 10 are empty rows.
  * Row 11 is considered "partially filled." The data in partially filled rows is read, parsed, checked for validation errors, and potentially used.

* **Combining _column span_ and _row span_** - After the column span and the row span are determined, Viva Insights validated the data in the rectangle of cells defined by the column and the row spans (including the column-header row). In the preceding examples, this rectangle extends from cells A1 through H11.

#### Data

Each cell of data in the .xlsx file must be formatted correctly, starting with the column-header row and continuing with the remaining rows, which contain field values:

##### Format the column-header row

All field header or column names must adhere to the following:

| Guideline | Notes or example |
| --------- | ---------------- |
| Column headers must be strings | In Microsoft Excel, use either the _General_ or _Text_ formatting option. To format a cell, see [Apply the correct data type](#apply-the-correct-data-type). |
| Begin with a letter, not a number | Example: _Date1_ |
| Contain only alphanumeric characters | Use letters and numbers only. <br>Example: _Date1_ |
| Contain no special characters | Do not use non-alphanumeric characters such as _@, #, %, &, *_ |
| Contain at least one lower-case letter | Example: _Hrbp_ <br>All uppercase does not work: <strike>HRBP</strike> |
| Contain no spaces | Example: _Date1_ |
| Adhere to the requirements for Viva Insights [required attributes](/viva/insights/setup/prepare-organizational-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#required-attributes) and [reserved optional attributes](/viva/insights/setup/prepare-organizational-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#reserved-optional-attributes), including for case sensitivity | For example, for the attributes _PersonId_ and _HireDate_ |

##### Format the field-value rows

To help ensure that Viva Insights can successfully validate the data in your upload file:  

1. Make sure that your data uses only [valid values and formats](#use-only-valid-values-and-formats).

2. Learn what [data types are required](#required-data-types) for the data in your upload file and then [apply the correct data type](#apply-the-correct-data-type) to the cells in your upload file.

##### Use only valid values and formats

When any data row or column has an invalid value for any attribute, the entire upload will fail until the source file is fixed (or the [mapping](/viva/insights/setup/upload-organizational-data-1st?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#field-mapping) changes the validation type of the attribute in a way that makes the cell valid).

The field values in the data rows must comply with the following rules:

* Each field can contain a maximum of 128 KB of data.
* The required **EffectiveDate** and **HireDate** field values must have the Date datatype. (To apply a data type, see [Apply the correct data type](#apply-the-correct-data-type).)
* The required **PersonId** and **ManagerId** field values must be valid email addresses (for example, gc@contoso.com).
* The required **Layer** field values and **HourlyRate** field values must contain numbers only.

>[!Note]
>Viva Insights does not currently perform currency conversions for HourlyRate data. All calculations and data analysis in Viva Insights assume the data to be in U.S. dollars.

The field values also cannot contain any of the following:

* No accent marks (á)
* No tildes (~)
* No short or long dashes (-, --)
* No commas (,)
* No "new line" characters (\n)
* No double (" ") or single quotes (‘ ‘)

##### Required data types

In a later step, you [map](/viva/insights/setup/upload-organizational-data-1st?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#field-mapping) data in columns to Viva Insights data types. Several attributes that you map in this step are required attributes. They expect particular data formats.

To be able to map data successfully, use the data specified in the following table. Apply these data types by using the steps in [Apply the correct data type](#apply-the-correct-data-type).

| Viva Insights data type | Format as this data type in Excel&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Notes |
| ----- | ----- | ----- |
| Email |  General | This data type is the default option so no special formatting is necessary. |
| Timezone | General | This data type is the default option so no special formatting is necessary. Every Timezone string must be one of the values specified in [Time zones for Viva Insights](/viva/insights/use/timezones-for-workplace-analytics?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json). |
| Boolean | General  | This data type is the default option so no special formatting is necessary. The data value can only be **TRUE** or **FALSE**|
| DateTime |Date | |
| Double |Number | |
| Integer |  Number | Do not include a decimal component. For example, "2.35" is not accepted, but "2" and "-2" are accepted. |
| String | General |  This data type is the default option so no special formatting is necessary. The "Text" data type is also acceptable. |
  
##### Apply the correct data type

Use the capabilities of Microsoft Excel to apply a data type to the cells in your file. Every cell, whether it contains a date, a number, or text, must be correctly formatted to the data type of your choice.

Use only the predefined formats that Excel offers. Do not use custom formats. To guarantee that you've selected a predefined format, follow these steps:

**To apply a data type in Microsoft Excel**

All of the data cells in a column must have the same data type, even if they do not have the same exact format. For example, Viva Insights will correctly parse a column that includes some cells with dd/mm/yyyy format and others with mm/dd/yyyy format as long as they all have the **Date** data type.

In this example, we're formatting cells that contains dates:

1. Select one or more cells in a column that you want to format.

   ![Save .csv file.](../images/wpa/setup/format-date-cell.png)

2. Right-click the selection (of one or more cells) and select **Format Cells**.
3. In the **Format Cells** dialog box, under **Category**, select **Date**.
4. Under **Type**, select a type. The selected cells will change to the new formatting style. If the cells do not change, go back to step 3 and make sure that you select a predefined Excel style.

   >[!Note]
   >Watch the cell carefully as you apply a data type to it. You can be sure that its data type has changed only if its appearance also changes&mdash;that is, if Excel changes it to display the type that you selected.

5. After you have finished formatting the data, save the worksheet with the extension .xlsx:

   1. In Excel, point to **File** and select **Save As**.
   2. Type a name for the file, choose the file type **Excel Workbook (*.xlsx)**, and select **Save**:

   ![Save as UTF-8 .csv file.](../images/wpa/setup/save-as-xlsx.png)

6. Save the location of this new file for later use.

## Format UTF-8 encoded .csv files

### Rules for .csv files

* **UTF-8** - Data files in .csv format must be in UTF-8 format.
* **Accepted date format** - All dates must be in the mm/dd/yyyy format.
* **Accepted number format** - Numerical fields (such as "HourlyRate") must be in the U.S. "number" format and cannot contain commas or currency designations (such as the dollar sign). Example: Use **8.75**, not **8,75**.
* **Column delimiters** - In every row, use commas to separate values.

### Use only valid values and formats

When any data row or column has an invalid value for any attribute, the entire upload will fail until the source file is fixed (or the mapping changes the validation type of the attribute in a way that makes the value valid).

All field header or column names must:

* Begin with a letter (not a number)
* Only contain alphanumeric characters (letters and numbers, for example Date1)
* Have at least one lower-case letter (Hrbp); all uppercase won’t work (HRBP)
* Have no spaces (Date1)
* Have no special characters (non-alphanumeric, such as @, #, %, &, *)
* Match exactly as listed for Viva Insights’ Required and Reserved optional attributes, including for case sensitivity (for example PersonId and HireDate)

The field values in the data rows must comply with the following rules:

* Each field can contain a maximum of 128KB of data.
* The required **EffectiveDate** and **HireDate** field values must be in the MM/DD/YYYY format.
* The required **PersonId** and **ManagerId** field values must be valid email addresses (for example, gc@contoso.com).
* The required **Layer** field values and **HourlyRate** field values must contain numbers only.

>[!Note]
> Viva Insights does not currently perform currency conversions for HourlyRate data. All calculations and data analysis in Viva Insights assume the data to be in U.S. dollars.

The field values also cannot contain any of the following characters:

* accent marks (á)
* tildes (~)
* short or long dashes (-, --)
* commas (,)
* "new line" characters (\n)
* double (" ") or single quotes (‘ ‘)

### Create a valid UTF-8 encoded .csv file in Microsoft Excel

1. Export organizational data from your HR database.
2. Open Excel and import the exported organizational data.
3. In Excel, organize the data:

   1. Place all of the data on a single worksheet.
   2. In the worksheet, the first row must contain column headers. Every column must have a column header. To know what columns (what data) to include, see [Prepare organizational data](/viva/insights/setup/prepare-organizational-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).
   3. All rows below row 1 must contain data about employees. Include one row of data per person, per EffectiveDate.

   >[!Note]
   >Each column represents an attribute. Many attributes are optional, but a few attributes (such as **PersonID**) are required. For details, see [Structure the organizational data](/viva/insights/setup/prepare-organizational-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#structure-the-organizational-data).

4. Save the worksheet into a single, flat, text file.

   1. In Excel, point to **File** and select **Save As**.
   2. Type a name for the file, choose the file type **CSV UTF-8 (Comma delimited) (*.csv)**, and select **Save**:

   ![Save as UTF-8 .csv file option.](../images/wpa/setup/csv-utf-8.png)

5. Save the location of this new .csv file for later use.

>[!Note]
>If your spreadsheet application does not offer **CSV UTF-8 (Comma delimited) (*.csv)** as a file-type choice (for example, versions of Excel older than Excel 2016), you'll need to use another program, such as Notepad++, to save this file as comma-delimited UTF-8.

### Example .csv data file

Here's an example snippet of a valid .csv data file:

PersonId,EffectiveDate,HireDate,ManagerId,TimeZone,LevelDesignation,Organization,Layer,Area
Emp1@contoso.com,10/1/2020,1/3/2014,Mgr1@contoso.com,Pacific Standard Time,5,Sales,8,Southeast
Emp2@contoso.com,11/1/2020,1/3/2014,Mgr1@contoso.com,Pacific Standard Time,5,Sales,8,Southeast
Emp3@contoso.com,12/1/2020,1/3/2014,Mgr2@contoso.com,Pacific Standard Time,4,Sales,7,Northeast
Emp4@contoso.com,10/1/2020,8/15/2015,Mgr3@contoso.com,Pacific Standard Time,6,Sales,9,Midwest
Emp5@contoso.com,11/1/2020,8/15/2015,Mgr3@contoso.com,Pacific Standard Time,6,Sales,9,Midwest
Emp6@contoso.com,12/1/2020,8/15/2015,Mgr3@contoso.com,Pacific Standard Time,6,Sales,9,Midwest  

## Subsequent steps

* **Role:** admin

After you have populated and formatted your organizational data file, you can continue with the following intake steps. This section provides an overview only. To see the complete procedures, select the links in these steps:

1. [File upload](/viva/insights/setup/upload-organizational-data-1st?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#file-upload).
2. [Field mapping](/viva/insights/setup/upload-organizational-data-1st?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#field-mapping). After the data file is uploaded, you will encounter the mapping screen, where you map the source columns in the data file to Viva Insights names and select a data type.
3. After you have confirmed the field mapping, [data validation](/viva/insights/setup/upload-organizational-data-1st?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#data-validation) starts.
4. When validation finishes, it reports [success](/viva/insights/setup/upload-organizational-data-1st?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#validation-succeeds) or [failure](/viva/insights/setup/upload-organizational-data-1st?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#validation-fails). In case of errors, validation logs are made available.

   Validation errors can be caused by:

   * Cells with invalid formatting, see [Rules for .xlsx files](#rules-for-xlsx-files) and [Rules for .csv files](#rules-for-csv-files)
   * Missing entries (empty or blank cells), see [Set validity threshold for custom fields](/viva/insights/setup/upload-organizational-data2?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#set-validity-threshold-for-custom-fields)
   * Invalid use of special characters in column headers or in data rows, see [Use only valid values and formats](#use-only-valid-values-and-formats)

   If validation fails:

   * If this is your first upload of organizational data, see [Validation fails](/viva/insights/setup/upload-organizational-data-1st?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#validation-fails) for details.
   * If this is a subsequent upload of organizational data, see [Validation fails](/viva/insights/setup/upload-organizational-data2?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#validation-fails) for details.
  
   > [!Note]
   > If this is a subsequent upload of organizational data, another factor that can play a role in validation is the _validity threshold_. For more information, see [Field column details](/viva/insights/setup/upload-organizational-data2?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#field-column-details) and [Set validity threshold for custom fields](/viva/insights/setup/upload-organizational-data2?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#set-validity-threshold-for-custom-fields).

<!-- NOTE FROM PRAMOD:
Specific instructions to create, debug & fix (in case of validation errors) should be separate for CSV & XSLX files. We should have a separate page for each. We should link to these pages as required in the Prepare organizational data, Upload org data (First upload), Upload org data (subsequent uploads) pages.
-->

## Related topic

[Prepare organizational data](/viva/insights/setup/prepare-organizational-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)

