---
title: Sales effectiveness dashboard for Power BI
description: Use the Sales effectiveness dashboard to visualize predefined data from Viva Insights in Power BI
author: madehmer
ms.author: loreenl
ms.topic: article
ms.localizationpriority: medium 
ms.prod: wpa
manager: scott.ruble
audience: Admin
---

# Sales effectiveness

The Sales effectiveness dashboard for Power BI that’s populated by Microsoft Viva Insights data to help you understand how your sales employees collaborate with external parties and identify opportunities to improve sales effectiveness in your organizations.

Part of the report requires CRM data for advanced insights about CRM account collaboration. For details about how to prepare and upload CRM data into into the advanced insights app, see [Upload CRM data](/viva/insights/setup/crm-data-upload?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json). Without CRM data, you can still run the report and access an external collaboration baseline for your organizations. Any collaborators with an external domain are defined as external collaborators.

The dashboard includes the following reports.

**External domains (No CRM data required)**:

1. **Collaboration baseline** - How much overall collaboration do employees have with external parties?
2. **Meeting engagement** - What are the employee meeting interactions with external parties?

**CRM account domains (CRM data required)**:

3. **Account collaboration baseline** - How much overall collaboration do employees have with CRM accounts?
4. **Cross-role engagement** - Which employee roles are engaging most with our CRM accounts?
5. **Meaningful engagement** - Are employees meaningfully engaging with CRM accounts?
6. **Account collaboration list** - Which accounts are most invested in?
7. **Account collaboration snapshot** - How are employees collaborating with specific accounts?

![Sales effectiveness dashboard in Power BI.](../Images/WpA/tutorials/pbi-sales-summary.png)

Each report includes a **Why this matters** section that explains the business implications, best practices, and recommended actions to improve sales effectiveness.

To populate the dashboard in Power BI, you must set up and successfully run the predefined **Sales effectiveness** query in the Query designer. To see CRM account collaboration details, you must also run the predefined **CRM collaboration** query.

After you successfully run it, you can download the template from the **Sales effectiveness** query on the **Results** page. After you download the template, you can then connect the query data to the dashboard in Power BI.

When the dashboard is populated with your data, you can use it to visualize, explore, and report about workplace patterns and trends relating to sales or other external-facing groups.

## Demonstration

The following demo uses sample data that is only representative of this dashboard and might not be exactly what you see in a live dashboard specific to your organization's unique data.

<iframe title="Sales effectiveness - Introduction" width="800" height="486" src=https://msit.powerbi.com/view?r=eyJrIjoiZDEyMjVmYmYtMmQyMy00M2ExLWFkNTMtZWI2MjhiODlkNTFhIiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9&embedImagePlaceholder=true frameborder="0" allowFullScreen="true"></iframe>

To find the template for the Sales effectiveness dashboard for Power BI, go to the [Query designer](https://workplaceanalytics.office.com/en-us/Analyze/QueryDesigner/NewQuery). (If that link doesn't work, try [this link instead](https://workplaceanalytics-eu.office.com/en-us/Analyze/QueryDesigner/NewQuery).) For complete steps, see [Set up the dashboard](#set-up-the-dashboard).

## Prerequisites

Before you can run the query and populate the dashboard in Power BI, you must:

* Be assigned the role of [Analyst](/viva/insights/use/user-roles?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) in the advanced insights app.
* Have the latest version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t?activetab=pivot:overviewtab) to download and install the latest version.

