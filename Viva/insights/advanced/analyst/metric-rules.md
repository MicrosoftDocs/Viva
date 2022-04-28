---
ROBOTS: NOINDEX,FOLLOW
title: Advanced insights metric rules
description: Describes what metrics rules are and how to use them for analysis data in Microsoft Viva Insights, including for queries and templates in the Advanced insights app
author: madehmer
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
manager: helayne
audience: Admin
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 

---

# Advanced insights metric rules

Microsoft Viva Insights uses email and calendar activities that are stored in a person's Microsoft 365 account to reveal internal and external collaboration trends. However, a person's calendar and email can contain a diverse set of activities (such as personal meetings, work-related social activities, all-day training meetings, and so forth) that are not relevant to work-related collaboration, and, if included in the metrics, would skew query results.

As a Viva Insights Analyst, you can view the **Metric rules** page within the Advanced insights app. Metric rules show what type of data is being excluded when using the available analysis tools, such as for templates and queries.

Viva Insights excludes events from analysis based on the default **Meeting attendance rule**. This rule is set by default to exclude meetings from analysis (such as all-day training meetings) where their inclusion might skew query results.

![Metric rules page](../../Images/advanced/metric-rules.png)
<!--customized is misspelled in the image, please replace when the UX is fixed-->

## View rule details

The default meeting attendance rule filters the meeting data for analysis purposes. To view rule details, do the following.

1. In the Advanced insights app, select **Analyst** > **Metric rules**.<!--add a link to the app when available?-->
1. Select **View details**, and then you can expand the sections listed on this page, such as **Rule exceptions**.

   ![Metric rule details page](../../Images/advanced/metric-rule-details.png)
   <!--add a better image, this one has typos-->

1. Optionally, you can select **Download sample results** to see an example .csv file that shows what's included and excluded from existing collaboration data.

## About the rules

* **Only apply to analysis data** - Metric rules only apply and filter data in the **Analyst** pages and for the data shown within the Viva Insights app in Teams for managers and leader insights. These rules are _not_ applied to the data shown in the **Data quality** pages, such as for Microsoft 365 data.
* **Are read-only** - These rules are set up automatically by default. For the first release of the new Advanced insights app, you cannot yet edit or change these metric rules.
* **Meetings excluded from collaboration metrics** - The default **Meeting attendance rule** excludes the time and count metrics for meetings that match the following criteria:

  * If duration of meeting is greater than or equal to 24 hours.
  * If the meeting is cancelled.
  * If the response to the meeting is anything except "Accepted" or the organizer is the user.
  * If the participant meeting count is less than or equal to 1.
  * If "Show as" is set to anything except "Busy."

* **Rule exceptions** - The section lists metrics that the **Meeting attendance rule** does not apply to because they're not counted as collaboration metrics, such as **Conflicting meeting hours**.
