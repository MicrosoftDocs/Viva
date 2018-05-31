---
# Metadata Sample
# required metadata

title: View download and export Workplace Analytics query results
description: This is topic describes how to view, download, and export Workplace Analytics query results to PowerBI and other data analysis tools. 
author: LeisaLaDell
ms.author: v-leash
ms.date: 3/5/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---
# View, download, and export query results 
 
The **Results** tab in **Queries** lists all the queries that have been run for your organization. 

![Query results tab](../images/wpa/Use/Query-results-tab.png)

In addition to seeing basic information about each query, you can view query results, download query results as a .csv file, and get a link that enables you to access and use the data from within Power BI. 
 
You can switch between **My results** and **All results**. 
![Switch between My results and All results](../images/wpa/Use/My-results-All-results.png) 

## View query results

#### To view query results  
* For the query you want, click **View**. ![View button](../images/wpa/Use/view.png)
  
## Use Workplace Analytics data in Power BI and other data analysis tools 
 
You can use data from your queries in other data analysis tools to do further analysis and create reports. Workplace Analytics gives you two options, download data as a .csv file, or get a link to an OData feed that you can use in Power BI.  
 
### Download and then import a .csv file 
 
#### To download query results as a .csv file  
1. For the query you want, click **Download** ![Download button](../images/wpa/Use/download.png) 
2. Import the .csv file into the tool that you want.  
 
### Get a link for OData feed that you can use in Power BI 
 
When you create reports in Power BI, you can share those reports with co-workers, but they will not have access to the raw data.   
 
#### To get a link to the data  
1. For the query you want, click **Copy link** . ![alt text for image](../images/wpa/Use/copy-link.png) 
2. In Power BI, type or paste the URL into the **OData feed** box.  
3. When prompted in Power BI, sign in your Workplace Analytics organizational account. You must have the Analyst role in Workplace Analytics.
![Sign in to Workplace Analytics organizational account](../images/wpa/Use/OData-feed-sign-in.png)
 
> [!Important]
> * The data in the OData feed is static, so if you want new or different data, you will need to run a new query and get a new corresponding URL.
> * The OData link is not available for query results created prior to 3/22/2018.    
 
 
### Related topic
[Connect to OData feeds in Power BI Desktop](https://docs.microsoft.com/en-us/power-bi/desktop-connect-odata) 
 
 
 
 