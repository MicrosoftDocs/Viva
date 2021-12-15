---
ROBOTS: NOINDEX,NOFOLLOW
title: Employee wellbeing dashboard
description: Use the Employee wellbeing dashboard to visualize insights into employee wellbeing across the company
author: madehmer
ms.author: v-mideh
ms.topic: article
ms.localizationpriority: medium 
ms.collection: m365initiative-viva-insights 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Employee wellbeing

The Employee wellbeing report uses a template that's populated by Viva Insights data to help you get insights into employee wellbeing across your company and uncover opportunities to improve focus, work-life balance, flexibility at work, and employee's sense of community.

The report covers the following topics:

* **Improve focus** &ndash; Do you have time to focus on your core priorities?
* **Balance work and life** &ndash; Are you able to protect personal time?
* **Handle urgency** &ndash; Can you manage unexpected demands and proactively shift some to planned work?
* **Embrace flexibility** &ndash; Are you adopting a flexible working schedule?
* **Take breaks** &ndash; Are you able to mindfully disconnect?
* **Stay connected** &ndash; Are you part of a community at work?

Each page includes a Why this matters flyout that explains the business implication of the topic and best practices or recommended actions to improve employee wellbeing.

To populate the dashboard in PowerBI, you must set up and successfully run the predefined Employee wellbeing query and Hourly collaboration query in Viva Insights.

After you successfully run these queries, you can download the template from the Employee wellbeing query on the Results page. After you download the template, you can then connect the query data from Viva Insights to the dashboard in PowerBI.

## Demonstration

The following demo uses sample data that is only representative of this dashboard and might not be exactly what you see in a live dashboard specific to your organization's unique data.

<br><iframe width="800" height="486" src="https://msit.powerbi.com/view?r=eyJrIjoiM2ZiY2Y4M2YtMTMyNi00NWY1LWEyMjctYTY2OTdlOWQzNDhhIiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9&embedImagePlaceholder=true&pageName=ReportSectionbbd7dee40bcdeee460e6" frameborder="0" allowFullScreen="true"></iframe>

To find the template for the Employee wellbeing report, go to the [Query designer](https://workplaceanalytics.office.com/en-us/Analyze/QueryDesigner/NewQuery). For complete steps, see [Set up the report](#set-up-the-report).

## Prerequisites  

Before you can run the queries and populate the dashboard in Power BI, you must:

* Be assigned the role of [Analyst](../use/user-roles.md) in Workplace Analytics.
* Have the latest version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t?activetab=pivot:overviewtab) to download and install the latest version.

## Set up the report

>[!Note]
>This dashboard is currently only available in English and will only work with data generated from the English version of Workplace Analytics. Before running the required queries, confirm or change the browser language to **en-us** in the app's URL: <https://workplaceanalytics.office.com/en-us/Home/>

