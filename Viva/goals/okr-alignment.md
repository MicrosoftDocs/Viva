---
title: OKR alignment
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
- Strat_SP_modern
- M365-collaboration
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Learn about the alignement tool"
---

# OKR alignment

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Alignment is one of the most powerful features of OKRs (Objectives and Key Results)! By aligning your objectives at an individual, team and organization level, strategically aligned OKRs rapidly get everyone on the same page, working towards results that matter.

Viva Goals visually signifies alignment with - you guessed it - a line. You can see all the key results nested under an objective on the Objective page, and under the **OKRs** tab in the organization, team and individual views.

:::image type="content" source="../media/goals/alignment-line.png" alt-text="The line indicating an alignment":::

What this line shows us is how OKRs at the team and individual level contribute to larger Objectives further upstream and laterally. All OKRs are visible to everyone in the organization: so each individual knows where the goal posts are and what needs to be done to get there.

## Aligning objectives

If you've been adding Key Results to your Objectives, as we showed you in a previous article, you'll notice they are already aligned to the Objective.

### Steps to align an objective

1. To align an objective, click on **More** within the Objective. From the drop-down, select **Align Objective**.

   :::image type="content" source="../media/goals/option-to-edit-an-alignment.png" alt-text="The option to edit an alignment":::

   :::image type="content" source="../media/goals/align-objective-dialog-box.png" alt-text="The Align Objective dialog box":::

1. When searching for objectives to align to, you can **search** for objectives, teams, owners, or time periods in the search bar or choose from the **suggested time periods and entities**. Select the objective you want to align to and click **Save**.
1. View and edit the added alignment from the Quick View page.

   :::image type="content" source="../media/goals/view-and-edit-the-added-alignment.png" alt-text="The Quick view page on which you can view and edit the added alignment":::

If you need to un-align them at any time, you can also do so from the **Full View** page. Find the **Edit Alignment** box on the right-hand side, remove the alignment and save it.


## Cascading

Organically, organization level KRs become team level Objectives, and team level KRs can become individual Objectives; which maintains vertical alignment in the organization. In OKR methodology, we call this effect ‘Cascading’.

## OKR Duality - an analogy

Have you noticed how an Objective can be a Key Result or an Objective depending on the view? This phenomenon is called OKR Duality and it works like an inheritance model. 

To use a metaphor, if you create a top level Objective with nothing above it, it’s always an objective and never a Key Result. We’ll call this one Grandma. If you then add a Key Result to Grandma, then Grandma becomes a parent and the Key Result becomes her child. Let’s call this first Key Result “Mom”, because she too will have children.

If you add another Key Result to the Mom Key Result, then the Mom Key Result becomes a parent too. Now Mom is a parent as well as a child - in other words - Mom is both an Objective and a Key Result. She’s a Key Result to Grandma and an Objective to her child. Mom is both things and will have a different identity depending on your viewpoint. From the child’s perspective: she’s an objective. From Grandma’s perspective, she’s a Key Result. 

What does this mean for your OKRs? Well, now that the Objectives are aligned, changes will roll up through the chain of alignment (or inheritance) to affect progress accordingly. This is incredibly handy for alerting the team to potential pinch points and risk areas downstream because they will be reflected in top level Objectives. The next section will walk you through how exactly this happens.

## Progress Roll-Up

The roll-up of status and progress through the alignment chain makes it easy to see the impact a Key Result has on its parent Objective and other Objectives in the OKR hierarchy. If progress is tracked based on % completed, Viva Goals will automatically update the status and progress of parent Objectives based on the progress of the key results. 

The actual value of the progress of the objective will be the average of the progress of its key results. The status will also be based on the statuses of each key result.

:::image type="content" source="../media/goals/progress-of-an-objective.png" alt-text="The illustration of the progress of an objective":::

However, if the objective is tracked by success metric, Viva Goals won't attempt to convert percentages into your chosen success metric. The owner of the Objective can manually update the progress with a check in and enter a value.

Once all key results are completed, the objective will be automatically be marked as completed and the average score of the key results will become the score of the objective.

Now that you know how to align Objectives for success, keep your allies close, and your alignments even closer…

### FAQs

**Q: Why do my OKR icons vary in the alignment search window?**

  A: Let’s take a look at how the objectives and key results appear in the alignment search window while trying to align your OKRs when your OKR Configuration is set as **Objectives and key results can be used interchangeably**.

   1. **When progress is being tracked via percentage**: These key results appear as Objectives in the alignment window since when you align another key result to it - the key result appearing in the alignment window search will act as an objective for the key result. This is because of the OKR configuration behaviour when the objectives and key results can be used interchangeably. Here, the key result for one objective can also act as an objective for another key result.
 
   2. **When progress is being tracked via metrics**: The key results appear with the key result icon as it is in the alignment window when their progress is being tracked by metrics.
   
   Once your OKRs are aligned, the icons will appear as intended. To learn more about the use of OKR icons, take a look at [Viewing icons](https://help.ally.io/en/articles/5228614-viewing-icons-for-objectives-key-results-projects-in-ally-io).


**Q: Can I add or edit OKR alignment?**

  A: You can add or edit OKR alignment on any OKR that hasn't been scored.
   
#### Steps to add or edit alignment

1. To edit or add alignment first create or edit the objective. Click on **Edit Alignment**.
  
   :::image type="content" source="../media/goals/editing-an-alignment.png" alt-text="Editing an alignment":::

2. When searching for objectives to align to, you can search or filter OKRs by entity and time period to narrow your results. For example, if I wanted to search for company OKRs, I would select **Digital Tones entity**.

   :::image type="content" source="../media/goals/digital-tones-option.png" alt-text="The Digital Tones option":::

3. Hover over the objective you want to align to and click **Align** then **Done**. 

   > [!NOTE]
   > You can expand an objective to show KRs below and align to those as well.

4. View and edit the added alignment on the Objective Detail page.
 
   :::image type="content" source="../media/goals/viewing-the-aligment-details.png" alt-text="Viewing the alignment details on the Objective Detail page":::