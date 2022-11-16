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

<!--original content from Jess, and some from the old Org trends doc-->

Organization insights show you leading indicators of wellbeing, productivity, and experience by measuring the group of employees who report directly or indirectly to you. You'll find these insights on each tab within the Microsoft Viva Insights app--Home, Teamwork, Productivity, and Wellbeing.<!--detail-->

## Who can access organization insights

To access organization insights, your admin needs to either assign you the **Insights Business Leader** role or configure you as a group manager. <!--how do they do this?-->

## How to use organization insights

If you're assigned the **Insights Business Leader** role, you can view organization insights that measure all employees in the company. If you're a group manager and have the **Insights Business Leader** role assigned, use the selector next to the section title to switch the scope of the insights you're viewing to your direct reports. <!--verify that the scope is for direct reports vs whole org-->

>[!Note]
>The list of direct and indirect reports is based on organizational data that your admin manages.

### Navigation

Here are some things to remember while you explore organization insights within the Viva Insights app.

#### Tooltips and recommended actions

If you need a detailed definition of an insight, select the tooltip to the right.

<!--image-->

Each organization insight card includes a button for a primary recommended action. When you select it, Viva Insights takes you to a related feature that might help address that insight. For example, if your insight indicates that average meeting hours are up, the recommended action card might encourage you to **Set up a no-meeting day**. When you select the button, you'll start the no-meeting day setup right away.

#### Explore more

Each insight card also contains an **Explore more** button, which takes you to a full-page report that provides more information. The report includes:

* Trending changes over time
* Comparisons to peer organizations and across internal group breakdowns (if eligible)
* Distributions to identify whether a significant share of employees have outlying experiences <!--explanation needed-->
* Explanatory notes to help you interpret what the insight measures
* Links to related insights and **Inspiration library** articles

<!--do we need to keep the below?-->

These **Explore more** pages only include internal group breakdowns for people who have one or more managers who report directly to them, and when those reporting managers themselves have big enough organizations of direct and indirect reports. You'll see results for those sub-organizations labeled with the name of the manager who reports directly to you-- for example, “Ava Kim’s organization.” 




## Privacy

<!--How much of this information should we provide for users? Should we move this to our privacy doc?-->

 Organization insights protect individual privacy by enforcing minimum group size, applying differential privacy to averages, and suppressing results for distribution tails. Here's a few more details about each of these topics:

* Minimum group size: Because it’s easier to guess information about an individual based on results about a smaller group, you  won’t see results for groups with fewer than 10 people. Your admin can increase this minimum.
* Differential privacy: For simple averages and totals, Viva Insights introduces a small amount of noise into each calculation. The aggregated amount stays accurate, but you can't add or subtract different values to figure out results for a single person.
* Distribution tails. Where an insight counts how many people have a certain profile, like what percentage of your organization gets enough focus time, you won’t see results that would otherwise tell you that “almost all” or “almost none” of the group fit the profile, because that would effectively give the you information about every individual in the group.
