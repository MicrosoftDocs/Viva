---
ROBOTS: NOINDEX,FOLLOW
title: Wellbeing - balance and flexibility report
description: Learn how the Wellbeing - balance and flexibility PowerBI template from Microsoft Viva Insights helps you discover whether your employees maintain work-life balance and flexibility at work
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

# Wellbeing – balance and flexibility report

The **Wellbeing – balance and flexibility report** uses a template populated by Microsoft Viva Insights data to help you get insights into employee wellbeing across your company. This analysis can help you uncover opportunities to improve focus, work-life balance, flexibility at work, and employees’ sense of community.

The report includes the following pages:

* **Improve focus** – Do employees have time to focus on their core priorities?
* **Balance work and life** – Are employees able to protect personal time?
* **Handle urgency** – Can employees manage unexpected demands and proactively shift some to planned work?
* **Embrace flexibility** – Are employees adopting a flexible working schedule?
* **Take breaks** – Are employees able to mindfully disconnect?
* **Stay connected** – Are employees part of a community at work?

![Wellbeing report, Report settings](/viva/insights/advanced/images/wellbeing-PBI-summary.png)

Each report includes a **Why it matters** section that explains the business implications, best practices, and recommended actions to help maintain or improve employee wellbeing.

To populate the report in Power BI, you’ll need to set up and successfully run the predefined **Wellbeing - balance and flexibility** query in Viva Insights.

## Demonstration

The following demonstration uses sample data that’s only representative of this report and might not be exactly what you see in a live report specific to your organization's unique data.

<iframe title="Wellbeing - Summary" width="600" height="373.5" src="https://msit.powerbi.com/view?r=eyJrIjoiNTcwNGQwMTctYWUwYy00MjAwLThlM2YtYTIwMWI4ZGEwZTg0IiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9" frameborder="0" allowFullScreen="true"></iframe>

## Prerequisites

Before you can run the queries and populate the report in Power BI, you’ll need to:

* Be assigned the role of Insights Analyst in Viva Insights.
* Have the June 2022 (or newer) version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://powerbi.microsoft.com/en-us/getting-started-with-power-bi/) to download and install the latest version.

## Report setup

### Run query

>[!Note]
> For this release of Viva Insights, this report is currently only available in English and will only work with data generated from the English version of Viva Insights.

1. In the Viva Insights Analyst experience, select **Analysis**.

2. Under **Power BI templates**, navigate to **Wellbeing - balance and flexibility** and select **Start analysis**. To get more information about the Wellbeing - balance and flexibility template before running your analysis, select **Learn more**.

    ![Wellbeing query start](/viva/insights/advanced/images/wellbeing-pbi-start.png)

3. Under **Query setup**:
    1. Type a **Query name**.
    1. Select a **Time period**. **Time period** defaults to **Last 3 months**.
    1. Optional: You can set the query to automatically update by checking the **Auto-refresh** box. When you select the **Auto-refresh** option, your query automatically runs and computes a new result every Viva Insights gets updated collaboration data for licensed people.

    >[!Note]
    >If the organizational data used in an auto-refreshing query changes (for example, an attribute name is altered or an attribute is removed), you might see an error when you run the query.

    4. Optional: Type a **Description**.
    
        Selecting **More settings** brings you to a pane, but there’s nothing you need to change there. In this pane:

        * Power BI queries are set to **Group by Week**. Do not change this **Group by** designation.
        * The **Metric rules** field defaults to **Meeting exclusions rule (preferred rule)**. This field isn’t customizable in this release; for more information, refer to [Metric rules](../metric-rules.md).
![Wellbeing query setup](/viva/insights/advanced/images/wellbeing-pbi-setup.png)

4. **In Predefined template metrics**, leave prepopulated metrics as they appear.  
![Wellbeing query predefined metrics](/viva/insights/advanced/images/wellbeing-pbi-predefined-metrics.png)

    >[!Note]
    > Metrics in Power BI templates can't be edited in this release of Viva Insights. To expand the full list of metrics included in the Power BI template, select the arrow in the box beneath Metrics, filters, and organizational attributes.

5. You can filter the employees in scope for the report under **Select which employees you want to include in the query**. Don’t remove the predefined “Is Active” filter. For more details about filter and metric options, see [Person queries](../person-query.md).

    ![Is active filter](/viva/insights/advanced/images/pbi-templates-isactive-filter.png)

6. Under **Select which employee attributes you want to include in the query**, add up to seven organizational attributes. Once the query runs, you can use these attributes to group and filter the reports.

7. Select **Run** on the upper right side of the screen, which can take a few minutes to complete.

8. When your query results are ready, go to the **Query results** page and select the **Power BI** icon to download the Power BI template and copy the query identifier. You'll need the query identifier later.

### Link report to query

9. Open the downloaded Wellbeing - balance and flexibility template.

10. If prompted to select a program, select **Power BI**.

11. When prompted by Power BI:
    1. Paste in the query identifier.
    1. Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Viva Insights data.
    1. Select **Load** to import the query results into Power BI.

