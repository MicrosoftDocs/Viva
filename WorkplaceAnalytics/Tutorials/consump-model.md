---

ROBOTS: NOINDEX,NOFOLLOW
title: Consumption billing model
description: The consumption model billing model for analyst usage of queries 
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: wpa
manager: scott.ruble
audience: Admin
---

# Billing model differences

Tenants subscribe to Workplace Analytics through one of the following billing models:

* **Consumption model** &ndash; The tenant pays Microsoft a fee that is based on the volume of query usage.
* **Per-user-per-month (PUPM) model** &ndash; The tenant pays Microsoft a monthly fee that is based on the number of licensed users.

Your tenant's choice of billing model affects the appearance and behavior of the pages for creating queries (such as [person queries](person-queries.md) and [meeting queries](meeting-queries.md)) and the [query results](../use/view-download-and-export-query-results.md) page. Analysts will see the following differences:

## For analysts in consumption-model tenants

In this model, there is no minimum monthly licensing cost for your organization; rather, all fees are based on the running of queries. Each query that you run consumes a number of "units," based on the following factors:

* the number of measured employees being analyzed
* the number of weeks of data included in the query output for each measured employee
* the number of base metrics in the query
* which base metrics are used. (Metrics are arranged into "price tiers"; metrics in higher price tiers consume more units than metrics in lower price tiers. For more information, see [Consumption model details](#consumption-model-details).)

As you design a query, Workplace Analytics uses these factors to calculate the cost of the query. Within the query editor, you can see the estimated number of units that the query &ndash; in its current state &ndash; would consume. This number is updated as you edit the query:

![units per query](../images/wpa/tutorials/conmod-credits-2.png)

In the bar above the estimated query cost, you can see how many units remain in your tenant's account. Analysts can continue to run queries as long as this balance remains above zero units.

### Consumption model details

In a consumption-model tenant, queries consume "units" as they are run. Usage calculation is as follows:

**units consumed** = **A** *  **B** * **C** * **D**

The terms in this formula are as follows:

* **A = users**

   This is the number of users whom the query will analyze.

* **B = metrics**

   This is the number of unique base metrics that are used at each price tier in the query. If the query includes more than one customization of one base metric, it counts as only a single use of that metric.

  <u>Example:</u> If a query measures Meeting hours between 8:00 and 9:00 AM and Meeting hours between 9:00 and 10:00 AM, this counts as only a single metric, Meeting hours.

  A “price tier” is associated with each metric, as described in the following item.

* **C = price-tier cost**

   This is the cost of the price tier that is in use for a metric in the query. A query consumes units at this rate. The higher the tier, the more units are consumed:

   | Tier | Metric used in the query | Units |
   | ---- | ------------ | -------------- |
   | 1    | Most Workplace Analytics metrics &ndash; for example, collaboration hours, internal network size, low quality meeting hours, and 65 other basic metrics | 1.25 |
   | 2    | Advanced Workplace Analytics metrics &ndash; specifically, the [Network query metrics](../tutorials/ona-metrics.md) of Workplace Analytics. | 2.25 |
   | 3    | Workplace Analytics metrics with [CRM data](crm-queries.md) &ndash; namely, external-facing metrics that calculate across CRM contacts. If you use CRM attributes to create filter customizations for a metric (for example, the Meeting hours metric where at least one attendee has _AccountName_ = _Contoso_), the metric is in tier 3. If a single metric has more than one customization and at least one of them uses a CRM attribute, the metric is in tier 3. | 6.00 |

   >[!Note]
   >If you use metrics at multiple price tiers, a subtotal is calculated for each metric and then all subtotals are added together. For example, if your query uses one metric in each of two price tiers, the total number of units consumed is **A** * **B** * **C** * **D** (for the metric on price tier 1) + **A** * **B** * **C** * **D** (for the metric on price tier 2)

* **D = weeks**

   This is the analysis period, in weeks.

#### See the usage calculation for the query

On the query page, you can see how units are calculated for the query that you are defining. To see the calculation, select the tooltip:

![query cost tooltip](../images/wpa/tutorials/estimated-query-cost-tooltip.png)

This opens a panel that describes the current calculation:

![query cost calculation](../images/wpa/tutorials/estimated-query-cost-expanded.png)

>[!Note]
>The cost that is shown in this way is an estimate; it can vary from the query's actual cost, which can be seen after the query has been run successfully.

#### Charges for recurring queries

Workplace Analytics uses this formula to calculate the units that are consumed whenever you run a query except for recurring ([auto-refresh](query-auto-refresh.md)) queries. The first time a recurring query runs, the formula uses the actual number of user-weeks that the query definition specifies. In subsequent runs of the query, the formula automatically uses the additional time period as the query duration. You are not charged for any historical data that has already been analyzed.

Note that the queried population can change between query refresh runs. Take the following example: There are 1,000 licensed employees when you first set up a "last four weeks" auto-refresh query. Before the query runs again, another 2000 employee licenses are approved. The first time that the query refreshes after the initial run, it will include:

* **1:** weeks 2 to 4 for the original population

* **2:** week 5 for the original population

* **3:** weeks 2 to 5 for the newly licensed population

Of these, the refresh query will charge for **2** and **3** because neither were included in the original query run, but it will not charge for **1**, which duplicates the data that was returned in the original query.

#### Charges for re-running a completed query

On the **Query designer** > **Results** page, you can locate a query that has already run, open it, edit it, and run it. This incurs a new cost, as if you were running the query for the first time. The steps to do this are as follows:

1. Open the **Query designer** > **Results** page.
2. In the list of queries, find a query whose status shows as completed, as indicated by a green check mark.
3. In the row for that query, select **More options** (the ellipsis) and then **View query**:

   ![options view query](../images/wpa/tutorials/query-actions.png)

   This opens the page for designing that query.

4. In the query designer, change a detail about the query. For example, change **Group by** from **Week** to **Month**, and then select **Run**.
The edited query runs again. As it does, it incurs a new cost, in units, calculated as described in [Consumption model details](#consumption-model-details).

#### No additional charges

No additional units are charged for the following:

* Workplace Analytics licenses that are assigned. You are charged for query volume, which is independent of licensing.  
* Your use of the following Workplace Analytics features: [plans](solutionsv2-intro.md), [My Team in Viva Insights](../use/viva-insights-my-team.md), [My organization in Viva Insights](../use/viva-insights-my-org.md), [Opportunities scan](../use/solutions-scan.md), [Explore pages](../use/explore-intro.md).
* Your choice of a query-results visualization method, such as Excel, PowerPoint, Power BI, or another visualization tool.
* Your use of organizational attributes in queries.
* The number of analysts who run queries in your organization.

### Results page

The **Queries** > **Results** page shows additional information if the consumption model is in use at your tenant:

* **PUPM-model tenants** &ndash; Analysts in a PUPM-model tenant can use the **Queries** > **Results** page as described in [View, download, and export query results](../use/view-download-and-export-query-results.md).

* **Consumption-model tenants** &ndash; For analysts in a consumption-model tenant, the **Results** page shows additional information. On this page, the **Query Cost** column shows the number of units charged to each query. Select the ![More information](../images/wpa/tutorials/more-info-50.png) (more information) option to see the details of this charge, namely the number of users analyzed, the number of base metrics used, the price tier of each metric, and the analysis period:

   ![Query results page](../images/wpa/tutorials/query-results-new-col.png)

### View analyst usage

The **Analyst usage** report is available for download in the administrative pages of Workplace Analytics. This report lists the queries that were run during a specified time period, the analysts who submitted them, and other details, including the query cost:

![Analyst usage report](../images/wpa/tutorials/usage-report-example1.png)

>[!Note]
>Only admins can download the Analyst usage report.

### To download the Analyst usage report

1. Sign in to Workplace Analytics as an admin. 
2. Go to the **Analyst usage** page:

   ![Download analyst usage report](../images/wpa/tutorials/analyst-usage2.png)

3. Select the time period for which you want information about query usage.
4. Select **Download**.

<!-- publishing notes:
1. COMPLETE DOCS WILL CONTAIN EVERYTHING: TO GO LIVE ON 10/1
2. QB2 WITH ANALYST USAGE PART CAN GO LIVE NOW -->

## For analysts in PUPM-model tenants

The query-creation pages show analysts no information about query usage or tenant billing. This is because, in the PUPM model, the design and use of queries has no effect on the amount that your organization is billed. Billing charges accrue behind the scenes, independently of query usage:

![PUPM: no units shown](../images/wpa/tutorials/pupm-no-credits-2.png)

## Related topics

* [Templates](../Tutorials/Power-bi-templates.md)
* [Workplace Analytics glossary](../Use/Glossary.md)
* [Metric descriptions](../Use/Metric-definitions.md)
