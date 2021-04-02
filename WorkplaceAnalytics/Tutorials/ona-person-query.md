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

It's frequently necessary to implement changes within organizations, whether this be introducing new procedures or rolling out new systems or technology. The traditional top-down method of using formal authority to drive change – perhaps starting with mass emails – it’s not always the most effective way. It might fail for any of several reasons including company culture, technical challenges, or problems with personality.

Instead, a more successful strategy uses change agents, who are influential, well-connected people in different levels of your company, not just at the top. Beyond an organization’s formal hierarchy, are informal networks of people who can exert influence within those networks and between them. The most influential people have large personal networks with above-average numbers of relationships with their colleagues.

Therefore, to help implement change, it pays to know who the influencers are. The Workplace Analytics Organizational network analysis (ONA) queries were designed for this purpose. They can help you find out who the best-connected people are in the company based on their collaboration characteristics.

This query type lets analysts use two related metrics:

* [Influence](../use/metric-definitions.md#influence-define) - This metric is a score of how well connected you are in the company. It acts recursively: if you’re connected to others who are well connected, you benefit from their connections as well.
* [Influence rank](../use/metric-definitions.md#influence-rank-define) - This metric indicates where influencers stand among other influencers. A rank of 1 represents the person with the greatest Influence score; a rank of 2 represents the person with the next greatest Influence score, and so on.

After you learn who the best connected people are in the company, division, or other group, you can act on the likelihood that these people can effectively connect within or across groups and become efficient drivers of change.

Also see [How Workplace Analytics calculates influence](#how-workplace-analytics-calculates-influence).

## Run a query to determine Influence

**Role** - Analyst

1. In Workplace Analytics, select **Analyze** > **Queries**.
2. In **Start custom query**, select **Network: Person**:

    ![ONA person query](../images/wpa/tutorials/person-ona-query.png)

3. Select and change **Enter query name here** to a name, and then enter a description for the query.
4. For **Group by**, select a time-grouping option: **Monthly** or **Aggregated**. If you choose Monthly, the query results will contain one row with data for each month in the time period that you chose. If you choose **Aggregated**, the query results will contain one row for the entire time period that you chose.

   >[!Note]
   >Currently, the only [meeting-exclusion rule](meeting-exclusions-intro.md) that can be used with an ONA query is the [Tenant default meeting exclusion rule](meeting-exclusion-concept.md#default-meeting-exclusion-rule). As you build your query, this rule is selected by default; it cannot be deselected.

5. If you want the query to run repeatedly, on a regular schedule, select **Auto-refresh**. (For more information, see [Auto-refresh option for queries](query-auto-refresh.md).) 
6. Under **Select metrics**, select **Influence** and/or **Influence rank**. Optionally, you can also edit the **Display name** of these metrics; the names of all selected metrics, whether or not you've edited them, will appear as column names in the query results. (Other metric customization options are not available.)
7. Under **Select filters**, select the groups of people for whom you want to see results. For example, to query about people in the engineering department or financial division, set this filter to **Domain Equals Engineering** or **Domain Equals Finance**.
8. Under **Organizational data**, select the attributes that you want to appear in the results along with the metrics data. You can use these attributes to further summarize the results to create analyses that compare and contrast the collaboration of different groups in the organization.
9. Select **Run**. The query takes a few minutes to complete.
10. On the **Queries > Results** page, the query status initially shows as **Submitted**. After the query status changes to **Succeeded**, you can view it or download it (as a .csv file).

>[!Note]
>You can view, copy, export, and visualize query results in different ways for different query types. The topic [View, download, and export query results](../use/view-download-and-export-query-results.md) describes how to see and share results. For example, you can [view query results](../use/view-download-and-export-query-results.md#view-query-results), [download and import query results](../use/view-download-and-export-query-results.md#download-and-import-query-results), and [use an OData feed in Power BI](../use/view-download-and-export-query-results.md#get-a-link-for-an-odata-feed-to-use-in-power-bi).

## ONA query output

The following columns are included in the query results for ONA queries:  

* **Person ID** - De-identified ID number for the person represented in that data row.
* **Date** - The start date of the aggregated output (for example, for the week of June 3rd to June 10th, the start date would be the 3rd. For a month, it's the first day of the month that your data encompasses).
* **Person attributes** - Attributes about the person supplied through the latest organizational (HR) data upload.
* **Metrics** - Any metrics that you include in the query. For more information, see [Influence](../use/metric-definitions.md#influence-define) and [Influence rank](../use/metric-definitions.md#influence-rank-define).

## How Workplace Analytics calculates influence

The terminology in the following description comes from graph theory. In graph theory, a "node" (also called a "vertex") is an object that can relate to other nodes -- other objects -- in the graph. This model becomes useful when we extend it to the workplace, where a "node" represents a person who has connections to co-workers and others.  

Influence indicates a node's potential influence on opinions of the network or an estimate of social status. Essentially, it uses the number and strength of connections coming into a node to rank the nodes. The values are between 0 and 1.

### Determine node rank

The most meaningful information to glean from Influence is the rank of the nodes. You can do this by using either of the two pertinent ONA metrics, Influence and Influence rank.

* Use [Influence rank](../use/metric-definitions.md#influence-rank-define). This metric assigns to each node a number that corresponds to their relative influence, with the lowest number (1) for the most influential node. You can use this metric, for example, to obtain a simple ranked list or to evaluate whether a node's network influence is changing over time.

* Use [Influence](../use/metric-definitions.md#influence-define). You use this metric in a more nuanced way than you'd use Influence rank. For example, assume that node A has an Influence of 0.6 and node B has an Influence of 0.3. You can accurately assume that node A is a more influential than node B, because node A ranks higher than node B. However, you cannot assume node A is twice as influential as node B because the values indicate a ranking or source of influence, not the amount of influence. The calculations for Influence use the relative collaboration time between individuals as the strengths of the connections for a person's influence measure.

## Related topics

* [ONA person-to-person queries](ona-person-to-person-query.md)
* [Metric descriptions / ONA metrics](../use/metric-definitions.md#organizational-network-analysis-ona-metrics)
* [View, download, and export query results](../use/view-download-and-export-query-results.md)
* [Best practices for influencers](../tutorials/gm-influencer.md)
