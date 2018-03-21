---
# Metadata Sample
# required metadata

title: Meetin queries in Workplace Analytics
description: This article describes when to use a meeting query and the kind of information they provide.  
author: rodonahu
ms.author: rodonahu
ms.date: 03/21/2018
ms.topic: get-started-article
ms.prod: wpa
---

# Meeting queries

The Workplace Analytics Meeting query provides a list of any meetings that occurred during a specific period, along with their attributes.

## How to choose between a Meeting or Person query 
Certain questions can be answered with either a Meeting or Person query.

 ![Meeting or Person query](../Images/WpA/Tutorials/person-or-meeting-query.png)

But for most questions you want to answer, the lines are more clear cut.

![Meeting query and Person query](../Images/WpA/Tutorials/meeting-or-person-query-2.png)
 
Use a meeting query when you want to understand the relationship between different meeting attributes.

Use a person query when you want to understand the relationship between a person’s organizational attributes – like their team, level, or location – and how they use their time, or when you want to know how one aspect of a person’s time use might influence another aspect of their time use.

## Create a meeting query
Setting up a meeting query is simple.

Select whether you want the metrics for each meeting summarized by day, week or month, and the time period you’d like to analyze.

If you want to exclude meetings from the calculations using custom criteria, you can select your custom rule set – otherwise, use the default. 

 ![Create meeting query](../Images/WpA/Tutorials/create-meeting-query1.png)

By running this query with no exclusions, you will get a helpful output file that can help you determine the right criteria to separate work-related activities from other calendar items.
 
 ![Meeting query no exclusions](../Images/WpA/Tutorials/meeting-no-exclusions.png)

## Add filters

You can add a filter to limit the list of meetings included in the output file.
The **Meeting** filter will limit the query based on the size, duration, or other attributes of the meeting.

The other filters will limit the query based on the organizational attributes of the different meeting participants.

![Meeting query filters](../Images/WpA/Tutorials/meeting-filter.png)


