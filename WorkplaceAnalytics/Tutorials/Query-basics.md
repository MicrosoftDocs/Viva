---

title: Workplace Analytics query overview
description: Workplace Analytics offers a number of flexible queries for custom data analysis
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
ms.prod: wpa
manager: scott.ruble
audience: Admin
---

[![Viva announcement](../images/viva-banner-2.png)](https://www.microsoft.com/microsoft-viva/insights)

# Queries overview

Workplace Analytics has a few different query options, including: **Person**, **Meeting**, **Group-to-group**, **Person-to-group**, **Peer comparison**, and **Network queries**. Each query type can help answer specific questions that you want to investigate. The different query types give you flexibility to look at data from multiple perspectives and generate powerful insights. You can also use the query types together to gain even more in-depth insights.

![Ways to query data](../Images/WpA/Use/ways-to-query-data.png)

With these queries, you can:

* Select as many or as few metrics as you need, for any population or time range.
* Customize metrics with a broad range of interaction details.
* Get your data in a clean and easy-to-use format that can take your analysis to the next level.

### Time limit for querying data 

<!-- ORIGINAL: The historical data on which queries are run is time limited: You can run queries only on data that is no older than 27 months. This 27-month period is a rolling window. This means that—after you have 27 months of data—with each month that passes, the limit of data that you can query (which lies 27 months in the past) advances by one month. -->

The historical data on which queries are run is time limited: You can run queries only on data that is no older than 27 months. This 27-month period is a _rolling window_. This means that&mdash; after you have 27 months of data&mdash;as [Microsoft 365 data](../use/office-365-data.md) is refreshed each week, the 27-month extent of data that you can query advances by one week to include the preceding 27 months.

The results of any queries that you've already run remain available to you, even after the data that was queried to produce those results passes the 27-month limit.

## Person query

Use a person query when you want to find broad trends in the organization by looking at aggregated metrics for a group of people.

Person query results show a de-identified list of the productivity metrics (such as time in meetings and email) of each measured employee. Each row of data represents one person and you can select to aggregate the results by day, week, or month.

With a person query you can compare across individual activities and attributes, such as:

* Time-use metrics
* Organizational attributes

See [Person queries](../Tutorials/person-queries.md) to learn more.

## Meeting query  

Use a meeting query when you want to understand the relationship between different meeting attributes.

With a meeting query you can compare across meeting attributes, such as:

* Size or duration
* Subject line keywords
* Double-booked or multitasking rates
* Meeting organizer attributes

See [Meeting queries](../Tutorials/meeting-queries.md) to learn more.

## Group-to-group query

Use a group-to-group query when you want to understand how one team invested their collaboration time with other teams within and outside of the organization.

For this query type, you can define a team in a variety of ways, with any organizational attribute or email domain. This enables you to answer questions such as:

* How did _Sales managers_ allocate their time between all external _customer domains_ (companies)?
* How much time did _Benefits analysts_ spend with _individual contributors_ in each _region_?
* How did _Corporate VPs_ allocate their time to _managers_ by _business unit_?

Group-to-group queries also offer alternative perspectives on collaboration. Rather than allocating collaboration hours across other teams, you can analyze the number of interactions between the teams, or analyze only those collaboration activities initiated by the “time giver” team.

See [Group-to-group queries](../Tutorials/group-to-group-queries.md) to learn more.

## Person-to-group query

Use a person-to-group query to help you understand how individuals invested their time with one or more collaborator teams within and outside of the organization.

As with a group-to-group query, you can define the person (or time investor) and that person's collaborator team or teams in a variety of ways, with any organizational attribute or email domain.

You can choose to analyze the number of interactions between a time investor and the defined collaboration team, or to analyze only those collaboration activities initiated by the specified time investor.

See [Person-to-group queries](../Tutorials/person-to-group-queries.md) to learn more.

## Peer comparison query

The peer comparison query helps you identify people whose collaboration patterns differ as compared to their peers. The query includes the measured employees, their specified metrics, and their peer group's averages for those metrics.

You can compare individuals with others who share the same manager, with their direct reports, or even with a custom peer group as defined with organizational attributes.

See [Peer comparison queries](../Tutorials/comparison-query.md) to learn more.

## Network queries

You can use the Organizational network analysis (ONA) queries in Workplace Analytics to find out who are the best-connected people in your company, division, or group based on collaboration data. After you learn who your influencers are, you can act on the likelihood that these people can effectively connect within or across groups and become efficient drivers of change.

See [ONA person queries](ona-person-query.md) and [ONA person-to-person queries](ona-person-to-person-query.md) for more details.
## Meeting exclusions

You can use meeting exclusions to exclude meetings that fall outside relevant norms from the queries. You can select between the default meeting exclusion rules or create custom rules that match your company's meeting conventions.

See [Meeting exclusions](../Tutorials/meeting-exclusions-intro.md) to learn more.

## Business scenario

An analyst might start by looking at a person query to see trends of employees across the company related to meeting collaboration.

If the metrics show indications of poor meeting behavior, such as too many long meetings, the analyst could create a meeting query to investigate specific meetings in depth to uncover causes of the poor meeting behavior.

Additionally, the analyst could create a group query to identify the groups involved in those meetings and further investigate potential causes that could be addressed. Finally, to address the problem, the analyst could work with a program to set up an improvement plan. See [Plans: walkthrough](../Tutorials/solutionsv2-intro.md) to learn more.

You can create queries in the following ways:

* Edit and use a [predefined query template](#predefined-query-templates).
* Create your own custom query.
* Open and edit a previously run query.

When you create a new query or edit an existing query, you can select the metrics to include and customize. You can also use filters to narrow the results and focus in on specific data.

![Customize metrics](../Images/WpA/Use/Customize-attributes-and-metrics.png)

## Predefined query templates

Workplace Analytics includes the following predefined query templates to help you get started with queries. In addition to these, a number of Power BI templates are also available. For details, see [Power BI templates](power-bi-intro.md).

* **Domain collaboration** analyzes collaboration patterns with external domains.
* **Standard meeting query** analyzes meetings by using the available base meeting query metrics.
* **Standard person query** analyzes collaboration patterns by using the available base person query metrics.
* **Hourly collaboration** analyzes meeting, email, instant-message, and call activity by hour of the day.

## Videos

The videos in this section were used in a bootcamp for training analysts in how to run queries in Workplace Analytics.

### A week in the life  

The _A week in the life_ video demonstrates how to work with a [person query](person-queries.md).

<iframe src="https://player.vimeo.com/video/434889941" width="580" height="512" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

### Expensive meetings

The _Expensive meetings_ video demonstrates how to work with a [meeting query](meeting-queries.md). 

<iframe src="https://player.vimeo.com/video/434889528" width="580" height="512" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

## Related topics

* [Power BI templates](../Tutorials/Power-bi-templates.md)
* [Workplace Analytics glossary](../Use/Glossary.md)
* [Metric descriptions](../Use/Metric-definitions.md)