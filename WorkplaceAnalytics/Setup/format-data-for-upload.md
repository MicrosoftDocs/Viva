---
# Metadata Sample
# required metadata

title: Format data for upload to Workplace Analytics
description: How to format .xlsx files and .csv files for upload to Workplace Analytics 
author: paul9955
ms.author: v-pascha
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Format data for upload

Various setup and usage tasks require admins to upload data to Workplace Analytics. Admins can upload files that contain organizational (HR) data <!--and CRM data--> as part of setup or as a regular data-refresh task. Analysts can upload files that specify groups of employees when they define queries of particular types. 

For these uploads, you can choose from among two file formats. The following sections describe how to format these files so that Workplace Analytics can use the data they contain. 

 * [Format .xlsx files](#format-xlsx-files)
 * [Format UTF-8 encoded .csv files](#format-csv-files)


### Which format to use?

**Recommended: Use .xlsx.** This format is easier to use in most cases. However, for many data uploads, you could use either format. Note that both formats have restrictions: 

1. **Use .xlsx if outside of the United States.** Files in the UTF-8 encoded .csv format are subject to United-States data formatting, so if your organization is based outside of the United States and uses non-U.S. formatting for dates, times, or numbers, use the .xlsx format. 
2. **Encode .csv files properly.** Only choose the .csv-file option if you can format it as required: UTF-8 encoded, and with all data (dates, times, numbers) in United-States format. Files in the .xlsx format do not have these restrictions.
3. **Stay under the size limit.** The upper limit of .xlsx files for upload is 1.5 GB. If your upload file is larger than 1.5 GB, use the .csv format instead.

> [!Note] 
> For more information about selecting and arranging the _contents_ of these files (as opposed to adhering to their _formatting_ rules), see  [Prepare organizational data](prepare-organizational-data.md). 

<!-- PER PRAMOD (23 AUGUST 2019) REMOVE THIS. "For now, CRM will continue to support upload only through CSV."
> * CRM data: [Prepare the CRM source data](crm-data-upload.md#prepare-the-crm-source-data)
-->
<!-- 
> * Upload groups for use in solutions: [Use a .csv file](../tutorials/solutions-conceptual.md#use-a-csv-file)  **[This link is a placeholder for now. This section will need to be rewritten.]**
-->

## Format UTF-8 encoded .csv files

### Rules for .csv files

 * **UTF-8** Data files in .csv format must be in UTF-8 format.
 > * **Accepted date format.** All dates must be in the mm/dd/yyyy format.
 > * **Accepted number format.** Numerical fields (such as "HourlyRate") must be in the U.S. "number" format and cannot contain commas or a dollar sign. Example: Use **8.75**, not **8,75**. 
 >  * **Delimiters.**  Use only the number delimiter (comma) of the United States. 

### Example .csv data file

Here's an example snippet of a valid .csv data file:

PersonId,EffectiveDate,HireDate,ManagerId,TimeZone,LevelDesignation,Organization,Layer,Area<br>
Emp1@contoso.com,10/1/2017,1/3/2014,Mgr1@contoso.com,Pacific Standard Time,5,Sales,8,Southeast<br>
Emp1@contoso.com,11/1/2017,1/3/2014,Mgr1@contoso.com,Pacific Standard Time,5,Sales,8,Southeast<br>
Emp1@contoso.com,12/1/2017,1/3/2014,Mgr2@contoso.com,Pacific Standard Time,4,Sales,7,Northeast<br>
Emp2@contoso.com,10/1/2017,8/15/2015,Mgr3@contoso.com,Pacific Standard Time,6,Sales,9,Midwest<br>
Emp2@contoso.com,11/1/2017,8/15/2015,Mgr3@contoso.com,Pacific Standard Time,6,Sales,9,Midwest<br>
Emp2@contoso.com,12/1/2017,8/15/2015,Mgr3@contoso.com,Pacific Standard Time,6,Sales,9,Midwest

### Use only valid values and formats

When any data row or column has an invalid value for any attribute, the entire upload will fail until the source file is fixed (or the mapping changes the validation type of the attribute in a way that makes the value valid). 

[!INCLUDE [Valid values and formats](../includes/org-data-upload-tips.md)]

### Create a valid UTF-8 encoded .csv file in Microsoft Excel

1. Export organizational data from your HR database.

2. Open Microsoft Excel and import the exported organizational data. 

3. In Excel, organize the data:

   a. Place all of the data on a single worksheet. 

   b. In the worksheet, the first row must contain column headers. Every column must have a column header. To know what columns (what data) to include, see [Prepare orgazational data](prepare-organizational-data.md). 

   c. All rows below row 1 must contain data about employees. Include one row of data per person, per EffectiveDate. (EffectiveDate is one of the required attributes in your data. For more information, see [Structure the organizational data](prepare-organizational-data.md#structure-the-organizational-data).)

4. Save the worksheet into a single, flat, text file.
   
   ![Save .csv file](../images/wpa/setup/csv-file-format.png)

   a. In Excel, point to **File** and select **Save As**.
   
   b. Type a name for the file, choose the file type **CSV UTF-8 (Comma delimited) (*.csv)**, and select **Save**:

   ![Save as UTF-8 .csv file](../images/wpa/setup/csv-utf-8.png)
 
   Note the location of the file, for later use.  
   
## Format .xlsx files 

### Rules for .xlsx files

Acceptable .xlsx files must adhere to the following: 

 * **File extension.** The extension must be _.xlsx_. It cannot be any other extension (such as .xls, .xlsb, or .xlsm) that is supported by Microsoft Excel or another spreadsheet applicaiton.
 * **No formulas or macros.** Include no formulas or macros in cells in the .xlsx file.
 * **Accepted number and date formats.** While .csv files require U.S. delimiter and date format, this restriction does _not_ apply to .xslx files. You can use the formats for other locales in .xlsx files. For more information, see [Selecting an accepted format](#selecting-an-accepted-format).
 * **Size limit.** The upper limit of .xlsx files for upload is 1.5 GB. If your upload file is larger than 1.5 GB, use the .csv format instead. 
 * **Internal structure.** See the following section, [Structure an .xlsx file](#structure-an-xlsx-file) to learn how to structure the columns and rows in an .xlsx file for successful upload.

#### Selecting an accepted format

For numbers and for dates, you can use only the predefined formats that Microsoft Excel offers. Do not use custom formats. To guarantee that you've selected a predefined format, follow these steps:

1. Select one or more cells in a column that you want to format. In this example, we're formatting cells that contains dates:

   ![Save .csv file](../images/wpa/setup/format-date-cell.pg)

2. Right-click the selection (of one or more cells) and select **Format Cells**.   

3. In the **Format Cells** dialog box, under **Category**, select **Date**.

4. Under **Type**, select a type. 

> [!Note] 
> Every cell in a column must have the same data type except the first (header) row, which contains strings. You can format the cells in row 1 as **General** or **Text** in Excel. 

 ### Structure an .xlsx file

 #### Sheets

 * **First sheet only.** Workplace Analytics will read only the first sheet of the .xlsx file. You can have data on other sheets, but it will be ignored. To confirm which sheet is the first sheet, open the file in Excel and locate the tab farthest to the left. 

 #### Columns 

 * **First row contains column headers.** In the first sheet, the values in the first row are considered to be column headers. Note that Workplace Analytics uses these column headers in the same ways that it uses column headers in .csv files, such as on the organizational-data Mapping page. 
 * **Blank and repetitive cells.** Workplace Analytics checks all cells in the first row to verify that there are no blank cells and no repetitions.
 * **Strings only in column headers.** Column headers must be strings.

 #### Data 

Use the help of the formatting function in Excel to make sure your data (all cells other than in the first row) is correctly formatted to the data type of your choice, such as date, number or text.

If you intend to use a column and map its data to a particular Workplace Analytics data type, see the following table for guidelines.

 | Workplace Analytics data type | Format the call as this type in Excel | 
 | ------------------ | --------- | 
 | TimeZone | In the Workplace Analytics mapping screen, make sure that all entries in the column are formatted as Text in Excel and then saved. All timezone strings must be one of the specified value for TimeZone values specified in [Time zones for Workplace Analytics](../use/timezones-for-workplace-analytics.md). |
| Email | In Excel, choose the data type Text or General and make sure that the string is in a valid email format; for example, abc@xyz.com |  
| Boolean | In Excel, the values "TRUE" and "FALSE" must be present. You can type these strings as General or Text strings. | 
| Datetime | In Excel, choose the appropriate data type, Datetime. |
| Double   | In Excel, choose the appropriate data type, Double |
| Integer  | In Excel, choose the appropriate data type, Integer. |
| String   | In Excel, choose General or Text. |











