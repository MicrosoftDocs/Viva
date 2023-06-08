---
ms.date: 04/27/2023
title: Recurring meeting audit Power BI report
description: Understand whether expensive large and long recurring meetings in your organization are worth their cost
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

# Recurring meeting audit report

The **Recurring meeting audit** Power BI report uses a template populated by Viva Insights data to help you understand whether expensive large and long recurring meetings in your organization are worth their cost.

Use this report to:

* Examine the quality of your most expensive recurring meetings.
* Learn about actions you can take to improve or remove these costly meetings.

The report includes recommended actions and metric definitions.

To populate the report in Power BI, you’ll need to set up and successfully run the predefined **Recurring meeting audit** query in Viva Insights.

[!INCLUDE [Demonstration](includes/demonstration.md)]

<iframe title="Report Section" width="600" height="373.5" src=https://msit.powerbi.com/view?r=eyJrIjoiODNjZmZhNTktOTI1NS00NjRkLThkZTQtYzEyNTNhNzkzMWUyIiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9 frameborder="0" allowFullScreen="true"></iframe>

## Prerequisites

Before you can run the queries and populate the report in Power BI, you’ll need to:

* Be assigned the role of **Insights Analyst** in Viva Insights.
* Have the December 2022 (or newer) version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://powerbi.microsoft.com/en-us/getting-started-with-power-bi/) to download and install the latest version.

[!INCLUDE [Report setup and run query](includes/report-setup-run-query.md)]

1. In the Viva Insights analyst experience, select **Analysis**.
2. Under **Power BI templates**, navigate to **Recurring meeting audit** and select **Start analysis**. 

[!INCLUDE [Setup steps](includes/setup-steps-meetingquery.md)]

## About report settings

After the **Recurring meeting audit** report is set up and populated with Viva Insights data in Power BI, you can view and set certain parameters within each page. We talk about specific settings in [About the report](#about-the-report) below. For a full list of settings and what they do, jump to the [Reference](#reference) section.

## About the report

### Overview

**Which groups are scheduling the greatest meeting load?**

Use this page to view groups in your company, and:

* The number of meetings those groups are scheduling.
* The average attendance and duration of those meetings.
* The total cost of those meetings, and how that cost is changing over time. 

After you’ve taken a look at all groups, use the information on this page to investigate which groups contribute most to overall meeting cost, or those who have large average attendances or durations. It’s helpful to view the biggest contributors to overall meeting cost. However, it might also be worthwhile to identify groups with lower overall cost but a tendency to schedule large and lengthy meetings. 

>[!Note]
> To change the date range of this report, use the **Start and end date** field. This field is the first filter from the right at the top of the page.

Pick a few groups you want to learn more about. You’ll learn more on the next page, **Meeting view**.

### Meeting view

**What recurring meeting series do we need to make more lean?**

Use this page to filter the groups you identified on the **Overview** page. For example, if you wanted to learn more about recurring meetings in the Marketing organization, you’d set the **Filter value** dropdown to “Marketing.” When you set this filter, you’ll get a list of the meetings that group scheduled. The list shows the most expensive meeting series, sorted by cost.

>[!Note]
>The default value for the **Filter by scheduler’s** dropdown is “Organization.” To filter by other organizational attributes—that is, pieces of descriptive information about the meeting scheduler—you’d need to add those attributes in while you’re building your query. Refer to step 6 above.

After you set your filters, explore quality and quantity metrics for each meeting series. All metrics, except meeting count and cost, are averages of meetings that happen between the **Start and end date**. 

When you hover over **Scheduler**, you'll see organizational attributes of the individual who scheduled the meeting, but not who that individual is. This information can help you contact the scheduling organization so you can make changes to the meeting series or provide recommendations about it.

#### About blank or "unknown" values

The **Meeting series title** field might be blank if your organization is suppressing all email subject lines and meeting titles. If **Meeting series title** is blank, you can still see other fields, like **Scheduler** and associated metrics. Contact your Insights Administrator if you need to view **Meeting series title**. 

If "Unknown" appears as the **Scheduler**, the scheduler has no organizational attributes. This might be because the organizational data file your admin uploaded has incomplete data, or the scheduler doesn't have a Viva Insights license.


### Take action

Find opportunity areas for your organization. This page includes best practices, recommendations, and links to related articles about ways to reclaim time by modifying how these expensive meetings are organized.

### Glossary

View the definitions of various concepts in the report.

## Reference

### Report settings

To find the **Settings** page, select the **Settings** link in the top-right corner of any report page. In **Settings**, you can make changes to the following parameters:

|Setting name(s)|Description|
|---------------|------------|
|**Select the report’s start and end date**|Use the calendar picker to set your report’s date range. Your report will only include meetings that occur after the start date and before the end date.
|**View report by scheduler’s...**|	The default value is “Organization,” so all report pages will group by the scheduler’s organization. To group by other organizational attributes—that is, pieces of descriptive information about the meeting scheduler—you’d need to add them while you’re building your query. Refer to step 6 in Run query.
|<ul><li>**Filter by scheduler’s...**<li>**Filter value**| Set filters to exclude or include meetings based on certain attributes of the meeting scheduler. For example, if you only want to view meetings scheduled by people in the Sales organization, you’d set Filter by scheduler’s to “Organization” and Filter value to “Sales.” <br><br>If you use these filters, you’ll notice the measured meetings count—located on the page’s right—reflects a reduced number.
|**Average cost of employee hour**|Set the average cost of an employee hour. The default value is 75, but you can set it from 0 – 1,000 to calculate a more accurate value for meeting hours across the report.
|<ul><li>**Filter by average meeting series duration** <li>**Filter by average meeting series attendance**|Filter which meetings appear in your report by setting average duration and attendance. The report gets these averages from all instances of a recurring meeting that happened between the two dates you set earlier.<br><br>For example, if you only want your report to include meetings between 30 minutes and 60 minutes on average, you’d set the low end of the slider to “30” and the high end of the slider to “60.“ Similarly, if you only want your report to include meetings with between 2 and 10 people, you’d set the low end of the slider to “2” and the high end of the slider to “10.”
|**Search meeting series name**| Filter which meetings appear in your report based on a keyword in their titles. For example, if you only want to include meetings that have “monthly” in the title, you’d add “monthly” as a keyword in the search bar here. <br><br>If the meeting organizer modifies the title, the report uses the most recent title for the meeting series name. The report allows one keyword at a time.|
|**Don’t include in the report**|Select the check box to leave out meetings that are probably blocks on people’s calendars. These blocks might be no-meeting days or similar events where people accept the invitation, but no one joined the meeting on Teams for the entire series. Deselect this box to include all meetings.

  
[!INCLUDE [Power BI tips and troubleshooting and Related topics](includes/powerbi-tips-related-topic.md)]