1. In [Viva Insights](https://workplaceanalytics.office.com/), select **Analyze** > **Query designer**.

2. In **Create** > **Other templates**, select **Employee wellbeing** to see the required setup steps, and then in step 2, select **Set up**.

<!--  UPDATE THIS IMAGE -->
   ![Business continuity template.](../Images/WpA/Tutorials/bc-setup-step2.png)

3. When prompted, confirm the following settings:

   * **Name** &ndash; Customize or keep the default name
   * **Group by** &ndash; Week
   * **Time period** &ndash; Select the time period you want to analyze
   * **Auto-refresh** &ndash; Keep this setting disabled by default. Turn it on only if you plan to track indicators on a weekly basis.
   * **Meeting exclusions** &ndash; Select the preferred rule for your tenant

<!-- Insert screenshot of Employee wellbeing query content -->

  >[!Important]
  >If you try to delete a predefined metric, you'll see a warning that the deletion might disable portions of the Power BI dashboard and reduce query results. In turn, this can limit your ability to visualize employee wellbeing patterns. Depending on the metric you delete, you might disable a single Power BI chart, several charts, or all the charts. Select **Cancel** to retain the metric.

 4. For **Select filters**, select **Active only** for "**Which measured employees do you want to include?**" Optionally, you can further filter the employees in scope for the dashboard. For more details about filter and metric options, see [Create a person query](./person-queries.md#create-a-person-query).

4. For **Organizational data**, keep the preselected **Organization** and **LevelDesignation** attributes that the dashboard requires.

   >[!Important]
   >If you remove the required, preselected Organizational data attributes, you might disable one or more Power BI charts.

5. Select any additional attributes (columns) that you want to include in the reports.
6. Select **Run** to run the query, which might take a few minutes to complete.
7. When prompted, return to Query designer, and then repeat  **Steps 3-7** for the **Hourly collaboration** query, which requires the same selections as for Employee wellbeing.

   >[!Important]
   >If you try to delete a predefined metric, you'll see a warning that the deletion might disable portions of the Power BI dashboard and reduce query results. In turn, this can limit your ability to visualize employee wellbeing patterns. Depending on the metric you delete, you might disable a single Power BI chart, several charts, or all the charts. Select **Cancel** to retain the metric.

9. When prompted, continue to **Results**. After both queries successfully run, select the **Download** icon for the **Employee wellbeing** query results, select **PBI template**, and then select **OK** to download the template.

<!-- VERIFY THIS SCREENSHOT OF QUERY RESULTS-->

   ![template download.](../Images/WpA/Tutorials/pbi-template-download.png)

10. Open the downloaded **Employee wellbeing** template.
11. If prompted to select a program, select **Power BI**.
12. When prompted by Power BI, copy and paste the OData links for both queries into their respective fields.

    a. In the Viva Insights **Query designer** > **Results** page, select the **Link** icon for each query, and select to copy the generated OData URL link.
    
    b. In Power BI, paste each copied link into its respective field.
     
    c. Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Viva Insights data.
     
    d. Select **Load** to import the query results into Power BI. Loading these large files may take some time to complete.

<!-- VERIFY THIS SCREENSHOT OF THE TEMPLATE POP-UP WINDOW -->

  ![Query URLs for Power BI.](../Images/WpA/Tutorials/odata-link-2.png)

13. If you're already signed in to Power BI with your Workplace Analytics organizational account, the dashboard visualizations will populate with your data: You are done and can skip the following steps. If not, proceed to the next step.

14. If you're not signed in to Power BI, or if an error occurs when updating the data, sign in to your organizational account again. In the **OData feed** dialog box, select **Organizational account** and then select **Sign in**. See [Troubleshooting](../tutorials/power-bi-templates.md#troubleshooting) for more details.

<!-- VERIFY THIS SCREENSHOT OF THE CREDENTIAL WINDOW -->

   ![Power BI sign in.](../Images/WpA/Tutorials/pbi-sign-in.png)

15. Select and enter credentials for the organizational account that you use to sign in to Viva Insights, and then select **Save**.

    >[!Important]
    >You must sign in to Power BI with the same account you use to access Viva Insights.

16. Select **Connect** to prepare and load the data, which can take a few minutes to complete.

<!-- INCLUDE THE FOLLOWING TIP? -->

>[!Tip]
>If you have preexisting query results that the dashboard is no longer using, a best practice that reduces processing time is to turn off the auto-refresh or delete the queries that the dashboard is no longer using. See [Stop auto-refresh](../Tutorials/Query-auto-refresh.md#stop-auto-refresh) for details.

## Report settings

After the Employee wellbeing report is set up and populated with Viva Insights data, as a first step to viewing data in the dashboard, view and set the following parameters on the **Settings** page. You can find **Settings** on the right panel of the introduction page. You can also adjust the report settings as you go through the report pages through the **Settings** icon.

<!-- (Insert screenshot of intro page settings)

(Insert screenshot of content page settings)
-->

* **Select the time period to measure** &ndash; This is the time period that you want to analyze.
* **Select an organizational attribute to view the report by** &ndash; The primary "group-by" attribute shown in all subsequent reports. You can change this attribute at any time and all subsequent report pages will show group values by the new attribute.
* **Select optional filters to exclude employee groups** &ndash; To filter the measured employee population, you can filter by any selected organizational attribute, and then filter by any of the values for these attributes. If you use filters, the measured employees count will reflect a reduced number. Measured employees reflect the number of employees in the filtered population who were active during the specified time period. Active employees are those who sent at least one email or instant message during a work week included in the current time period.
* **Exclude weeks marked with a holiday indicator** &ndash; You can check the box to exclude unusually low collaboration weeks based on individual collaboration patterns. These low collaboration weeks usually occur when employees are taking time off from work.
* **Exclude non-knowledge workers** &ndash; You can check the box to exclude employees who spent a weekly average of less than five hours in meetings, email, instant messages, and calls because they are likely non-knowledge workers or they do not use Outlook or Teams.
After confirming the settings, check the number of measured employees to confirm this is the population you want to analyze. 

<!-- Add a paragraph about the standard time settings -->

## About the report

The Employee wellbeing report includes the following report pages that help you identify your employees' wellbeing across the company.

* **Improve focus** &ndash; Shows the average daily collaboration hours for each employee by organization as compared to focus hours. This highlights how an employee's collaboration load is impacting their focus time.
* **Balance work and life** &ndash; Shows the average daily after-hours collaboration for each employee, the distribution of employees by their after-hours collaboration, and percentage of employees that were active during the weekends at least once every four weeks. Understanding employees' after-hours and weekend work behaviors can uncover opportunities to improve their work-life balance.
* **Handle urgency** &ndash; Shows the percentage of employees and work weeks involved in urgent collaboration and the impact of urgent collaboration on employees' after-hours collaboration patterns. Urgent collaboration is defined by keywords such as "urgent" in the email subject lines or meeting invitation titles. The list of these keywords is provided in the report. This highlights how unexpected demands are managed in your company and unlocks opportunities to shift some of them to planned work.
* **Embrace flexibility** &ndash; Highlights three key aspects that help you identify employees' flexibility at work:
   * **Flexible start times** &ndash; Shows the percentage of weeks in which the employees have at least one day of flexible start time in a week.
   * **Recurring time to disconnect** &ndash; Shows the percentage of weeks in which the employees take at least one hour of recurring break each day over the week.
   * **Control active hours** &ndash; Shows the percentage of weeks in which the employees limit their work activities to their expected working hours over the week. If the employees have a standard work schedule from 9:00 AM to 5:00 PM, their expected working hours for each day is eight hours.
This analysis provides insights about how employees are adopting flexible working schedules.
* **Take breaks** &ndash; Shows the percentage of weeks in which an average employee falls under each activity pattern by organization. Defined by collaboration hour blocks and whether recurring breaks are taken, the activity patterns indicate how employees arrange their weekly work schedule. This information provides opportunities to identify groups that may experience burnout and struggle to disconnect from work.
* **Stay connected** &ndash; Highlights how employees connect with colleagues through small group meetings and informal communication. Understanding the average weekly meeting hours an employee spent in small group meetings and the distribution of emails and chats by type of colleagues they interact with can provide insights about whether employees are forming communities and rapport at work.

The dashboard also includes:

* A **Behavioral trends** page that tracks key metrics over time
* A **Take action** page that provides actionable recommendations to improve behaviors
* An **Explore further** page that highlights the research and studies in each topic
* A **Glossary** page that describes all the metrics in the report

## Power BI tips, troubleshooting, and FAQs

For details about how to share the dashboard and other Power BI tips, troubleshoot any issues, or review the FAQ, see [Power BI tips, FAQ, and troubleshooting](../tutorials/power-bi-templates.md).

## Related topic

[View, download, and export query results](../use/view-download-and-export-query-results.md)
