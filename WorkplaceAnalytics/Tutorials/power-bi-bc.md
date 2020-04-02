---

ROBOTS: NOINDEX,NOFOLLOW
title: Power BI Business Continuity Dashboard
description: Use the Business Continuity Dashboard to visualize predefined query data from Workplace Analytics in Power BI
author: madehmer
ms.author: 
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Power BI Business Continuity Dashboard

You can use the Power BI Business Continuity Dashboard populated by Workplace Analytics data to gain insights into how your organization is adapting to business disruptions, such as a switch to 100 percent remote work.

This dashboard directionally highlights where disruption to ways of working might be having the largest impacts, offering a measurable starting point for helping leaders understand where they might use tools and processes to support and sustain new ways of working.

The following are a few of the top-level business questions asked by leaders that this dashboard enables you to visualize and explore.

|Business question |Analysis |
|-------------|------------------|
|How is business as usual changing? |<ul><li>How are employee collaboration patterns changing in response to this disruption?  </li><li>Which collaboration tools are people substituting for in-person interaction? |
|How are employees adapting to the disruption? |<ul><li>What share of employees are experiencing significant shifts in their weekly work spans and collaboration levels? </li><li>How are working patterns flexing across our collaboration mediums? </li></ul>|
|Are we maintaining external relationships? |<ul><li>Are you still connecting with customers, partners, and vendors? </li><li>Which teams and functions are experiencing the the biggest changes in external collaboration? </li></ul>|
|How do we foster employee community and engagement? |<ul><li>Are managers still connecting one-on-one with their team members? </li><li>Are employees staying connected to their peers in this 100 percent remote working environment? </li></ul>|

To populate the Business Continuity Dashboard in Power BI, you must set up and successfully run the predefined **Business Continuity** and **Hourly Collaboration** queries in Workplace Analytics. The results of these queries will refresh your downloaded Power BI dashboard on a weekly basis.  

After you successfully run these required queries, you'll see the Power BI template as an available download option for the Business Continuity query. This template is required to create the dashboard in Power BI. After you download the Power BI template, you can then connect the query data from Workplace Analytics to the dashboard in Power BI.

When the Business Continuity Dashboard is populated with data, you can use it to visualize, explore, and report about your organization's workplace patterns and trends.

## Prerequisites  

Before you can run the queries and populate the dashboard in Power BI, you must:

* Be assigned the role of [Analyst](../use/user-roles.md) in Workplace Analytics.
* Have the latest version of Power BI Desktop installed. Go to [Get Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t?activetab=pivot:overviewtab) to download and install it.

## Video: Dashboard setup

<iframe width="640" height="564" src="https://player.vimeo.com/video/402717048" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>

## Set up the dashboard

