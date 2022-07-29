---
title: "Jira Integration"
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: <TBD>
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals
search.appverid:
- MET150

description: "Learn how to integrate your OKRs in Viva Goals with Jira Views."
---

# Jira integration

Integrating Jira with Viva Goals allows any updates on linked Jira user stories or epics to automatically track progress on Objectives and Key Results (OKRs) in Viva Goals. This makes for a powerful setup because it ensures your OKR process isn't waiting on manual check-ins and any progress is updated real-time on Viva Goals.

Here are two scenarious where teams see the benefit of the Viva Goals integration with Jira:

1. A Product Manager links their Objective, Ship feature Email Campaign, with an epic in Jira. As stories within the epic get done, the objective gets closer to its goal.

2. An Engineering team resolves to fix 20 bugs in a quarter. They link their objective to an epic under which all bugs get filed, and set the target of their key performance indicator (KPI) success metric to 20. Viva Goals ensures that even when the number of bugs filed under the epic keeps growing, the objective has hit its goal as soon as 20 bugs are closed.

## How to enable the Jira integration

Admins can enable this integration by performing the following steps:

- From the sidebar, go to **Admin** and select the **Integrations** tab.
    
    :::image type="content" source="../media/goals/9/viva-goals-integrations-page.png" alt-text="Integrations page in Viva Goals." lightbox="../media/goals/9/viva-goals-integrations-page.png":::

- In Jira, you'll have an option to **Enable** the integration. If a connection has been made previously or if the integration has been enabled already, you'll have the option to **Manage** the enabled integration.
    
    :::image type="content" source="../media/goals/9/jira-enable-button.png" alt-text="Enabling Jira in Viva Goals." lightbox="../media/goals/9/jira-enable-button.png":::

- This integration can also be **disabled** from the same section. Go to **Change** and select **Disable integration** from the dropdown to disable the integration.
    
    :::image type="content" source="../media/goals/9/jira-disable-button.png" alt-text="Disabling Jira in Viva Goals." lightbox="../media/goals/9/jira-disable-button.png":::

## How to configure the Jira connection

- After you enable the integration, the first step is to configure a Jira connection.

- Select **New Connection**, and provide a name for the connection.
    
    :::image type="content" source="../media/goals/9/jira-new-connection-button.png" alt-text="Adding new Jira connection in Viva Goals." lightbox="../media/goals/9/jira-new-connection-button.png":::

- Add the **Server URL** of your Jira account.
    
    :::image type="content" source="../media/goals/9/jira-configure-new-connection.png" alt-text="Configuring new Jira connection in Viva Goals." lightbox="../media/goals/9/jira-configure-new-connection.png":::

