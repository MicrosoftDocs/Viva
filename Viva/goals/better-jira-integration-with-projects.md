---
title: "JIRA integration with projects"
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

description: "Need to see how your execution in JIRA is helping you achieve your key results? Now you can, using Viva Goals' new Projects feature"
---

# JIRA integration with projects

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

While Objectives and Key Results tell you what your goal is and how you will know when you got there, the best organizations also keep a laser focus on day to day execution to achieve their key results.

## What are projects

Projects help you keep track of all the work your organization is executing to achieve your OKRs. Like key results, projects can also be created under objectives and other key results in Viva Goals, depending on which outcome they help to achieve. You can create a project by clicking on **Add project** under the appropriate objective or key result.
  
The following are recommended ways to use Projects:

1. Objective that is tracked by a KPI metric: If a project must be completed to achieve the KPI metric, we recommend creating the project as a child of the Objective. Progress of the project will not roll up to the parent since it is KPI metric based.
  
1. Objective with multiple key results: Projects can be siblings to the key result, so you can see the outcomes needed to meet the objective (the key results) and the output needed to achieve those outcomes (the projects).

Projects are always placed after all the objectives and key results at each level of the hierarchy.

## JIRA projects

Projects in Viva Goals currently support JIRA, the popular project management system. Like the current JIRA integration, you can specify a JQL to retrieve the list of tasks from JIRA that constitute your project.

While Viva Goals supports a [JIRA integration](https://help.ally.io/en/articles/2285939-jira-integration) for OKRs, projects let you see the individual tasks and their completion state, helping you understand your execution at a much deeper level. The updates for a project also call out what has changed since the last checkin - which tasks were completed, were any tasks added or removed.

Viva Goals will periodically check on project progress in JIRA, and update status. Progress and Status is calculated for projects exactly like [key results](https://help.ally.io/en/articles/3065807-how-are-progress-and-status-calculated). Similar to key results, you can also check in on a project, where you can temporarily override the status. However, this override will last only as long as Viva Goals does not detect a change in the completion status of the project in JIRA, at which point, it will overwrite your checkin with an automated update.

## Current limitations with projects

Projects currently have the following limitations:

1. You cannot create unaligned, top-level projects. They must align to an objective or key result.
1. You cannot edit the alignment for a project when creating it. You can only create it under an existing objective or key result, and it will be aligned to that objective or key result.
1. Private Projects are not supported. Projects can be seen by all Viva Goals users.
1. You cannot clone projects, and you cannot perform bulk actions like changing time period on multiple projects at once.
1. Projects can have a maximum of 200 tasks.

Now you can understand how your teams are executing to meet your OKRs, and dive in to unblock them. In the future, we plan to add other popular project management systems, so that Viva Goals can give you a holistic view of your business.
