---
# Metadata Sample
# required metadata

title: Upload .xlsx files to Workplace Analytics
description: Background of uploading .xlsx files to Workplace Analytics 
author: paul9955
ms.author: v-pascha
ms.date: 08/15/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Upload .xlsx files to Workplace Analytics

Various setup and usage tasks require admins to upload data to Workplace Analytics. Admins can upload .csv files that contain organizational (HR) data and CRM data as part of setup or as a regular data-refresh task. Analysts can upload .csv files that specify groups of employees when they define queries of particular types. These .csv files must be in UTF-8 format and they must use the number delimiter (comma) and date format (mm/dd/yyyy) of the United States. 

However, _comma-separated values_ (.csv) is not the only format that Workplace Analytics supports for data upload. It also accepts the .xlsx format, provided that you follow the rules in the following section, [Rules for .xlsx files](#rules-for-xlsx-files). 

## Rules for .xlsx files

 * **File extension.** The extension must be _.xlsx_. It cannot be any other extension (such as .xls, .xlsb, or .xlsm) that is supported by Microsoft Excel or another spreadsheet applicaiton.
 * **No formulas.** Include no formulas in cells in the .xlsx file.
 * **Accepted number and date formats.** While .csv files require U.S. delimeter and date format, this restriction does _not_ apply to .xslx files. You can use the formats for other locales in .xlsx files. 
 * **Size limit.** The upper limit of .xlsx files for upload is 1.5 GB. If your upload file is larger than 1.5 GB, use the .csv format instead. 
 * **Internal structure.** See the following section, [Structure an .xlsx file](#structure-an-xlsx-file) to learn how to structure the columns and rows in an .xlsx file for successful upload.

 ## Structure an .xlsx file

 ### Sheets

 * **First sheet only.** Workplace Analytics will read only the first sheet of the .xlsx file. You can have data on other sheets, but it will be ignored. To confirm which sheet is the first sheet, open the file in Excel and locate the tab farthest to the left. 

 ### Columns 

 * **First row contains column headers.** In the first sheet, the values in the first row are considered to be column headers. Note that Workplace Analytics uses these column headers in the same ways that it uses column headers in .csv files, such as on the organizational-data Mapping page. 
 * **Blank and repetitive cells.** Workplace Analytics checks all cells in the first row to verify that there are no blank cells and no repetitions.
 * **Strings only in column headers.** Column headers must be strings.

 ### Data 

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











