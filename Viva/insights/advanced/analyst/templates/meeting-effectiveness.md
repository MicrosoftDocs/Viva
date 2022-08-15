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

The **Meeting effectiveness report** uses a template populated by Viva Insights data to identify whether employees practice habits that lead to more effective meetings.

The report enables you to visualize and explore the following top-level business questions asked by leaders:

* 

Each report page includes a **Why this matters** interpretation, **recommended actions**, and **metric definitions**.

To populate the report in Power BI, you’ll need to set up and successfully run the predefined **Meeting effectiveness** query in Viva Insights.

## Demonstration

The following demonstration uses sample data that’s only representative of this report and might not be exactly what you see in a live report specific to your organization's unique data.

<iframe title="Business resilience - Summary" width="600" height="373.5" src="https://msit.powerbi.com/view?r=eyJrIjoiY2RmYWY4YmYtMTdhZC00MTZkLWEwZmMtMDA5ZTczNTIyODI5IiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9" frameborder="0" allowFullScreen="true"></iframe>

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

    ![Set up the report page in Power BI](/viva/insights/advanced/images/br-pbi-start.png)

3. Under **Query setup**:
    1. Type a **Query name**.
    1. Select a **Time period**. **Time period** defaults to **Last 3 months**.
    >[!Important]
    > Some metrics in this query only have history back to May 2022. Setting the Time period to before May 2022 will result in incomplete data.
    1. Optional: You can set the query to automatically update by checking the **Auto-refresh** box. When you select the **Auto-refresh** option, your query automatically runs and computes a new result every time Viva Insights gets updated collaboration data for licensed people.

    >[!Note]
    >If the organizational data used in an auto-refreshing query changes (for example, an attribute name is altered or an attribute is removed), you might see an error when you run the query.

    4. Optional: Type a **Description**.
    
        Selecting **More settings** brings you to a pane, but there’s nothing you need to change there. In this pane:

        * Power BI queries are set to **Group by Week**. You can't edit this field.
        * The **Metric rules** field defaults to **Meeting exclusions rule (preferred rule)**. This field isn’t customizable in this release; for more information, refer to [Metric rules](../metric-rules.md).
![Set up the report page in Power BI](/viva/insights/advanced/images/br-pbi-query-setup.png)

4. **In Predefined template metrics**, leave prepopulated metrics as they appear.  
![Set up the report page in Power BI](/viva/insights/advanced/images/br-pbi-predefined-metrics.png)

    >[!Note]
    > Metrics in Power BI templates can't be edited in this release of Viva Insights. To expand the full list of metrics included in the Power BI template, select the arrow in the box beneath **Metrics, filters, and organizational attributes**.

5. You can filter the employees in scope for the report under **Select which employees you want to include in the query**. Don’t remove the predefined “Is Active” filter. For more details about filter and metric options, see [Create a Custom Person query](../person-query.md).

    ![Is active filter](/viva/insights/advanced/images/pbi-templates-isactive-filter.png)

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
    1. Select **Load** to import the query results into Power BI.

12. If prompted by Power BI, sign in using your organizational account. Power BI then loads and prepares the data, which can take a few minutes to complete for large files.

>[!Important]
> You need to sign in to Power BI with the same account you use to access Viva Insights.

## Report settings

After the Meeting effectiveness report is set up and populated with Viva Insights data in Power BI:

1. Select the report's time period. This setting primarily alters the data displayed in the trend charts. Reducing the time period to less than eight weeks isn't recommended because some insights, like the month-over-month indicators, won’t have enough data to calculate.
1. Select the report's aggregation period. The aggregation period defines the amount of time that all aggregated insights are computed over. For example, if you select **Last 4 weeks**, then the report includes the last four weeks leading up to the end date when it computes insights. If you select **Last 1 week**, the report only includes the last week leading up to the end date when it computes insights.
1. Select the average cost of an employee meeting hour. Change this value to calculate a more accurate value for meeting hours across the report.
1. Select an organizational attribute to view the report by. This attribute is the primary group-by attribute shown in all subsequent pages. You can change this attribute at any time; all subsequent report pages will show values grouped by the new attribute.
1. Select optional filters to exclude employee groups. To filter the measured employee population, you can filter by any selected Organizational attribute, and then filter by any of the values for these attributes. If you use these optional filters, the measured employees count will reflect a reduced number.
1. Set exclusions. Use the check boxes to:
    * Exclude employees who are likely non-knowledge workers (that is, those spending less than five hours per week on average in meetings, emails, and/or Teams calls and chats).
    * Exclude weeks that are likely holiday or paid-time-off weeks, or weeks that individuals are on other types of leave.

