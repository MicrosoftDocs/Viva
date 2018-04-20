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

Query results, especially when viewed in a visualization tool, can uncover dynamic patterns. These patterns evolve over time because the workplace behavior of employees evolves over time. To isolate one instance of evolving workplace behavior over time, use the appropriate query not once but on a regular basis. Do this by using the Auto-update feature of Workplace Analytics. 

## Create an auto-update query

[!INCLUDE [To create an auto-update query](../Includes/to-create-auto-update-query.md)]

## Behavior of an auto-update query

 * When the query runs for the first time, it uses data from the exact date range that you defined.
 * The query automatically runs again, once per week. Each run coincides with the date on which Workplace Analytics refreshes mail and calendar data from Microsoft Exchange. 
 * Each time the query runs automatically, its date range advances by one week. That is, its start date becomes one week later and its end date also becomes one week later.  
 * Automatic query runs will repeat indefinitely, or until you return to this page and clear the auto-update option or delete the query. 

## View the results of an auto-update query

1. On the Queries page of Workplace Analytics, click **Results**.  
2. In the table of results, find your query. 

For an auto-update query the Results page shows the following: 

 * The results of the latest weekly run.
 * The date on which it ran. This lets you know how recently the results were obtained. 
 * An icon that indicates it to be an auto-update query.

## Visualize the results of an auto-update query

On the Results page, you can copy a link by clicking the link icon at the end of the query's row. You can then paste this link into Power BI. 

After you do this, Power BI maintains a connection to this query in Workplace Analytics. In the future, to visualize the query's current results, open the Workplace Analytics project in Power BI and click **Refresh**. 
