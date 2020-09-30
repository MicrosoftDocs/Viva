---

title: Business continuity dashboard
description: Use the Business continuity dashboard to visualize predefined query data from Workplace Analytics in Power BI
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Business continuity

The Business continuity dashboard uses a Power BI template that’s populated populated by Workplace Analytics data to gain insights into how your organization and your employees are being impacted by the shift to remote work.

This dashboard directionally highlights where the shift to remote work might have the largest impacts, offering a measurable starting point for helping leaders understand where they might use tools and processes to support and sustain new ways of working.

The dashboard enables you to visualize and explore the following top-level business questions asked by leaders:

* How are collaboration activities changing?
* What are the impacts of work-life integration?
* Are external relationships being maintained?
* Are employees engaged and connected?
* How are work patterns evolving?
* How can remote work effectiveness be improved?

To populate the dashboard in Power BI, you must set up and successfully run the predefined **Business continuity** and **Hourly collaboration** queries in Workplace Analytics. The results of these queries will refresh your downloaded Power BI dashboard on a weekly basis.  

After you successfully run these required queries, you'll see the Power BI template as an available download option for the Business continuity query. This template is required to create the dashboard in Power BI. After you download the Power BI template, you can then connect the query data from Workplace Analytics to the dashboard in Power BI.

When the Business continuity dashboard is populated with data, you can use it to visualize, explore, and report about your organization's workplace patterns and trends.

For an interactive demonstration of this dashboard, see [Business continuity demo](../power-bi-demos/business-continuity.md).

## Demonstration

<br><iframe width="800" height="486" src="https://msit.powerbi.com/view?r=eyJrIjoiM2ZiY2Y4M2YtMTMyNi00NWY1LWEyMjctYTY2OTdlOWQzNDhhIiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9&embedImagePlaceholder=true&pageName=ReportSectionbbd7dee40bcdeee460e6" frameborder="0" allowFullScreen="true"></iframe>

## Prerequisites  

Before you can run the queries and populate the dashboard in Power BI, you must:

* Be assigned the role of [Analyst](../use/user-roles.md) in Workplace Analytics.
* Have the latest version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t?activetab=pivot:overviewtab) to download and install the latest version.

## Template update

