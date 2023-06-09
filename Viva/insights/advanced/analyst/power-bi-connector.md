---
ms.date: 06/09/2023
title: Use the Power BI connector
description: Learn how to connect your Viva Insights data to Power BI through the Power BI connector
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

# Connect through the Power BI Connector

To connect your Viva Insights data to Power BI through the [Power BI connector](/connectors/powerbi/), follow these steps:

1. In Power BI Desktop:
    1. Select **Get Data** in the ribbon.
    1. In the **Get Data** window, select **Online Services** from the left navigation.
    1. Select **Viva Insights**. 
    1. Select the **Connect** button.
    1. Select **Continue** if you see a **Connecting to a third-party service** dialog box.
1. In the advanced insights app:
    1. Go to **Analyst > Query results**.
    1. Find your query.
    1. Select **Link** to get the partition and query identifiers.
1. In Power BI Desktop's **Connect to Viva Insights Data** window:
    1. Enter the partition identifier.
        >[!Note]
        >Query name isn't supported right now.
    1. Enter the query identifier.
    1. Set advanced parameters (optional).
        1. In Schema type, select:
            1. **Pivoted (Default)** to load organizational attributes as individual columns. Here's an example of how your results would load with this option:
            
            |PersonId|MetricDate|Collaboration hours|Organization|SupervisorIndicator|
            |---------|---------|--------|------|--------|
            |A|5/7/2023|23.6|Finance|Manager|

            2. **Unpivoted** to load organizational attributes as key-value pairs. Here's an example of how your results would load with this option:
            
            |PersonId|MetricDate|Collaboration hours|AttributeName|AttributeValue|
            |---------|---------|--------|------|--------|
            |A|5/7/2023|23.6|Organization|Finance|
            |A|5/7/2023|23.6|SupervisorIndicator|Manager|


    1. In Data granularity, select:
        1. **Aggregated data (default)** to push queries to the Viva Insights service to get aggregated results in Power BI. 
        1. **Row-level data** to load the raw query results into Power BI.  
        >[!Note] 
        >Learn more about aggregated and row-level data later, in [About data granularity and data connectivity mode](#about-data-granularity-and-data-connectivity-modes). 
    2. Select a **Data connectivity** mode: 
        1. **Import** – This mode brings a copy of your query results into Power BI Desktop. As you create or interact with visualizations, Power BI Desktop uses these copied results. To see underlying data changes after the initial import or the most recent refresh, you'll need to import the full dataset again to refresh the data. 
        1. **DirectQuery** – This mode doesn't import any query results into Power BI Desktop. You can select columns to appear in the Power BI Desktop **Fields** list. As you create or interact with visualizations, Power BI Desktop uses your results as they appear in Viva Insights, so you're always viewing current data. 
        >[!Note] 
        >Learn more about these modes later, in [About data granularity and data connectivity mode](#about-data-granularity-and-data-connectivity-modes). 
    1. Select **OK**. 
1.	If you're prompted to sign in, select **Sign in**. Then, enter your credentials and select **Connect**. 
1. In the preview window, select **Load**. Optionally, select **Transform Data** to transform and shape the data in the Power Query editor before loading it into Power BI. 

## About data granularity and data connectivity modes 

### Data granularity 

With the **Data granularity** advanced parameter, choose whether you want to: 

* Load raw query results from Viva Insights into Power BI (**Row-level data**).
* Have Power BI use the Viva Insights service to summarize data, and then return that summarized data to you in Power BI (**Aggregated data**).

#### Aggregated data 

When you use **Aggregated data**, the Power BI Connector automatically enforces the privacy rules configured in the advanced insights app by providing aggregated query data in Power BI. This option helps you to confidently build reports and share them with others without having to worry about privacy settings. 

Consider using **Aggregated data** when: 

* You plan to share your report with others and want to enforce privacy rules by default. 
* You plan to use simple aggregations, like averages. 

>[!Important]
>If you select **Aggregated data** as the **Data granularity** and **Import** as the **Data Connectivity mode**, you'll need to summarize the data in Power Query. You can group by any attribute you want here—for example, Organization, LevelDesignation, or FunctionType.  
>
>If you don’t summarize in Power Query, Power BI will try to import raw query results into Power BI. However, you’ll get an empty table because the Power BI Connector will enforce privacy rules from the advanced insights app. If you want to import raw query results, use **Row-level data** as the **Data granularity** instead. 

#### Row-level data 

When you use **Row-level data**, Viva Insights loads raw query results into Power BI, and the Power BI Connector doesn't enforce privacy rules. You’ll need to manually implement privacy rules when you build your report. For example, you can create a bar chart to visualize the average time people spend in meetings by organization, but you'll need to filter out organizations with fewer employees than the minimum group size. 

Consider using **Row-level data** when: 

* You're doing exploratory analysis and want to have access to row-level data in Power BI. 
* You won’t share the report with others, or you make sure to manually apply privacy rules before you share. 
* You need to use complex aggregations with multiple filters and conditions. 
* You need to support complex transformations. 
  
>[!Note] 
>When using **Row-level data** granularity, select **Import** for the **Data connectivity mode**. **DirectQuery** imports raw query results every time Power BI renders a visual, which creates a bad experience for you and your report's users. 
 


