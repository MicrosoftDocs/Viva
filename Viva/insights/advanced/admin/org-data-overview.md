---
title: Organizational data overview
description: This article gives an overview of the Organizational data page in the Microsoft Viva Insights advanced insights app. 
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Organizational data in Viva Insights

Organizational data is information about your company provided to the advanced insights app. As an admin, you can use the **Organizational data** page to both upload data and to understand the quality of previously uploaded or refreshed data.

>[!Note]
>The app can receive data in one of two ways: from the Azure Active Directory—which is the default source—or through a .csv file that an admin uploads. You can view the current active data source on the **Data hub** tab.

The **Organizational data** page includes **Data hub**, **Data connections**, and **Data quality** tabs.

## Data hub

The **Data hub** tab is the first tab you see when you select the **Organizational data** page, and it includes the following information:

### Data quality

This section shows the number of:

* Missing and low-quality data fields
* Available insights
* Missing insights
* Days since the data was last refreshed

It also shows, as a donut chart, the percentage of insights displayed based on the total number of possible insights. By adding more organizational data, more insights become available and this percentage increases.

## Missing or low-quality organizational data

This section shows the names of the missing insights and missing data fields summarized above. To find out more about a missing insight, select its name from the **Missing or low-quality insights** column. The **Missing or low-quality data fields** column then highlights which data fields are associated with the selected insight—that is, which data fields you should include in your upload. A **Description** column provides details about the metric you selected. 
 
## Current active data source

Based on how you’re uploading organizational data, this section shows either **Azure Active Directory** or **.csv upload.**

### Changing the active data source

If you want to manually upload organizational data using a .csv file, instead of using the default Azure Active Directory data source, navigate to **.csv upload** beneath **Other available data sources**. Then select the **Start** button to begin a manual upload.

>[!Important]
>Once you upload organizational data in a .csv file, the Azure Active Directory is no longer available as a data source.

## Data connections

In the **Data connections** tab, you can:

* Start new imports.
* Edit existing imports.
* View imports in progress.
* View import history.

Learn how to upload organizational data and view import results in [Upload organizational data (first upload)](./upload-org-data-first.md)

## Data quality

The **Data quality** tab includes the following elements:

* **Data fields** – These are all the attributes provided by your organization in the organizational data upload file. When you create queries, you can filter and group employees in the organization by these data fields, so being familiar with them will give you insight into the types of queries to use for analysis.
* **Quality score** – The percentage of measured employees who have a non-blank value for the specified data field. This score is intended as guidance, not to be an absolute measure of quality. A quality score of more than 95% leads to better quality insights. If quality scores are low, it'll be difficult to determine how people collaborate across different characteristics. Additionally, low quality scores on required data fields may give skewed (under-reported) metric calculations for metrics that rely on those attributes.
* **Employees with this field** – The number of measured employees and internal collaborators with a non-blank value for the data field.
* **Unique values** – The count of the unique attribute values included in the data. For example, if a **Region** data field contains North, South, Central, East, West and Southwest, its unique values count is six.

## Related topic

* [Prepare organizational data](prepare-org-data.md)