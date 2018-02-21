---
# Metadata Sample
# required metadata

title: Workplace Analytics Data Sources
description: placeholder text -- placceholder text This is a Checklist to introduce what is required to implement Workplace Analytics for your Organization
author: rodonahu
ms.author: rodonahu
ms.date: 1/19/2018
ms.topic: get-started-article
ms.prod: wpa
---
# Data sources

Data sources contains high-level dashboard views that Workplace Analytics administrators and data analysts can use to verify that Office 365 and organizational data is loaded and ready to use.

![Data sources](../images/WpA/Use/Data-sources.png)

### To view the Data sources metrics

* On the navigation bar, click **Sources**.

The Data sources page consists of three sections:

* **Data sources summary** is an overview of the source mailboxes and collaborators that make up the data set.
* **Office 365 data summary** shows the overall trend of email and meeting hours and volume in the data set.
* **Organizational data summary** provides information about the Organizational Attributes that are in the data set.

Using Data sources metrics, Workplace Analytics administrators and data analysts can:

* Get a high-level view of the data that is available for analysis.
* Verify that the organizational data they need for their specific analysis are available, and work with internal suppliers of the data (HR information system administrators, line of business (LOB) system administrators, or data analysts) to verify the necessary data has been loaded as expected.
* Verify that the data is of sufficient quality to analyze the business problem.

## Data sources summary
The Data sources summary provides the following information about your data:

* The number of **measured employees** for which Workplace Analytics gathers meeting and email data. These are the people that can be the subject of your analysis. (This should be equal to the number of Workplace Analytics licenses that you assigned during provisioning.) This number can help determine whether you have a good representation of the organization.

* The number of people not part of your measured population (both internal and external) with whom the measured employees collaborated.

* The date range of the Office 365 data. Use this range to verify if you have data for the period you want to analyze.

* The organizational data coverage for measured employees and other internal collaborators. This can tell you if you have loaded enough attributes about your population to allow accurate filtering and grouping of data, and for all metrics to be computed correctly. 

For more information about what data is needed to compute metrics, see these topics:

[Prepare and upload organizational data](../use/Prepare-and-upload-organizational-data.md)

[Metric definitions](../Use/Metric-definitions.md)

[Glossary](../Use/Glossary.md)

## Office 365 data summary
Office 365 data summary provides a view that you can use to evaluate meeting and email collaboration data levels over a given time period. It provides a view of average weekly meeting and mail hours, sent mails, and meetings attended over time. The Last refreshed date shows when data was most recently processed.

Analysts can use these views to look for time periods that have unexpected gaps in activity, inconsistent or degraded data, or activity levels that are higher or lower than what might be considered normal for your organization.

These are some examples of scenarios where you might encounter inconsistency in email or meeting volume: 

* **Major holidays**: It is typical to see drops in email and meeting activity around major holidays, which could potentially impact analysis. You can remove these weeks from your outputs if desired.

* **Email archive policies**: Business policies can impact historical data processed during initial setup. As you view historical data, if you see a steady decline or point-in-time drop-off in email and/or meeting activity, it may be due to archiving. Using this view, you can select a time period where the mail volume is stable.

* **Recurring meetings**: When a recurring meeting series is removed from a calendar, all past instances of this meeting are removed. As you view historical data, if you see a steady decline in meeting activity, it may be due to recurring meetings having been removed from calendars.

## Organizational data summary

Organizational data summary provides details about the attributes that have been supplied, as well as the population coverage for each of the attributes (coverage is defined as the percentage of measured employees who have a value specified for the given attribute). The **Last refreshed** date shows when data was last processed.

### Values
This is a list of the attributes supplied by your organization. When you [create queries](../Use/Create-queries.md), you can filter and group employees in the organization by using the attributes, so being familiar with these attributes will help give insight into the types of queries you may want to create for analysis.

### Measured employees
This is the number of measured employees who had a value for the attribute.

### Coverage
This is the percentage of measured employees who have a value specified for the given attribute. If coverage levels are low, it will be difficult to determine how people collaborate across different characteristics. Additionally, low coverage on required attributes may give skewed (under reported) metric calculations for metrics that rely on those attributes.

### Unique values
This is the count of the unique attribute values included in the data. For example, if the attribute Region contains North, South, Central, East, West and Southwest, it’s unique values count is 6.