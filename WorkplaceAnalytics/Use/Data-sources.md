---
# Metadata Sample
# required metadata

title: Workplace Analytics data sources
description: An overview of Sources in Workplace Analytics 
author: madehmer
ms.author: v-midehm
ms.date: 05/24/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Sources

**Sources** contains high-level views for Workplace Analytics administrators and data analysts to confirm that your Office 365, organizational data, and if applicable, Customer Relationship Management (CRM) data is loaded and ready to use. Sources includes the following:

- [Sources](#sources)
  - [Office 365 data](#office-365-data)
  - [Organizational data](#organizational-data)
      - [Detailed coverage information for an attribute](#detailed-coverage-information-for-an-attribute)
  - [CRM data](#crm-data)

![Sources](../images/WpA/Use/sources-o365.png)

[!INCLUDE [To open Sources in Workplace Analytics](../includes/to-open-wpa-sources.md)]

## Office 365 data

As an analyst, you can use this page to confirm that your Office 365 data is up-to-date. This page includes the following types of data.

* **Measured employees**: The number of measured employees to whom your Workplace Analytics administrator assigned licenses to during setup. Workplace Analytics extracts Office 365 data about meeting, email, unscheduled calls, and instant messages for these people. <!-- When the data extraction process is successful for these employees, they are included in your measured population. If extraction errors occur and Workplace Analytics didn't get data for a person, that person is licensed but not counted as a measured employee in Workplace Analytics.--> As an Analyst or Limited Analyst, this is the population you can analyze within Workplace Analytics. This number can help determine whether you have good data coverage for analysis.

  >[!Note]
  > Your admin can assign employees Workplace Analytics licenses as a group with Azure Active Directory (AAD). If this number seems inaccurate, confirm with your admin that only active employees are assigned licenses through AAD. For more details, see [Assign licenses](../setup/assign-licenses-to-population.md).

* **Internal collaborators**: This is the number of unmeasured employees included in the latest extraction of Office 365 data with whom the measured employees collaborated. These people are not part of your measured population but are internal to your organization. <!--Internal collaborators can include employees from other groups, vendors, or contractors that are working with your team and are included in the same internal domain as your team, but are not in your measured population.-->

* **External collaborators**: This is the number of people outside your company or who are external to your email domain with whom your measured employees collaborated. For more information about external collaboration, see [External collaboration](../use/explore-metrics-external-collaboration.md).

* **Average weekly collaboration chart**: This chart shows the average weekly collaboration hours for measured employees by type, which can include hours spent on email, in meetings, in unscheduled calls, and on instant messages. The Last refreshed date shows when Office 365 Exchange and Teams data was most recently processed for this chart.

<!-- MARILYN IS CHECKING WITH CATY ABOUT THE VERACITY OF THIS NOTE:
  >[!Note]
  > If collaboration activity for Teams drops below 30 percent of the total collaboration, the unscheduled calls and instant message data will not show due to insufficient data.
-->

Analysts can use these views to look for date ranges that have unexpected gaps in activity, inconsistent or degraded data, or activity levels that are higher or lower than what might be considered normal for your organization.

<!-- REPLACE WITH NEW ONE, PER MARILYN 30 MAY
![Office 365 data sources page](../images/wpa/Use/sources-o365-data-summary.png)
-->

![Office 365 data sources page](../images/wpa/use/measured-collab.png)

The following are examples of where you might encounter inconsistency in volume for email, meetings, calls, and instant messages.

* **Major holidays**: Drops in email and meeting activity around major holidays is typical and can potentially impact analysis. You can remove these weeks from your outputs to reduce its impact.

* **Email archive policies**: Business policies can impact historical data processed during initial setup. As you view historical data, if you see a steady decline or point-in-time drop-off in email and/or meeting activity, it might be due to archiving. By using this view, you can select a date range to analyze your collaboration data where the mail volume is stable.

* **Recurring meetings**: When a recurring meeting series is removed from a calendar, all past instances of this meeting are removed. As you view historical data, if you see a steady decline in meeting activity, it might be due to recurring meetings having been removed from calendars. By using this view, you can select a date range to analyze your collaboration data where the meeting volume is stable. 

## Organizational data

Organizational data is information about employees that your company provides to Workplace Analytics through your most [recent upload](../setup/upload-organizational-data.md) of organizational (HR) data and the specified date range of Office 365 data.

As either an admin or an analyst, you can use this page to understand the data's quality and completeness for employees who have been detected in the Office 365 data for the specified date range. Select **Settings** at the top right of the page to change what date range you want to view.

![Organizational data sources page](../images/wpa/Use/org-data-sources.png)

The following is listed in the table on this page.

* **Attributes**: These attributes are provided by your organization in the organizational or HR data upload file. When you [create queries](../Tutorials/Query-basics.md), you can filter and group employees in the organization by these attributes, so being familiar with the attributes will help give insight into the types of queries you might want to create for analysis.
* **Employees with attribute**: The number of measured employees and internal collaborators with a non-blank value for the attribute.
* **Coverage**: The percentage of measured employees who have a non-blank value for the specified attribute. If coverage levels are low, it'll be difficult to determine how people collaborate across different characteristics. Additionally, low coverage on required attributes may give skewed (under reported) metric calculations for metrics that rely on those attributes.
* **Unique values**: The count of the unique attribute values included in the data. For example, if the **Region** attribute contains **North**, **South**, **Central**, **East**, **West** and **Southwest**, it’s unique values count is six.

>[!Note]
> You can select a column name to sort the list by it in descending or ascending order. You can also type a keyword in the **Search** field to search all attributes that include that keyword, such as email or phone.


#### Detailed coverage information for an attribute

 To view a list of the top 500 values for an attribute and other details about it, select the attribute's name in the list. For example, the following graphic shows the top values and details for **Area**.

![View Organizational data attributes for area](../images/wpa/Use/org-data-attributes.png)

This detailed coverage page includes the following.

* **Coverage over time**: This chart shows how the attribute when the data was last uploaded and processed, which is at the top of the list.
* **Values**: Lists all values for the selected attribute provided in the uploaded data. When you [create queries](../Tutorials/Query-basics.md), you can filter and group accounts with a few of these attributes, so being familiar with these helps give insight into the types of queries you might want to create for analysis.
* **Employees with value**: This shows the number of people that have that attribute value in the data file. For example, the following graphic shows the number of contacts that have a non-blank value for that attribute.
* **Coverage**: Shows the percentage of measured employees with that value.

>[!Note]
> Select Download Excel to view the complete list of attribute details for that have more than 500 value for the page view. To view the list for a different attribute, go back to the Organizational data intro page and select its name from the table.

For more information about what data is needed for metric calculations, see:

* [Prepare organizational data](../setup/Prepare-organizational-data.md)

* [Metric definitions](../Use/Metric-definitions.md)

## CRM data

This page provides a high-level view of the latest available CRM data that was uploaded and successfully processed in Workplace Analytics. It includes the number of accounts, contacts, and seller assignments that are available for data analysis.

By combining this data in Workplace Analytics, you can now analyze how sales activities connect to organizational outcomes. For example, you could analyze if the time your sales team spent with various accounts is proportionate to the revenue potential of those accounts, or if your top tier accounts are getting enough attention from your sales team?

The **Join coverage** section describes the percent overlap between the uploaded list of accounts and the other uploaded lists of important CRM data, such as contacts and seller assignments, as shown in the following graphic. The higher the percentage overlap the more accurate analysis you can accomplish.

![CRM data sources page](../images/wpa/Use/crm-sources.png)

For join coverage based on the latest data uploads, you might see one of the following important notices, as shown in the following graphic.

* **Data is not associated**: This occurs when one or more attributes cannot be associated between the two sets of data for join coverage. You can select to download a .csv file and view the contacts or sellers that can't be associated with the corresponding accounts in the accounts table.
* **Data has not been processed**: This occurs when an upload hasn't been done yet, the data is currently being processed, or something failed during the validation or data processing phase. You can select the link to the Upload page and view the current status of the upload, correct any issues, or upload new data. You can also ignore this warning, if you don't plan to upload that specific data file.

![CRM join notices](../images/wpa/Use/crm-join-notices.png)

You can select one of the data titles, such as accounts or contacts, to view a list of attributes for it. For example, the following shows a list of attributes for contacts.

![View CRM attributes for contacts](../images/wpa/Use/crm-contact-attributes.png)

Similar to the Organizational data page, the CRM data attributes list includes the following.

* **Data upload date and time**: Shows when the data was last uploaded and processed, which is at the top of the list.
* **Attribute**: Lists the attributes provided in the uploaded data. When you [create queries](../Tutorials/Query-basics.md), you can filter and group accounts with a few of these attributes, so being familiar with these helps give insight into the types of queries you might want to create for analysis.
* **Employees with attribute**: Depending on what data you're looking at, this shows the number of people that have that attribute in that data file. For example, the following graphic shows the number of contacts that have a non-blank value for that attribute.
* **Coverage**: Shows the percentage of attributes that have non-blank values. For example in following graphic, 87.5% or 7 out of 8 accounts have non-blank values for the AccountAnnualRevenue attribute.
* **Unique values**: The count of the unique attribute values included in the data.

![View CRM attributes for accounts](../images/wpa/Use/crm-account-attributes.png)

>[!Note]
> You can select a column name to sort the list by it in descending or ascending order.

To view a list of the top 100 values for an attribute, select the attribute's name from the list. For example, the following graphic shows the top values for **AccountId** in an accounts data file.

* To view the list for a different attribute, select it from the list at the top of the table.
* You can select a column title to sort the list by that column in descending or ascending order.
* Type a keyword in the **Search** field to search all attributes that include that keyword, such as email or phone.

![View CRM attribute values for accounts](../images/wpa/Use/crm-account-attribute-values.png)