The Business continuity dashboard is being updated on a frequent cadence to address evolving remote work business questions. To ensure you are using the latest version of the dashboard, download the Power BI template from your most recently run Workplace Analytics Business continuity query, then repeat **Steps 8-15** in [Set up the dashboard](#set-up-the-dashboard). You don't have to run the queries again for template updates.

If you started using the Business continuity dashboard in April or May 2020 and you selected to use six months of data for your queries, you need to repeat **Steps 1-7** in [Set up the dashboard](#set-up-the-dashboard) to run new queries that include data for the last one year, which will encompass activity before and during the shift to remote work in March. To continue to use your custom version of the Business Continuity dashboard and not update to the latest version of the template, do the following instead of **Steps 8-15** in [Set up the dashboard](#set-up-the-dashboard): 

1. After both queries successfully run, open your existing Business continuity dashboard in Power BI Desktop.
2. In **Transform data**, select **Edit parameters**.
3. Replace the existing URLs for Business continuity and Hourly collaboration query URLs with the new query URLs, and then select **OK**.
4. A best practice that reduces future query processing time is to turn off the auto-refresh or delete the preexisting queries that the dashboard is no longer using. See [Stop the auto-refresh option](../Tutorials/Query-auto-refresh.md#stop-the-auto-refresh-option) for details.

## Dashboard setup video

> [!Important]
> Where the video shows selecting **Last 6 months** when running the queries, be sure you select **Last 1 year** instead. The queries will then have data that includes activity before and during the shift to remote work in March 2020.

<iframe width="640" height="564" src="https://player.vimeo.com/video/402717048" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>

## Set up the dashboard

1. In [Workplace Analytics](https://workplaceanalytics.office.com/), select **Analyze** > **Queries**.
2. Under **Start from preselected filters and metrics**, select **Business continuity** (or **Hourly collaboration** per **Step 7**) to open the predefined query, which contains the required metrics to populate the dashboard.

   ![Predefined queries](../Images/WpA/Tutorials/predefined-bc-queries.png)

3. Select or confirm the following query settings:

   * **Name** - Customize or keep the default name
   * **Group by** - Week
   * **Time period** - Last 1 year
   * **Auto-refresh** - Enable the setting
   * **Meeting exclusions** - Select the preferred rule for your tenant

   > [!Important]
   > * The dashboard is designed to show you how a shift to remote work can change your organization's work patterns. For best results, select **Last 1 year** for the **Time period** to include time before and after a shift.
   > * If you try to delete a predefined metric, you'll see a warning that the deletion might disable portions of the Power BI dashboard and reduce query results. In turn, this can limit your ability to visualize collaboration patterns. Depending on the metric you delete, you might disable a single Power BI chart, several charts, or all the charts. Select **Cancel** to retain the metric.

   ![Business continuity queries](../Images/WpA/Tutorials/bcd-query.png)

4. In **Select filters**, select **Active only** for "**Which measured employees do you want to include?**" Optionally, you can further filter the employees in scope for the dashboard. For more details about filter and metric options, see [Create a Person Query](./person-queries.md).
5. In **Organizational data**, keep the preselected **Organization**, **LevelDesignation**, and **TimeZone** attributes that the dashboard requires. You can then select any other attributes (columns) to include in the dashboard.

   > [!Important]
   > If you remove the required, preselected Organizational data attributes, you might disable one or more Power BI charts.

6. Select **Run** to run the query, which might take several minutes to complete.
7. Repeat **Steps 2-6** for the **Hourly collaboration** query, which requires the same selections as for Business continuity.
8. In **Queries** > **Results**, after both queries successfully run, select the **Download** icon for the **Business continuity** query results, select **PBI template**, and then select **OK** to download the template.

   ![Power BI template download](../Images/WpA/Tutorials/pbi-template-download.png)

9. Open the downloaded **Business continuity Power BI template**.
10. If prompted to select a program, select **Power BI**.
11. When prompted by Power BI, copy and paste the OData links for both queries into their respective fields.

    * In the Workplace Analytics **Queries** > **Results** page, select the **Link** icon for each query, and select to copy the generated OData URL link.
    * In Power BI, paste each copied link into its respective field.
    * Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Workplace Analytics data.
    * Select **Load** to import the query results into Power BI. Loading these large files may take some time to complete.

    ![Query URLs for Power BI](../Images/WpA/Tutorials/odata-link-2.png)

12. If you're already signed in to Power BI with your Workplace Analytics organizational account, the dashboard visualizations will populate with your data. You are done and can skip the following steps. If not, proceed to the next step.
13. If you're not signed in to Power BI, or if an error occurs when updating the data, sign in to your organizational account again. In the **OData feed** dialog box, select **Organizational account**, and then select **Sign in**. See [Troubleshooting](../tutorials/power-bi-templates.md#troubleshooting) for more details.

    ![Power BI sign in](../Images/WpA/Tutorials/pbi-sign-in.png)

14. Select and enter credentials for the organizational account that you use to sign in to Workplace Analytics, and then select **Save**.

    >[!Important]
    >You must sign in to Power BI with the same account you use to access Workplace Analytics.

15. Select **Connect** to prepare and load the data, which can take a few minutes to complete.
16. If you have preexisting query results that the dashboard is no longer using, a best practice that reduces processing time is to turn off the auto-refresh or delete the queries that the dashboard is no longer using. See [Stop the auto-refresh option](../Tutorials/Query-auto-refresh.md#stop-the-auto-refresh-option) for details.

## Dashboard settings

After the Business continuity dashboard is set up and populated with Workplace Analytics data, as a first step to viewing data in the dashboard, view and set the following parameters on the **Settings** page.

* **Earlier time frame** - This is the baseline for your analysis and all changes will be compared with this time frame.

    >[!Note]
    >The **Earlier time frame** must precede and not overlap with the **Current time frame**. If the two timeframes overlap, you'll get a warning about the timelines overlapping.

* **Current time frame** - This is the timeframe you want to compare with the earlier timeframe.
* **Organizational attribute to view the report by** - The primary “group-by” attribute shown in all subsequent reports. You can change this attribute at any time and all subsequent report pages will show group values by the new attribute.
* **Organizational attribute to filter by** – To filter the measured employee population, you can filter by any selected Organizational attribute, and then filter by any of the values for these attributes. If you filter, the measured employees count will reflect a reduced number. To clear an existing filter, select **Ctrl** while clicking the **Clear filter arrow** (or with a touchscreen, select the **Clear filter arrow**). Measured employees reflect the number of employees in the filtered population who were active in the specified time period. Active employees are those who sent at least one email or instant message in the work week included in the current timeframe.

  ![Business continuity dashboard settings](../Images/WpA/Tutorials/bcd-settings.png)

After confirming the settings, check the number of measured employees to confirm this is the population you want to analyze.

> [!Important]
> As new data is processed on a weekly basis, select **Refresh** in the Power BI Home ribbon to view the most recent data.

## About the reports

The dashboard reports directionally highlight where a shift to remote work is having the largest impact. They also give you a measurable starting point for identifying where leaders can use tools and processes to support employees in a new way of working. All metrics are defined in the **Glossary**. A “why it matters” interpretation is also included in a text box for each report.

The following describes each report with specific nuances to consider for each.

* **How are collaboration activities changing?** – Shows how employee collaboration patterns are changing in response to a shift in work patterns, and which collaboration tools people are substituting for in-person interactions.  
* **What are the impacts of work-life integration? [1]** - Helps you assess if some employees are disproportionately affected. You can select from multiple values to view the percentage of employees whose collaboration hours increased or decreased by more than the specified number of hours.
* **What are the impacts of work-life integration? [2]** - Shows changes in after-hours collaboration activity. You can select from multiple values to view the percentage of employees whose after-hours work increased or decreased by more than the specified number of hours.  You can also examine the activity by time of day for meetings, emails and instant messages.
* **Are external relationships being maintained?** - Quantifies changes in communication with customers, partners, and other people outside the organization.  
* **Are employees engaged and connected?** - Unlike the other reports that show changes between the baseline and the current timeframes, *this report only shows metrics for the last two weeks of the current time frame*. This view enables you to assess if manager 1:1 meetings and organizational collaboration, which are keys to fostering employee engagement and community, are still occurring virtually.

  > [!Note]
  > The report’s metrics are based solely on the last two weeks of the **Current time frame** and not on a comparison with the **Earlier time frame**. Also, these charts are based on small group meetings of less than eight people and only analyze meeting, call, and instant-message activity, excluding email activity. For more details on metrics, see the Glossary in the dashboard.

## Power BI tips, troubleshooting, and FAQs

For details about how to share the dashboard and other Power BI tips, troubleshoot any issues, or review the most frequently asked questions, see [Power BI templates in Workplace Analytics](../tutorials/power-bi-templates.md).

## Related topics

[View, download, and export query results](../use/view-download-and-export-query-results.md)
