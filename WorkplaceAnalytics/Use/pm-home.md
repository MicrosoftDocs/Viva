---
ROBOTS: NOINDEX,NOFOLLOW
title: Workplace Analytics Home page for People Managers
description: Learn how the Workplace Analytics Home page uses industry-based research to show you actionable insights into more effective business outcomes for your team
author: madehmer
ms.author: madehmer
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Workplace Analytics Home page for People Managers

As a people manager, the **Home** page gives you research-based behavioral insights into how your team gets work done.

![People Manager Home page](../images/wpa/use/pm-home.png)

## Analysis scope

The top right of the page shows who is included in this analysis. This data is based on the most recent organizational data uploaded to and processed in Workplace Analytics, which includes the current date range and the number of measured employees in your team. For more details about uploads and measured employees, see [Organizational data](organizational-data.md).

## Employee experience

A positive employee experience reduces turnover, boosts productivity, and leads to happier employees.

For example, are employees routinely getting one-on-one time with their managers? Research shows that employees who get consistent manager coaching are five times more likely to stay engaged, which leads to increased productivity and greater employee retainment.

![Employee experience](../images/wpa/use/pm-employee-exp.png)

## Organizational agility

Nimble teams can efficiently adapt to market changes and gain a true competitive advantage.

For example, do your employees have time to focus on their work? Research shows that employees who have time to focus on deep work can master difficult tasks and produce higher quality work.
<!--
![Organizational agility](../images/wpa/use/org-agility.png)-->

## Supporting evidence

Each insight includes **Supporting evidence** that links you to a related article at [Microsoft Workplace Insights](https://insights.office.com/). These articles are authored by:

* Industry experts based on research.
* Organizations that have effectively used Workplace Analytics to improve their business outcomes.

## Differential privacy

Differential privacy is the acceptable deviation of keeping individual employees data private without comprising the accuracy of the metrics shown. Workplace Analytics hides metric details at the aggregation level. And noise or de-identified data is used to protect employee privacy when manager pivot or filter for more specific data points.

## Metrics for teams like you

As a group manager, this section compares your team's metrics to other teams like yours, such a similar size team with similar work activity.

The following are how the metrics are calculated that support the behavioral insights about teams that are similar to yours.

|Behavior |Metric name | Metric definition |Metric calculation |
|---------|--------------|--------|--------|
|Manager coaching |**Manager coaching hours 1:1** |The total number of hours that a manager spends in one-on-one meetings with all of their direct reports. | 100 multiplied by the number of people who have manager coaching hours that are greater than the threshold minutes per week divided by the total number of employees with a manager), and then this monthly calculation is divided by four to get the weekly totals. |
| Wellbeing | **After-hours collaboration** |Number of hours the person spent in meetings and on email outside of working hours. **Note**: To target or filter for after-hours collaboration, you can use a filter with the Collaboration hours metric. |100 multiplied by the number of people who collaborated outside of working hours /total measured employees in the company), which is then averaged for the last six months. |
|Meetings |**Meeting hours** <br><br>**Long or large meetings** | Number of meeting hours the time investor group has spent meeting with the collaborator group. <br><br>Number of meetings that last more than one hour or have nine or more attendees. |100 multiplied by the number of people who have meeting hours in long or large meetings, divided by the meeting hours per person that are greater than 0.5, which is then divided by the total number of measured employees in the team. This is then averaged for the last six months. |
|Focus |**Focus hours** |Total number of hours with two or more one-hour blocks of time where the person had no meetings. |100 multiplied by the number of employees who had greater than 20 hours of focus time (two or more one-hour blocks) for the week, divided by the total number of measured employees in the team. This is then averaged for the last six months.|
Manager connectedness | **Networking outside organization** |Number of departments outside their own that a person had meaningful interactions with, within the last 28 days (or if reported by month, within the last month). | 1.  Filters the population to only include *active* managers (**IsActive** equals **True**) in the calculation. <br>2.  Then uses every time period, which is every available month's (four weeks) data, to get the maximum metric for **Network breadth**, which for person queries is **Networking outside the organization**. <br>3.  Next the computation checks for and excludes managers that have a maximum Network breadth greater than or equal to three from the count. <br>4.  And then for every four weeks, it counts the managers who have a Network breadth that's less than three, and uses that count to calculate the percentage as compared to the total number of managers in the population. <br>5.  This percentage is then averaged for every month. |
|Email overload | | | |
|Efficient communication | | |  |
|Cross-group collaboration | | | |  
|Influencers | | | |

## View recommended plan

As people manager, you'll also see an option to **View recommended plan** for each business insight. You can use this option to take immediate action for the groups listed in that specific insight. For more details about creating plans, see [Create a plan](../tutorials/solutionsv2-task.md#create-a-plan).

## About the metrics

The following describes the metrics used in each of the business insight questions.

|Question |Description  |
|---------|--------------|
|Are employees finding time to recharge? |The number of employees that spend greater than one hour outside of their designated work hours in meetings and email each week, divided by the total number of measured employees. |
|Are your employees overloaded by long and large meetings? |The number of employees that spend over 50 percent of their total meeting time in long or large meetings, divided by the total number of measured employees. |
|Do employees have 1:1 time with managers? |The number of employees who have 15 minutes of 1:1 time with their manager each week (based on the total 1:1 time in the month), divided by the total number of measured employees. |
|Do employees have time to focus? |The number of employees who have 20 or more hours each of available time for focused work, divided by the total number of measured employees. |
|Are managers accessing diverse information? |The number of managers who had more than three meaningful connections outside of their organization each month. |
|Where are the influencers in your company? |The number of organizations that have fewer than expected numbers of influencers, which are based on thresholds defined for the organization and company size. |

## Related topics

* [Explore the metrics](explore-intro.md)
* [Plans](../tutorials/solutionsv2-intro.md)
* [Metric descriptions for Workplace Analytics](metric-definitions.md)