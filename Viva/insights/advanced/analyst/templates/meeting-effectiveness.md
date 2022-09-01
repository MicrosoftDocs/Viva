---
ROBOTS: NOINDEX,FOLLOW
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

The **Meeting effectiveness** uses a template populated by Viva Insights data to identify whether employees practice habits that lead to more effective meetings.

The report enables you to:

* Identify behaviors that improve meeting effectiveness.
* Determine which groups are and aren't practicing these behaviors.
* Learn how to drive the behaviors that enable more effective meetings.
* Track how these behavioral patterns change over time.

Each report page includes a **Why it matters** interpretation, **recommended actions**, and **metric definitions**.

To populate the report in Power BI, you’ll need to set up and successfully run the predefined **Meeting effectiveness** query in Viva Insights.

## Prerequisites

Before you can run the queries and populate the report in Power BI, you’ll need to:

* Be assigned the role of **Insights Analyst** in Viva Insights.
* Have the June 2022 (or newer) version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://powerbi.microsoft.com/en-us/getting-started-with-power-bi/) to download and install the latest version.

## Report setup

### Run query

>[!Note]
> For this release of Viva Insights, this report is currently only available in English and will only work with data generated from the English version of Viva Insights.

1. In the Viva Insights Analyst experience, select **Analysis**.

2. Under **Power BI templates**, navigate to **Meeting effectiveness** and select **Start analysis**. To get more information about the Meeting effectiveness template before running your analysis, select **Learn more**.

    ![Screenshot that shows the Meeting effectiveness icon in Viva Insights.](/viva/insights/advanced/images/me-pbi-icon2.png)

3. Under **Query setup**:
    1. Type a **Query name**.
    1. Select a **Time period**. **Time period** defaults to **Last 3 months**.
    >[!Important]
    > Some metrics in this query only have history back to May 2022. If you set the **Time period** to before May 2022, your query won't have complete data.
    3. Optional: You can set the query to automatically update by checking the **Auto-refresh** box. When you select the **Auto-refresh** option, your query automatically runs and computes a new result every time Viva Insights gets updated collaboration data for licensed people.

    >[!Note]
    >If the organizational data used in an auto-refreshing query changes (for example, an attribute name is altered or an attribute is removed), you might see an error when you run the query.

    4. Optional: Type a **Description**.
    
        Selecting **More settings** brings you to a pane, but there’s nothing you need to change there. In this pane:

        * Power BI queries are set to **Group by Week**. You can't edit this field.
        * The **Metric rules** field defaults to **Meeting exclusions rule (preferred rule)**. This field isn’t customizable in this release; for more information, refer to [Metric rules](../metric-rules.md).
![Screenshot that shows the Query setup screen.](/viva/insights/advanced/images/me-pbi-query-setup.png)

4. **In Predefined template metrics**, leave prepopulated metrics as they appear.  
![Screenshot that shows predefined metrics.](/viva/insights/advanced/images/me-pbi-query-metrics.png)

    >[!Note]
    > Metrics in Power BI templates can't be edited in this release of Viva Insights. To expand the full list of metrics included in the Power BI template, select the arrow in the box beneath **Metrics, filters, and organizational attributes**.

5. You can filter the employees in scope for the report under **Select which employees you want to include in the query**. Don’t remove the predefined “Is Active” filter. For more details about filter and metric options, see [Create a Custom Person query](../person-query.md).

    ![Screenshot that shows the Is active filter.](/viva/insights/advanced/images/pbi-templates-isactive-filter.png)

6. Under **Select which employee attributes you want to include in the query**, add up to seven organizational attributes. Once the query runs, you can use these attributes to group and filter the reports.

    >[!Important]
    >Some employee attributes are required to set up this Power BI template, which are preselected for you in the query. *Don't remove any preselected attributes.*
    >
    >If you see attributes marked in red and the query’s **Run** button disabled, it means that these required attributes are missing from your organizational data. Contact your admin to upload them.

7. Select **Run** on the upper right side of the screen, which can take a few minutes to complete.

8. When your query results are ready, go to the **Query results** page and select the **Power BI** icon to download the Power BI template and copy the query identifier. You'll need the query identifier later.

### Link report to query

9. Open the downloaded **Meeting effectiveness** template.

10. If prompted to select a program, select **Power BI**.

11. When prompted by Power BI:
    1. Paste in the query identifier.
    1. Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Viva Insights data.
        ![Screenshot that shows the minimum group size prompt in PowerBI.](/viva/insights/advanced/images/me-pbi-report-group-size.png)
    1. Select **Load** to import the query results into Power BI.

12. If prompted by Power BI, sign in using your organizational account. Power BI then loads and prepares the data, which can take a few minutes to complete for large files.

>[!Important]
> You need to sign in to Power BI with the same account you use to access Viva Insights.

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


![Screenshot that shows Report settings page in PowerBI.](/viva/insights/advanced/images/me-pbi-report-settings.png)

<!--

### Employees with low collaboration

By default, this report excludes employees who spend a weekly average of less than five hours in meetings, email, instant messages, and calls because they're likely non-knowledge workers or they don't use Outlook or Teams.

The report also excludes unusually low collaboration weeks based on individual collaboration patterns. These low-collaboration weeks usually occur when employees are taking time off from work.

If you want to include employees with low collaboration in your analysis, select the **Clear filter** (eraser) icon to clear the **IsLikelyKnowledgeWorker** and **IsLikelyHoliday** filters in the Power BI Filters pane.-->

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

## Power BI tips, FAQs, and troubleshooting

For details about how to share the report and other Power BI tips, troubleshoot any issues, or review the FAQ, see [Power BI tips, FAQ, and troubleshooting](../templates/power-bi-faq-troubleshoot.md).

## Related topic

[Access query results and modify existing queries](../query-results.md)
