---
ROBOTS: NOINDEX,NOFOLLOW
title: Query designer in Workplace Analytics
description: The Query designer in Workplace Analytics offers predefined Power BI templates and other custom query options for more in-depth data analysis
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
ms.prod: wpa
manager: scott.ruble
audience: Admin
---

# Query designer

The Query designer in Workplace Analytics has a number of different options that help you answer specific business questions and the flexibility to look at the data from multiple perspectives.

* Select as many or as few organizational metrics as you need, for a specific population or date range.
* Customize the metrics included in query results with a broad range of filters and other options.
* Combine query results from different queries to gain even more in-depth insights.

The designer includes the following types of queries.

* [**Query templates and reports**](#query-templates-and-reports) - You can use predefined query templates and reports that you can use to view and analyze data in Power BI or Workplace Analytics. These options help you focus your analysis for specific business outcomes, such as to transform meeting culture, enhance organizational resilience, develop effective managers, boost employee engagement, and more.

![Predefined templates and reports](../Images/WpA/Tutorials/query-templates.png)

* [**Custom queries**](#custom-queries) - Select **Get started** in the **Query** section to create a custom query based on the type of organizational data that you want to analyze, such as person, meeting, group-to-group, person-to-group, peer comparison, or network queries. You can then download the query data results as .csv files or depending on the type of data, visualize it directly in Workplace Analytics.

![New query options](../Images/WpA/Tutorials/new-query.png)

You can create queries as follows:

* Edit and use a predefined [query template](#reports-and-templates).
* Create your own [custom query](#custom-queries).
* Open and edit a previously run query.

## Query templates and reports

In Workplace Analytics, select **Query designer** to see predefined query templates and reports that help you analyze organizational data based on behavioral insights that relate to specific business outcomes.

For example, select the **Business continuity** section to see more details about the report, example report data, prerequisites, and setup steps.

![Business continuity template details](../Images/WpA/Tutorials/query-template-details.png)

You can also filter the templates and reports list to see what is available for a specific business insight. For example, the following shows what you'll see if you select **Filters** > **Develop effective managers**.

![Report filter for develop effective managers](../Images/WpA/Tutorials/query-template-filters.png)

Workplace Analytics includes a number of predefined query templates that help you get started with queries, including the following.

* [**Ways of working assessment**](./power-bi-collab-assess.md) - Power BI template that shows a quick and easy way to see current collaboration behaviors and culture and insights into employee wellbeing and engagement in your organization.
* [**Ways of working tracker**](./power-bi-collab-track.md) - Power BI template that shows how you can track behavior change and target opportunities to improve employee wellbeing, meeting culture, and manager effectiveness.
* [**Return to worksites**](./power-bi-return-tw.md) - Power BI template that shows how to plan who returns to work, and when, where, and how they do for the different work locations.
* [**Business continuity**](./power-bi-bc.md) - Power BI template that shows example insights into how shifting to remote work has impacted business.
* [**Microsoft Teams insights**](./power-bi-teams.md) - Power BI template that shows how adopting Microsoft Teams can affect collaboration and productivity in your organization.
* [**Manager effectiveness**](./power-bi-manager.md) - Power BI template that helps leaders measure behaviors and trends of their people managers across four key themes within the organization, including coach, empower, connect, and model.
* [**Behavior patterns for Glint**](./power-bi-glint.md) - Power BI template that combines behavioral data from Workplace Analytics and sentiment data from Glint for insights that help identify opportunities to influence behavior and improve business outcomes.
* [**Sales business continuity**](./pbi-bc-sales.md) - Power BI template that shows insights into how shifting to remote work has impacted your sales organization.
* [**Quickstart overview**](./power-bi-quickstart.md) - Power BI template that shows a high-level view of key organizational metrics to get a quick perspective on how the organization is collaborating and a way to identify potential areas that might require additional analysis.
* [**Collaboration overload**](./power-bi-collab-overload.md) - Power BI template that shows where overall collaboration patterns, time fragmentation, or meeting quality could be improved in your organization.
* [**Influence insights**](./pbi-influence-db.md) - Power BI template that shows how you can learn who your influencers are and leverage their ability to disseminate information and effectively drive change.
* [**Manager impact**](./power-bi-manager-impact.md) - Power BI template that shows insights about key leadership behaviors by organization and best practices recommended by industry experts to either maintain or improve leadership work patterns.
* **Build focus hours** finds groups that have the lowest amount of focus time.
* **Calls and IMs** analyzes call and instant-message hours by person.
* **Meetings attendees query** analyzes meeting hours by the number of attendees.
* **Meetings day query** analyzes meeting hours by day of the week.
* **Meetings duration query** analyzes meeting hours by duration.
* **Meetings start time query** analyzes meeting hours by time of day.
* **Protect after hours** finds groups that collaborate the most outside of work hours.
* **Reduce meeting hours** finds groups that are overwhelmed by meetings.
* **Standard person query** provides all base metrics available for a person query.
* **Hourly collaboration** analyzes meeting, email, instant-message, and call activity by hour of the day.

## Custom queries

In **Query designer** > **Query**, select **Get started**, and then you can select to create one of the following types of queries from scratch, or when available and listed, select from one or more related predefined queries.

When you create a new query or edit an existing query, you select the metrics to include. You can also use filters to narrow the results and focus in on specific data. You can then download the query data results as .csv files or depending on the type of data, visualize it directly in Workplace Analytics.

![Customize metrics](../Images/WpA/Use/Customize-attributes-and-metrics.png)

* [**Person queries**](person-queries.md) - Use to find broad organizational trends by analyzing aggregated productivity metrics (such as time in meetings and email) for a de-identified list of individual employees.
* [**Meeting queries**](meeting-queries.md) - Use to analyze the relationship between different meeting attributes, such as size or duration, subject line keywords, double-booked hours, and multitasking hours.
* [**Group-to-group queries**](group-to-group-queries.md) - See how a team invested their collaboration time with other teams within and outside of the organization. You can define a team in a variety of ways, with any organizational attribute or email domain. This also offers alternative perspectives on collaboration.
* [**Person-to-group queries**](person-to-group-queries.md) - Helps analyze the number of interactions between a time investor and the defined collaboration team, or to analyze only those collaboration activities initiated by the specified time investor. You can define the person and collaborator team or teams in a variety of ways, with any organizational attribute or email domain.
* [**Peer comparison queries**](comparison-query.md) - Helps identify people whose collaboration patterns differ as compared to their peers. The query includes the measured employees, their specified metrics, and their peer group's averages for those metrics. You can compare individuals with others who share the same manager, with their direct reports, or even with a custom peer group as defined with organizational attributes.
* **Network queries** - Use [ONA person queries](ona-person-query.md) and [ONA person-to-person queries](ona-person-to-person-query.md) to find out who the best-connected people in your company, division, or group are, which is based on collaboration data. After you learn who your influencers are, you can act on the likelihood that these people can effectively connect within or across groups and become efficient drivers of change.

## Meeting exclusions

You define meeting exclusions to exclude types of meetings from analysis (such as all-day training meetings) where their inclusion might skew query results. You can select between the default meeting exclusion rules or create custom rules that match your company's meeting conventions.

See [Meeting exclusions](meeting-exclusions-intro.md) for details.

## Attendee exclusions

You can use the responses by meeting invitees to optionally exclude them from analysis. For example, invitees who accepted a meeting invitation as "Tentative" would normally be included in analysis by default. By adding an attendee exclusion, you can explicitly exclude them. In this way, creating attendee exclusions lets you effectively redefine "meeting attendance."

See [Attendee exclusions](attendee-exclusion-rules.md) for details.

## Data time limit

The historical data that queries and reports use is time limited. You can run queries only on data from the last 27 months. This 27-month period is a _rolling window_. After the first 27 months of [Microsoft 365 data](../use/office-365-data.md) is uploaded and processed in Workplace Analytics, it refreshes each week. This means the 27-month extent of data that you can query advances by one week to include the preceding 27 months.

However, historical query results that have already been run remain available, even after the data in the query results passes the 27-month limit.

## Related topics

* [Power BI templates](../Tutorials/Power-bi-templates.md)
* [View, download, and export query results](../use/view-download-and-export-query-results.md)
* [Workplace Analytics glossary](../Use/Glossary.md)
* [Metric descriptions](../Use/Metric-definitions.md)
