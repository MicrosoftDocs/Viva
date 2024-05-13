---
ms.date: 03/02/2023
title: Business resilience report
description: Learn how to use the Microsoft Viva Insights Power BI template to compare employee behavior before and after a business transition
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

# Business resilience report

The **Business resilience report** uses a template populated by Viva Insights data to compare employee behavior before and after a business transition.

With this report, you can visualize and explore the following top-level business questions asked by leaders:

* How are collaboration activities changing?
* How has manager coaching changed over time?
* How have internal relationships changed over time?
* Are external relationships being maintained?

Each report page includes a **Why this matters** interpretation, **recommended actions**, and **metric definitions**.

To populate the report in Power BI, you’ll need to set up and successfully run the predefined **Business resilience** query in Viva Insights.

[!INCLUDE [Demonstration](includes/demonstration.md)]

> [!VIDEO https://msit.powerbi.com/view?r=eyJrIjoiY2RmYWY4YmYtMTdhZC00MTZkLWEwZmMtMDA5ZTczNTIyODI5IiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9]

[!INCLUDE [Prerequisites](includes/prerequisites.md)]

[!INCLUDE [Report setup and run query](includes/report-setup-run-query.md)]

1. In the Viva Insights analyst experience, select **Analysis**.
2. Under **Power BI templates**, navigate to **Business resilience** and select **Start analysis**. For more information about the Business resilience template before running your analysis, select **Learn more**.
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

After the Business resilience report is set up and populated with Viva Insights data in Power BI, you’ll be prompted to select **Baseline** and **Current** time periods, which can’t overlap.

Select **Next** after you’ve made your selections. If you change your mind later, you’ll be able to change the **Baseline** and **Current** time periods in the **Settings** page.

Then, view and set the following parameters on the **Settings** page:

|Setting|Description|
|-------|-----------|
|**Baseline**|This is the baseline for your analysis; all changes will be compared with this time period. <br><br>*Make sure the **Baseline** time period precedes and doesn’t overlap with the **Current** time period. If the two time frames overlap, you'll receive a warning.*
|**Current** | This is the time period you want to compare with the **Baseline**.|
|**Select an organizational attribute to view the report by**|This is the primary group-by attribute shown in all subsequent pages. You can change this attribute at any time; all subsequent report pages will show values grouped by the new attribute.|
|**Select optional filters to exclude employee groups**|To filter the measured employee population, you can filter by any selected organizational attribute, and then filter by any of the values for these attributes. If you filter, the measured employees count will reflect a reduced number.|
|**Exclusions** | Use the check boxes to: <ul><li>Exclude employees who are likely non-knowledge workers (that is, those spending less than five hours per week on average in meetings, emails, and/or Teams calls and chats). <li>Exclude weeks that are likely holiday or paid-time-off weeks, or weeks that individuals are on other types of leave.|
|**Select the preferred language for your report** | Change the language for your report. |

## About the report

The **Business resilience report** pages, listed below, directionally highlight where a shift to remote work is having the largest impact. The reports also give you a measurable starting point to identify where leaders can use tools and processes to support employees in a new way of working. The **Glossary** defines All metrics. A **Why it matters** interpretation is also included in a text box for each report.

### Collaboration

**How are collaboration activities changing?**

Discover how employee collaboration patterns are changing in response to a shift in work patterns, and which collaboration tools people are substituting for in-person interactions. 

Transitions at work can cause changes in employee collaboration patterns as they adjust to a new normal. Groups with large increases in collaboration might be facing challenges managing their workload, while groups with significantly reduced workloads might be struggling to adapt.

### Manager coaching

**How has manager coaching changed over time?**

Learn how your business's recent transition has impacted manager coaching.

Managers are crucial factors in the development, engagement, and wellbeing of their reports and in periods of transition, managers help their reports prioritize and provide stability. However, long periods of transition could also require managers to take on new or additional responsibilities, leaving less time for them to support their teams. We recommend that individual contributors spend a minimum of one hour per month in 1:1 meetings with their managers, or 15 minutes per week on average. Employees with this level of 1:1 interaction with their managers are called *coached employees* in this report.

### Internal connections

**How have internal relationships changed over time?**

Understand employee networks are changing and how much time people spend connecting with others. 

Internal relationships are key to preventing isolation and helping employees feel supported and connected to their company’s mission, yet times of change can make it challenging to maintain existing relationships. Large decreases in network size could indicate growing isolation, while large increases could indicate either healthy relationship growth, or if networks become too large, burnout. Meanwhile, small-group conversations build networks and help employees feel less isolated.

### External connections

**Are external relationships being maintained?**

Find out how different parts of the company may have been impacted by business shifts in different ways.

Despite business changes, it’s important to ensure that relationships with continuing customers, partners, and vendors stay strong. In times of change, internal demands can take precedence over time previously spent with external contacts. Those external contacts might also be refocusing on their own critical priorities and might not have time to meet with your sales and support teams.

For groups with increased external engagement, make sure these business shifts don’t come at the expense of increased after-hours activity and work week spans. For groups experiencing a decrease, consider guiding them to proactively check in with their external contacts.

### Trends

**How are important behaviors evolving over time?** 

View trends for key leading indicator metrics for business resilience, including collaboration hours, percent of employees with at least one hour per month of manager 1:1s, internal network size, and external collaboration hours.

### Take action

Uncover opportunity areas with related best practices and recommendations and links to related articles about ways to help your managers improve in each area.

### Glossary

The **Glossary** describes metrics used in the report pages.

[!INCLUDE [Power BI tips and troubleshooting and Related topics](includes/powerbi-tips-related-topic.md)]