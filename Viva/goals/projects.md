---
title: "Projects"
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
localization_priority: Priority
ms.collection:  
- m365initiative-viva-goals
search.appverid:
- MET150

description: "Learn how to track your projects and tasks directly in Viva Goals."
---

# Projects in Viva Goals

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Projects help you keep track of all the work your organization is executing to achieve your Objectives and Key Results (OKRs). Like key results, projects can also be created under objectives and other key results in Viva Goals, depending on which outcome they help to achieve. Select **Add project** under the appropriate objective or key result to create a project.

There are **two ways of adding Projects in Viva Goals** – you can bring projects to Viva Goals through an integration with the project management tool you use, or you can create a project with a task list directly in Viva Goals.

## How to add Projects directly in Viva Goals?

- From the list view of your OKRs, you'll find an option to **Add Project** underneath the corresponding objective or key result.

- Alternately, you can add projects from the **Projects tab** where your entire list of projects will be populated.

    :::image type="content" source="../media/goals/ways of adding projects.gif" alt-text="Add Projects directly":::

- Provide the project details — title, type (individual, team, or organizational project), the project owner, and the time period.

- Under the **Outcome section**, you'll find two options to break down your project — either into milestones or by adding tasks to your project. 

- As for adding tasks to your project, there are two ways in which you can add tasks — either directly in Viva Goals or through an integration.

- You can **add tasks directly** by providing details such as task name, due date and owner.

    > [!NOTE]
    >
    > For key performance indicator (KPI) based projects:
    >
    > - If you are adding a KPI-based project, select **Add a metric** to specify the metrics of your project — the starting and target value, the unit, and what the metric is.
    >
    > - You can add tasks to your KPI-based project by selecting **Add tasks**. The task details you need provide are the task name, the owner, and the due date.
    >
    > - However, these tasks will not roll up to the project. You will still have the option to update the project progress either manually or automatically through an integration but you cannot update the progress automatically based on the completed tasks (though you can add tasks).
    >
    >     :::image type="content" source="../media/goals/kpi based projects.gif" alt-text="For adding KPI based projects":::
    >
- Once you've added your tasks, the next step is determining how the progress of the project will be calculated:

  - With tasks — project progress can be calculated either manually or automatically based on the completed tasks.

  - Without tasks — project progress will be calculated automatically from the connected data source.

- Align the project to an objective or key result, and select **Save**.

    :::image type="content" source="../media/goals/adding tasks.gif" alt-text="Align project to key result":::

Native projects can be seen on the OKR and Projects tabs for your entity showing the manual or rollup icon, implying that the progress is being updated either manually or based on the completion of native project tasks.

:::image type="content" source="../media/goals/viva-goals-native-projects-progress.png" alt-text="Native Projects Progress":::
    
## Clone Projects
    
Cloning projects is a quicker way of creating new projects while retaining the existing settings, and tasks pertaining to the cloned project. In addition, towards the end of a stipulated time period (for instance, end of a quarter), you might not have been able to make desired progress on a few projects, and might not have been able to get started on a few of them. You can carry unfinished projects in Viva Goals to the subsequent time period by simply cloning them. This is an efficacious method to roll over unfinished projects than editing the time period.

In this article, we'll show you when to clone projects, and how to do it.

### When to clone Projects?

Here’s when cloning might come in handy:

1. A quicker way to set new Projects for the current time period

2. An easier way to carry over unfinished Projects to a new time period

Say, you’ve spent the better part of your planning phase carefully creating Projects, delegating ownership, and adding due dates, that aligns with the Objectives and Key Results (OKRs). Within a team, most of them will have similar Projects based on the functionality — for instance, the Product Marketing Team will have projects that are similar, but support different features because the rollout plan for a feature release will remain the same. Instead of creating Projects all over again, you can clone the projects, make some quick edits, and hit the ground running. The ability to clone projects makes it simple to get set up quickly, while still allowing the flexibility for personalization.

While you’re scoring and closing OKRs, you stumble upon unfinished projects, which you would like to continue working on, and so you decide to roll them over to the subsequent time period — for instance, you have an objective to increase brand awareness by publishing 10 blogs. Owing to various reasons, you’re unable to publish 10, and end up getting five blogs out the door. You can clone this project to the next quarter, and continue to work on the remaining five blogs to accomplish your target. By cloning a project, you’re saving the progress in your current time period, and resetting the progress for the next time period. This is way more effective than editing the time period of projects.

### How to clone Projects?

1. Against a specific project, select **More actions** icon, and select **Clone**.

2. From the dialogue box, configure the following:  

    **Time period:** Viva Goals will default to the current time period (useful if you’re duplicating projects). If you're carrying over unfinished projects, select the appropriate time period from the dropdown menu.

    **Owner:** Choose to either retain the original owner, or assign a new one.

    **Entity type:** The Project can be assigned to an organization, a particular team, or a specific user.

    **Alignment:** By default, the cloned project will be unaligned. Select **Add alignment**, if you want the project to align with an objective.

    > [!NOTE]
    > Unaligned OKRs will be displayed only in the Projects dashboard, and not in the current time period view. Unless you align the project to an objective, you will not be able to see the Project in the current time period view.
    
## Projects Dashboard

Apart from being aligned to OKRs, Projects also get their own dashboard in Viva Goals, so that you can monitor your execution. The dashboard is available at the individual, team and organization levels.

:::image type="content" source="../media/goals/Projects Tab.gif" alt-text="Project Creation Projects Tab":::
    
## Project progress and status

Progress in Viva Goals is measured either as percentage complete or a key performance indicator (KPI) metric (for example, 10 out of 15 sales calls made). Projects currently use only the percentage complete method, as measured by tasks completed within the project.

