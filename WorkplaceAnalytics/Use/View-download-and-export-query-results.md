---
# Metadata Sample
# required metadata

title: View download and export Workplace Analytics query results
description: This is topic describes how to view, download, and export Workplace Analytics query results to PowerBI and other data analysis tools. 
author: paul9955
ms.author: madehmer
ms.date: 12/3/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# View, download, and export query results

   > [!Note]
   > To complete this procedure, you must have the Analyst role in Workplace Analytics.

In Workplace Analytics, the **Queries** > **Results** page lists all the queries that have been run for your organization.

![Query results tab](../images/wpa/Use/query-results-page.png)

In addition to seeing basic information about each query, you can view query results, download query results as a .csv file, delete them, or get a link to access them as data in Power BI or Excel.

   > [!Note]
   > On the **Results** page, you can switch between **My results** and **All results**.

## View query results

* Next to the query you want to view, select the ellipsis (**...**) > **View query**.
  
## Use Workplace Analytics data in Power BI, Excel, or other data-analysis tool

You can use data from your queries in a data-analysis tool to do further analysis and create reports. Workplace Analytics gives you two options, download data as a .csv file or get a link to an OData feed that you can use in Power BI.

### Download and import a query

1. On the **Analyze** > **Queries** > **Results** page, next to the query you want, select **Download**.
2. Import the .csv file into the tool that you want.  

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