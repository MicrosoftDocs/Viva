---
# Metadata Sample
# required metadata

title: Group-to-group queries in Workplace Analytics
description: Group-to-group queries uncover how a team invested their time across the rest of the organization and beyond.  
author: paul9955
ms.author: rodonahu
ms.date: 05/03/2018
ms.topic: get-started-article
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

**To create a group query**
1. In Workplace Analytics, click **Queries** and click **Group-to-group**.
2. Type a name for the query, and optionally, type a description. 
3. For Group by, select a time-grouping option -- day, week, or month. 
4. Select a date range. The query will analyze only those group-to-group interactions that took place during this date range.
5. Select a set of meeting exclusions. The query will ignore meetings that are filtered out by the meeting exclusions you choose. Move on to the Select metrics section:

   ![Select metrics](../Images/WpA/tutorials/g2g-01-select-metrics.png)

6. Answer this question to specify the type of data you want to analyze. Select one of the following three metrics: 

    * **Count** gives you the number of interactions that occurred between the two groups. These interactions are not subject to the time-allocation rules.

    * **Hours** gives you how much time each time-investor group allocated to collaborators, regardless of who initiated the meeting or email.

    * **Organizational load** is similar to hours but is limited to only the time associated with activities initiated by the time-investor group.
   
   In the following sections, you determine other aspects of the character of your query by choosing how to group both the time investors and the collaborators. For example, you could examine how senior leaders allocated time across different organizations by setting the time investors' group to “level” and the collaborators' group to “organization.”

   Move on to the Time investors section:
   ![Group and filter time investors](../Images/WpA/tutorials/g2g-02-group-filter-time-investors.png)

7. The next question is How do you want to group the time investors? Answer this by selecting an attribute of this group of people; for example, FunctionType, IsInternal, or tenuremonths. 
8. Optionally, remove some of the time investors from this analysis. Do this by applying filters in the Do you want to limit the analysis to only certain time investors? area.

   You have now finished specifying the time investors you want to analyze and how you want the query to group them. Now, you make similar determinations about the collaborators. 

   Move on to the Their collaborators section:
   ![Exclude collaborators](../Images/WpA/tutorials/g2g-03-exclude-collaborators.png)
   
9. 




Unlike a person or meeting query, the group query requires you to select a single metric of between-group collaboration.



![Group collaborators](../Images/WpA/tutorials/g2g-04-group-collaborators.png)

