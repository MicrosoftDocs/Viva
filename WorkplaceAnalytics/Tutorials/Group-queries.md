---
# Metadata Sample
# required metadata

title: Group queries in Workplace Analytics
description: This topic discusses how group queries in Workplace Analytics can help you understand how a team has invested their time across the rest of the organization and beyond.  
author: rodonahu
ms.author: rodonahu
ms.date: 03/19/2018
ms.topic: get-started-article
ms.prod: wpa
---

# Group queries

Workplace Analytics group queries give results that help you understand how a team invested their time across the rest of the organization and beyond. The query results list pairs of groups, as defined by an organizational attribute of your choosing, along with how much time the first group allocated to the second group.

![Group A allocates time to Group B](../Images/WpA/tutorials/Group-query1.png) 

## Brief overview of time allocation

The details of time allocation are complicated. You can learn more details in the time allocation tutorial, which explains the logic and works through several examples. Here are the basic concepts: 

Time allocation measures how groups spent their time. For each meeting and email, the total time that one group spends on an interaction (email or meeting) must divided up among the other participating groups.

A "time investor" allocates their time among the other participants in an interaction in proportion how many people are in the "collaborator" group for that interaction.

A group query can analyze time allocation only for employees in the population of measured employees, namely those who are licensed for Workplace Analytics. People who do not have a license for Workplace Analytics can appear as collaborators, but never as time investors.

The time-allocation approach assumes that a time-investor group allocates time only to themselves if no other groups are participating in the meeting or email.

 ![Principles of time allocation](../Images/WpA/Tutorials/principals-of-time-allocation.png)

## Create a group query 

While setting up a group query differs from setting up meeting or person queries, the options for time-period aggregation, time range, and meeting-exclusion rules are the same as for meeting and person queries.

But a group requires that you choose a grouping attribute for Group A (the time investors) …
… and for Group B (the collaborators). 

For example, you could examine how senior leaders allocated time across different organizations by setting Group A to “level” and Group B to “organization”.

![Create group query](../Images/WpA/tutorials/Group-query2.png)

Unlike a person or meeting query, the group query requires you to select a single metric of between-group collaboration.

![Group metrics](../Images/WpA/Tutorials/Group-query3.png)

**Count** gives you the number of interactions that occurred between the two groups. These interactions are not subject to the time-allocation rules.

**Hours** gives you how much time each time-investor group allocated to collaborators, regardless of who initiated the meeting or email.

**Organizational load** is similar to hours but is limited to only the time associated with activities initiated by the time-investor group.
 
The group query also includes the options to **Add filter** and **Limit population** option. These give you more control over how time is allocated, but also can create unexpected results. 