12. If prompted by Power BI, sign in using your organizational account. Power BI then loads and prepares the data, which can take a few minutes to complete for large files.

>[!Important]
> You must sign in to Power BI with the same account you use to access Viva Insights.

## Report settings

After the **Wellbeing - balance and flexibility** report is set up and populated with Viva Insights data in Power BI, review information on the **Summary** page. Then, view and set the following parameters on the **Settings** page. You can find **Settings** on the right panel of the introduction page. You can also adjust the report settings as you go through the report pages through the Settings icon.

![Wellbeing report summary page](/viva/insights/advanced/images/wellbeing-pbi-summary.png)

* **Select the time period to measure** – This is the time period that you want to analyze. Note that the four-week trend information on the summary page won’t show if the selected time period is less than eight weeks.
* **Select an organizational attribute to view the report by** – The primary "group-by" attribute shown in all subsequent reports. You can change this attribute at any time and all subsequent report pages will show group values by the new attribute.
* **Select optional filters to exclude employee groups** – To filter the measured employee population, you can filter by any selected organizational attribute, and then filter by any of the values for these attributes. If you use filters, the measured employees count will represent a reduced number. Measured employees are the number of employees in the filtered population who were active during the specified time period. Active employees are those who send at least one email or instant message during a work week that's included in the current time period.
* **Exclude weeks marked with a holiday indicator** – Select to exclude unusually low collaboration weeks based on individual collaboration patterns. These low collaboration weeks usually occur when employees are taking time off from work.
* **Exclude non-knowledge workers** – Select to exclude employees who spend a weekly average of no more than five hours in meetings, emails, instant messages, and calls because they’re unlikely to be knowledge workers or they don’t use Outlook or Teams.

### Customize working hours

For **Embrace flexibility** and **Take break** pages, you can customize the standard working hours for your organization as a baseline. Select **Customize working hours**, and then select the standard start time and end time. Employees’ collaboration patterns will then be compared with these time settings.

![Wellbeing report customize standard working hours page](/viva/insights/advanced/images/wellbeing-pbi-workinghours.png)

## About this report

The **Wellbeing - balance and flexibility** report includes the following report pages that help you identify your employees' wellbeing across the company.

### Improve focus

This page shows the average weekly collaboration hours for each employee by organization as compared to focus hours. This view highlights how an employee's collaboration load is impacting their focus time.

### Balance work and life

This page shows the average weekly after-hours collaboration for each employee, the distribution of employees by their after-hours collaboration, and percentage of employees that were active during the weekends at least once every four weeks. Understanding employees' after-hours and weekend work behaviors can uncover opportunities to protect the boundary between work and personal life.

### Handle urgency

This page shows the percentage of employees and work weeks involved in urgent collaboration and the impact of urgent collaboration on employees' after-hours collaboration patterns. Urgent collaboration is defined by keywords such as "urgent" in the email subject lines or meeting invitation titles. The list of these keywords is provided in the report. This report highlights how unexpected demands are managed in your company and unlocks opportunities to shift some of them to planned work.

### Embrace flexibility

This page highlights three key aspects that help you identify employees' flexibility at work:

* **Flexible start times** – Shows the percentage of weeks in which the employees have at least one day of flexible start time in a week.
* **Recurring time to disconnect** – Shows the percentage of weeks in which the employees take at least one hour of recurring break each day over the week.
* **Control active hours** – Shows the percentage of weeks in which the employees limit their work activities to their expected working hours over the week. If the employees have a standard work schedule from 9:00 AM to 5:00 PM, their expected working hours for each day is eight hours. This analysis provides insights into how employees are adopting flexible working schedules.

>[!Tip]
>
>You can customize work hours in the upper right of this page, next to **Settings**.

### Take breaks

This page shows the percentage of weeks in which an average employee falls under each activity pattern by organization. Defined by collaboration hour blocks and whether recurring breaks are taken, the activity patterns indicate how employees arrange their weekly work schedule. This information provides opportunities to identify groups that may experience burnout and struggle to disconnect from work.

>[!Tip]
>
>You can customize work hours in the upper right of this page, next to **Settings**.

### Stay connected

This page highlights how employees connect with colleagues through small group meetings and informal communication. Understanding the average weekly meeting hours an employee spent in small group meetings and the distribution of emails and chats by type of colleagues they interact with can provide insights about whether employees are forming communities and rapport at work.

### Other pages

The report also includes:

* A **Behavioral trends** page that tracks key metrics over time
* A **Take action** page that provides actionable recommendations to improve behaviors
* An **Explore further** page that highlights the research and studies in each topic
* A **Glossary page** that describes all the metrics in the report

## Power BI tips, FAQs, and troubleshooting

For details about how to share the report and other Power BI tips, troubleshoot any issues, or review the FAQ, see [Power BI tips, FAQ, and troubleshooting](./power-bi-faq-troubleshoot.md).

## Related topic

[Access query results and modify existing queries](/viva/insights/advanced/analyst/query-results.md)