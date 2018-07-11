---
# Metadata Sample
# required metadata

title: Person-to-group queries in Workplace Analytics
description: Person-to-group queries in Workplace Analytics uncover how an individual invested their time across the rest of the organization and beyond.
author: madehmer
ms.author: v-midehm
ms.date: 06/13/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Person-to-group queries

Person-to-group queries in Workplace Analytics give results that help you understand how an individual invests their time across the rest of the organization and beyond. The query results list individuals (the "time investors") by their PersonIDs, one or more groups that you define in the query ("collaborators"), and the amount of time that the time investor spends with the groups that you define.

![Time investors allocate time to various groups](../Images/WpA/tutorials/p2g-query.png)

> [!Note] 
> Because individuals are assigned a randomly generated PersonID to maintain de-identification, there is no way to identify an individual in the output of a query.

## Overview of time allocation

An understanding of time allocation helps you create better group queries. The details of time allocation can be complicated. Here is a summary of the basic concepts:

* Time allocation measures how groups spent their time. For each interaction (a meeting attended or an email sent or received), the total time that one group spent on the interaction is divided among the other groups that participated.
* A time investor allocates their time among the other participants in the interaction (the collaborators) in proportion to how many people are in the collaborator group for that interaction.
* A group query can analyze time allocation only for employees in the population of measured employees, namely those who are licensed for Workplace Analytics. People who do not have a license for Workplace Analytics can appear as collaborators, but never as time investors.
* The time-allocation approach assumes that a time-investor group allocates time only to themselves if no other groups are participating in the meeting or email.

## Create a person-to-group query

While setting up a person-to-group query differs from setting up meeting or group-to-group queries, some of the options you set, such as for time-period aggregation, time range, and meeting-exclusion rules, are the same as for the other query types. To set up a person-to-group query, follow these steps:

**To create a person-to-group query**

1. In Workplace Analytics, click **Queries**, and then click **Person-to-group**.
2. Type a name for the query, and optionally, type a description.
3. For Group by, select a time-grouping option -- day, week, or month.
4. Select a date range. The query will analyze only those person-to-group interactions that took place during this date range.
5. Select a set of meeting exclusions. The query will ignore meetings that are filtered out by the meeting exclusions that you choose. 

    Move on to the Select metrics section:

   ![Select metrics](../Images/WpA/tutorials/g2g-01-select-metrics.png)

6. Select one or more metrics that the query will use for measuring interactions between the time investors and collaborators. In other words, what data do you want the query to output for your analysis? Here are the choices:

    * **Collaboration hours** gives you the total amount of time that an individual spent with collaborating groups. This includes both time spent working in emails and time spent in meetings.

    * **Email count** and **Email hours** give you, respectively, the number of emails that were sent between the time investor and groups, and the amount of time the time investor spent sending and reading emails.

    * **Meeting count** and **Meeting hours** give you, respectively, the number of meetings in which the time investor and the collaborators participated, and the number of hours the time investor spent in meetings.

    * **Network size** tells you how many unique people the time investor was in contact with in the selected collaboration group over the selected time period.

    In the following sections, you determine other aspects of the character of your query by choosing how to group both the time investors and the collaborators. For example, you could examine how senior leaders allocated time across different organizations by setting the time investors' group to “level” and the collaborators' group to “organization.”

   Move on to the Time investors section:

   ![Group and filter time investors](../Images/WpA/tutorials/p2g-limit-time-investors.png)

7. The next question is Do you want to limit the analysis to only certain time investors? This lets you optionally apply filters to remove from your analysis some time investors, while you retain others. For example, if you specify _FunctionType_ Equals _Account Management_, the query results will report only on time investors who work in Account Management.

   You have now finished specifying the time investors whose behavior you want to analyze. Now, make determinations about the collaborators.

   Move on to the section called Their collaborators:

   ![Exclude collaborators](../Images/WpA/tutorials/g2g-03-exclude-collaborators.png)

8. Add filters to exclude collaborators. The filtering options (such as layer, Domain, FunctionType, or Organization) that you can use here are the same ones that were available to you for excluding time investors in the preceding step. At this point, the collaborators are ungrouped; that is, the query results would not inform you which collaborators (the ones in Sales? the ones in R&D? the ones in particular external domains?) interacted with the time investors.
9. Now, you can group the collaborators. By doing this, you can have the query results inform you which groups interacted with the time investors. You can also combine groups of collaborators for the purpose of isolating other specific groups who interacted with the time investors. 

    ![Group collaborators](../Images/WpA/tutorials/g2g-04-group-collaborators.png)

10. Choose **Run**. This submits the query and displays the Results page of the Queries area of Workplace Analytics. The status of the query is displayed as Submitted. After the query run completes, you can view it, download it (in .csv file format), or [Copy an OData link](https://docs.microsoft.com/en-us/workplace-analytics/use/view-download-and-export-query-results#get-a-link-for-odata-feed-that-you-can-use-in-power-bi) that you can use in a visualization tool such as Power BI.
