---
ms.date: 06/19/2024
title: Microsoft 365 Copilot adoption report
description: Learn how to use the Microsoft 365 Copilot adoption Power BI template to understand Copilot employee usage across an organization.
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva-insights
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Microsoft 365 Copilot adoption report

The **Microsoft 365 Copilot adoption** report helps leaders understand Copilot usage across their organization. The insights can help you accelerate Copilot adoption, and help employees transform their work with Microsoft 365 Copilot.

This report has five sections. These sections help you answer the following business questions:

* How does Copilot usage compare across groups?
* How does Copilot usage compare across apps?
* What are the most frequently used Copilot features in each app?
* What is the Copilot usage trend across groups?
* What is the breakdown of Copilot usage across groups?  

Lastly, the ”Learn more” section provides an overview of research articles and case studies about Copilot adoption and impact.

To populate the report in Power BI, you’ll need to set up and successfully run the predefined **Microsoft 365 Copilot adoption** query in Viva Insights.

## Demonstration

The following demonstration uses sample data that’s only representative of this report and might not be exactly what you see in a live report specific to your organization's unique data.

> [!VIDEO https://msit.powerbi.com/view?r=eyJrIjoiMmVmOTk3ZTEtNDgzZS00NTI4LWEyZDQtZjYxY2NhNjY0ZjlmIiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9]

## Prerequisites

Before you can run the queries and populate the report in Power BI, you’ll need to: 

* Be assigned the role of **Insights Analyst** in Viva Insights.
* Have the June 2022 (or newer) version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://www.microsoft.com/power-platform/products/power-bi/getting-started-with-power-bi) to download and install the latest version.
* Have Microsoft 365 Copilot licenses assigned to the employees you would like to include as part of your measured population.

## Report setup

### Run query

1. In the Viva Insights analyst experience, select **Create analysis**.
2. Under **Templates**, navigate to **Microsoft 365 Copilot adoption** and select **Set up analysis**. The template can also be found underneath the **Copilot** section.
3. Under **Query setup**:
    
    1. Type a **Query name**.
    1. Select a **Time period**. **Time period** defaults to **Last 6 months**.
    1. Set **Auto-refresh** (optional). You can set the query to automatically update by checking the **Auto-refresh** box. When you select the **Auto-refresh** option, your query automatically runs and computes a new result every time Viva Insights gets updated collaboration data for licensed people.
       > [!NOTE]
       > If organizational data used in an auto-refreshing query changes (for example, an attribute name is altered or an attribute is removed), the query might stop auto-refreshing.
     4. Type a **Description** (optional).   
     5. Change the metric rule (optional). To set a new metric rule, select **More settings**. Then, pick a new rule from the list. [Learn more about metric rules](../../analyst/metric-rules.md).
        > [!NOTE]
        > The **More settings** pane also contains **Group by** settings. Power BI queries are set to **Group by Week**, and you're not able to edit this field.

4. Under **Predefined template metrics**, view a list of preselected metrics, which appear as gray tags. These metrics are required to set up the Power BI report and you can’t remove them. However, you can add other metrics by selecting **Add metrics**.
    > [!IMPORTANT]
    > Low-quality or missing organizational data might affect your metrics and result in warnings or errors. [Learn more about data quality notifications](../../analyst/data-quality-analyst-experience.md).

5. In **Select which employees you want to include in the query**, add filters to narrow down the employees in scope for your report. Don’t remove the predefined “Is Active” filter. [Learn more about filter and metric options](../../analyst/filters.md). If you notice a warning or error here, it's because one of your attributes is missing from your organizational data or it's of low quality.

6. Under **Select which employee attributes you want to include in the query**, add up to 20 organizational attributes. Once the query runs, you can use these attributes to group and filter the reports.

    > [!IMPORTANT]
    > This PowerBI query needs some specific attributes to run, and we've preselected them for you. These attributes appear in gray and you can't remove them. We might also include some attributes that help your template, but aren't required for your query to run. These attributes appear in blue and you can remove them.
    >
    > If you notice attributes marked with yellow warnings, that attribute's quality is low. If you notice attributes marked in red and the query's **Run** button disabled, then your organizational data is missing that attribute.
    >
    > [Learn more about attributes and data quality](../../analyst/data-quality-analyst-experience.md).

7. Select **Run** on the upper right. The query might take a few minutes to run.

### Link report to query

1. Open the downloaded template.

2. If you're prompted to select a program, select **Power BI**.

3. When you're prompted by Power BI:

    1. Paste in the partition and query identifiers. 
    2. Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Viva Insights data. 
    3. Select **Load** to import the query results into Power BI. 

4. If prompted by Power BI, sign in using your organizational account. Power BI then loads and prepares the data. For large files, this process might take a few minutes.