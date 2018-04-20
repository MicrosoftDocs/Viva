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

# The auto-update option

Analysts can run different kinds of queries, such as person queries. To do this, they start by applying a date filter. They then choose the query type.

Until now, queries were a one-time operation: you ran it, you got your results, and you were done. To visualize workplace patterns uncovered by this query, you could then take these query results, load them into Power BI. The query presented you with a snapshot of workplace behavior. 

But customers have expressed the need to see more than a snapshot, to see trends over time, to be able to easily reuse a query that they’ve spent time setting up and running. This is because query results, especially when viewed in Power BI, can show analysts patterns that are not static. These patterns evolve over time as the workplace behavior of employees evolves over time. 
We are therefore introducing the feature called Auto update results.

By using this feature, analysts can check a box to request that their query results get automatically updated on a regular basis. This regular period is defined as one week.

While you are creating your query, you define a time range of one, three, six, or twelve months. In addition to selecting a time range, you can now select Auto update.
When the query first runs, it uses data from the exact date range that you defined. You know the start and end dates. 

<img src="../Images/WpA/Tutorials/auto-update.PNG" alt="Setting auto-update for a Workplace Analytics query">

But this isn’t the end of the story for your query if you picked Auto update.

The query will automatically run again without your having to launch it again. Workplace Analytics will continue to re-run it every week. Its run coincides with the time that Workplace Analytics refreshes its mail and calendar data from Microsoft Exchange. 

It will run for an indefinite period of time, or until you deselect Auto update. 

When you view the Results page to see your results, you always see the results of the latest run. Workplace Analytics displays the date on which it last ran this query, so you can always see how up to date your results are. 

When you view the Queries page, you can copy a link by clicking the link icon. You can then paste this link into Power BI. After you do this, Power BI is aware of the connection to Workplace Analytics and to this automatic query. This means that, to visualize this data in Power BI and know that you are seeing the most current information – the results of the most recent automatic query run – all you need to do in Power BI is click update when you have the Workplace Analytics project open. 