>[!Note]
>For best results, you must have CRM data available. Without it, insights about account collaboration will be unavailable. For instructions, see [Upload CRM data](/viva/insights/setup/crm-data-upload?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

## Set up the dashboard

>[!Note]
>This dashboard is currently only available in English and will only work with data generated from the English version of the app. Before running the required queries, confirm the browser language in the app's URL includes **en-us**, or change it to include **en-us**: ...office.com/en-us/...

1. In [the app](https://workplaceanalytics.office.com/)(if that link doesn't work, try [this link instead](https://workplaceanalytics-eu.office.com/)), select **Analyze** > **Query designer**.
2. In **Create** > **Other templates**, select **Sales effectiveness** to see the required setup steps, and then in Step 2, select **Set up** for **Sales effectiveness** (or for **CRM collaboration** from **Step 8**).

    ![Power BI Sales setup steps](../Images/WpA/tutorials/pbi-sales-setup.png)

3. When prompted, confirm the following settings:

   * **Name** - Customize or keep the default name
   * **Group by** - Week
   * **Time period** - Select the time period you want to analyze
   * **Auto-refresh** – Keep this setting disabled by default. Turn it on only if you plan to track indicators on a weekly basis.
   * **Meeting exclusions** - Select the preferred rule for your tenant

   >[!Important]
   >If you try to delete a predefined metric, you'll see a warning that the deletion might disable portions of the Power BI dashboard and reduce query results. In turn, this can limit your ability to visualize employee wellbeing patterns. Depending on the metric you delete, you might disable a single Power BI chart, several charts, or all the charts. Select **Cancel** to retain the metric.

4. In **Select filters**, confirm **Active only** is set for **Which measured employees do you want to include in your query results**. When possible, filter the employees to the sales group or external-facing employees for the dashboard. For details about filters and metrics, see [Create a Person Query](/viva/insights/tutorials/person-queries?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).
5. In **Organizational data**, keep the preselected **LevelDesignation** and **Organization** attributes that the dashboard requires.

   >[!Important]
   >If you remove these required, preselected Organizational data attributes, you might disable one or more Power BI charts.

6. You can then select any additional attributes (columns) that you want to include in the reports, such as the following:

   * An attribute that identifies the job titles or roles among sales employees, which can be leveraged to understand role-based work patterns and teaming models.
   * An attribute that identifies top performers. Performance can be based on sales quota attainment or any other outcome criteria your organization uses. This can be leveraged to discover work behaviors and best practices among the top performers.
   * An attribute that identifies the sales regions or customer segments, which can be leveraged to understand region-specific or segment-specific work patterns.

7. Select **Run** (at top right) to run the query, which can take a few minutes up to a few hours to complete.
8. To use CRM data in the dashboard, select to return to the Query designer and set up the **CRM collaboration** query. Skip **Steps 9-12** if not running the CRM collaboration query.
9. Repeat **Step 3** for the query settings.

   >[!Important]
   >If you try to delete a predefined metric, you'll see a warning that the deletion might disable portions of the Power BI dashboard and reduce query results. In turn, this can limit your ability to visualize employee wellbeing patterns. Depending on the metric you delete, you might disable a single Power BI chart, several charts, or all the charts. Select **Cancel** to retain the metric.

10. In **Time investors**, confirm **Active only** is set for **Do you want to limit the analysis to only certain time investors**. If you applied a filter for the Sales effectiveness query, apply the same filter criteria for this query.
11. In **Their collaborators**, keep the following settings that are applied by default:

    * **Employees’ IsInternal** equals **True** for **Do you want to exclude any collaborators**
    * **AccountName** for **How do you want to group the people who collaborated with the time investors**
    * **Employees’ IsInternal** equals **False** for **Do you want to focus the analysis on a particular set of collaborators and group all others as “Unclassified”**
    * **Default match with CRM data** for **How would you like to join collaborators with accounts**

    ![Their collaborators selections for Power BI Sales dashboard](../Images/WpA/tutorials/pbi-sales-collaborators.png)

    >[!Note]
    >The **Default match with CRM data** setting identifies an external person as a collaborator only when their email address is an exact match in [Customer contacts](/viva/insights/setup/crm-data-upload?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json). Alternatively, if **Default + Extrapolation match with CRM data** is selected, an external person is identified as a collaborator if they share the same email domain as a customer contact.

12. In **Organizational data**, keep the preselected attributes and select the same optional attributes as you did for the **Sales effectiveness** query in **Step 6**.
13. When prompted, continue to **Results**. After both queries successfully run, in **Query designer** > **Results**, select the **Download** icon for the **Sales effectiveness** query results, select **PBI template**, and then select **OK** to download the template.
14. Open the downloaded **Sales effectiveness** template.
15. If prompted to select a program, select **Power BI**.
16. When prompted by Power BI:

    * In the **Query designer** > **Results**, select the **Link** icon for the Sales effectiveness query, and select to copy the generated OData URL link. If you ran the CRM collaboration query, then also copy the link for it.
    * In Power BI, paste the copied link or links into their respective fields.
    * Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Viva Insights data.
    * Select **Load** to import the query results into Power BI. Loading these large files might take a few minutes up to a few hours to complete.

    ![Power BI Sales OData links](../Images/WpA/tutorials/pbi-sales-odata.png)

17. If you're already signed in to Power BI with your Viva Insights organizational account, the dashboard visualizations will populate with your data. You are done and can skip the following steps. If not, proceed to the next step.
18. If you're not signed in to Power BI, or if an error occurs when updating the data, sign in to your organizational account again. In the **OData feed** dialog box, select **Organizational account**, and then select **Sign in**. See [Troubleshooting](/viva/insights/tutorials/power-bi-templates?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#troubleshooting) for more details.

    ![Power BI sign in.](../Images/WpA/Tutorials/pbi-sign-in.png)

19. Select and enter credentials for the organizational account that you use to sign in to the advanced insights app for Viva Insights, and then select **Save**.

    >[!Important]
    >You must sign in to Power BI with the same account you use to access Viva Insights.

20. Select **Connect** to prepare and load the data, which can take a few minutes to complete. After the data loads, you'll see visualization charts in Power BI about  Sales effectiveness within your organization.

## Report settings

After the Sales effectiveness dashboard is set up and populated with Viva Insights data in Power BI, you need to select the following **Settings**. Select **Settings** on the right side of the **Introduction** page. You can also adjust the report settings on any report page through the **Settings** icon.

* **Select the time period to measure** - This is the time period that you want to analyze.
* **Select the attribute you’d like to group external parties or CRM accounts by** - The primary “group-by” attribute shown in all subsequent reports. You can change this attribute at any time and all subsequent report pages will show group values by the new attribute. This attribute is used to determine how external parties or CRM accounts are grouped. Any external party or CRM account that’s contacted by an employee in the group is categorized into that group value.
* **Filter to certain employee groups in value selection** – You can filter by any of the values in the same attribute selected as the “group-by” attribute to filter the measured employee population. If you use filters, the measured employees count will reflect a reduced number. Measured employees reflect the number of employees in the filtered population who were active during the specified time period. Active employees are those who sent at least one email or instant message during a work week included in the current time period. If you also load the CRM collaboration query, you will find the measured CRM accounts count. The measured CRM accounts count may reflect a reduced number if you use filters. Measured CRM accounts shows the number of accounts contacted by the selected population.

After confirming the settings, check the number of measured employees and CRM accounts to confirm this is the population you want to analyze.

For **Cross-role engagement** and **Account collaboration snapshot**, you can select an internal employee grouping attribute to identify the teaming pattern and collaboration details for the employee groups. The report uses **LevelDesignation** by default. However, you can select the **Settings** (gear) icon to change it.

![Power BI Sales settings.](../Images/WpA/Tutorials/pbi-sales-settings.png)

## About the report

The Sales effectiveness dashboard includes the following reports that help you identify opportunities to help your external-facing groups be more successful.

* **External collaboration baseline** – Shows the weekly average internal and external collaboration hours and a breakdown of the external collaboration by meetings, emails, and Teams instant messages and unscheduled calls. This provides insights about how employees allocate time with external parties and how that compares across groups.
* **Meeting engagement** – Shows the weekly average external meeting counts and the distribution of employees by their meeting patterns, from no external meetings to more than 9 external meetings per week. This highlights employees’ direct interaction with external parties  and effective sales meetings, which are critical elements in generating sales and reaching revenue goals.
* **Account collaboration baseline** – Shows the weekly average CRM account collaboration hours by emails and meetings, weekly average CRM account meeting count, and the distribution of employees by their CRM account meeting patterns. This provides a baseline view of the employees’ CRM account collaboration.
* **Cross-role engagement** – Shows the distribution of CRM account collaboration hours by internal employee groups and the weekly average collaboration hours by these groups. This provides insights about how employees in different roles, functions or levels team up in CRM account interactions, and points out opportunities to clarify and redefine roles and responsibilities among employees in sales conversations.
* **Meaningful engagement** – Shows the distribution of CRM accounts by latest meaningful engagement and the distribution of employees by the number of accounts they had meaningful engagement with in an average 4-week period. A CRM account is meaningfully engaged means that there were at least two interactions (including one email and one meeting, two emails, or two meetings) between any employee and at least one contact from the account in the past 4 weeks. This highlights how accounts are being maintained and how the employees are managing the account portfolio on a regular basis. Further insights and opportunities can be identified to improve the account engagement and seller assignment strategy.
* **Account collaboration list** – Shows a list of CRM accounts together with the collaboration details, including total collaboration hours, email hours, meeting hours, number of employees who contacted the account, number of employees who meaningfully engaged with the account, and the latest date of engagement. This list provides insights about how time is invested in CRM accounts and whether the level of investment is aligned with the account strategy.
* **Account collaboration snapshot** – Shows the level of time investment and employee engagement with a particular account. Time investment view includes collaboration hours invested in the account in the past week and past 4 weeks, and the collaboration breakdown by emails and meetings over time. Employee engagement view includes number of employees connected with the account in the past week and past 4 weeks, and a breakdown of collaboration details by internal employee groups. This account deep-dive highlights the resource investment, teaming model, and overall collaboration cycle with the account, and provides opportunities to drive and improve effective sales activities.

The dashboard also includes the following:

* **Behavioral trends** - Track key metrics over time, including one for external collaboration baseline that doesn’t require CRM data, and the other one for CRM account collaboration.
* **Take action** - Has actionable recommendations to improve behaviors.
* **Glossary** - Describes all the metrics used in the reports.

## Learning resources

Learn how to identify and improve sales effectiveness by using Viva Insights with the following resources:

* [Introduction to customer focus with Microsoft Viva Insights](/learn/modules/workplace-analytics-customer-focus/)
* [Viva Insights Customer Focus Playbook](https://download.microsoft.com/download/7/e/b/7eb4dff1-a139-4174-a54d-6616929f16f7/Customer-focus-playbook.pdf)

## Power BI tips, troubleshooting, and FAQs

For details about how to share the dashboard and other Power BI tips, troubleshoot any issues, or review the FAQ, see [Power BI tips, FAQ, and troubleshooting](/viva/insights/tutorials/power-bi-templates?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

## Related topic

[View, download, and export query results](/viva/insights/use/view-download-and-export-query-results?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)
