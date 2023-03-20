---
ms.date: 07/14/2022
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

## About missing and low-quality data

### Missing data

Missing data means that certain employee attributes--that is, columns--haven’t been included in the organizational data your admin uploaded. Because employee attributes are tied to insights, missing attributes lead to missing insights.

### Low-quality data and coverage

Viva Insights uses *coverage* to determine low-quality attributes. Coverage is the percentage of non-blank rows in organizational data. 

In organizational data files, each column header contains attribute names, and each row within those columns contains attribute values. If a column has no blank rows--meaning that an attribute column has a value for every employee--that attribute has *high coverage*. If a column has too many blank rows, that attribute has *low coverage*. 

Attributes with less than 30% coverage are considered low-quality. Similar to missing insights, when data is of low quality, related insights are of low quality, too.

In the image below, the attribute on the left has high coverage and the attribute on the right has low coverage. Viva Insights would consider the attribute on the right to be a low-quality attribute.

:::image type="complex" source="../images/analyst-quality-attributes-smaller.png" alt-text="Screenshot that shows a full-coverage attribute and a low-coverage attribute."lightbox="../images/analyst-quality-attributes2.png":::
   Screenshot of an upload file that shows two attributes: Organization and TimeZone. Organization has values for all 19 displayed rows. TimeZone only has values for 6 displayed rows.
:::image-end:::

To view the quality of uploaded data, select **Organizational data** on the app’s left pane. If there’s a problem with data used in a query you’ve run or are about to run, warning messages in your query might also take you to the **Organizational data** page, as we explain below.


## Data-quality notifications 

### In queries

While setting up a custom query or Power BI template query, you might get a notification about low-quality attributes. If a low-quality attribute is impacting your query, you'll notice a banner at the top of the page. You'll also get specific information about which employee attributes are of low quality, and which metrics and filters are those attributes are impacting.<!--You can also go to the Organizational data page to check on the quality of your data, and to see which insights are missing or of low quality.--> 

To increase data quality, you might need to have your admin upload attributes or other data.


#### Warnings or errors on metrics

Low-quality attributes can affect metrics. For example, a metric that calculates the amount of time people spend in meetings organized by Marketing must depend on an employee attribute that identifies people in Marketing. If the employee attribute is low-quality, the metric will be impacted by the low-quality of the employee attribute.

Metrics impacted by low-quality employee attributes will be marked with a warning icon. If you hover over the warning icon, you’ll see the name of the employee attribute that’s impacting the metric. You can still select the metric and use it in your query.

#### Warnings or errors on filters

You can use filters to create custom metrics and select which employees or meetings you want to include in your query.

Low-quality employee attributes will be marked with a warning icon. You can still use the employee attribute to create a filter.

#### Warnings or errors on attributes

When setting up a query, you can select which employee attributes to include. Low-quality employee attributes will be marked with a warning icon. You can still select the employee attribute in your query.

### Warnings and errors in Power BI template queries

#### Warnings or errors on metrics

Predefined template metrics are preselected in Power BI templates. They appear in gray, and you can’t remove them. If a preselected metric is impacted by low-quality employee attributes, the metric will be marked:

* With a warning icon, if the metric impacts only a few insights in the Power BI template. If you hover over the warning icon, you’ll see the name of the employee attribute that’s impacting the metric. You can still run the query and load the results into Power BI.
    >[!Important]
    >We currently don’t highlight the insights that are impacted by low-quality employee attributes Power BI. We will build this in the future.

* With an error icon, if the metric impacts all insights in the Power BI template. If you hover over the error icon, you’ll see the name of the employee attribute that’s impacting the metric. You can’t run the query or load results into Power BI.

#### Warnings or errors on filters

See <include link to Setting up a custom query -> Applying filters>

Selecting employee attributes

Some employee attributes are required to set up Power BI templates. We preselect them for you, and you can’t remove them.
•	Low-quality required employee attributes will be marked with a warning icon. You can still run your query and load results into Power BI.
Important
We currently don’t highlight the insights that are impacted by low-quality employee attributes in Power BI. We will build this in the future.
•	Missing required employee attributes will be marked with an error icon. You can’t run the query or load results into Power BI.
Some employee attributes are optional when you set up Power BI templates. We preselect them for you, but you can remove them if you want. Certain insights of filtering capabilities may be impacted in the Power BI templates.
•	Low-quality or missing optional employee attributes will be marked with a warning icon. You can still run your query and load results into Power BI. If the employee attribute is missing, the field will be empty in Power BI.

### Data-quality notifications in query results

You may have decided to run a query knowing that it’s results will be impacted by low-quality employee attributes. Or you may have set up a query which was not impacted by low-quality employee attributes at the time of setup, but over time the quality of the attributes used in it may have changed, impacting periodic refreshes.

Query results impacted by low-quality employee attributes will be marked as having succeeded, but impacted by low-quality employee attributes. If you select the query name or select View query, you’ll get information on the attributes impacting the query.


### Using the Organizational data page

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
 

