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
 * The query automatically runs again, once per week. Each of these runs coincides with the date on Workplace Analytics refreshes mail and calendar data from Microsoft Exchange. 
 * Each time the query runs automatically, its date range advances by one week. That is, its start date becomes one week later and its end date becomes one week later.  
 * Automatic query runs will repeat indefinitely, or until you return to this page and clear the auto-update option or delete the query. 

## Viewing the results of an auto-update query

When you open the Results page to see your results, you see the results of the latest weekly run of this query. Workplace Analytics displays an icon that indicates that this is an auto-update query. It also displays the most recent date on which the query ran, so that you know how new the results are. 

## Visualizing the results of an auto-update query

When you open the Queries page, you can copy a link by clicking the link icon. You can then paste this link into Power BI. After you do this, Power BI makes use of a connection to this query in Workplace Analytics.

Subsequently, to visualize the query's current results, open the Workplace Analytics project in Power BI and click Refresh. 
