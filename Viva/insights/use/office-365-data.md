---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 12/16/2019
title: Viva Insights Microsoft 365 data
description: What's available on the Microsoft 365 data sources page in the advanced insights app with Microsoft Viva Insights
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Microsoft 365 data

>[!Important]
>Advanced insights in Viva Insights doesn't currently support mailboxes in [Sweden go-local](/microsoft-365/enterprise/o365-data-locations#sweden). To get updated data for advanced insights, you cannot have [licenses assigned](../setup/Assign-licenses-to-population.md) to users with mailboxes in Sweden go-local.

As an admin or an analyst, you can use this page to confirm that your Microsoft 365 data is up-to-date. Use this page to look for date ranges that have unexpected gaps in activity, inconsistent or degraded data, or activity levels that are higher or lower than what might be considered normal for your organization.

![Data sources.](../images/WpA/Use/m365data.png)

**Microsoft 365 data** includes the following:

* **Measured employees** - The employees to whom your Viva Insights admin assigned licenses during setup. After license assignments, the advanced insights app extracts Microsoft 365 data about meetings, email, unscheduled calls, and instant messages for these people. When the data extraction process is successful for these employees, they are included in your measured population. If extraction errors occur and Viva Insights didn't get data for a person, that person is licensed but not counted as a measured employee in Viva Insights. If you are an analyst or limited analyst, this is the population that you can analyze within Viva Insights. The number of measured employees can help determine whether you have good data coverage for analysis.

  >[!Note]
  > Your admin can assign employees Viva Insights licenses as a group with Azure Active Directory (Azure AD). If this number seems inaccurate, confirm with your admin that only active employees are assigned licenses through Azure AD. For more details, see [Assign licenses](/viva/insights/setup/assign-licenses-to-population?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

* **Internal collaborators** - These are unmeasured employees who were included in extractions of Microsoft 365 data with whom the _measured_ employees collaborated. These people are not part of your measured population but are internal to your organization. Internal collaborators can include employees from other groups, vendors, or contractors that are working with your team and are included in the same internal domain as your team, but are not in your measured population.

* **External collaborators** - These are people outside of your company or external to your email domain with whom your measured employees collaborated. For more information about external collaboration, see [External collaboration](/viva/insights/use/explore-metrics-external-collaboration?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

* **Average weekly collaboration chart** - This chart shows the last refreshed on weekly collaboration hours for measured employees by type, which can include hours spent on email, in meetings, in unscheduled calls, and on instant messages. The Last refreshed date shows when Office 365 Exchange and Teams data was most recently processed for this chart.

Hover your cursor over the chart data to get more details and use the chart legend to change what data (meetings, email, instant messages, and calls) the chart shows.

  ![Microsoft 365 data sources chart data.](../images/wpa/use/measured-collab.png)
<!--
  >[!Note]
  > If collaboration activity for Teams drops below 30 percent of the total collaboration, the unscheduled calls and instant message data will not show due to insufficient data.
-->

## Origin of data counts

In **Sources** > **Microsoft 365 data**, you can see the current count of three categories of data. Most of this data originates with people in your organization, who might or might not have Viva Insights licenses. However, some data originates outside of your organization or comes from mailboxes of other types.

Determining the origins of data also determines how to categorize it, as shown in the following flow chart.

  ![Origin of data counts.](../images/wpa/use/data-sources-final.png)

The following shows where each appears in **Microsoft 365 data**.

  ![Microsoft 365 data sources page info.](../images/wpa/use/data-sources-relate.png)

## Possible causes of inconsistent data

The following are examples of where you might encounter instances of inconsistency in the volume of email, meetings, calls, and instant messages data.

* **Major holidays** - Drops in email and meeting activity around major holidays are typical and can potentially impact analysis. You can remove these weeks from your outputs to reduce its impact.

* **Email archive policies** - Business policies can impact historical data processed during initial setup. As you view historical data, if you see a steady decline or point-in-time drop-off in email and/or meeting activity, it might be due to archiving. By using the Average weekly collaboration chart (see the preceding illustration), you can select a date range to analyze your collaboration data where the mail volume is stable.

* **Recurring meetings** - When a recurring meeting series is removed from a calendar, all past instances of this meeting are removed. As you view historical data, if you see a steady decline in meeting activity, it might be due to recurring meetings having been removed from calendars. By using the Average weekly collaboration chart (see the preceding illustration), you  can select a date range to analyze your collaboration data where the meeting volume is stable.

## Related topics

* [Organizational data](/viva/insights/use/organizational-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)
* [CRM data](/viva/insights/use/crm-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)
* [Prepare organizational data](/viva/insights/setup/prepare-organizational-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)

