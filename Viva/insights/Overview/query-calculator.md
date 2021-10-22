---

title: Query calculator for Viva Insights
description: Use the Query cost predictor in Microsoft Viva Insights
author: madehmer
ms.author: v-mideh
ms.topic: article
ms.localizationpriority: medium 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin

---

# Query cost predictor

The Microsoft Viva Insights in Workplace Analytics app gives analysts access to the Query designer. However, by using the Query designer to get query results used for advanced analysis, you might want to use this Query cost predictor to confirm what analysis you’d like analysts to create for your organization before queries are run in the Query designer.

With the [Consumption model in Viva Insights](../tutorials/consump-model.md), when you run a query, it consumes a few "units" based on the following factors:

* The number of measured employees included in the analysis
* The number of weeks of data included in the query output for each measured employee
* The number of metrics used in the query or Power BI template
* The type of metrics used from the different price tiers; metrics in the higher price tiers consume more units than metrics in lower price tiers

As an analyst, when you design a query, Viva Insights uses these factors to calculate the cost of the query. Power BI templates are built on top of queries. You must run one or more queries and provide the query results from one or more successfully completed queries to use with a Power BI template.
The Query cost predictor can help you get an estimated cost of running queries and using them with Power BI templates.

## Power BI template estimate

1. Open the Query cost predictor.
2. In **Power BI templates**, select the following details, and then select **Calculate** to get an estimate:

   * Name of the Power BI template
   * Time period for the analysis
   * Number of measured employees to include in the analysis

The following example shows the cost of running the queries required for the Business continuity template, for the last month, and for 15 employees. 

![Power BI template cost estimate example.](../images/wpa/overview/qcost-example.png)

## Query estimate

1. Open the Query cost predictor.
2. In Query types, select the following details, and then select Calculate to get an estimate:

   * Type of query, such as a Person or Meeting query
   * Metrics to include in the analysis
   * Time period for the analysis
   * Number of measured employees to include in the analysis

The following example shows the cost of running a person query with three metrics, for the last three months, for 1,000 employees.

![Query cost estimate example.](../images/wpa/overview/qcost-example-2.png)
