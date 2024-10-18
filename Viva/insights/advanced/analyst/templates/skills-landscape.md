---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 09/02/2024
title: Skills landscape report
description: Navigate the skills landscape report in Viva Insights
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva-insights
manager: ablubetk
audience: Admin
---
# Skills landscape report (preview)

>[!Important]
>This feature is in private preview. Features in preview might not be complete and could undergo changes before becoming available in the broader public release.

The Skills landscape report helps you explore top skills people in your company may be using and identify potential skill gaps. These insights are powered by Skills in Viva.
With this report, you can:
* Discover top skills in your organization
* See how skills may be distributed across groups
* Identify potential skill gaps
* Explore related skills insights

Before we get started, there are a few things you should know:
* People need to have eligible licenses for both **Viva Insights** and **Skills in Viva** to be included in this report.
* The skills data imports from Skills in Viva to Viva Insights through APIs. Your Microsoft 365 admin or knowledge admin needs to provide consent in the MAC portal to confirm the connection.
* Only people with Viva Insights analyst role can run and set up this report. Your Insights admin needs to assign the analyst role to enable their access.
* For this private preview, the report is only available in English.
* For this private preview, the report only includes the past month of skills insights. You can run the report monthly to track skill trends and changes.

To populate the report in Power BI, you need to set up, and successfully run the predefined **Skills landscape** query in Viva Insights.

:::image type="content" source="../../images/pbi-01.png" lightbox="../../images/pbi-01.png" alt-text="Screenshot of run analysis to populate report.":::

[!INCLUDE [Demonstration](includes/demonstration.md)]

