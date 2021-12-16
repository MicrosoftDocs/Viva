---
ROBOTS: NOINDEX,NOFOLLOW
title: Power BI My organization dashboard
description: Use the Power BI My organization dashboard to visualize predefined data from Viva Insights in Power BI
author: madehmer
ms.author: helayne
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

# My organization dashboard in Power BI

*This experience is only available through private preview.*

As employees shift to remote work and to digital only collaboration, Microsoft Viva Insights can help you stay on track and make data-driven decisions that can help your employees do their best work.

The Power BI My organization dashboard directionally highlights where a shift to remote work might have the largest impacts, offering a measurable starting point for helping leaders understand where they might use tools and processes to support and sustain new ways of working.

You can use this dashboard to visualize and explore your company’s collaboration activity in Microsoft Teams and Outlook and get ideas about how to help your organization be successful moving forward. 

The dashboard includes the following reports:

* **Protecting personal time** - Shows the percentage of employees who are successfully protecting their personal time by limiting their after-hours work to less than five hours each week. As digital collaboration becomes our new norm, it’s important to establish communication guidelines and boundaries to encourage employees to balance work and life and maintain good wellbeing.
* **Connecting in small groups** – Shows how much time employees spend interacting at least one hour each week with eight or fewer people to encourage small-group collaboration where most have a voice in the activity.
* **Finding time to focus** - Measures how much uninterrupted focus time your employees get during the workweek, which are one- to two-hour blocks of time with no collaboration activity. People need this valuable time to complete challenging work, think creatively, and generate new ideas.
* **Getting manager coaching** - Measure how much 1:1 time managers spend with their employees on average each month. Research shows that time spent 1:1 with your manager helps keep employees engaged and improves their job performance and career development.
* **Effective meetings** - Shows the percentage of employees who spend the majority of their time in short or focused meetings, which are less than one hour long with two to eight participants. Research shows short and targeted meetings are more inclusive with higher participation where decisions get made and work gets done.

![Power BI My organization template.](../Images/WpA/Tutorials/pbi-myorg.png)

Each report also includes the following details:

* **How we measure this** - Near the top of each report, you can select "How we measure this" to see what metrics were used to calculate the data and insights provided.
* **Top tools and suggestions** - In the blue area at the top right of each report, you'll see a few suggestions and tool tips that can help support the insights and analysis shown on the page.
* **Supporting articles** - To the right of "Current State," you'll see links to articles about why this analysis matters based on industry research and other businesses experience.
* **Go deeper** - Shows other available reports or options that you can use for more advanced and focused analysis relating to the data shown.
* **Supporting insights** - This section show the top insights that are important to focus on based on the analysis shown. For example, for Protecting personal time, you might see insights about what activities drive most of your employees after-hours work and how many hours they spend collaborating.

The following is an example of what you'll see in the Protecting personal time report:

![Protecting personal time report.](../Images/WpA/Tutorials/pbi-ppt-report.png)

To populate the dashboard in Power BI, you must set up **My organization insights** in Workplace Analytics for Viva Insights. The results will refresh your downloaded Power BI dashboard on a weekly basis.

## Demonstration

This uses sample data that is only representative of the dashboard and might not be exactly what you see in a live dashboard specific to your organization's unique data.

