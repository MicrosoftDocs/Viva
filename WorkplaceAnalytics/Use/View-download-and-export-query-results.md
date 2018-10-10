---
# Metadata Sample
# required metadata

title: View download and export Workplace Analytics query results
description: This is topic describes how to view, download, and export Workplace Analytics query results to PowerBI and other data analysis tools. 
author: madehmer
ms.author: v-midehm
ms.date: 9/4/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# View, download, and export query results

   > [!Note]
   > To complete this procedure, you must have the Analyst role in Workplace Analytics.

In Workplace Analytics, on the **Queries** page, the **Results** tab lists all the queries that have been run for your organization.

![Query results tab](../images/wpa/Use/Query-results-tab.png)

In addition to seeing basic information about each query, you can view query results, download query results as a .csv file, and get a link that you can use to access these results as data within Power BI.

   > [!Note]
   > On the **Queries** page, you can switch between **My results** and **All results**:
   
   ![Switch between My results and All results](../images/wpa/Use/My-results-All-results.png)

## View query results

#### To view query results

* Next to the query you want, select the ellipsis (**...**) &gt; **View query**.
  
## Use Workplace Analytics data in Power BI or in other data-analysis tools

You can use data from your queries in a data-analysis tool to do further analysis and create reports. Workplace Analytics gives you two options, download data as a .csv file, or get a link to an OData feed that you can use in Power BI.  

### Download and then import a .csv file

#### To download query results as a .csv file

1. On the Queries &gt; Results page, next to the query you want, select **Download**.

2. Import the .csv file into the tool that you want.  

### Get a link for an OData feed that you can use in Power BI

   > [!Note]
   > When you create reports in Power BI, you can share those reports with co-workers, but they will not have access to the raw data.

#### To get a link to the data

1. Next to the query you want, select **Copy link**:

   ![copy link image](../images/wpa/Use/copy-link.png)

2. In Power BI, type or paste the URL into the **OData feed** dialog box.  

3. Select **Organizational account** and then select **Sign in**:

   ![Sign in to Workplace Analytics organizational account](../images/wpa/Use/OData-feed-sign-in.png)

4. If you have more than one organizational account, an Office 365 dialog box prompts you to choose one. Select the account that you use when you log in to Workplace Analytics. This signs you in to Power BI and displays the OData feed dialog box, with the notification "You are currently signed in."

5. In the OData feed dialog box, select **Connect**. A "Refresh" dialog box might appear and display the status of the preparation of your data for import.  

6. You are now signed in to Power BI. This is indicated by the "You are currently signed in" notification in the OData feed dialog box.

   > [!Note]
   > At this point, you've imported data into Power BI. You can now create visualizations of this data.  
   
   > [!Important]
   > * The data in the OData feed is static, so if you want new or different data, you will need to run a new query and get a new corresponding URL.
   > * The OData link is not available for query results created prior to 3/22/2018.

### Related topics

[Connect to OData feeds in Power BI Desktop](https://docs.microsoft.com/en-us/power-bi/desktop-connect-odata) 

[Power BI templates in Workplace Analytics](../tutorials/power-bi-templates.md)
