---

title: Organizational network analysis (ONA) person queries 
description: Describes how to use Organizational network analysis (ONA) person queries in Workplace Analytics to determine the "Influence" metric of individuals in your organization
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
manager: scott.ruble
audience: Admin
ms.prod: wpa

---

# Organizational network analysis person queries

ONA person queries help you measure connectivity within an organization. In addition to the two influence metrics ([Influence](../use/metric-definitions.md#influence-define) and [Influence rank](../use/metric-definitions.md#influence-rank-define)), ONA person queries also offer the a selection of tie metrics, starting with [Diverse ties](../use/metric-definitions.md#diverse-ties-define) and [Strong ties](../use/metric-definitions.md#strong-ties-define).  

For basic information about these connectivity metrics, see their definitions in [Workplace Analytics metrics / ONA metrics](../use/metric-definitions.md#organizational-network-analysis-ona-metrics). For deeper descriptions of the connectivity metrics, see [ONA metrics](ona-metrics.md).

## Run a query to determine ties and influence

You can use any of connectivity metrics in the ONA person query; in this example procedure, you will query for Influence or Influence rank.

**Role** - Analyst

1. In Workplace Analytics, select **Analyze** > **Queries**.
2. In **Start custom query**, select **Network: Person**:

    ![ONA person query](../images/wpa/tutorials/person-ona-query.png)

3. Select and change **Enter query name here** to a name, and then enter a description for the query.
4. For **Group by**, select a time-grouping option: **Monthly** or **Aggregated**. If you choose Monthly, the query results will contain one row with data for each month in the time period that you chose. If you choose **Aggregated**, the query results will contain one row for the entire time period that you chose.

   >[!Note]
   >Currently, the only [meeting-exclusion rule](meeting-exclusions-intro.md) that can be used with an ONA query is the [Tenant default meeting exclusion rule](meeting-exclusion-concept.md#default-meeting-exclusion-rule). As you build your query, this rule is selected by default; it cannot be deselected.

5. If you want the query to run repeatedly, on a regular schedule, select **Auto-refresh**. (For more information, see [Auto-refresh option for queries](query-auto-refresh.md).)

6.  Under **Select network boundary conditions**, define a filter to select the measured employees that you want to analyze in this query. You can use the filters of this step, for example, to narrow the scope to a division or a group. If you skip this (optional) step, all measured employees will remain eligible for analysis.

    **More information about this option:** If you run this query on the entire company, the results will be based on all collaborations across the company. If this is your goal, you can retain the default search range, which is unlimited. But your goal might be to determine only particular people, perhaps to involve them in a pilot project to introduce a new tool or procedure. In this case, limit the query to search only within a particular division or group.

7.  Under **Select collaboration types**, specify the types of collaboration activities that you want to include in your analysis. Your choices are **Emails and meetings**, **Teams instant messages**, and **Teams calls**.

    **More information about this option:** As the nature of the workplace evolves, different ways to collaborate gain or lose popularity, doing so at different rates among different populations. Some people and organizations are more formal in nature -- for example, a legal division or HR -- and they might invariably use email. They might also tend to message more recipients at once, for which they might prefer email.
    
    Other people who have a less traditional, more casual, or more personal outlook might prefer Teams IMs or calls. Analysts who study this communication can reach different inferences based on formal or informal communication. Depending on the types of change they want to make in the company, they might want to focus the analysis on one group of employees or the other.

8.  Under **Select metrics**, select one or more of the available metrics. Optionally, you can also edit the **Display name** of these metrics; the names of all selected metrics, whether or not you've edited them, will appear as column names in the query results. (Other metric customization options are not available.)

9.  Under **Select filters**, select the groups of people for whom you want to see results. For example, to query about people in the engineering department or financial division, set this filter to **Domain Equals Engineering** or **Domain Equals Finance**.

10. Under **Organizational data**, select the attributes that you want to appear in the results along with the metrics data. You can use these attributes to further summarize the results to create analyses that compare and contrast the collaboration of different groups in the organization.

11. Select **Run**. The query takes a few minutes to complete.

12. On the **Queries \> Results** page, the query status initially shows as **Submitted**. After the query status changes to **Succeeded**, you can view it or download it (as a .csv file).

>[!Note]
>You can view, copy, export, and visualize query results in different ways for different query types. The topic [View, download, and export query results](../use/view-download-and-export-query-results.md) describes how to see and share results. For example, you can [view query results](../use/view-download-and-export-query-results.md#view-query-results), [download and import query results](../use/view-download-and-export-query-results.md#download-and-import-query-results), and [use an OData feed in Power BI](../use/view-download-and-export-query-results.md#get-a-link-for-an-odata-feed-to-use-in-power-bi).

## ONA query output

The following columns are included in the query results for ONA queries:  

* **Person ID** - De-identified ID number for the person represented in that data row.
* **Date** - The start date of the aggregated output (for example, for the week of June 3rd to June 10th, the start date would be the 3rd. For a month, it's the first day of the month that your data encompasses).
* **Person attributes** - Attributes about the person supplied through the latest organizational (HR) data upload.
* **Metrics** - Any metrics that you include in the query. For more information, see [Organizational network analysis (ONA) metrics](../use/metric-definitions#organizational-network-analysis-ona-metrics).

## Related topics

* [ONA metrics](ona-metrics.md)
* [ONA person-to-person queries](ona-person-to-person-query.md)
* [Metric descriptions / ONA metrics](../use/metric-definitions.md#organizational-network-analysis-ona-metrics)
* [View, download, and export query results](../use/view-download-and-export-query-results.md)
* [Best practices for influencers](../tutorials/gm-influencer.md)