- For Jira instances on the cloud, enter the email address and the Application Programming Interface (API) token associated with your Jira account. The instructions for generating an API token for your Jira cloud account are **[described here](https://confluence.atlassian.com/cloud/api-tokens-938839638.html)**.

- Select **Next** to get up and running with this integration. You can edit the saved connection at any time.

While in most cases one connection is enough, Viva Goals allows you to connect with multiple Jira instances. Select **New connection** to add another instance. You can add names to your connections to differentiate them. These names are displayed to members when they link their OKRs to Jira stories.

## How to connect the Jira connection to an OKR

Once you have configured the connection, the next step is to start linking OKRs to the stories or epics in Jira.

- While **creating or editing an OKR**, select **Connect data source to auto-update progress**. From the drop-down menu, select **Jira**.
    
    :::image type="content" source="../media/goals/9/select-jira-datasource.png" alt-text="Selecting Jira from the list of data sources in Viva Goals." lightbox="../media/goals/9/select-jira-datasource.png":::

- If you've already created a connection, or if your administrator has shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections created or shared.

- Select the method using which you want to measure the progress of the key result—percent complete or KPI (success metric). If you're choosing KPI, provide a metric, starting value, and target value.

- Select a connection, and add a JQL query to match any issues that would relate to the objective or key result. This also means that as more issues in Jira match the query, they keep getting linked to the success of the objective or key result.
    
    :::image type="content" source="../media/goals/9/jira-connection-details.png" alt-text="Adding new Jira connection to OKRs in Viva goals." lightbox="../media/goals/9/jira-connection-details.png":::
    
    A JQL query can be copied from Jira. Search for issues you want to link to your objective using available filters on Jira. Next, select the **Advanced** option and Jira automatically converts your search to a JQL query. You can copy and paste the query string into your integration with Viva Goals.

The JQL query linked to the objective or key result can be edited at any given point in time. This leads to a recalculation of current progress.

> [!NOTE]
> If you are using Jira next-gen projects, the support for JQL can behave slightly different compared to classic Jira projects. For example, a Jira next-gen project does not support query based on epic link. Here is an official Jira quote summarizing this scenario, "Users should query on next-gen epics using the parent =. If you want to combine Epics from both project types, an example of such a query would be: "Epic Link" = NPC-6 OR parent = NJDP-5. The Parent field can now be selected as a column in the Global Issue Navigator and exported from Jira."

- Select the metric you want to use to track progress. For more information on the Jira metrics supported, see the following tabular column:

    | Track progress by | Percent complete | KPI |
    |---------|---------|---------|
    | Count of tickets | % of tickets that are marked as done out of the total number of tickets that match the specified JQL configuration. </br> Example OKR: Deliver the Jira integration by this quarter. </br> (Measured by the % of completed tasks in this project) | Number of tickets that match the specified JQL configuration. </br> Example OKR: Complete 10 consultations this quarter. </br> (Measured by the number of consultation tickets marked as completed) |
    | Time spent | % of total hours spent on the completed ticket out of the total number of hours spent on tickets that match the specified  JQL configuration. </br> Example OKR: Hit 100% of the billable hours this quarter. | Total hours spent on tickets that match the specified JQL configuration. </br> Example OKR: Complete 200 hours of consulting this quarter. |
    | Original estimate | % of total estimated hours on the completed tickets out of the total number of estimated hours on tickets that match the specified JQL configuration. </br> Example OKR: Achieve 80% velocity of features shipped. | Total estimated hours on tickets that match the specified JQL configuration. </br> Example OKR: Plan 350 hours of work for client A. |
    | Remaining estimate | N/A | Total remaining estimate on tickets that match the JQL configuration. </br> Example OKR: Ensure cost savings of 20 hours this quarter. |
    | Progress | N/A | Average of the progress metric on tickets that match the JQL configuration. The progress of a ticket in Jira is computed as Time logged/Total time. </br> Example OKR: Average 70% progress on training projects planned. |
    | [Story points] | % of story points on the completed tickets out of the total story points on tickets that match the specified JQL configuration. | Number of story points on the completed tickets out of the total story points on tickets that match the specified JQL configuration. |
    | Custom fields – these are fields available in your Jira instance. Viva Goals will automatically pull all the numeric custom fields in your Jira instance, and you'll be able to track the progress by any of the Jira custom fields. | Track the percent complete of the associated numeric custom field in your Jira instance. | Track the total completion number of the associated numeric custom field in your Jira instance. |

    > [!NOTE]
    > For more information on how Jira does time and progress tracking, visit this [Jira article](https://confluence.atlassian.com/jiraportfolioserver0326/tracking-progress-and-status-1005330901.html).

If you choose to track the progress by KPI, you will have the option to measure progress by completed tickets only or all tickets by toggling the checkbox.  

> [!NOTE]
> **Done** tickets include tickets with all statuses that is associated with the Jira's **Done** workflow status category irrespective of the resolution status of the tickets ([reference to Jira article](https://support.atlassian.com/jira-core-cloud/docs/build-the-workflow-you-need/)).

## Examples of how the Jira integration works  

Let’s look at two different examples of how the JIRA integration works. 

### Example 1

A Product Manager, Dana, links their objective (**Ship feature Email Campaigns**) with an epic in Jira. A simple JQL query used to set up the link could be: "Epic Link" = AE-786  
  
If the epic has 10 stories, owned by different designers, engineers and testers in the team, the progress of Dana’s objective would update every time one of the 10 stories gets closed. For instance, when three stories get closed in Jira, Viva Goals would automatically update the progress of the objective to 30%. If an eleventh story gets added under the Epic, this progress gets recalculated to 27%.

### Example 2

Consider the objective: **Improve the overall quality of the product**. In this case, you might want to track the number of bugs generated as opposed to the progress of issues, as an indicator of overall quality. You can use the **Count of Tickets** metric in the tracking field to achieve the desired setup. Viva Goals will automatically tally up all the tickets generated.

When an objective or key result is linked to Jira, members can see the Jira icon next to the progress bar indicating there's a connection.

The following colors of the progress bar indicate the status of the objective:

- If the progress is 0 - 25% less than the expected progress at any given point in time, the OKR status is Behind, and the progress bar color will be Orange.

- If the progress is over 25% less than the expected progress at any given point in time, the OKR status is At Risk, and the progress bar color will be Red.

Viva Goals pulls in new updates from Jira every 60 minutes. However, you can also manually refresh to pull in any new changes.

## How to use the Jira integration with Projects 

While Objectives and Key Results tell you what your goal is and how you will know when you get there, using the Projects function keeps teams laser focused on day-to-day execution to achieve key results.

### What are Projects? 

Projects help you keep track of all the work your organization is executing to achieve your OKRs. Like key results, projects can also be created under objectives and other key results in Viva Goals, depending on which outcome they help to achieve. You can create a project by clicking on Add project under the appropriate objective or key result.

**There are two recommended scenarios for using Projects:**

**1. Objective is tracked by a KPI metric:** If a project must be completed to achieve the KPI metric, we recommend creating the project as a child of the Objective. Progress of the project will not roll up to the parent since it is KPI metric based.

**2. Objective has multiple key results:** Projects can be siblings to key results, so you can see outcomes needed to meet the objective (the key results) as well as the output needed to achieve those outcomes (the projects).

Projects are always placed after objectives and key results at each level of the hierarchy.

### How to integrate Projects in Viva Goals and Jira 

Projects in Viva Goals currently support JIRA, the popular project management system. Like the current JIRA integration, you can specify a JQL to retrieve the list of tasks from JIRA that constitute your project.

While Viva Goals supports a JIRA integration for OKRs, projects let you see the individual tasks and their completion state, helping you understand your execution at a much deeper level. The updates for a project also call out what has changed since the last checkin - which tasks were completed, were any tasks added or removed.

Viva Goals will periodically check on project progress in JIRA, and update status. Progress and Status is calculated for projects exactly like key results. Similar to key results, you can also check in on a project, where you can temporarily override the status. However, this will last only as long as Viva Goals does not detect a change in the completion status of the project in JIRA, at which point, it will overwrite your checkin with an automated update.

### Current limitations with Projects

Projects currently have the following limitations:

1. You cannot create unaligned, top-level projects. They must align to an objective or key result.
2. You cannot edit the alignment for a project when creating it. You can only create it under an existing objective or key result, and it will be aligned to that objective or key result.
3. Private Projects are not supported. Projects can be seen by all Viva Goals users.
4. You cannot clone projects, and you cannot perform bulk actions like changing time period on multiple projects at once.
5. Projects can have a maximum of 200 tasks.

## How to track progress via Jira story points in Viva Goals 

Each organization takes on ambitious projects that are complex, and it becomes increasingly challenging for teams to meet realistic deadlines. This is where project estimation comes handy. The process of estimation doesn't have to be onerous. Done right, it catalyzes the accomplishment of multiple projects.

There are several estimation metrics, and one such metric is story points. Story points is an estimation metric in agile frameworks used for gauging the effort involved in implementing a work item. Story points in Jira help in estimating the backlog work items during every sprint planning.

### How to track progress of key results in Viva Goals using story points

The status of key results will be updated automatically depending on the story points completed in Jira.

While creating or editing a key result in Viva Goals, choose the method using which you want to measure the progress—percent complete or KPI (success metric).

**If you choose to measure progress by the complete percentage:**

- Select Connect data source to auto-update progress. From the drop-down menu, select Jira.

- If you have already created a connection, or if your administrator has shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections created or shared.

- Provide the JQL, and from the drop-down menu for tracking progress, select Story Points.

- Select Next > Save.

**If you choose to measure progress by the KPI metric:**

The name of the metric will automatically be set as 'Story Points' if you choose to track the progress by story points. However, if you wish to have a different one, you can provide the name for the metric. Set a target value and starting value.

- Select Connect data source to auto-update progress. From the drop-down menu, select Jira.

- If you have already created a connection, or if your administrator has shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections created or shared.

- Provide the JQL, and from the drop-down menu for tracking progress, select Story Points. 

- The checkbox for 'Count only done tickets' will be ticked by default. If you want to measure the progress of the key result by story points of the completed tickets in Jira, this option comes handy. However, if you want to measure the progress of the key result by story points of all the tickets pertaining to the JQL in Jira, irrespective of the completion status, you can uncheck the box.

- Select Next > Save.

### How to track progress of projects in Viva Goals using story points

The status of projects will be updated automatically depending on the story points completed in Jira.

- While creating or editing a project in Viva Goals, select Select an option to add tasks to project. From the drop-down menu, select Jira.

    :::image type="content" source="../media/goals/9/jira-project-connection.png" alt-text="Selecting Jira connection for Projects in Viva goals." lightbox="../media/goals/9/jira-project-connection.png":::

- If you have  already created a connection, or if your administrator has shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections created or shared.

- Provide the JQL, and from the drop-down menu for tracking progress, select Story Points.

- All the tasks associated with the JQL will be listed, along with additional task details—name, story points, assignee, and due date.

- Select Next > Save.

### Common questions about using Jira story points in Viva Goals 

**1. Can I track progress by the custom fields in my Jira instance?** 

Yes, you can track the progress of key results and projects in Viva Goals by the custom field in your Jira instance. In addition to the metrics supported by Viva Goals, you can bring any numeric custom field from Jira to measure the progress. To know more about using custom fields, read our article on Jira integration.

**2. What is the difference between story points and story point estimates?** 

Jira has two types of service projects: classic and next-gen. The estimation on classic projects is story points, and the estimation on next-gen projects is story point estimates. 
