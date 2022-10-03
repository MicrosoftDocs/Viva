---
ROBOTS: NOINDEX,NOFOLLOW
title: Download a query Report in UTF-8 format
description: If your query reports cannot be opened properly in Excel because they contain multi-byte characters, follow these steps to work around the problem   
author: madehmer
ms.author: helayne
ms.topic: troubleshooting
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Download a query report in UTF-8 format

Your query reports might not open properly if their data contains certain (multibyte) characters. This topic describes this problem and its workaround.

## Cannot properly open a .csv file

### Background

When you run a query in Microsoft Viva Insights, the query results are available as a .csv file that you can then download and view in Microsoft Excel.

At least one of the metrics in queries include meeting data from Outlook, which includes meeting subject lines. At least some of the meeting subject lines contains multibyte characters. This might be because your organization uses a multibyte language (such as Chinese, Japanese, or Korean), or because the data contains characters such as an EM-DASH (—) or letters with diacritical marks (such as the ã in "São Paulo").

### Problem

These multibyte characters cause the .csv file to malfunction if you try to open it in Excel in the default way.

### Solution

You can import a .csv file by opening it in Microsoft Excel. After you open it, you can save it as an Excel file (with the .xlsx extension) or as a .csv file in UTF-8 format. The steps to do this differ in different versions of Excel. The following describes the steps for Excel versions 2017 and 2010.

#### Excel 2017

1. In Viva Insights, download the .zip file that contains the .csv report file.
2. Extract the .csv file to a safe location on your computer; take note of this folder.
3. Open a new workbook in Microsoft Excel.
4. On the ribbon, open the Data tab.
5. In the Get & Transform Data area, select **From Text/CSV**.
6. In the Import Data dialog box, select the extracted .csv file and select **Import**.
7. In the dialog box that appears, change File Origin to **65001: Unicode (UTF-8)**.
8. In the preview pane, examine the data. If it is still incorrect, contact [Microsoft support](https://support.microsoft.com/contactus/) for further guidance. If the data is correct, go to the next step.
9. Select **Comma** as the delimiter.
10. Select **Load**.

#### Excel 2010

1. In Viva Insights, download the .zip file that contains the .csv report file.
2. Extract the .csv file to a safe location on your computer; take note of this folder.
3. Open a new workbook in Microsoft Excel.
4. On the ribbon, open the **Data** tab.
5. In the **Get External Data** area, select **From Text**.
6. In the **Import Text File** dialog box, locate the extracted .csv file and select **Import**.
7. In the Text Import Wizard, do the following:

   * *Step 1 of 3:* Under Original data type, select **Delimited** and then select **Next**.
   * *Step 2 of 3:* In the Delimiters area, select **Comma** and then select **Next**.
   * *Step 3 of 3:* Under Column data format, select **Text** and then select **Finish**.

8. The Import Data dialog box asks where you want to put the data. Choose any cell in the blank worksheet and then select **OK**.

The multibyte characters should now show up correctly in Excel. You can save the file as an Excel file or an OpenDocument Spreadsheet file without losing the multibyte characters.

## Related topics

[Get support](../overview/getting-support.md)