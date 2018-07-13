---
# Metadata Sample
# required metadata

title: Group-to-group queries in Workplace Analytics
description: Group-to-group queries uncover how a team invested their time across the rest of the organization and beyond with Workplace Analytics.  
author: madehmer
ms.author: rodonahu
ms.date: 06/20/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Group-to-group queries

Group-to-group queries in Workplace Analytics give results that help you understand how a team invested their time across the rest of the organization and beyond. The query results list pairs of groups, as defined by an organizational attribute of your choosing, along with how much time people in the first group (the "time investors") allocated to other groups ("collaborators").

![Group A allocates time to Group B](../Images/WpA/tutorials/Group-query1.png) 

## Overview of time allocation

An understanding of time allocation helps you create better group queries. The details of time allocation are complicated. Here is a summary of the basic concepts: 

* Time allocation measures how groups spent their time. For each interaction (a meeting attended or an email sent or received), the total time that one group spent on the interaction is divided among the other groups that participated.
* A time investor allocates their time among the other participants in the interaction (the collaborators) in proportion to how many people are in the collaborator group for that interaction.
* A group query can analyze time allocation only for employees in the population of measured employees, namely those who are licensed for Workplace Analytics. People who do not have a license for Workplace Analytics can appear as collaborators, but never as time investors.
* The time-allocation approach assumes that a time-investor group allocates time only to themselves if no other groups are participating in the meeting or email.

The following illustration depicts these concepts:

 ![Principles of time allocation](../Images/WpA/Tutorials/principals-of-time-allocation.png)

<!-- Per Dheepak, this pptx is not for public consumption 
> [!Note]  
> For more information, see the time allocation tutorial, which explains the logic and works through several examples. 
-->

## Create a group-to-group query

While setting up a group query differs markedly from setting up meeting or person queries, some of the options you set, such as for time-period aggregation, time range, and meeting-exclusion rules, are the same as for meeting and person queries. To set up a group-to-group query, follow these steps: 

**To create a group-to-group query**

1. In Workplace Analytics, select **Queries** and then select **Group-to-group**.
2. Type a name for the query, and optionally, type a description.
3. For Group by, select a time-grouping option -- day, week, or month.
4. Select a date range. The query will analyze only those group-to-group interactions that took place during this date range.
5. Select a set of meeting exclusions. The query will ignore meetings that are filtered out by the meeting exclusions that you choose. 

   Move on to the Select metrics section:

   ![Select metrics](../Images/WpA/tutorials/G2G-changes_03.png)

