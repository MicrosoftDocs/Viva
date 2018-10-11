---
# Metadata Sample
# required metadata

title: Use the auto-refresh option for queries in Workplace Analytics 
description: This topic describes the auto-refresh option in Workplace Analytics queries.     
author: paul9955
ms.author: v-pascha
ms.date: 10/11/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Auto-refresh option for queries

## One-time queries show you a snapshot

As an analyst, you can run different kinds of queries in Workplace Analytics, including person, meeting, and group queries. You start creating the query by choosing the query type and applying a date filter.

You can run a query as a one-time event: You set it up, run it once, and obtain the results. To visualize workplace patterns uncovered by this query, you can load the results into a data-visualization tool such as Microsoft Power BI. This presents you with views into a snapshot of workplace behavior. 

## Auto-refresh shows you trends over time

Query results, especially when viewed in a visualization tool, can uncover dynamic patterns. These patterns evolve over time because the workplace behavior of employees evolves over time. To isolate one instance of evolving workplace behavior over time, use the appropriate query not once but multiple times -- or even better, on a regular schedule. You can do this by using the auto-refresh feature of Workplace Analytics. 

## Create an auto-refresh query

[!INCLUDE [To create an auto-refresh query](../Includes/to-create-auto-refresh-query.md)]

## Behavior of an auto-refresh query

 * When you create the query, you run it for the first time. As it runs, it uses data from the exact date range that you defined.
 * The query automatically runs again, once every week. Each run coincides with the date on which Workplace Analytics refreshes mail and calendar data from Microsoft Exchange. 
 * Each time the query runs automatically, its date range advances by one week. That is, its start date becomes one week later and its end date also becomes one week later.  
 * Workplace Analytics runs the auto-refresh query on this weekly schedule for one year.

## Obtain the results of an auto-refresh query

1. On the Queries page of Workplace Analytics, click **Results**.  
2. In the table of results, find your query. 

For an auto-refresh query, the Results page shows the following: 

 * The results (a .csv file) of the _latest_ weekly run. Click **Download** to download an archived file of the results. 
 * The date on which the query last ran.  
 * An icon that indicates it to be an auto-refresh query.

## Visualize the results in Power BI

On the Results page of Workplace Analytics, you can also obtain a link to a query's results and then use this link in Power BI. 

1. At the right end of the query's row, click **Copy link**:

   <img src="../Images/WpA/Tutorials/Get-results-link.png" alt="Copy a query's results link">

2. Click **Copy**. The Get results link dialog box displays the word "Copied." 
3. In Power BI, on the Home tab, click **Get Data** and then click **OData feed**.
4. In the OData feed dialog box, paste into the URL field the link that you copied:

   <img src="../Images/WpA/Tutorials/OData-feed.png" alt="OData feed in Power BI">

5. Click **OK**.
6. Enter your client credentials and then click **Connect**.

After you do this, Power BI maintains a connection to this query in Workplace Analytics. In the future, to visualize the query's current results, open the Workplace Analytics project in Power BI and click **Refresh**. 

### Related topics

[View, download, and export query results](../use/view-download-and-export-query-results.md)