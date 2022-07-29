---
title: Align OKRs
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
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Align OKRs"
---

# Align OKRs

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers and only in English. The features described here are subject to change. Viva Goals is only being released to WW tenants. It isn't being released to GCC, GCC High, or DoD environments. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## How to align OKRs across your organization

Alignment is one of the most powerful features of objectives and key results (OKRs). By aligning your objectives at an individual, team, and organization level, strategically aligned OKRs rapidly get everyone on the same page, working toward results that matter.

Viva Goals visually signifies alignment with a line. You can see all the key results nested under an objective on the **Objective** page and on the **OKRs** tab in the organization, team, and individual views.

This line shows how OKRs at the team and individual level contribute to larger objectives upstream and laterally. All OKRs are visible to everyone in the organization, so each individual knows where goalposts are and what needs to be done to achieve success.

### How to align objectives 

1. To align an objective to another objective, select **More** within the objective. From the dropdown, select **Align Objective**.

1. When you search for objectives to align to, you can search for objectives, teams, owners, or time periods from the search bar or choose from the **suggested time periods and entities**. Select the objective you want to align to, and then select **Save**.
1. View and edit the added alignment from the **Quick View** page.

If you need to unalign objectives, you can also do that from the **Full View** page. Find the **Edit Alignment** box on the right, remove the alignment, and save.

### How to edit alignment

1. To edit alignment, select **Edit Alignment**.

2. When you search for objectives to align to, you can search or filter OKRs by entity and time period to narrow your results.

3. Hover over the objective you want to align to, select **Align** and then **Done**.

   > [!NOTE]
   > You can expand an objective to show KRs below and align to those as well.

4. View and edit the added alignment on the **Objective Detail** page.

## How to update progress on your objectives  

The rollup of status and progress through the alignment chain makes it easy to see the impact a key result has on its parent objective and other objectives in the OKR hierarchy.

- **If progress is tracked based on percent completed, Viva Goals will automatically update the status and progress of parent objectives based on the progress of the key results.** The value of progress on the objective will be the average of the progress of its key results.

- **If the objective is tracked by a success metric such as a KPI, Viva Goals won't try to convert percentages into your chosen success metric.** The owner of the objective can manually update the progress with a check-in and enter a value.

- **Once all key results are complete, the objective will automatically be marked as complete.** The average score of the key results will become the score of the objective.

### Three ways to update progress on objectives

Engaging everyone with company goals and driving OKR adoption is the primary responsibility of OKR champions and team managers. Better visibility into how progress is updated will help you understand user engagement with the objectives.

Progress mode indicates how the progress of an OKR is updated. There are three modes of updating progress.

|Mode  |Description  |
|---------|---------|
|Manually     |  Progress of the objective is determined by the objective owner through a manual registration.        |
|Automatic via rollup from children     |     Progress of the objective is rolled up automatically from the key results.     |
|Automatically from a data source     |     Progress of the objective is updated automatically based on data from an integration.     |

> [!NOTE]
> If you have Projects in Viva Goals, you can check in on progress with these projects manually. When you switch to the automatic mode, progress will roll up from tasks under Projects. These tasks can either be added in Viva Goals directly or through an integration.

### How to set the progress mode for an OKR

**When you create or edit the objective:** When you create or edit an objective, you can determine how the progress will be updated. If your objective is measured by percent of completion, you'll have three progress modes to choose from—manually, automatic via rollup from children, or automatically from a data source. If your objective is measured with a KPI, you won't be able to update the progress via rollup because we don't want to override the metric. You'll have to automate the update through an integration, or register manually.

**From the list view:** The icon to the left of the progress bar indicates progress mode. You can select the icon to change the progress mode, or you can make a registration instantly by using the slider progress bar.

**When you make a registration:** If the progress of your objective is updated automatically, you can make a registration and switch to manual progress mode. In this case, the automatic progress will be overridden by the manual registration. You can always switch back to the previous progress mode to resume updating the progress automatically from the children or the connected data source.

**If the progress is rolled up automatically through an integration, follow these steps:**

1. Select the integration icon, and then select the **Check-in** button.
1. Make a registration as you see fit and save it. You'll notice the change in the icon that represents the manual mode.
1. To switch back to the previous mode, select the manual icon, and then select the **Check-in** button.
1. Save this registration, as you'll have the option to resume updating the progress through the connected data source.

### How to set check-in reminders

If you switch an OKR or a project into the manual override progress mode, you'll get check-in reminders for as long as the OKR or project stays in manual mode. Once you revert it to the automated progress mode, whether by rollup or integration, you'll no longer get  reminders to check in.
