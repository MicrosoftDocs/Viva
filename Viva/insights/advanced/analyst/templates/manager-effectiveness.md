---
ROBOTS: NOINDEX,FOLLOW
title: Manager effectiveness report
description: Learn how the Ways of working PowerBI template from Microsoft Viva Insights helps you gain insight into the collaboration habits and effectiveness of your people managers.
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

# Manager effectiveness report

The **Manager effectiveness report** uses a template populated by Microsoft Viva Insights data to analyze people-manager behaviors in your organization. HR analysts can use this analysis to measure behaviors and trends of people managers across four key themes within your organization— manager capacity, coach, empower, connect, and model.

Each theme includes insights about manager effectiveness and ways to help maintain or increase preferred leadership behaviors. Key metrics are used to deep-dive into each theme, along with a **Why this matters** interpretation and best practices recommended by industry experts.

![Manager effectiveness report, Summary](/viva/insights/advanced/images/manager-effectiveness-pbi-summary.png)

To populate the report in Power BI, you’ll need to set up and successfully run the predefined **Manager effectiveness** query in Viva Insights.

## Demonstration

The following demonstration uses sample data that’s only representative of this report and might not be exactly what you see in a live report specific to your organization's unique data.

<iframe title="Manager effectiveness - Summary" width="600" height="373.5" src="https://msit.powerbi.com/view?r=eyJrIjoiNzY1YTI3ZmQtYjVkZi00YTA2LWI0MjEtN2MxNDQ4MGE0YmZjIiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9" frameborder="0" allowFullScreen="true"></iframe>

## Prerequisites

Before you can run the queries and populate the report in Power BI, you’ll need to:

* Be assigned the role of **Insights Analyst** in Viva Insights.
* Have the June 2022 (or newer) version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://powerbi.microsoft.com/en-us/getting-started-with-power-bi/) to download and install the latest version.

## Report setup

### Run query

>[!Note]
> For this release of Viva Insights, this report is currently only available in English and will only work with data generated from the English version of Viva Insights.

1. In the Viva Insights Analyst experience, select **Analysis**.

2. Under **Power BI templates**, navigate to **Manager effectiveness** and select **Start analysis**. To get more information about the Manager effectiveness template before running your analysis, select **Learn more**.

    ![Query start](/viva/insights/advanced/images/me-pbi-start.png)

3. Under **Query setup**:
    1. Type a **Query name**.
    1. Select a **Time period**. **Time period** defaults to **Last 3 months**.
    1. Optional: You can set the query to automatically update by checking the **Auto-refresh** box. When you select the **Auto-refresh** option, your query automatically runs and computes a new result every time Viva Insights gets updated collaboration data for licensed people.

    >[!Note]
    >If the organizational data used in an auto-refreshing query changes (for example, an attribute name is altered or an attribute is removed), you might see an error when you run the query.

    4. Optional: Type a **Description**.
    
        Selecting **More settings** brings you to a pane, but there’s nothing you need to change there. In this pane:

        * Power BI queries are set to **Group by Week**. Don't change this **Group by** designation.
        * The **Metric rules** field defaults to **Meeting exclusions rule (preferred rule)**. This field isn’t customizable in this release; for more information, refer to [Metric rules](../metric-rules.md).
![Query setup](/viva/insights/advanced/images/me-pbi-setup.png)

4. **In Predefined template metrics**, leave prepopulated metrics as they appear.  
![Predefined metrics](/viva/insights/advanced/images/me-pbi-predefined-metrics.png)

    >[!Note]
    > Metrics in Power BI templates can't be edited in this release of Viva Insights. To expand the full list of metrics included in the Power BI template, select the arrow in the box beneath **Metrics, filters, and organizational attributes**.

5. You can filter the employees in scope for the report under **Select which employees you want to include in the query**. Don’t remove the predefined “Is Active” filter. For more details about filter and metric options, see [Create a Custom Person query](../person-query.md).
![Is active filter](/viva/insights/advanced/images/pbi-templates-isactive-filter.png)

6. Under **Select which employee attributes you want to include in the query**, add up to seven organizational attributes. Once the query runs, you can use these attributes to group and filter the reports.

    >[!Important]
    >Some employee attributes are required to set up this Power BI template, which are preselected for you in the query. *Don't remove any preselected attributes.*
    >
    >If you see attributes marked in red and the query’s **Run** button disabled, it means that these required attributes are missing from your organizational data. Contact your admin to upload them.

7. Select **Run** on the upper right side of the screen, which can take a few minutes to complete.

