---
# Metadata Sample
# required metadata

title: Workplace Analytics query overview
description: Workplace Analytics offers a number of flexible queries for custom data analysis.
author: madehmer
ms.author: madehmer
ms.date: 11/12/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---
# Queries overview

You can create four types of queries in Workplace Analytics: **Person**, **Meeting**, **Group-to-group**, and **Person-to-group**. Each query type can help answer specific questions you want to investigate. The different query types give you flexibility to look at data from multiple perspectives and generate powerful insights. You can also use the query types together to gain even more in-depth insights.

![Ways to query data](../Images/WpA/Use/Ways-to-query-data-Create-queries.png)

With these queries, you can:

* Select as many or as few metrics as you need, for any population or time range.
* Customize metrics with a broad range of interaction details.
* Get your data in a clean and easy-to-use format that can take your analysis to the next level.

## Person query

Use a person query when you want to understand the relationship between a person’s organizational attributes (their team, level, or location) and how they use their time, or when you want to know how one aspect of a person’s use of time might influence another aspect of their time use.

With a person query you can compare across individual activities and attributes, such as:

* Time-use metrics
* Organizational attributes

## Meeting query  

Use a meeting query when you want to understand the relationship between different meeting attributes.

With a meeting query you can compare across meeting attributes, such as:

* Size or duration
* Subject line keywords
* Double-booked or multitasking rates
* Meeting organizer attributes

## Group-to-group query

Use a group-to-group query when you want to understand how one team invested their collaboration time across other teams within and outside of the organization.

For this query type, you can define a team in a variety of ways, with any organizational attribute or email domain. This enables you to answer questions such as:

* How did _Sales managers_ allocate their time between all external _customer domains_ (companies)?
* How much time did _Benefits Analysts_ spend with _individual contributors_ in each _region_?
* How did _Corporate VPs_ allocate their time to _managers_ by _business unit_?

Group-to-group queries also offer alternative perspectives on collaboration. Rather than allocating collaboration hours across other teams, you can analyze the number of interactions between the teams, or analyze only those collaboration activities initiated by the “time giver” team.

## Person-to-group query

Use a person-to-group query to help you understand how individuals invested their time with one or more collaborator teams within and outside of the organization.

Similar to a group-to-group query, you can define the person (or time investor) and that person's collaborator team or teams in a variety of ways, with any organizational attribute or email domain.

You can choose to analyze the number of interactions between a time investor and the defined collaboration team, or analyze only those collaboration activities initiated by the specified time investor.

## Meeting exclusions

You can use Meeting exclusions to exclude meetings that fall outside relevant norms from the queries. You can select between the default meeting exclusion rules or create custom rules that match your company's meeting conventions.

### Related topics

[Understand meeting exclusions](../Use/Understand-meeting-exclusions.md)

[Create custom meeting exclusions rule](../Use/Create-custom-meeting-exclusions-rules.md)

## Business scenario

An analyst may start by looking at a [Person query](#person-query) to see trends of employees across the company related to meeting collaboration.

If the metrics show indications of poor meeting behavior, such as too many long meetings, the analyst could create a [Meeting query](#meeting-query) to investigate specific meetings in depth to uncover causes of the poor meeting behavior.

Additionally, the analyst could create a [Group query](#group-query) to identify the groups involved in those meetings and further investigate potential causes that could be addressed.

There are three ways to create queries:

* Use and edit pre-defined query templates
* Create custom queries from scratch
* Open and edit a previously run query

When you create or edit a query, you will select the metrics that you want to include (many can be customized), and you can use filters to narrow the results and drill down on specific data of interest.

![Customize attributes and metrics](../Images/WpA/Use/Customize-attributes-and-metrics-Create-queries.png)

## Pre-defined query templates

Workplace Analytics includes a number of pre-defined query templates to help you get started with using queries, such as the following.

* **Collaboration overload** is a Power BI template that identifies collaboration patterns
* **Manager impact** is a Power BI template that analyzes manager trends
* **Build focus hours** finds groups that have the lowest amount of focus time
* **Meetings attendees query** analyzes meeting hours by the number of attendees
* **Meetings day query** analyzes meeting hours by day of the week
* **Meetings duration query** analyzes meeting hours by duration
* **Meetings start time query** analyzes meeting hours by time of day
* **Protect after hours** finds groups that collaborate the most outside of work hours
* **Reduce meeting hours** finds groups that are overwhelmed by meetings
* **Standard query** provides all base metrics available for a person query

### Related topics

[Person queries](../Tutorials/Person-queries.md)

[Meeting queries](../Tutorials/meeting-queries.md)

[Group-to-group queries](../Tutorials/group-to-group-queries.md)

[Person-to-group queries](../Tutorials/person-to-group-queries.md)

[Workplace Analytics glossary](../Use/Glossary.md)

[Metric descriptions](../Use/Metric-definitions.md)
