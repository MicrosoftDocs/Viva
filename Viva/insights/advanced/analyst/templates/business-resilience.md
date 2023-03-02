---
ms.date: 03/02/2023
title: Business resilience report
description: Learn how to use the Microsoft Viva Insights Power BI template to compare employee behavior before and after a business transition
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

With this report, you can visualize and explore the following top-level business questions asked by leaders:

* How are collaboration activities changing?

* How has manager coaching changed over time?

* How have internal relationships changed over time?

* Are external relationships being maintained?

Each report page includes a **Why this matters** interpretation, **recommended actions**, and **metric definitions**.

To populate the report in Power BI, you’ll need to set up and successfully run the predefined **Business resilience** query in Viva Insights.

[!INCLUDE [Demonstration](includes/demonstration.md)]

<iframe title="Business resilience - Summary" width="600" height="373.5" src="https://msit.powerbi.com/view?r=eyJrIjoiY2RmYWY4YmYtMTdhZC00MTZkLWEwZmMtMDA5ZTczNTIyODI5IiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9" frameborder="0" allowFullScreen="true"></iframe>

[!INCLUDE [Prerequisites](includes/prerequisites.md)]

[!INCLUDE [Report setup and run query](includes/report-setup-run-query.md)]

1. In the Viva Insights analyst experience, select **Analysis**.

2. Under **Power BI templates**, navigate to **Business resilience** and select **Start analysis**. For more information about the Business resilience template before running your analysis, select **Learn more**.

    ![Screenshot that shows the Business resilience icon.](/viva/insights/advanced/images/br-pbi-start.png)

[!INCLUDE [Setup step 3](includes/setup-step-3.md)]

    ![Screenshot that shows the Query setup section.](/viva/insights/advanced/images/br-pbi-query-setup.png)

[!INCLUDE [Setup step 4](includes/setup-step-4.md)]

    ![Screenshot that shows predefined metrics.](/viva/insights/advanced/images/br-pbi-predefined-metrics.png)

[!INCLUDE [Setup steps 5-12](includes/setup-steps-5-12.md)]

## Report settings

After the Business resilience report is set up and populated with Viva Insights data in Power BI, you’ll be prompted to select **Baseline** and **Current** time periods, which can’t overlap.

![Screenshot that shows the Set up the report page in Power BI.](/viva/insights/advanced/images/br-set-up-report.png)

Select **Next** after you’ve made your selections. If you change your mind later, you’ll be able to change the **Baseline** and **Current** time periods in the **Settings** page.

Then, view and set the following parameters on the **Settings** page.

* **Baseline** – This is the baseline for your analysis; all changes will be compared with this time period.

    >[!Important]
    > Make sure the **Baseline** time period precedes and doesn’t overlap with the **Current** time period. If the two time frames overlap, you'll receive a warning.

* **Current** – This is the time period you want to compare with the **Baseline**.

* **Select an organizational attribute to view the report by** – This is the primary group-by attribute shown in all subsequent pages. You can change this attribute at any time; all subsequent report pages will show values grouped by the new attribute.

* **Select optional filters to exclude employee groups** – To filter the measured employee population, you can filter by any selected organizational attribute, and then filter by any of the values for these attributes. If you filter, the measured employees count will reflect a reduced number.

* **Exclusions** – Use the check boxes to:

    * Exclude employees who are likely non-knowledge workers (that is, those spending less than five hours per week on average in meetings, emails, and/or Teams calls and chats).

    * Exclude weeks that are likely holiday or paid-time-off weeks, or weeks that individuals are on other types of leave.

* **Select the preferred language for your report** – Change the language for your report. 


## About the report

The **Business resilience report** pages, listed below, directionally highlight where a shift to remote work is having the largest impact. The reports also give you a measurable starting point for identifying where leaders can use tools and processes to support employees in a new way of working. All metrics are defined in the **Glossary**. A **Why it matters** interpretation is also included in a text box for each report.

### Collaboration

**How are collaboration activities changing?**

This page shows how employee collaboration patterns are changing in response to a shift in work patterns, and which collaboration tools people are substituting for in-person interactions. 

Transitions at work can cause changes in employee collaboration patterns as they adjust to a new normal. Groups with large increases in collaboration might be facing challenges managing their workload, while groups with significantly reduced workloads might be struggling to adapt.

### Manager coaching

**How has manager coaching changed over time?**

This page shows how manager coaching has been impacted by your business’s recent transition.

Managers are crucial factors in the development, engagement, and wellbeing of their reports and in periods of transition, managers help their reports prioritize and provide stability. However, long periods of transition could also require managers to take on new or additional responsibilities, leaving less time for them to support their teams. We recommend that individual contributors spend a minimum of one hour per month in 1:1 meetings with their managers, or 15 minutes per week on average. Employees with this level of 1:1 interaction with their managers are called *coached employees* in this report.

### Internal connections

**How have internal relationships changed over time?**

This page shows how employee networks are changing and how much time people spend connecting with others. 

Internal relationships are key to preventing isolation and helping employees feel supported and connected to their company’s mission, yet times of change can make it challenging to maintain existing relationships. Large decreases in network size could indicate growing isolation, while large increases could indicate either healthy relationship growth, or if networks become too large, burnout. Meanwhile, small-group conversations build networks and help employees feel less isolated.

### External connections

**Are external relationships being maintained?**

This page shows how different parts of the company may have been impacted by business shifts in different ways.

Despite business changes, it’s important to ensure that relationships with continuing customers, partners, and vendors stay strong. In times of change, internal demands can take precedence over time previously spent with external contacts. Those external contacts might also be refocusing on their own critical priorities and might not have time to meet with your sales and support teams.

For groups with increased external engagement, make sure these business shifts don’t come at the expense of increased after-hours activity and work week spans. For groups experiencing a decrease, consider guiding them to proactively check in with their external contacts.

### Trends

**How are important behaviors evolving over time?** 

This page shows the trends for key leading indicator metrics for business resilience, including collaboration hours, percent of employees with at least one hour per month of manager 1:1s, internal network size, and external collaboration hours.

### Take action

This page lists opportunity areas with related best practices and recommendations and links to related articles about ways to help your managers improve in each area.

### Glossary

The **Glossary** describes metrics used in the report pages.

[!INCLUDE [Power BI tips and troubleshooting and Related topics](includes/powerbi-tips-related-topic.md)]