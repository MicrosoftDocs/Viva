---
ms.date: 03/02/2023
title: Manager effectiveness report
description: Learn how the Manager effectiveness PowerBI template from Microsoft Viva Insights helps you gain insight into the collaboration habits and effectiveness of your people managers.
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

# Manager effectiveness report

The **Manager effectiveness report** uses a template populated by Microsoft Viva Insights data to analyze people-manager behaviors in your organization. HR analysts can use this analysis to measure behaviors and trends of people managers across five key themes within your organization: manager capacity, coach, empower, connect, and model.

Each theme includes insights about manager effectiveness and ways to help maintain or increase preferred leadership behaviors. Key metrics are used to deep-dive into each theme, along with a **Why this matters** interpretation and best practices recommended by industry experts.

To populate the report in Power BI, you’ll need to set up and successfully run the predefined **Manager effectiveness** query in Viva Insights.

[!INCLUDE [Demonstration](includes/demonstration.md)]

> [!VIDEO https://msit.powerbi.com/view?r=eyJrIjoiNzY1YTI3ZmQtYjVkZi00YTA2LWI0MjEtN2MxNDQ4MGE0YmZjIiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9]

[!INCLUDE [Prerequisites](includes/prerequisites.md)]

* Have **SupervisorIndicator**, the attribute that identifies managers, included as part of your organizational data.
 
[!INCLUDE [Report setup and run query](includes/report-setup-run-query.md)]

1. In the Viva Insights analyst experience, select **Analysis**.
2. Under **Power BI templates**, navigate to **Manager effectiveness** and select **Start analysis**. To get more information about the Manager effectiveness template before running your analysis, select **Learn more**.

 3. Under **Query setup**:
    
    1. Type a **Query name**.
    1. Select a **Time period**. **Time period** defaults to **Last 6 months**.
    1. Set **Auto-refresh** (optional). You can set the query to automatically update by checking the **Auto-refresh** box. When you select the **Auto-refresh** option, your query automatically runs and computes a new result every time Viva Insights gets updated collaboration data for licensed people.
       > [!NOTE]
       > If organizational data used in an auto-refreshing query changes (for example, an attribute name is altered or an attribute is removed), the query might stop auto-refreshing.
     4. Type a **Description** (optional).   
     5. Change the metric rule (optional). To set a new metric rule, select **More settings**. Then, pick a new rule from the list. For more information about metric rules, refer to [Metric rules](../../analyst/metric-rules.md).
        > [!NOTE]
        > The **More settings** pane also contains **Group by** settings. Power BI queries are set to **Group by Week**, and you're not able to edit this field.

 1. Under **Predefined template metrics**, view the list of preselected metrics, which appear as gray tags. These metrics are required to set up the Power BI report and you can’t remove them. You can add other metrics by selecting **Add metrics**.
    > [!IMPORTANT]
    > Low-quality or missing organizational data might affect your metrics and result in warnings or errors. Learn more about data-quality notifications in [Data quality in the analyst experience](../../analyst/data-quality-analyst-experience.md).

 1. In **Select which employees you want to include in the query**, add filters to narrow down the employees in scope for your report. Don’t remove the predefined “Is Active” filter. For more details about filter and metric options, refer to [Filters](../../analyst/filters.md). If you notice a warning or error here, it's because one of your attributes is missing from your organizational data or is of low quality.
 1. Under **Select which employee attributes you want to include in the query**, add up to 14 organizational attributes, including the required **Organization** and **HireDate** attributes, and the optional **LevelDesignation** attributes. Once the query runs, you can use these attributes to group and filter the reports.
    > [!IMPORTANT]
    > This PowerBI query needs some specific attributes to run, and we've preselected them for you. These attributes appear in gray and you can't remove them. We might also include some attributes that help your template, but aren't required for your query to run. These attributes appear in blue and you can remove them.
    >
    > If you notice attributes marked with yellow warnings, that attribute's quality is low. If you notice attributes marked in red and the query's **Run** button disabled, then your organizational data is missing that attribute. 
    >
    > Learn more about attributes and data quality in [Data quality in the analyst experience](../../analyst/data-quality-analyst-experience.md).
 1. Under **Select which spotlight attributes you want to include in the query**, add at least one and up to five attributes to use as a legend for insights in the report. You’ll also be able to focus on a specific group of employees in the report. Insights for this group will be highlighted.
 1. Under **Select an attribute that indicates the employee’s engagement score**, you can optionally select an attribute that represents how engaged employees are. 
1. Select **Run** on the upper right side of the screen. The query might take a few minutes to run.
 1. When your query results are ready, go to the **Query results page** and select the Power BI icon. Download the Power BI template and get the partition and query identifiers. You’ll need these identifiers later.

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
:::image type="content" source="../../images/analyst-pbi-org-account1.png" alt-text="Screenshot that shows signing into to Power BI on the Organizational account tab":::


## Report settings

After the **Manager effectiveness report** is set up and populated with Viva Insights data in Power BI, map values as prompted, which are listed below.

|Value   |Prompt| 
|----------|----|
|Individual contributor     |Select the attribute values that identify employees as individual contributors who do not manage people within your organization      |
|Manager indicator|Select the attribute values that identify managers who manage people within your organization, such as **Mgr** and **Mgr+.**|

After this initial prompt, you can then select **Settings** at top right of any page to view and change the following parameters:

|Setting|Description|
|-------|----------|
|**Select the time period for the report** | Select the time period for which you want to view data in the report.|
|**Select an attribute to group data by** | Select the primary group-by attribute shown in all the reports. You can change this attribute at any time and all report pages will show group values by the new attribute.|
|**Select optional report filter** | Select the organizational attribute and values you want to filter the employees in the report.|
|**Exclusions** | Use the check boxes to: <ul><li>Exclude employees who are likely non-knowledge workers (that is, those spending less than five hours per week in meetings, emails, and/or Teams calls and chats). <li>Exclude weeks that are likely holiday or paid-time-off weeks or weeks that individuals are on other types of leave.|
|**Select the preferred language for your report** –| Change the language for your report.|


## About this report

The report contains one report page per theme, and each report page asks a related business question. The following section:

* Lists the report pages that fall under each theme and describes which data they contain.
* Describes the report’s **Behavioral trends** and **Take action** pages. 

### Manager capacity

**Do managers have enough time for their employees?**

Discover the weekly average number of hours that managers spent collaborating with people in the company, divided into groups and types of communication (meetings, emails, chats, and calls). Also view the average percentage of collaboration time that managers spent with direct reports as compared to others in the organization.

### Coach

**Are employees receiving sufficient coaching time with their manager?**

Analyze managers’ behavior in scheduling 1:1 time with their direct reports by groups. Metrics include monthly average number of minutes in 1:1 meetings with direct reports, percentage of employees who receive a different number of 1:1 hours with their manager, and the average frequency of 1:1 time (weekly, monthly, or quarterly).

### Empower

**Are managers balancing oversight with employee autonomy?**

View the percentage of employees whose managers co-attend their meetings and might be micromanaging them as direct reports. You can also see weekly average number of hours that managers co-attended meetings and spent in 1:1 meetings with their direct reports.

### Connect

**How well-connected are managers and do they leverage their network to help build connections for their employees?**

Find out the internal network size distribution of managers as compared to the full organizational population, calling out the share of managers who are among the top 25% most connected employees in the company. Also view the average internal network size of managers as compared to individual contributors broken out by group.

## Model

**Are managers modeling good work-life balance habits?**

View the distribution of managers by average weekly time spent in after-hours collaboration, calling out the share of managers spending more than five hours per week in collaboration outside of their set working hours. You can also see the difference in average after-hours collaboration hours for managers and individual contributors, broken out by group. 

### Behavioral trends

**How are manager behaviors evolving?**

Understand trends for key leading indicator metrics for managers, including metrics about coaching and empowerment, network connections, and after-hours work habits.

### Take action

**How can manager effectiveness be improved?** 

Review opportunity areas with related best practices and recommendations and links to related articles about ways to help your managers improve in each area.

### Glossary

The **Glossary** describes metrics used in the report pages.

[!INCLUDE [Power BI tips and troubleshooting and Related topics](includes/powerbi-tips-related-topic.md)]

