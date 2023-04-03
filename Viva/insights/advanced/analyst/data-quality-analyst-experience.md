---
ms.date: 03/22/2023
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

Missing data means that certain employee attributes—that is, columns—weren't in the organizational data your admin uploaded. Because employee attributes are tied to insights, missing attributes lead to missing insights.

### Low-quality data and coverage

Viva Insights uses *coverage* to determine low-quality attributes. Coverage is the percentage of rows in your organizational data file that aren't blank.

In organizational data files, each column header contains attribute names, and each row within those columns contains attribute values. If a column has no blank rows, that attribute has *high coverage*. If a column has too many blank rows, that attribute has *low coverage*. Attributes with less than 30% coverage are considered *low-quality*. Similar to missing insights, when data is of low quality, related insights are of low quality, too.

In the image below, the attribute on the left, **Organization**, has high coverage. The attribute on the right, **TimeZone**, has low coverage. If an admin uploaded this data to the advanced insights app, Viva Insights would consider **TimeZone** to be a low-quality attribute.

:::image type="complex" source="../images/analyst-quality-attributes-smaller.png" alt-text="Screenshot that shows a full-coverage attribute and a low-coverage attribute."lightbox="../images/analyst-quality-attributes2.png":::
   Screenshot of an upload file that shows two attributes: Organization and TimeZone. Organization has values for all 19 displayed rows. TimeZone only has values for 6 displayed rows.
:::image-end:::

### To view data quality

Two pages in the advanced insights app inform you about your data quality: **Data hub** and **Organizational data**. You can get to these pages by selecting them from the app's left pane.

#### On the Data hub

Use the **Data hub** page to view the number of:

* Missing or low-quality insights
* Available insights
* Missing or low-quality data fields
* Days since the data last refreshed

You can also view the percentage of insights displayed in Viva Insights based on the total number of possible insights. When your admin adds more organizational data, more insights become available and this percentage increases.

If fields are missing from your uploaded data, you'll find them in a list beneath the **Missing or low-quality insights and data fields** header. Select a missing insight to see its related data fields, and vice versa. To remove an insight from this list, your admin will need to upload the related data field(s) to the advanced insights app.

#### On the Organizational data page

Use this page to view attribute-specific information, including:

* **Quality score**, which represents the attribute's [coverage](#low-quality-data-and-coverage).
* **Last updated**, which lists when your admin last uploaded this attribute Viva Insights.
* **Employees with this field**, which shows how many employees in your organizational data have a value for this attribute.
* **Unique values**, which shows how many values for the attribute are unique.

### To contact your admin 

To address the data-quality errors and warnings we explain below—or to address missing insights on the **Data hub**—you might need to have your admin re-upload organizational data. The **Contact admin** page provides a list of your organization’s admins and their contact information, and also provides a button to directly send them an email. Reach the **Contact admin** page on the app's left pane.

## Attribute-quality notifications in queries

You might notice warnings about attribute quality while you're building custom or Power BI queries. These warnings can crop up in three places: 

* On metrics that use low-quality attributes
* In filters, when you use a low-quality attribute in a condition statement
* On low-quality attributes you select

In addition to warnings on specific metrics and attributes, you'll also find a banner at the top of the page.

Because your admin makes updates to your organizational data, attribute quality can change over time. While setting up a query, Viva Insights calculates the quality of attributes for the time period you select.

### In custom queries

#### Warnings on metrics

Low-quality attributes can affect metrics. Let's use an example. In your query, you want to add a metric that calculates how long people spend in meetings organized by the marketing department. This metric depends on an employee attribute that identifies people in the marketing department. If that attribute is of low quality, the metric won't have all the information it needs to work properly. 


If your organizational data contains low-quality attributes, you might notice a yellow warning tag on your metrics. To find out which attribute is causing a warning on your metric, hover over the metric name. The warning will say something like this:

`The low quality of TimeZone is affecting this metric`

Even though the metric has a warning, you can still use it in your query.

#### Warnings on filters

When you're using a filter, either to create custom metrics or to select which employees or meetings to include in your query, you might notice attribute warnings in your condition statement(s). If an attribute is of low quality, the app will mark it with a warning icon, but you can still use it in your filter.

#### Warnings on attributes

When setting up a query, you'll select which employee attributes you want the query to include. Similar to metrics, the app will mark low-quality employee attributes with a warning icon. Even though the attribute has a warning, you can still use it in your query.

### In Power BI template queries

In PowerBI template queries, you might encounter data-quality errors and/or warnings. Let's discuss when these notifications might appear.

#### Warnings or errors on preselected metrics

Power BI templates use metrics to produce insights. To make sure your template shows these insights correctly, we've preselected metrics for you in Power BI template queries. Preselected metrics appear in gray, and you can’t remove them. If a preselected metric uses a low-quality attribute, the app will flag the metric with a warning. Hover over the warning icon to get the name of the low-quality attribute. If your query has warnings, you can still run it and load the results into Power BI.

> [!NOTE]
> Right now, Power BI reports don't show which insights use flagged metrics.

#### Warnings or errors on filters

Warnings on filters appear the same as they do in [custom queries](#warnings-on-filters).

#### Warnings or errors on employee attributes

##### Basic attributes

Power BI templates require certain basic attributes to work properly. These attributes appear in gray, and you can’t remove them.

If basic attributes are of low quality, the app will flag them with a warning. If your query has low-quality basic attributes, you can still run it and load results into Power BI.

>[!Note]
>Right now, Power BI reports don't show which insights use flagged metrics.

If basic attributes are missing from your organizational data, the app will flag them with an error, and you won't be able to run the query or load results into Power BI. You'll need to contact your admin to get the right data uploaded.

##### Supplemental attributes

We also preselect a few supplemental attributes in your query, which help create filter-based insights in your Power BI template. You can remove these attributes from your query if you want, but keep in mind that doing so might affect certain insights in Power BI.

If your query has low-quality supplemental attributes, or if supplemental employee attributes are missing from your organizational data, the app will flag these attributes with a warning. You can still run your query and load results into Power BI. However, missing or low-quality supplemental attributes will result in missing or low-quality insights in your template.

### Data-quality notifications in query results

On the **Query results** page, you might notice warnings next to your query's name. These warnings might crop up for a few reasons. Maybe you ran a query knowing that it used low-quality attributes. Or, your query might not have had any low-quality attributes at the time you ran it, but after a recent data upload, the quality of some attributes decreased.

If you find a data-quality warning, select the query's name or **View query**. The app will show which attributes are of low quality. 

