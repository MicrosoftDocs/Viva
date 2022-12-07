---
title: Organization insights in the Viva Insights app
description: Find Organization insights in Microsoft Viva Insights 
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.collection: viva-insights-personal
ms.localizationpriority: medium 
ms.service: viva
ms.subservice: viva-insights
manager: anirudhbajaj
audience: user
---

# Organization insights in the Viva Insights app

Organization insights help leaders and managers of large teams understand how their organizations—the people who report to them directly or indirectly—are succeeding at work. Leaders and managers can see key indicators of their organization’s wellbeing, productivity, and team culture, and they can find features and tools to help support their teams.

Getting access

There are two ways for the Insights Administrator to grant access to organization insights:

•	They can assign a person to the Insights Business Leader role, or
•	They can enable a person as a Group Manager under Viva Insights 

Manager Settings

To be eligible to view organization insights, a person must have a premium Viva Insights license. Additionally, people in that person’s organization must also have a premium Viva Insights license for those people to be measured in an organizational insight. That means that for an Insights Business Leader to see an insight for their entire company, every person in their company must have a premium license.
People with the Insights Business Leader role can see organization insights that include every person in their tenant. People with the Group Manager role can see organization insights that only include people who report to them directly or indirectly. This reporting hierarchy is uploaded and maintained by the Insights Administrator. People with both the Insights Business Leader role and Group Manager role will be able to toggle between the two organization insights views.

Data and privacy

Viva Insights commits that no user will discover information about another identified individual that they didn’t already know. This principle applies to every feature in Viva Insights, including organization insights.

Organization insights are fundamentally different from the other features in Viva Insights: 

•	Organization insights give a person access to insights about other people based on information that they wouldn’t already have
•	All other insights only give a person access to insights about themselves or about how they interact with others based on data they already have available 
Because organization insights give a person new information about other people, the insights have protections in place to ensure that information cannot be tied to an identified individual. Organization insights apply three strategies to protect individual identity:
•	Minimum group size. Because it’s easier to guess information about an individual based on results about a smaller group, leaders and managers won’t see results for groups with fewer than 10 people. The Insights Administrator may choose to increase this threshold even further for additional protection.
•	Differential privacy. For simple averages and totals, there is a small amount of noise introduced into each calculation. The aggregated amount stays accurate, but this makes it impossible to add or subtract different values to figure out results for a single person.
•	Distribution tails. Some insights measure how many people have a certain profile, like what percentage of an organization gets enough focus time. Leaders and managers won’t see results that would otherwise reveal that “almost all” or “almost none” of the group fit the profile, because that would effectively give you information about every individual in the group.

Using organization insights

Organization insights are more than just a dashboard – they also provide helpful features to share insights and actions with your organization.

Insight scope selector. At the top of any page or section with organization insights, you will see an indicator showing how many people are being measured. If you have the group manager role, this is your reporting organization. If you have the Insights Business Leader role, this is the entire company. If you have both roles, you will be able to choose between the two views.

Insight indicators show you your organization’s average for the most recent period available, and how much it has changed from the period prior. 

Insight details can give you additional context for understanding the measured results. These details can include trend lines, peer comparisons, comparisons across groups within your organization, and distributions.

Sharing is available for most insight cards, and allow you to send a screenshot to another person, or provide a link to invite them to the same location in Viva Insights. Note that this link won’t give them access to the same data you can see, but if they also have access to organization insights, they will be able to see results for their own group.

Actions point you to other workflows in Viva Insights that can help support you or your organization to manage the measured behavior.

Helpful terms

Reporting hierarchy. The reporting hierarchy is managed by your Viva Insights administrator. It identifies reporting relationships throughout the company: people who are managers, and the people who report to them. The reporting hierarchy may be sourced from Azure Active Directory or from a manual upload from your company’s HR information system. It is used to identify people in your organization, your peer organization, and any organizations that might report up to you.

Current period. Unless otherwise stated, most insights are showing the result for the most recent period – that usually means the most recent complete week of data. A few insights use a four-week or rolling four-week window instead, to smooth normal variability and make it easier to understand the insight. If an insight uses something other than the most recent week for the current period, you will see it called out on the insight card.

Prior period. The prior period is the period immediately before the most recent period – usually the week before the most recent completed week.

Employees. Organization insights provide measures for groups of employees, and are meant to capture what typical workday activity looks like for those employees. To avoid skewing the averages by including people who are not at work during the week (for example, they are on holiday or out sick), organization insights only measure people who have some activity in Outlook or Teams during the week.
Your organization. If the insight scope selector says, “Your organization”, your this group includes everyone who reports to you directly or indirectly. It is based on your organization’s reporting hierarchy, which is managed by your Viva Insights administrator. If the insights scope selector says, “[Your company name]”, this group includes everyone who has been set up as part of the premium insights group by your Viva Insights administrator.

Peer organization. Peer organization includes groups near your own group in the reporting hierarchy. If available, the peer organization includes people who report directly or indirectly up to your manager, but not up to you. If there are no such groups, or they don’t meet the minimum group size, the peer organization includes people who report directly or indirectly up to your skip-level manager but not up to you. If there’s not enough people who meet that definition either, you will not see peer organization insights. 

Insights Business Leaders who are viewing insights for the entire company will also not see peer organization insights.

Organization breakdown. The groups displayed in the organization breakdown are based on your reporting hierarchy. Each group includes people who report directly or indirectly to a person who reports to you. The insights represent the activity of the group, not just that person who reports to you, even though their name is used to label the group. 

Insight Business Leaders who are viewing the insights for the entire company will see the organization breakdown by organizations reporting to top-layer leaders.

Metric definitions
You can find definitions for any metric used in an organization insight by clicking on the (i) icon next to the organization insight card or organization insight page title. 
Metric	How it’s calculated
After-hours collaboration hours	After-hours collaboration measures how much time per week a person spends in meetings, emails, Teams chats, and Teams calls outside of their configured working hours.

Uninterrupted focus hours	Uninterrupted focus hours measures blocks of time longer than an hour where the person is not in a meeting or Teams call or sending email or Teams chats. 

Daily active hours	Daily active hours measures time in 30-minute blocks in a day where the person had any activity where they took a meeting or Teams call or sent an email or Teams chat.
Collaboration hours	Collaboration hours measures the total time per week a person spends in meetings, emails, Teams chats, and Teams calls. 

Meeting hours	Meeting hours measures the total time per week a person spends in meetings based on accepted meetings on their Outlook calendar and excluding calendar items that are likely non-meetings, such as appointments.

Join on time rate	Join on time rate measures the percentage of Teams meetings where the person joined early or within five minutes of the meeting’s scheduled start time.

Recurring meeting hours	Recurring meeting hours measures the total time per week a person spends in recurring meetings based on accepted meetings on their Outlook calendar and excluding calendar items that are likely non-meetings, such as appointments.

Large and long meeting hours	Large and long meeting hours measures the total time per week a person spends in meetings that are longer than an hour or have more than 8 attendees.

Multitasking hours	Multitasking hours measures how much time per week a person spends in emails and chats that overlap with their meetings and Teams calls.

Manager 1:1 meeting hours	Manager 1:1 meeting hours measures how much time a person spends in meetings with just themselves and their direct manager. This is calculated over a rolling four-week period. 

Internal network size	Internal network size measures the number of colleagues connected to the person. Connections are based on at least two interactions in the prior four-week period, excluding very large and long interactions. 

Manager co-attendance rate	Manager co-attendance rate measures what percentage of meeting hours are attended by both the person and the person’s direct manager.

