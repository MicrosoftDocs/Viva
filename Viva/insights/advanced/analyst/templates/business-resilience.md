---
ROBOTS: NOINDEX,FOLLOW
title: Business resilience report
description: Learn how to use the Microsoft Viva Insights Power BI template to know about your organization's hybrid workforce experience
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

# Business resilience report

The **Business resilience report** uses a template populated by Viva Insights data to compare employee behavior before and after a business transition.

The report enables you to visualize and explore the following top-level business questions asked by leaders:

* How are collaboration activities changing?
* How has manager coaching changed over time?
* How have internal relationships changed over time?
* Are external relationships being maintained?

Each report page includes a **Why this matters** interpretation, **recommended actions**, and **metric definitions**.

To populate the report in Power BI, you’ll need to set up and successfully run the predefined **Business resilience** query in Viva Insights.

## Demonstration

The following demonstration uses sample data that’s only representative of this report and might not be exactly what you see in a live report specific to your organization's unique data.

<iframe title="Business resilience - Summary" width="600" height="373.5" src="https://msit.powerbi.com/view?r=eyJrIjoiY2RmYWY4YmYtMTdhZC00MTZkLWEwZmMtMDA5ZTczNTIyODI5IiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9" frameborder="0" allowFullScreen="true"></iframe>

## Prerequisites

Before you can run the queries and populate the report in Power BI, you’ll need to:

* Be assigned the role of Insights Analyst in Viva Insights.
* Have the June 2022 (or newer) version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://powerbi.microsoft.com/en-us/getting-started-with-power-bi/) to download and install the latest version.

## Report setup

### Run query

>[!Note]
> For this release of Viva Insights, this report is currently only available in English and will only work with data generated from the English version of Viva Insights.

1. In the Viva Insights Analyst experience, select **Analysis**.

2. Under **Power BI templates**, navigate to **Business resilience** and select **Start analysis**. To get more information about the Business resilience template before running your analysis, select **Learn more**.

    ![Set up the report page in Power BI](/viva/insights/advanced/images/br-pbi-start.png)

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
![Set up the report page in Power BI](/viva/insights/advanced/images/br-pbi-query-setup.png)


4. **In Predefined template metrics**, leave prepopulated metrics as they appear.  
![Set up the report page in Power BI](/viva/insights/advanced/images/br-pbi-predefined-metrics.png)

    >[!Note]
    > Metrics in Power BI templates can't be edited in this release of Viva Insights. To expand the full list of metrics included in the Power BI template, select the arrow in the box beneath Metrics, filters, and organizational attributes.

5. You can filter the employees in scope for the report under **Select which employees you want to include in the query**. Don’t remove the predefined “Is Active” filter. For more details about filter and metric options, see [Person queries](../person-query.md).

    ![Is active filter](/viva/insights/advanced/images/pbi-templates-isactive-filter.png)

6. Under **Select which employee attributes you want to include in the query**, add up to seven organizational attributes. Once the query runs, you can use these attributes to group and filter the reports.

    >[!Important]
    >Some employee attributes are required to set up this Power BI template, which are preselected for you in the query. *Do not remove any preselected attributes.*
    >
    >If you see attributes marked in red and the query’s **Run** button disabled, it means that these required attributes are missing from your organizational data. Contact your admin to upload them.

7. Select **Run** on the upper right side of the screen, which can take a few minutes to complete.

8. When your query results are ready, go to the **Query results** page and select the **Power BI** icon to download the Power BI template and copy the query identifier. You'll need the query identifier later.
<!--- pending confirmation whether users are prompted--->

### Link report to query

9. Open the downloaded Business resilience template.

10. If prompted to select a program, select **Power BI**.

11. When prompted by Power BI:
    1. Paste in the query identifier.
    1. Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Viva Insights data.
    1. Select **Load** to import the query results into Power BI.

12. If prompted by Power BI, sign in using your organizational account. Power BI then loads and prepares the data, which can take a few minutes to complete for large files.

>[!Important]
> You must sign in to Power BI with the same account you use to access Viva Insights.

## Report settings

After the Business resilience report is set up and populated with Viva Insights data in Power BI, you’ll be prompted to select **Baseline** and **Current** time periods, which can’t overlap.

