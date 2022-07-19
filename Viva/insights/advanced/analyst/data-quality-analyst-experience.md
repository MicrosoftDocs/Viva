---
ROBOTS: NOINDEX,FOLLOW
title: Data quality in the analyst experience
description: Learn about organizational data in the Analyst experience of the Microsoft Viva Insights advanced insights app.
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
manager: anirudhbajaj
audience: Admin
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 

---

# Data quality in the analyst experience

Admins are responsible for uploading organizational data. However, you as an analyst might want, or be prompted, to check the quality of uploaded data. This article discusses what low-quality and missing data is, and how to identify it.

## Data types

### Missing data

Missing data means that certain employee attributes haven’t been included in the organizational data your admin uploaded. Because employee attributes are tied to insights, missing attributes lead to missing insights.

### Low-quality data

#### Coverage

Coverage describes the number of non-blank rows in an organizational data file. In organizational data files, each column contains attribute values—for example, the image below represents an Organization attribute; its values are the locations in each row. 

If a column has no blank rows, that attribute has high coverage. If a column has too many blank rows, that attribute has low coverage. Attributes with low coverage are considered low-quality data. Similar to missing insights, when data is of low quality, related insights are of low quality, too.
 
To see the quality of uploaded data, you can directly access the **Organizational data** page through the app’s left pane. If there’s a problem with the data used in a query you’ve run or are about to run, warning messages might take you to the **Organizational data** page, as explained below.

## Checking data quality and contacting admins

To check on the quality of your data, and to see which insights are missing or of low quality, go to the **Organizational data** page. To increase data quality, you might need attributes or other data uploaded by your admin.

### Organizational data page

You can get to the **Organizational data** page in two ways: Either by directly selecting it from the app’s left pane, or by selecting **View data quality** within a banner message (described later in this article).

The **Organizational data** page contains two tabs: **Data hub** and **Data quality**.

#### Data hub

The **Data hub** tab shows the number of:

* Missing or low-quality insights
* Available insights
* Missing or low-quality data fields
* Days since the data was last refreshed

It also shows, as a donut chart, the percentage of insights displayed based on the total number of possible insights. When more organizational data is added, more insights become available and this percentage increases.

Beneath the summary is a list of missing insights and missing data fields. You can select a missing insight to see its related data fields, and vice versa.

A blurb describes how to improve data quality.

The **Data quality** tab provides attribute-specific information, including **Quality score**.

### Contacting your admin 

To address data-quality errors and warnings, you might need to have your admin re-upload organizational data. 

The **Contact admin** page, which is under construction right now, will provide a list of your organization’s admins and their contact information, and also provide a button to directly send them an email.
 
