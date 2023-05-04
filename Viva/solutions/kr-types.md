---
ms.date: 03/29/2023
title: Define KR Types in Viva Goals
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager: Liz.Pierce
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:
  - m365initiative-viva-goals
  - Tier1
search.appverid:
- MET150
description: "Learn how to set KR types while creating your Key Results"
---

# Define KR Types in Viva Goals

Key Result types enable users to establish goals with defined outcomes. These KR types can be quantity-type key results that measure progress from one point to another, quality-type key results that act as guardrails and help monitor consistency and efficiency, or a KR type that establishes a baseline. 

## What are the different KR types you can create in Viva Goals? 
Viva Goals allows you to create six distinct types of Key Results, which we classify into three categories:

1. [Regular KR types](#regular-kr-types-quantity) (Quantity KRs)
1. [Control KR types](#control-kr-types-quality) (Quality/Guardrail KRs)
1. [Baseline KR types](#baseline-kr-types) 

### Regular KR types (Quantity): 

Regular KR types are used when trying to achieve a specific metric.

1. **Reach:** The 'Reach' metric type is useful when you're starting at zero and have a specific target that you want to achieve. For example, "Conduct 5 internal surveys" or "Gain 500 users for new community site".

1. **Increase from:** When the OKR is required to track a metric, which is already at a certain number and must increase to a higher number, you can choose the 'Increase from' metric. For example, “Increase revenue from $20mn to $40mn this year”. Here, the ‘from’ indicates the starting value of $20Mn and the ‘to’ indicates the target value of $40Mn.  

1. **Decrease from:** Similarly, when the OKR is required to track a metric, which is already at a certain number and must decrease further to a lower number, you can select the ‘Decrease from’ metric type. For example, “Reduce P0 bugs from 50 to 10 this quarter”. Here, the start value is the higher value of 50 and the target value is the lower value 10.  

### Control KR types (Quality) 

Control KR types are used when you must keep key results above or below a certain threshold value. This is done to maintain the quality of a metric and set guardrails for accepted results.

Viva Goals has two control metrics:  

1. **Stay below:** The 'Stay Below' KR type is useful when a metric must remain below a certain threshold. For example, “Keep customer churn below $100k”. The only input is the target value, which acts as a threshold for success.

1. **Stay above:** The 'Stay Above' KR type is useful when a metric must remain above a certain threshold. For example, “Keep customer NPS score above 9”. The only input is the target value, which acts as a threshold for success.

**Adding risk threshold to control metrics:**

**Optional:** Users can add a “Risk threshold” value to the control metrics they're creating. If a control metric has a threshold added, then it manifests in the following ways: 

1. Behind Status: Any check-ins that fall between the risk threshold value and the final target value will be marked as “Behind.” 
1. Accepted risk threshold value: For stay above key results, the risk threshold must always be lesser than the final target value of the key result. For stay below key results, the risk threshold must always be greater than the final target value of the key result.

### Baseline KR types 
  
**Find a baseline:** The 'Find a baseline' KR type is useful when an organization is trying to measure a goal, which is important enough to be tracked alongside other key results, but the target value isn't yet known.

For example, "Measure baseline customer retention rate", can be tracked during a time period, even though the starting or target metric isn't yet known because the metric hasn't been tracked by the organization previously, or can't be set with any degree of confidence. In such cases a baseline key result can be created where there's no need to set a target value.

## How can you set KR types for a Key Result?

1. Add a key result by selecting '...' and then choosing the **Add a Key Result** option from the dropdown. You can also edit an existing key result to set a KR type for it.

    :::image type="content" source="../media/goals/add-key-result.png" alt-text="Screenshot that shows how to add a key result." lightbox="../media/goals/add-key-result.png":::

3. In the 'Create Key Results' quick view page that appears, enter the title of the key result.
4. Select **Add metric** that appears below the title.

    :::image type="content" source="../media/goals/add-metric-button.png" alt-text="Screenshot that shows where to find the add metric button." lightbox="../media/goals/add-metric-button.png":::
    
6. Enter the target name and choose the appropriate KR type using the **Target should** dropdown.

    :::image type="content" source="../media/goals/target-should-dropdown.png" alt-text="Screenshot that shows the various KR types under the target should dropdown." lightbox="../media/goals/target-should-dropdown.png":::
    
8. Depending on the KR type, enter the target values and select **Create**.

    :::image type="content" source="../media/goals/create-kr-button.png" alt-text="Screenshot that shows the create button to save your changes and create your Key Result." lightbox="../media/goals/create-kr-button.png":::

## Progress and Status Calculation: 
Progress and status calculations in Viva Goals vary depending on the key result categories—regular KR types and control KR types.  

### Progress status calculation for regular KR types  
Progress and status for the regular KR types are determined by two types of progress:

**Expected progress:** Viva Goals calculates expected progress based on the start and end date of an OKR. At the beginning of the time period, the expected progress is 0% and at the end of the time period the expected progress will be 100% 

**Actual Progress:** Actual progress is calculated based on the check-ins made on the OKR. There are three ways check-ins can be made:
1. Manually
1. From a data source (Integration) 
1. Roll up from Key results

### Status calculation for regular KR types: 

There are two ways in which status can be determined.

1. **Derive Status based on Actual Progress:** Status of the OKR is set based on the actual progress made via automatic progress updates.
2. **Manually Update Status:** Users can manually update the status of the OKRs by making check-ins. This overrides the status set automatically by Viva Goals based on progress updated via roll-up from key results or via a data source.

You can learn in detail how the progress and status are calculated for regular KR types in [this article](/viva/goals/track-okr-progress-status).

## Progress status calculation for control KR types 
Progress and status for the control KR types ‘Stay below’ and ‘Stay above’ are calculated as follows: 

**Stay below:** 

If the current metric value is less than the threshold or target value, then the progress of the OKR is set to 100%, and the status is set to “On Track”. 

Let's take the example key result "Keep churn below 100k" as shown in the image below. The progress graph, on the right, can be seen with a point in the graph that represents a check-in. Each check-in made will be represented as a point in the graph.

:::image type="content" source="../media/goals/on-track-stay-below-kr.png" alt-text="Screenshot that shows the progress graph for a stay below KR that's on track." lightbox="../media/goals/on-track-stay-below-kr.png":::

The red dotted line indicates the border value below which the progress points must be in order to be "On Track". 

Similarly, if the value is greater than or equal to the threshold or target value, then the progress of the OKR is 0% and the status is set to “At Risk”.

Let's take the example key result "Maintain page response time below 2 seconds". As shown in the image, the current progress or check-in made is depicted as a point in the graph.

:::image type="content" source="../media/goals/at-risk-stay-below-kr.png" alt-text="SScreenshot that shows the progress graph for a stay below KR that's at risk." lightbox="../media/goals/at-risk-stay-below-kr.png":::

Since it's greater than the border value of 2, it lies above the red dotted line and in the shaded area that represents "At Risk". This indicates that the status of the key result is "At Risk".

> [!NOTE]
> Any check-in or progress point that lies on the red line or in the shaded grey area is "At Risk" while those that lie in the white area are **On Track.**

**Stay above:**

If the value is greater than the threshold value, then the progress is set to 100% and the status is “On Track”. 

Let's consider the key result "Ensure NPS stays above 9", where 9 is the border value represented by the red dotted line as shown in the image below. Each point in the graph represents a check-in. Since the point lies in the white area above the dotted line, the progress status is "On Track" as the white area represents "On Track".

:::image type="content" source="../media/goals/on-track-stay-above-kr.png" alt-text="Screenshot that shows the progress graph for a stay above KR that's on track." lightbox="../media/goals/on-track-stay-above-kr.png":::

If the value is equal to or less than the threshold value, then progress of OKR is 0% and status is set to “At Risk”. 

Let's take the example of the following key result: "Maintain average FCSAT score above 8". Here, 8 is the border value represented by the red line. Since the current progress value is 7.8, which is less than the border value, the progress point is shown to be present in the shaded grey area. This area represents "At Risk" and so, the status of the key result is "At Risk".

:::image type="content" source="../media/goals/at-risk-stay-above-kr.png" alt-text="Screenshot that shows the progress graph for a stay above KR that's at risk." lightbox="../media/goals/at-risk-stay-above-kr.png":::

For control KR types, there's no notion of “Behind” since we consider these KR types as met or unmet. 

## How does roll up happen for control KR types? 
Based on the progress of the control metric-type key result (either of 0% or 100%), the value is rolled up from the child KR to the parent objective. 

If you want to turn off roll-up, this can be done by making the contribution of each key result to 0%. Here's how:

1. Right-click on the parent objective and select **Manage contributions**. 

    :::image type="content" source="../media/goals/manage-contributions-button.png" alt-text="Screenshot that shows where to find manage contributions." lightbox="../media/goals/manage-contributions-button.png":::
    
2. Changing the corresponding KRs to 0% and select **Save**.  

    :::image type="content" source="../media/goals/manage-contributions.png" alt-text="Screenshot that shows roll-up being disabled for a few Key Results." lightbox="../media/goals/manage-contributions.png":::
    
## Status calculation for baseline key results  

Baseline key results don't have a notion of progress associated with it, but have statuses, which are different from the other types of key results. 

The statuses for baseline key results are: **Not started, In-progress, Closed, Postponed.** Whenever there's a check-in value associated with a baseline type of key result, the status is automatically updated to ‘in-progress’. The user must manually update the status of the Key result to any other state such as closed or postponed. 

**Roll up:** If the parent key result created and the children key result created under the parent are all of type baseline, then the sum of values from the children is rolled up to the parent.

## FAQ (Frequently Asked Questions)

1. **After adding risk threshold to an existing control metric the status will automatically change to Behind?**
    1. No, only the next time when you make a check-in or edit the values, will the status get updated to **Behind** until then it will continue to stay **At-risk** or **On-track** only whatever the status was before the risk threshold was added.  
