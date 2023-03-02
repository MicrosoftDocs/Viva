---
ms.date: 03/02/2023
title: Manager effectiveness report
description: Learn how the Ways of working PowerBI template from Microsoft Viva Insights helps you gain insight into the collaboration habits and effectiveness of your people managers.
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

# Manager effectiveness report

The **Manager effectiveness report** uses a template populated by Microsoft Viva Insights data to analyze people-manager behaviors in your organization. HR analysts can use this analysis to measure behaviors and trends of people managers across four key themes within your organization: manager capacity, coach, empower, connect, and model.

Each theme includes insights about manager effectiveness and ways to help maintain or increase preferred leadership behaviors. Key metrics are used to deep-dive into each theme, along with a **Why this matters** interpretation and best practices recommended by industry experts.

![Screenshot that shows the Manager effectiveness report, Summary.](/viva/insights/advanced/images/manager-effectiveness-pbi-summary.png)

To populate the report in Power BI, you’ll need to set up and successfully run the predefined **Manager effectiveness** query in Viva Insights.

[!INCLUDE [Demonstration](includes/demonstration.md)]

<iframe title="Manager effectiveness - Summary" width="600" height="373.5" src="https://msit.powerbi.com/view?r=eyJrIjoiNzY1YTI3ZmQtYjVkZi00YTA2LWI0MjEtN2MxNDQ4MGE0YmZjIiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9" frameborder="0" allowFullScreen="true"></iframe>

[!INCLUDE [Prerequisites](includes/prerequisites.md)]

[!INCLUDE [Report setup and run query](includes/report-setup-run-query.md)]

1. In the Viva Insights analyst experience, select **Analysis**.

2. Under **Power BI templates**, navigate to **Manager effectiveness** and select **Start analysis**. To get more information about the Manager effectiveness template before running your analysis, select **Learn more**.

    ![Query start](/viva/insights/advanced/images/me-pbi-start.png)

[!INCLUDE [Setup steps](includes/setup-steps.md)]

## Report settings

After the **Manager effectiveness report** is set up and populated with Viva Insights data in Power BI, map values as prompted, which are listed below.

|Value   |Prompt| 
|----------|----|
|Individual contributor     |Select the attribute values that identify employees as individual contributors who do not manage people within your organization      |
|Manager indicator|Select the attribute values that identify managers who manage people within your organization, such as **Mgr** and **Mgr+.**|

![Screenshot that shows the Manager effectiveness report IC and Mgr questions.](/viva/insights/advanced/images/manager-effectiveness-pbi-questions.png)

After this initial prompt, you can then select **Settings** at top right of any page to view and change the following parameters:

* **Select the time period for the report** – Select the time period for which you want to view data in the report. 

* **Select an attribute to group data by** – Select the primary group-by attribute shown in all the reports. You can change this attribute at any time and all report pages will show group values by the new attribute.

* **Select optional report filter** – Select the organizational attribute and values you want to filter the employees in the report.

* **Exclusions** – Use the check boxes to:

    * Exclude employees who are likely non-knowledge workers (that is, those spending less than five hours per week in meetings, emails, and/or Teams calls and chats).

    * Exclude weeks that are likely holiday or paid-time-off weeks or weeks that individuals are on other types of leave.

* **Select the preferred language for your report** – Change the language for your report. 

![Screenshot that shows the Manager effectiveness report, customize report.](/viva/insights/advanced/images/manager-effectiveness-pbi-customize-report.png)


## About this report

The report contains one report page per theme, and each report page asks a related business question. The following section:

* Lists the report pages that fall under each theme and describes which data they contain.

* Describes the report’s **Behavioral trends** and **Take action** pages. 

### Manager capacity

**Do managers have enough time for their employees?**

This page shows the weekly average number of hours that managers spent collaborating with people in the company, divided into groups and types of communication (meetings, emails, chats, and calls). It also shows the average percentage of collaboration time that managers spent with direct reports as compared to others in the organization.

### Coach

**Are employees receiving sufficient coaching time with their manager?**

This page analyzes managers’ behavior in scheduling 1:1 time with their direct reports by groups. Metrics include monthly average number of minutes in 1:1 meetings with direct reports, percentage of employees who receive a different number of 1:1 hours with their manager, and the average frequency of 1:1 time (weekly, monthly, or quarterly).

### Empower

**Are managers balancing oversight with employee autonomy?**

This page shows the percentage of employees whose managers co-attend their meetings and might be micromanaging them as direct reports. It also shows the weekly average number of hours that managers co-attended meetings and spent in 1:1 meetings with their direct reports.

### Connect

**How well-connected are managers and do they leverage their network to help build connections for their employees?**

This page shows the internal network size distribution of managers as compared to the full organizational population, calling out the share of managers who are among the top 25% most connected employees in the company. It also shows the average internal network size of managers as compared to individual contributors broken out by group.

## Model

**Are managers modeling good work-life balance habits?**

This page shows the distribution of managers by average weekly time spent in after-hours collaboration, calling out the share of managers spending more than five hours per week in collaboration outside of their set working hours. It also shows the difference in average after-hours collaboration hours for managers and individual contributors, broken out by group. 

### Behavioral trends

**How are manager behaviors evolving?**

This page shows the trends for key leading indicator metrics for managers, including metrics about coaching and empowerment, network connections, and after-hours work habits.

### Take action

**How can manager effectiveness be improved?** 

This page lists opportunity areas with related best practices and recommendations and links to related articles about ways to help your managers improve in each area.

### Glossary

The **Glossary** describes metrics used in the report pages.

[!INCLUDE [Power BI tips and troubleshooting and Related topics](includes/powerbi-tips-related-topic.md)]

