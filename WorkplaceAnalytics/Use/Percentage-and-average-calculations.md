---
# Metadata Sample
# required metadata

title: Percentage and average calculations in Workplace Analytics
description: This topic contains information and best practices to help ensure that analysts accurately calculate percentages and averages within Workplace Analytics. 
author: v-leash
ms.author: v-leash
ms.date: 02/14/2018
ms.topic: get-started-article
ms.prod: wpa
---
# Percentage and average calculations in Workplace Analytics

This topic contains information and best practices to help ensure that analysts accurately calculate percentages and averages within Workplace Analytics.
## Overview
* In queries, rows with no value (null) are excluded from results.
* Impact: Excluded and null values can skew percentage and average calculations.
* Best practice step 1: Add the **Sent mail** metric for each query to help ensure each person is represented.
* Best practice step 2: Before calculating percentages or averages, replace null values with zeros.

## In queries, rows with no value (null) are excluded from results
When Workplace Analytics generates query results, there is no row for a person if the results for the metrics are null. Also, for any null-value metrics in a row, Workplace Analytics leaves the value in that cell blank; it does not return a zero.
Example In a query for the metric **Manager 1:1 hours**  for a week, two people (Person ID 0003 and 0004) of a team of five employees had no Manager 1:1 hours that week. Therefore, those two employees are excluded from the output.


Person ID  | Date | Manager 1:1 hours
---------|----------|---------
0001 | 01/01/2017 | 0.5
0002 | 01/01/2017 | 0.5
0005 | 01/01/2017 | 2.0

## Impact: Null values can skew percentage and average calculations
Since there is no row for a person where the metric is null, if an analyst calculates percentages and/or averages, the results would be inaccurate because they do not account for the entire team (excluding Person ID 0003 and 0004 in this example). 
Example continued – skewed average The average manager 1:1 hours from the results above, would be inaccurate, showing 1 (3 hours divided by 3 people), rather than .6 (3 hours divided by 5 people).

### Average Manager 1:1 Hours - skewed average
Date | Average Manager 1:1 Hours 
---------|----------
 01/01/2017 | 1.0 

## Best practice step 1: Add the Sent mail metric for each query
To ensure that query results include a row for every active employee, add the **Sent mail** metric. This is a common metric that is highly likely to have at least one value for each person.

The query output then includes a row for all people who sent email during the period, even if other metrics are null.

### Example continued – With Sent mail metric

**Person ID**|**Date**|**Sent Mail**|**Manager 1:1 Hours**
:-----:|:-----:|:-----:|:-----:
1|1/1/2017|53|0.5
2|1/1/2017|62|0.5
3|1/1/2017|40| 
4|1/1/2017|100| 
5|1/1/2017|109|2

In our example, the query now includes all team members. However, since the null values are blank, before you calculate percentages or averages, you need to replace null values with zeros.

## Best practice step 2: Before calculating percentages or averages, replace null values with zeros
Once you have the query results, before you calculate averages and percentages, replace all null values with zero.

### Example continued – Replace null with zero and calculate average

**Person ID**|**Date**|**Sent Mail**|**Manager 1:1 Hours**
:-----:|:-----:|:-----:|:-----:
1|1/1/2017|53|0.5
2|1/1/2017|62|0.5
3|1/1/2017|40|[[replace null with 0]]
4|1/1/2017|100|[[replace null with 0]]
5|1/1/2017|109|2

Once you have replaced null values with zeros, you can calculate the average and get a more accurate result.
### Average Manager 1:1 Hours with all team members represented, and null values replaced with zero 
**Date**|**Average Manager 1:1 Hours**
:-----:|:-----:
1/1/2017|0.6