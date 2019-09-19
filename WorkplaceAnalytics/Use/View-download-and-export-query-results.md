---
# Metadata Sample
# required metadata

title: View download and export Workplace Analytics query results
description: Describes how to view, download, and export Workplace Analytics query results to PowerBI and other data analysis tools
author: paul9955
ms.author: v-midehm
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# View, download, and export query results

   > [!Note]
   > You must have the Analyst role in Workplace Analytics to view, download, or export query results.

In Workplace Analytics, **Analyze** > **Queries** > **Results** > **All results** lists all the queries that have been run for your organization.

![Query results tab](../images/wpa/Use/query-results-page.png)

In addition to seeing basic information about each query, you can view query results, download query results as a .csv file, delete them, or get a link to access them as data in Power BI or Excel.

   > [!Note]
   > In **Results**, you can switch between **My results** and **All results**.

## View query results

* Next to the query you want to view, select the ellipsis (**...**) > **View query**.
  
## Use Workplace Analytics data in Power BI, Excel, or other data-analysis tool

You can use data from your queries in a data-analysis tool to do further analysis and create reports. Workplace Analytics gives you two options, download data as a .csv file or get a link to an OData feed that you can use in Power BI.

### Download and import a query

The following steps are for Excel 2016. For other versions of Excel, open **Help** within Excel and search and use Excel's instructions on how to import a .csv file.

1. In **Analyze** > **Queries** > **Results** > **All results**, next to the query you want, select the **Download** icon.
2. If prompted, select to download the query as a PBI (Power BI) template or a .csv file.  
3. For .csv files, open and right-click the zip file, which contains a .csv version of the query, select **Extract All**, and extract the .csv to a local folder.
4. Open **Excel**, select to open **a new document**, and then open **a blank workbook**.
5. In the blank Excel workbook, select the **Data** tab at the top, and then select **Get Data** > **From File** > **From Text/CSV**.
6. Locate, select, and open the .csv file you unzipped in step 3.
7. In the **Text Import Wizard**, in **File Origin**, select **Unicode (UTF-8)**, and in **Preview**, confirm the data (including multi-byte characters) are shown correctly.​
8. In **Delimiter**, select **Comma**, and in **Data Type Detection**, select the applicable option, and then select **Load**.
9. Select **File** > **Save As** and save the file as an Excel (.xlsx) file to maintain the data in its currently formatted form, including multi-byte characters.​

### Get a link for an OData feed to use in Power BI

   > [!Note]
   > You can share Power BI dashboards. For more information, see [Share your Power BI dashboards and reports with coworkers and others](https://docs.microsoft.com/en-us/power-bi/service-share-dashboards).

1. Next to the query you want, select **Copy link**:

   ![copy link image](../images/wpa/Use/copy-link.png)

2. In Power BI, type or paste the URL into the **OData feed** dialog box.  
3. Select **Organizational account** and then select **Sign in**:

   ![Sign in to Workplace Analytics organizational account](../images/wpa/Use/OData-feed-sign-in.png)

4. Office 365 dialog box prompts you to choose an account. Select the account that you use when you log in to Workplace Analytics. This signs you in to Power BI and displays the OData feed dialog box, with the notification "You are currently signed in."
5. In the OData feed dialog box, select **Connect**. A "Refresh" dialog box might appear and display the status of the preparation of your data for import.

   After Power BI finishes importing your Workplace Analytics data, you can use the controls of Power BI to create visualizations of the data.

   > [!Important]
   > * The OData link is not available for query results that were created before 3/22/2018.

   > [!Note]
   > The auto-refresh option for queries determines whether the data in the OData feed is static or dynamic:
   >   * If the URL is tied to a query that is set to auto refresh, the data in the Odata feed updates on a regular schedule. For more information, see [Auto-refresh option for queries](../tutorials/query-auto-refresh.md). 
   >   * If the URL is tied to a query that is not set to auto refresh, the data in the OData feed is not automatically updated. This means that if you want new or different data, you will need to run a new query and get a new corresponding URL. 

## Related topics

[Connect to OData feeds in Power BI Desktop](https://docs.microsoft.com/en-us/power-bi/desktop-connect-odata) 

[Power BI templates in Workplace Analytics](../tutorials/power-bi-templates.md)

[Auto-refresh option for queries](../tutorials/query-auto-refresh.md)

[Share your Power BI dashboards and reports with coworkers and others](https://docs.microsoft.com/en-us/power-bi/service-share-dashboards)