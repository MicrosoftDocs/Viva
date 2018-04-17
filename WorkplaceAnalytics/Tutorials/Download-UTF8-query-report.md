---
# Metadata Sample
# required metadata

title: Download the Query Report from Workplace Analytics
description: This topic discusses how group queries in Workplace Analytics can help you understand how a team has invested their time across the rest of the organization and beyond.  
author: paul9955
ms.author: v-pascha
ms.date: 04/17/2018
ms.topic: get-started-article
ms.prod: wpa
---

# Download a query report in UTF-8 format 

Depending on the language in use at your organization (for example, Chinese, Japanese, Korean), your organizational attributes might contain multi-byte characters. In this case, you might need to open the downloaded csv in special UTF-8 format by importing to a new Excel file. 

1. Download the .zip file from WpA and unzip the csv report file to a safe recognizable location on your computer.
2. Open a new document in Excel and select the "Data" tab.
3. Click **Get External Data** on the ribbon and then select **From Text**. Excel opens a file browsing window.
4. Select the CSV file that you unzipped that contains the data and then click **Open**. The Text Import Wizard starts automatically.
5. Change the File Origin setting to Unicode (UTF-8). Check the characters in the preview pane.
6. If you imported a fixed-width text file, select **Fixed Width** as the data type. Otherwise, select **Delimited** as the data type.
Click **Next**.
7. Select **Comma** as the delimiter for a CSV file. For a text file, either select the appropriate delimiter or adjust the fixed column width in the preview pane. Click **Next**.
8. Click **Finish** to complete the import. 

The multi-byte characters should now display correctly in Excel. You can save the file as an Excel file or an OpenDocument Spreadsheet file without losing the multi-byte characters.
