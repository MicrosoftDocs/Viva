---

title: View, download, and export Workplace Analytics query results
description: Describes how to view, download, and export Workplace Analytics query results to Power BI and other data analysis tools
author: madehmer
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# View, download, and export query results

**Role:** Analyst role is required in Workplace Analytics to view, download, or export query results
  
In Workplace Analytics, the **Analyze** > **Queries** > **Results** > **All results** page lists all the queries available for your organization. In addition to seeing basic information about each query, you can view query results, download query results as a .csv file, delete results, or get a link to access them as data in Power BI or Excel.

![Query results tab](../images/wpa/use/query-results.png)

## View query results

On the **Analyze** > **Queries** > **Results** page, you can switch between **All results** (includes queries created by all analysts) and **My results** (only queries that you created, as an analyst).

1. In Workplace Analytics, go to **Analyze** > **Queries** > **Results** > **All results**.

2. Next to the query you want to view, select the ellipsis (**...**) > **View query**.
  
## Use Workplace Analytics data in Power BI, Excel, or other data-analysis tool

You can use the following options to access and use Workplace Analytics query data in a different data-analysis tool to create visuals and reports outside of Workplace Analytics.

|Option | Description |
|------ | ----------- |
|[Download and import query results](#download-and-import-query-results) | Exports *static raw data* from a Workplace Analytics query as a .csv file, which you can then import into a tool of your choice. <br><br>When sharing analysis in the other tool, take caution to ensure that only authorized users can access the raw data. |
|[Get a link for an OData feed to use in Power BI](#get-a-link-for-an-odata-feed-to-use-in-power-bi) | Automatically imports dynamic, raw query data from Workplace Analytics into Power BI.<br> <br>When sharing analysis in Power BI, take caution to ensure that only authorized users can access the raw data. <br> <br>If the query is set up to auto-refresh in Workplace Analytics, your Power BI visuals will automatically update on the same schedule.|
|[Connect through the Workplace Analytics Power BI Connector](#connect-through-the-power-bi-connector) | Automatically connects Power BI to dynamic, aggregated data from within Workplace Analytics Person or Meeting queries. <br> <br>Automatically enforces data privacy by keeping the raw data in Workplace Analytics. As you create visuals in Power BI, the Connector dynamically provides the aggregated data to support them (in DirectQuery mode). <br> <br>If the query is set up to auto-refresh in Workplace Analytics, your Power BI visuals will automatically update on the same schedule. |

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

1. Next to the query you want, select the **Copy link** icon.
2. In Power BI, paste the URL into the **OData feed** dialog box.
3. Select **Organizational account** and then select **Sign in**:

   ![Sign in to Workplace Analytics organizational account](../images/wpa/use/OData-feed-sign-in.png)

4. When the **Office 365** dialog box prompts you, select the account and enter the password that you use to log in to Workplace Analytics. You'll then see: "You are currently signed in."
5. In the **OData feed** dialog box, select **Connect**. A "Refresh" dialog box might appear and display the status of the preparation of your data for import.

   After Power BI finishes importing your Workplace Analytics data, use Power BI tools to create visualizations of the data.

   > [!Important]
   > The OData link is not available for query results that were created before March 22, 2018.

   > [!Note]
   > The auto-refresh option for queries determines whether the data in the OData feed is static or dynamic:
   >   * If the URL is tied to a query that is set to auto refresh, the data in the Odata feed updates on a regular schedule. For more information, see [Auto-refresh option for queries](../tutorials/query-auto-refresh.md).
   >   * If the URL is tied to a query that is not set to auto refresh, the data in the OData feed is not automatically updated. This means that if you want new or different data, you must run a new query and get a new corresponding URL.

### Use an OData link to view data in Excel

**Role:** analyst or limited analyst

1. Go to **Workplace Analytics** > **Analyze** > **Queries** > **Results**.
2. Next to the query whose results you want to view, select the **Copy link** icon and select **Copy**:

   ![Copy OData link from query results](../images/wpa/use/odata-link-copied.png)

2. Open Excel and select **Blank workbook**.
3. In the new Excel workbook, in the **Data** menu, select **Get Data > From Other Sources > From OData Feed**:

   ![Sign in to Workplace Analytics organizational account](../images/wpa/use/data-odata-in-excel.png)

4. In Excel, paste the copied OData link into the **OData feed** dialog box and select **OK**:

   ![Paste link into Excel](../images/wpa/use/link-pasted-in-excel.png)

5. Select **Organizational account** and then select **Sign in**:
6. When the Office 365 dialog box prompts you, select the account and enter the password that you use to log in to Workplace Analytics. You'll then see: "You are currently signed in."
7. In the **OData feed** dialog box, select **Connect**. At this point, a **Refresh** dialog box might show the status of the preparation of your data for import. 

After Excel finishes importing your Workplace Analytics data, use Excel to explore and create visualizations of the data.

### Connect through the Power BI Connector

**Role:** analyst or limited analyst

The Power BI Connector automatically enforces the privacy rules configured in Workplace Analytics by providing aggregated query data in Power BI. It also automatically updates your Power BI visuals by using the same auto-refresh schedule set for the query in Workplace Analytics.  

You can connect to aggregated, auto-refreshed data from custom Person or Meeting queries in Workplace Analytics, which include the metrics and attributes that you want to dynamically analyze and visualize within Power BI.

#### Prerequisites

##### Power BI desktop

Install the latest version of Power BI Desktop:

1. Go to [PowerBI Desktop site](https://powerbi.microsoft.com/desktop/).
2. Select **Download free** and follow the online instructions to install and launch it.

##### Partition access

Partitions in Workplace Analytics allow access to specific partitions of data within Workplace Analytics. To import query data into Power BI, you need access to the partition in Workplace Analytics that contains the metrics and attributes you want to analyze in Power BI. (To gain access to that partition, use the following steps to sign in to your organizational account and select the partition ID.) <!-- For details, see [Partitions in Workplace Analytics](../setup/partitions-in-wpa.md). -->

#### Use the Power BI Connector

1. In Power BI Desktop, select **Get Data**.
2. Select **Online Services**, select **Workplace Analytics**, and then select **Connect**.
3. Locate and copy the identifier of the currently selected Workplace Analytics partition. To do this, select the user icon in the top right of the page in Workplace Analytics, select **My information**, and then highlight and copy the **Partition identifier**.

    ![My information screen](../images/wpa/use/top-right-my-info.png)

4. In **Connect to Workplace Analytics Data**, paste the copied partition identifier.

    ![Enter Workplace Analytics data connections](../images/wpa/use/pbi-wpa-connect.png)

    To import Person metrics, continue to the next step. Or to connect to a custom person or meeting query:

    * Enter one or more keywords or the complete query name in **Query Name**.
    * Or enter the query's ID in **Query Identifier**:

      a. Go to **Workplace Analytics** > **Analyze** > **Queries** > **Results**, and then select the **Copy link** icon next to the query you want to connect to in Power BI.

      b. Only highlight and copy the **32-digit ID** just before the query type at the end of the link, and then paste it into **Query Identifier** in the Power BI:

      ![Query ID](../images/wpa/use/pbi-wpa-query-id.png)

5. Select a data connectivity mode, and then select **OK**. For details, see [Use DirectQuery in Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-use-directquery).

   * **DirectQuery** (*recommended*) – As you create Power BI visuals, the Connector will provide the aggregated data to support them.  
   * **Import** – Requires you to identify how you want to aggregate the data first. That data is then imported into Power BI and from there you can create your visualizations.  

6. The first time you use the Power BI Connector for a partition ID, or when your authentication token expires, and you're prompted to sign in, select **Sign in**, enter your Office 365 credentials, and then select **Connect**:

7. In the **Power BI Navigator**, select the query name or standard person metrics that you want to analyze, and then select **Load**.

    ![Power BI Navigator](../images/wpa/use/pbi-navigator.png)

In Power BI, you can use the **Power Query Editor** to shape and combine data and create visualizations with the available fields. For details about how to use Power BI, see [Power BI documentation](https://docs.microsoft.com/power-bi/).

The following is an example of a chart that shows an organization-wide analysis of collaboration hours and meeting hours trend.

![Get Data button](../images/wpa/use/example-pbi-visual.png)

After you have finished creating visuals, you can publish your reports to Power BI online and share them with others in your organization. For more information, see [Share your Power BI dashboards and reports with coworkers and others](https://docs.microsoft.com/power-bi/service-share-dashboards).

## Related topics

* [Connect to OData feeds in Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-connect-odata)
* [Power BI templates in Workplace Analytics](../tutorials/power-bi-templates.md)
* [User roles in Workplace Analytics](../use/user-roles.md)
* [Auto-refresh option for queries](../tutorials/query-auto-refresh.md)
