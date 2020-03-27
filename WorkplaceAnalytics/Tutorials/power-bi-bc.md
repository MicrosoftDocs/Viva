---

ROBOTS: NOINDEX,NOFOLLOW
title: Power BI Business Continuity Dashboard
description: Use the Power BI Business Continuity Dashboard to visualize predefined query data from Workplace Analytics in Power BI
author: madehmer
ms.author: 
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Power BI Business Continuity Dashboard

You can use the Power BI Business Continuity Dashboard populated by Workplace Analytics data to answer questions about how your organization is adapting to business disruption, such as a switch to 100 percent remote work.

Workplace Analytics collaboration data directionally highlights where disruption to ways of working is having the largest impact, which is a measurable starting point for identifying how leaders, tools, and processes can support and sustain a new way of working.

The following are a few of the top-level business questions asked by leaders about continuing business during a disruption that this dashboard enables you to visualize and explore.

|Business question |Analysis |
|-------------|------------------|
|How is business as usual changing? |<ul><li>How are activity levels changing in response to a disruption? </li><li>Which lines of business are more impacted? </li></ul>|
|How are employees adapting to the disruption?  |<ul><li>How many employees are experiencing significant shifts in workweek span and collaboration demand? </li><li>How are employees shifting their work patterns across the collaboration activities, such as calls and chats? </li></ul>|
|Are we maintaining external relationships? |<ul><li>How much has changed with customer, partner, and vendor collaboration? </li><li>Which lines of business are experiencing the largest increases and decreases in external demand? </li></ul>|
|How do you foster employee community and engagement? |<ul><li>Are your managers regularly checking in with their employees about their wellbeing and health? </li><li>Are employees managing to stay engaged while in an all-remote work environment? </li></ul>|

To populate the Business Continuity Dashboard in Power BI, you must set up and successfully run the following predefined **Business Continuity** and **Hourly Collaboration** queries in Workplace Analytics. The results of these queries will refresh your downloaded Power BI dashboard on a weekly basis.  

After you successfully run these required queries, you'll see the Power BI template as an available download option for the Business Continuity query. This template is required to create the dashboard in Power BI. After you download the Power BI template, you can then connect the query data from Workplace Analytics to the dashboard in Power BI.

After the Business Continuity Dashboard is populated with data, you can use it to visualize, explore, and report about your organization's workplace patterns and trends.

## Prerequisites  

Before you can add and populate the dashboard in Power BI, you must:

