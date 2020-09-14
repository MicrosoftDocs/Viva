---
# Metadata Sample
# required metadata

title: Workplace Analytics Organizational data
description: What's available on the Organizational data sources page in Workplace Analytics 
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Organizational data

Organizational data is information about employees that your company provides to Workplace Analytics through [uploads](../setup/upload-organizational-data.md) of organizational (HR) data.

As either an admin or an analyst, you can use this page to understand the data quality and completeness for employees who have an entry in the HR data file and are detected in the specified week's refresh of Office 365 data.

![Organizational data sources page](../images/wpa/Use/org-data-sources.png)

This page includes the following.

* **Page settings** (Settings and filters): Use the Page settings panel to the right of the page to change the **Group by** increments of time (day, week, or month) and what employees to include (all employees, internal collaborators, or measured employees) in the data shown. You can also use the Page setting **Filters** to filter the employee data shown on this page by a specific attribute, such as to only show employees in the sales or development groups.
* **Attributes**: These are all the attributes provided by your organization in the organizational or HR data upload file. When you [create queries](../Tutorials/Query-basics.md), you can filter and group employees in the organization by these attributes, so being familiar with them will give you insight into the types of queries to use for analysis.
* **Employees with attribute**: The number of measured employees and internal collaborators with a non-blank value for the attribute.
* **Coverage**: The percentage of measured employees who have a non-blank value for the specified attribute. If coverage levels are low, it'll be difficult to determine how people collaborate across different characteristics. Additionally, low coverage on required attributes may give skewed (under-reported) metric calculations for metrics that rely on those attributes.
* **Unique values**: The count of the unique attribute values included in the data. For example, if the **Region** attribute contains **North**, **South**, **Central**, **East**, **West** and **Southwest**, it’s unique values count is six.

>[!Note]
> You can select a column name to sort the list by it in descending or ascending order. You can also type a keyword in the **Search** field to narrow the list to all attributes that contain that keyword.

## Attribute details

 To view a list of the top 500 values for an attribute and other details about it, select the attribute's name in the list. For example, the following graphic shows the top values and details for **Region**.

![View Organizational data attributes for Region](../images/wpa/Use/org-data-attributes.png)

This page includes the following.

* **Page settings** (Settings and filters): Use the Page settings panel to the right of the page to change the **Group by** increments of time (day, week, or month), the date range, and what employees to include (all employees, internal collaborators, or measured employees) in the data shown. You can also use the Page setting **Filters** to filter the employee data shown on this page by a specific attribute, such as to only show employees in the sales or development groups.
* **Coverage for**: This chart shows the coverage for the selected attribute at different moments in time. This historical data gives you insight into how the data for this attribute has changed over time and what date ranges will be useful for analysis. Select a bar in the chart to see the details for that date in the table.
* **Values**: Lists all values that exist for the selected attribute that were included in the uploaded organizational data for the selected date. When you [create queries](../Tutorials/Query-basics.md), you can filter and group accounts with a few of these attributes, so being familiar with these gives you insight into what types of queries will be useful for analysis.
* **Employees with this value**: This shows the number of people that have that attribute value in the data. For example, the following graphic shows the number of contacts that have a non-blank value for the selected attribute.
* **Coverage**: Shows the percentage of employees with that value.

>[!Note]
> Next to **Attribute details**, you can select a different attribute to change the focus of the details to it. Also, only the first 500 values are shown in this page's table. If the selected attribute has more than 500 values, you can select **Download CSV** to view the complete list of attribute values and details for those with more than 500 values in the downloaded .csv file.

For more information about what data is needed for metric calculations, see:

* [Prepare organizational data](../setup/Prepare-organizational-data.md)
* [Metric definitions](../Use/Metric-definitions.md)

## Related topics

* [Office 365 data](office-365-data.md)
* [CRM data](crm-data.md)