---
ms.date: 07/14/2022
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

In this article, we discuss the value of organizational data for analysts, distinguish the two types of organizational data that the advanced insights app can use, and briefly describe the **Organizational data** page in the app's admin experience.

## About organizational data

Organizational data is descriptive information about employees. The advanced insights app combines organizational data with Microsoft 365 data to provide detailed, actionable insights into the company's communication and collaboration trends. Depending on the organizational data available, an analyst can uncover these trends and use them to make more effective business decisions.

Here's an example: an analyst might use organizational data to learn how people communicate across job functions, department groups, and management hierarchies by enabling the grouping and filtering of descriptive attributes.

Advanced insights automatically collects collaboration data from Microsoft 365. Analyzing just this data would create an incomplete picture; it’s organizational data that provides analysis context.

## About data sources

The advanced insights app can get organizational data in one of two ways: through Azure Active Directory, which is the default setting, or through an organizational data file that you as an admin upload. Azure Active Directory automatically syncs with the advanced insights app and provides data for these attributes:

* **PersonId**
* **ManagerId**
* **Organization**

In your imported data, you'll also notice:

* **Domain**, which Viva Insights gets from users' primary SMTP addresses.
* **TimeZone**, which Viva Insights gets from users' Outlook/Exchange settings.

If you want to include more attributes, for example, those we discuss in [Prepare organizational data](prepare-org-data.md#attribute-reference), then you'd want to choose a data file as your source.

>[!Important]
> After you upload a .csv file with organizational data, you won't be able to switch back to using Azure Active Directory. You'll need to regularly upload .csv files to keep your organizational data current.

### To prepare a .csv data file

To learn how to set up and structure an organizational data .csv file, refer to [Prepare organizational data](prepare-org-data.md).

## Organizational data in the advanced insights app

The **Organizational data** page includes **Data hub**, **Data connections**, and **Data quality** tabs.

## Data hub

The **Data hub** tab is the first tab you see when you select the **Organizational data** page, and it includes the following information:

### Data quality

This section shows the number of:

* Missing and low-quality data fields.
* Available insights.
* Missing insights.
* Days since the data was last refreshed.

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

* **Data fields** – All the attributes provided by your organization in the organizational data upload file. When you create queries, you can filter and group employees in the organization by these data fields, so being familiar with them will give you insight into the types of queries to use for analysis.
* **Quality score** – The percentage of measured employees who have a non-blank value for the specified data field. This score is intended as guidance, not to be an absolute measure of quality. A quality score of more than 95% leads to better-quality insights. If quality scores are low, it'll be difficult to determine how people collaborate across different characteristics. Additionally, low quality scores on required data fields may give skewed (under-reported) metric calculations for metrics that rely on those attributes.
* **Employees with this field** – The number of measured employees and internal collaborators with a non-blank value for the data field.
* **Unique values** – The count of the unique attribute values included in the data. For example, if a **Region** data field contains North, South, Central, East, West and Southwest, its unique values count is six.

## Related topic

[Prepare organizational data](prepare-org-data.md)
