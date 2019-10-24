---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: The Group Manager (GM) role in Workplace Analytics 
description: Description of the Group Manager (GM) role in Workplace Analytics 
author: paul9955
ms.author: v-pascha
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# The group manager role

The group manager (GM) role has a well-defined purpose in Workplace Analytics: to create improvement plans for employees in their reporting structure. 

The role of a group manager differs from other Workplace Analytics roles in that its scope is predefined and unalterable: The employees in the reporting structure&mdash;all of their reports, direct and indirect&mdash;are automatically assigned to the GM's group. (The GM is also included in this group.)

Improvement plans are part of the **Solutions** feature of Workplace Analytics. Consequently, GMs have access only to the **Solutions** area of Workplace Analytics. Under **Solutions**, GMs can also open the **Solutions** &gt; **Manage** and **Solutions** &gt; **Track** pages, where they can track the progress of their own active plans and the state of their own completed plans. GMs cannot view other groups or track the progress of other plans. 

If you have the GM role assigned as well as the analyst role, the analyst role overrides and you have access to the broader analyst experience, not merely the GM experience. For more information about roles in Workplace Analytics, see [User roles](../use/user-roles.md).

Because a GM can work only with their reports, they cannot define arbitrary groups of employees. For example, the means by which an analyst can define or specify a group&mdash;by uploading a .csv file, by filtering, or by selecting groups in a chart&mdash;are unavailable to GMs.
 
## Plan creation for group managers

* [Create a plan (group manager role)](#create-a-plan-group-manager-role)
* [Track progress (group manager role)](#track-progress-group-manager-role)

### Create a plan (group manager role)

A plan that a GM creates automatically contains the data of the GM's reporting structure. All members of the group, including the GM, are automatically signed up for the plan. 

**Role:** group manager

1. As a GM, when you open Workplace Analytics, you go directly to the **Solutions** page.

   ![Pick a plan](../images/wpa/tutorials/pick-a-plan.png)
     
   This page shows three plans: _Focus plan_, _Collaboration plan_, and _Wellbeing plan_. Consider the type of plan that you want to create. The card for each plan describes the plan and offers **Start now** and **Analyze** options. 

2. (Optional) For a particular plan, select **Analyze**. This displays read-only summary data about your team as a whole. This data pertains to that plan’s area of focus. For example, if you select **Analyze** on the _Focus plan_ card, you will see data that pertains to that plan with regard to your team. After you view this information, select **Start now** and then go to step 4.

    > [!Note]  
    > You cannot view summary data about your team if its size does not exceed the minimum group size. Workplace Analytics admins can set a minimum group size for GM teams that differs from the general Workplace Analytics setting for minimum group size. 

3. For one of the three plans, select **Start now**. This opens the **Set up new plan** panel.

<!--
    ![Group manager -- set up new plan](../../images/wpa/tutorials/gm-set-up-new-plan.png) 
-->

4. Check the figure that is shown on this page for **Number of direct and indirect reports**. If this team size looks incorrect, contact your admin. They should examine the organizational data (HR) file and the manager hierarachy within that file for errors.

5. Select **Validate**. 
  
    After validation finishes, Workplace Analytics shows any resulting details, warnings, and insights about the group. The warnings might indicate that some potential participants are ineligible for various reasons. If, after validation, there are enough participants for the plan, select **Start plan**. This displays the _Your plan was successfully submitted_ page.
 
<!--   
    ![Group manager -- set up new plan](../images/wpa/tutorials/gm-set-up-new-plan-2.png) 
--> 

### Track progress (Group manager role)

Once a plan is underway, you can view the **Manage** page to track the plan’s progress. Note that you can see progress for your team only, and only for a single plan. This is because your team can have only one plan underway at a time. (You cannot subdivide your team into smaller groups that run different plans simultaneously.)

