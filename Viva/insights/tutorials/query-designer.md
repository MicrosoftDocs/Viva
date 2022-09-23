---
ROBOTS: NOINDEX,NOFOLLOW
title: Query designer in Viva Insights
description: The Query designer in Viva Insights offers predefined Templates and other custom query options for more in-depth data analysis
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Query designer

The **Query designer** in the advanced insights app combines templates and queries together into a single view.

* [**Templates**](#templates) &ndash; The templates provide an easy way to bring a predefined set of query metrics into a template, where you can quickly analyze workplace patterns and trends about a specific business challenge.
* [**Queries**](#queries) &ndash; You can also create your own custom query to create datasets that answer custom business challenges. After creating a dataset, you can analyze the data in a tool of your choice.

## Requirements for analysts

[!INCLUDE [Requirements for analysts](../includes/analyst-requirements.md)]

## Templates

The Query designer has a number of [predefined templates](#available-templates) that help you analyze behavioral patterns relating to common business challenges, such as: how to transform meeting culture, enhance organizational resilience, develop effective managers, boost employee engagement, and more.

![Templates.](../Images/WpA/Tutorials/query-designer.png)

The templates are designed to use query output. After you find the right template for your analysis, you can run a more specific query and plug it into the template to get a more complete Power BI report.

To find the right template, read the template descriptions or select one to view additional information about it.

If you select one of the templates, such as **Business continuity**, you'll see the questions that the template can help you answer, what its prerequisites are, and how to set it up. You’ll also notice that it requires you to have a recent version of Power BI and to run two pre-defined queries.

![Template details.](../images/wpa/tutorials/qd-template-details.png)

>[!Note]
>The **Setup steps** are condensed and simplified. For more complete instructions, see documentation for the specific template.

You can also filter the list of templates to help identify which ones answer questions about business outcomes that you might have. For example, you’ll see the following when you select **Filters** > **Develop effective managers**.

![Example filtered template view.](../images/wpa/tutorials/qd-template-filter.png)

### Available templates

The advanced insights app currently includes the following predefined templates.

* [**Ways of working assessment**](./power-bi-collab-assess.md) &ndash; Shows a quick and easy way to see current collaboration behaviors and culture and insights into employee wellbeing and engagement in your organization.
* [**Ways of working tracker**](./power-bi-collab-track.md) &ndash; Shows how you can track behavior change and target opportunities to improve employee wellbeing, meeting culture, and manager effectiveness.
* [**Return to worksites**](./power-bi-return-tw.md) &ndash; Shows how to plan which employees return to work, and when, where, and how they do so for different work locations.
* [**Business continuity**](./power-bi-bc.md) &ndash; Shows example insights into how shifting to remote work affected your business.
* [**Microsoft Teams insights**](./power-bi-teams.md) &ndash; Shows how adopting Microsoft Teams can affect collaboration and productivity in your organization.
* [**Manager effectiveness**](./power-bi-manager.md) - Helps leaders measure behaviors and trends of their people managers across four key themes within the organization, including coach, empower, connect, and model.
* [**Behavior patterns for Glint**](./power-bi-glint-2.md) &ndash; Combines behavioral data from Viva Insights and sentiment data from Glint to produce insights that help identify opportunities to influence behavior and improve business outcomes.
* [**Sales business continuity**](./pbi-bc-sales.md) &ndash; Shows insights into how shifting to remote work impacted your sales organization.

For details about how to share a dashboard and other Power BI tips, troubleshoot any issues, or review the FAQ, see [Power BI tips, FAQ, and troubleshooting](../tutorials/power-bi-templates.md).

## Queries

In the Query designer, you can also create your own custom [query](#query-types) by selecting **Get started** under **Query**.

![New query options.](../Images/WpA/Tutorials/qd-new-query.png)

When available and listed, you can also select from one or more related [query templates](#query-templates). For example, when creating a new Person query, you can either select **Start a new query** or select a query template, such as **Standard person query** or **Hourly collaboration**, which already have specific metrics set up to help you get started.

![Query templates available when creating a new query.](../Images/WpA/Tutorials/qd-query-options.png)

You can download the query data results as .csv files, or depending on the type of data, you can also visualize it directly in the advanced insights app. See [View, download, and export query results](../use/view-download-and-export-query-results.md) for details.

### Query types

* [**Person queries**](person-queries.md) - Use to find broad organizational trends by analyzing aggregated productivity metrics (such as time in meetings and email) for a de-identified list of individual employees.
* [**Meeting queries**](meeting-queries.md) - Use to analyze the relationship between different meeting attributes, such as size or duration, subject line keywords, double-booked hours, and multitasking hours.
* [**Group-to-group queries**](group-to-group-queries.md) - See how a team invested their collaboration time with other teams within and outside of the organization. You can define a team in various ways, with any organizational attribute or email domain. This query also offers alternative perspectives on collaboration.
* [**Person-to-group queries**](person-to-group-queries.md) - Helps analyze the number of interactions between a time investor and the defined collaboration team, or to analyze only those collaboration activities initiated by the specified time investor. You can define the person and collaborator team or teams in a variety of ways, with any organizational attribute or email domain.
* [**Peer comparison queries**](comparison-query.md) - Helps identify people whose collaboration patterns differ as compared to their peers. The query includes the measured employees, their specified metrics, and their peer group's averages for those metrics. You can compare individuals with others who share the same manager, with their direct reports, or even with a custom peer group as defined with organizational attributes.
* **Network queries** - Use [Network person queries](ona-person-query.md) and [Network person-to-person queries](ona-person-to-person-query.md) to find out who the best-connected people in your company, division, or group are, which is based on collaboration data. After you learn who your influencers are, you can act on the likelihood that these people can effectively connect within or across groups and become efficient drivers of change.

### Query templates

In addition to the templates, the advanced insights app also includes the following query templates.

* **Domain collaboration** - Analyzes collaboration patterns with external domains.
* **Standard meeting query** - Analyzes meetings by using the available base meeting query metrics.
* **Standard person query** - Provides all base metrics available for a person query.
* **Hourly collaboration** - Analyzes meeting, email, instant-message, and call activity by hour of the day.
* **Person query for surveys** - Combines survey data and Viva Insights data for exporting to an analysis tool of your choice, such as Power BI. Survey data from Qualtrics can be integrated with Viva Insights data. For details, see [Qualtrics integration](../use/qualtrics.md).

## Meeting exclusions

You define meeting exclusions to exclude types of meetings from analysis (such as all-day training meetings) where their inclusion might skew query results. You can select between the default meeting exclusion rules or create custom rules that match your company's meeting conventions.

See [Meeting exclusions](meeting-exclusions-intro.md) for details.

## Attendee exclusions

You can use the responses by meeting invitees to optionally exclude them from analysis. For example, invitees who accepted a meeting invitation as "Tentative" would normally be included in analysis by default. By adding an attendee exclusion, you can explicitly exclude them. In this way, creating attendee exclusions lets you effectively redefine "meeting attendance."

See [Attendee exclusions](attendee-exclusion-rules.md) for details.

## Data time limit

The historical data that queries and reports use is time limited. You can run queries only on data from the last 27 months. This 27-month period is a _rolling window_. After the first 27 months of [Microsoft 365 data](../use/office-365-data.md) is uploaded and processed in Viva Insights, it refreshes each week. This means the 27-month extent of data that you can query advances by one week to include the preceding 27 months.

However, historical query results that have already been run remain available, even after the data in the query results passes the 27-month limit.

## Related topics

* [Templates](../Tutorials/Power-bi-templates.md)
* [View, download, and export query results](../use/view-download-and-export-query-results.md)
* [Glossary](../Use/Glossary.md)
* [Metric descriptions](../Use/Metric-definitions.md)
