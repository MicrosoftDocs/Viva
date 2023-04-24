---
ROBOTS: NOINDEX, NOFOLLOW
ms.date: 04/24/2023
title: Onboarding and development report
description: Learn how the Onboarding and development PowerBI template from Microsoft Viva Insights helps you support new employees and those transitioning to a new role
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

# Onboarding and development report

The **Onboarding and development** report helps leaders understand the onboarding experience of new hires and/or employees who've started out in a new role within the company. The report also identifies opportunities to improve the onboarding experience and structure development. 

Because research shows it typically takes new employees 12 months to reach their full performance potential, this report focuses on the entire period a new hire is learning, connecting, and developing in their new role. Additionally, you can customize the definition of new hire to best fit your organization: whether it includes employees who recently joined the company or also employees who recently started out in a new role. You can also customize the number of months the new hire should be in the new role.

This report has three sections, which each address different facets of the onboarding experience for new hires and those new in role. These sections help you answer the following business questions: 

* **Coach with manager 1:1s**
    * Are new hires getting the 1:1 coaching and support from their managers that they need? 
* **Boost time spent learning** 
    * Is the organization sufficiently encouraging new hires and employees to set aside time for learning?
* **Foster new hire networks** 
    * How are new hires developing their network and how fast are they integrating into the organization’s network?

Key metrics provide a deep-dive into each topic, along with a **Why it matters** interpretation and recommended actions. 

To populate the report in Power BI, you’ll need to set up and successfully run the predefined **Onboarding and development** query in Viva Insights. 

[!INCLUDE [Demonstration](includes/demonstration.md)]

<iframe title="Report Section" width="600" height="373.5" src=https://msit.powerbi.com/view?r=eyJrIjoiZjhhNTI3ZDktNDBmYi00MDZjLWFmNjgtNTEyYmM5ZDg3MjU5IiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9 frameborder="0" allowFullScreen="true"></iframe>

[!INCLUDE [Prerequisites](includes/prerequisites.md)]
* Have the **HireDate** attribute, which indicates when a person was hired, uploaded as part of your organizational data.

>[!Note]
>If you want your report to include new hires and existing employees who've transferred to a new role, you'll also need to include the **RoleStartDate** attribute, which indicates when a person started in a new role or function. Without **RoleStartDate**, however, the rest of the report will still load. 
>
>You can add new attributes to your organizational data at any time. For more details on how to add new data for existing employees, refer to [subsequent uploads](../../admin/upload-org-data-subsequent.md).

[!INCLUDE [Report setup and run query](includes/report-setup-run-query.md)]


1. In the Viva Insights analyst experience, select **Analysis**.
1. Under **Power BI templates**, navigate to **Onboarding and development** and select **Start analysis**. 

[!INCLUDE [Setup steps](includes/setup-steps.md)]

## Report settings

After the **Onboarding and development** report is set up and populated with Viva Insights data in Power BI, map values as prompted, which are listed below: 

* **New hire categories** – Select the categories you want to consider as “new hires” in the report. Include “Employees who are new to the company,” “Employees who are new in role,” or both. 
* **Max. number of months in role to consider** – Select the maximum number of months the new hire needs to be with the company or in the new role to be considered a “new hire.”  

After this initial prompt, you can view and set the following parameters on the **Settings** page:

* **Select the time period for the report** – Select the time period for which you want to view data in the report.  
* **View report by** – Select the primary group-by attribute shown in all the report pages. You can change this attribute at any time and all report pages will show group values by the new attribute.
* **Filter by attribute** (optional) – Select the organizational attribute and values you want to use to filter the employees shown in this report.
* **Exclusions** – Use the check boxes to:
    * Exclude employees who are likely non-knowledge workers (that is, those spending less than five hours per week in meetings, emails, and/or Teams calls and chats).
    * Exclude weeks that are likely holiday or paid-time-off weeks or weeks that individuals are on other types of leave.
* **Select the preferred language for your report** – Change the language for your report. 

After confirming the settings, check the number of measured employees to confirm this is the population you want to analyze.

## About this report

In this section, we:

* Provide metrics specific to this report. 
* List the three main report pages, including the business question the page seeks to answer and the type of insights and data the page contains. 

### Coach with manager 1:1s 

**Are new hires getting the 1:1 coaching and support from their managers that they need?**

Learn how much time employees spend, on average, in monthly 1:1s with their manager. We display this information by group and also by new hires versus tenured employees. 

Here's what the visuals on this page show:

* Middle chart – Percentage of new hires who get a recommended minimum 50 minutes of monthly 1:1 time with their managers
* Lower middle chart – Distribution of new hires and tenured employees by the average monthly manager 1:1 time they receive
* Top right chart – How the average monthly time in manager 1:1s is trending over time  

### Boost time spent learning 

**Is the organization sufficiently encouraging new hires and employees to set aside time for learning?** 

View the average hours employees spent in learning-related calendar events per month, broken out by new hires and tenured employees. 

Here's what the visuals on this page show:

* Middle card 
    * Hero metric – Percentage of new hires who don't have any learning-related calendar events in a month
    * Chart – Distribution of employees by average monthly learning-related calendar events, broken out by new hires and tenured employees
* Top right chart – How the average monthly time in learning-related calendar events is trending over time

#### About learning-related keywords

This report figures out which calendar events are learning related by using keywords from meeting and appointment titles in Outlook. We've added a default set of keywords that contains these terms:

* train
* learn
* course
* introduction
* onboarding
* induction
* academy
* education
* brown bag
* brownbag

To learn more about customizing metrics, refer to [Customizing metrics in Viva Insights](../custom-metrics.md).

### Foster new hire networks 

**How are new hires developing their network and how fast are they integrating into the organization’s network?** 

Learn how new hires are negotiating and creating networks at work, and also whether those new hires are getting enough manager coaching time.

Here are the visuals that this page shows:

* Left card – Average internal network size, split by connections within groups and across groups
* Middle chart – How sufficient manager coaching time (that is, 50 minutes or more per month) affects employees' average network size within groups and across groups
* Top right chart – How the average internal network size is trending over time

#### About connections within and between groups

This report bases internal network size on the number of people a person had a reciprocal interaction within the past month. These interactions can happen within and across groups.

Connections within groups are based on *strong ties*. A strong tie happens when two people frequently communicate and have several network connections in common. Strong ties usually indicate that two people are in the same workgroup or on the same team. 

Connections across groups are based on *diverse ties*. A diverse tie happens when two people interact but don't have any common connections, or when two people interact for the first time. Diverse ties offer good sources of new and varied information from across the company.


### Glossary

View this report's metrics.

### Other features 

The report also includes the following features: 

* **Why it matters** interpretations – Get additional context and links to supporting research. 
* **Take action** recommendations – Discover opportunity areas and recommended actions for each section in the report.

[!INCLUDE [Power BI tips and troubleshooting and Related topics](includes/powerbi-tips-related-topic.md)]
