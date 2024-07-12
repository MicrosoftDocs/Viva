---
ms.date: 07/12/2024
title: Microsoft 365 Copilot adoption report
description: Learn how to use the Microsoft 365 Copilot adoption Power BI template to understand Copilot employee usage across an organization.
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection:
- viva-insights-advanced
- viva-copilot
- magic-ai-copilot 
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

The following demonstration uses sample data that’s only representative of this report and might not be exactly what you see in a live report specific to your organization's unique data.<br/><br/>

> [!VIDEO https://msit.powerbi.com/view?r=eyJrIjoiMmVmOTk3ZTEtNDgzZS00NTI4LWEyZDQtZjYxY2NhNjY0ZjlmIiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9]

## Prerequisites

Before you can run the queries and populate the report in Power BI, you’ll need to: 

* Be assigned the role of **Insights Analyst** in Viva Insights and licensed with Viva Insights.
* Have the June 2022 (or newer) version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://www.microsoft.com/power-platform/products/power-bi/getting-started-with-power-bi) to download and install the latest version.
* Have Microsoft 365 Copilot licenses and Microsoft Viva Insights licenses assigned to the employees you would like to include as part of your measured population.

## Report setup

### Run query

1. In the [Viva Insights analyst experience](https://analysis.insights.viva.office.com/), select **Create analysis**.
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

    > [!IMPORTANT]
    > You need to sign in to Power BI with the same account you use to access Viva Insights. If available, select **Organizational account** from the left. You might have to sign in more than once.
    >
    > :::image type="content" source="../../images/analyst-pbi-org-account1.png" alt-text="Screenshot that shows signing into to Power BI on the Organizational account tab":::

### Report settings

#### Settings page

View and set the following parameters on the **Settings** page. You can find **Settings** on the right panel of the introduction page. You can also adjust the report settings as you go through the report pages through the **Settings** icon.

* **Time period for the report** – Select the time period for which you want to view data in the report.
* **Group by** – Select the primary group-by attribute shown in all the report pages. You can change this attribute at any time and all report pages will show group values by the new attribute.
* **Apply filters** (optional) – Select the organizational attribute and values you want to use to filter the employees shown in this report.
* **Customize active Copilot user definition** – Customize the usage frequency for active Copilot users. You can choose between:

  * At least one active day in the selected time period
  * At least one active day per four weeks
  * At least one active day per week 

  A day is marked as active if the user took at least one action with Copilot on that respective day. 

* **Report language** – Change the language for your report.

## About this report 

The **Microsoft 365 Copilot adoption** report includes the following report pages that help you better understand and accelerate Copilot adoption across the company.

##### Microsoft 365 Copilot adoption summary

Get an overview of Microsoft 365 Copilot adoption across the company. Get a baseline view of the number of employees who are actively using Microsoft 365 Copilot features and what direction adoption is trending. This page also provides a quick overview of the Microsoft 365 app in which Copilot is used as well as the top-most used Copilot feature. Lastly, it highlights the organization with the highest Copilot usage. 

##### How does Copilot usage compare across groups? 

Gain insight into which groups in your company are leaders in Copilot adoption. Use this page to: 

* Understand the breakdown of active Copilot users by group (left-side card) 
* Understand the usage frequency by exploring the average number of Copilot actions taken per person per week and per month, by group.  

Active Copilot users are defined as users who have used Copilot at least once in the selected time period. 

##### How does Copilot usage compare across apps?

Learn more about how Copilot usage differs by app across organizations and functions. The heatmap shows the share of active Copilot users in each Microsoft 365 app as a percentage of the total number of people in the respective group. Active Copilot users are defined as users who have used Copilot at least once in the selected time period.  

##### What are the most frequently used Copilot features in each app?

Understand how your employees are using Copilot in each Microsoft 365 app. The cards on this page show the total number of Copilot user actions taken or the unique number of active Copilot users in each Microsoft 365 app broken out by Copilot action. Use the arrows at the bottom of the page to explore Copilot actions taken in PowerPoint and Excel.  

##### What is the Copilot usage trend across groups? 

Explore how Copilot usage has changed over time for different groups in your company. Explore how Copilot usage is changing over time, using the left-side card. The trendline shows the total weekly number of Copilot user actions or unique active Copilot users in the filtered groups for the selected time period. The table on the right shows the number of unique active Copilot users per month and the month-over-month change.  

##### What is the breakdown of Copilot usage across groups? 

Dive one layer deeper and explore different usage metrics at the same time for different groups in a side-by-side view. Use the metric filter at the top to select the metrics you would like to include and compare in the table. Metrics include:

* Active Copilot users
* Monthly active Copilot users
* Weekly active Copilot users
* Percentage of active Copilot users
* Percentage of Copilot licensed users
* Average number of actions performed
* Copilot licensed users
* Measured employees

Metric definitions can be found in the glossary. 

##### Learn what our research says about the adoption of Copilot 

Learn more about what our research says about the adoption of Copilot. The articles in this section range from practical guides on how to get started with Copilot to research findings related to the adoption and perceived impact of employees using Copilot within various Microsoft apps and services.

##### Glossary

View this report's metric definitions.

### Power BI tips, FAQs, and troubleshooting 

[Learn more](./power-bi-faq-troubleshoot.md) about how to share the report and other Power BI tips, troubleshoot any issues, or review the FAQ.

### Related topics

- [Access query results and modify existing queries](../query-results.md)
- [Filters](../filters.md)
