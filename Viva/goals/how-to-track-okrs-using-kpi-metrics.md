---
title: How to track OKRs using KPI metrics?
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
description: "Learn how to track OKRs using KPI metrics"
---

# How to track OKRs using KPI metrics?

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

You can use a KPI metric when you want to set custom "start" and "target" values for your OKR, as opposed to just going from 0-100% progress. Doing so gives you a much more accurate idea of progress while executing your OKRs.

KPI metrics in Viva Goals support two types of units - Numeric and % based.

KPI metrics will be available for both objectives and key results if you configure your OKRs by selecting the **Objectives and key results can be used interchangeably** option. In case you selected the **Objectives are always aspirational, key results are always measurable** option, you'll be able to add KPI Metrics to only key results, as key results are only measurable. For more information on configuration of OKRs by rules, see [OKR Model Configuration Rules](https://help.ally.io/en/articles/5214200-configure-your-okr-rules-in-ally-io).

## Objectives and key results measured on the basis of a numeric unit

Use numeric units unless your target is a percentage value. To create an objective that’s tracked by a numeric KPI, see the following video and perform the following steps:

1. Select the **Add Objective** option and fill in your objective title and other details like type, owner, time period.

   :::image type="content" source="../media/goals/filling-details-of-an-objective.png" alt-text="Filling details of an objective":::

2. In the **Outcome** pane, select the **Add a metric** option to give details about the metric you’d like to measure and the target you’d like to achieve.

   :::image type="content" source="../media/goals/add-a-metric.png" alt-text="Adding a metric":::

3. Select **Show more options** if the starting value needs to be changed.

   > [!NOTE]
   > By default, Viva Goals will set the starting value as **0 (zero)** and the unit as **Number**.

   :::image type="content" source="../media/goals/show-more-options.png" alt-text="Show more options":::

   You can specify the starting value and also choose a unit based on how you’d like to measure progress. 

4. Once you’ve added details about how you’d like to measure progress, select **Create**.

   :::image type="content" source="../media/goals/measurement-method-defining-process.png" alt-text="Creating a method by which you can measure progress":::

## Objectives and key results measured on the basis of % unit

An objective’s completion doesn’t mean it has to hit a 100%. You can choose to set your objective’s completion % as 60. You can use KPI metrics with the % unit to do this customization.

To create an objective that’s tracked by a % KPI, see the following video and perform the following steps:

1. Select the **Add Objective** option and fill in your objective title and other details like type, owner, time period.

   :::image type="content" source="../media/goals/add-objective-option.png" alt-text="The Add objective option":::

2. Once done, select the **Add a metric** option under the **Outcome** pane and give details about the metric you’d like to measure and the target you’d like to achieve.

   :::image type="content" source="../media/goals/add-a-metric-option.png" alt-text="The Add a metric option":::

3. To change the metric %, select **Show more options**. 

   > [!NOTE]
   > By default, Viva Goals will set the starting value as **0 (zero)** and the unit as **Number**.

   :::image type="content" source="../media/goals/show-more-options-ui-item.png" alt-text="The Show more options UI items":::
 
   You can choose the % unit from the **Unit** dropdown list and edit the different starting value, as necessary. 

4. Once you’ve added details about how you’d like to measure progress, select **Create**.

   :::image type="content" source="../media/goals/adding-details-to-measure-progress.png" alt-text="Adding details to measure progress":::

Since start and target might not be 0 and 100%, respectively, a % KPI metric's overall progress is scaled relative to its "start" and "target" metrics. For example, if the metric goes from 30% to 50% and its current value is 40%, it has achieved 50% progress given its "starting point" and "target".

This progress is calculated as follows:

Let "S "be the "Starting" metric and "T" be the "Target" you’d like to achieve. "P" is the value of the progress you’ve made so far.

- S = 30 (Starting value)
- T = 50 (Target)
- P = 40 (Progress made)

Here’s how the key result’s progress is used to calculate scaled progress:

[P−S/T−S]∗100

So for this key result, the scaled progress would be [10/20]∗100 =50%.