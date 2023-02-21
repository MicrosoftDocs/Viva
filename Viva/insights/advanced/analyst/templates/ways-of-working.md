---
ms.date: 02/20/2023
title: Ways of working report
description: Learn how the Ways of working PowerBI template from Microsoft Viva Insights helps you explore collaboration, meeting, wellbeing, and coaching patterns.
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

# Ways of working report

The **Ways of working** report uses a template populated by Viva Insights data to conduct a broad diagnostic of a company’s collaboration patterns, meeting effectiveness, wellbeing, and coaching to uncover areas for improvement. The pages in the report help you answer these business questions: 

* **Understand collaboration patterns**
    * How much time are employees spending using digital collaboration tools? 
    * How much time are people spending in different collaboration modes? 
* **Make meetings effective** 
    * How is the organization spending its meeting time? 
    * How much time is the organization spending in recurring meetings? 
    * Does habit or necessity drive multitasking? 
* **Improve wellbeing** 
    * Are employees getting enough time to work on their core priorities? 

* **Encourage coaching and development** 
    * Are employees getting enough 1:1 coaching time with their managers?
    * Are managers balancing oversight with employee autonomy? 

To populate the report in Power BI, you’ll need to set up and successfully run the predefined **Ways of working** query in Viva Insights. 

## Demonstration

The following demonstration uses sample data that’s only representative of this report and might not be exactly what you see in a live report specific to your organization's unique data.

<iframe title="Ways of Working - Summary" width="600" height="373.5" src="https://msit.powerbi.com/view?r=eyJrIjoiYWE0MGExNGEtMmIwNC00ZDg4LWI4MmYtYWM2Yjc0NzAzMmI2IiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9" frameborder="0" allowFullScreen="true"></iframe>

## Prerequisites

Before you can run the queries and populate the report in Power BI, you’ll need to:

* Be assigned the role of **Insights Analyst** in Viva Insights.
* Have the June 2022 (or newer) version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://powerbi.microsoft.com/en-us/getting-started-with-power-bi/) to download and install the latest version.

## Report setup

### Run query

>[!Note]
> For this release of Viva Insights, this report is currently only available in English and will only work with data generated from the English version of Viva Insights.

1. In the Viva Insights analyst experience, select **Analysis**.

2. Under **Power BI templates**, navigate to **Ways of working** and select **Start analysis**. To get more information about the Ways of working template before running your analysis, select **Learn more**.

    ![Screenshot that shows the Ways of working icon.](/viva/insights/advanced/images/wow-pbi-start.png)

3. Under **Query setup**:
    1. Type a **Query name**.
    1. Select a **Time period**. **Time period** defaults to **Last 3 months**.
    1. Optional: You can set the query to automatically update by checking the **Auto-refresh** box. When you select the **Auto-refresh** option, your query automatically runs and computes a new result every time Viva Insights gets updated collaboration data for licensed people.

    >[!Note]
    >If the organizational data used in an auto-refreshing query changes (for example, an attribute name is altered or an attribute is removed), you might see an error when you run the query.

    4. Optional: Type a **Description**.
    
        Selecting **More settings** brings you to a pane, but there’s nothing you need to change there. In this pane:

        * Power BI queries are set to **Group by Week**. You can't edit this field.
        * The **Metric rules** field defaults to **Meeting exclusions rule (preferred rule)**. This field isn’t customizable in this release; for more information, refer to [Metric rules](../metric-rules.md).
![Screenshot that shows the Query setup section.](/viva/insights/advanced/images/wow-pbi-setup.png)

4. **In Predefined template metrics**, leave prepopulated metrics as they appear.  
![Screenshot that shows predefined query metrics.](/viva/insights/advanced/images/wow-pbi-predefined-metrics1.png)

    >[!Note]
    > Metrics in Power BI templates can't be edited in this release of Viva Insights. To expand the full list of metrics included in the Power BI template, select the arrow in the box beneath **Metrics, filters, and organizational attributes**.

5. You can filter the employees in scope for the report under **Select which employees you want to include in the query**. Don’t remove the predefined “Is Active” filter. For more details about filter and metric options, see [Create a Custom Person query](../person-query.md).

    ![Screenshot that shows the Is active filter.](/viva/insights/advanced/images/pbi-templates-isactive-filter.png)

6. Under **Select which employee attributes you want to include in the query**, add up to seven organizational attributes. Once the query runs, you can use these attributes to group and filter the reports.

    >[!Important]
    >Some employee attributes are required to set up this Power BI template, which are preselected for you in the query. *Don't remove any preselected attributes.*
    >
    >If you see attributes marked in red and the query’s **Run** button disabled, it means that these required attributes are missing from your organizational data. Contact your admin to upload them.

7. Select **Run** on the upper right side of the screen, which can take a few minutes to complete.

8. When your query results are ready, go to the **Query results** page and select the **Power BI** icon to download the Power BI template and copy the query identifier. You'll need the query identifier later.

### Link report to query

9. Open the downloaded **Ways of working** template.

10. If prompted to select a program, select **Power BI**.

11. When prompted by Power BI:
    1. Paste in the query identifier.
    1. Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Viva Insights data.
    1. Select **Load** to import the query results into Power BI.