* Be assigned the role of [Analyst](../use/user-roles.md) in Workplace Analytics.
* Have Power BI Desktop installed. See [Install and run Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-getting-started#install-and-run-power-bi-desktop) for details.

## Setting up

1. In [Workplace Analytics](https://workplaceanalytics.office.com/), select **Analyze** > **Queries**.
2. Under the **Start from preselected filters and metrics** select **Business Continuity** to open this predefined query, which has all the required metrics to populate the Power BI template.
3. Select or confirm the options for **Group by**, **Time period**, and **Meeting exclusions** and then, select to **auto-refresh** the query.

   > [!Important]
   > The dashboard is designed to show you how a disruption can change your organization's work patterns. For best results, select the Last 6 months for the **Time period**, which should include time before and after the disruption.

4. In **Select metrics**, confirm the preselected, required metrics and select any other metrics to include in the dashboard.

   > [!Important]
   > If you try to delete a required metric, you'll see a warning that the deletion might disable portions of the Power BI dashboard and reduce query results. In turn, this can limit your ability to visualize collaboration patterns. Depending on the metric you delete, you might disable a single Power BI chart, several charts, or all of the possible charts. You can select **Cancel** to retain the metric.

5. In **Select filters**, you can optionally select to filter the data. For more details about filter and metric options, see [Create a Person Query](./person-queries.md).
6. In **Organizational data**, keep the preselected **Organization**, **LevelDesignation**, and **TimeZone** attributes that the dashboard requires. You can then select any other attributes (columns) to include in the dashboard.

   > [!Important]
   > If you remove the required preselected attributes, you might disable one or more Power BI chart.

7. Select **Run** to run the query, which might take several minutes to complete.
8. Repeat the previous steps to create the **Hourly Collaboration** query, which require the same **Organizational data** attributes as the **Business Continuity** query.
9. In **Queries** > **Results**, after the queries successfully run, select the **download** icon for the **Business Continuity** query results, and then select **PBI template**, which downloads the template and copies the OData link to the clipboard.
10. Select **OK**, and then open the downloaded **Business Continuity Power BI template**.
11. If prompted, select to open Power BI.
12. When prompted, paste the OData links for both queries, and then select **Load**. On the **Results** page, select the **link** icon for each query to get the link.
13. If prompted to **Sign in** to Power BI, enter your **Workplace Analytics login credentials** to connect to the query results.
14. If you're already logged in to Power BI with your Workplace Analytics organizational account, your data loads and Power BI uses visualization charts to show your data. You are done and can skip the following steps. If not, proceed to the next step.
15. If not logged in to Power BI, the left pane of **OData feed** (highlights the current sign-in account for Power BI), select **Organizational account**.

    >[!Important]
    >You can view Workplace Analytics data (including query results) in Power BI only if you've been assigned the Analyst role in Workplace Analytics. Also, you must sign in with the correct account by using the following steps.

16. If prompted, select **Sign in**.
17. In the **Office 365** dialog box, select the organizational account that you use to log in to Workplace Analytics. The OData feed dialog box will then show that "you are currently signed in" to Power BI.
18. Select **Connect** to show the status of the data preparation, which might take several minutes.

## Using the dashboard

After the Business Continuity Dashboard is set up and populated with Workplace Analytics data, refer to the following to learn how to use the Power BI visualization charts to analyze your organization's collaboration patterns.

> [!Important]
> Workplace Analytics utilizes pseudonymized and aggregated behavioral data to provide a focused lens into how groups are getting work done. As with any behavioral dataset, you must view this data directionally about how groups act and respond to stimuli. Additionally, a number of underlying factors are used to calculate group-level, summary metrics.
>
> **For example**: Insights about changes in after-hours activity blends data about how people are experiencing large increases in overall activity levels with other individuals who are forced to work split schedules to integrate work and their out-of-work responsibilities. As such, the insights within this dashboard should be used as a lens perspective on how work is getting done, and not used in isolation of more traditional management approaches.

### Settings and scope

As a first step to viewing data in the dashboard, set the following parameters in the **Settings & Scope** page.

* **Baseline time frame** - The baseline for your analysis and all changes will be compared with this time frame.

    >[!Note]
    >The **Baseline time frame** must precede and not overlap with the **Selected time frame**. If the two time frames overlap, you'll get a "Warning: Baseline and Current Timelines overlap" message.

* **Selected time frame** - This is the time frame you want to compare to the baseline time frame.
* **Scope** - Select the **Organizations** and **Time zones** you want to analyze in the report. These filters are applied across all the pages in the Power BI report.

After changing one or more of these settings, confirm the number of scoped employees are what you want to analyze.

> [!Important]
> As additional data is processed on a weekly basis, you'll need to adjust the **Selected Time Frame** if you want to view the most recent data.

### Power BI tips

A few tips to help you use the Business Continuity Dashboard in Power BI:  

* **Cross-filter and cross-highlight** - All visuals on a report page are interconnected. If you select a data point on one of the visuals, all the others on the page that contain that data will change, based on that selection.
* **Drill a visual that has a hierarchy** - When a visual has a hierarchy, you can drill down to reveal additional details. Any chart in the dashboard labeled with "By Organization and Level Designation" supports the Power BI drill down capability.

For more details about using Power BI, see [Interact with visuals in reports, dashboards, and apps](https://docs.microsoft.com/power-bi/consumer/end-user-visualizations).

## Sharing the dashboard

Like other products that work with sensitive data, such as HR systems, Workplace Analytics is not meant for the general workforce. Rather, its users are expected to have training regarding how to handle sensitive information. Training should be specific to your organization. Suggested topics may include your organization's HR policies, employee privacy policy, how to handle and store sensitive data, and insider trading. See [Data-protection considerations](../privacy/data-protection-considerations.md) when using data generated by Workplace Analytics.

You can share the Business Continuity Dashboard in a few different ways in Power BI. To learn more, see [Ways to share your work in Power BI](https://docs.microsoft.com/power-bi/service-how-to-collaborate-distribute-dashboards-reports).

**Best ways to share**

* **Share insights in an app** - This option allows users to navigate the dashboard without access to the underlying data. See [Publish an app in Power BI](https://docs.microsoft.com/power-bi/service-create-distribute-apps) for details.
* **Share as a PDF or other static file** - This option is not interactive. See [Printing from the Power BI service](https://docs.microsoft.com/power-bi/consumer/end-user-print).

## Frequently asked questions

#### Q1 Who can create the dashboard in Power BI?

You must be assigned the role of [Analyst](../use/user-roles.md) in Workplace Analytics to create the dashboard. You must also have a Power BI license and have the desktop version installed. See [Install and run Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-getting-started#install-and-run-power-bi-desktop) for details.

#### Q2 How frequently is data refreshed in the dashboard?

The dashboard gets repopulated once a week after Workplace Analytics finishes its weekend processing. **Note**: Change the **Selected time frame** seting in the dashboard's **Settings & Scope** report to view the most recently processed data.

#### Q3 How do I share the dashboard with others in my organization?

You can share the dashboard with others in your organization *without sharing the underlying data* by publishing the insights in an app or as PDF or static file. See [Sharing the dashboard](#sharing-the-dashboard) for details.

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

## Support

* **Dashboard support** - Contact the Workplace Analytics team member that referred you to this page for support about onboarding, usage, and interpretation of the data contained within the dashboard.
* **Workplace Analytics support** - Refer to [Workplace Analytics documentation](../index.md) or [Workplace Analytics Support](../overview/getting-support.md) for additional help.
* **Support with other Microsoft products and tools** - Support for Power BI and other tools used in the context of this dashboard can be found through each product's associated support channels.

## Related topics

* [Power BI templates in Workplace Analytics](../tutorials/power-bi-templates.md)
* [View, download, and export query results](../use/view-download-and-export-query-results.md)
