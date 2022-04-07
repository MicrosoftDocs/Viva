---
title: Roll up the progress of objectives tracked by KPI
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
description: "Learn how progress roll-up is calculated for objectives measured by KPIs"
---

# Roll-up of progress for objectives tracked by KPI

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

You can use a KPI (Key Performance Indicator) metric when you want to set custom "start" and "target" values to your objective. Objectives tracked using KPI metrics are associated with "Units". Units represent the method of measuring an objective’s progress. Viva Goals supports two types of units - **Numeric** and **% based**. The roll-up of progress for each of these units is calculated differently.

The calculation methods are described in the following table:

|Method  |Description  |
|---------|---------|
|Numeric Units     |     For objectives tracked based on a numeric unit, the progress of the objective will be the **sum of numeric key results**.     |
|% Units |    For objectives tracked based on the % unit, the progress of the objective will be calculated as the **weighted average of all key results**, whether they're metric based, or are just going to reach 100% completion. You can also set individual key results that don't contribute to the parent.     |

## Objectives measured based on the numeric unit

Progress for objectives that're tracked based on numeric units is calculated as the **sum of all the key results**. For objectives tracked by numeric KPIs, your objective and key results (OKRs) should essentially carry the same units for the progress roll-up to work. For instance, when an objective is measured based on a KPI metric with a numeric unit, the key results will contribute to the progress only when they’re also calculated by numeric metrics.

To create an objective that’s tracked by a numeric KPI, perform the following steps:

1. Select the **Add Objective** option and fill in your objective title and other details like type, owner, and time period.

   :::image type="content" source="../media/goals/create-an-objective.png" alt-text="Creating an objective":::

2. In the **Outcome** pane, select the **Add a metric** option to give details about the metric you’d like to measure, the starting value, and the target you’d like to achieve. You can also select a unit based on how you’d like to measure progress.

   :::image type="content" source="../media/goals/add-metric.png" alt-text="Add a metric":::

   :::image type="content" source="../media/goals/add-a-metric-2.png" alt-text="Add a metric-2":::

3. Once you’ve added details about the metric, select **Automatic via rollup from key results** as the progress mode under the **Progress**' pane, and select **Save**.

> [!NOTE]
> The **Progress** pane has three different types of progress modes: 
> - Manually
> - Automatic via rollup from key results
> - Automatically from a data source.
> 
> For more information about all the progress modes, see [Progress Modes](https://help.ally.io/en/articles/4754259-progress-modes).

   :::image type="content" source="../media/goals/select-a-progress-mode.png" alt-text="Select a progress mode":::

Say, for example, your Sales team has an objective to **increase ARR from $1M to $2M**. Now the objective is tracked by a KPI metric that's numeric. This objective has key results that're also measured by a numeric KPI.

**Objective**: Increase ARR from $1M to $2M
**KR 1**: Increase NAMER ARR from $400K to $800K
**KR 2**: Increase MENA ARR from $100K to $700K

:::image type="content" source="../media/goals/example of an objective.png" alt-text="Objective to increase ARR":::

## Objectives measured based on the % unit

Progress of the objectives that're tracked based on the % unit will be calculated as the **weighted average**. You can also set the % completion arbitrarily as per your requirement. This'll work for both manual progress updates and automated updates from integrations. Objectives that're tracked by % complete KPIs can have key results that're tracked either by % metric or by the numeric metric.

Simply put, an objective’s completion doesn’t mean it has to hit a 100%. You can choose to set your objective’s completion % as 60 and update progress manually or connect your objective with an integration that’ll allow you to measure the progress based on % completion.

Say, for example, your Marketing team has an objective to **achieve record-breaking engagement to increase paying customers**’ from 30% to 60%. This objective has the following key results that contribute to the parent’s progress.

**Item**: Objective
**Title**: Achieve record-breaking engagement to increase paying customers
**Metric**: Paying customers
**Target**: 60
**Starting**: 30
**Unit**: %

**Item**: Key result 1
**Title**: Increase monthly trial signups from 25% to 40%
**Metric**: Trial signups
**Target**: 40
**Starting**: 25
**Unit**: %

**Item**: Key result 2
**Title**: Boost NPS score from 7 to 8
**Metric**: NPS
**Target**: 8
**Starting**: 7
**Unit**: Numeric

**Item**: Key result 3
**Title**: Increase monthly conversion of new paid customers from 15% to 35%
**Metric**: MoM Conversion
**Target**: 35
**Starting**: 15
**Unit**: %

:::image type="content" source="../media/goals/objectives-and-achievement.png" alt-text="Objectives metrics":::

For instance, there’s a progress of 5% made in key result 3 (Increase monthly conversion of new paid customers from 15% to 35%). Whenever there’s a progress checked-in, the actual progress made will be displayed under the progress bar and the scaled progress is shown right next to the progress bar.

Let **S** be the "starting" metric and **T** be the "target" you’d like to achieve. **P** is the value of the progress you’ve made so far.

In this example, there’s a registration made at 20%.

S = 15 (Starting value) 
T = 35  (Target) 
P = 20  (Progress made) 

Here’s how the key result’s progress is used to calculate scaled progress: 

[P−S/T−S]∗100

So for this key result, the scaled progress would be [5/20]∗100 =25% 

## Objectives measured based on the % unit can have key results that're tracked by % metric or the numeric metric

Objectives that're tracked by % complete KPIs can have key results that're tracked by % metric or by the numeric metric. The key results' progress will roll up to the parent’s progress, irrespective of its metric. This roll-up is because the numeric metric can be converted and expressed as a percentage.

In this example, consider the key result 2 (Boost NPS score from 7 to 8), where the progress is measured as a numeric metric. Say there’s a registration made and the value increases from 7 to 7.2, then the progress made will be considered as 20% and will contribute to the parent’s progress.

In case you don’t want a key result measured by a numeric value to contribute to an objective that’s measured by % complete KPI, you can open the **Edit weight and progress roll up** menu and select the **Doesn't contribute towards the progress of the parent** option.

The objective’s progress is the weighted average of the key results that contribute to the parent.

Let KR1 be the scaled progress of key result 1, KR2 be the scaled progress of key result 2 and so on, and ‘n’ be the total number of key results.

Scaled progress of Objective = ([KR1 + KR2 + KR3+ KRn] / n)*100

In this example, the following inputs are available:

- Scaled progress of KR1 = 0%
- Scaled progress of KR 2 = 25%
- Scaled progress of KR 3 = 20%

Based on these inputs, the scaled progress of the objective is: 

[(0+25+20/3)*100]  = 15% 

The actual progress of the objective is calculated by the product of the scaled progress and the difference between the target and the starting metric value added to the started metric.

Actual progress of the objective = [Scaled progress of the objective * Difference between the target and starting metric] + Starting metric.

Actual progress of the objective = [(15/100)*(60-30)] = 4.5+30 = 34.5%

:::image type="content" source="../media/goals/actual-progress-of-objective.png" alt-text="Actual progress of the objective":::