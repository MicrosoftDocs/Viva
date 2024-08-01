---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 06/28/2024
title: Develop effective managers with Microsoft Viva Insights
description: Learn how to use insights data to analyze and develop effective managers in your organization
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: Low 
ms.service: viva-insights
manager: scott.ruble
audience: Admin
---

# Develop effective managers insights

*This experience is only available through private preview.*

Managers have a large impact on employee engagement, development and performance, and are pivotal for driving organizational change. Each of the behaviors listed show how your organization compares with others based on industry research and your specific organizational data.

![Develop effective managers page.](./images/develop-managers.png)

## Calculations

The following are the percentage insights, their underlying metrics, and a little about the calculations used for them.

![Develop effective managers percentage insight example.](./images/develop-managers-percent.png)

|Behavior |Percentage insight | Metrics |Calculations |
|---------|--------|--------------------|----------------------|
|Optimize meeting hours |Percentage of your managers' meetings that are structured around decision making |[Long and large meetings](glossary.md#large-meeting-define) and [meeting hours](metrics.md#meeting-hours-define) |The percentage of managers who spend over 50 percent of meeting hours in long or large meetings. Long meetings are longer than one hour and large meetings have more than eight attendees. The percentages are calculated weekly and averaged for the entire time period. |
|Prevent burnout |Percentage of managers who are working after hours for more than one hour each week |[After-hours collaboration](metrics.md#after-hours-collaboration-define) |The percentage of managers who spend more than one hour collaborating through email, calls, instant messages, and meetings outside of working hours. This percentage is calculated weekly and averaged over the entire time period. |
|Strengthen management pipeline |Percentage of employees who have the potential for managerial roles |[Influence](metrics.md#influence-define) |Employees who are currently in non-managerial roles with influence scores greater than or within 10 percent of their immediate manager’s influence score. |
|Promote coaching and development |Percentage of employees who have less than 15 minutes of 1:1 time with their managers each week |[Meeting hours with manager 1:1](metrics.md#meeting-hours-with-manager-1-1-define) |The percentage of employees who spend less than 15 minutes of coaching time with their managers each week. To account for different frequencies in coaching, this percentage is calculated monthly and then divided by four for the weekly average. |
|Empower employees |Percentage of employees who have a majority of their meetings attended by their manager |[Meeting hours with manager](metrics.md#meeting-hours-with-manager-define) and [meeting hours](metrics.md#meeting-hours-define) |The percentage of employees who spend over 50 percent of their meeting hours with their manager in attendance. This percentage is calculated weekly and averaged over the entire time period. |

The following defines the organizational data shown in the visual behavioral insights.

![Develop effective managers visual insight example.](./images/develop-managers-visual.png)

|Behavior |Visual insight | Definitions |
|---------|--------|----------------------|
|Optimize meeting hours |Manager meetings by duration and number of attendees | Shows the percentage of [manager meetings](metrics.md#meeting-hours-with-manager-define) based on their type, including: [Large meetings](glossary.md#large-meeting-define) with more than eight attendees, [long meetings](glossary.md#long-meeting-define) that are longer than one hour, [long and large meetings](glossary.md#long-and-large-meeting-define) with more than eight attendees and are longer than one hour, and [decision making meetings](glossary.md#decision-making-meeting-define) with between two and eight attendees and are less than one hour in duration. These percentages are calculated weekly and averaged over the entire time period. |
|Prevent burnout |Distribution of after-hours collaboration from managers |Percentage of managers based on their weekly [after hours collaboration](metrics.md#after-hours-collaboration-define). They are divided into those who spend less than one hour, between one to five hours, and more than five hours collaborating after hours. These percentages are calculated weekly and averaged over the entire time period. |
|<a name="ona-strengthen-define"></a>Strengthen management pipeline |Distribution of potential manager candidates |An [organizational network graph](glossary.md#ona-define) that represents the distribution of current managers and potential managers within your organization, based on [influence scores](metrics.md#influence-define). You can use this insight to evaluate future managers with high influence scores who are currently not in managerial roles. |
|Promote coaching and development |Distribution 1:1 time with managers each month |Shows the percentage of employees based on their monthly average number of [meeting hours with managers 1:1](metrics.md#meeting-hours-with-manager-1-1-define). They are divided into employees who have no 1:1s, between zero and one hour, and more than one hour of 1:1s with their manager in a month. These percentages are calculated monthly and averaged over the entire time period. This graph also uses the [influence metric](metrics.md#influence-define). |
|Empower employees |Distribution of manager-employee coaching relationships |Uses the average time employees spend with their [managers in 1:1s](metrics.md#meeting-hours-with-manager-1-1-define) and the percentage of [meeting hours with the manager](metrics.md#meeting-hours-with-manager-define) in attendance. The different manager-employee coaching relationships are grouped by employee time percentages that are weekly averages based on the monthly calculations: <ul><li>**Coached** - Spend more than 15 minutes in 1:1s and less than 30 percent of their meeting hours with their managers in attendance.</li><li>**Co-attended** - Spend less than 15 minutes in 1:1s and more than 30 percent of their meeting hours with their managers in attendance. </li><li>**Micromanaged** - Spend more than 15 minutes in 1:1s and more than 30 percent of their meeting hours with their managers in attendance. </li><li>**Under-coached** - Spend less than 15 minutes in 1:1s and less than 30 percent of their meeting hours with their managers in attendance. </li> |

## Take action

In the **Take action** section for each insight, select **See your insights** to see the most effective actions you can do now to drive change toward better business outcomes in your organization.

You also might see one or more groups listed who are affected and would benefit the most from these recommendations, which are based on your organizational data and industry research.

## Best practices

This section describes why each of the following behaviors matter and the top best practices that can help managers be more effective.

* [Optimize meeting hours](#optimize-meeting-hours)
* [Prevent burnout](#prevent-burnout)
* [Strengthen management pipeline](#strengthen-management-pipeline)
* [Promote coaching and development](#promote-coaching-and-development)
* [Empower employees](#empower-employees)

### Optimize meeting hours

Long and large meetings are costly and often a waste of manager time. Shorter and smaller meetings provide the best conditions for effective decision making.

To optimize meetings:

* Use [Teams and OneNote](https://support.microsoft.com/office/add-a-onenote-notebook-to-teams-0ec78cc3-ba3b-4279-a88e-aa40af9865c2) to share meeting notes about decisions and action items as an alternative way to keep your team informed.
* Use [Manager insights in Workplace Analytics](/viva/insights/manager-insights/introduction) to help identify ways to support team behavior.

For more best practices and how to set team meeting rules and policy, see [Best practices for meetings](/viva/insights/tutorials/gm-meetings)

### Prevent burnout

Pressure to "always be on" and long hours can lead to burnout. The amount of time managers spend collaborating outside of business hours is an indicator of burnout risk.

Here are some ways to support employee wellbeing:

* Use [personal wellbeing data](/viva/insights/personal/Use/wellbeing) about after-hours activity and encourage them to disconnect.
* Use the [Inline suggestions in Outlook](/viva/insights/personal/Use/mya-notifications#delay-delivery) to automatically delay email delivery to align with coworkers' configured working hours.

For more best practices and how to define and share working hours, see [Best practices for wellbeing](/viva/insights/tutorials/gm-wellbeing).

### Strengthen management pipeline

Potential influencers are often difficult to discover within an organization. Employees who are well-connected and play an important role in sharing information throughout the organization may be effective leaders.

To leverage influencers:

* Use personal network insights to cultivate influence and the [Network](/viva/insights/personal/use/network) page to see connections, top collaborators, and suggestions on how to improve connections.
* Move cross-functional team collaboration to Microsoft Teams and ask influencers to create [Channels in Teams](/microsoftteams/teams-channels-overview) for cross-functional team collaboration and to drive the conversations.
* Consider employees with high potential, not just top performers. Attributes that have contributed to past success may not predict future success. Broaden measures used to identify leaders to include those that assess potential, such as influence ranking.

For more best practices and how to identify and utilize influencers, see [Best practices for influencers](/viva/insights/tutorials/gm-influencer).

### Promote coaching and development

Manager one-on-one (1:1) time can improve engagement and job performance, while lack of manager coaching can cause employee disengagement and attrition.

One of the top best practices for promoting coaching and development is to require that managers schedule recurring 1:1 meetings with their direct reports for 30 minutes at least twice a month and hold them accountable for achieving that goal. See [Catch up with your team](/viva/insights/personal/use/use-the-insights#catch-up-with-your-team) for help with scheduling and managing your 1:1s.

For more best practices and how to develop a 1:1 conversation series, see [Best practices for manager coaching](/viva/insights/tutorials/gm-coaching).

### Empower employees

Cultivating autonomy and development are essential for employee engagement. When managers empower employees to make decisions and tackle new challenges, enables them to be more effective and reclaim time.

To increase information sharing:

* Use [Teams and OneNote](https://support.microsoft.com/office/add-a-onenote-notebook-to-teams-0ec78cc3-ba3b-4279-a88e-aa40af9865c2) to share meeting notes about decisions and action items as an alternative way to keep your team informed.
* Use [My team in Teams](/viva/insights/use/myteam) to identify ways to support team behavior.

For more best practices and how to set team meeting rules and policy, see [Best practices for meetings](/viva/insights/tutorials/gm-meetings).