[My organization in Power BI demo](https://msit.powerbi.com/groups/me/reports/a46f5da2-58ba-467d-b1e8-68541ab302ea/ReportSection047f79d6110db8b7d45b?ctid=72f988bf-86f1-41af-91ab-2d7cd011db47&bookmarkGuid=Bookmarkcd33e1e642e6511e8d55)

## Prerequisites  

Before you can run the results and populate the dashboard in Power BI, you must:

* Be assigned the role of [Analyst](../use/user-roles.md) in Workplace Analytics.
* Have the latest version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version.
Then go to [Get Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t?activetab=pivot:overviewtab) to download and install the latest version.

## Set up the dashboard

>[!Note]
>This dashboard is currently only available in English and will only work with data generated from the English version of Workplace Analytics. Before completing the setup steps, confirm or change the browser language to **en-us** in the app's URL: <https://workplaceanalytics.office.com/en-us/Home/>

1. In [Workplace Analytics](https://workplaceanalytics.office.com/), select **Analyze** > **Query designer**.
2. In **Create** > **Other templates**, select **My organization insights** to see the required setup steps, and then in step 2, select **Set up**.
3. When prompted, select or confirm the following settings:

   * **Name** - Customize or keep the default name
   * **Group by** - Select **Week**
   * **Time period** - Select the time period for this analysis
   * **Auto-refresh** - Enable this setting
   * **Exclusions** - Select the preferred rules

   >[!Important]
   >If you try to delete a predefined metric, you'll see a warning that the deletion might disable portions of the Power BI dashboard and reduce results. In turn, this can limit your ability to visualize collaboration patterns. Depending on the metric you delete, you might disable a single Power BI chart, several charts, or all the charts. Select **Cancel** to retain the metric.

4. In **Select filters**, for "**Which measured employees do you want to include?**," you can filter the employees in scope for the dashboard. For more details about filter and metric options, see [Create a Person Query](./person-queries.md).
5. In **Organizational data**, keep the preselected organizational data attributes that the dashboard requires. You can then select any other attributes (columns) to include in the dashboard.

   > [!Important]
   > If you remove the required, preselected organizational data attributes, you might disable one or more Power BI charts.

6. Select **Run** to run the query, which might take several minutes to complete.
7. When prompted, select to go to **Results**. After the results successfully run, select the **Download** icon for the **My organization insights** results, select **PBI template**, and then select **OK** to download the template.

   ![Download the Power BI Teams insights template.](../Images/WpA/Tutorials/teams-template.png)

8. Open the downloaded **My organization insights template**.
9. If prompted to select a program, select **Power BI**.
10. When prompted by Power BI:

    1. In the Workplace Analytics **Query designer** > **Results**, select the **Link** icon for each result, and select to copy the generated OData URL link.
    2. In Power BI, paste each copied link into its respective URL field.
    3. Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Workplace Analytics data.
    4. Select **Load** to import the results into Power BI. Loading these large files may take some time to complete.

    ![Query URLs for Power BI.](../Images/WpA/Tutorials/teams-odata.png)

11. If you're already signed in to Power BI with your Workplace Analytics organizational account, the dashboard visualizations will populate with your data. You are done and can skip the following steps. If not, proceed to the next step.
12. If you're not signed in to Power BI, or if an error occurs when updating the data, sign in to your organizational account again. In the **OData feed** dialog box, select **Organizational account**, and then select **Sign in**. See [Troubleshooting](../tutorials/power-bi-templates.md#troubleshooting) for more details.

    ![Power BI sign in.](../Images/WpA/Tutorials/pbi-sign-in.png)

13. Select and enter credentials for the organizational account that you use to sign in to Workplace Analytics, and then select **Save**.

    >[!Important]
    >You must sign in to Power BI with the same account you use to access Workplace Analytics.

14. Select **Connect** to prepare and load the data, which can take a few minutes to complete.

## Organizational data

After the dashboard is set up and populated with data in Power BI, as a first step, confirm the date range and number of measured employees that's shown at the top of each page is what you expected for this analysis.

>[!Important]
>As new data is processed on a weekly basis, select **Refresh** in the **Power BI Home** ribbon to view the most recent data.

## Power BI tips, troubleshooting, and FAQs

For details about how to share the dashboard and other Power BI tips, troubleshoot any issues, or review the FAQ, see [Power BI tips, FAQ, and troubleshooting](../tutorials/power-bi-templates.md).

## Related topic

[View, download, and export query results](../use/view-download-and-export-query-results.md)
