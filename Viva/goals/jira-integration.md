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

When you integrate Jira with Viva Goals, all updates on linked Jira user stories or epics are automatically tracked as progress on your objectives and key results (OKRs) in Viva Goals. This powerful functionality ensures that your OKR process isn't waiting for manual check-ins, as progress is updated in real time in Viva Goals.

Here are two scenarios where teams see the benefit of Viva Goals integration with Jira:

- A product manager links their objective, ship feature email campaign with an epic in Jira. As stories in the epic get completed, the objective gets closer to its goal.

- An engineering team resolves to fix 20 bugs in a quarter. They link their objective to an epic under which all bugs are filed, and they set the target of their key performance indicator (KPI) success metric to 20. Viva Goals records that objective has hit its goal when 20 bugs are closed.

## How to enable Jira integration

Admins follow these steps to enable integration:

1. From the sidebar, go to **Admin** and select the **Integrations** tab.
    
    :::image type="content" source="../media/goals/9/viva-goals-integrations-page.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/9/viva-goals-integrations-page.png":::

1. In Jira, you'll have an option to **Enable** the integration. If a connection was made previously or if the integration was already enabled, you'll have the option to **Manage** the enabled integration.
    
    :::image type="content" source="../media/goals/9/jira-enable-button.png" alt-text="Screenshot shows where you choose to enable Jira." lightbox="../media/goals/9/jira-enable-button.png":::

    The integration can be **disabled** from the same section: Go to **Change** and select **Disable integration** from the dropdown.
    
    :::image type="content" source="../media/goals/9/jira-disable-button.png" alt-text="Screenshot shows how to disable Jira in Viva Goals." lightbox="../media/goals/9/jira-disable-button.png":::

## How to configure the Jira connection

After you enable the integration, the first step is to configure a Jira connection:

1. Select **New Connection**, and provide a name for the connection.
    
   :::image type="content" source="../media/goals/9/jira-new-connection-button.png" alt-text="Screenshot shows where you name your new Jira connection." lightbox="../media/goals/9/jira-new-connection-button.png":::

1. Add the **Server URL** of your Jira account.
    
    :::image type="content" source="../media/goals/9/jira-configure-new-connection.png" alt-text="Screenshot shows where you configure a new Jira connection." lightbox="../media/goals/9/jira-configure-new-connection.png":::

