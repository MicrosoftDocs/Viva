---
ms.date: 07/14/2022
title: Wellbeing - balance and flexibility report
description: Learn how the Wellbeing - balance and flexibility PowerBI template from Microsoft Viva Insights helps you discover whether your employees maintain work-life balance and flexibility at work
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

# Wellbeing – balance and flexibility report

The **Wellbeing – balance and flexibility report** uses a template populated by Microsoft Viva Insights data to help you get insights into employee wellbeing across your company. This analysis can help you uncover opportunities to improve focus, work-life balance, flexibility at work, and employees’ sense of community.

With this report, you can visualize and explore the following top-level business questions asked by leaders:

* **Protect focus** – Do employees have enough time to focus, and are they using Viva Insights to help find that time?
* **Balance work and life** – Are employees able to protect personal time?
* **Handle urgency** – Can employees manage unexpected demands and proactively shift some to planned work?
* **Embrace flexibility** – Are employees adopting a flexible working schedule?
* **Take breaks** – Are employees able to mindfully disconnect?
* **Stay connected** – Are employees part of a community at work?

![Screenshot that shows the Wellbeing report, Report settings.](/viva/insights/advanced/images/wellbeing-PBI-summary1.png)

Each report page includes a **Why this matters** interpretation, **recommended actions**, and **metric definitions**.

To populate the report in Power BI, you’ll need to set up and successfully run the predefined **Wellbeing – balance and flexibility report** query in Viva Insights.

[!INCLUDE [Demonstration](includes/demonstration.md)]

<iframe title="Wellbeing - Summary" width="600" height="373.5" src="https://msit.powerbi.com/view?r=eyJrIjoiNTcwNGQwMTctYWUwYy00MjAwLThlM2YtYTIwMWI4ZGEwZTg0IiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9" frameborder="0" allowFullScreen="true"></iframe>

[!INCLUDE [Prerequisites](includes/prerequisites.md)]

## Report setup

1.	In the Viva Insights analyst experience, select **Analysis**.
2.	Under Power BI templates, navigate to **Wellbeing – balance and flexibility report** and select **Start analysis**. 
[!INCLUDE [Setup step 3](includes/setup-step-3.md)]
<!--image-->
[!INCLUDE [Setup step 4](includes/setup-step-4.md)]
<!--image-->

[!INCLUDE [Setup steps 5-12](includes/setup-steps-5-12.md)]

## Report settings

After the **Wellbeing - balance and flexibility** report is set up and populated with Viva Insights data in Power BI, review information on the **Summary** page. Then, view and set the following parameters on the **Settings** page. You can find **Settings** on the right panel of the introduction page. You can also adjust the report settings as you go through the report pages through the **Settings** icon.

![Screenshot that shows the Wellbeing report summary page.](/viva/insights/advanced/images/wellbeing-pbi-summary1.png)

* **Select the time period to measure** – This is the time period that you want to analyze. Note that the four-week trend information on the summary page won’t show if the selected time period is less than eight weeks.
* **Select an organizational attribute to view the report by** – This is the primary "group-by" attribute shown in all subsequent reports. You can change this attribute at any time and all subsequent report pages will group values by the new attribute.
* **Select optional filters to exclude employee groups** – To filter the measured employee population, you can filter by any selected organizational attribute, and then filter by any of the values for these attributes. If you use filters, the measured employees count will show a reduced number. Measured employees are the number of employees in the filtered population who were active during the specified time period. Active employees are those who send at least one email or Teams chat during a work week that's included in the current time period.
* **Exclude weeks marked with a holiday indicator** – Select this control to exclude unusually low collaboration weeks based on individual collaboration patterns. These low collaboration weeks usually occur when employees are taking time off from work.
* **Exclude non-knowledge workers** – Select to exclude employees who spend a weekly average of no more than five hours in meetings, emails, instant messages, and calls because they’re unlikely to be knowledge workers or they don’t use Outlook or Teams.

### Customize working hours

For **Embrace flexibility** and **Take break** pages, you can customize the standard working hours for your organization as a baseline. Select **Customize working hours**, and then select the standard start time and end time. Employees’ collaboration patterns will then be compared with these time settings.