> [!VIDEO https://msit.powerbi.com/view?r=eyJrIjoiZDlmOTY4NTctYmVhYi00ZWM5LTlkYmQtYWZhZDIwNjEwMGYzIiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9]
 
## Prerequisites
Before you can run the queries and populate the report in Power BI, you need to:
* Be assigned the role of **Insights Analyst** in Viva Insights.
* Have the December 2022 (or newer) version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://www.microsoft.com/en-us/power-platform/products/power-bi/getting-started-with-power-bi) to download and install the latest version.
* People must be eligible for both **Skills in Viva** and **Viva Insights** to be included in this report. **Skills data** is required for this report. Contact your knowledge admin or Microsoft 365 admin for details.

## Report setup
### Run query
1.	In the Viva Insights analyst experience, select **Analysis.**
2.	Under Power BI templates, navigate to **Skills landscape** and select **Start analysis.**
3.	Under **Query setup**:

    1. Type a **Query name.**

    2. Type a **Description** (optional).

    >[!Note]
    >You're not able to edit the date range for this report. This report analyzes the skills data in the past month.

    The **More settings** pane also contains **Group by** settings. This Power BI query is set to **Group by Month**, and you're not able to edit this field.

4.	Under **Predefined template metrics**, there is one preselected metric, which appears as a gray tag. It is required to have at least one collaboration metric to run the query and you can’t remove it. You can add other metrics by selecting **Add metrics**, but these metrics don’t appear in the Power BI report—they just appear in your query results file.
5.	In **Select which employees you want to include in the query**, add filters to narrow down the employees in scope for your report. For more details about filter and metric options, refer to [Filters.](../filters.md)

    >[!Important]
    > Only people with valid **Skills in Viva** data and **Viva Insights** licenses are included in this report. The population count in **Employees with Skills in Viva** data shows the number of employees the query will measure. The query won't run if the population count is zero.

6.	Under **Select which employee attributes you want to include in the query**, add up to seven organizational attributes. Once the query runs, you can use these attributes to group and filter the reports.

    >[!Important]
    > This Power BI query needs some specific attributes to run, including some required attributes to indicate employee skills, and we've preselected them for you. These attributes appear in gray and you can't 
      remove them.
    > If you notice attributes marked with yellow warnings, that attribute's quality is low. If you notice attributes marked in red and the query's **Run** button disabled, then your organizational data is 
      missing that attribute.
      Learn more about attributes and data quality in [Data quality in the analyst experience.](../data-quality-analyst-experience.md)

7.	Select **Run** on the upper right side of the screen. The query might take a few minutes to run.
8.	When your query results are ready, go to the **Query results page** and select the **Power BI icon**. Download the Power BI template and get the partition and query identifiers. You need these identifiers later.

### Link report to query

1. Open the downloaded template.
1. If you're prompted to select a program, select **Power BI**.
1. When you're prompted by Power BI:
   1. Paste in the partition and query identifiers.
   1. Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Viva Insights data.
   1. Select **Load** to import the query results into Power BI.
1. If prompted by Power BI, sign in using your organizational account. Power BI then loads and prepares the data. For large files, this process might take a few minutes.
   > [!IMPORTANT]
   > You need to sign in to Power BI with the same account you use to access Viva Insights. If available, select **Organizational account** from the left. You might have to sign in more than once.
   > :::image type="content" source="../../images/analyst-pbi-org-account1.png" alt-text="Screenshot that shows signing into to Power BI on the Organizational account tab." :::

## Report settings
View and set the following parameters in **Report settings**. You can find this section on the right panel of the report's pages.

| Setting | Description |
| ------- | ------------------|
| Time period for the report | This shows the time period of the insights in the report. The report includes the skills data for the past month. |
| Group by | Set the primary group-by attribute for all report pages. You can change this attribute at any time and all report pages will group values by the new attribute. |
| Filter | Select an organizational attribute, and then filter by any of the values for the selected attribute. For example, if you selected "Organization" as the attribute, you could set "Engineering" as the filter value. You'll only see data from the Engineering organization, so setting filters lowers the **People included in this report** count. |
|Skill customization | Exclude skills inferred by AI: Choose whether to exclude AI-inferred skills in the distribution insights. AI-inferred skills are powered by Skills in Viva based on people’s job titles and recent Microsoft 365 activities. If you select this option, the report will only include confirmed skills in the distribution insights.<br></br> Exclude related skills: Choose whether to exclude related skills in the distribution insights. If you select this option, the report will only include confirmed and AI-inferred skills (if selected). Additional people with related skills are no longer included. |

## About the report
The report provides insights about the skills landscape in your organization to help you identify distribution of top skills, connections between skills, and potential skill gaps.


### About skill distribution and related concepts
This is the total number or percentage of people in your organization who have either confirmed they have a skill or are presumed to have a skill based on AI reasoning and analysis. Distribution can be filtered to include only confirmed skills in **Report settings**. Additionally, people with related skills can be included in the distribution, which is configurable on each report page. 
* **Skill confirmed by user**: A skill that a person confirmed they have in Skills in Viva.
* **Skill inferred by AI**: A skill that an AI system predicts a person has but hasn’t been confirmed by the person. AI inferences are based on job titles and recent Microsoft 365 activities. 
* **Related skills**: If two skills are related, it's more likely they share a common knowledge foundation or can be used to accomplish similar tasks. 


### Skills in Viva data coverage 

This page provides a summary of your organization’s skills data. This page can help you:

* Understand how many people are included in this report. If the number doesn’t look correct, you can contact your admin for more information 

* Discover how many people have confirmed their skills. As more people confirm their skills, the data’s relevance and accuracy improves 

* Identify top skills in your organization across the measured population 

### Skills distribution

This page provides insights on how skills are distributed between groups (determined by organizational attributes). You can use these insights to understand the skill profile for a group, compare differences across groups, and identify potential skill gaps.

When people with related skills are included in the distribution, the following insights become available:

* Additional population, by breakdown groups, that may have been using at least a skill that’s related to the selected skill 

* Top skills that are related to the selected skill, based on the distribution in the organization

### Skills landscape (beta)

Powered by Skills in Viva and currently in beta experimentation, this page shows how skills are clustered and connected to each other to help you: 

* Identify skills distribution based on categories that matter to your organization 

* Better allocate resources by understanding how skills complement each other 

#### Explore your organization’s top skills
In these interactive visuals, you can explore the distribution of skills in your organization and how they're connected. Starting with an optional filter on skill categories, you can view the top skills for that category in the first layer. Selecting one of these skills will then show the skills that roll up into it. If computer science is in the top layer, and AI is in the drilldown, this means people who may have the AI skill will also have computer science. The skills drilldown is powered by the parent-child skill relationship in Skills in Viva.

#### View distribution details
This chart provides more insight as to whether skills are confirmed or inferred by AI, and whether related skills are included in the data. 

You can search for a skill to filter the distribution details to that skill.

### Glossary
Get definitions for key concepts introduced in this report. For more information about Skills in Viva, see [Skills in Viva Overview.](https://support.microsoft.com/office/skills-in-viva-overview-98df33d7-817b-42d2-8a07-eef3bb44e078) 

## Power BI tips, FAQs, and troubleshooting
For details about how to share the report and other Power BI tips, troubleshoot any issues, or review the FAQ, see [Power BI tips, FAQ, and troubleshooting.](./power-bi-faq-troubleshoot.md)

## Related topics
[Access query results and modify existing queries](../query-results.md)

[Filters](../filters.md)

