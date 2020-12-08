---
title: Boost employee engagement with Workplace Analytics
description: Learn how to use Workplace Analytics data to analyze and improve employee engagement
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Boost employee engagement

*This experience is only available through private preview at this time.*

Employees with high job satisfaction and a strong sense of belonging are more likely to produce high-quality work, identify business opportunities, and remain at the organization.

For example, are employees routinely getting one-on-one time with their managers? Research shows that employees who get consistent manager coaching are five times more likely to stay engaged, which leads to increased productivity and greater employee retainment.

Each of the behaviors listed show how your organization compares with others based on industry research and your specific organizational data.

![Employee engagement page](../images/wpa/use/boost-ee.png)

## Calculations

The following are the percentage insights, their underlying metrics, and a little about the calculations used for them.

![Employee engagement percentage insight](../images/wpa/use/boost-ee-percent.png)

|Behavior |Percentage insight | Metrics |Calculations |
|---------|--------|--------------------|----------------------|
|Promote coaching and development |Percentage of employees who have less than 15 minutes of 1:1 time with their managers each week |[Meeting hours with manager 1:1](metric-definitions.md#meeting-hours-with-manager-1-1-define) |Percentage of employees with less than 15 minutes of weekly 1:1 time with their managers. To account for various 1:1 meeting frequencies, the total time is calculated for each employee per month and averaged over a week. |
|Prevent employee burnout |Percentage of employees who are working after hours for more than one hour each week |[After-hours metrics](metric-definitions.md#person-metrics) |Percentage of employees who spend more than one hour collaborating through emails, calls, instant messages, and meetings outside of working hours. This percentage is calculated weekly and averaged over the entire time period. |
|Drive employee empowerment |Percentage of employees who have a majority of their meetings attended by their manager |[Meeting hours with manager](metric-definitions.md#meeting-hours-with-manager-define) and [meeting hours](metric-definitions.md#meeting-hours-define)|Percentage of employees who spend over 50 percent of their meeting hours with their manager present in the meeting. This percentage is calculated weekly and averaged over the entire time period. |
<!--|Encourage team cohesion |Percentage of employees who are members of teams with strong cohesion |[Cross-organization collaboration and internal collaboration hours](metric-definitions.md#person-metrics) |Calculation info |-->

The following defines the organizational data shown in the visual behavioral insights.

![Employee engagement visual insight](../images/wpa/use/boost-ee-visual.png)

|Behavior |Visual insight | Definition |
|---------|--------|----------------------|
|Promote coaching and development |Distribution of monthly 1:1 time with managers |Percentage of employees based on their monthly meeting hours with managers 1:1. They are divided into employees who have no 1:1s, between zero and one hour, and more than one hour of 1:1s with their manager in a month. These percentages are calculated monthly and averaged over the entire time period. This graph uses the [meeting hours with manager 1:1](metric-definitions.md#meeting-hours-with-manager-1-1-define) metric.|
|Prevent employee burnout | Distribution of weekly after-hours collaboration |Percentage of employees based on their weekly [after-hours collaboration](metric-definitions.md#after-hours-collaboration-define). They are divided into employees who spend less than one hour collaborating after-hours, employees who spend between one to five hours collaborating after-hours, and employees who spend more than five hours collaborating after-hours. These percentages are calculated weekly and averaged over the entire time period. |
|Drive employee empowerment |Distribution of manager-employee coaching relationships |Uses the average time employees spend with [their managers in 1:1s](metric-definitions.md#meeting-hours-with-manager-1-1-define) and the percentage of [meeting hours with manager in attendance](metric-definitions.md#meeting-hours-with-manager-define), the different manager-employee coaching relationships are grouped by employee time percentages: <ul><li>**Coached** - Spend more than 15 minutes in 1:1s (weekly average based on the monthly calculation) and those who spend less than 30 percent of their meeting hours with their managers in attendance.  </li><li>**Co-attended** - Spend less than 15 minutes in 1:1s (weekly average based on the monthly calculation) and those who spend more than 30 percent of their meeting hours with their managers in attendance. </li><li>**Micromanaged** - Spend more than 15 minutes in 1:1s (weekly average based on the monthly calculation) and those who spend more than 30 percent of their meeting hours with their managers in attendance. </li><li>**Under-coached** - Spend less than 15 minutes in 1:1s (weekly average based on the monthly calculation) and employees who have less than 30 percent of their meeting hours with their managers in attendance.</li> |<!--|Encourage team cohesion |Cohesion within teams |An [organizational network graph](insight-ona-measures.md) that shows the number of teams with strong cohesion and those who are not very cohesive based on the average monthly collaboration activity within the team’s network. This uses [collaboration hours and other related metrics](metric-definitions.md#person-metrics). |-->

## Take action

You can select **Take action** to see ways you can improve employee engagement. Depending on your role, the following are available in addition to the recommendations within Take action.

* **Opportunity groups** - Lists the groups who are most affected and would benefit the most from these recommended best practices or [Plans](../Tutorials/solutionsv2-intro.md), which are based on your organizational data and industry research.
* **Explore the stats** – Depending on the recommendation, this links to [Management and coaching data](explore-metrics-management-and-coaching.md) or [Teamwork data](../tutorials/teamwork-solution.md.
* **Explore in Power BI** - If available, links to [Power BI reports](../tutorials/power-bi-intro.md) for more advanced analysis for one or more of the recommendations.
* **Plans** - Opens a new [Plan](../Tutorials/solutionsv2-intro.md) you can set up relating to one or more of the recommendations.

## Best practices

This section describes why each of the following behaviors matter and the top best practices that can help keep employees engaged.

* [Promote coaching and development](#promote-coaching-and-development)
* [Prevent employee burnout](#prevent-employee-burnout)
* [Drive employee empowerment](#drive-employee-empowerment)

### Promote coaching and development

Manager one-on-one (1:1) time can improve engagement and job performance, while lack of manager coaching can cause employee disengagement and attrition. According to the research referenced in [What great managers do daily](https://insights.office.com/productivity/what-great-managers-do-daily/): "A Gallup study found that at least 70 percent of the variance in employee engagement scores is driven by who the boss is."

One of the top best practices for promoting coaching and development is to require that managers schedule recurring 1:1 meetings with their direct reports for 30 minutes at least twice a month and hold them accountable for achieving that goal. See [Catch up with your team](../myanalytics/use/use-the-insights.md#catch-up-with-your-team) for help with scheduling and managing your 1:1s.

For more best practices and how to develop a 1:1 conversation series, see [Best practices for manager coaching](../tutorials/gm-coaching.md).

### Prevent employee burnout

Pressure to "always be on" and long hours can lead to employee burnout. The amount of time employees spend collaborating outside of business hours is an indicator of burnout risk.

Based on research presented in the [Why unplugging from work is more work than we think](https://insights.office.com/productivity/unplugging/): "New research and our growing understanding about human behavior tell us two things for certain: that unplugging is more necessary than ever, and that true unplugging is not a single action but a social agreement — a culture shift that employees and companies must create together." Ways to support wellbeing:

* Use [MyAnalytics wellbeing data](../MyAnalytics/Use/wellbeing.md) to learn about after-hours work habits and encourage your team to take time to disconnect and recharge.
* Use [Inline suggestions in Outlook](../MyAnalytics/Use/mya-notifications.md#delay-email-delivery) to automatically delay email delivery to align with configured working hours for coworkers.

For more best practices and how to define and share working hours, see [Best practices for wellbeing](../tutorials/gm-wellbeing.md).
<!--
### Encourage team cohesion

Employees who maintain strong connections within their team feel a sense of organizational belonging.

According to the [Horizontal collaboration and cross-silo leadership](https://insights.office.com/networks/cross-silo-leadership-horizontal-collaboration/) article, it's important to develop and deploy cultural "brokers" to "promote cross-boundary work in one of two ways: by acting as a bridge or as an adhesive."

Ways to support team cohesion:

* Ask employees to use [MyAnalytics network features](../myanalytics/use/network.md) to add people to their "important people" list, which enables suggestions to meet and reminders to respond to emails and complete tasks from them.
* Host informal gatherings, such as virtual opportunities for your team to bond over non-work activities and form new connections. Create agendas with fun conversation prompts and activities, such as online trivia games.
* Strengthen connections with a [Teams channel](https://www.microsoft.com/microsoft-365/microsoft-teams/group-chat-software) for group communications and chats.

For more best practices and how to open your network to your teams, see [Best practices for manager connectedness](../tutorials/gm-connectedness.md).-->

### Drive employee empowerment

Cultivating autonomy and development are essential for employee engagement. By empowering employees to make decisions and tackle new challenges, enables managers to be more effective and reclaim time.

[How to boost your team’s productivity](https://insights.office.com/productivity/how-to-boost-your-teams-productivity/) explains that the "key to improving individual productivity is to eliminate or delegate unimportant tasks and replace them with value-added ones." Ways to empower employees:

* Use [Teams and OneNote](https://support.microsoft.com/office/add-a-onenote-notebook-to-teams-0ec78cc3-ba3b-4279-a88e-aa40af9865c2) to share meeting notes about decisions and action items as an alternative way to keep your team informed.
* Use [Manager insights in Workplace Analytics](../manager-insights/introduction.md) to help identify ways to support team behavior.

For more best practices and how to set team meeting rules and policy, see [Best practices for meetings](../tutorials/gm-meetings.md).

## Related topics

* [Business outcomes overview](insights.md)
* [Metric descriptions for Workplace Analytics](metric-definitions.md)
