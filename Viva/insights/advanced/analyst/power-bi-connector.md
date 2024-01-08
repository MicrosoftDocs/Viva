---
ms.date: 01/04/2024
title: Use the Power BI connector
description: Learn how to connect your Viva Insights data to Power BI through the Power BI connector
author: zachminers
ms.author: v-zachminers
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

# Connect to Viva Insights using the Power BI Connector

To connect your Viva Insights data to Power BI using the [Power BI connector](/connectors/powerbi/), follow these steps:

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
   1. Enter the query identifier.
        
      > [!Note]
      > Query name isn't supported right now.
         
   1. Set advanced parameters (optional).
     1. In Schema type, select from two options:
        * **Pivoted (Default)** to load organizational attributes as individual columns. Here's an example of how your results would load with this option:
        
          |PersonId|MetricDate|Collaboration hours|Organization|SupervisorIndicator|
          |---------|---------|--------|------|--------|
          |A|5/7/2023|23.6|Finance|Manager|
        
        * **Unpivoted** to load organizational attributes as key-value pairs. Here's an example of how your results would load with this option:
           
          |PersonId|MetricDate|Collaboration hours|AttributeName|AttributeValue|
          |---------|---------|--------|------|--------|
          |A|5/7/2023|23.6|Organization|Finance|
          |A|5/7/2023|23.6|SupervisorIndicator|Manager|
       
          >[!Important]
          >The **Unpivoted** option is only supported for **Aggregated data** data granularity.
       
     1. In Data granularity, select from these options:
        * **Aggregated data (default)** to have Power BI use the Viva Insights service to summarize data, and then return that summarized data to you in Power BI. 
        * **Row-level data** to load raw query results from Viva Insights into Power BI.  
        > [!Note] 
        > Learn more about aggregated and row-level data later, in [About data granularity and data connectivity mode](#about-data-granularity-and-data-connectivity-modes). 
     1. Select a **Data connectivity** mode: 
        * **Import** – This mode brings a copy of your query results into Power BI Desktop. As you create or interact with visualizations, Power BI Desktop uses these copied results. To see underlying data changes after the initial import or the most recent refresh, you'll need to import the full dataset again to refresh the data. 
        * **DirectQuery** – This mode doesn't import any query results into Power BI Desktop. You can select columns to appear in the Power BI Desktop **Fields** list. As you create or interact with visualizations, Power BI Desktop uses your results as they appear in Viva Insights, so you're always viewing current data. 
        
        > [!Note] 
        > Learn more about these modes later, in [About data granularity and data connectivity mode](#about-data-granularity-and-data-connectivity-modes). 
    
1. Select **OK**. 
   If you're prompted to sign in, select **Sign in**. Enter your credentials and select **Connect**.
1. In the preview window, select **Load**. Optionally, select **Transform Data** to transform and shape the data in the Power Query editor before loading it into Power BI. 

## About data granularity and data connectivity modes 

### Data granularity 

With the **Data granularity** advanced parameter, choose whether you want to: 

* Load raw query results from Viva Insights into Power BI (**Row-level data**).
* Have Power BI use the Viva Insights service to summarize data, and then return that summarized data to you in Power BI (**Aggregated data**).

#### Aggregated data 

When you use **Aggregated data**, the Power BI Connector automatically enforces the privacy rules configured in the advanced insights app, including the [Minimum group size](../setup-maint/privacy-settings.md#minimum-group-size), by providing aggregated query data in Power BI. This option helps you to confidently build reports and share them with others without having to worry about privacy settings.

Consider using **Aggregated data** when:

* You plan to share your report with others and want to enforce privacy rules by default.
* You plan to use simple aggregations, like averages.

> [!Important]
> If you select **Aggregated data** as the **Data granularity** and **Import** as the **Data Connectivity mode**, you'll need to summarize the data in Power Query. You can group by any attribute you want here—for example, Organization, LevelDesignation, or FunctionType.  
>
> If you don’t summarize in Power Query, Power BI will try to import raw query results into Power BI. However, you’ll get an empty table because the Power BI Connector will enforce privacy rules from the advanced insights app. If you want to import raw query results, use **Row-level data** as the **Data granularity** instead. 

#### Row-level data 

When you use **Row-level data**, Viva Insights loads raw query results into Power BI, and the Power BI Connector doesn't enforce privacy rules, including the [Minimum group size](../setup-maint/privacy-settings.md#minimum-group-size). You’ll need to manually implement privacy rules when you build your report. For example, you can create a bar chart to visualize the average time people spend in meetings by organization, but you'll need to filter out organizations with fewer employees than the minimum group size.

Consider using **Row-level data** when:

* You're doing exploratory analysis and want to have access to row-level data in Power BI.
* You won’t share the report with others, or you make sure to manually apply privacy rules before you share.
* You need to use complex aggregations with multiple filters and conditions.
* You need to support complex transformations.
  
> [!Note] 
> When using **Row-level data** granularity, select **Import** for the **Data connectivity mode**. **DirectQuery** imports raw query results every time Power BI renders a visual, which creates a bad experience for you and your report's users. 
 
