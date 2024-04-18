---
ms.date: 04/18/2024
title: Skills landscape report
description: Navigate the skills landscape report in Viva Insights
author: kateylundquist
ms.author: v-klundquist
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights
manager: ablubetk
audience: Admin
---
# Skills landscape report 
*Applies to: private preview customers only*

The Skills landscape report helps you explore top skills people in your company may be using and identify potential skill gaps. These insights are powered by Skills in Viva.
With this report, you can:
* Discover top skills in your organization and how they are connected
* See how skills may be distributed across groups
* Identify potential skill gaps
* Explore related skills insights

Before we get started, there are a few things you should know:
* People need to have eligible licenses for both **Viva Insights** and **Skills in Viva** to be included in this report
* The skills data will import from Skills in Viva to Viva Insights through APIs. Your Microsoft 365 admin or knowledge admin needs to provide consent in the MAC portal to confirm the connection.
* Only people with Viva Insights analyst role can run and set up this report. Your Insights admin needs to assign the analyst role to enable their access.
* For this private preview, the report is only available in English.
* For this private preview, the report only includes the past month of skills insights. You can run the report monthly to track skill trends and changes.

To populate the report in Power BI, you will need to set up and successfully run the predefined **Skills landscape** query in Viva Insights.

:::image type="content" source="../images/pbi-01.png" alt-text="Screenshot of run analysis to populate report.":::
 
## Prerequisites
Before you can run the queries and populate the report in Power BI, you’ll need to:
* Be assigned the role of **Insights Analyst** in Viva Insights.
* Have the December 2022 (or newer) version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://www.microsoft.com/en-us/power-platform/products/power-bi/getting-started-with-power-bi) to download and install the latest version.
* People must be eligible for both **Skills in Viva** and **Viva Insights** to be included in this report. **Skills data** is required for this report. Please contact your knowledge admin or Microsoft 365 admin for details.

## Report setup
### Run query
1.	In the Viva Insights analyst experience, select **Analysis.**
2.	Under Power BI templates, navigate to **Skills landscape** and select **Start analysis.**
3.	Under **Query setup**:

    1. Type a **Query name.**

    2. Type a **Description** (optional).

>[!Note]
>You’re not able to edit the date range for this report. This report analyzes the skills data in the past month.

The **More settings** pane also contains **Group by** settings. Power BI queries are set to **Group by Month**, and you're not able to edit this field.

