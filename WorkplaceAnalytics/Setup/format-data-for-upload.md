---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Format data for upload to Workplace Analytics
description: How to format .xlsx files and .csv files for upload to Workplace Analytics 
author: paul9955
ms.author: v-pascha
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Format organizational data for upload

Workplace Analytics admins upload files that contain organizational (HR) data as part of setup and as a regular data-refresh task.  

<!-- THIS IS THE HEADER AND INTRO PARAGRAPH TO USE WHEN THIS TOPIC APPLIES TO UPLOAD OF ALL/VARIOUS DATA TO WPA. 
FOR NOW (AUGUST 2019), MENTION ONLY ORG DATA. 

# Format data for upload

Various setup and usage tasks require admins to upload data to Workplace Analytics. Admins can upload files that contain organizational (HR) data as part of setup or as a regular data-refresh task. Analysts can upload files that specify groups of employees when they define queries of particular types. 
END OF EVENTUAL HEADER & INTRO PARAGRAPH
-->

For these uploads, you can choose from among two file formats. The following sections describe how to format these files so that Workplace Analytics can parse and use their data. 

 * [Format .xlsx files](#format-xlsx-files)
 * [Format UTF-8 encoded .csv files](#format-utf-8-encoded-csv-files)


### Which format to use?

**Recommended: Use the .xlsx format.** We recommend this format because it is usually easier to use. But in many cases, you could use either format, provided that you heed their restrictions: 

1. **Use .xlsx if outside of the United States.** Files in the UTF-8 encoded .csv format are subject to United-States data formatting, so if your organization is based outside of the United States and uses non-U.S. formatting for dates, times, or numbers, use the .xlsx format. 
2. **Encode .csv files properly.** Only choose the .csv-file option if you can format it as required: UTF-8 encoded, and with all data (dates, times, numbers) in United-States format. Files in the .xlsx format do not have these restrictions.
3. **Stay under the size limit.** The upper limit of .xlsx files for upload is 1.0 GB. If your upload file is larger than 1.0 GB, use the .csv format instead.

> [!Note] 
> * For more information about selecting and arranging the _contents_ of these files (as opposed to adhering to their _formatting_ rules), see  [Prepare organizational data](prepare-organizational-data.md). 
> * If you've uploaded data by using one file format and would like to upload data in a different file format in the future, you can do so, as long as you format the data according to the rules in the following sections. 

<!-- PER PRAMOD (23 AUGUST 2019) REMOVE THIS. "For now, CRM will continue to support upload only through CSV."
> * CRM data: [Prepare the CRM source data](crm-data-upload.md#prepare-the-crm-source-data)
-->
<!-- 
> * Upload groups for use in solutions: [Use a .csv file](../tutorials/solutions-conceptual.md#use-a-csv-file)  **[This link is a placeholder for now. This section will need to be rewritten.]**
-->

## Format .xlsx files 

Workplace Analytics can accept organizational data in .xlsx files produced by Microsoft Excel or by other spreadsheet applications. 

### Rules for .xlsx files

Acceptable .xlsx files must adhere to the following:  

 * **File extension.** The extension must be _.xlsx_. It cannot be any other extension (such as .xls, .xlsb, or .xlsm) that is supported by Microsoft Excel or another spreadsheet application.
 * **Size limit.** The upper limit of .xlsx files for upload is 1.0 GB. If your upload file is larger than 1.0 GB, use the .csv format instead. 
 * **No formulas or macros.** Include no formulas or macros in cells in the .xlsx file.
* **No special objects.** Do not include charts, images, pivot tables, or other such entities in the file.
 * **Accepted number and date formats.** While .csv files require U.S. delimiter and date format, this restriction does _not_ apply to .xslx files. You can use the formats for other locales in .xlsx files. For more information, see [Apply the correct data type](#apply-the-correct-data-type).
 * **Internal structure.** See the following section, [Structure an .xlsx file](#structure-an-xlsx-file) to learn how to structure the columns and rows in an .xlsx file for successful upload.

 ### Structure an .xlsx file

 #### Sheets

 * **First sheet only.** Workplace Analytics will read only the first sheet of the .xlsx file. You can have data on other sheets, but it will be ignored. To confirm which sheet is the first sheet, open the file in Excel and locate the tab farthest to the left. 

   In the following example, only the data in the sheet labeled "DataSheet" will be used:

   ![First data sheet only](../images/wpa/setup/first-sheet-only.png)

 #### Columns and rows

 * **The first row contains column headers only.** In the first sheet, the values in the first row are considered to be column headers. 
 
    Column headers in an .xlsx file are used the same as column headers in a .csv file. You use them on the [Mapping](upload-organizational-data-1st.md#field-mapping) page of the organizational-data upload sequence to identify columns. 
   
   The names they are given on that page can later be used by analysts when they build [queries](../tutorials/query-basics.md). 

 * **No duplicate column headers.** Every column header must be unique. 
 * **No blank or repetitive cells.** Workplace Analytics checks all cells in the first row to verify that there are no blank cells and no repetitions.
 * **Strings only in column headers.** Column headers must be strings. In Microsoft Excel, use either the _General_ or _Text_ formatting option. To format a cell, see [Apply the correct data type](#apply-the-correct-data-type).
 * **Only _column span_ data is used.** The _column span_ is the set of contiguous columns in the worksheet that starts with column A and ends with the final column that has a header. In the column-header row, between the first and the last column (inclusive), every cell must contain data and be unique. 
 
   **Example 1:** In this example, the column span is columns A through H: 
   
   ![Column span](../images/wpa/setup/column-span-simple.png)

   **Example 2:** In this example, the column-header cell G1 is missing: 

   ![Column span](../images/wpa/setup/column-span-simple-w-blank.png)

   In this case, the column span still consists of columns A through H because cell H1 is the last non-blank cell in the first row. However, cell G1 is reported as having an error ("blank header value").

   **Example 3:** In this example, the values in cells J3 and J4 are ignored because they lie outside the column span. (The column span extends only to column H, so any data in columns beyond H is ignored.)

   ![Column span](../images/wpa/setup/column-span.png)

* **How _row-span_ data is used.** After Workplace Analytics calculates the column span, it calculates the _row span_. It does these calculations in this order because the row span can be determined only after the column span is known.  
 
  The row span is the set of rows in the worksheet that starts with row 2 (the first row after the column header row) and extends to the last row (the row numbered the highest) that contains data in columns within the column span. 

   **Example 4:** In this example, the row span is rows 2 through 11: 

   ![Row span](../images/wpa/setup/row-span.png)

   Workplace Analytics considers the rows in this example as follows:
    * Rows 2, 3, and 4 are valid rows. 
    * Rows 5 through 10 are empty rows.
    * Row 11 is considered "partially filled." The data in partially filled rows is read, parsed, checked for validation errors, and potentially used.

* **Combining _column span_ and _row span_.** After the column span and the row span are determined, Workplace Analytics begins to validate the data in the rectangle of cells defined by the column span and the row span (including the column-header row). In the preceding examples, this rectangle extends from cell A1 to cell H11. 

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
| Adhere to the requirements for Workplace Analytics [required attributes and reserved-optional attributes](prepare-organizational-data.md#required-reserved-optional-and-custom-attributes), including for case sensitivity | For example, for the attributes _PersonId_ and _HireDate_ |

##### Format the field-value rows

To help ensure that Workplace Analytics can successfully validate the data in your upload file, follow these steps:  

1. Make sure that your data uses only [valid values and formats](#use-only-valid-values-and-formats). 

2. Learn what [data types are required](#required-data-types) for the data in your upload file and then [apply the correct data type](#apply-the-correct-data-type) to the cells in your upload file. 

##### Use only valid values and formats

When any data row or column has an invalid value for any attribute, the entire upload will fail until the source file is fixed (or the [mapping](upload-organizational-data-1st.md#field-mapping) changes the validation type of the attribute in a way that makes the cell valid). 

The field values in the data rows must comply with the following rules:

* Each field can contain a maximum of 128KB of data. 
* The required **EffectiveDate** and **HireDate** field values must have the Date datatype. (To apply a data type, see [Apply the correct data type](#apply-the-correct-data-type).)
* The required **PersonId** and **ManagerId** field values must be valid email addresses (for example, gc@contoso.com). 
* The required **Layer** field values and **HourlyRate** field values must contain numbers only.

>[!Note]
> Workplace Analytics does not currently perform currency conversions for HourlyRate data. All calculations and data analysis in Workplace Analytics assume the data to be in U.S. dollars.

The field values also cannot contain any of the following:

* No accent marks (á)
* No tildes (~)
* No short or long dashes (-, --)
* No commas (,)
* No "new line" characters (\n)
* No double (" ") or single quotes (‘ ‘)

##### Required data types

In a later step, you [map](upload-organizational-data-1st.md#field-mapping) data in columns to Workplace Analytics data types. Several attributes that you map in this step are required attributes. They expect particular data formats.

To be able to map data successfully, use the data specified in the following table. Apply these data types by using the steps in [Apply the correct data type](#apply-the-correct-data-type).

| 	Workplace Analytics data type	| 	Format as this data type in Excel&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;	| 	Notes	|  
| 	-----	| 	-----	| 	-----	| 
| 	Email	| 	General 	| 	This data type is the default option so no special formatting is necessary. 	| 
| 	Timezone	| 	General 	| 	This data type is the default option so no special formatting is necessary. Every Timezone string must be one of the values specified in [Time zones for Workplace Analytics](../use/timezones-for-workplace-analytics.md). 	| 
| 	Boolean	| 	General 	| 	This data type is the default option so no special formatting is necessary. The data value can only be **TRUE** or **FALSE**	| 
| 	DateTime	| 	Date	| 		| 
| 	Double	| 	Number	| 		| 
| 	Integer	| 	Number	| 	Do not include a decimal component. For example, "2.35" is not accepted, but "2" and "-2" are accepted. 	| 
| 	String	| 	General 	| 	This data type is the default option so no special formatting is necessary. The "Text" data type is also acceptable.	|
  
##### Apply the correct data type

Use the capabilities of Microsoft Excel to apply a data type to the cells in your file. Every cell, whether it contains a date, a number, or text, must be correctly formatted to the data type of your choice. 

Use only the predefined formats that Excel offers. Do not use custom formats. To guarantee that you've selected a predefined format, follow these steps:

**To apply a data type in Microsoft Excel**

All of the data cells in a column must have the same data type, even if they do not have the same exact format. For example, Workplace Analytics will correctly parse a column that includes some cells with dd/mm/yyyy format and others with mm/dd/yyyy format as long as they all have the **Date** data type. 

In this example, we're formatting cells that contains dates:

1. Select one or more cells in a column that you want to format. 

   ![Save .csv file](../images/wpa/setup/format-date-cell.png)

2. Right-click the selection (of one or more cells) and select **Format Cells**.   

3. In the **Format Cells** dialog box, under **Category**, select **Date**.

4. Under **Type**, select a type. The selected cells will change to the new formatting style. If the cells do not change, go back to step 3 and make sure that you select a predefined Excel style.

   > [!Note] 
   > Watch the cell carefully as you apply a data type to it. You can be sure that its data type has changed only if its appearance also changes&mdash;that is, if Excel changes it to display the type that you selected.

5. After you have finished formatting the data, save the worksheet with the extension .xlsx:

   a. In Excel, point to **File** and select **Save As**.
   
   b. Type a name for the file, choose the file type **Excel Workbook (*.xlsx)**, and select **Save**:

   ![Save as UTF-8 .csv file](../images/wpa/setup/save-as-xlsx.png)
 
   Note the location of this file, for later use.  

## Format UTF-8 encoded .csv files

### Rules for .csv files

 * **UTF-8** Data files in .csv format must be in UTF-8 format.
 > * **Accepted date format.** All dates must be in the mm/dd/yyyy format.
 > * **Accepted number format.** Numerical fields (such as "HourlyRate") must be in the U.S. "number" format and cannot contain commas or currency designations (such as the dollar sign). Example: Use **8.75**, not **8,75**. 
 >  * **Column delimiters.**  In every row, use commas to separate values. 

### Use only valid values and formats

When any data row or column has an invalid value for any attribute, the entire upload will fail until the source file is fixed (or the mapping changes the validation type of the attribute in a way that makes the value valid). 

All field header or column names must:

* Begin with a letter (not a number)
* Only contain alphanumeric characters (letters and numbers, for example Date1)
* Have at least one lower-case letter (Hrbp); all uppercase won’t work (HRBP)
* Have no spaces (Date1)
* Have no special characters (non-alphanumeric, such as @, #, %, &, *)
* Match exactly as listed for Workplace Analytics’ Required and Reserved optional attributes, including for case sensitivity (for example PersonId and HireDate)

The field values in the data rows must comply with the following rules:

* Each field can contain a maximum of 128KB of data. 
* The required **EffectiveDate** and **HireDate** field values must be in the MM/DD/YYYY format.
* The required **PersonId** and **ManagerId** field values must be valid email addresses (for example, gc@contoso.com). 
* The required **Layer** field values and **HourlyRate** field values must contain numbers only.

>[!Note]
> Workplace Analytics does not currently perform currency conversions for HourlyRate data. All calculations and data analysis in Workplace Analytics assume the data to be in U.S. dollars.

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

   a. Place all of the data on a single worksheet. 

   b. In the worksheet, the first row must contain column headers. Every column must have a column header. To know what columns (what data) to include, see [Prepare orgazational data](prepare-organizational-data.md).

   > [!Note] 
   > Each column represents an attribute. Many attributes are optional, but a few attributes (such as **EffectiveDate**) are required. (For more information, see [Structure the organizational data](prepare-organizational-data.md#structure-the-organizational-data).) 

   c. All rows below row 1 must contain data about employees. Include one row of data per person, per EffectiveDate. 

4. Save the worksheet into a single, flat, text file.

   a. In Excel, point to **File** and select **Save As**.
   
   b. Type a name for the file, choose the file type **CSV UTF-8 (Comma delimited) (*.csv)**, and select **Save**:

   ![Save as UTF-8 .csv file](../images/wpa/setup/csv-utf-8.png)
 
   Note the location of this file, for later use.  

> [!Note] 
> If your spreadsheet application does not offer **CSV UTF-8 (Comma delimited) (*.csv)** as a file-type choice (for example, versions of Excel older than Excel 2016), you'll need to use another program, such as Notepad++, to save this file as comma-delimited UTF-8. 

### Example .csv data file

Here's an example snippet of a valid .csv data file:

PersonId,EffectiveDate,HireDate,ManagerId,TimeZone,LevelDesignation,Organization,Layer,Area<br>
Emp1@contoso.com,10/1/2017,1/3/2014,Mgr1@contoso.com,Pacific Standard Time,5,Sales,8,Southeast<br>
Emp1@contoso.com,11/1/2017,1/3/2014,Mgr1@contoso.com,Pacific Standard Time,5,Sales,8,Southeast<br>
Emp1@contoso.com,12/1/2017,1/3/2014,Mgr2@contoso.com,Pacific Standard Time,4,Sales,7,Northeast<br>
Emp2@contoso.com,10/1/2017,8/15/2015,Mgr3@contoso.com,Pacific Standard Time,6,Sales,9,Midwest<br>
Emp2@contoso.com,11/1/2017,8/15/2015,Mgr3@contoso.com,Pacific Standard Time,6,Sales,9,Midwest<br>
Emp2@contoso.com,12/1/2017,8/15/2015,Mgr3@contoso.com,Pacific Standard Time,6,Sales,9,Midwest  

## Subsequent steps

* **Role:** admin

After you have populated and formatted your organizational data file, you can continue with the following intake steps. This section provides an overview only. To see the complete procedures, select the links in these steps:

1. [File upload](upload-organizational-data-1st.md#file-upload).

2. [Field mapping](upload-organizational-data-1st.md#field-mapping). After the data file is uploaded, you will encounter the mapping screen, where you map the source columns in the data file to Workplace Analytics names and select a datatype.

3. After you have confirmed the field mapping, [data validation](upload-organizational-data-1st.md#data-validation) starts. 

4. When validation finishes, it reports [success](upload-organizational-data-1st.md#validation-succeeds) or [failure](upload-organizational-data-1st.md#validation-fails). In case of errors, validation logs are made available.

   Validation errors can be caused by:

   * cells with invalid formatting (See [Rules for .xlsx files](#rules-for-xlsx-files) and [Rules for .csv files](#rules-for-csv-files).)
   * missing entries (empty cells) 
   * invalid use of special characters in column headers or in data rows (See [Use only valid values and formats](#use-only-valid-values-and-formats).)
 
   If validation fails, see the following:

   * If this is your first upload of organizational data: [Validation fails](upload-organizational-data-1st.md#validation-fails)
   * If this is a subsequent upload of organizational data: [Validation fails](upload-organizational-data.md#validation-fails)
  
   > [!Note] 
   > If this is a subsequent upload of organizational data, another factor that can play a role in validation is _validity threshold_. For more information, see [Columns in the field tables](upload-organizational-data.md#columns-in-the-fields-tables) and [Set validity threshold for custom fields](upload-organizational-data.md#set-validity-threshold-for-custom-fields).

<!-- NOTE FROM PRAMOD:
Specific instructions to create, debug & fix (in case of validation errors) should be separate for CSV & XSLX files. We should have a separate page for each. We should link to these pages as required in the Prepare organizational data, Upload org data (First upload), Upload org data (subsequent uploads) pages.
-->

## Related topic

[Prepare orgazational data](prepare-organizational-data.md)












