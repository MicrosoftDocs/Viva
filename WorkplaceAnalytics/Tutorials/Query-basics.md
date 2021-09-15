---

title: Workplace Analytics query overview
description: Workplace Analytics offers a number of queries for custom data analysis
author: paul9955
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
ms.prod: wpa
manager: scott.ruble
audience: Admin
---

[![Viva announcement](../images/viva-banner-2.png)](https://www.microsoft.com/microsoft-viva/insights)

# Queries overview

The Query designer in Workplace Analytics offers a few different custom query options, including: [Person](#person-query), [Meeting](#meeting-query), [Group-to-group](#group-to-group-query), [Person-to-group](#person-to-group-query), [Peer comparison](#peer-comparison-query), and [Network](#network-queries) queries. Each query type can help you investigate and answer specific business questions. The different query types give you the flexibility to look at data from multiple perspectives and generate powerful insights. You can also combine output from two different queries to gain even more in-depth insights.

With these queries, you can:

* Select as many or as few metrics as you need, for any population or time range.
* Customize metrics with a broad range of interaction details.
* Get your data in a clean and easy-to-use format that can take your analysis to the next level.

## Time limit for querying data 

The historical data on which queries are run is time limited: You can run queries only on data that is no older than 27 months. This 27-month period is a _rolling window_. This means that, after you have 27 months of [Microsoft 365 data](../use/office-365-data.md) data, as the data is refreshed each week, the 27-month extent of data that you can query advances by one week to include only the preceding 27 months.

The results of any queries that you've already run remain available to you, even after the data that was queried to produce those results passes the 27-month limit.

<!-- REMOVING THIS SECTION FOR NOW. PUTTING IT IN A HIDDEN TOPIC, QUERY-BASICS2.MD, WHILE THESE FEATURES ARE ADDED, ONE BY ONE, IN AUGUST-SEPTEMBER 2021:  

## Billing model differences

Tenants subscribe to Workplace Analytics through one of the following billing models:

* **Consumption model** &ndash; The tenant pays Microsoft a fee that is based on the volume of query usage.
* **Per-user-per-month (PUPM) model** &ndash; The tenant pays Microsoft a monthly fee that is based on the number of licensed users.

Your tenant's choice of billing model affects the appearance and behavior of the pages for creating queries (such as [person queries](person-queries.md) and [meeting queries](meeting-queries.md)) and the [query results](../use/view-download-and-export-query-results.md) page. Analysts will see the following differences:

### For analysts in consumption-model tenants

In this model, there is no minimum monthly licensing cost for your organization; rather, all fees are based on the running of queries. Each query that you run consumes a number of "units," based on the following factors: the number of measured employees being analyzed, the number of weeks of data included in the query output for each measured employee, the number of base metrics in the query, and which base metrics are used. (Metrics are arranged into "price tiers"; metrics in higher price tiers consume more units than metrics in lower price tiers. For more information, see [Consumption model details](#consumption-model-details).)

As you design a query, Workplace Analytics uses these factors to calculate the cost of the query. Within the query editor, you can see the estimated number of units that the query &ndash; in its current state &ndash; would consume. This number is updated as you edit the query:

![units per query](../images/wpa/tutorials/conmod-credits-2.png)

IN QUERY-BASICS2 UPDATE THIS IMAGE TO INCLUDE THE  WALLET

In the bar above the estimated query cost, you can see how many units remain in your tenant's account. Analysts can continue to run queries as long as this balance remains above zero units.


#### Consumption model details

OUTDATED: REPLACE WITH QB2 CONTENT

In a consumption-model tenant, queries consume "units" as they are run. Unit calculation is as follows:

**units consumed in a query** = **number of user-weeks analyzed/1000** x ((**P1** * **N1**) + (**P2** * **N2**) + (**P3** * **N3**))

In this formula, **Px** is the **price tier** of a metric and **Nx** is the **number of base metrics** for that tier that are included in the query. The terms in this formula are further described here:

* **user-weeks analyzed** is defined as the number of historical weeks of analysis that are available for each employee in the population that you are analyzing. The population size is the number of employees that meet the _Filter group_ criteria that are defined for the query. Your choice of a time period by which to aggregate metrics (by week or by month) does not affect your charges for the query.

   User-weeks are additive: Let’s say your query covers the past year. If one employee is present for all 52 weeks of analysis and another is present for only the last two weeks of analysis, this counts as 54 user-weeks.

* **number of base metrics** is defined as the number of unique Workplace Analytics metrics that are included in the query. If the query includes multiple customizations of one base metric, it counts as only a single use of that base metric.

  <u>Example:</u> If a query measures Meeting hours between 8:00 and 9:00 AM and Meeting hours between 9:00 and 10:00 AM, this counts as only a single metric, Meeting hours.

  A “price tier” is associated with each metric, as described in the following item. 

* **price tier** is the rate at which a query consumes units. The higher the tier, the more units are consumed:

| Tier | Metric used in the query | Units |
| ---- | ------------ | -------------- |
| 1    | Most Workplace Analytics metrics &ndash; for example, collaboration hours, internal network size, low quality meeting hours, and 65 other basic metrics | 1.25 |
| 2    | Advanced Workplace Analytics metrics &ndash; The metrics in tier 2 are the [ONA metrics](../use/metric-definitions.md#organizational-network-analysis-ona-metrics) of Workplace Analytics. | 2.25 |
| 3    | Workplace Analytics metrics with [CRM data](crm-queries.md) &ndash; namely, external-facing metrics that calculate across CRM contacts. If you use CRM attributes to create filter customizations for a metric (for example, the Meeting hours metric where at least one attendee has _AccountName_ = _Contoso_), the metric is in tier 3. If a single metric has more than one customization and at least one of them uses a CRM attribute, the metric is in tier 3. | 6.00 |

##### Charges for recurring queries

Workplace Analytics uses this formula to calculate units consumed every time that you run a query except for recurring ([auto-refresh](query-auto-refresh.md)) queries. The first time a recurring query runs, the formula uses the actual number of user-weeks that the query definition specifies. In subsequent runs of the query, the formula automatically uses one week as the query duration. You are not charged for any historical data that has already been analyzed.

However, the queried population can change in between query refresh runs. For example, there might be 1,000 licensed employees when you first sets up a "last four weeks" auto-refresh query. Before the query runs again, another 2000 employee licenses are approved. Subsequently, the refresh query will include:

* **A:** weeks 2 to 4 for the original population

* **B:** week 5 for the original population

* **C:** weeks 2 to 5 for the newly licensed population

Of these, the refresh query should charge for **B** and **C** because neither were included in the original query run, but it should not charge for **A**, which duplicates the data that's returned in the original query.

##### No additional charges

REPLACE WITH QB2 CONTENT

No additional units are charged for the following:

* Workplace Analytics licenses that are assigned. You are charged for query volume, which is independent of licensing.  
* Your use of the following Workplace Analytics features: [plans](solutionsv2-intro.md), [My Team in Viva Insights](../use/viva-insights-my-team.md), [My organization in Viva Insights](../use/viva-insights-my-org.md), [Opportunities scan](use/solutions-scan.md), [Explore pages](../use/explore-intro.md).
* Your choice of a query-results visualization method, such as Excel, PowerPoint, Power BI, or another visualization tool.
* Your use of organizational attributes in queries.
* The number of analysts who run queries in your organization.

### For analysts in PUPM-model tenants

The query-creation pages show analysts no information about query usage or tenant billing. This is because, in the PUPM model, the design and use of queries has no effect on the amount that your organization is billed. Billing charges accrue behind the scenes, independently of query usage:

![PUPM: no units shown](../images/wpa/tutorials/pupm-no-credits-2.png)

### Results page

The **Queries** > **Results** page shows additional information if the consumption model is in use at your tenant:

* **PUPM-model tenants** &ndash; Analysts in a PUPM-model tenant can use the **Queries** > **Results** page as described in [View, download, and export query results](../use/view-download-and-export-query-results.md).

* **Consumption-model tenants** &ndash; For analysts in a consumption-model tenant, the **Results** page shows additional information. On this page, the **Query Cost** column shows the number of units charged to each query. Select the ![More information](../images/wpa/tutorials/more-info-50.png) (more information) option to see the details of this charge, namely the number of users analyzed, the number of base metrics used, the price tier of each metric, and the analysis period:

   ![Query results page](../images/wpa/tutorials/query-results-new-col.png)

ADD INFO ABOUT ANALYST USAGE 
ONLY ADMIN CAN DOWNLOAD THIS REPORT 

1. COMPLETE DOCS WILL CONTAIN EVERYTHING: TO GO LIVE ON 10/1
2. QB2 WITH ANALYST USAGE PART CAN GO LIVE NOW 
 
NEED ANNOUNCEMENT TO THE TEAM ABOUT WHAT WE'RE RELEASING : "WHAT IS THE CHANGE" REFLECTS THIS DOCUMENTATION. NISHANT WILL MAKE THIS AND SEND TO ME FOR REVIEW. 

-->

## Query types

You can find these queries on the **Analyze** > **Queries** page of Workplace Analytics.

### Person query

Use a person query when you want to find broad trends in the organization by looking at aggregated metrics for a group of people.

Person query results show a de-identified list of the productivity metrics (such as time in meetings and email) of each measured employee. Each row of data represents one person and you can select to aggregate the results by day, week, or month.

With a person query you can compare across individual activities and attributes, such as:

* Time-use metrics
* Organizational attributes

See [Person queries](../Tutorials/person-queries.md) to learn more.

### Meeting query  

Use a meeting query when you want to understand the relationship between different meeting attributes.

With a meeting query you can compare across meeting attributes, such as:

* Size or duration
* Subject line keywords
* Double-booked or multitasking rates
* Meeting organizer attributes

See [Meeting queries](../Tutorials/meeting-queries.md) to learn more.

### Group-to-group query

Use a group-to-group query when you want to understand how one team invested their collaboration time with other teams within and outside of the organization.

For this query type, you can define a team in a variety of ways, with any organizational attribute or email domain. This enables you to answer questions such as:

* How did _Sales managers_ allocate their time between all external _customer domains_ (companies)?
* How much time did _Benefits analysts_ spend with _individual contributors_ in each _region_?
* How did _Corporate VPs_ allocate their time to _managers_ by _business unit_?

Group-to-group queries also offer alternative perspectives on collaboration. Rather than allocating collaboration hours across other teams, you can analyze the number of interactions between the teams, or analyze only those collaboration activities initiated by the “time giver” team.

See [Group-to-group queries](../Tutorials/group-to-group-queries.md) to learn more.

### Person-to-group query

Use a person-to-group query to help you understand how individuals invested their time with one or more collaborator teams within and outside of the organization.

As with a group-to-group query, you can define the person (or time investor) and that person's collaborator team or teams in a variety of ways, with any organizational attribute or email domain.

You can choose to analyze the number of interactions between a time investor and the defined collaboration team, or to analyze only those collaboration activities initiated by the specified time investor.

See [Person-to-group queries](../Tutorials/person-to-group-queries.md) to learn more.

### Peer comparison query

The peer comparison query helps you identify people whose collaboration patterns differ as compared to their peers. The query includes the measured employees, their specified metrics, and their peer group's averages for those metrics.

You can compare individuals with others who share the same manager, with their direct reports, or even with a custom peer group as defined with organizational attributes.

See [Peer comparison queries](../Tutorials/comparison-query.md) to learn more.

### Network queries

You can use Network queries in Workplace Analytics to find out who the best-connected people are in your company, division, or group based on collaboration data. After you learn who your influencers are, you can act on the likelihood that these people can effectively connect within or across groups and become efficient drivers of change.

See [Network person queries](ona-person-query.md) and [Network person-to-person queries](ona-person-to-person-query.md) for details.

## Meeting exclusions

You can use meeting exclusions to exclude meetings that fall outside relevant norms for the data. You can select between the default meeting exclusion rules or create custom rules that match your company's meeting conventions.

See [Meeting exclusions](../Tutorials/meeting-exclusions-intro.md) to learn more.

## Business scenario

An analyst might start by looking at a person query to see trends of employees across the company related to meeting collaboration.

If the metrics show indications of poor meeting behavior, such as too many long meetings, the analyst could create a meeting query to investigate specific meetings in depth to uncover causes of the poor meeting behavior.

Additionally, the analyst could create a group query to identify the groups involved in those meetings and further investigate potential causes that could be addressed. Finally, to address the problem, the analyst could work with a program to set up an improvement plan. See [Plans: walkthrough](../Tutorials/solutionsv2-intro.md) to learn more.

You can create queries in the following ways:

* Edit and use a [Query template](#query-templates).
* Create your own custom query.
* Open and edit a previously run query.

When you create a new query or edit an existing query, you can select the metrics to include and customize. You can also use filters to narrow the results and focus in on specific data.

![Customize metrics](../Images/WpA/Use/Customize-attributes-and-metrics.png)

## Query templates

Workplace Analytics includes a number of predefined query templates to help you get started with the Query designer. For details, see [Templates](power-bi-intro.md).

* **Domain collaboration** analyzes collaboration patterns with external domains.
* **Standard meeting query** analyzes meetings by using the available base meeting query metrics.
* **Standard person query** analyzes collaboration patterns by using the available base person query metrics.
* **Hourly collaboration** analyzes meeting, email, instant-message, and call activity by hour of the day.

## Videos

The following videos were used to train analysts on how to run queries in Workplace Analytics.

>[!Note]
>These videos were recorded before the new [Query designer](query-designer.md) was available.

### A week in the life  

The _A week in the life_ video demonstrates how to work with a [Person query](person-queries.md).

<iframe src="https://player.vimeo.com/video/434889941" width="580" height="512" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

### Expensive meetings

The _Expensive meetings_ video demonstrates how to work with a [Meeting query](meeting-queries.md). 

<iframe src="https://player.vimeo.com/video/434889528" width="580" height="512" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

## Related topics

* [Templates](../Tutorials/Power-bi-templates.md)
* [Workplace Analytics glossary](../Use/Glossary.md)
* [Metric descriptions](../Use/Metric-definitions.md)
