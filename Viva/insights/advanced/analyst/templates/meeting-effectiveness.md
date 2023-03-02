---
ROBOTS: NOINDEX,FOLLOW
ms.date: 07/14/2022
title: Meeting effectiveness report
description: Learn how to use the Microsoft Viva Insights Power BI template to identify whether employees practice habits that lead to more effective meetings
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

# Meeting effectiveness report

The **Meeting effectiveness** report uses a template populated by Viva Insights data to identify whether employees practice habits that lead to more effective meetings.

The report enables you to:

* Identify behaviors that improve meeting effectiveness.
* Determine which groups are and aren't practicing these behaviors.
* Learn how to drive the behaviors that enable more effective meetings.
* Track how these behavioral patterns change over time.

Each report page includes a **Why it matters** interpretation, **recommended actions**, and **metric definitions**.

To populate the report in Power BI, you’ll need to set up and successfully run the predefined **Meeting effectiveness** query in Viva Insights.

[!INCLUDE [Demonstration](includes/demonstration.md)]

<iframe title="Meeting effectiveness" width="600" height="373.5" src="https://msit.powerbi.com/view?r=eyJrIjoiNmU5NWVkMDctYThiNy00Njc3LThkM2EtZmEwMDI0ZTc3YWQ3IiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9&pageName=ReportSectioncaaab41517184d398c3f" frameborder="0" allowFullScreen="true"></iframe>

[!INCLUDE [Prerequisites](includes/prerequisites.md)]

[!INCLUDE [Report setup and run query](includes/report-setup-run-query.md)]

1. In the Viva Insights analyst experience, select **Analysis**.

2. Under **Power BI templates**, navigate to **Meeting effectiveness** and select **Start analysis**. To get more information about the Meeting effectiveness template before running your analysis, select **Learn more**.

[!INCLUDE [Setup steps](includes/setup-steps.md)]

## Report settings

After the Meeting effectiveness report is set up and populated with Viva Insights data in Power BI:

1. Select the report's time period. This setting primarily alters the data displayed in the trend charts. Reducing the time period to less than eight weeks isn't recommended because some insights, like the month-over-month indicators, won’t have enough data to calculate.

1. Select the report's aggregation period. The aggregation period defines the span of time the report uses to calculate all aggregated insights. For example, if you select **Last 4 weeks**, insights will be aggregated over the four-week period leading up to the end date. Alternatively, if you select **Last 1 week**, insights be aggregated over the last week leading up to the end date.

1. Select the average cost of an employee meeting hour. Change this value to calculate a more accurate value for meeting hours across the report.

1. Select an organizational attribute to view the report by. This attribute is the primary group-by attribute shown in all subsequent pages. You can change this attribute at any time; all subsequent report pages will show values grouped by the new attribute.

1. Select optional filters to exclude employee groups. To filter the measured employee population, you can filter by any selected organizational attribute, and then filter by any of the values for these attributes. If you use these optional filters, the measured employees count will reflect a reduced number.

1. Set exclusions. Use the check boxes to:

    * Exclude employees who are likely non-knowledge workers (that is, those spending less than five hours per week on average in meetings, emails, and/or Teams calls and chats).

    * Exclude weeks that are likely holiday or paid-time-off weeks, or weeks that individuals are on other types of leave.

1. Select the preferred language for your report. Change the language for your report. 

![Screenshot that shows Report settings page in PowerBI.](/viva/insights/advanced/images/me-pbi-report-settings.png)


## About the report

The Meeting effectiveness report includes several report pages that help you find out whether your organization is practicing healthy meeting habits.

Except for the first two pages, each report page follows a similar format: an all-up group average for the metric, and then a breakdown of that metric average by the organizational attribute selected. These averages are calculated over the aggregation period you selected in [report settings](#report-settings). You can also see how the group average has trended from the selected **Start date** to **End date**, or select **Why this matters** for an explanation of the purpose behind the page. Finally, each page ends with a **Take action** suggestion, where you can elect **Explore more** to access additional details about suggested actions.

### Overview

This page shows a high-level overview of all insights included in the report: three insights that address meeting-hour quantity and six insights that address meeting-hour quality.

#### Meeting-hour-quality insights

All insights that show the quality of meeting hours—like Short and small or Advanced meeting notice—are measured as a percent of all person meeting hours that have those traits. For example, let's say two people join a 30-minute meeting. One person joins on time and the other joins late. That meeting had 60 cumulative minutes of meeting time, but only 30 of those minutes were joined on time. So, 50% of meeting time was joined on time.

#### Mover icons

The **Top mover** icon calls out the insight with the greatest change, while the **Bottom mover** icon calls out the insight with the least change.

#### Time-based comparisons

Based on the aggregation period selected, you’ll either see month-over-month comparisons or week-over-week comparisons by default. If you select **Last 4 weeks**, the report shows month-over-month calculations comparing the last four weeks to the four weeks before that. If you select **Last 1 week**, the report shows week-over-week calculations comparing the last one week to the week before that.

### Meeting lifecycle

This page shows similar insights to the overview page, but it displays them based on the phases of the meeting lifecycle: before, during, and after.

When organizing meetings and trying to make sure time is spent effectively, it can help to think about the meeting in these three phases:

* **Before** the meeting, think about who the right attendees are, how much time you’ll need, who your required stakeholders are and whether they’re available, and more.

* **During** the meeting, make sure you get started on time, get through your agenda, and enable people to participate.

* **After** the meeting, evaluate it, ask for feedback, and send out notes and action items.

### Meeting hours

Sometimes it's shocking to learn just how much time your organization spends in meetings. Once you understand that investment, it’s easy to start asking questions about how to decrease the amount of non-productive meeting time. This page displays the value of time spent in meetings. If this value isn't worth tracking in your organization, you can always navigate to **Settings** and set that value to **0**.

### Short and small

This page shows the percentage of meeting hours that are short (between zero and one hours) and small (between two and eight attendees). You can see how this data trends over time, and also the percent distribution of large, long and large, short and small, and long meetings. 

### Advanced meeting notice

On this page, you can see how meetings are being scheduled with advanced notice—that is, the percentage of meeting hours that organizers schedule 24 hours or more before that meeting is set to start. You can also see what portion of meetings fall into even more urgent categories.

### Attendee availability

Use this page to understand the prevalence of overlapping meetings and how available attendees are. This page shows the percentage of meeting hours where an employee had no overlapping meetings on their calendar.

### Joined on time

This page shows the percentage of meeting hours where employees joined a Teams meeting early or within five minutes after the start time.

### Ended on time

This page shows the percentage of meeting hours where employees ended a Teams meeting early or within one minute after the end time. 

### No multitasking

Use this page to understand how multitasking affects your organization. You can see the percentage of meeting hours where a person wasn’t sending or reading emails or chats during a meeting. This page also provides categories of multitaskers based on  number of collaboration hours and multitasking tendencies.

### After meetings

Even after you leave a meeting room (whether physically or virtually), the meeting isn’t done. Make sure that you're always disseminating clear action items and next steps. Also, consider how the meeting went to make sure your next meeting is more effective than the last. This page provides a few helpful tips to ensure this trend remains positive.

#### Glossary

This page defines the metrics and other key terms used in the report. 

[!INCLUDE [Power BI tips and troubleshooting and Related topics](includes/powerbi-tips-related-topic.md)]