4.	Under **Predefined template metrics**, there is one preselected metric which appears as a gray tag. It is required to have at least one collaboration metric to run the query and you can’t remove it. You can add other metrics by selecting **Add metrics**, but these metrics won’t be available to use in the Power BI report—they’ll just appear in your query results file.
5.	In **Select which employees you want to include in the query**, add filters to narrow down the employees in scope for your report. For more details about filter and metric options, refer to [Filters.](https://learn.microsoft.com/viva/insights/advanced/analyst/filters) 

>[!Important]
> Only people with valid **Skills in Viva** data and **Viva Insights** licenses are included in this report. The population count in **Employees with Skills in Viva** data shows the number of employees the query will measure. The query won’t run if the population count is zero.
6.	Under **Select which employee attributes you want to include in the query**, add up to seven organizational attributes. Once the query runs, you can use these attributes to group and filter the reports.

>[!Important]
> This Power BI query needs some specific attributes to run, including some required attributes to indicate employee skills, and we've preselected them for you. These attributes appear in gray and you can't remove them.

If you notice attributes marked with yellow warnings, that attribute's quality is low. If you notice attributes marked in red and the query's **Run** button disabled, then your organizational data is missing that attribute.
Learn more about attributes and data quality in [Data quality in the analyst experience.](https://learn.microsoft.com/viva/insights/advanced/analyst/data-quality-analyst-experience)

7.	Select **Run** on the upper right side of the screen. The query might take a few minutes to run.
8.	When your query results are ready, go to the **Query results page** and select the **Power BI icon**. Download the Power BI template and get the partition and query identifiers. You’ll need these identifiers later.

### Link report to query

>[!Note]
>Use the same template as in other online documentation.

:::image type="content" source="../images/pbi-02.png" alt-text="Screenshot of a diagram for Microsoft Entra ID that shows each data source on the left, arrows in the center, and each attribute on the right.":::

### Report settings
View and set the following parameters on the **Settings** page. You can find **Settings** on the right panel of the introduction page. You can also adjust the report settings as you go through the report pages through the **Settings** icon.

| Setting | Description |
| ------- | ------------------|
| Organizational attribute | Set the primary group-by attribute for all report pages. You can change this attribute at any time and all report pages will group values by the new attribute. |
| Optional filter | Select an organizational attribute, and then filter by any of the values for the selected attribute. For example, if you selected "Organization" as the attribute, you could set "Engineering" as the filter value. You'll only see data from the Engineering organization, so setting filters lowers the **People included in this report** count. |
|Skills insight customization | Choose whether you want this report to include AI-inferred skills in the distribution insights. AI-inferred skills are powered by Skills in Viva based on people’s job titles and recent Microsoft 365 activities. If this option is not selected, the report will only include confirmed skills in the distribution insights. |


**People included in this report**

This figure shows how many people your report is analyzing. When you adjust your filters, you'll notice different numbers here.
To protect privacy, this report doesn't show groups with fewer than ten people. Learn more about minimum group size in our [setup documentation.](https://learn.microsoft.com/viva/insights/advanced/setup-maint/privacy-settings#minimum-group-size)

### About the report
The report provides insights about the skills landscape in your organization to help you identify distribution of top skills, connections between skills, and potential skill gaps.

This report contains some key concepts for skills.

#### Skill distribution
This is the total number or percentage of people in your organization who have either confirmed they have a skill or are presumed to have a skill based on AI reasoning and analysis. Distribution can be filtered to include only confirmed skills on the settings page. Additionally, people with related skills can be included in the distribution, which is configurable on each report page. 
* **Confirmed skills**: A skill that a person confirmed they have in Skills in Viva.
* **AI-inferred skills**: A skill that an AI system predicts a person has but hasn’t been confirmed by the person. AI inferences are based on job titles and recent Microsoft 365 activity. 
* **Related skills**: If two skills are related, it’s more likely they share a common knowledge foundation or can be used to accomplish similar tasks. 

Use the following pages to explore the skills landscape in your organization.

#### Skills overview
This page shows how skills are clustered and connected to each other to help you:
* Maximize learning and career advancement programs
* Identify skills distribution based on categories that matter to your organization
* Better allocate resources by understanding how skills complement each other

#### Explore your organization’s top skills
In this interactive visual, you can explore the distribution of skills in your organization and how they are connected. Start with a category of skills, you can click to see the top skills for that category in the first layer. Selecting one of these skills will then show the skills that roll up into it in the next layer. If computer science is in the first layer, and AI is in the second, this means people who may have the AI skill will also have computer science. This report shows a maximum of five layers.

The connection of skills between layers is based on the parent-child skill relationship powered by Skills in Viva.

#### View distribution details
This chart provides more insight as to whether skills are confirmed or inferred by AI, and whether related skills are included in the data. 

Select a skill in the interactive visual above, or search for a skill to filter the distribution details to that skill.

#### Skills distribution
This page provides insights on how skills are distributed between groups (determined by organizational attributes). You can use these insights to understand the skill profile for a group and identify potential skill gaps.
Skills are grouped based on the same hierarchy applied in the **Skills overview** page. 

#### Skills breakdown
On this page, you can explore the distribution of a selected skill across your organization, and identify gaps where certain skills may be needed.

When people with related skills are included in the distribution, the following insights become available. 
* Additional population, by breakdown groups, that may have been using at least a skill that’s related to the selected skill
* Top skills that are related to the selected skill, based on the distribution in the organization

#### Glossary
Get definitions for key concepts introduced in this report. For more information about Skills in Viva, see [Skills in Viva Overview.](https://support.microsoft.com/office/skills-in-viva-overview-98df33d7-817b-42d2-8a07-eef3bb44e078)

### Power BI tips, FAQs, and troubleshooting
For details about how to share the report and other Power BI tips, troubleshoot any issues, or review the FAQ, see [Power BI tips, FAQ, and troubleshooting.](https://learn.microsoft.com/viva/insights/advanced/analyst/templates/power-bi-faq-troubleshoot)

### Related topics
[Access query results and modify existing queries](https://learn.microsoft.com/viva/insights/advanced/analyst/query-results)

[Filters](https://learn.microsoft.com/viva/insights/advanced/analyst/filters)
