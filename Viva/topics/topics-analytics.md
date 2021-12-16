---
title: Analytics for Microsoft Viva Topics
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
ms.reviewer: cjtan
audience: admin
ms.topic: article
ms.service: o365-administration
search.appverid: MET150
ms.localizationpriority: medium
description: Learn about analytics for Microsoft Viva Topics.
---

# Security and privacy in Microsoft Viva Topics

Insights are available for Viva Topics in the Microsoft 365 admin center. You need to be a SharePoint admin and a Groups admin to see these reports.

To access Viva Topics insights
1. In the Microsoft 365 amdin center, expand **Settings** and select **Search & intelligence**.
1. On the **Insights** tab, select **Viva Topics**.

## Topics overview

The **Topics overview** section provides a look at topic visibility in your organization.

The changes from the last time period appear next to each metric. If the time period selected is larger than when data was first available, the delta is collected from a starting point of 0.

![Screenshot of analytics for topics visible.](../media/topics-analytics-topics-visible.png) 

|Measure|Value|
|:------|:----|
|Topics visible|The number of topics that are visible to topic viewers.|
|Discovered by Viva Topics|The number of topics that have been [discovered by Topics](/topics/topic-experiences-discovery-curation) or have AI-discovered properties.|
|Created by users|The number of topics that have been [manually created](/viva/topics/create-a-topic)|
|Hidden by settings|If you have [configured Topics to not show suggested topics to topic viewers](/topics/topic-experiences-discovery#prevent-topic-viewers-from-seeing-suggested-topics), the number of hidden topics will be reflected here|
|Removed|The number of topics that have been [removed by user feedback and knowledge managers](/viva/topics/manage-topics)|

## File processing for topic discovery

The **File processing for topic discovery** section shows the number of files that have been processed as Topics crawls the [content sources that you selected](/viva/topics/topic-experiences-discovery).

|Measure|Value|
|:------|:----|
|Unique files processed|The number of files that have been processed for topic discovery|

![Screenshot of analytics for unique files processed.](../media/topics-analytics-unique-files.png) 

## See also

[Plan topic experiences](plan-topic-experiences.md)

[Set up topic experiences](set-up-topic-experiences.md)
