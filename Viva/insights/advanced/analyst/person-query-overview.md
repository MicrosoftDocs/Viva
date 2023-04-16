---
ms.date: 07/14/2022
title: Person query overview
description: Learn about custom person queries in the Microsoft Viva Insights advanced insights app
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Person query overview

## About custom person queries

The custom person query analyzes data from the point of view of each individual in the organization. This method  creates flexibility in analyzing data. For example, you can learn:

* How time use varies by different organizational attributes.
* How specific subgroups in the organization spend their time.
* How one aspect of collaboration influences other time-use habits.

:::image type="content" source="../images/person-query-diagram.png" alt-text="Screenshot that show three questions person queries can help answer":::

Each query returns one row per person, per period.

Your results include any organizational data attributes in the latest available organizational data. You can use those organizational attributes to further summarize the custom person query results and create powerful analyses that compare and contrast collaboration of different groups in the organization.

### What custom person queries do

With a custom person query, you can:

* Compare activities and attributes across the organization at the person level, like:
    * Time-use metrics.
    * Organizational attributes.
* Investigate and answer specific business questions.
* Look at data from multiple perspectives and generate powerful insights.

### When to use a custom person query

Use a custom person query when you want to find broad trends in your organization by looking at aggregated metrics for a group of people. With custom person queries, you can select as many or as few metrics as you need, for any population or time range.

### Where to find custom person queries

To access and run your own custom person queries, follow this navigation in the [advanced insights app](https://go.microsoft.com/fwlink/?linkid=2201482):

**Analysis > Custom queries > Person queries > Start analysis**

>[!Note]
>If you're an existing Viva Insights customer, refer to the note in the [Introduction](../introduction-to-advanced-insights.md) for more information about using the new platform.

### What person query results show

Person queries give you data in a clean and easy-to-use format that can take your analysis to the next level. Results show a de-identified list of each measured employee’s productivity metrics (like time in meetings and email). Each row of data represents one person, and you can select to aggregate the results by day, week, or month. You can also combine .csv output files from two different custom person queries to gain even more in-depth insights. For more information about query results, refer to [Access query results and modify existing queries](./query-results.md). 

:::image type="content" source="../images/query-csv-output.png" alt-text="Screenshot that shows person query result .csv output.":::

### How to run a custom person query

Refer to [Person query](./person-query.md) for step-by-step instructions on running a custom person query, additional guidance, and an example query.

## Time limit for querying data

The historical data on which queries are run is time limited: You can run queries only on data that is no older than 27 months. This 27-month period is a rolling window. This means that, after you have 27 months of Microsoft 365 data, as the data is refreshed each week, the 27-month extent of data that you can query advances by one week to include only the preceding 27 months.

## Business scenario

An analyst might start by looking at a custom person query to see trends of employees across the company related to meeting collaboration. Additionally, the analyst could create a query to identify the groups involved in those meetings and further investigate potential causes that could be addressed.

You can create custom queries, open and edit a query you’ve previously run, or clone a query that you or other analysts in your organization have run.

>[!Caution]
>Editing a query overwrites existing results. To keep a query’s existing results, clone it instead.

When you create a new query or edit or clone an existing query, you can select which metrics you want to include. You can also use conditions and condition groups to narrow your results and focus in on specific data.

## Videos

For a video walk-through on setting up your query, select the **Watch demo video** option above **Query setup** or navigate to the **Video demos** page through the app’s left pane.

## Related topics

[Person query](./person-query.md)

[Query results](./query-results.md)

[Metric descriptions](../reference/metrics.md)


