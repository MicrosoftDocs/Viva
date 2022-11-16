---
title: Organization insights in the Viva Insights app
description: Find Organization insights in Microsoft Viva Insights 
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.collection: viva-insights-personal
ms.localizationpriority: medium 
ms.service: viva
ms.subservice: viva-insights
manager: anirudhbajaj
audience: user
---

# Organization insights in the Viva Insights app

<!--original content from Jess-->


Organization insights show organization-wide trends by measuring the group of employees who report directly or indirectly to you. <!--detail-->

## Who can access organization insights

To access organization insights, your admin needs to either assign you the **Insights Business Leader** role or configure you as a group manager. <!--how do they do this?-->

## How to use organization insights

If you're assigned the **Insights Business Leader** role, you can view organization insights that measure all employees in the company. If you're a group manager and have the **Insights Business Leader** role assigned, use the selector next to the section title to switch the scope of the insights you're viewing. 

>[!Note]
>The list of direct and indirect reports is based on organizational data that your admin manages.

### Navigation

Here are some things to remember while you explore organization insights within the Viva Insights app.

* Tooltips: If you need a detailed definition of an insight, select the tooltip to the right.

 Select the tooltip next to each insight's title to find a detailed definition.
* Each organization insight card includes a button for a primary recommended action. Clicking this button gives the user a shortcut to launch or share a related Viva Insights workflow or feature.
* If the user clicks the “Explore more” button from the card, they will navigate to a full-page report that provides more information about the measure, including:
    * Trending changes over time
    * Comparisons to peer organizations and across internal group breakdowns (if eligible)
    * Distributions to identify if there is a significant share of employees with outlying experience
    * Explanatory notes to support interpreting the measures
    * Links to related insights and inspiration library articles
* The “Explore more” pages will only include peer comparison for users for whom a sufficiently large peer organization is identified. Peer organizations are identified based on the reporting hierarchy managed by the Insights Administrator, and include employees who report directly or indirectly to the user’s manager (or skip-manager) but not to the user. Some users will not have an identifiable or sufficiently large peer organization based on these definitions – these users will not see peer comparisons.
* The “Explore more” pages will only include internal group breakdowns for users who have one or more managers who report directly to them, and when those reporting managers themselves have sufficiently large organizations of direct and indirect reports. For these users, they will see results for those sub-organizations labeled with the name of the manager who reports directly to the user (“Ava Kim’s organization”). 




## Privacy

<!--Should we move this to our privacy doc?-->

* Organization insights continue to protect individual privacy by enforcing minimum group size, applying differential privacy to averages, and suppressing results for distribution tails:
    * Minimum group size. Because it’s easier to guess information about an individual based on results about a smaller group, users  won’t see results for groups with fewer than 10 people. This minimum can be increased by the Insights Administrator.
    * Differential privacy. For simple averages and totals, there is a small amount of noise introduced into each calculation. The aggregated amount stays accurate, but this makes it impossible to add or subtract different values to figure out results for a single person.
    * Distribution tails. Where an insight counts how many people have a certain profile, like what percentage of your organization gets enough focus time, users won’t see results that would otherwise tell you that “almost all” or “almost none” of the group fit the profile, because that would effectively give the user information about every individual in the group.
