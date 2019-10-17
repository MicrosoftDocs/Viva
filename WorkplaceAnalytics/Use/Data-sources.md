---
# Metadata Sample
# required metadata

title: Workplace Analytics Data sources
description: An overview of Data sources in Workplace Analytics 
author: madehmer
ms.author: v-midehm
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Data sources

**Data sources** contains high-level dashboard views that Workplace Analytics administrators and data analysts can use to verify that Office 365 and organizational data is loaded and ready to use.

![Data sources](../images/WpA/Use/data-sources.png)

[!INCLUDE [To open the Workplace Analytics Sources page](../includes/to-open-wpa-sources.md)]

The Data sources page consists of the following sections:

* **Data sources summary** is an overview of the source mailboxes and collaborators that make up the data set.
* **Office 365 data summary** shows the overall trend of email and meeting hours and volume in the data set.
* **Organizational data summary** provides information about the Organizational Attributes that are in the data set.

Using Data sources metrics, Workplace Analytics administrators and data analysts can:

* Get a high-level view of the data that is available for analysis.
* Verify that the organizational data they need for their specific analysis is available, and work with internal suppliers of the data (HR information system administrators, line of business [LOB] system administrators, and data analysts) to verify the necessary data has been loaded as expected.
* Verify that the data is of sufficient quality to analyze the business problem.

## Data sources summary

The Data sources summary provides the following information about your data:

* The number of **measured employees** for whom your Workplace Analytics administrator assigned licenses during setup. After license assignments, Workplace Analytics extracts Office 365 data about meetings, email, unscheduled calls, and instant messages for these people. When the data extraction process is successful for these employees, they are included in your measured population. If extraction errors occur and Workplace Analytics didn't get data for a person, that person is licensed but not counted as a measured employee in Workplace Analytics. If you are an analyst or limited analyst, this is the population that you can analyze within Workplace Analytics. The number of measured employees can help determine whether you have good data coverage for analysis.

* The number of people not part of your measured population (both internal and external) with whom the measured employees collaborated.

* The date range of the Office 365 data. Use this range to verify if you have data for the period you want to analyze.

* The organizational data coverage for measured employees and other internal collaborators. This can tell you if you have loaded enough attributes about your population to allow accurate filtering and grouping of data, and for all metrics to be computed correctly.

![Data sources summary](../images/wpa/Use/Data-sources-summary.png)

For more information about what data is needed to compute metrics, see these topics:

* [Prepare organizational data](../setup/Prepare-organizational-data.md)

* [Metric definitions](../Use/Metric-definitions.md)

* [Glossary](../Use/Glossary.md)

## Office 365 data summary

Office 365 data summary provides a view that you can use to evaluate meeting and email collaboration data levels over a given time period. It provides a view of average weekly meeting and email hours, sent emails, and meetings attended over time. The Last refreshed date shows when data was most recently processed.

Analysts can use these views to look for time periods that have unexpected gaps in activity, inconsistent or degraded data, or activity levels that are higher or lower than what might be considered normal for your organization.

![Data sources summary](../images/wpa/Use/o365-data.png)

The following are examples of where you might encounter inconsistency in email or meeting volume.

* **Major holidays**: Drops in email and meeting activity around major holidays is typical and can potentially impact analysis. You can remove these weeks from your outputs to reduce its impact.

* **Email archive policies**: Business policies can impact historical data processed during initial setup. As you view historical data, if you see a steady decline or point-in-time drop-off in email and/or meeting activity, it may be due to archiving. Using this view, you can select a time period where the mail volume is stable.

* **Recurring meetings**: When a recurring meeting series is removed from a calendar, all past instances of this meeting are removed. As you view historical data, if you see a steady decline in meeting activity, it may be due to recurring meetings having been removed from calendars.

## Organizational data summary

Organizational data summary provides details about the attributes that have been supplied, as well as the population coverage for each of the attributes (coverage is defined as the percentage of measured employees who have a value specified for the given attribute).

![Data sources summary](../images/wpa/Use/organizational-data-summary.png)

The **Last refreshed** date shows when data was last processed.

### Values

A list of the attributes provided by your organization. When you [create queries](../Tutorials/Query-basics.md), you can filter and group employees in the organization by using the attributes, so being familiar with these attributes will help give insight into the types of queries you may want to create for analysis.

### Measured employees

The number of employees for whom your Workplace Analytics administrator assigned licenses to during setup. Workplace Analytics collects meeting and email data about these people. As an Analyst or Limited Analyst, this is the population you can analyze within Workplace Analytics.

### Coverage

The percentage of measured employees who have a value specified for the given attribute. If coverage levels are low, it will be difficult to determine how people collaborate across different characteristics. Additionally, low coverage on required attributes may give skewed (under reported) metric calculations for metrics that rely on those attributes.

### Unique values

The count of the unique attribute values included in the data. For example, if the attribute Region contains North, South, Central, East, West and Southwest, it’s unique values count is six.
