---

ROBOTS: NOINDEX,NOFOLLOW
title: Business Continuity Dashboard in Power BI
description: Use the Power BI template to run a query, export its results, and visualize the data in the Business Continuity Dashboard in Power BI
author: madehmer
ms.author: 
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Business Continuity Dashboard in Power BI

The Business Continuity Dashboard in Power BI helps answer questions about how your organization is adapting to suddenly having a significant portion or all of your employees working remotely.

Workplace Analytics uses Office 365 data activity to provide real-time, behavioral data about how your company is adapting and evolving to meet challenges associated with a move to remote work.  disruption, such as 100 percent remote work (maybe for the first time ever), work-from-home requirements, social isolation, and school closures.


* Introduction to using behavioral data in near real time to understand how the organization is adapting and evolving to meet new challenges associated with a move to remote work
* Highlight of metrics that indicate how business has been responding to these changes. Each of these metric cards can be clicked through to show additional detail


The top-level business questions asked by leaders and analysts include the following.

|Business question |Analysis |
|-------------|------------------|
|Is business running as usual? |<ul><li>High-level overview of community activity level spanning before and after the disruption </li><li>Trendline of activity </li></ul>|
|What is being disrupted? |<ul><li>Engagement with customers and suppliers </li><li>Cross-functional teaming and partnering </li></ul>|
|How are employees adapting to the disruption?  |<ul><li>Activity shifts throughout a work day or week, including: Activity by time of day, After-hours, and Workweek span </li><li>Channels used to replace in-person connections </li></ul>|
|How do you foster employee community and engagement? |<ul><li>Employees who've lost connection points with their manager </li><li>Meaningful connection points within informal interactions </li></ul>|

The template enables you to connect query data in Workplace Analytics to Power BI, and then use it in the Business Continuity Dashboard to visualize and report about your organization's workplace patterns and trends.

This Power BI template uses the following predefined Workplace Analytics Person queries where you select the applicable chart data to use in Power BI.

* Business Continuity
* Activity by Time of Day

## To set up 

Use the following steps to download the template and generate the Workplace Analytics query data that's required to populate the Business Continuity dashboard in Power BI.

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

6. After confirming the settings, select **Run** to run the query. Repeat these steps to create the **Activity by Time of Day** query.
7. After the queries successfully run and their status shows as a green check mark, continue to the next step to connect the query data to Power BI.

For more details about metrics and filters available for Person queries, see [Create a Person Query](./person-queries.md).

## To connect query data to Power BI

1. Open the Power BI template for Business Continuity that you downloaded in the previous steps.
2. When prompted for the OData URL, go to Workplace Analytics **Queries** > **Results**, select the **link** icon for the **Business Continuity** query results (with a green check mark status), and then select **Copy**.
3. In the Power BI **Business Continuity Dashboard** prompt, paste the query results link, and then select **Load**.
4. When prompted to **Sign in** in Power BI, enter your **Workplace Analytics login credentials** to connect to the query results.
5. If prompted to sign in to your account, select **Organization Account**, enter your **Microsoft Office 365 credentials** that you use to access Workplace Analytics, then select **Connect**.
6. Repeat these steps for the **Activity by Time of Day** query results.

## To analyze data in Power BI



## Related topics

[Power BI templates in Workplace Analytics](../tutorials/power-bi-templates.md)

[View, download, and export query results](../use/view-download-and-export-query-results.md)
