---

ROBOTS: NOINDEX,NOFOLLOW
title: Query overview
description: Viva Insights offers a number of flexible queries for custom data analysis
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

<!-- NOTE: This topic exists only for the private preview that Nishant had going during Aug.-Sept. 2021. Now that consumption-model billing has gone GA (Oct 1), we should be able to delete this. Confirm first with Nishant that no preview customers might need it still. -->

# Queries overview

The advanced insights app has a few different query options, including: **Person**, **Meeting**, **Group-to-group**, **Person-to-group**, **Peer comparison**, and **Network queries**. Each query type can help answer specific questions that you want to investigate. The different query types give you flexibility to look at data from multiple perspectives and generate powerful insights. You can also use the query types together to gain even more in-depth insights.

![Ways to query data.](../Images/WpA/Use/ways-to-query-data.png)

With these queries, you can:

* Select as many or as few metrics as you need, for any population or time range.
* Customize metrics with a broad range of interaction details.
* Get your data in a clean and easy-to-use format that can take your analysis to the next level.

## Time limit for querying data 

The historical data on which queries are run is time limited: You can run queries only on data that is no older than 27 months. This 27-month period is a _rolling window_. This means that&mdash; after you have 27 months of data&mdash;as [Microsoft 365 data](../use/office-365-data.md) is refreshed each week, the 27-month extent of data that you can query advances by one week to include the preceding 27 months.

The results of any queries that you've already run remain available to you, even after the data that was queried to produce those results passes the 27-month limit.

## Billing model differences

Tenants subscribe to the advanced insights app through one of the following billing models:

* **Consumption model** &ndash; The tenant pays Microsoft a fee that is based on the volume of query usage.
* **Per-user-per-month (PUPM) model** &ndash; The tenant pays Microsoft a monthly fee that is based on the number of licensed users.

<!-- CURRENT (TEMPORARY) TEXT: -->

Your tenant's choice of billing model affects the page for creating [person queries](person-queries.md). Analysts will see the following differences:

<!-- ULTIMATE (GA) TEXT, COMMENTED OUT FOR NOW: -->
<!--
Your tenant's choice of billing model affects the analyst experience as follows:

* The appearance and behavior of the page for creating queries (such as  [person queries](person-queries.md) and [meeting queries](meeting-queries.md)) will differ.
* The [query results](../use/view-download-and-export-query-results.md) page will offer additional functionality.

Analysts will see the following differences: -->

### For analysts in consumption-model tenants

In this model, there is no minimum monthly licensing cost for your organization; rather, all fees are based on the running of queries. Each query that you run consumes a number of "units," based on the following factors:

* The number of measured employees being analyzed.
* The number of weeks of data included in the query output for each measured employee.
* The number of base metrics in the query.
* What base metrics are used, which are arranged into "price tiers"; metrics in higher price tiers consume more units than metrics in lower price tiers. For more information, see [Capacity model details](#capacity-model-details).

As you design a query, the advanced insights app uses these factors to calculate the cost of the query. Within the query editor, you can see the estimated number of units that the query &ndash; in its current state &ndash; would consume. This number is updated as you edit the query:

![query estimate](../images/wpa/tutorials/query-estimate-1.png)

#### Capacity model details

In a capacity-model tenant, queries consume "units" as they are run. Usage calculation is as follows:

**units consumed** = **A** * **B** * **C** * **D**

The terms in this formula are as follows:

* **A = users**

   This is the number of users whom the query will analyze. Also see [User scope in usage calculations](#user-scope-in-usage-calculations).

* **B = metrics**

   This is the number of unique base metrics that are used at each price tier in the query. If the query includes more than one customization of one base metric, it counts as only a single use of that metric.

  <u>Example:</u> If a query measures Meeting hours between 8:00 and 9:00 AM and Meeting hours between 9:00 and 10:00 AM, this counts as only a single metric, Meeting hours.

  A “price tier” is associated with each metric, as described in the following item.

* **C = price-tier cost**

<a name="price-tier-anchor"></a>**Price tier costs**

   This is the cost of the price tier that is in use for a metric in the query. A query consumes units at this rate. The higher the tier, the more units are consumed:

   | Tier | Metric used in the query | Units |
   | ---- | ------------ | -------------- |
   | 1    | Most Viva Insights metrics &ndash; for example, collaboration hours, internal network size, low quality meeting hours, and 65 other basic metrics | 1.25 |
   | 2    | Advanced Viva Insights metrics &ndash; specifically, the [Network query metrics](../tutorials/ona-metrics.md). | 2.25 |
   | 3    | The Viva Insights metrics with [CRM data](crm-queries.md) &ndash; namely, external-facing metrics that calculate across CRM contacts. If you use CRM attributes to create filter customizations for a metric (for example, the Meeting hours metric where at least one attendee has _AccountName_ = _Contoso_), the metric is in tier 3. If a single metric has more than one customization and at least one of them uses a CRM attribute, the metric is in tier 3. | 6.00 |

   >[!Note]
   >If you use metrics at multiple price tiers, a subtotal is calculated for each metric and then all subtotals are added together. For example, if your query uses one metric in each of two price tiers, the total number of units consumed is **A** * **B** * **C** * **D** (for the metric on price tier 1) + **A** * **B** * **C** * **D** (for the metric on price tier 2)

* **D = weeks**

   This is the analysis period, in weeks.

#### User scope in usage calculations

As described in [Capacity model details](#capacity-model-details), the calculation is the same across all query types: **units consumed** = **A** (users) * **B** (metrics) * **C** (price-tier cost) * **D** (weeks). With this in mind, the user scope for the various query types is defined as follows:

* **Person query**: **A** (users) = the number of [measured employees](../use/glossary.md#measured-employees-define), as filtered in the query definition

* **Meeting query**: **A** (users) = the number of licensed users that are invited in the filtered meetings

* **Person-to-group query**: **A** (users) = the number of time investors

* **Group-to-group query**: **A** (users) = the number of time investors

* **Peer Comparison**: **A** (users) = the number of employees in the reference groups

* **Network: Person query**:  **A** (users) = the number of filtered measured employees in the query. Note that network metrics are charged at tier 2 (see [Price tier costs](#price-tier-anchor)).

* **Network: Person-to-person query**: User scope is determined by the number of filtered measured employees in the query. Note that network metrics are charged at tier 2 (see [Price tier costs](#price-tier-anchor)).

##### See the usage calculation for the query

On the query page, you can see how units are calculated for the query that you are defining. To see the calculation, select the tooltip:

![query cost tooltip.](../images/wpa/tutorials/query-estimate-1.png)

This opens a panel that describes the current calculation:

![query cost calculation.](../images/wpa/tutorials/query-estimate.png)

>[!Note]
>* The cost that is shown in this way is an estimate; it can vary from the query's actual cost, which can be seen after the query has been run successfully.
>* This cost calculator is not available for meeting queries.

##### Charges for recurring queries

Viva Insights uses this formula to calculate the units that are consumed whenever you run a query except for recurring ([auto-refresh](query-auto-refresh.md)) queries. The first time a recurring query runs, the formula uses the actual number of user-weeks that the query definition specifies. In subsequent runs of the query, the formula automatically uses the additional time period as the query duration. You are not charged for any historical data that has already been analyzed.

Note that the queried population can change between query refresh runs. Take the following example: There are 1,000 licensed employees when you first set up a "last four weeks" auto-refresh query. Before the query runs again, another 2000 employee licenses are approved. The first time that the query refreshes after the initial run, it will include:

* **1:** weeks 2 to 4 for the original population

* **2:** week 5 for the original population

* **3:** weeks 2 to 5 for the newly licensed population

Of these, the refresh query will charge for **2** and **3** because neither were included in the original query run, but it will not charge for **1**, which duplicates the data that was returned in the original query.

##### Charges for re-running a completed query

On the **Query designer** > **Results** page, you can locate a query that has already run, open it, edit it, and run it. This incurs a new cost, as if you were running the query for the first time. The steps to do this are as follows:

1. Open the **Query designer** > **Results** page.
2. In the list of queries, find a query whose status shows as completed, as indicated by a green check mark.
3. In the row for that query, select **More options** (the ellipsis) and then **View query**:

   ![options view query.](../images/wpa/tutorials/query-actions.png)

   This opens the page for designing that query.

4. In the query designer, change a detail about the query. For example, change **Group by** from **Week** to **Month**, and then select **Run**.

The edited query runs again. As it does, it incurs a new cost, in units, calculated as described in [Capacity model details](#capacity-model-details).

##### No additional charges

No additional units are charged for the following:

* Viva Insights licenses that are assigned. You are charged for query volume, which is independent of licensing.  
* Your use of the following the advanced insights app features: [plans](solutionsv2-intro.md), [My team in Viva Insights](../org-team-insights/teamwork-habits.md), [My organization in Viva Insights](../org-team-insights/org-trends.md), [Explore pages](../use/explore-intro.md).
* Your choice of a query-results visualization method, such as Excel, PowerPoint, Power BI, or another visualization tool.
* Your use of organizational attributes in queries.
* The number of analysts who run queries in your organization.

<!-- REMOVE THIS ENTIRE SECTION FOR NOW (AUGUST 19 2021). RETURN THIS SECTION TO THE DOC AFTER GA. -->
<!-- 

### Results page

In Query designer results, you'll see additional information if the capacity model is in use at your tenant:

* **PUPM-model tenants** &ndash; Analysts in a PUPM-model tenant can use the **Query designer** > **Results** page as described in [View, download, and export query results](../use/view-download-and-export-query-results.md).

* **Capacity-model tenants** &ndash; For analysts in a capacity-model tenant, the **Results** page shows additional information. On this page, the **Query Cost** column shows the number of units charged to each query. Select the ![More information.](../images/wpa/tutorials/more-info-50.png) (more information) option to see the details of this charge, namely the number of users analyzed, the number of base metrics used, the price tier of each metric, and the analysis period:

   ![Query cost.](../images/wpa/tutorials/query-cost.png)
-->
### View analyst usage

The **Analyst usage** report is available for download in the administrative pages of the advanced insights app. This report lists the queries that were run during a specified time period, the analysts who submitted them, and other details, including the query cost:

![Analyst usage report](../images/wpa/tutorials/usage-report-example1.png)

>[!Note]
>Only admins can download the Analyst usage report.

### To download the Analyst usage report

1. Sign in to the advanced insights app as an admin.
2. Go to the **Analyst usage** page:

   ![Download analyst usage report](../images/wpa/tutorials/analyst-usage2.png)

3. Select the time period for which you want information about query usage.
4. Select **Download**.

### For analysts in PUPM-model tenants

The query-creation pages show analysts no information about query usage or tenant billing. This is because, in the PUPM model, your organization has been billed for the usage of the product during the time of purchase:

![PUPM: no units shown](../images/wpa/tutorials/pupm-no-credits-2.png)

<!-- END OF BILLING MODEL DIFFERENCES SECTION -->

## Query types

You can run the following types of queries through the Query designer.

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

You can use the Organizational network analysis (ONA) queries in the advanced insights app to find out who are the best-connected people in your company, division, or group based on collaboration data. After you learn who your influencers are, you can act on the likelihood that these people can effectively connect within or across groups and become efficient drivers of change.

See [ONA person queries](ona-person-query.md) and [ONA person-to-person queries](ona-person-to-person-query.md) for more details.

## Meeting exclusions

You can use meeting exclusions to exclude meetings that fall outside relevant norms from the queries. You can select between the default meeting exclusion rules or create custom rules that match your company's meeting conventions.

See [Meeting exclusions](../Tutorials/meeting-exclusions-intro.md) to learn more.

## Business scenario

An analyst might start by looking at a person query to see trends of employees across the company related to meeting collaboration.

If the metrics show indications of poor meeting behavior, such as too many long meetings, the analyst could create a meeting query to investigate specific meetings in depth to uncover causes of the poor meeting behavior.

Additionally, the analyst could create a group query to identify the groups involved in those meetings and further investigate potential causes that could be addressed. Finally, to address the problem, the analyst could work with a program to set up an improvement plan. See [Plan walkthrough](../Tutorials/solutionsv2-intro.md) to learn more.

You can create queries in the following ways:

* Edit and use a [predefined query template](#predefined-query-templates).
* Create your own custom query.
* Open and edit a previously run query.

When you create a new query or edit an existing query, you can select the metrics to include and customize. You can also use filters to narrow the results and focus in on specific data.

![Customize metrics.](../Images/WpA/Use/Customize-attributes-and-metrics.png)

## Predefined query templates

The advanced insights app includes the following predefined query templates to help you get started with queries. In addition to these, a number of Power BI templates are also available. For details, see [Power BI templates](power-bi-intro.md).

* **Domain collaboration** analyzes collaboration patterns with external domains.
* **Standard meeting query** analyzes meetings by using the available base meeting query metrics.
* **Standard person query** analyzes collaboration patterns by using the available base person query metrics.
* **Hourly collaboration** analyzes meeting, email, instant-message, and call activity by hour of the day.

## Videos

The videos in this section were used in a bootcamp for training analysts in how to run queries in the advanced insights app.

### A week in the life  

The _A week in the life_ video demonstrates how to work with a [person query](person-queries.md).

<iframe src="https://player.vimeo.com/video/434889941" width="580" height="512" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

### Expensive meetings

The _Expensive meetings_ video demonstrates how to work with a [meeting query](meeting-queries.md). 

<iframe src="https://player.vimeo.com/video/434889528" width="580" height="512" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

## Related topics

* [Power BI templates](../Tutorials/Power-bi-templates.md)
* [Glossary](../Use/Glossary.md)
* [Metric descriptions](../Use/Metric-definitions.md)
