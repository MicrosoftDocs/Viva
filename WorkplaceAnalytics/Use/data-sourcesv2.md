---
# Metadata Sample
# required metadata

title: Workplace Analytics data sources
description: An overview of Sources in Workplace Analytics 
author: madehmer
ms.author: v-midehm
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Data sources

>[!Note]
>You must be assigned either the administrator or the analyst role to access the **Data sources** page. For more information, see [Assign roles to Workplace Analytics admins and analysts](../setup/assign-roles-to-wpa-admins.md).

**Data sources** contains high-level views for Workplace Analytics administrators and data analysts to confirm that your Office 365 and organizational data is loaded and ready to use. Sources includes the following:

  - [Office 365 data](#office-365-data)
  - [Organizational data](#organizational-data)
  - [CRM data](#crm-data)

![Sources](../images/WpA/Use/sources-o365.png)

[!INCLUDE [To open Sources in Workplace Analytics](../includes/to-open-wpa-sources.md)]

## Office 365 data

As an admin or an analyst, you can use this page to confirm that your Office 365 data is up-to-date. Use this page to look for date ranges that have unexpected gaps in activity, inconsistent or degraded data, or activity levels that are higher or lower than what might be considered normal for your organization.

This page includes the following types of data.

* **Measured employees**: The employees to whom your Workplace Analytics administrator assigned licenses during setup. After license assignments, Workplace Analytics extracts Office 365 data about meetings, email, unscheduled calls, and instant messages for these people. When the data extraction process is successful for these employees, they are included in your measured population. If extraction errors occur and Workplace Analytics didn't get data for a person, that person is licensed but not counted as a measured employee in Workplace Analytics. If you are an analyst or limited analyst, this is the population that you can analyze within Workplace Analytics. The number of measured employees can help determine whether you have good data coverage for analysis.

  >[!Note]
  > Your admin can assign employees Workplace Analytics licenses as a group with Azure Active Directory (AAD). If this number seems inaccurate, confirm with your admin that only active employees are assigned licenses through AAD. For more details, see [Assign licenses](../setup/assign-licenses-to-population.md).

* **Internal collaborators**: These are unmeasured employees who were included in extractions of Office 365 data with whom the _measured_ employees collaborated. These people are not part of your measured population but are internal to your organization. Internal collaborators can include employees from other groups, vendors, or contractors that are working with your team and are included in the same internal domain as your team, but are not in your measured population.

* **External collaborators**: These are people outside of your company or external to your email domain with whom your measured employees collaborated. For more information about external collaboration, see [External collaboration](../use/explore-metrics-external-collaboration.md).

* **Average weekly collaboration chart**: This chart shows the last refreshed on weekly collaboration hours for measured employees by type, which can include hours spent on email, in meetings, in unscheduled calls, and on instant messages. The Last refreshed date shows when Office 365 Exchange and Teams data was most recently processed for this chart.

Hover your cursor over the chart data to get more details and use the chart legend to change what data (meetings, email, instant messages, and calls) the chart shows.

  ![Office 365 data sources page](../images/wpa/use/measured-collab.png)
<!--
  >[!Note]
  > If collaboration activity for Teams drops below 30 percent of the total collaboration, the unscheduled calls and instant message data will not show due to insufficient data.
-->

The following are examples of where you might encounter instances of  inconsistency in the volume of email, meetings, calls, and instant messages data.

* **Major holidays**: Drops in email and meeting activity around major holidays is typical and can potentially impact analysis. You can remove these weeks from your outputs to reduce its impact.

* **Email archive policies**: Business policies can impact historical data processed during initial setup. As you view historical data, if you see a steady decline or point-in-time drop-off in email and/or meeting activity, it might be due to archiving. By using the Average weekly collaboration chart (see the preceding illustration), you can select a date range to analyze your collaboration data where the mail volume is stable.

* **Recurring meetings**: When a recurring meeting series is removed from a calendar, all past instances of this meeting are removed. As you view historical data, if you see a steady decline in meeting activity, it might be due to recurring meetings having been removed from calendars. By using the Average weekly collaboration chart (see the preceding illustration), you  can select a date range to analyze your collaboration data where the meeting volume is stable.

## Organizational data

Organizational data is information about employees that your company provides to Workplace Analytics through [uploads](../setup/upload-organizational-data.md) of organizational (HR) data.

As either an admin or an analyst, you can use this page to understand the data quality and completeness for employees who have an entry in the HR data file and are detected in the specified week's refresh of Office 365 data.

![Organizational data sources page](../images/wpa/Use/org-data-sources.png)

This page includes the following.

* **Page settings**: Use the Page settings panel to the right of the page to change the **Group by** increments of time (day, week, or month) and what employees to include (all employees, internal collaborators, or measured employees) in the data shown. You can also use the Page setting **Filters** to filter the employee data shown on this page by a specific attribute, such as to only show employees in the sales or development groups.
* **Attributes**: These are all the attributes provided by your organization in the organizational or HR data upload file. When you [create queries](../Tutorials/Query-basics.md), you can filter and group employees in the organization by these attributes, so being familiar with them will give you insight into the types of queries to use for analysis.
* **Employees with attribute**: The number of measured employees and internal collaborators with a non-blank value for the attribute.
* **Coverage**: The percentage of measured employees who have a non-blank value for the specified attribute. If coverage levels are low, it'll be difficult to determine how people collaborate across different characteristics. Additionally, low coverage on required attributes may give skewed (under reported) metric calculations for metrics that rely on those attributes.
* **Unique values**: The count of the unique attribute values included in the data. For example, if the **Region** attribute contains **North**, **South**, **Central**, **East**, **West** and **Southwest**, it’s unique values count is six.

>[!Note]
> You can select a column name to sort the list by it in descending or ascending order. You can also type a keyword in the **Search** field to narrow the list to all attributes that contain that keyword.

### Attribute details

 To view a list of the top 500 values for an attribute and other details about it, select the attribute's name in the list. For example, the following graphic shows the top values and details for **Region**.

![View Organizational data attributes for Region](../images/wpa/Use/org-data-attributes.png)

This page includes the following.

* **Page settings**: Use the Page settings panel to the right of the page to change the **Group by** increments of time (day, week, or month), the date range, and what employees to include (all employees, internal collaborators, or measured employees) in the data shown. You can also use the Page setting **Filters** to filter the employee data shown on this page by a specific attribute, such as to only show employees in the sales or development groups.
* **Coverage for**: This chart shows the coverage for the selected attribute at different moments in time. This historical data gives you insight into how the data for this attribute has changed over time and what date ranges will be useful for analysis. Select a bar in the chart to see the details for that date in the table.
* **Values**: Lists all values that exist for the selected attribute that were included in the uploaded organizational data for the selected date. When you [create queries](../Tutorials/Query-basics.md), you can filter and group accounts with a few of these attributes, so being familiar with these gives you insight into what types of queries will be useful for analysis.
* **Employees with this value**: This shows the number of people that have that attribute value in the data. For example, the following graphic shows the number of contacts that have a non-blank value for the selected attribute.
* **Coverage**: Shows the percentage of employees with that value.

>[!Note]
> Next to **Attribute details**, you can select a different attribute to change the focus of the details to it. Also, only the first 500 values are shown in this page's table. If the selected attribute has more than 500 values, you can select **Download CSV** to view the complete list of attribute values and details for those with more than 500 values in the downloaded .csv file.

For more information about what data is needed for metric calculations, see:

* [Prepare organizational data](../setup/Prepare-organizational-data.md)

* [Metric definitions](../Use/Metric-definitions.md)

## CRM data

This page provides a high-level view of the latest available CRM data that was uploaded and successfully processed in Workplace Analytics. It includes the number of accounts, contacts, and seller assignments that are available for data analysis.

By combining this data in Workplace Analytics, you can now analyze how sales activities connect to organizational outcomes. For example, you could analyze if the time your sales team spent with various accounts is proportionate to the revenue potential of those accounts, or if your top tier accounts are getting enough attention from your sales team.

The **Join coverage** section describes the percent overlap between the uploaded list of accounts and the other uploaded lists of important CRM data, such as contacts and seller assignments, as shown in the following graphic. The higher the percentage overlap the more accurate analysis you can accomplish.

![CRM data sources page](../images/wpa/Use/crm-sources.png)

For join coverage based on the latest data uploads, you might see one of the following important notices, as shown in the following graphic.

* **Data is not associated**: This occurs when one or more attributes cannot be associated between the two sets of data for join coverage. You can select to download a .csv file and view the contacts or sellers that can't be associated with the corresponding accounts in the accounts table.
* **Data has not been processed**: This occurs when an upload hasn't been done yet, the data is currently being processed, or something failed during the validation or data processing phase. You can select the link to the Upload page and view the status of the upload, correct any issues, or upload new data. You can also ignore this warning if you don't plan to upload that specific data file.

![CRM join notices](../images/wpa/Use/crm-join-notices.png)

You can select one of the data titles, such as accounts or contacts, to view a list of attributes for it. For example, the following shows a list of attributes for contacts.

![View CRM attributes for contacts](../images/wpa/Use/crm-contact-attributes.png)

Similar to the Organizational data page, the CRM data attributes list includes the following.

* **Data upload date**: Shows when the data was last uploaded and processed, which is at the top of the list.
* **Attribute**: Lists the attributes provided in the uploaded data. When you [create queries](../Tutorials/Query-basics.md), you can filter and group accounts with a few of these attributes, so being familiar with these helps give insight into the types of queries you might want to create for analysis.
* **Employees with this attribute**: Depending on what data you're looking at, this shows the number of people that have that attribute in that data file. For example, the following graphic shows the number of contacts that have a non-blank value for that attribute.
* **Coverage**: Shows the percentage of attributes that have non-blank values. For example, in following graphic, 87.5% or 7 out of 8 accounts have non-blank values for the **AccountAnnualRevenue** attribute.
* **Unique values**: The count of the unique attribute values included in the data.

![View CRM attributes for accounts](../images/wpa/Use/crm-account-attributes.png)

>[!Note]
> You can select a column name to sort the list by it in descending or ascending order.

To view a list of the top 100 values for an attribute, select the attribute's name from the list. For example, the following graphic shows the top values for **AccountId** in an accounts data file.

* To view the list for a different attribute, select it from the list at the top of the table.
* You can select a column title to sort the list by that column in descending or ascending order.
* Type a keyword in the **Search** field to search all attributes that include that keyword, such as email or phone.

![View CRM attribute values for accounts](../images/wpa/Use/crm-account-attribute-values.png)
