---
# Metadata Sample
# required metadata

title: Download the Query Report from Workplace Analytics in UTF-8 format
description: If your query reports cannot be opened properly in Excel because they contain multibyte characters, follow these steps to work around the problem.   
author: paul9955
ms.author: v-pascha
ms.date: 04/18/2018
ms.topic: get-started-article
ms.prod: wpa
---

# Download a query report in UTF-8 format 

Your query reports might not open properly if their data contains certain (multibyte) characters. This topic describes this problem and its workaround. 

## Cannot properly open a .csv file

### Background

You have run a query to perform an analysis of workplace behavior. When the query finished, Workplace Analytics wrote the query results to a .csv file, which it then placed in a compressed (zipped) folder. Now that you have your query results, you want to proceed with your analysis by opening the results in Microsoft Excel. 

At least one of the metrics that you used in this query includes meeting data from Outlook, and that data includes meeting subject lines. At least some of the meeting subject lines contains multibyte characters. This could be because your organization uses a multibyte language (such as Chinese, Japanese, or Korean), or because the data contains characters such as an EM-DASH (—) or letters with diacritical marks (such as the ã in "São Paulo"). 

### Problem
These multibyte characters cause the .csv file to malfunction if you try to open it in Excel in the default way. 

### Solution
Import the .csv file into Excel as a UTF-8 file. After you have opened the file in Excel in this way, you can save the file as an Excel file (with the .xlsx extension) or as a .csv file in UTF-8 format, and then work with it in the normal ways. Follow these steps:

**To import a .csv file as a UTF-8 file** 

> [!Note] 
> In some versions of Excel the options you choose are different. The following steps present you with alternatives that your version of Excel might offer.  

1. In Workplace Analytics, download the .zip file that contains the .csv report file. 
2. Extract the .csv file to a safe location on your computer; take note of this folder.
3. Open a new workbook in Microsoft Excel, and then select the Data tab.
4. On the ribbon, click **Get Data** (or **Get External Data**), point to **From File**, and click **From Text/CSV** (or **From Text**).
5. In the Import Data dialog box, select the extracted .csv file and click **Import** (or **Open**). 
6. In the dialog box that appears, change File Origin to **65001: Unicode (UTF-8)** (or **Unicode (UTF-8)**). In the preview pane, examine the data. If it is still incorrect, contact your Workplace Analytics FastTrack representative for further guidance. If the data is correct, go on to the next step. 
7. Select **Comma** as the delimiter. 
8. Click **Load** (or **Finish**).

The multi-byte characters should now display correctly in Excel. You can save the file as an Excel file or an OpenDocument Spreadsheet file without losing the multi-byte characters.