![Set up the report page in Power BI](/viva/insights/advanced/images/br-set-up-report.png)

Select **Next** after you’ve made your selections. If you change your mind later, you’ll be able to change the **Baseline** and **Current** time periods in the **Settings** page.

Then, view and set the following parameters on the **Settings** page.

* **Baseline** – This is the baseline for your analysis; all changes will be compared with this time period.

    >[!Important]
    > Make sure the **Baseline** time period precedes and doesn’t overlap with the **Current** time period. If the two time frames overlap, you'll receive a warning.

* **Current** – This is the time period you want to compare with the **Baseline**.
* **Select an organizational attribute to view the report by** – This is the primary group-by attribute shown in all subsequent pages. You can change this attribute at any time; all subsequent report pages will show values grouped by the new attribute.
* **Select optional filters to exclude employee groups** – To filter the measured employee population, you can filter by any selected Organizational attribute, and then filter by any of the values for these attributes. If you filter, the measured employees count will reflect a reduced number.
* **Exclusions** – Use the check boxes to:
    * Exclude employees who are likely non-knowledge workers (that is, those spending less than five hours per week on average in meetings, emails, and/or Teams calls and chats).
    * Exclude weeks that are likely holiday or paid-time-off weeks, or weeks that individuals are on other types of leave.

## About the report

The **Business resilience report** pages, listed below, directionally highlight where a shift to remote work is having the largest impact. The reports also give you a measurable starting point for identifying where leaders can use tools and processes to support employees in a new way of working. All metrics are defined in the **Glossary**. A **Why it matters** interpretation is also included in a text box for each report.

### Collaboration

**How are collaboration activities changing?**

This page shows how employee collaboration patterns are changing in response to a shift in work patterns, and which collaboration tools people are substituting for in-person interactions. 

Transitions at work can cause changes in employee collaboration patterns as they adjust to a new normal. Groups with large increases in collaboration may be facing challenges managing their workload, while groups with significantly reduced workloads may be struggling to adapt.

### Manager coaching

**How has manager coaching changed over time?**

This page shows how manager coaching has been impacted by your business’s recent transition.

Managers are crucial factors in the development, engagement, and wellbeing of their reports and in periods of transition, managers help their reports prioritize and provide stability. However, long periods of transition could also require managers to take on new or additional responsibilities, leaving less time for them to support their teams. We recommend that individual contributors spend a minimum of one hour per month in 1:1 meetings with their managers, or 15 minutes per week on average. Employees with this level are called “coached employees” in this report.

### Internal connections

**How have internal relationships changed over time?**

This page shows how employee networks are changing and how much time people spend connecting with others. 

Internal relationships are key to preventing isolation and helping employees feel supported and connected to their company’s mission, yet times of change can make it challenging to maintain existing relationships. Large decreases in network size could indicate growing isolation, while large increases could indicate either healthy relationship growth, or if networks become too large, burnout. Meanwhile, small-group conversations build networks and help employees feel less isolated.

### External connections

**Are external relationships being maintained?**

This page shows how different parts of the company may have been impacted by business shifts in different ways.

Despite business changes, it’s important to ensure that relationships with continuing customers, partners, and vendors stay strong. In times of change, internal demands can take precedence over time previously spent with external contacts. Those external contacts may also be refocusing on their own critical priorities and may not have time to meet with your sales and support teams.

For groups with increased external engagement, make sure these business shifts don’t come at the expense of increased after-hours activity and work week spans. For groups experiencing a decrease, consider guiding them to proactively check in with their external contacts.

### Trends

**How are important behaviors evolving over time?** 

This page shows the trends for key leading indicator metrics for business resilience, including collaboration hours, percent of employees with at least one hour per month of manager 1:1s, internal network size, and external collaboration hours.

### Take action

This page lists opportunity areas with related best practices and recommendations and links to related articles about ways to help your managers improve in each area.

### Glossary

The **Glossary** describes metrics used in the report pages.


## Power BI tips, FAQs, and troubleshooting

For details about how to share the report and other Power BI tips, troubleshoot any issues, or review the FAQ, see [Power BI tips, FAQ, and troubleshooting](./power-bi-faq-troubleshoot.md).

## Related topic

[Access query results and modify existing queries](../query-results.md)
