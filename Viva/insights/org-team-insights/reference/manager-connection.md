---
ms.date: 02/14/2023
title: Manager connection in Viva Insights
description: Learn about how to enhance manager connection with recommendations in Microsoft Viva Insights
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
ms.collection: 
- m365initiative-viva-insights 
- viva-insights-leader
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: helayne
audience: Admin
---

# Manager connection

Because a focus on *coaching* and *empowering* employees sets your team up to deliver their best, Microsoft Viva Insights uses these two elements make up the Manager connection framework. This article explains how to leverage best practices for coaching and empowerment, and how related insights are calculated.

You can find the **Manager connection** page in the Viva Insights app, within the **Organization trends** tab.

![Screenshot that shows the Manager connection page.](../../Images/WpA/Use/org-manager-connection1.png)

## Coaching

### Engage with directs through regular 1 on 1 meetings

:::image type="content" alt-text="Screenshot of the app that shows the 'Engage with directs through regular 1 on 1 meetings' insight, with a percentage insight, a distribution of monthly 1:1 time with managers, and a 'Take action' section." source="../../Images/WpA/Use/org-trends-connection-coaching.png":::

#### Insights

For **Engage with directs through regular 1 on 1 meetings**, the **Manager connection** page provides a percentage insight that shows how many employees meet with their manager for less than one hour a month and a visual insight that shows the distribution of monthly 1:1 time with managers.

Here's some information about how those metrics are calculated:

