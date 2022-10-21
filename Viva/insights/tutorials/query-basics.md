---
ROBOTS: NOINDEX,NOFOLLOW
title: Query overview
description: Advanced insights with Viva Insights offers a number of queries for custom data analysis
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

# Queries overview

The Query designer offers a few different custom query options, including: [Person](#person-query), [Meeting](#meeting-query), [Group-to-group](#group-to-group-query), [Person-to-group](#person-to-group-query), [Peer comparison](#peer-comparison-query), and [Network](#network-queries) queries. Each query type can help you investigate and answer specific business questions. The different query types give you the flexibility to look at data from multiple perspectives and generate powerful insights. You can also combine output from two different queries to gain even more in-depth insights.

With these queries, you can:

* Select as many or as few metrics as you need, for any population or time range.
* Customize metrics with a broad range of interaction details.
* Get your data in a clean and easy-to-use format that can take your analysis to the next level.

## Time limit for querying data

The historical data on which queries are run is time limited: You can run queries only on data that is no older than 27 months. This 27-month period is a _rolling window_. This means that, after you have 27 months of [Microsoft 365 data](/viva/insights/use/office-365-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) data, as the data is refreshed each week, the 27-month extent of data that you can query advances by one week to include only the preceding 27 months.

The results of any queries that you've already run remain available to you, even after the data that was queried to produce those results passes the 27-month limit.

## Capacity model

You can subscribe a tenant to using the the advanced insights app through the Capacity model where the tenant consumes capacity units based on their volume of query usage.

The appearance and behavior of the pages for creating and running queries and of the query results page will depend on whether your tenant is subscribed to the Workplace Analytics SKU or to the Viva Insights SKU.

For more details, see [Capacity model](/viva/insights/tutorials/consump-model?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

## Query types

You can run the following types of queries in Query designer.

### Person query

Use a person query when you want to find broad trends in the organization by looking at aggregated metrics for a group of people.

Person query results show a de-identified list of the productivity metrics (such as time in meetings and email) of each measured employee. Each row of data represents one person and you can select to aggregate the results by day, week, or month.

With a person query you can compare across individual activities and attributes, such as:

* Time-use metrics
* Organizational attributes

See [Person queries](/viva/insights/Tutorials/person-queries?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) to learn more.

### Meeting query  

Use a meeting query when you want to understand the relationship between different meeting attributes.

With a meeting query you can compare across meeting attributes, such as:

* Size or duration
* Subject line keywords
* Double-booked or multitasking rates
* Meeting organizer attributes

See [Meeting queries](/viva/insights/Tutorials/meeting-queries?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) to learn more.

### Group-to-group query

Use a group-to-group query when you want to understand how one team invested their collaboration time with other teams within and outside of the organization.

For this query type, you can define a team in a variety of ways, with any organizational attribute or email domain. This enables you to answer questions such as:

* How did _Sales managers_ allocate their time between all external _customer domains_ (companies)?
* How much time did _Benefits analysts_ spend with _individual contributors_ in each _region_?
* How did _Corporate VPs_ allocate their time to _managers_ by _business unit_?

Group-to-group queries also offer alternative perspectives on collaboration. Rather than allocating collaboration hours across other teams, you can analyze the number of interactions between the teams, or analyze only those collaboration activities initiated by the “time giver” team.

See [Group-to-group queries](/viva/insights/Tutorials/group-to-group-queries?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) to learn more.

### Person-to-group query

Use a person-to-group query to help you understand how individuals invested their time with one or more collaborator teams within and outside of the organization.

As with a group-to-group query, you can define the person (or time investor) and that person's collaborator team or teams in a variety of ways, with any organizational attribute or email domain.

You can choose to analyze the number of interactions between a time investor and the defined collaboration team, or to analyze only those collaboration activities initiated by the specified time investor.

See [Person-to-group queries](/viva/insights/Tutorials/person-to-group-queries?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) to learn more.

### Peer comparison query

The peer comparison query helps you identify people whose collaboration patterns differ as compared to their peers. The query includes the measured employees, their specified metrics, and their peer group's averages for those metrics.

You can compare individuals with others who share the same manager, with their direct reports, or even with a custom peer group as defined with organizational attributes.

See [Peer comparison queries](/viva/insights/Tutorials/comparison-query?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) to learn more.

### Network queries

You can use Network queries in the advanced insights app to find out who the best-connected people are in your company, division, or group based on collaboration data. After you learn who your influencers are, you can act on the likelihood that these people can effectively connect within or across groups and become efficient drivers of change.

See [Network person queries](/viva/insights/tutorials/ona-person-query?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) and [Network person-to-person queries](/viva/insights/tutorials/ona-person-to-person-query?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) for details.

## Meeting exclusions

You can use meeting exclusions to exclude meetings that fall outside relevant norms for the data. You can select between the default meeting exclusion rules or create custom rules that match your company's meeting conventions.

See [Meeting exclusions](/viva/insights/Tutorials/meeting-exclusions-intro?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) to learn more.

## Business scenario

An analyst might start by looking at a person query to see trends of employees across the company related to meeting collaboration.

If the metrics show indications of poor meeting behavior, such as too many long meetings, the analyst could create a meeting query to investigate specific meetings in depth to uncover causes of the poor meeting behavior.

Additionally, the analyst could create a group query to identify the groups involved in those meetings and further investigate potential causes that could be addressed. Finally, to address the problem, the analyst could work with a program to set up an improvement plan. See [Plan walkthrough](/viva/insights/Tutorials/solutionsv2-intro?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) to learn more.

You can create queries in the following ways:

* Edit and use a [Query template](#query-templates).
* Create your own custom query.
* Open and edit a previously run query.

When you create a new query or edit an existing query, you can select the metrics to include and customize. You can also use filters to narrow the results and focus in on specific data.

![Customize metrics.](../Images/WpA/Use/Customize-attributes-and-metrics.png)

## Query templates

The advanced insights app includes a number of predefined query templates to help you get started with the Query designer. For details, see [Templates](/viva/insights/tutorials/power-bi-intro?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

* **Domain collaboration** analyzes collaboration patterns with external domains.
* **Standard meeting query** analyzes meetings by using the available base meeting query metrics.
* **Standard person query** analyzes collaboration patterns by using the available base person query metrics.
* **Hourly collaboration** analyzes meeting, email, instant-message, and call activity by hour of the day.

## Videos

The following videos were used to train analysts on how to run queries.

>[!Note]
>These videos were recorded before the new [Query designer](/viva/insights/tutorials/query-designer?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) was available.

### A week in the life  

The _A week in the life_ video demonstrates how to work with a [Person query](/viva/insights/tutorials/person-queries?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

<iframe src="https://player.vimeo.com/video/434889941" width="580" height="512" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

### Expensive meetings

The _Expensive meetings_ video demonstrates how to work with a [Meeting query](meeting-queries.md). 

<iframe src="https://player.vimeo.com/video/434889528" width="580" height="512" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

## Related topics

* [Templates](../Tutorials/Power-bi-templates.md)
* [Glossary](../Use/Glossary.md)
* [Metric descriptions](../Use/Metric-definitions.md)
