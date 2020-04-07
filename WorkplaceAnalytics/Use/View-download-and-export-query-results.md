---

title: View, download, and export Workplace Analytics query results
description: Describes how to view, download, and export Workplace Analytics query results to PowerBI and other data analysis tools
author: madehmer
ms.author: paul9955
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# View, download, and export query results

**Role:** Analyst role is required in Workplace Analytics to view, download, or export query results.
  
In Workplace Analytics, the **Analyze** > **Queries** > **Results** > **All results** page lists all the queries that have been run for your organization. In addition to seeing basic information about each query, you can view query results, download query results as a .csv file, delete results, or get a link to access them as data in Power BI or Excel.

![Query results tab](../images/wpa/use/query-results-page.png)

## View query results

On the **Analyze** > **Queries** > **Results** page, you can switch between **All results** (the results of queries that all analysts have run, as shown in the preceding screenshot) and **My results** (only the results of queries that the analyst who is viewing this page has run).

1. In Workplace Analytics, open the **Analyze** > **Queries** > **Results** > **All results** page.

2. Next to the query you want to view, select the ellipsis (**...**) > **View query**.
  
## Use Workplace Analytics data in Power BI, Excel, or other data-analysis tool

You can use data from your queries in a data-analysis tool to do further analysis and create reports. Workplace Analytics gives you three options to do this:

| Option | Description |
| ------ | ----------- |
| [Download and import query results](#download-and-import-query-results) | After a Workplace Analytics query returns results, visualize them in a tool of your choice. |
| [Get a link for an OData feed to use in Power BI](#get-a-link-for-an-odata-feed-to-use-in-power-bi) | After a Workplace Analytics query returns results, visualize them in Power BI. |
| [Connect through the Workplace Analytics Power BI Connector](#connect-through-the-power-bi-connector) | Visualize Workplace Analytics data within Power BI by running aggregated query data. |

### Download and import query results

The following steps are for Excel 2016. For other versions of Excel, open **Help** within Excel and search and use Excel's instructions on how to import a .csv file.

1. In **Analyze** > **Queries** > **Results** > **All results**, next to the query you want, select the **Download** icon.
2. If prompted, select to download the query results as a .csv file.
3. Select to open and right-click the zip file, which contains a .csv version of the query, and then select **Extract All** and extract the .csv to a local folder.
4. Open **Excel**, select to open **a new document**, and then open **a blank workbook**.
5. In the blank Excel workbook, select the **Data** tab at the top, and then select **Get Data** > **From File** > **From Text/CSV**.

    ![import .csv file](../images/wpa/Use/import-csv.png)

6. Locate, select, and open the .csv file you unzipped in step 3.
7. In the **Text Import Wizard**, in **File Origin**, select **Unicode (UTF-8)**, and in **Preview**, confirm the data (including multi-byte characters) are shown correctly.​
8. In **Delimiter**, select **Comma**, and in **Data Type Detection**, select the applicable option, and then select **Load**.
9. Select **File** > **Save As** and save the file as an Excel (.xlsx) file to maintain the data in its currently formatted form, including multi-byte characters.​

### Get a link for an OData feed to use in Power BI

   > [!Note]
   > You can share Power BI dashboards. For more information, see [Share your Power BI dashboards and reports with coworkers and others](https://docs.microsoft.com/power-bi/service-share-dashboards).

1. Next to the query you want, select **Copy link**:

   ![copy link image](../images/wpa/use/copy-link.png)

2. In Power BI, paste the URL into the **OData feed** dialog box.
3. Select **Organizational account** and then select **Sign in**:

   ![Sign in to Workplace Analytics organizational account](../images/wpa/use/OData-feed-sign-in.png)

4. When the **Office 365** dialog box prompts you, select the account and enter the password that you use to log in to Workplace Analytics. You'll then see: "You are currently signed in."
5. In the **OData feed** dialog box, select **Connect**. A "Refresh" dialog box might appear and display the status of the preparation of your data for import.

   After Power BI finishes importing your Workplace Analytics data, use Power BI tools to create visualizations of the data.

   > [!Important]
   > * The OData link is not available for query results that were created before March 22, 2018.

   > [!Note]
   > The auto-refresh option for queries determines whether the data in the OData feed is static or dynamic:
   >   * If the URL is tied to a query that is set to auto refresh, the data in the Odata feed updates on a regular schedule. For more information, see [Auto-refresh option for queries](../tutorials/query-auto-refresh.md).
   >   * If the URL is tied to a query that is not set to auto refresh, the data in the OData feed is not automatically updated. This means that if you want new or different data, you must run a new query and get a new corresponding URL.

### Connect through the Power BI Connector

**Required role:** Analyst or Limited analyst

You can use the Power BI Connector to connect to or import Workplace Analytics data and construct visualizations and build insights about the data in Power BI.

You can import specific metrics and person attributes from Workplace Analytics, or create and connect a new person or meeting query to define what metrics and attributes you want to connect to and analyze in Power BI.

The Connector automatically enforces the privacy rules configured by the organization's Workplace Analytics admin by only providing and guarantees the freshness of any visualized data.

> [!Note]
> The Power BI Connector does not use results of previously-run queries. Instead, it creates Power BI visualizations by running aggregated queries of Workplace Analytics data on standard [Person metrics](metric-definitions.md#person-metrics). (Aggregated queries include groupings of metrics on one or more columns of organizational-data attributes, with aggregations such as Sum, Average, Min, and Max on the metric columns.)

#### Prerequisites

##### Power BI desktop

If you don't already have Power BI Desktop, use the following steps to install it.

1. Go to [PowerBI Desktop site](https://powerbi.microsoft.com/desktop/).
2. Select **Download free** and follow the online instructions to install and launch it.

##### Partition access

Partitions in Workplace Analytics allow access to specific partitions of data within Workplace Analytics. To import query data into Power BI, you need access to the partition in Workplace Analytics that contains the metrics and attributes you want to analyze in Power BI. (To gain access to that partition, use the following steps to sign in to your organizational account and select the partition ID.) <!-- For details, see [Partitions in Workplace Analytics](../setup/partitions-in-wpa.md). -->

#### Use the Power BI Connector

1. In Power BI Desktop, select the **Get Data** button:

    ![Get Data button](../images/wpa/use/get-data-in-pbi.png)

2. Select **Online Services**, select **Workplace Analytics**, and then select **Connect**:

    ![Get Online Services](../images/wpa/use/get_data_screen.png)

3. Locate and copy the identifier of the currently selected Workplace Analytics partition. To do this, select the user icon in the top right of the page in Workplace Analytics, and then select **My information**:

    ![My information screen](../images/wpa/use/top-right-my-info.png)

    In **My information**, copy the partition identifier:

    ![My information screen](../images/wpa/use/my-information.png)

4. In **Connect to Workplace Analytics Data**, paste the copied partition identifier:

    ![Enter Workplace Analytics data connections](../images/wpa/use/pbi-wpa-connect.png)

    To import Person metrics, continue to the next step. Or to connect to a custom person or meeting query:

    a. Enter one or more keywords or the complete query name in **Query Name**.
    b. Or enter the query's ID in **Query Identifier**. To do this:

      * Go to **Workplace Analytics** > **Analyze** > **Queries** > **Results**, and then select the **Copy link** icon next to the query you want to connect to in Power BI.
      * Only highlight and copy the **32-digit ID** just before the query type at the end of the link, and then paste it into **Query Identifier** in the Power BI :

      ![Query ID](../images/wpa/use/pbi-wpa-query-id.png)

5. Select the applicable data connectivity mode: **Direct Query** (recommended) or **Import**, and then select **OK**. For details, see [Use DirectQuery in Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-use-directquery).

6. The first time you use the PowerBI Connector for a particular partition ID or when your authentication token expires, you'll be prompted to sign in. Select **Sign in** and then enter your Office 365 credentials:

    ![Sign in](../images/wpa/use/login-to-o365_2.png)

7. If the connection is a success, Power BI lists the available queries that match the Query Name or ID or person metrics in the **Fields** section. For example:

    ![Metrics](../images/wpa/use/pbi-query-list.png)

In Power BI, you can now create visualizations using the selected fields.

For example, you can generate a bar chart that shows an organization-wide analysis of collaboration hours or examines the meeting-hours trend for an entire organization.

![Get Data button](../images/wpa/use/example-pbi-visual.png)

After you have finished creating visualizations, you can publish your reports to Power BI online and share them with others in your organization. For more information, see [Share your Power BI dashboards and reports with coworkers and others](https://docs.microsoft.com/power-bi/service-share-dashboards).

## Related topics

[Connect to OData feeds in Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-connect-odata)

[Power BI templates in Workplace Analytics](../tutorials/power-bi-templates.md)

[User roles in Workplace Analytics](../use/user-roles.md)

[Auto-refresh option for queries](../tutorials/query-auto-refresh.md)

[Share your Power BI dashboards and reports with coworkers and others](https://docs.microsoft.com/power-bi/service-share-dashboards)