1. In [Workplace Analytics](https://workplaceanalytics.office.com/), select **Analyze** > **Queries**.
2. Under **Start from preselected filters and metrics**, select **Business Continuity** (or **Hourly Collaboration** per **Step 7**) to open the predefined query, which contains the required metrics to populate the dashboard.

   ![Predefined queries](../Images/WpA/Tutorials/predefined-bc-queries.png)

3. Select or confirm the following query settings:

   * **Name** - Customize or keep the default name
   * **Group by** - Week
   * **Time period** - Last 6 months
   * **Auto-refresh** - Enable the setting
   * **Meeting exclusions** - Select the preferred rule for your tenant

   > [!Important]
   > * The dashboard is designed to show you how a disruption can change your organization's work patterns. For best results, select **Last 6 months** for the **Time period** to include time before and after the disruption.
   > * If you try to delete a predefined metric, you'll see a warning that the deletion might disable portions of the Power BI dashboard and reduce query results. In turn, this can limit your ability to visualize collaboration patterns. Depending on the metric you delete, you might disable a single Power BI chart, several charts, or all the charts. Select **Cancel** to retain the metric.

   ![Business Continuity queries](../Images/WpA/Tutorials/bc-query.png)

4. In **Select filters**, select **Active only** for "**Which measured employees do you want to include?**" Optionally, you can further filter the employees in scope for the dashboard. For more details about filter and metric options, see [Create a Person Query](./person-queries.md).
5. In **Organizational data**, keep the preselected **Organization**, **LevelDesignation**, and **TimeZone** attributes that the dashboard requires. You can then select any other attributes (columns) to include in the dashboard.

   > [!Important]
   > If you remove the required, preselected Organizational data attributes, you might disable one or more Power BI charts.

6. Select **Run** to run the query, which might take several minutes to complete.
7. Repeat **Steps 2-6** for the **Hourly Collaboration** query, which requires the same selections as for Business Continuity.
8. In **Queries** > **Results**, after both queries successfully run, select the **Download** icon for the **Business Continuity** query results, select **PBI template**, and then select **OK** to download the template.

   ![Power BI template download](../Images/WpA/Tutorials/pbi-template-download.png)

9. Open the downloaded **Business Continuity Power BI template**.
10. If prompted to select a program, select **Power BI**.
11. When prompted by Power BI, copy and paste the OData links for both queries into their respective fields.

    * In the Workplace Analytics **Queries** > **Results** page, select the **Link** icon for each query, and select to copy the generated OData URL link.
    * In Power BI, paste each copied link into its respective field.
    * Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Workplace Analytics data.
    * Select **Load** to import the query results into Power BI. Loading these large files may take some time to complete.

    ![Query URLs for Power BI](../Images/WpA/Tutorials/odata-link-2.png)

12. If you're already signed in to Power BI with your Workplace Analytics organizational account, the dashboard visualizations will populate with your data. You are done and can skip the following steps. If not, proceed to the next step.
13. If you're not signed in to Power BI, or if an error occurs when updating the data, sign in to your organizational account again. In the **OData feed** dialog box, select **Organizational account**, and then select **Sign in**.

    ![Power BI sign in](../Images/WpA/Tutorials/pbi-sign-in.png)

14. Select and enter credentials for the organizational account that you use to sign in to Workplace Analytics, and then select **Save**.

    >[!Important]
    >You must sign in to Power BI with the same account you use to access Workplace Analytics.

15. Select **Connect** to prepare and load the data, which can take a few minutes to complete.

## Use the dashboard

After the Business Continuity Dashboard is set up and populated with Workplace Analytics data, the following guidelines help you set up and use the Power BI visualization charts to analyze your organization's collaboration patterns.

### Settings and scope

As a first step to viewing data in the dashboard, view and set the following parameters in the **Settings and scope** tab.

* **Baseline time frame** - This is the baseline for your analysis and all changes will be compared with this time frame.

    >[!Note]
    >The **Baseline time frame** must precede and not overlap with the **Selected time frame**. If the two time frames overlap, you'll get a "Warning: Baseline and Current timelines overlap" message.

* **Selected time frame** - This is the time frame you want to compare to the baseline time frame.
* **Scope** - Select the **Organizations** and **Time zones** you want to analyze in the report. These filters are applied across all the pages in the Power BI report.
* **Minimum group size** - This displays the minimum group size that has been configured for this report.

    >[!Important]
    >Make sure this adheres to your organization's policies around minimum aggregation requirements for displaying Workplace Analytics data.

  ![Dashboard Settings and scope](../Images/WpA/Tutorials/pbi-settings-scope.png)

After changing one or more of the settings in **Settings and scope**, confirm the number of scoped employees are what you want to analyze.

> [!Important]
> As additional data is processed on a weekly basis, you'll need to adjust the **Selected Time Frame** if you want to view the most recent data.

## About the reports

The following dashboard reports directionally highlight where disruptions to ways of working are having the largest impact, and provide a measurable starting point for identifying where leaders can use tools and processes to support employees in a new way of working. All metrics are defined in the Glossary report at the end of the dashboard. An interpretation is provided in the text box of each report. The following describes each report with specific nuances to consider for each.

* **Business Continuity at a Glance** - Frames the data and gives an overview of the metrics. Hover your cursor over each metric to see its definition. Select the **i** icon next to each business question to view the related report.
* **How is 'Business as Usual' changing?** - Shows the trend in collaboration hours by channel. You can further drill into the displayed Organization by the attribute Level Designation.
* **How are employees adapting to the disruption? [1]** - Enables you to assess whether some employees are disproportionately affected. You can adjust the **Threshold** slider control to view the percentage of employees whose collaboration hours increased or decreased by more than the specified number of hours.
* **How are employees adapting to the disruption? [2]** -  Demonstrates the slippage between work and life balance. You can adjust the **Threshold** slider control to view the percentage of employees whose after-hours increased or decreased by more than the specified number of hours.
* **Are we maintaining external relationships?** - Quantifies changes in communication with customers, partners and other people outside the organization.  You can further drill into the displayed Organization by the attribute Level Designation.
* **How can we foster employee engagement and community?** - Unlike the other reports that show changes between the baseline and the current time frames, ***this report only shows metrics for the current time frame.*** This view enables you to assess if manager 1:1 meetings and organizational collaboration, which are keys to fostering employee engagement and community, are still occurring virtually.

  > [!Note]
  > The metrics for the "How do we foster employee engagement and community?" report are only based on the **Selected time frame** and not on a comparison with the Baseline time frame.

### Power BI tips

A few tips to help you use the Business Continuity Dashboard in Power BI:  

* **Cross-filter and cross-highlight** - All visuals on a report page are interconnected. If you select a data point on one of the visuals, all the others on the page that contain that data will change, based on that selection.
* **Drill down into a visual that has a hierarchy** - When a visual has a hierarchy, you can drill down to reveal additional details. Any chart in the dashboard labeled with "By Organization and Level Designation" supports the Power BI drill down capability.

For more details about using Power BI, see [Interact with visuals in reports, dashboards, and apps](https://docs.microsoft.com/power-bi/consumer/end-user-visualizations).

## Share the dashboard

Like other products that work with sensitive data, such as HR systems, Workplace Analytics is not meant for the general workforce. Rather, its users are expected to have training regarding how to handle sensitive information. Training should be specific to your organization. See [Data-protection considerations](../privacy/data-protection-considerations.md) when using data generated by Workplace Analytics.

Anyone you share the Power BI *desktop file* with can access the underlying dataset at the same level of granularity as a Workplace Analytics Analyst.   For this reason, consider the following alternatives that do not provide access to the underlying data:

* **Share as a PDF or other static file** - This option generates a report that's not interactive. See [Export reports from Power BI to PDF](https://docs.microsoft.com/power-bi/consumer/end-user-pdf).
* **Publish the report to Power BI Service and share insights in an app** - This option allows other users to navigate the dashboard without access to the underlying data. See [Distribute insights in an app](https://docs.microsoft.com/power-bi/service-how-to-collaborate-distribute-dashboards-reports#distribute-insights-in-an-app) for details.

## Frequently asked questions

#### Q1 Who can create the dashboard in Power BI?

You must be assigned the role of [Analyst](../use/user-roles.md) in Workplace Analytics to create the dashboard. You must also have a Power BI license and have the desktop version installed. See [Install and run Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-getting-started#install-and-run-power-bi-desktop) for details.

#### Q2 How frequently is data refreshed in the dashboard?

The dashboard gets repopulated once a week after Workplace Analytics finishes its weekend processing. **Note**: You must manually adjust the **Selected time frame** setting in the dashboard's **Settings and scope** report to view the most recently processed data.

#### Q3 How do I share the dashboard with others in my organization?

You can share the dashboard with others in your organization *without sharing the underlying data* by publishing the insights in an app or as PDF or static file. See [Share the dashboard](#share-the-dashboard) for details.

#### Q4 Can I share the underlying dashboard dataset with others in my organization?

To maintain data privacy, only employees assigned the role of [Analyst](../use/user-roles.md) in Workplace Analytics should have access to the underlying dataset in the Power BI dashboard.

#### Q5 How do I set up and run a Workplace Analytics query?

See [Create a Person Query](./person-queries.md) for details.

#### Q6 How do I change the axis of a chart to use a different Organizational data attribute?

Only the required Organizational attributes are used when setting up the Power BI file. If you selected more organizational attributes when setting up your queries, you can use those additional attributes in your visuals. To use a different organizational attribute, search within the Fields pane for the Organizational attribute you want to use. Then, click on the visual you want to modify to select it. Finally, drag the Organizational attribute from the Fields pane to the Axis section in the Visualizations pane.

#### Q7 How do I integrate additional metrics or data sources with this dashboard?

See [Connect to data in Power BI](https://docs.microsoft.com/power-bi/connect-data/) to learn more about how to connect data in Power BI. See [Prepare organizational data](../setup/prepare-organizational-data.md) to learn about what organizational data you can analyze in Workplace Analytics and see [Data sources](../use/data-sourcesv2.md) to see what data sources you can connect to and analyze from within Workplace Analytics.

#### Q8 How do I use Power BI?

See [Power BI documentation](https://docs.microsoft.com/power-bi/) for details on how to use Power BI.

#### Q9 What languages is the dashboard available in?

The dashboard is currently only available in English.

## Troubleshooting

#### OData error: The given URL neither points to an OData service or a feed

If you are signed in with the wrong organizational account, you'll get an error message when loading the data with the Power BI template. To fix it, follow these steps:

1. Close the error message, and then open the **Transform data** menu, and select **Data source settings**.
2. In **Data source settings**, select **Global permissions**, select "**https://workplace.analytics.office.com**", and then select **Edit permissions**.
3. For **Credentials**, select **Edit**.
4. In the **OData feed** dialog box, select **Organizational account**, and then select **Sign in** or **Sign in as a different user**.
5. Select the account that you use to sign in to Workplace Analytics, enter the password, and then when prompted in **OData feed**, select **Save**.
6. In **Edit Permissions**, select **OK**, and then close the **Data source settings** window.
7. Close Power BI and follow the instructions in [Set up the dashboard](#set-up-the-dashboard).

#### The Power BI visuals fail to load or show errors in the tables

Power BI cannot complete a data join if data values are missing in the Organization or LevelDesignation tables. To validate this error:

1. In the **Fields** pane in Power BI, look for an **error** (!) icon in either the **Organization** or **LevelDesignation** tables. If you see an error, such as the following about blank values, select the field with the error to view it.

   ![Power BI error](../Images/WpA/Tutorials/pbi-dashboard-error.png)

2. To remediate this error, select **Transform Data** from the **Transform Data** menu to open the Power Query Editor.
3. Select the **Business Continuity** query.
4. In the data preview table, locate the column for Organization and/or LevelDesignation, expand the column header, and select **Remove Empty**, and then select **OK**.
5. Select the **Hourly Collaboration** query and repeat Steps 3-4 to filter out empty values.
6. Select **Close & Apply** to apply the changes and return to the dashboard.

## Support

* **Dashboard support** - Contact the Workplace Analytics team member that referred you to this page for support about onboarding, usage, and interpretation of the data contained within the dashboard.
* **Workplace Analytics support** - Refer to [Workplace Analytics documentation](../index.md) or [Workplace Analytics Support](../overview/getting-support.md) for additional help.
* **Support with other Microsoft products and tools** - Support for Power BI and other tools used in the context of this dashboard can be found through each product's associated support channels.

## Related topics

* [Power BI templates in Workplace Analytics](../tutorials/power-bi-templates.md)
* [View, download, and export query results](../use/view-download-and-export-query-results.md)
