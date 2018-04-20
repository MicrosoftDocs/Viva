---
# Metadata Sample
# required metadata

title: Use auto-update in WpA queries 
description: This topic describes the auto-update option in Workplace Analytics queries.     
author: paul9955
ms.author: v-pascha
ms.date: 04/20/2018
ms.topic: get-started-article
ms.prod: wpa
---

# Auto-update option for queries

## One-time queries show you a snapshot

As an analyst, you can run different kinds of queries, including person, meeting, and group queries. You start creating the query by applying a date filter and choosing the query type.

You can run queries as a one-time event: You set it up, run it once, and obtain the results. To visualize workplace patterns uncovered by this query, you can load the results into a data-visualization tool such as Microsoft Power BI. This presents you with views into a snapshot of workplace behavior. 

## Auto-update shows you trends over time

Query results, especially when viewed in a visualization tool, can uncover dynamic patterns. These patterns evolve over time because the workplace behavior of employees evolves over time. To isolate one instance of workplace behavior over time, use the appropriate query not once but on a regular basis. Do this by using the Auto-update feature of Workplace Analytics. 

## Create an auto-update query

[!INCLUDE [To create an auto-update query](../../Includes/to-create-auto-update-query.md)]

## Behavior of an auto-update query

 * When the query runs for the first time, it uses data from the exact date range that you defined.
 * The query automatically runs again, once per week. These subsequent runs coincide with the date on Workplace Analytics refreshes the mail and calendar data that it obtains from Microsoft Exchange. 
 * The query will run for an indefinite period of time, or until you return to this page and clear the Auto update option. 

## Viewing the results of an auto-update query

When you open the Results page to see your results, you see the results of the latest weekly run of this query. Workplace Analytics displays an icon that indicates that this is an Auto-update query. It also displays the most recent date on which the query ran, so that you know how new the results are. 

## Visualizing the results of an auto-update query

When you open the Queries page, you can copy a link by clicking the link icon. You can then paste this link into Power BI. After you do this, Power BI makes use of a connection to this query in Workplace Analytics.

Subsequently, to visualize the query's current results, open the Workplace Analytics project in Power BI and click Refresh. 
