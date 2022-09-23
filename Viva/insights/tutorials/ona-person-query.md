---
ROBOTS: NOINDEX,NOFOLLOW
title: Network person queries 
description: Describes how to use Network person queries in Viva Insights to determine the Influence metric of individuals in your organization
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
manager: scott.ruble
audience: Admin
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 

---

# Network person queries

Network person queries help you measure connectivity within an organization. In addition to the two influence metrics ([Influence](../use/metric-definitions.md#influence-define) and [Influence rank](../use/metric-definitions.md#influence-rank-define)), Network person queries also offer the a selection of tie metrics, starting with [Diverse ties](../use/metric-definitions.md#diverse-ties-define) and [Strong ties](../use/metric-definitions.md#strong-ties-define).  

For basic information about these connectivity metrics, see their definitions in [Network metrics](../use/metric-definitions.md#network-metrics). For deeper descriptions of the connectivity metrics, see [Network metrics](ona-metrics.md).

## Run a query to determine ties and influence

You can use any of connectivity metrics in the Network person query. In the following example steps, you will query for Influence or Influence rank.

**Role** - Analyst

1. In the advanced insights app, select **Analyze** > **Query designer**, and then select **Get started** under **Query**.
2. Select **Network: Person**.
3. Select **Enter query name here** and name this query, and then enter a description for it.
4. For **Group by**, select a time-grouping option: **Monthly** or **Aggregated**. If you choose Monthly, the query results will contain one row with data for each month in the time period that you chose. If you choose **Aggregated**, the query results will contain one row for the entire time period that you chose.

   >[!Note]
   >Currently, the only [meeting-exclusion rule](meeting-exclusions-intro.md) that can be used with a Network query is the [Tenant default meeting exclusion rule](meeting-exclusion-concept.md#default-meeting-exclusion-rule). As you build your query, this rule is selected by default; it cannot be deselected.

5. If you want the query to run repeatedly, on a regular schedule, select **Auto-refresh**. (For more information, see [Auto-refresh option for queries](query-auto-refresh.md).)

6. Under **Select network boundary conditions**, define a filter to select the measured employees that you want to analyze in this query. You can use the filters of this step, for example, to narrow the scope to a division or a group. If you skip this (optional) step, all measured employees will remain eligible for analysis.

    **More information about this option:** If you run this query on the entire company, the results will be based on all collaborations across the company. If this is your goal, you can retain the default search range, which is unlimited. But your goal might be to determine only particular people, perhaps to involve them in a pilot project to introduce a new tool or procedure. In this case, limit the query to search only within a particular division or group.

7. Under **Select collaboration types**, specify the types of collaboration activities that you want to include in your analysis. Your choices are **Emails and meetings**, **Teams instant messages**, and **Teams calls**. (The **Emails and meetings** option is mandatory and cannot be deselected.)

    **More information about this option:** As the nature of the workplace evolves, different ways to collaborate gain or lose popularity, doing so at different rates among different populations. Some people and organizations are more formal in nature &ndash; for example, a legal division or HR &ndash; and they might invariably use email. Also, they might tend to message multiple recipients at the same time, for which they might prefer email.

    Other people who have a less traditional, more casual, or more personal outlook might prefer Teams IMs or calls. Analysts who study this communication can reach different inferences based on formal or informal communication. Depending on the types of change they want to make in the company, they might want to focus the analysis on one group of employees or the other.

8. Under **Select metrics**, select one or more of the available metrics. Optionally, you can also edit the **Display name** of these metrics; the names of all selected metrics, whether or not you've edited them, will appear as column names in the query results. (Other metric customization options are not available.)

9. Under **Select filters**, select the groups of people for whom you want to see results. For example, to query about people in the engineering department or financial division, set this filter to **Domain Equals Engineering** or **Domain Equals Finance**.

10. Under **Organizational data**, select the attributes that you want to appear in the results along with the metrics data. You can use these attributes to further summarize the results to create analyses that compare and contrast the collaboration of different groups in the organization.

11. Select **Run**. The query takes a few minutes to complete.

12. In **Query designer** > **Results**, the query status initially shows as **Submitted**. After the query status changes to **Succeeded**, you can view it or download it (as a .csv file).

>[!Note]
>You can view, copy, export, and visualize query results in different ways for different query types. The topic [View, download, and export query results](../use/view-download-and-export-query-results.md) describes how to see and share results. For example, you can [view query results](../use/view-download-and-export-query-results.md#view-query-results), [download and import query results](../use/view-download-and-export-query-results.md#download-and-import-query-results), and [use an OData feed in Power BI](../use/view-download-and-export-query-results.md#get-a-link-for-an-odata-feed-to-use-in-power-bi).

## Network query output

The following columns are included in the query results for Network queries:  

* **Person ID** - De-identified ID number for the person represented in that data row.
* **Date** - The start date of the aggregated output (for example, for the week of June 3rd to June 10th, the start date would be the 3rd. For a month, it's the first day of the month that your data encompasses).
* **Person attributes** - Attributes about the person supplied through the latest organizational (HR) data upload.
* **Metrics** - Any metrics that you include in the query. For more information, see [Network metrics](../use/metric-definitions.md#network-metrics).

## Related topics

* [Network metrics](ona-metrics.md)
* [Network person-to-person queries](ona-person-to-person-query.md)
* [Network metric definitions](../use/metric-definitions.md#network-metrics)
* [View, download, and export query results](../use/view-download-and-export-query-results.md)
* [Best practices for influencers](../tutorials/gm-influencer.md)
