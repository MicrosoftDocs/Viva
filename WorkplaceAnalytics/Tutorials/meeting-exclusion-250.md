---
title: Meeting exclusion rules -- Large meeting limitation 
description: Meeting exclusion rules -- Concepts   
author: paul9955
ms.author: v-pausch
ms.topic: troubleshooting
localization_priority: normal 
ms.prod: wpa
---

# Meeting exclusion rules: Large-meeting limitation

### Background

To remove particular meetings or classes of meetings from analysis, you can create custom meeting exclusion rules, as described in [Meeting exclusion rules](meeting-exclusions-intro.md). One of the classes of meetings that you can remove from analysis is large meetings. By default, the filter value for meeting size is 250. This means that, in the default meeting exclusion rule, all meetings that have 250 or more participants will be excluded. 

In one of the steps for creating a custom meeting exclusion rule, you can change the filter value to a number other than 250.

### Problem

The custom rule will not function properly in certain cases, if its large-meeting filter value is set to a number equal to or higher than 250, _or_ if the large-meeting exclusion contains exceptions. 

### Solution

Both of the following solutions work:

 * **Use the default rule.** If you use the default large meetings exclusion provided to you in the flow, you will not encounter any issues.
 * **Keep filter value under 250.** Meeting exclusion rules can be used in queries. To use a custom meeting exclusion rule with particular metrics in queries, you must remove all meetings that have 250 or more attendees.

#### Restrictions

Depending on which customizations you make in the large-meetings step, you might be able to use this rule only in certain cases, as described here:

If you do any of the following:

 * Set the filter value to a number higher than 250
 * Create exceptions to this exclusion
 * Skip the large meetings rule

... these things will happen:

 * Your data load will fail if this rule is used as a preferred, or default, rule in Explore the stats data.
 * Any meeting queries that contain the [impacted metrics](#impacted-metrics) will fail. 

### Impacted metrics

 * For meeting queries, particular metrics do not support meetings with greater than 250 attendees. If the exclusion rule that is applied on a query that contains these metrics does not include an exclusion to remove meetings with more than 250 attendees, the query will fail. 

<!--
The impacted metrics are: 

<List of metrics here> FOR THIS, PUT "PARTICULAR QUERIES IN MEETING QUERIES"
-->
 * Any meeting query metric that has a participant filter applied to it will fail. 
