---
ms.date: 03/13/2023
title: New hire onboarding and development report
description: Learn how the New hire onboarding and development PowerBI template from Microsoft Viva Insights helps you 
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

# New hire onboarding and development report

The **New hire onboarding and development** report  helps leaders understand the onboarding experience of new hires and/or employees who've started out in a new role within the company. The report also identifies opportunities to improve the onboarding experience and structure development. 

Because research shows it typically takes new employees 12 months to reach their full performance potential, this report focuses on the entire period a new hire is learning, connecting, and developing in their new role. Additionally, you can customize the definition of new hire to best fit your organization: whether it includes employees who recently joined the company or also employees who recently started out in a new role. You can also customize the number of months the new hire should be in the new role.

This report has three sections, which each address different facets of the onboarding experience for new hires and those new in role. These sections help you answer the following business questions: 

* **Coach with managers**
    * Are new hires getting the 1:1 coaching and support from their managers that they need? 
* **Boost time spent in training** 
    * Is the organization sufficiently encouraging new hires and employees to set aside time for learning?
* **Foster new hire networks** 
    * How are new hires developing their network and how fast are they integrating into the organization’s network?

Key metrics provide a deep-dive into each topic, along with a **Why it matters** interpretation and recommended actions. 

To populate the report in Power BI, you’ll need to set up and successfully run the predefined **Onboarding and development** query in Viva Insights. 

[!INCLUDE [Demonstration](includes/demonstration.md)]

<iframe title="Ways of Working - Summary" width="600" height="373.5" src="https://msit.powerbi.com/view?r=eyJrIjoiYWE0MGExNGEtMmIwNC00ZDg4LWI4MmYtYWM2Yjc0NzAzMmI2IiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9" frameborder="0" allowFullScreen="true"></iframe>

[!INCLUDE [Prerequisites](includes/prerequisites.md)]

[!INCLUDE [Report setup and run query](includes/report-setup-run-query.md)]
* Have the **HireDate** attribute, which indicates when a person was hired, uploaded as part of your organizational data.

>[!Note]
>If you want your report to include new hires and existing employees who've transferred to a new role, you'll also need to include the **RoleStartDate** attribute, which indicates when a person started in a new role or function. Without **RoleStartDate**, however, the rest of the report will still load. 
>
>You can add new attributes to your organizational data at any time. For more details on how to add new data for existing employees, refer to [subsequent uploads](../../admin/upload-org-data-subsequent.md) 


1. In the Viva Insights analyst experience, select **Analysis**.
2. Under **Power BI templates**, navigate to **Onboarding and development** and select **Start analysis**. 

[!INCLUDE [Setup steps new hire](includes/setup-steps-newhire.md)]

## Report settings

After the **Onboarding and development** report is set up and populated with Viva Insights data in Power BI, map values as prompted, which are listed below: 

* **New hire categories** – Select the categories you want to consider as “new hires” in the report. Include “Employees who are new to the company,” “Employees who are new in role,” or both. 
* **Max/number of months in role to consider** – Select the maximum number of months the new hire needs to be with the company or in the new role to be considered a “new hire.”  

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

### Coach with managers  

**Are new hires getting the 1:1 coaching and support from their managers that they need?**

Learn how much time employees spend, on average, in monthly 1:1s with their manager. We display this information by group and also by new hires versus tenured employees. 

Here's what the visuals on this page show:

* Middle chart – Percentage of new hires who get a recommended minimum 50 minutes of monthly 1:1 time with their managers
* Lower middle chart – Distribution of new hires and tenured employees by the average monthly manager 1:1 time they receive
* Top right chart – How the average monthly time in manager 1:1s is trending over time  

### Boost time spent in training 

**Is the organization sufficiently encouraging new hires and employees to set aside time for learning?** 

View the average hours employees spent in training-related calendar events per month, broken out by new hires and tenured employees. 

Here's what the visuals on this page show:

* Middle card 
    * Hero metric – Percentage of new hires who don't have any training-related calendar events in a month
    * Chart – Distribution of employees by average monthly training-related calendar events, broken out by new hires and tenured employees
* Top right chart – How the average monthly time in training-related calendar events is trending over time

#### About training-related keywords

This report figures out which calendar events are training related by using keywords from meeting and appointment titles in Outlook. We've added a default set of keywords that contains these terms:

* train
* learn
* course
* introduction
* onboarding
* induction
* academy
* education
* brown bag


##### To customize your keywords

You can change which keywords the report uses by editing your query in the advanced insights app. First, you'll create your own version of the **Calendared learning time** metric, and then you'll add that metric to your query.

###### Create your own version of the Calendared learning time metric

1. Select **Add metrics**.
1. Expand the **Learning time** group.
 1. On **Calendared learning time**, select the ellipses, and then select **Clone**. The metric builder opens.
1. To remove keywords:
    1. Under step 3 in the metric builder, select the trashcan icon to the right of the **Value** field.
1. To add keywords:
    1. Under step 3 in the metric builder, select **Add condition**.
    1. Set the **Meeting activity** attribute to "Meeting," and leave the **Meeting attribute** at "Subject" and the **Operator** at "=."
    1. Under **Value**, enter the keyword you want the query to look for in meeting and appointment titles. For example, if you wanted to include meetings with the word "skills" in the title, you'd add "skills" as the value here.
    1. Repeat steps a through c for as many keywords as you want to add.
1. Under **Name and publish**, add a name for your new metric. You can edit the **Description** if you want.
1. Under **Publication**, select the checkbox if you want other analysts in your organization to be able to use this metric in future queries.
1. Select **Save and publish**, or just **Save** if you chose not to make the metric available to other analysts. You'll arrive back at the query page.

###### Add your new metric to the query

1. On the query page, select **Add metrics** again. 
1. Expand the **Defined by me** metric category. You'll find your new metric there.
1. Select the checkbox next to your new metric.
1. Select the **Add to query** button.

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
* **Take action** recommendations – Discover opportunity areas and recommended actions for each section in the report

[!INCLUDE [Power BI tips and troubleshooting and Related topics](includes/powerbi-tips-related-topic.md)]