8. When your query results are ready, go to the **Query results** page and select the **Power BI** icon to download the Power BI template and copy the query identifier. You'll need the query identifier later.

### Link report to query

9. Open the downloaded **Manager effectiveness** template.

10. If prompted to select a program, select **Power BI**.

11. When prompted by Power BI:
    1. Paste in the query identifier.
    1. Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Viva Insights data.
    1. Select **Load** to import the query results into Power BI.

12. If prompted by Power BI, sign in using your organizational account. Power BI then loads and prepares the data, which can take a few minutes to complete for large files.

>[!Important]
> You must sign in to Power BI with the same account you use to access Viva Insights.

## Report settings

After the **Manager effectiveness report** is set up and populated with Viva Insights data in Power BI, map values as prompted, which are listed below.

|Value   |Prompt| 
|----------|----|
|Individual contributor     |Select the attribute values that identify employees as individual contributors who do not manage people within your organization      |
|Manager indicator|Select the attribute values that identify managers who manage people within your organization, such as **Mgr** and **Mgr+.**|

![Manager effectiveness report IC and Mgr questions](/viva/insights/advanced/images/manager-effectiveness-pbi-questions.png)

After this initial prompt, you can then select **Settings** at top right of any page to view and change the following parameters:
* **Select the time period for the report** – Select the time period for which you want to view data in the report.  
* **Select an attribute to group data by** – Select the primary group-by attribute shown in all the reports. You can change this attribute at any time and all report pages will show group values by the new attribute.
* **Select optional report filter** – Select the organizational attribute and values you want to filter the employees in the report.
* **Exclusions** – Use the check boxes to:
    * Exclude employees who are likely non-knowledge workers (that is, those spending less than five hours per week in meetings, emails, and/or Teams calls and chats).
    * Exclude weeks that are likely holiday or paid-time-off weeks or weeks that individuals are on other types of leave.

![Manager effectiveness report IC and Mgr questions](/viva/insights/advanced/images/manager-effectiveness-pbi-customize-report.png)

## About this report

The report contains one report page per theme, and each report page asks a related business question. The following section:

* Lists the report pages that fall under each theme and describes which data they contain.
* Describes the report’s **Behavioral trends** and **Take action** pages. 

### Manager capacity

**Do managers have enough time for their employees?**

This page shows the weekly average number of hours that managers spent collaborating with people in the company, divided into groups and types of communication (meetings, emails, chats, and calls). It also shows the average percentage of collaboration time that managers spent with direct reports as compared to others in the organization.

### Coach

**Are employees receiving sufficient coaching time with their manager?**

This page analyzes managers’ behavior in scheduling 1:1 time with their direct reports by groups. Metrics include monthly average number of minutes in 1:1 meetings with direct reports, percentage of employees who receive a different number of 1:1 hours with their manager, and the average frequency of 1:1 time (weekly, monthly, or quarterly).

### Empower

**Are managers balancing oversight with employee autonomy?**

This page shows the percentage of employees whose managers co-attend their meetings and might be micromanaging them as direct reports. It also shows the weekly average number of hours that managers co-attended meetings and spent in 1:1 meetings with their direct reports.

### Connect

**How well-connected are managers and do they leverage their network to help build connections for their employees?**

This page shows the internal network size distribution of managers as compared to the full organizational population, calling out the share of managers that are among the top 25% most connected employees in the company. It also shows the average internal network size of managers as compared to individual contributors broken out by group.

## Model

**Are managers modeling good work-life balance habits?**

This page shows the distribution of managers by average weekly time spent in after-hours collaboration, calling out the share of managers spending more than five hours per week in collaboration outside of their set working hours. It also shows the difference in average after-hours collaboration hours for managers and individual contributors, broken out by group. 

### Behavioral trends

**How are manager behaviors evolving?**

This page shows the trends for key leading indicator metrics for managers, including metrics about coaching and empowerment, network connections, and after-hours work habits.

### Take action

**How can manager effectiveness be improved?** 

This page lists opportunity areas with related best practices and recommendations and links to related articles about ways to help your managers improve in each area.

### Glossary

The **Glossary** describes metrics used in the report pages.

## Power BI tips, FAQs, and troubleshooting

For details about how to share the report and other Power BI tips, troubleshoot any issues, or review the FAQ, see [Power BI tips, FAQ, and troubleshooting](./power-bi-faq-troubleshoot.md).

## Related topic

[Access query results and modify existing queries](/viva/insights/advanced/analyst/query-results.md)
