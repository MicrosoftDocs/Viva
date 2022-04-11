---
title: "Native Projects"
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

# Native Projects

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## Projects in Viva Goals

Projects help you keep track of all the work your organization is executing to achieve your Objectives and Key Results (OKRs). Like key results, projects can also be created under objectives and other key results in Viva Goals, depending on which outcome they help to achieve. Select **Add project** under the appropriate objective or key result to create a project. To know more about Projects, see [getting started with Projects](https://help.ally.io/en/articles/4224975-what-are-projects).

There are **two ways of adding Projects in Viva Goals** – you can bring projects to Viva Goals through an integration with the project management tool you use, or you can create a project with a task list directly in Viva Goals.

## How to add Projects directly in Viva Goals?

- From the list view of your OKRs, you'll find an option to **Add Project** underneath the corresponding objective or key result.

- Alternately, you can add projects from the **Projects tab** where your entire list of projects will be populated.

    :::image type="content" source="../media/goals/ways of adding projects.gif" alt-text="Add Projects directly":::

- Provide the project details — title, type (individual, team, or organizational project), the project owner, and the time period.

- Under the **Outcome section**, you'll find two options to break down your project — either into milestones or by adding tasks to your project. For more details on adding Project Milestones, read our [help article](https://help.ally.io/en/articles/5406030-project-milestones-in-ally-io).

- As for adding tasks to your project, there are two ways in which you can add tasks — either directly in Viva Goals or through an integration. For more information on the project integrations we support, see [Projects](https://help.ally.io/en/articles/4224975-what-are-projects).

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

### FAQs

### How to manually order the tasks of a Project?

Users can sort the Tasks by *Name*, *Assignee* or *Due Date*.

Select either **Name**, **Assignee** or **Due Date** columns to expand the sort options.

> [!NOTE]
> This is possible only in the Full View of the Project that contains Tasks.

### Can I add a Due Date for a Task that is later than the end date of the Project?

We can add Tasks to a Project that are due even after the Project Time Period.

For example, if the Project has been created for Q4 2021 (October 2021 to December 2021), the user will be able to add a task with a Due Date of January 2022.

:::image type="content" source="../media/goals/viva-goals-due-date-for-task.png" alt-text="Due date for task":::

> [!NOTE]
> While saving the task, the application will indicate **Due date is after project’s end date** to the user but the task can still be saved.
> 
> :::image type="content" source="../media/goals/viva-goals-due-date-after-project-end-date.png" alt-text="Due date is after project end date":::

### Where can I find my tasks in Viva Goals?

The tasks are created for the Projects in Viva Goals and you'll find them listed under the Projects section.
