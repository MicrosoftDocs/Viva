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

The Workplace Analytics group query will help you understand how a team invested their time across the rest of the organization and beyond.

The query output lists pairs of groups, as defined by an organizational attribute of your choosing, along with how much time the first group allocated to second group.

 [[image placeholder]]

## Quick overview of time allocation

The details of time allocation can get complicated. You get more details in the full time allocation tutorial that explains the logic and works through several examples.

For now, here’s the short version.

Time allocation measures how groups budgeted their time. For each meeting and email, the total time that one group spends on the interaction has to be divided up among the other participating groups.

A “time giver group” allocates their time among the other participants in an interaction in proportion how many people are in each “time receiver group.”

Keep in mind that the group query can only analyze time allocation for licensed employees. Non-licensed collaborators can show up as time receivers, but never as time givers.

Finally, the time allocation approach assumes that a time giver group will only allocate time to themselves if no other groups are participating in the meeting or email.

 

## Create a group query 

Setting up a group query is a little different than setting up a meeting or person query.

The options for time period aggregation, time range, and meeting exclusion rules are the same as for the other two queries.
But it requires choosing a grouping attribute for Group A, your time givers…
…and for Group B, your time receivers. For example, you could examine how senior leaders allocated time across different organizations by setting Group A to “level” and Group B to “organization”.

 

Unlike a person or meeting query, the group query requires you to select a single measure of between-group collaboration.

Count gives you the number of interactions that occurred between the two groups. These interactions are not subject to the time allocation rules.

Hours gives you how much time each time giver group allocated to time receivers, regardless of who initiated the meeting or email.

Organizational load is similar to hours but limited to just time associated with activities initiated by the time giver group.

 

The group query includes filtering options and a “limit population” option. These give you more control over how time is allocated, but also can create unexpected results. 

For a better understanding of how these options impact the group query, be sure to check out the full group query training.

