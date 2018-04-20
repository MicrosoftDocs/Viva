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

As an analyst, you can run different kinds of queries in Workplace Analytics, including person, meeting, and group queries. You start creating the query by applying a date filter and choosing the query type.

You can run a query as a one-time event: You set it up, run it once, and obtain the results. To visualize workplace patterns uncovered by this query, you can load the results into a data-visualization tool such as Microsoft Power BI. This presents you with views into a snapshot of workplace behavior. 

## Auto-update shows you trends over time

Query results, especially when viewed in a visualization tool, can uncover dynamic patterns. These patterns evolve over time because the workplace behavior of employees evolves over time. To isolate one instance of evolving workplace behavior over time, use the appropriate query not once but on a regular basis. You can do this by using the auto-update feature of Workplace Analytics. 

## Create an auto-update query

[!INCLUDE [To create an auto-update query](../Includes/to-create-auto-update-query.md)]

## Behavior of an auto-update query

 * When the query runs for the first time, it uses data from the exact date range that you defined.
 * The query automatically runs again, once every week. Each run coincides with the date on which Workplace Analytics refreshes mail and calendar data from Microsoft Exchange. 
 * Each time the query runs automatically, its date range advances by one week. That is, its start date becomes one week later and its end date also becomes one week later.  
 * Workplace Analytics will run the auto-update query on its weekly schedule, indefinitely.

## Obtain the results of an auto-update query

1. On the Queries page of Workplace Analytics, click **Results**.  
2. In the table of results, find your query. 

For an auto-update query, the Results page shows the following: 

 * The results of the _latest_ weekly run.
 * The date on which it ran. This shows how recently these results were obtained. 
 * An icon that indicates it to be an auto-update query.

## Visualize the results in Power BI

On the Results page, you can obtain a link to a query's results and then use this link in Power BI. 

1. At the right end of the query's row, click **Copy link**:

   <img src="../Images/WpA/Tutorials/Get-results-link.png" alt="Copy a query's results link">

2. Click **Copy**. the Get results link displays the word "Copied." 
3. In Power BI, on the Home tab, click **Get Data** and then click **OData feed**.
4. In the OData feed dialog box, paste the link that you copied into the URL field:

   <img src="../Images/WpA/Tutorials/OData-feed.png" alt="OData feed in Power BI">

5. Click **OK**.
6. Enter your client credentials and then click **Connect**.

After you do this, Power BI maintains a connection to this query in Workplace Analytics. In the future, to visualize the query's current results, open the Workplace Analytics project in Power BI and click **Refresh**. 
