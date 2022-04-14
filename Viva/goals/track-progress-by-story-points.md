---
title: Track progress by story points
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: 
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
localization_priority: Priority
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Measure the progress of OKRs in Viva Goals by story points in Jira."
---

# Track progress by story points

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## Introduction to Story Points 

Each organization takes on ambitious projects that are complex, and it becomes increasingly challenging for teams to meet realistic deadlines. This is where project estimation comes handy. The process of estimation doesn't have to be onerous. Done right, it catalyzes the accomplishment of multiple projects. 

There are several estimation metrics, and one such metric is story points. Story points is an estimation metric in agile frameworks used for gauging the effort involved in implementing a work item. Story points in Jira help in estimating the backlog work items during every sprint planning. 

## How do I set up Jira integration? 

To hit the ground running with Jira integration in Viva Goals, here's what you need to do: 

- From the navigation menu, select **Admin >** select the **Integrations** tab.

- Against Jira, you'll have an option to **Enable** the integration. If a connection has been made previously or if the integration has been enabled already, you'll have the option to **Manage** the enabled integration.

- This integration can also be **disabled** from the same section by clicking on **Change**, and **choosing Disable integration** from the dropdown.

    :::image type="content" source="../media/goals/goals-enable-jira-integration.gif" alt-text="Image of Jira integration":::

If you need additional help in setting up your connection, read our help article on [Jira integration.](https://help.ally.io/en/articles/2285939-jira-integration)

## Track progress of key results in Viva Goals by story points 

The status of key results will be updated automatically depending on the story points completed in Jira. 

- While **creating or editing a key result in Viva Goals**, choose the method using which you want to measure the progress—percent complete or KPI (success metric). 

**If you choose to measure progress by the complete percentage**:

- Select **Connect data source to auto-update progress**. From the drop-down menu, select **Jira**. 

- If you've already created a connection, or if your administrator has shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections created or shared.

- Provide the **JQL**, and from the drop-down menu for **tracking progress**, select **Story Points**. 

- Select **Next > Save**. 

**If you choose to measure progress by the KPI metric**:

- The name of the metric will automatically be set as 'Story Points' if you choose to track the progress by story points. However, if you wish to have a different one, you can provide the name for the metric. Set a target value and starting value.  

- Select **Connect data source to auto-update progress**. From the drop-down menu, select **Jira**. 

- If you've already created a connection, or if your administrator has shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections created or shared.

- Provide the **JQL**, and from the drop-down menu for **tracking progress**, select **Story Points**. 

- The checkbox for 'Count only done tickets' will be ticked by default. If you want to measure the progress of the key result by story points of the completed tickets in Jira, this option comes handy. However, if you want to measure the progress of the key result by story points of all the tickets pertaining to the JQL in Jira, irrespective of the completion status, you can uncheck the box. 

- Select **Next > Save**. 

    :::image type="content" source="../media/goals/goals-jira-sp-kr.gif" alt-text="Image of progress by the KPI metric":::

## Track progress of projects in Viva Goals by story points 

The status of projects will be updated automatically depending on the story points completed in Jira. 

- While creating or editing a project in Viva Goals, select **Select an option to add tasks to project**. From the drop-down menu, select **Jira**.

- If you've already created a connection, or if your administrator has shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections created or shared.

- Provide the **JQL**, and from the drop-down menu for **tracking progress**, select **Story Points**.

- All the tasks associated with the JQL will be listed, along with additional task details—**name, story points, assignee, and due date**. 

- Select **Next > Save**.

    :::image type="content" source="../media/goals/goals-jirasp-projects.gif" alt-text="Image of track progress of projects by story points ":::

Best practice

For Jira issues that don't have an estimation, the average of story points of the remaining issues in the specified JQL will be assigned automatically. As best practice, Viva Goals sets the default value of story points for non-estimated Jira issues to the average value, and this will help in measuring the progress in a meaningful way than just using 0 as the default value. 

Say, you have 3 issues, out of which 2 issues have the estimation as 4 story points and 5 story points respectively. If the third issue doesn't have a story point estimate, the default value will be average of story points of the other two issues, which would be 4.5.

## Common questions 

#### 1. Can I track progress by the custom fields in my Jira instance? 

Yes, you can track the progress of key results and projects in Viva Goals by the custom field in your Jira instance. In addition to the metrics supported by Viva Goals, you can bring any numeric custom field from Jira to measure the progress. To know more about using custom fields, read our article on [Jira integration.](https://help.ally.io/en/articles/2285939-jira-integration) 

#### 2. What's the difference between story points and story point estimate? 

Jira has two types of service projects—classic and next-gen. The estimation on classic projects is story points, and the estimation on next-gen projects is story point estimate. 