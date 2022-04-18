---
title: "Asana Integration"
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

description: "Learn how to use the Asana integration with your OKRs."
---

# Asana Integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## About Asana Integration

Viva Goals can integrate with Asana projects to automatically update your Objectives and Key Results (OKRs) in Viva Goals. The OKRs progress is calculated by the number of tasks or subtasks that have been completed in Asana. This integration works for both types of measuring progress: Percentage Completed or key performance indicator (KPI) progress.

For example, you're a marketer using Asana to work on a customer advisory project. You would set an objective to curate a list of customer executives onboard from different regions. Use the Asana integration to easily keep track of the completed list. Viva Goals will sync the values for you and chart your progress toward the goal, thus saving time while keeping your OKRs current.

## Set up

An admin can set up the Asana integration on Viva Goals. To do so:

1. Navigate to Viva Goals’ integrations page through **Admin -> Integrations**.

2. **Enable** the Asana integration.

3. Select **New Connection** and in the popup that follows, sign in to your Asana account. Next, configure Asana connections that can be used by Viva Goals users to link their OKRs and update progress.

    :::image type="content" source="../media/goals/viva-goals-asana-integration-1.png" alt-text="Asana Integration 1":::

4. Select‘**Next** to finish the setup.

Viva Goals allows you to connect with multiple Asana accounts. Select **New connection** to add another and differentiate them using names. These names are displayed to members when they link their OKRs to Asana projects.

## How to use Asana Integration?

Once the setup is complete, users in your organization can link their OKRs to Asana projects by performing the following steps:

1. While creating (or editing) an Objective or Key Result, select **Add an integration**.

2. From the list of integrations, pick **Asana**.

    :::image type="content" source="../media/goals/viva-goals-asana-integration-2.png" alt-text="Asana Integration 2":::

3. Next, select the **Connection**, if multiple exist, and link a project to the objective. To do so, select the name of the project.

4. To further filter the list of tasks or subtasks, select tasks assigned to a user or pick tasks with a specific status.

    :::image type="content" source="../media/goals/viva-goals-asana-integration-3.png" alt-text="Asana Integration 3":::

    In the following example, we're counting the total number of customer executives who have been onboarded based on different segments. We’re tracking the progress by the number of subtasks completed under the main task.

    :::image type="content" source="../media/goals/viva-goals-asana-integration-4.png" alt-text="Asana Integration 4":::

5. Select **Next** to finish and save your OKR. You should now see an Asana icon next to the OKR - now Viva Goals will automatically count up the finished blog posts. The OKR syncs automatically every hour, but to refresh it manually, select **refresh**.

    :::image type="content" source="../media/goals/viva-goals-asana-integration-5.png" alt-text="Asana Integration 5":::

The following colors of the progress bars indicate the status of the Objective:

- If the progress is 0-25% less than expected progress at any point in time, the status is Behind (orange).

- If the progress is over 25% less than expected progress at any point in time, the status is At-Risk (red).

## % Completed vs KPI

The difference between % Completed and KPI is that with the KPI option you can set a target higher or lower than completing all the tasks in the project.

For example, I have a project with 100 tasks that spans the entire year. I may choose to use KPI and set my target at 25 because my OKR period only lasts a quarter.

I would want to track the completion of tasks but only against the target of 25 and not the entire 100 in the project.  

Learn more about Viva Goals’ other integrations [here](http://help.gotoally.com/integrations).