After confirming these settings, check the number of measured employees to make sure it's the population you want to analyze.

<!--screenshot-->

<!-- Q for Andrew: If we automatically exclude non-knowledge workers and low collab weeks, can we remove step 6 above?-->

### Employees with low collaboration

By default, this report excludes employees who spend a weekly average of less than five hours in meetings, email, instant messages, and calls because they're likely non-knowledge workers or they don't use Outlook or Teams.

The report also excludes unusually low collaboration weeks based on individual collaboration patterns. These low-collaboration weeks usually occur when employees are taking time off from work.

If you want to include employees with low collaboration in your analysis, select the **Clear filter** (eraser) icon to clear the **IsLikelyKnowledgeWorker** and **IsLikelyHoliday** filters in the Power BI Filters pane.

## About the report

The Meeting effectiveness report includes the following report pages that help you … <>

### Overview

This page shows a high-level overview of all insights included in the report: three insights address the quantity of meeting hours and six insights comment on the quality of the meeting hours.

<!--phrasing-->

All insights that show the quality of meeting hours, like **Short and small** or **Advanced meeting notice**, are measured as a percent of all person meeting hours that have those traits. <!--phrasing-->

For example, let's say two people join a 30-minute meeting. One person joins on time and the other joins late. That meeting had 60 cumulative minutes of meeting time, but only 30 of those minutes were joined on time. So, 50% of meeting time was joined on time.

The **Top mover** icon calls out the insight that had the greatest change, while the **Bottom mover** icon calls out the insight with the least change.

Finally, based on the aggregation period selected, you’ll either see month-over-month comparisons or week-over-week comparisons by default. If you select **Last 4 weeks**, the report shows month-over-month calculations comparing the last four weeks to the four weeks before that. If you select **Last 1 week**, the report shows week-over-week calculations comparing the last one week to week before that.

### Meeting lifecycle

This page shows similar insights to the overview page, but displays them based on the phases of the meeting lifecycle: **before**, **during**, and **after**.

When organizing meetings and trying to ensure the time is spent effectively, it can help to think about the meeting broken down into these three phases. Before the meeting, you want to think about who the right attendees are, how much time you’ll need, who your required stakeholders are and whether they’re available, and more. During the meeting, you’ll want to ensure you get started on time, get through your agenda, and engage the participation. After the meeting, you'll want to evaluate it, ask for feedback, and send out notes and action items.

### Meeting hours

Sometimes it can be shocking to learn just how much time your organization spends in meetings. Once you understand that investment, it’s easy to start asking questions about how to decrease the amount of non-productive meeting time.

To learn more about **Why it matters**, click on the icon next the title of the page.

<!--question for Andrew: "all remaining report pages..." How many are there? Could we list them out to be explicit? Are these the bulleted list below?-->

This format of this page reflects how all remaining report pages look: an all-up group average for the metric, and then a breakdown of that metric average by the organizational attribute selected. These averages are calculated over the aggregation period you selected in [report settings](#report-settings).You can also see how the group average has trended from the selected **Start date** to **End date**.

On this page in particular, you can see the value of time spent in meetings. If this is something not worth tracking for your organization, you can always go into Settings and set that value to zero.

Finally, each page ends with a **Take action** suggestion. Click on the **Explore more** to access relevant links and next steps.

From there, you can explore the following pages and learn about the various insights, why the matter, and how to take action.

* Short and small
* Advanced meeting notice
* Attendee availability
* Joined on time
* Ended on time
* No multitasking

### After meetings

Even after you leave a meeting room (physically, or virtually), the meeting isn’t done. Ensure that you are always disseminating clear action items and next steps. Also consider how the meeting went to make sure your next meeting is more effective than the last. This page provides a few helpful tips to ensure this trend remains positive.

#### Glossary

This page defines the metrics and other key terms used in the report 

## Power BI tips, FAQs, and troubleshooting

For details about how to share the report and other Power BI tips, troubleshoot any issues, or review the FAQ, see [Power BI tips, FAQ, and troubleshooting](../templates/power-bi-faq-troubleshoot.md).

## Related topic

[Access query results and modify existing queries](../query-results.md)
