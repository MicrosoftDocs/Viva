---
title: "What are Projects?"
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

description: "Learn how to use Projects to monitor your execution in Viva Goals."
---

# What are Projects?

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

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

## How to add Projects

Projects can be enabled by your organization admin from the **Admin > OKR model configuration** dashboard as shown:

:::image type="content" source="../media/goals/viva-goals-add-projects-admin-dashboard.png" alt-text="Add Projects Admin Dashboard":::

In Viva Goals, Projects can exist at the Organization, Team, or Individual level. Like key results, projects can also be created under objectives and other key results in Viva Goals, depending on which outcome they help to achieve. To create a project, select **Add project** under the appropriate objective or key result.

:::image type="content" source="../media/goals/Project Creation.gif" alt-text="Project Creation Add Project":::

You can also create projects that aren't aligned to any OKR in the Projects Dashboard.

## Projects Dashboard

Apart from being aligned to OKRs, Projects also get their own dashboard in Viva Goals, so that you can monitor your execution. The dashboard is available at the individual, team and organization levels.

:::image type="content" source="../media/goals/Projects Tab.gif" alt-text="Project Creation Projects Tab":::

## How to structure Objectives, Key Results, and Projects?

The recommended structure is to have an Objective, with the Key Results and Projects under it. This way, you can see the outcomes needed to meet the objective (the key results) and the output needed to achieve those outcomes (the projects). Projects are always placed after all the objectives and key results at each level of the hierarchy. For example:

:::image type="content" source="../media/goals/viva-goals-structure-objectives-key-results-projects.png" alt-text="Structure Objectives, Key Results, and Projects":::

If you're an Enterprise customer, you can take advantage of [Viva Goals multi-alignment](https://help.ally.io/en/articles/3550399-multiple-alignment) and [alignment weights](https://help.ally.io/en/articles/3140710-weighted-objectives) features to have projects contribute to multiple objectives.

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

## FAQs

### Is my key result really a project?

Most key results that aren't KPI metric based are probably projects. The main questions to ask are:

- Is this key result really an outcome for the business, or is it an output on the way to an outcome?

- Can I follow the parent objective with **as measured by** and complete it with this key result in a convincing manner?

One good indicator that a key result may really be a project is if it's percentage-completion based and doesn't have any children. Another indicator is if the language is delivery-oriented, look for words like **Ship ...**, **Deliver ...**, **Implement...**.

If you want to try out your key result as a project or vice-versa, Viva Goals offers an easy way to do so without losing your updates to the key result or project. For more information, see [Converting OKRs to Projects and back](https://help.ally.io/en/articles/4271288-converting-okrs-to-projects-and-back).

### What pricing plans are projects supported on?

Projects in Viva Goals are available across all our pricing plans. The JIRA On Premise integration for Projects is only available for Enterprise Customers (JIRA Cloud is available across all plans). Reach out to your organization admin to have projects enabled for you.