![Screenshot that shows the Wellbeing report customize standard working hours page.](/viva/insights/advanced/images/wellbeing-pbi-workinghours1.png)

## About the report

The **Wellbeing - balance and flexibility** report includes the following report pages that help you identify your employees' wellbeing across the company.

### Protect focus

This topic contains three pages, which each focus on a different theme: overview, adoption, and impact.

#### Overview

**Do employees have enough time to focus, and are they using Viva Insights to help find that time?**

Get a baseline view of how much time employees have to focus and how much time they kept as focus time using Viva Insights. This page helps you understand whether employees are actively protecting non-meeting time for focused work. You can also access adoption and impact pages from this page.

#### Adoption

**Are employees using Viva Insights to set aside time for individual work?**

Learn how consistently employees kept focus time over the last four weeks, and whether they’re using a Viva Insights focus plan to book their time. Use this page to:

* Better understand how your company is adopting focus time.
* Discover groups who haven't enrolled in a focus plan but have a high potential to benefit from one.

#### Impact

**How are employees benefiting from protecting time in Viva Insights?**

Find out how focus time is positively impacting employees. Like the last page, this page shows the number of hours employees kept for focus time over the last four weeks, and how employees booked that time--that is, with or without a focus plan. 

Also, use this page to:

* Explore the impact of focus time on after-hours collaboration.
* Reduce meeting conflicts during focus hours by starting a shared no-meeting day plan. 

### Balance work and life

**Are employees able to protect personal time?**

To help understand after-hours working trends, view the:

* Average weekly after-hours collaboration for each employee.
* Distribution of employees by their after-hours collaboration.
* Percentage of employees who were active during the weekends at least once every four weeks.

When you understand employees' after-hours and weekend work behaviors, you might uncover opportunities to protect the boundary between work and personal life.

### Handle urgency

**Can employees manage unexpected demands and proactively shift some to planned work?**

To uncover how unexpected demands are managed in your company, and to unlock opportunities to shift some of these demands to planned work, view:

* The percentage of employees and work weeks involved in urgent collaboration.
* The impact of urgent collaboration on employees' after-hours collaboration patterns. 

This report defines urgent collaboration using the following keywords in the email subject lines or meeting invitation titles: "urgent," "immediately," "ASAP," "fire drill," "immediate action." You can also find this list of keywords in the report.

### Embrace flexibility

**Are employees adopting a flexible working schedule?**

Identify employees' flexibility at work by exploring these three key percentages:

* **Flexible start times** – Weeks where employees had at least one day of flexible start time.
* **Recurring time to disconnect** – Weeks where employees took at least one hour of recurring break each day.
* **Control active hours** – Weeks where employees limited their work activities to their expected working hours. Expected work hours are the hours employees plan to work. For example, if employees have a standard work schedule from 9:00 AM to 5:00 PM, their expected working hours for each day would be eight hours. 

This analysis offers insight into how employees are adopting flexible working schedules.

>[!Tip]
>
>You can customize work hours in the upper right of this page, next to **Settings**.

### Take breaks

**Are employees able to mindfully disconnect?**

Find out how well employees are able to disconnect from work, and identify groups who might experience burnout. View the percentage weeks employees spent in each of the following categories (arranged here from most to least active online):

* Always on 
* Long (non-stop) 
* Long (with breaks)
* Standard (non stop)
* Standard (flexible)
* Low activity

Also view a distribution of this information by organization.


>[!Tip]
>
>You can customize work hours in the upper right of this page, next to **Settings**.

### Stay connected

**Are employees part of a community at work?**

Discover how employees connect with colleagues through small group meetings and informal communication. On this page, you'll find the:

* Average weekly meeting hours employees spent in small group meetings.
* Distribution of emails and chats by colleague type. 

This information offers insight into whether employees are forming communities and rapport at work.

### Other pages

The report also includes:

* A **Behavioral trends** page that tracks key metrics over time.
* A **Take action** page that provides actionable recommendations to improve behaviors.
* An **Explore further** page that highlights the research and studies in each topic.
* A **Glossary page** that describes all the metrics in the report.

[!INCLUDE [Power BI tips and troubleshooting and Related topics](includes/powerbi-tips-related-topic.md)]