12. If prompted by Power BI, sign in using your organizational account. Power BI then loads and prepares the data, which can take a few minutes to complete for large files.

>[!Important]
> You need to sign in to Power BI with the same account you use to access Viva Insights.

## Report settings

After the **Ways of working** report is set up and populated with Viva Insights data in Power BI, review information on the **Summary** page. Then, view and set the following parameters on the **Settings** page:

* **Select the time period for the report** – Select the time period for which you want to view data in the report.  
* **Select an attribute to group data by** – Select the primary group-by attribute shown in all the reports. You can change this attribute at any time and all report pages will show group values by the new attribute.
* **Select optional report filter** – To filter the measured employee population, you can filter by any selected organizational attribute, and then filter by any of the values for these attributes. If you use filters, the measured employees count will reflect a reduced number. Measured employees reflect the number of employees in the filtered population who were active during the specified time period. Active employees are those who’ve sent at least one email or Teams chat during a work week included in the current time period.
* **Exclusions** – Use the check boxes to:
    * Exclude employees who are likely non-knowledge workers (that is, those spending less than five hours per week in meetings, emails, and/or Teams calls and chats).
    * Exclude weeks that are likely holiday or paid-time-off weeks or weeks that individuals are on other types of leave.

After confirming the settings, check the number of measured employees to confirm this is the population you want to analyze.

![Screenshot that shows the Report settings page in Power BI.](/viva/insights/advanced/images/wow-pbi-report-settings.png)

## About this report

The **Ways of working** report includes the following report pages that help you assess your company's collaboration culture and employee experience. 

### Understand collaboration patterns 

<!--#### Collaboration baseline and after-hours collaboration

*How much time are employees spending using digital collaboration tools?* 

This page compares the average weekly collaboration hours for each person by group to after-hours collaboration. This information highlights how collaboration load is impacting after-hours work.-->

|Page name|Business question| Page function|
|----|----------|---------------|
|Collaboration baseline and after-hours collaboration |*How much time are employees spending using digital collaboration tools?*| Compares the average weekly collaboration hours for each person by group to after-hours collaboration. This information highlights how collaboration load is impacting after-hours work.
|Collaboration modes |How much time are people spending in different collaboration modes? |This page displays, by group, the average number of hours per week that people are spending in:<ul><li>Meetings.<li>Email.<li>Teams chats.<li>Teams unscheduled calls.


#### Collaboration modes

**How much time are people spending in different collaboration modes?** 

This page displays, by group, the average number of hours per week that people are spending in:

* Meetings.
* Email.
* Teams chats.
* Teams unscheduled calls.

Toggle between total collaboration or after-hours collaboration. Understanding differences between how teams get work done can uncover both replicable best practices and areas of opportunity.

### Make meetings effective

#### Long or large meetings

**How is the organization spending its meeting time?** 

This page shows the percentage of time spent in the different meeting types by the number of invitees, including the meeting organizer, and duration, highlighting how the organization spends its meeting time. Analyzing meeting practices at the organizational level can help pinpoint sources of meeting overload to streamline or those groups with successful meeting best practices that could be replicated across the company.

#### Recurring meeting hours

**How much time is the organization spending in recurring meetings?** 

This page shows the time spent in recurring meetings, by meeting categories. Large or long recurring meetings are easy candidates to streamline by reducing the number of invitees or the meeting frequency or duration.

#### Multitasking

**Does habit or necessity drive multitasking?** 

This page shows the distribution of employees by their average collaboration hours and average multitasking rate—the percentage of meetings and Teams calls hours where they’ve multitasked. This analysis helps determine whether multitasking rates during meetings are a function of habit or a consequence of lacking enough free time during the workday to catch up on email outside of meetings. 

### Improve wellbeing 

#### Uninterrupted focus hours 

**Are employees getting enough time to work on their core priorities?** 

This page shows the average available-to-focus hours—time without any scheduled meetings during working hours—and uninterrupted hours—time without any scheduled meetings during working hours not interrupted by email or Teams chat or calls.

### Encourage coaching and development

#### Manager 1:1 time & frequency

**Are employees getting enough 1:1 coaching time with their managers?** 

This page shows the distribution of employees by how much weekly 1:1 time they get with their managers. This information highlights whether employees are getting enough 1:1 manager coaching.

### Empower your workforce

**Are managers balancing oversight with employee autonomy?** 

This page shows the distribution of employees attending the same meetings as their managers and their average weekly 1:1 meeting time with their managers, which is compared across the company. It also analyzes different segments of manager behaviors based on their rates of attending the same meeting as their reports and their 1:1 meeting time.

### Behavioral trends

This page shows the trends for key leading indicator metrics.

### Take action

This page lists opportunity areas with related best practices and recommendations and links to related articles about ways to help your managers improve in each area. 

### Glossary

The report also includes a **Glossary** page that describes all the report metrics.

## Power BI tips, FAQs, and troubleshooting

For details about how to share the report and other Power BI tips, troubleshoot any issues, or review the FAQ, see [Power BI tips, FAQ, and troubleshooting](./power-bi-faq-troubleshoot.md).

## Related topic

[Access query results and modify existing queries](/viva/insights/advanced/analyst/query-results.md)

