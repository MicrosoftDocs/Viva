---

title: Power BI Quickstart overview dashboard
description: Use the Quickstart overview dashboard to visualize predefined data from Workplace Analytics in Power BI
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Quickstart overview

The Quickstart overview dashboard for Power BI uses Workplace Analytics data to provide a high-level view of key organizational metrics. It's a great way to get a quick perspective on how the organization is collaborating and to identify potential areas that might require additional analysis.

This dashboard provides insights into the following areas about your organization.

* **Population overview** – Shows the number of employees who are included in this analysis and trends for the key collaboration indicators, including average values for the most recent week’s top collaboration metrics.
* **Organizational pulse** – Shows collaboration profiles by group and how employees spend their time, which can help you identify opportunities to improve employee capacity. Look for groups that spend excessive hours in email or spend too much time in low quality meetings.
* **Stress in the organization** – Shows key metrics drive and impact employee stress, including uneven work loads, time fragmentation, or long hours, and helps indicate where workloads can be rebalanced and working norms improved.
* **Onboarding and engagement** – Shows key indicators about employee network diversity, onboarding and integration, and initiative and engagement across the organization, which helps you analyze onboarding effectiveness, job satisfaction, and performance. This data is often paired with additional outcome data, such as employee surveys.
* **Leadership profile** – Shows key indicators about meetings with managers and leadership exposure, which helps you understand how well managers in your organization are supporting and empowering employees to do their best work.

To populate the dashboard in Power BI, you must set up and successfully run the predefined **Quickstart overview** query in Workplace Analytics.

## Prerequisites

Before you can run the query and populate the dashboard in Power BI, you must:

* Be assigned the role of [Analyst](../use/user-roles.md) in Workplace Analytics.
* Have the latest version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t?activetab=pivot:overviewtab) to download and install the latest version.

## Set up the dashboard

1. In [Workplace Analytics](https://workplaceanalytics.office.com/), select **Analyze** > **Queries**.
2. Under **Start from preselected filters and metrics**, select **Quickstart overview** to open the predefined query, which contains the required metrics to populate the dashboard.
3. Select or confirm the options for **Group by**, **Time period**, and **Meeting exclusions**.
4. In **Select metrics**, keep the preselected metrics, which are required for the dashboard to work.
5. In **Select filters**, select **Active only** for **Which measured employees do you want to include in your query results?** Optionally, you can further filter the employees in scope for the dashboard. For more details about filter and metric options, see [Create a Person Query](./person-queries.md).
6. In **Organizational data**, you can choose **Select all** to include all available attributes. At a minimum, select those required for the dashboard to work, such as **HireDate**, **LevelDesignation**, **ManagerId**, **Organization**, and **TimeZone**.
7. Select **Run** (at top right) to run the query, which can take a few minutes up to a few hours to complete.
8. After the query successfully runs, in **Queries** > **Results**, select the **Download** icon for the **Quickstart overview** query results, select **PBI template**, and then select **OK** to download the template.
9. Open the downloaded **Quickstart overview template**.
10. If prompted to select a program, select **Power BI**.
11. When prompted by Power BI, in Workplace Analytics **Queries** > **Results**, select the **Link** icon for the Quickstart overview query, and then select to copy the generated OData URL link, and then select **Load** to import the query results into Power BI. Loading these large files may take a few minutes to a few hours to complete.
12. If you're already signed in to Power BI with your Workplace Analytics organizational account, the dashboard visualizations will populate with your data. You are done and can skip the following steps. If not, proceed to the next step.
13. If you're not signed in to Power BI, or if an error occurs when updating the data, sign in to your organizational account again. In the **OData feed** dialog box, select **Organizational account**, and then select **Sign in**. See [Troubleshooting](../tutorials/power-bi-templates.md#troubleshooting) for more details.

    ![Power BI sign in](../Images/WpA/Tutorials/pbi-sign-in.png)

14. Select and enter credentials for the organizational account that you use to sign in to Workplace Analytics, and then select **Save**.

     >[!Important]
     >You must sign in to Power BI with the same account you use to access Workplace Analytics.

15. Select **Connect** to prepare and load the data, which can take a few minutes to complete. After the data loads, you'll see visualization charts in Power BI about collaboration patterns within your organization.

## Power BI tips, troubleshooting, and FAQs

For details about how to share the dashboard and other Power BI tips, troubleshoot any issues, or review the most frequently asked questions, see [Power BI templates in Workplace Analytics](../tutorials/power-bi-templates.md).

## Related topic

[View, download, and export query results](../use/view-download-and-export-query-results.md)