Percentage insight |Metric | Calculation| 
|----------|-----------|----------------|
|Percentage of employees who have less than one hour of 1:1 time with their managers each month| [Meeting hours with manager 1:1](../../advanced/reference/metrics.md#meeting-hours-with-manager-1-1-define)| The percentage of employees who spend less than one hour of coaching time with their managers each month. This percentage is calculated monthly and averaged over the entire time period.|

|Visual insight| Definition|
|--------------|-----------|
Distribution 1:1 time with managers each month| Shows the percentage of employees based on their monthly average number of meeting hours with manager 1:1. They are divided into employees who have no 1:1s, between zero and one hour, and more than one hour of 1:1s with their manager in a month. These percentages are calculated monthly and averaged over the entire time period. This graph also uses the influence metric.

#### Best practices

Manager 1:1 time can improve engagement and job performance, while a lack of manager coaching can contribute to employee disengagement and attrition. According to the research referenced in [What great managers do daily](https://insights.office.com/productivity/what-great-managers-do-daily/): "A Gallup study found that at least 70 percent of the variance in employee engagement scores is driven by who the boss is."

Here are ways to engage with directs through 1:1 meetings:

* Schedule recurring 1:1s. One of the top best practices for promoting coaching and development is to require that managers schedule recurring 1:1 meetings with their direct reports for 30 minutes at least twice a month and hold them accountable for achieving that goal. See [Catch up with your team](../../personal/use/use-insights.md#catch-up-with-your-team) for help with scheduling and managing your 1:1s.

* Prepare discussion points, but stay flexible. While 1:1s are best with some structure, flexibility allows you and your directs to talk about top-of-mind topics.
* Use Viva Insights to automatically schedule 1:1 time, receive reminders to do so, and follow up on tasks related to direct reports.

For more best practices and how to develop a 1:1 conversation series, see [Best practices for manager coaching](../../tutorials/gm-coaching.md).

## Empowerment

### Promote autonomy through guidance and support

:::image type="content" alt-text="Screenshot that shows the 'Promote autonomy through guidance and support' insight,  with a percentage insight, a distribution of manager-employee coaching relationships, and a 'Take action' section." source="../../Images/WpA/Use/org-trends-connection-empowerment.png":::

#### Insights

For **Promote autonomy through guidance and support**, the **Manager connection** page provides a percentage insight that shows how many employees have their managers attend a majority of their meetings and a visual insight that shows the distribution of manager-coaching relationships.

Here’s some information about how those metrics are calculated:

|Percentage insight |Metric| Calculation|
|-------------------|------|------------|
|Percentage of employees who have a majority of their meetings attended by their manager|[Meeting hours with manager](../../advanced/reference/metrics.md#meeting-hours-with-manager-define) and [meeting hours](../../advanced/reference/metrics.md#meeting-hours-define)|The percentage of employees who spend over 50 percent of their meeting hours with their manager in attendance. This percentage is calculated weekly and averaged over the entire time period.|

|Visual insight| Definition|
|--------------|-----------|
|Distribution of manager-employee coaching relationships |Uses the average time employees spend with their [managers in 1:1s](../../advanced/reference/metrics.md#meeting-hours-with-manager-1-1-define) and the percentage of [meeting hours with the manager](../../advanced/reference/metrics.md#meeting-hours-with-manager-define) in attendance. The different manager-employee coaching relationships are grouped by employee time percentages, which are weekly averages based on monthly calculations: <ul><li>**Coached** – An employee who spends more than 15 minutes in 1:1s and less than 30 percent of their meeting hours with their managers in attendance.</li><li>**Co-attended** – An employee who spends less than 15 minutes in 1:1s and more than 30 percent of their meeting hours with their managers in attendance. </li><li>**Micromanaged** – An employee who spends more than 15 minutes in 1:1s and more than 30 percent of their meeting hours with their managers in attendance. </li><li>**Under-coached** – An employee who spends less than 15 minutes in 1:1s and less than 30 percent of their meeting hours with their managers in attendance. </li> |

#### Best practices

When managers empower their employees to make decisions and tackle new challenges, it provides growth opportunities for employees while freeing up time for managers to get work done.

[How to boost your team’s productivity](https://insights.office.com/productivity/how-to-boost-your-teams-productivity/) explains that "helping your team manage its time well is a critical factor for its success."

Here are ways to promote autonomy through guidance and support:

* Encourage others on your team to take the lead. If you’re unable to attend a meeting, provide some notes in advance and delegate another team member to lead it.
* Use Teams to share meeting recordings and notes about decisions and action items as an alternative way to keep your team informed.

For more best practices and how to set team meeting rules and policy, see [Best practices for meetings](../../tutorials/gm-meetings.md).

## Insights for leaders

If you're assigned the **Insights Business Leader** role in Microsoft Viva Insights, you'll find some additional information on the **Manager connection** tab. Specifically, the following insights are available to you.

### Empowerment

#### Empower teams by emphasizing the role of managers as connectors

![Screenshot that shows the influencers insight.](../../Images/WpA/Use/org-leader-empowerment1.png)

##### Insights

For **Empower teams by emphasizing the role of managers as connectors**, the **Manager connection** page provides a percentage insight that shows the share of employees that can be reached via the most influential employees and a visual insight that shows how these influencers are connected across the larger organizational network. 

Here's some information about how those metrics are calculated:

|Percentage insight |Metric| Calculation|
|-------------------|------|------------|
|Percentage of teams composed of individuals tightly connected across workstreams|Influence*|Count of employees who are connected to top influencers divided by the total number of measured employees.|

|Visual insight| Definition|
|--------------|-----------|
Reach of influencers | Each employee is represented by a dot with dot size scaled by that employee’s influence score. Dot coloration indicates whether that individual is classified as a top influencer. 

<sup>\* Influence indicates, as a numeric score, how well connected a person is within the company. A higher score means that the person is better connected and has greater potential to drive change. (A person’s connection score is based on the frequency of collaboration activities, which include emails, meetings, Teams calls, and Teams chats with other people within the company.) Type: Score.</sup>

##### Best practices

Influencers are people within an organization who are well connected and can drive innovation by efficiently sharing information with others.

The [Measuring your employees’ invisible forms of influence](https://insights.office.com/productivity/measuring-your-employees-invisible-forms-of-influence/) article says that "traditional organizational reporting structures limit managers’ visibility into how their employees are influencing and contributing to other teams. New workplace metrics are needed to help leaders get a more complete picture of this." 

Here are a couple of ways to leverage influencers:

* Use [Insights](../../personal/use/use-insights.md) and the [Stay connected](../../personal/teams/reference/viva-insights-stay-connected.md) page to see connections, top collaborators, and suggestions on how to improve connections and cultivate influence.
* Use [Microsoft Teams channels](/microsoftteams/teams-channels-overview) for cross-functional team collaboration and to drive conversations.

#### Incorporate fresh ideas and perspectives through broad manager networks

![Screenshot that shows the team cohesion insight.](../../Images/WpA/Use/org-leader-empowerment2.png)

##### Insights

For **Incorporate fresh ideas and perspectives through broad manager networks**, the **Manager connection** page provides a percentage insight that shows the share of managers that have many unique ties and a visual insight that shows how these managers are connected across the larger organizational network.

Here's some information about how those metrics are calculated:

|Percentage insight |Metric| Calculation|
|-------------------|------|------------|
|Percentage of managers connected to few people outside of their own teams|Diverse ties*|Binary determination, based on whether each manager’s count of diverse ties places them within the top vs. bottom half compared to all measured managers within the company.|

|Visual insight| Definition|
|--------------|-----------|
Reach of influencers | Each employee is represented by a dot with dot size scaled by that employee’s influence score. Dot coloration indicates whether that individual is classified as a top influencer.

<sup>\* Diverse ties indicate how varied and how broad a person's connections are, based on both the infrequent direct collaboration between two people and on the differences in the common network they share between themselves. (Collaboration activities consist of emails, meetings, Teams calls, and Teams chats.) A person doesn't need to have much direct collaboration with their diverse ties, so it’s easy to have more diverse ties than strong ties. Diverse ties present good sources of fresh and varied information from across the company. Type: Count.</sup>

##### Best practices

Managers who have diverse ties across an organization are typically considered more effective and help their employees build strong networks.

In the [Empowering your employees to empower themselves](https://insights.office.com/management-strategy/empowering-your-employees-to-empower-themselves/) article: "Your employees understand their jobs. They know their tasks, roles, and functions within the organization, and it’s time for you to let them do what they need to do to get the job done." 

Here are some ways to foster connectivity:

* Create cross-team communities for people with similar interests to share ideas, knowledge, and resources. This can also be done using [Teams channels](/microsoftteams/teams-channels-overview).
* Enable and use the [Viva Insights Outlook add-in](../../personal/use/use-insights.md) and [Stay connected](../../personal/teams/reference/viva-insights-stay-connected.md) to add colleagues to your **Important people** list, receive suggestions to meet, reminders to respond to emails, and complete tasks for these contacts. And urge your team to do the same.
* Create a shared [Teams channel](/microsoftteams/teams-channels-overview) to strengthen connectivity through channel interactions about projects, strategic topics, and goals to enable information sharing, brainstorming, and team building.
