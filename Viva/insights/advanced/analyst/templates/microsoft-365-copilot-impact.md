---
ms.date: 09/16/2024
title: Microsoft 365 Copilot impact report
description: Learn how to use the Microsoft 365 Copilot impact Power BI template to understand the effects of Copilot usage among employees across your organization.
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

# Microsoft 365 Copilot impact report (public preview)

> [!Important]
> This feature is available to all customers in public preview. Features in preview might not be complete and could undergo changes before becoming available in the broader release.

The **Microsoft 365 Copilot impact** report helps leaders understand the impact of Copilot usage among employees across their organization. The insights can help you evaluate the relationship between Copilot adoption and collaboration patterns. It also spotlights the total number of hours employees were “assisted” by Copilot in their daily work.

The report summary page provides an overview of the total number of active Copilot users, the total number of Copilot actions taken, and the number of Copilot assisted hours. From here the user can dive deeper into the following five sections:  

* Meetings
* Teams chat
* Email
* Documents
* Business Chat (work)

Each of these sections allows the user to evaluate how collaboration patterns have changed after employees started using Copilot. It also provides comparisons between Copilot and non-Copilot users across groups. 

Lastly, the “Learn what our research says about the impact of Copilot” section provides an overview of research articles and case studies about Copilot adoption and impact. 

To populate the report in Power BI, you’ll need to set up and successfully run the predefined **Microsoft 365 Copilot impact** query in Viva Insights.

## Demonstration

The following demonstration uses sample data that’s only representative of this report and might not be exactly what you see in a live report specific to your organization's unique data.<br/><br/>

> [!VIDEO https://msit.powerbi.com/view?r=eyJrIjoiZjYyMzlhZGItZWIyMC00NzRlLThlYjMtMTgwN2E5NjU3ZWE1IiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9]

## Prerequisites

Before you can run the queries and populate the report in Power BI, you’ll need to: 

* Be assigned the role of **Insights Analyst** in Viva Insights and licensed with Viva Insights.
* Have the June 2022 (or newer) version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://www.microsoft.com/power-platform/products/power-bi/getting-started-with-power-bi) to download and install the latest version.
* Have Microsoft 365 Copilot licenses and Microsoft Viva Insights licenses assigned to the employees you would like to include as part of your measured population.

## Report setup

### Run query

1. In the [Viva Insights analyst experience](https://analysis.insights.viva.office.com/), select **Create analysis**.
2. Under **Templates**, navigate to **Microsoft 365 Copilot impact** and select **Set up analysis**. The template can also be found underneath the **Copilot** section.
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

The **Microsoft 365 Copilot impact** report includes the following report pages that help you better understand and accelerate Copilot adoption across the company.

##### Microsoft 365 Copilot impact summary 

Learn more about how your company uses Copilot. The page’s top section provides a baseline of the number of active Copilot users across the company, the total number of Copilot actions taken by these users, and an estimate of the number of Copilot assisted hours.

##### Copilot assisted hours metric

Copilot assisted hours are an estimate of the total time employees were assisted by using Copilot over the selected time period. Employees can re-invest time savings from Copilot in learning, training, skilling, and having a greater business impact. The metric is computed based on your employees’ actions in Copilot and multipliers derived from [Microsoft’s research on Copilot users](https://www.microsoft.com/en-us/worklab/). The metric should be viewed as a general estimate based on the most relevant Copilot usage data and research currently available. The underlying calculation methodology will evolve over time as new information becomes available.

The “Hours and value calculator” link provides a breakdown of how the total Copilot assisted hours figure is calculated. The user can also switch back and forth between an hours calculator and a value calculator. The value calculator multiplies the assisted hours by an average hourly rate. The average hourly rate is set to $72 by default based on estimates from the U.S. Bureau of Labor Statistics. You can update the hourly rate on the “Hours and value calculator” page.  

##### Structure of the report 

The rest of the summary page presents a set of five cards with the total number of Copilot actions taken by users in meetings, emails, Teams chat, Documents, and Copilot chat (work), respectively. Select **Dive deeper** to see the relationship between Copilot adoption and collaboration patterns, and explore changes over time and differences between groups. Each of the cards, e.g. meetings, email, Teams chat, Documents, and Copilot work (chat), come with three deep dive analysis pages:

* Compare Copilot usage and collaboration behavior after Copilot adoption 
* Compare collaboration behavior between Copilot and non-Copilot users across groups 
* Compare Copilot usage and collaboration behavior between two groups 

The structure of each of these pages is the same for the deep dive into meetings, email, Teams chat, Documents, and Copilot work (chat), but the types of Copilot and behavioral metrics shown differs. In the next section we will walk through the structure of each of these pages.

##### Compare Copilot usage and collaboration behavior after Copilot adoption 

This page shows the impact of Copilot usage on employees’ collaboration behavior. In the meetings section, for example, you can evaluate the number and duration of meetings that were summarized with Copilot. You can also learn how meeting behavior has changed for employees after adopting Copilot.

> [!Important]
> To accurately capture the first time employees began using Copilot in different apps, make sure your query includes the time period in which your company first started using Copilot. For example, if your company enabled Copilot in January 2024, make sure data going back to January 2024 is included in the query.

##### Compare collaboration behavior between Copilot and non-Copilot users across groups 

This page compares meeting behavior between users who have a Copilot license and use Copilot features, and those who don’t use any Copilot features or don’t have a Copilot license. Specifically, the following types of employee segments can be selected and compared across groups:

* Active Copilot users 
* Non-Copilot users 
* Active Copilot users 
* Inactive Copilot users  

The definitions of these segments can be found in the glossary.  

Using the “Group by” filter, you can compare Copilot and non-Copilot users across different functions or organizations in the company. Use the metrics dropdown menu  to select collaboration metrics relevant to meetings, emails, documents, Teams chat, or Copilot chat (work), depending on what section of the report you’re in. This page is only available for the meetings, email, and Teams chat sections. 

##### Compare Copilot usage and collaboration behavior between two groups 

This page compares Copilot usage and collaboration behavior between two customizable cohorts of employees. In the meeting section, for example, you can evaluate the difference in the number and duration of meetings that were summarized with Copilot between these two cohorts. You can also evaluate the difference in the meeting behavior. In addition to organizational filters, there is a “type” filter you can use to filter on the following segments of employees:

* Active Copilot users 
* Non-Copilot users 
* Active Copilot users 
* Inactive Copilot users  

The definitions of these segments can be found in the glossary.  

##### Learn what our research says about the adoption of Copilot 

The articles in this section range from practical guides on how to get started with Copilot to research findings related to the adoption and perceived impact of employees using Copilot within various Microsoft apps and services.

##### Glossary

View this report's metric definitions.

### Power BI tips, FAQs, and troubleshooting 

[Learn more](./power-bi-faq-troubleshoot.md) about how to share the report and other Power BI tips, troubleshoot any issues, or review the FAQ.

### Related topics

- [Access query results and modify existing queries](../query-results.md)
- [Filters](../filters.md)