6. Answer the question _What would you like to know about the interactions?_ to specify the types of data that you want to analyze. Note that you can select multiple metrics, as shown here:  

   ![Select metrics](../Images/WpA/tutorials/g2g-01-select-metrics_2.png)

   For more information about the metrics that you can use in group-to-group queries, see [Group-to-group metrics](../use/metric-definitions.md#group-to-group-metrics). 

   In the following sections, you determine other aspects of the character of your query by choosing how to group both the time investors and the collaborators. For example, you could examine how senior leaders allocated time across different organizations by setting the time investors' group to “level” and the collaborators' group to “organization.”

   Move on to the Time investors section:

   ![Group and filter time investors](../Images/WpA/tutorials/g2g-02-group-filter-time-investors.png)

8. The next question is How do you want to group the time investors? Answer this by selecting an attribute of this group of people; for example, FunctionType, IsInternal, or tenuremonths.
9. Optionally, remove some of the time investors from this analysis. Do this by applying filters under the question _Do you want to limit the analysis to only certain time investors?_

   You have now finished specifying the time investors whose behavior you want to analyze and how you want the query to group them. Now, you make similar determinations about the collaborators. 

   Move on to the section called Their collaborators:

   ![Exclude collaborators](../Images/WpA/tutorials/g2g-03-exclude-collaborators.png)
   
10. Add filters to exclude collaborators. The filtering options (such as layer, Domain, FunctionType, or Organization) that you can use here are the same ones that were available to you for excluding time investors in the preceding step. At this point, the collaborators are ungrouped; that is, the query results would not inform you which collaborators (the ones in Sales? the ones in R&D?) interacted with the time investors.
11. Now, you can group the collaborators. By doing this, you can have the query results inform you which groups interacted with the time investors. You can also combine groups of collaborators for the purpose of isolating other specific groups who interacted with the time investors.

    ![Group collaborators](../Images/WpA/tutorials/g2g-04-group-collaborators.png)

12. Select **Run**. This submits the query and displays the Results page of the Queries area of Workplace Analytics. The status of the query is displayed as Submitted. After the query run completes, you can view it, download it (in .csv file format), or [Copy an OData link](https://docs.microsoft.com/en-us/workplace-analytics/use/view-download-and-export-query-results#get-a-link-for-odata-feed-that-you-can-use-in-power-bi) that you can use in a visualization tool such as Power BI.



<!-- VERIFY THIS CONTENT THEN MAKE A NEW TOPIC OUT OF IT. FOR MORE IN-DEPTH LEARNERS

# Walkthrough

## Group time investors or collaborators

Before you create a query, you need a clear concept of the question that you want the query to answer. Whose time do you want to analyze, and what do you want to know about it. The example we'll use here is that of your Sales team. Specifically, how much time did they spend over a particular six-month period with the Product marketing team. To obtain this information, write a query that uses grouping and filtering, as described in this section. 

Using the Their collaborators section of the Group-to-group query page

### What grouping means

When you use the Group collaborators option, you create groups by finding commonalities between individuals. For example, do you want a group of people who all work in offices in the same time zone? Do you want a group of managers all at the same level? Do you want all people who work in IT to form a group? These are all attributes that are uploaded in the HR data. You can use any HR data attribute for grouping, plus one other attribute: the person's email domain. 

### What grouping accomplishes

When you create a query, you typically find out how much time certain people spent with certain other people. That is, you take the time that the "time investors" spent in the meeting and you allocate that time proportionally among the distinct other groups that were represented in (attended) the interaction. 

## Step-by-step example

In this example, you want to find out how much time the people in Sales spent with marketing people in their interactions over the six-month period. These are the steps you take:

**To create the Sales - Product marketing query**

 1. Open the Queries page in Workplace Analytics.
 2. Click **Group-to-group** query.
 3. On the Queries > Group-to-group query page, type the query name.
 4. Type a description for the query.
 5. Indicate any particular meeting exclusions, or use the default set of meeting exclusions. Now go to the Select metrics section.
 6. Select an interaction type to learn more about. In this case, select Hours.
 7. Several metrics pertain to this interaction type. Choose the metric that most closely matches the information you want. Now go to the Time investors section.
 8. You want to study the people in Sales. Sales is an example of a workplace function, so select FunctionType under How do you want to group the time investors?
 9. The next question is Do you want to limit the analysis to only certain time investors? Because you want to limit your current study to people in Sales, the answer is Yes. Create a filter in which FunctionType = Sales. You have just created a group that the query will report about. Move on to the Their collaborators section.
 10. The first question in this section is Do you want to exclude any collaborators? The answer to this question depends on the scope of information that you want your query to supply. Your goal is to study the interaction between Sales and Product marketing. If these interactions are all you want to know about, you can now exclude all collaborators other than Product marketing. Do this by setting FunctionType in the left side of the filter builder, and adding all groups other than Product marketing on the right side. 
  
     Alternatively, you could exclude no groups. This would still answer your core question -- How much time did Sales spend with Marketing during these six months? But by letting the data from other groups also appear, you would see the Sales-Marketing interactions in the broader context of the overall behavior of your Sales team.

 13. Move on to the next question: How do you want to group the people who collaborated with the time investors? Because you are interested in the collaborators who are in Product marketing, and Product marketing is a workplace function, you want to group by workplace function, so select FunctionType.
 14. Finally, answer the question: Are there any collaborators you'd like to group all together to simplify the results? This question lets you optionally designate as "noise" the query results that you do not want to focus on. 

     Remember that you just selected FunctionType as the grouping mechanism for collaborators. If you do not answer this final question, the query will return discrete data about each group that interacted with your people in Sales. 

     If you do answer this question, you can have the query results treat all groups other than Product marketing as one "other" group, which it appropriately names "Other." To do this, in the filter builder, select FunctionType on the left, Equals in the center, and on the right, select all options other than Product Marketing. Now, when the query returns its results, all these other groups will appear together as one group called "Other." 

When we run this query, the query does this: It considers the time that the time investors spent in share interactions (such as meetings) and allocates it proportionally among the distinct other groups that attended the interaction. Again, note that groups are defined by the organizational (HR) attributes that selected to define them. 

## Group to simplify: more details

You can make your query results easier to interpret by using the Group to simplify option in the Their collaborators section. 
Grouping to simply doesn't change the allocation of time; it just simplifies the output of your query. In effect, it removes noise so that you can focus more easily on the data that you are seeking, on the answer to your question.

For example, the Sales team has met with individuals on six other teams. You care only about how much time they spent with one of those other teams, Product marketing. Use Group to simplify to concentrate on Product marketing. 

Although Sales also met with people in IT, Finance, R&D, Engineering, and Operations, you don't care about the time they spend with those groups. The total amount of time they spent with all those other groups combined might interest you, but the detailed breakdown does not. To clean up the query output in this regard, use the Group to simplify option under Their collaborators. The query results then treat Product Marketing as one group, and all other internal collaborators as a second group, called "other." Note that you cannot specify more than one "other" group; however, WpA automatically groups others into two groups by domain, internal others and external others. 