1. For Jira instances in the cloud, enter the email address and the application programming interface (API) token associated with your Jira account. See the [instructions to generate an API token for your Jira cloud account](https://confluence.atlassian.com/cloud/api-tokens-938839638.html).

1. Select **Next** to get the integration running. You can edit the saved connection at any time.

In most cases, one connection is enough. But Viva Goals allows you to connect with multiple Jira instances. Select **New connection** to add another instance. You can add names to your connections to differentiate them. These names are displayed to members when they link their OKRs to Jira stories.

## How to link the Jira connection to an OKR

After you configure a connection, the next step is to link OKRs to stories or epics in Jira:

1. When you create or edit an OKR, select **Connect data source to auto-update progress**. From the drop-down menu, select **Jira**.
    
    :::image type="content" source="../media/goals/9/select-jira-datasource.png" alt-text="Screenshot shows where you select Jira as the data source." lightbox="../media/goals/9/select-jira-datasource.png":::

1. If you already created a connection or if your administrator shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections already created or shared.

1. Select the method you want to use to measure the progress of the key result, percent complete or KPI (success metric). If you choose KPI, provide a metric, starting value, and target value.

1. Select a connection, and add a JQL query to match any issues that would relate to the objective or key result. Jira issues that match the query will be linked to the success of the objective or key result.
    
    :::image type="content" source="../media/goals/9/jira-connection-details.png" alt-text="Screenshot shows where you add a Jira query." lightbox="../media/goals/9/jira-connection-details.png":::
    
    A JQL query can be copied from Jira. Search for issues you want to link to your objective by using the filters in Jira. Next, select the **Advanced** option, and Jira automatically converts your search into a JQL query. You can copy and paste the query string into your integration with Viva Goals.

   The JQL query linked to the objective or key result can be edited at any time. Any edit prompts a recalculation of current progress.

   > [!NOTE]
   > If you're using Jira next-gen projects, support for JQL behaves differently compared to classic Jira projects. For example, a Jira next-gen project doesn't support querying based on Epic links. For this scenarios, Jira states: 
   >
   >*Users should query on next-gen epics using the parent =. If you want to combine Epics from both project types, an example of such a query would be: "Epic Link" = NPC-6 OR parent = NJDP-5. The Parent field can now be selected as a column in the Global Issue Navigator and exported from Jira.*

1. Select the metric you want to use to track progress. For details about the Jira metrics supported, see the following table:

    | Track progress by | Percent complete | KPI |
    |---------|---------|---------|
    | Count of tickets | Percent of tickets that are marked as done out of the total number of tickets that match the specified JQL configuration. </br> Example OKR: Deliver the Jira integration by this quarter. </br> (Measured by the percent of completed tasks in this project) | Number of tickets that match the specified JQL configuration. </br> Example OKR: Complete 10 consultations this quarter. </br> (Measured by the number of consultation tickets marked as completed) |
    | Time spent | Percent of total hours spent on the completed ticket out of the total number of hours spent on tickets that match the specified JQL configuration. </br> Example OKR: Hit 100 percent of the billable hours this quarter. | Total hours spent on tickets that match the specified JQL configuration. </br> Example OKR: Complete 200 hours of consulting this quarter. |
    | Original estimate | Percent of total estimated hours on the completed tickets out of the total number of estimated hours on tickets that match the specified JQL configuration. </br> Example OKR: Achieve 80 percent velocity of features shipped. | Total estimated hours on tickets that match the specified JQL configuration. </br> Example OKR: Plan 350 hours of work for client A. |
    | Remaining estimate | N/A | Total remaining estimate on tickets that match the JQL configuration. </br> Example OKR: Ensure cost savings of 20 hours this quarter. |
    | Progress | N/A | Average of the progress metric on tickets that match the JQL configuration. The progress of a ticket in Jira is computed as *time logged/total time*. </br> Example OKR: Average 70 percent progress on training projects planned. |
    | [Story points] | Percent of story points on the completed tickets out of the total story points on tickets that match the specified JQL configuration. | Number of story points on the completed tickets out of the total story points on tickets that match the specified JQL configuration. |
    | Custom fields – These fields are available in your Jira instance. Viva Goals automatically pulls all the numeric custom fields in your Jira instance, and you can track their progress. | Track the percent complete of the associated numeric custom field in your Jira instance. | Track the total completion number of the associated numeric custom field in your Jira instance. |

    > [!NOTE]
    > For more information on Jira time and progress tracking, see this [Jira article](https://confluence.atlassian.com/jiraportfolioserver0326/tracking-progress-and-status-1005330901.html).

If you choose to track progress by KPI, you can toggle between the option to measure progress by completed tickets only or by all tickets.  

> [!NOTE]
> **Done** tickets include tickets with all statuses that are associated with the Jira **Done** workflow status category irrespective of the resolution status of the tickets. (See [How to create workflows for company-managed projects](https://support.atlassian.com/jira-core-cloud/docs/build-the-workflow-you-need/)).

## Examples of how Jira integration works  

Let's look at two different examples of how JIRA integration works. 

### Example 1

A product manager, Dana, links their objective (**Ship feature Email Campaigns**) with an epic in Jira. A simple JQL query used to set up the link could be: 

"Epic Link" = AE-786  
  
If the epic has 10 stories owned by different designers, engineers, and testers on the team, the progress of Dana’s objective would update every time one of the 10 stories gets closed. For instance, when three stories get closed in Jira, Viva Goals would automatically update the progress of the objective to 30 percent. If an 11th story gets added under the Epic, this progress gets recalculated to 27 percent.

### Example 2

Consider an objective to *Improve the overall quality of the product*. In this case, you might want to track the number of bugs generated as opposed to the progress of issues as an indicator of overall quality. You can use the **Count of Tickets** metric in the tracking field to achieve the desired setup. Viva Goals will automatically tally up all the tickets generated.

When an objective or key result is linked to Jira, members can see the Jira icon next to the progress bar that indicate a connection.

The following colors of the progress bar indicate the status of the objective:

- If the progress is 0 to 25 percent less than the expected progress at any time, the OKR status is *behind*, and the progress bar will be orange.

- If the progress is more than 25 percent less than expected progress at any point, the OKR status is *at risk*, and the progress bar will be red.

Viva Goals pulls in new updates from Jira every 60 minutes. However, you can also manually refresh to pull in any new changes.

## How to use the integration with projects 

While objectives and key results tell you what your goal is and how you'll know when you get there, the projects functionality helps keep teams focused on day-to-day execution to achieve key results.

### What are projects? 

Projects help you keep track of all the work your organization executes to achieve your OKRs. Like key results, projects can  be created under objectives and under other key results in Viva Goals, depending on which outcome they help to achieve. To create a project, select **Add project** under the objective or key result.

**There are two recommended scenarios for using projects:**

- **Objective is tracked by a KPI metric:** If a project must be completed to achieve the KPI metric, we recommend that you create the project as a child of the objective. Progress of the project won't roll up to the parent because it's KPI-metric based.

- **Objective has multiple key results:** Projects can be siblings to key results, so you can see outcomes needed to meet the objective (the key results) and the output needed to achieve those outcomes (the projects).

Projects are always placed after objectives and key results at each level of the hierarchy.

### How to integrate projects in Viva Goals and Jira 

Projects in Viva Goals currently support Jira, the popular project management system. Like the current Jira integration, you can specify JQL to retrieve the list of tasks from Jira that constitute your project.

While Viva Goals supports Jira integration for OKRs, projects let you see the individual tasks and their completion state. This functionality helps you understand your execution at a much deeper level. The updates for a project also call out what has changed since the last check-in: which tasks were completed and any tasks added or removed.

Viva Goals periodically checks on project progress in Jira and updates status. Progress and status are calculated for projects just like for key results. As with key results, you can also check in on a project, where you can temporarily override the status. However, this stage will last only as long as Viva Goals doesn't detect a change in the completion status of the project in JiraA, at which point it will overwrite your check-in with an automated update.

### Current limitations with projects

Projects currently have the following limitations:

- You can't create unaligned, top-level projects. They must align to an objective or key result.
- You can't edit the alignment for a project when you create it. You can only create it under an existing objective or key result, and it will be aligned to that objective or key result.
- Private projects aren't supported. Projects can be seen by all Viva Goals users.
- You can't clone projects, and you can't perform bulk actions like changing the time period on multiple projects at once.
- Projects can have a maximum of 200 tasks.

## How to track progress via Jira story points in Viva Goals 

As an organization adds complex projects, and it becomes increasingly challenging for teams to meet realistic deadlines. This is where project estimation comes handy. The estimation process doesn't have to be onerous. When it's done right, estimation catalyzes the accomplishment of multiple projects.

There are several estimation metrics. One is story points, which is an estimation metric in agile frameworks used for gauging the effort involved in implementing a work item. Story points in Jira help you estimate the backlog of work items during sprint planning.

### How to track progress of key results in Viva Goals using story points

The status of key results will be updated automatically depending on the story points completed in Jira.

When you create or edit a key result in Viva Goals, choose the method you want to use to measure progress: percent complete or KPI (success metric).

**If you choose to measure progress by the complete percentage:**

1. Select **Connect data source** to auto-update progress. From the drop-down menu, select Jira.

1. If you already created a connection or if your administrator shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections already created or shared.

1. Provide the JQL, and from the drop-down menu for tracking progress, select **Story Points**.

1. Select **Next** > **Save**.

**If you choose to measure progress by the KPI metric:**

1. The name of the metric will automatically be set as *Story Points* if you choose to track the progress by story points. However, you can customize the name for the metric. Set a target value and starting value.

1. Select **Connect data source** to auto-update progress. From the drop-down menu, select **Jira**.

1. If you already created a connection or if your administrator shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections already created or shared.

1. Provide the JQL, and from the drop-down menu for tracking progress, select **Story Points**. 

1. The **Count only done tickets** checkbox will be selected by default. If you want to measure the progress of the key result by story points of the completed tickets in Jira, this option is handy. However, if you want to measure the progress of the key result by story points of all the tickets pertaining to the JQL in Jira irrespective of the completion status, clear the checkbox.

1. Select **Next** > **Save**.

### How to track progress of projects in Viva Goals using story points

The status of projects will be updated automatically depending on the story points completed in Jira.

1. When you create or edit a project in Viva Goals, select **Select an option** to add tasks to the project. From the drop-down menu, select **Jira**.

    :::image type="content" source="../media/goals/9/jira-project-connection.png" alt-text="Screen shot shows where you select Jira connection for a project." lightbox="../media/goals/9/jira-project-connection.png":::

1. If you already created a connection or if your administrator shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections already created or shared.

1. Provide the JQL, and from the drop-down menu for tracking progress, select **Story Points**.

   All the tasks associated with the JQL will be listed, along with other task details like name, story points, assignee, and due date.

1. Select **Next** > **Save**.

### Common questions about using Jira story points in Viva Goals 

**Can I track progress by the custom fields in my Jira instance?** 

Yes, you can track the progress of key results and projects in Viva Goals by the custom field in your Jira instance. In addition to the metrics supported by Viva Goals, you can bring any numeric custom field from Jira to measure the progress.

**What's the difference between story points and story point estimates?** 

Jira has two types of service projects: classic and next-gen. The estimation on classic projects is story points, and the estimation on next-gen projects is story point estimates.
