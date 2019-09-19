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

In Workplace Analytics, the **Analyze** > **Queries** > **Results** page lists all the queries that have been run for your organization.

![Query results tab](../images/wpa/use/query-results-page.png)

In addition to seeing basic information about each query, you can view query results, download query results as a .csv file, delete them, or get a link to access them as data in Power BI or Excel.

   > [!Note]
   > On the **Results** page, you can switch between **My results** and **All results**.

## View query results

* Next to the query you want to view, select the ellipsis (**...**) > **View query**.
  
## Use Workplace Analytics data in Power BI, Excel, or other data-analysis tool

You can use data from your queries in a data-analysis tool to do further analysis and create reports. Workplace Analytics gives you three options to do this:

 * [Download and import query results](#download-and-import-query-results) 
 * [Get a link for an OData feed to use in Power BI](#get-a-link-for-an-odata-feed-to-use-in-power-bi)
 * [Connect through the PowerBI-Workplace Analytics connector](#connect-through-the-powerbi-workplace-analytics-connector)

### Download and import query results

1. On the **Analyze** > **Queries** > **Results** page, next to the query you want, select **Download**. A .csv file of results is downloaded.

2. Import the .csv file into the data-visualization tool.  

### Get a link for an OData feed to use in Power BI

   > [!Note]
   > You can share Power BI dashboards. For more information, see [Share your Power BI dashboards and reports with coworkers and others](https://docs.microsoft.com/en-us/power-bi/service-share-dashboards).

1. Next to the query you want, select **Copy link**:

   ![copy link image](../images/wpa/use/copy-link.png)

2. In Power BI, type or paste the URL into the **OData feed** dialog box.  
3. Select **Organizational account** and then select **Sign in**:

   ![Sign in to Workplace Analytics organizational account](../images/wpa/use/OData-feed-sign-in.png)

4. Office 365 dialog box prompts you to choose an account. Select the account that you use when you log in to Workplace Analytics. This signs you in to Power BI and displays the OData feed dialog box, with the notification "You are currently signed in."
5. In the OData feed dialog box, select **Connect**. A "Refresh" dialog box might appear and display the status of the preparation of your data for import.

   After Power BI finishes importing your Workplace Analytics data, you can use the controls of Power BI to create visualizations of the data.

   > [!Important]
   > * The OData link is not available for query results that were created before 3/22/2018.

   > [!Note]
   > The auto-refresh option for queries determines whether the data in the OData feed is static or dynamic:
   >   * If the URL is tied to a query that is set to auto refresh, the data in the Odata feed updates on a regular schedule. For more information, see [Auto-refresh option for queries](../tutorials/query-auto-refresh.md). 
   >   * If the URL is tied to a query that is not set to auto refresh, the data in the OData feed is not automatically updated. This means that if you want new or different data, you will need to run a new query and get a new corresponding URL. 

### Connect through the PowerBI-Workplace Analytics connector

The Power BI Workplace Analytics Connector is a Power BI Desktop connector for Microsoft Workplace Analytics. You can use it to build insights in Power BI by importing out-of-the-box metrics and person attributes from Workplace Analytics. The Connector automatically enforces the privacy rules that were configured by the organization's Workplace Analytics admin and guarantees the freshness of any visualized data. 

#### Prerequisites

##### Power BI desktop

To make this connection, you first need to download Power BI desktop. Follow these steps:

1. Open the [PowerBI Desktop site](https://powerbi.microsoft.com/desktop/). 
2. Select **Download free**. If a dialog box asks you "Open Microsoft Store?", select **Open Microsoft Store**.
3. In the Microsoft Store app, select **Get**. Power BI then is downloaded to your device and installed automatically. 
4. Select **Launch**. Power BI opens. 

##### Partition access

Partitions in Workplace Analytics allow access to data. To import metrics and attributes into Power BI, you will need access to the partition in Workplace Analytics that contains these metrics and attributes. (A step in the following procedure has you sign in to your work account to gain access to that partition.) For more information, see [Role-based Authorization in Kusto](https://docs.microsoft.com/en-us/azure/kusto/management/access-control/role-based-authorization). 

#### Use the connector

1.	In Power BI Desktop, select the **Get Data** button:

    ![Get Data button](../images/wpa/use/get-data-in-pbi.png)

2.	Select **Online Services** and then select **Workplace Analytics**:

    ![Get Data button](../images/wpa/use/copy-link.png)

3.	Enter the Workplace Analytics partition ID:

    ![Get Data button](../images/wpa/use/copy-link.png)

4.	Select the Data Connectivity mode you'd like to use: **Direct Query** (recommended) or **Import**. For more information about this choice, see [Use DirectQuery in Power BI Desktop](https://docs.microsoft.com/en-us/power-bi/desktop-use-directquery).
 
5.	If prompted, sign in to your work account:

    ![Get Data button](../images/wpa/use/copy-link.png)

6.	At this point, if the connection is a success, Power BI displays a list of metrics and attributes in the **Fields** section:

    ![Get Data button](../images/wpa/use/copy-link.png)

   In Power BI, you can now create visualizations using those fields.

7.	After you have finished creating visualizations, you can publish your reports to Power BI online and share them with others in your organization. For more information, see [Share your Power BI dashboards and reports with coworkers and others](https://docs.microsoft.com/en-us/power-bi/service-share-dashboards). 

## Related topics

[Connect to OData feeds in Power BI Desktop](https://docs.microsoft.com/en-us/power-bi/desktop-connect-odata) 

[Power BI templates in Workplace Analytics](../tutorials/power-bi-templates.md)

[Auto-refresh option for queries](../tutorials/query-auto-refresh.md)

[Share your Power BI dashboards and reports with coworkers and others](https://docs.microsoft.com/en-us/power-bi/service-share-dashboards)