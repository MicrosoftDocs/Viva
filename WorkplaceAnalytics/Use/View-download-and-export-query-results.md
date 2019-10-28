---
# Metadata Sample
# required metadata

title: View, download, and export Workplace Analytics query results
description: Describes how to view, download, and export Workplace Analytics query results to PowerBI and other data analysis tools
author: paul9955
ms.author: v-midehm
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# View, download, and export query results

* **Role:** Analyst. You must have the analyst role in Workplace Analytics to view, download, or export query results.
  
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
| [Connect through the PowerBI-Workplace Analytics connector](#connect-through-the-powerbi-workplace-analytics-connector) | Visualize data within Power BI by running aggregated queries on standard person metrics. This option does _not_ start with query results that Workplace Analytics has produced. |

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

* **Role:** analyst or limited analyst

The Power BI-Workplace Analytics connector lets you construct visualizations of data from Workplace Analytics while you are running Power BI. Use it to build insights in Power BI by importing out-of-the-box metrics and person attributes from Workplace Analytics. The Connector automatically enforces the privacy rules that were configured by the organization's Workplace Analytics admin and guarantees the freshness of any visualized data.

> [!Note] 
> The Power BI-Workplace Analytics connector does not use results of already-run queries. Instead, it creates Power BI visualizations by running aggregated queries of Workplace Analytics data on standard [Person metrics](metric-definitions.md#person-metrics). (Aggregated queries include groupings of metrics on one or more columns of organizational-data attributes, with aggregations such as Sum, Average, Min, and Max on the metric columns.)

#### Prerequisites

##### Power BI desktop

To make this connection, you first need to download Power BI desktop. Follow these steps:

1. Open the [PowerBI Desktop site](https://powerbi.microsoft.com/desktop/). 
2. Select **Download free**. If a dialog box asks "Open Microsoft Store?", select **Open Microsoft Store**.
3. In the Microsoft Store app, select **Get**. Power BI is then downloaded to your device and automatically installed. 
4. Select **Launch**. Power BI opens. 

##### Partition access

Partitions in Workplace Analytics allow access to data. To import metrics and attributes into Power BI, you will need access to the partition in Workplace Analytics that contains those metrics and attributes. (To gain access to that partition, you will follow steps in the following procedure that have you sign in to your organizational account and select the partition ID.) For more information, see [User roles in Workplace Analytics](../use/user-roles.md). 

#### Use the connector

1.	In Power BI Desktop, select the **Get Data** button:

    ![Get Data button](../images/wpa/use/get-data-in-pbi.png)

2.	Select **Online Services**, select **Workplace Analytics**, and then select **Connect**:

    ![Get Data button](../images/wpa/use/get_data_screen.png)

3.  Determine the identifier of the currently selected Workplace Analytics partition. To do this, select the user icon in the top right corner of the page, and then select **My information**:

    ![My information screen](../images/wpa/use/top-right-my-info.png)

    Next, find the partition identifier in the **My information** dialog box: 
       
    ![My information screen](../images/wpa/use/my-information.png)

4.	Enter the partition identifier:

    ![Enter partition ID](../images/wpa/use/connect_to_wpa_part_id.png)

5.	Select the data connectivity mode that you'd like to use: **Direct Query** (recommended) or **Import**. For more information about this choice, see [Use DirectQuery in Power BI Desktop](https://docs.microsoft.com/en-us/power-bi/desktop-use-directquery).

    ![Select Direct Query or Import](../images/wpa/use/connect_to_wpa_mode.png)

6.  Select **OK**.    
 
7.	The first time that you use the PowerBI-Workplace Analytics connector for a particular partition ID, and again later, after your authentication token expires, you will be prompted that "you aren't signed in":

    ![Not signed in](../images/wpa/use/wpa_select_authentication.png)

    When you see this prompt, select **Sign in** and then provide your Office 365 credentials:

    ![Sign in](../images/wpa/use/login-to-o365_2.png)

8.	At this point, if the connection is a success, Power BI displays a list of metrics and attributes in the **Fields** section. This list could resemble the following:

    ![Metrics](../images/wpa/use/list-of-metrics-2-col_2.png)

In Power BI, you can now create visualizations using those fields.

For example, you can generate a bar chart that shows an organization-wide analysis of collaboration hours or examines the meeting-hours trend for an entire organization.

![Get Data button](../images/wpa/use/example-pbi-visual.png)

After you have finished creating visualizations, you can publish your reports to Power BI online and share them with others in your organization. For more information, see [Share your Power BI dashboards and reports with coworkers and others](https://docs.microsoft.com/en-us/power-bi/service-share-dashboards). 

## Related topics

[Connect to OData feeds in Power BI Desktop](https://docs.microsoft.com/en-us/power-bi/desktop-connect-odata) 

[Power BI templates in Workplace Analytics](../tutorials/power-bi-templates.md)

[User roles in Workplace Analytics](../use/user-roles.md)

[Auto-refresh option for queries](../tutorials/query-auto-refresh.md)

[Share your Power BI dashboards and reports with coworkers and others](https://docs.microsoft.com/en-us/power-bi/service-share-dashboards)
