---
ms.date: 03/04/2024
title: Meeting effectiveness report
description: Learn how to use the Microsoft Viva Insights Power BI template to identify whether employees practice habits that lead to more effective meetings
author: kateylundquist
ms.author: v-klundquist
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

 >[!Note]
>To improve clarity and eliminate confusion, we've changed the names of several insights in this report. While the conclusions drawn from the data are the same, you'll notice a shift from a passive tone to a more actionable tone in how the insights are framed. Learn more about this change [here](https://techcommunity.microsoft.com/t5/viva-insights-blog/updated-insight-names-in-meeting-effectiveness-report-template/ba-p/3884865).

[!INCLUDE [Demonstration](includes/demonstration.md)]

> [!VIDEO https://msit.powerbi.com/view?r=eyJrIjoiNmU5NWVkMDctYThiNy00Njc3LThkM2EtZmEwMDI0ZTc3YWQ3IiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9&pageName=ReportSectioncaaab41517184d398c3f]

[!INCLUDE [Prerequisites](includes/prerequisites.md)]

[!INCLUDE [Report setup and run query](includes/report-setup-run-query.md)]

1. In the Viva Insights analyst experience, select **Analysis**.

2. Under **Power BI templates**, navigate to **Meeting effectiveness** and select **Start analysis**. To get more information about the Meeting effectiveness template before running your analysis, select **Learn more**.

[!INCLUDE [Setup steps](includes/setup-steps.md)]

## Report settings

After the Meeting effectiveness report is set up and populated with Viva Insights data in Power BI:.

|Setting|Description|
|--------|----------|
|**Select the time period for the report**| This setting primarily alters the data displayed in the trend charts. Reducing the time period to less than eight weeks isn't recommended because some insights, like the month-over-month indicators, won’t have enough data to calculate.|
|**Aggregation period**|The aggregation period defines the span of time the report uses to calculate all aggregated insights. For example, if you select **Last 4 weeks**, insights will be aggregated over the four-week period leading up to the end date. Alternatively, if you select **Last 1 week**, insights be aggregated over the last week leading up to the end date.|
|**Average cost of an employee meeting hour**| Change this value to calculate a more accurate value for meeting hours across the report.|
|Optional filters to exclude employee groups| To filter the measured employee population, you can filter by any selected organizational attribute, and then filter by any of the values for these attributes. If you use these optional filters, the measured employees count will reflect a reduced number.|
|**View report by**|This attribute is the primary group-by attribute shown in all subsequent pages. You can change this attribute at any time; all subsequent report pages will show values grouped by the new attribute.|
|**Optional exclusions**| Use the check boxes to: <ul><li>Exclude employees who are likely non-knowledge workers (that is, those spending less than five hours per week on average in meetings, emails, and/or Teams calls and chats).<li>Exclude weeks that are likely holiday or paid-time-off weeks, or weeks that individuals are on other types of leave.|
|**Select the preferred language for your report**|Change the language for your report.|

>[!Note]
> Right now, the **Optional exclusions** listed above are not available if you choose to view the report in the browser. The **Optional exclusions** are only available if you download the Power BI template and open it in Power BI Desktop.

## About the report

The Meeting effectiveness report includes several report pages that help you find out whether your organization is practicing healthy meeting habits.

Except for the first two pages, each report page follows a similar format: an all-up group average for the metric, and then a breakdown of that metric average by the organizational attribute selected. These averages are calculated over the aggregation period you selected in [report settings](#report-settings). You can also see how the group average has trended from the selected **Start date** to **End date**, or select **Why this matters** for an explanation of the purpose behind the page. Finally, each page ends with a **Take action** suggestion, where you can elect **Explore more** to access additional details about suggested actions.

### Overview

Get a high-level overview of all insights included in the report: three insights that address meeting-hour quantity and six insights that address meeting-hour quality.

#### Meeting-hour-quality insights

All insights that show the quality of meeting hours—like large and long or short notice—are measured as a percent of all person meeting hours that have those traits. For example, let's say two people join a 30-minute meeting. One person joins on time and the other joins late. That meeting had 60 cumulative minutes of meeting time, but 30 of those minutes were joined late. So, 50% of meeting time was joined late.

#### Mover icons

The **Largest increase** icon calls out the insight that has increased the most in the aggregation period, relative to the previous period. This may be worth investigating based on the size of the increase. The **Largest decrease** icon calls out the insight that has decreased the most in the aggregation period—like meetings joined or ended late—relative to the previous period. This can be a cause for celebration.

#### Time-based comparisons

Based on the aggregation period selected, you’ll either see month-over-month comparisons or week-over-week comparisons by default. If you select **Last 4 weeks**, the report shows month-over-month calculations comparing the last four weeks to the four weeks before that. If you select **Last 1 week**, the report shows week-over-week calculations comparing the last one week to the week before that.

### Meeting lifecycle

View similar insights to the overview page, but based on the phases of the meeting lifecycle: before, during, and after.

When organizing effective meetings, it can help to think about the meeting in these three phases:

* **Before** the meeting, think about who the right attendees are, how much time you’ll need, who your required stakeholders are, whether they’re available, and more.

* **During** the meeting, make sure you get started on time, get through your agenda, and enable people to participate.

* **After** the meeting, evaluate it, ask for feedback, and send out notes and action items.

### Meeting hours

Sometimes it's shocking to learn just how much time your organization spends in meetings. Once you understand that investment, it’s easy to start asking questions about how to decrease the amount of non-productive meeting time. On this page, understand the value of time spent in meetings. If this value isn't worth tracking in your organization, you can always navigate to **Settings** and set that value to **0**.

### Large and long

Discover the percentage of meeting hours that are large (has nine or more invitees including the organizer) and long (over one hour). You can see how this data trends over time and the percent distribution of small and short, long, large, and large long meetings.

### Short notice

Learn about meetings that are being scheduled with short notice—that is, the percentage of meeting hours that organizers schedule fewer than 24 hours before that meeting is set to start.

### Conflicting

Understand the prevalence of overlapping meetings and how available attendees are. This page shows the percentage of meeting hours where an employee had overlapping meetings on their calendar.

### Joined late

View the percentage of meeting hours where employees joined a Teams meeting after five minutes past the scheduled start time.

### Ended late

View the percentage of meeting hours where employees ended a Teams meeting after one minute past the scheduled end time.

### Multitasked

Find out how multitasking affects your organization. You can see the percentage of meeting hours where a person was sending or reading emails or chats during a meeting. This page also provides categories of multitaskers based on the number of collaboration hours and multitasking tendencies.

### After meetings

Even after you leave a meeting room (whether physically or virtually), the meeting isn't done. Make sure you're always disseminating clear action items and next steps. Also, consider how the meeting went to make sure your next meeting is more effective than the last. Get a few helpful tips from this page to ensure this trend remains positive.

#### Glossary

View the metrics and other key terms used in the report. 

[!INCLUDE [Power BI tips and troubleshooting and Related topics](includes/powerbi-tips-related-topic.md)]