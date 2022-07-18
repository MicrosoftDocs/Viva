---
ROBOTS: NOINDEX,FOLLOW
title: Metric rules in Viva Insights
description: Learn about metric rules in Microsoft Viva Insights 
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
manager: anirudh-bajaj
audience: Admin
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
---

# Advanced insights metric rules

Microsoft Viva Insights uses email and calendar activities stored in a person's Microsoft 365 account to reveal internal and external collaboration trends. However, a person's calendar and email can contain a diverse set of activities (for example, personal meetings, work-related social activities, and all-day training meetings) that aren't relevant to work-related collaboration. If those activities were included in the metrics, they'd skew query results.

When you use the available analysis tools—like for templates and queries—Viva Insights excludes events from analysis that might skew query results based on the default **Meeting exclusions** rule. You can see what kind of data this rule excludes on the **Metric rules** page within the advanced insights app.

## View rule details

The default **Meeting exclusions rule** filters the meeting data for analysis purposes. You can view rule details on the **Metric rules** page, which you can get to in two ways:

1. Through the side menu:
    1. In the advanced insights app analyst experience, select  **Analysis > Metric rules**.
    1. Select **View details**, and then you can expand the sections listed on this page, such as **Rule exceptions**.
1. When building a query:
    1. Under **Query setup**, select the **More settings** button, which opens a pane on the left side of the screen.
    1. Select **See metric rule details**.

To see an example .xlsx file that shows what's included and excluded from existing collaboration data, you can select **Download sample results**.

## About metric rules

The app's metric rules:

* Only apply to analysis data – Metric rules only apply and filter data in the **Analysis** pages and for the data shown within the Viva Insights app in Teams for managers and leader insights.
* Are read-only – These rules are set up automatically by default. For the first release of the new advanced insights app, you can't edit or change these metric rules, but you'll be able to in the future.
* Exclude certain meeting types from collaboration metrics – The default **Meeting exclusions** rule excludes the time and count metrics for meetings that match the following criteria:
    * If the duration of the meeting is 24 hours or more.
    * If the meeting is canceled.
    * If the user is not the meeting organizer, and if their response to a meeting invite is anything other than "Accept."
    * If there are less than two participants.
    * If the event is set to show as anything other than "Busy" on participant's calendars.

![Meeting attendance rule](/viva/insights/advanced/images/metric-rules.png)

### Rule exceptions

 The **Are there exceptions to this rule?** section lists metrics that the **Meeting exclusions** rule doesn't apply to because they're not collaboration metrics, which are the following:

* **Available-to-focus hours**
* **Conflicting meeting hours**
* **Working-hours meeting hours**
