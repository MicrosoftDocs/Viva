---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 02/07/2024
title: Use Leader reports to uncover key business outcomes
description: Learn how to use Leader reports in Viva Insights to view metrics and suggested actions focused on specific business outcomes.
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: helayne
audience: Admin
---

# Use Leader reports to uncover key business outcomes

>[!IMPORTANT]
> The features described below are for private preview customers only. Features in preview might not be complete and could undergo changes before becoming available in the broader public release.

Leader deep-dive reports in Viva Insights focus on customers, business operations, and agility. You can find these reports under **Team insights** in the Viva Insights app in Teams and on the web.

With these reports, leaders can view a variety of  metrics and suggested actions focused on specific business outcomes. Leaders can further drill down into the insights with custom filters such as time periods and breakdowns by group. [Learn more about filters in organization insights](./org-insights.md).

Each report includes three sections:

* Executive summary, which highlights the big changes compared to peers’ teams over the prior month

* Key metrics, which provide a deep dive into each topic, along with a “Why it matters” interpretation and recommended actions

* Metric comparison, which addresses the different business outcomes. In the trend graph, you can view the key metric averages (the key metric in the first data table column), and learn how they change over time. You can view a four-month distribution of averages for:

    * Your entire company

    * Peer organizations (if applicable)

    * Groups within your organization (that is, different reporting hierarchies within your company)

To add more organizations to your trend graph, under **Show trend**, select the eye icon. The trend graph only supports up to 20 organizations. To protect individual privacy, we don't show organizational insights if your organization is smaller than the minimum group size.

You can sort by any of the headers in the **Groups within your organization** table.

:::image type="content" source="./images/leader-reports-main.png" alt-text="Screenshot showing the Leader reports page." lightbox="../images/leader-reports-main.png":::

### Prerequisites 

To view these reports:

* Your Insights admin needs to assign you the **Insights Business Leader** role. With this role, you can access organization insights that include every measured employee in your tenant.

* Or, you’ve been assigned the **Group Manager** role, and you have a number of direct and indirect reports that meets or exceeds the minimum group size your Insights admin set. With this role, you can access organization insights that include people who report to you directly or indirectly.

* If you’ve been assigned both the **Insights Business Leader** role and the **Group Manager** role, you can view the relevant organization insights for either role. [Learn more about insights by role](./org-insights.md).

## Overview of the Leader reports

### New hire onboarding and integration

The **New hire onboarding and integration** report helps leaders understand the onboarding experience of new hires as well as the transition for employees who've started out in a new role within the company. The report also identifies opportunities to improve the onboarding and professional development experience.

Because research shows it takes new employees 12 months on average to reach their full performance potential, this report focuses on the entire 12-month period a new hire is learning, connecting, and developing in their new role.

This report can help you answer the following questions:

* How are new hires developing their network, and how fast are they integrating into the organization’s network?

* Are new hires getting the 1:1 coaching and support from their managers that they need?

* Is the organization sufficiently encouraging new hires and employees to set aside time for learning and training?

This report is powered by the following metrics:

| Metric | Definition |
|---|---|
| Internal network size for new hires | Number of people within the organization with whom a new hire has had a reciprocal interaction in the past four weeks. |
| Calendared learning time  | Number of hours blocked in a person’s calendar for learning activities. An appointment or meeting is considered a learning activity based on keywords that appear in the subject line. | 
| Meeting hours with manager 1:1 for new hires | Number of meeting hours involving only the new hire and their manager. |

**About learning-related keywords**

This report identifies calendar events as learning-related by using these keywords from meeting and appointment titles in Outlook:

* train

* learn

* course

* introduction

* onboarding

* induction

* academy

* education

* brown bag

* brownbag

### External focus

This report helps leaders understand how employees are managing external relationships, and how different parts of the company may have been impacted by business shifts.

Despite business changes, it’s important to ensure that relationships with customers, partners, and vendors stay strong. In times of change, internal demands can take precedence over time previously spent with external contacts. Those external contacts might also be refocusing their own priorities, and might not have time to meet with your organization.

This report can help leaders improve their strategies for communicating and collaborating with external groups. And for groups with *increased* external engagement, these insights can help leaders ensure these engagements don’t come at the expense of increased after-hours work.

This report is powered by the following metrics:

| Metric | Definition |
|---|---|
| External collaboration hours | Average time employees spent in meetings, emails, Teams calls, and Teams chats with at least one other person outside the company. |
| Employees' contact with external partners | Number of employees in meetings, emails, Teams calls, and Teams chats with at least one other person outside the company. |

### Urgent collaboration

This report helps leaders understand how employees manage unexpected demands, and in turn shift these demands to planned work. To enable this shift, the report provides these types of insights:

* Average time employees spend per week responding to urgent work requests

* The percentage of employees and work weeks involved in urgent collaboration

* The number of employees who worked on urgent email or meeting requests

* Average time employees spend per week in unscheduled Teams calls during and outside of working hours

This report identifies urgent collaboration using the following keywords in the email subject lines or meeting invitation titles:  

* urgent  

* immediately  

* ASAP  

* fire drill  

* immediate action

#### Privacy and engagement rates

Viva Insights respects user privacy. For this reason, Viva Insights does not show information about individuals, and when necessary to protect privacy, it reports approximated values in this way:

* **Below minimum:** For engagement rates lower than the minimum threshold, the threshold value is reported. For example, when 20 percent of 10 measured employees engage with a leader’s sent email, meetings, and shared files, Viva Insights displays the engagement rate as "< 25%."

* **Between thresholds:** If the actual engagement rate falls between the "Minimum" and "Maximum" values shown in the table, then the actual engagement rate is reported.

* **Above maximum:** For engagement rates higher than the maximum threshold, the threshold value is reported. For example, when 80 percent of 10 measured employees engage with a leader’s sent email, meetings, and shared files, Viva Insights displays the engagement rate as "> 75%."

Engagement rate thresholds:

| Number of employees | Engagement rate |
|---|---|
| 10-20 | Minimum: 25% <br> <br /> Maximum: 75% |
| > 21 | Minimum: 10% <br> <br /> Maximum: 90% |

[Learn more about privacy in Viva Insights](../advanced/privacy/privacy.md).