By default, project progress does *not* roll up to the parent, to keep the focus on achieving key results (For more information, see: **[Roll Up Process of Key Results](https://help.ally.io/en/articles/1931651-roll-up-of-progress-of-key-results)**). However, this is controlled by an admin setting and can be overridden on a per project level. The admin setting decides the default (whether progress rolls up or not) when projects are created. Should you decide this default doesn't apply to your project, you can always change it from the project's settings.

:::image type="content" source="../media/goals/viva-goals-edit-alignment.png" alt-text="Edit Alignment":::

Viva Goals compared the progress of an item with its expected progress and computes a Status as outlined here **([OKR Status Indicators](https://help.ally.io/en/articles/3065807-okr-status-indicators))**. Status for projects is also computed in the same manner as OKRs.

**Project owners can do manual check-ins to provide the progress values (or) connect to a data integration to automatically update progress.**

You can choose to have a project without any tasks in Viva Goals and just check in manually to update the project progress.

:::image type="content" source="../media/goals/No Task list.gif" alt-text="Project Progress No Task list":::

If you would like to see the individual tasks in your project, you can create a task list directly in Viva Goals. Viva Goals also supports popular project management systems like JIRA, Asana and Wrike, with many more on the way. When you use a task list in Viva Goals or connect to these systems, progress of the project is automatically computed based on the number of tasks completed vs outstanding. You can edit a project to add an integration after creating it without one. When that happens, project progress will be recomputed based on the tasks, however your previous history of checkins will be maintained. You can read about Viva Goals' support for task lists, and popular integrations here:

- **[Native Projects](https://help.ally.io/en/articles/4397690-native-projects-in-ally)**

- **[Jira Integration with Projects](https://help.ally.io/en/articles/4097674-better-jira-integration-with-projects)**

- **[Asana Projects](https://help.ally.io/en/articles/4238088-asana-projects-in-ally)**

- **[Wrike Projects](https://help.ally.io/en/articles/4510436-wrike-projects-in-ally-io)**
    
## Best practices when thinking about Projects
    
A common mistake when writing Objectives and Key Results (OKRs) is to provide an execution plan instead of signing up for business outcomes. Let's take an example; Imagine a fictional organization that is developing a video gaming platform. They might have aspirations of taking over the North American video gaming market. But their OKRs might look like this:

**Objective:** Become the best gaming platform in North America.

- **Key Result:** Ship new version of gaming platform

- **Key Result:** Deliver social gaming features

While the organization can certainly achieve these key results, there's no guarantee accomplishing them will result in the objective being achieved. They are, at best, steps along the way to achieve your key results. In many cases, these steps are necessary before the key results can be achieved, and need to be monitored as much as the key results are.

In Viva Goals, we call these undertakings Projects - they're the outputs delivered by your organization's execution, whereas the key results are **outcomes**. Projects connect the strategic to the tactical by helping you keep track of your execution and making sure there are no bottlenecks. Ideally, project progress must *not* roll up to the objective, so you can stay focused on achieving the actual outcomes - the key results.

Coming back to our fictional organization, here's the same OKR written with projects in the picture:

**Objective:** Become the best gaming platform in North America.

- **Key Result:** Achieve 150M Monthly Active Users

- **Key Result:** Exceed 90% User Retention

- **Project:** Ship new version of gaming platform

- **Project:** Deliver social gaming features

- **Project:** Deliver high speed gaming backbone network

You can see that the projects aren't results themselves, but the work the company needs to do in order to get to the key results, or maximize their chances of achieving them. By showing key results and projects in a single view like this, an organization can have a conversation both about its strategy and the execution needed to get the strategic results.
    
### Structuring Objectives, Key Results, and Projects

The recommended structure is to have an Objective, with the Key Results and Projects under it. This way, you can see the outcomes needed to meet the objective (the key results) and the output needed to achieve those outcomes (the projects). Projects are always placed after all the objectives and key results at each level of the hierarchy. For example:

:::image type="content" source="../media/goals/viva-goals-structure-objectives-key-results-projects.png" alt-text="Structure Objectives, Key Results, and Projects":::

### FAQs

1. How to manually order the tasks of a Project?

A: Users can sort the Tasks by *Name*, *Assignee* or *Due Date*.

Select either **Name**, **Assignee** or **Due Date** columns to expand the sort options.

> [!NOTE]
> This is possible only in the Full View of the Project that contains Tasks.

2. Can I add a Due Date for a Task that is later than the end date of the Project?

A: We can add Tasks to a Project that are due even after the Project Time Period.

For example, if the Project has been created for Q4 2021 (October 2021 to December 2021), the user will be able to add a task with a Due Date of January 2022.

:::image type="content" source="../media/goals/viva-goals-due-date-for-task.png" alt-text="Due date for task":::

> [!NOTE]
> While saving the task, the application will indicate **Due date is after project’s end date** to the user but the task can still be saved.
> 
> :::image type="content" source="../media/goals/viva-goals-due-date-after-project-end-date.png" alt-text="Due date is after project end date":::

3. Where can I find my tasks in Viva Goals?

A: The tasks are created for the Projects in Viva Goals and you'll find them listed under the Projects section.

4. Is my key result really a project?

A: Most key results that aren't KPI metric based are probably projects. The main questions to ask are:

- Is this key result really an outcome for the business, or is it an output on the way to an outcome?

- Can I follow the parent objective with **as measured by** and complete it with this key result in a convincing manner?

One good indicator that a key result may really be a project is if it's percentage-completion based and doesn't have any children. Another indicator is if the language is delivery-oriented, look for words like **Ship ...**, **Deliver ...**, **Implement...**.

If you want to try out your key result as a project or vice-versa, Viva Goals offers an easy way to do so without losing your updates to the key result or project.
