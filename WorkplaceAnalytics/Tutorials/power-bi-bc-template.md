---

ROBOTS: NOINDEX,NOFOLLOW
title: Power BI template for Business Continuity
description: Use a Power BI template to run a query, export its results, and visualize them in Power BI for Business Continuity
author: madehmer
ms.author: 
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Power BI template for Business Continuity

The Business Continuity Power BI template created by the Workplace Analytics team enables you to connect to query data in Workplace Analytics, and then use it in Power BI to visualize and report about your organization's workplace patterns and trends.

This Power BI template uses the following predefined Workplace Analytics Person queries where you select the applicable chart data to show you in Power BI.

* Business Continuity
* Activity by Time of Day

## To set up and use the Power BI template

Use the following steps to use this template with the required Workplace Analytics query data.

1. Download and save the Workplace Analytics Power BI template.
2. Open [Workplace Analytics](https://workplaceanalytics.office.com/).
3. In **Queries**, run a query for each of the following predefined Person queries in the **Start from preselected filters and metrics** section:

   * Business Continuity
   * Activity by Time of Day

4. Enter or select the following for each query.

   |Query setting |Required entry or selection |
   |-------------|------------------|
   |Query Name |Name of the applicable query, Business Continuity or Activity by Time of Day|
   |Group by |Week |
   |Time Period |Custom range |
   |Auto-refresh |Select to enable |
   |Date Range | Sun, 01/05/2020 to the Latest Date Available |
   |Meeting Exclusions | Select the Tenant Default Meeting Exclusion Rule as applicable for the tenant |

    ![Business Continuity query settings](../Images/WpA/tutorials/business-continuity-query.png)

5. Optionally, you can specify additional metrics and filters for each query:

   * **Metrics** - The template automatically includes all applicable metrics. However, you can add and customize additional metrics that you want to use in Power BI. For example, collaboration levels between communities of interest and trending topics.
   * **Filters** - You can add filters to focus on specific populations of measured employees. Otherwise, it's preset to return data for all active employees within the measured population.
   * **Organizational data** - Select all or some of the Organizational Data columns to use in Power BI as pivot points or population filters. At a minimum, you must select the **Organization**, the **LevelDesignation**, and the **TimeZone**.

6. After confirming the settings, select **Run** to create the query. Repeat these steps until you've created both predefined queries.

For more details about metrics and filters available in Person queries, see [Create a Person Query](./person-queries.md).

## To analyze data in Power BI

1. 

## Related topics

[Power BI templates in Workplace Analytics](../tutorials/power-bi-templates.md)

[View, download, and export query results](../use/view-download-and-export-query-results.md)
