---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Manager-deployed plans in Workplace Analytics, which use the Group Manager (GM) role 
description: Description of creating manager-deployed plans for whose who have the Group Manager (GM) role in Workplace Analytics 
author: paul9955
ms.author: paul9955
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Manager-deployed plans

A manager can create change-management plans for the people in their reporting structure. To do this, the manager makes use of their group manager (GM) role, which was defined for exactly that purpose: creating and tracking plans for the manager's group. 

The group-manager role has predefined and unalterable scope: The employees in the reporting structure&mdash;all of their reports, direct and indirect&mdash;are automatically assigned to the GM's group. (The GM is also included in this group.)

As a GM, you can access **Plans** in Workplace Analytics to which the GMs have access. In **Plans**, you can create, manage, and track the progress of an active plan and the state of completed plans for your team.  

<!-- NOT YET CONNECTED TO THE BROADER WPA EXPERIENCE SO NOT YET INTEGRATED WITH THE OTHER ROLES
If you have the GM role assigned as well as the analyst role, the analyst role overrides and you have access to the broader analyst experience, not merely the GM experience. For more information about roles in Workplace Analytics, see [User roles](../use/user-roles.md).
-->

The GM can see the behavior trends of their reports. To protect the privacy of individual employees, this behavior data is aggregated, which means that the GM cannot see individual employee behaviors.

## Plan creation for group managers

* [Create a plan (group manager role)](#create-a-plan-group-manager-role)
* [Track progress (group manager role)](#track-progress-group-manager-role)

### Create a plan (group manager role)

A plan that a GM creates automatically contains the employees of the GM's reporting structure. All members of the group, including the GM, are automatically signed up for the plan. 

1. As a GM, when you open Workplace Analytics, you go directly to the **Plans** page.

   ![Pick a plan](../images/wpa/tutorials/pick-a-plan.png)
     
   This page shows three plans: _Focus plan_, _Collaboration plan_, and _Wellbeing plan_. Consider the type of plan that you want to create. The card for each plan describes the plan and offers **Start now** and **Analyze** options. 

2. (Optional) For a particular plan, select **Analyze**. This displays read-only summary data about your team as a whole. This data pertains to that plan's area of focus. For example, if you select **Analyze** on the _Collaboration plan_ card, you will see data that pertains to that plan with regard to your team:

   ![Info for Collaboration plan](../images/wpa/tutorials/gm-analysis.png)
   
   After you view this information, select **Start now** and then go to step 4.

3. For one of the three plans, select **Start now**. This opens the **Set up new plan** panel.

<!-- LOCATE THIS IMAGE!
    ![Group manager -- set up new plan](../../images/wpa/tutorials/gm-set-up-new-plan.png) 
-->

4. Check the figure that is shown on this page for **Number of direct and indirect reports**. This number is based on the organizational file that was uploaded by the Workplace Analytics admin and is reflects the number of assigned Workplace Analytics licenses. If this team size looks incorrect, contact your admin. They should examine the organizational data (HR) file and the manager hierarachy within that file for errors.

5. Select **Validate**. 
  
    After validation finishes, Workplace Analytics shows any resulting details, warnings, and insights about the group. The warnings might indicate that some potential participants are ineligible for various reasons. If, after validation, there are enough participants for the plan, select **Start plan**. This displays the _Your plan was successfully submitted_ page.
 
<!-- LOCATE THIS IMAGE! 
    ![Group manager -- set up new plan](../images/wpa/tutorials/gm-set-up-new-plan-2.png) 
--> 

### Track progress (group manager role)

Once a plan is underway, you can view the **Manage** page to track the plan's progress.

![Track progress](../images/wpa/tutorials/solutions-track.png) 

Note that you can see progress for your team only, and only for a single plan. This is because your team can have only one plan underway at a time. (You cannot subdivide your team into smaller groups that run different plans simultaneously.)

