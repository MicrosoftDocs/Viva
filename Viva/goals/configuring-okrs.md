---
title: Configure OKRs
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
description: "Learn how you can confirgure OKRs"
---

# Configuring OKRs in Viva Goals

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## OKR alignment

Alignment is one of the most powerful features of OKRs (Objectives and Key Results)! By aligning your objectives at an individual, team and organization level, strategically aligned OKRs rapidly get everyone on the same page, working towards results that matter.

Viva Goals visually signifies alignment with - you guessed it - a line. You can see all the key results nested under an objective on the Objective page, and under the **OKRs** tab in the organization, team and individual views.

:::image type="content" source="../media/goals/alignment-line.png" alt-text="The line indicating an alignment":::

What this line shows us is how OKRs at the team and individual level contribute to larger Objectives further upstream and laterally. All OKRs are visible to everyone in the organization: so each individual knows where the goal posts are and what needs to be done to get there.

### Aligning objectives

If you've been adding Key Results to your Objectives, as we showed you in a previous article, you'll notice they're already aligned to the Objective.

### Steps to align an objective

1. To align an objective, click on **More** within the Objective. From the drop-down, select **Align Objective**.

   :::image type="content" source="../media/goals/option-to-edit-an-alignment.png" alt-text="The option to edit an alignment":::

   :::image type="content" source="../media/goals/align-objective-dialog-box.png" alt-text="The Align Objective dialog box":::

1. When searching for objectives to align to, you can **search** for objectives, teams, owners, or time periods in the search bar or choose from the **suggested time periods and entities**. Select the objective you want to align to and click **Save**.
1. View and edit the added alignment from the Quick View page.

   :::image type="content" source="../media/goals/view-and-edit-the-added-alignment.png" alt-text="The Quick view page on which you can view and edit the added alignment":::

If you need to un-align them at any time, you can also do so from the **Full View** page. Find the **Edit Alignment** box on the right-hand side, remove the alignment and save it.

### Steps to add or edit alignment

1. To edit or add alignment first create or edit the objective. Click on **Edit Alignment**.
  
   :::image type="content" source="../media/goals/editing-an-alignment.png" alt-text="Editing an alignment":::

2. When searching for objectives to align to, you can search or filter OKRs by entity and time period to narrow your results. For example, if I wanted to search for company OKRs, I would select **Digital Tones entity**.

   :::image type="content" source="../media/goals/digital-tones-option.png" alt-text="The Digital Tones option":::

3. Hover over the objective you want to align to and click **Align** then **Done**. 

   > [!NOTE]
   > You can expand an objective to show KRs below and align to those as well.

4. View and edit the added alignment on the Objective Detail page.
 
   :::image type="content" source="../media/goals/viewing-the-aligment-details.png" alt-text="Viewing the alignment details on the Objective Detail page":::

### Progress Roll-Up

The roll-up of status and progress through the alignment chain makes it easy to see the impact a Key Result has on its parent Objective and other Objectives in the OKR hierarchy. If progress is tracked based on % completed, Viva Goals will automatically update the status and progress of parent Objectives based on the progress of the key results. 

The actual value of the progress of the objective will be the average of the progress of its key results. The status will also be based on the statuses of each key result.

:::image type="content" source="../media/goals/progress-of-an-objective.png" alt-text="The illustration of the progress of an objective":::

However, if the objective is tracked by success metric, Viva Goals won't attempt to convert percentages into your chosen success metric. The owner of the objective can manually update the progress with a check in and enter a value.

Once all key results are completed, the objective will automatically be marked as completed and the average score of the key results will become the score of the objective.

Now that you know how to align objectives for success, keep your allies close, and your alignments even closer.

## Manage OKR contribution

Viva Goals’ OKR contribution feature provides users (objective owners and creators) more flexibility and customizability in specifying weights and measuring progress. Users will now be able to define and control contribution at the parent level. All the contributions add up to a total of 100% and objective owners/creators have an option to mark a child’s contribution as "fixed". This feature is available only for OKRs that've progress mode as **Updated via roll-up from key results**.

### Who can manage contribution?

Users who have "edit" permissions for the OKR (including check-in owners) can edit the contributions of children.

### How to manage OKR contribution

You can set or edit your OKRs’ contribution from the **More actions** dropdown list. To do this task, perform the following steps:

1. Select the **Manage children’s contribution** option.

   :::image type="content" source="../media/goals/manage-contributions-of-children.gif" alt-text="Managing the contribution of children":::

   > [!NOTE]
   > You can also open the **Manage children's contribution** modal from the objective quick view by selecting the objective's title and also from the objective's detail view, as depicted in the following two images, respectively.
   > 
   > :::image type="content" source="../media/goals/manage-contribution.png" alt-text="Manage contribution - 1":::
   > 
   > :::image type="content" source="../media/goals/manage-contribution-2.gif" alt-text="Manage contribution - 2":::

   The **Manage contributions** dialog box is displayed.

2. Add or edit the contributions of the children (objectives, key results, or projects)

   :::image type="content" source="../media/goals/add-or-edit-contributions-of-children.png" alt-text="Adding or editing the contributions of the children":::

   > [!NOTE]
   > You can also enable or disable the **New children should start contributing by default** toggle. By enabling this toggle (which is enabled by default), you'll allow a newly created child to contribute to the parent. This enablement will readjust the contributions you’d have assigned to each child.

3. Select **Save** to save all the changes.

### Key points to note for OKR contribution

1. OKR contribution is available only for OKRs that have progress mode as **Updated via roll-up from key results**.
1. All the contributions will add up to a total of 100%. The default contribution is automatically assigned by Viva Goals to all the children equally. For example, if an objective has three key results (children), the default contribution assigned to each child will be 33.33%.
1. As soon as a child’s contribution is edited, the contribution is considered as “fixed”. This rule means, if a new child gets added or if an existing child gets removed, the contributions marked as "fixed" won't be adjusted. For example, if an objective has three key results (children), and the contribution of the first key result is edited as 50%, the contributions of second and third key results will be automatically adjusted to 25% each. In future, if there's a fourth key result that gets added, only the contribution of the second and third key results will be adjusted.
1. You can also reset all the custom contributions to default by selecting the **Reset to default** option.

## How to track OKRs using KPI metrics?

You can use a KPI metric when you want to set custom "start" and "target" values for your OKR, as opposed to just going from 0-100% progress. Doing so gives you a much more accurate idea of progress while executing your OKRs.

KPI metrics in Viva Goals support four types of units - Numeric (No unit), % (Percentage), $ (Dollar), and € (Euro).

1. Select the **Add Objective** option and fill in your objective title and other details like type, owner, time period.

   :::image type="content" source="../media/goals/filling-details-of-an-objective.png" alt-text="Filling details of an objective":::

2. Expand the **Outcome** pane and enter the name of the metric you’d like to achieve under **Metric name**.

   :::image type="content" source="../media/goals/add-a-metric.png" alt-text="Adding a metric":::

3. Under **Target** click the **Increase to** drop down if you want to switch to **Decrease to** as the type of metric you'd like to track.

4. Click on the drop down next to **%** to change the unit. You can use the following units:

a. No unit
b. % Percentage
c. $ Dollar
d. € Euro
   
5. If the starting value needs to be changed, click on the **Edit** button next to **Starting from: 0%**.

[screenshot]

6. Once you’ve added details about how you’d like to measure progress, select **Create**.

   :::image type="content" source="../media/goals/measurement-method-defining-process.png" alt-text="Creating a method by which you can measure progress":::


Since start and target might not be 0 and 100%, respectively, a % KPI metric's overall progress is scaled relative to its "start" and "target" metrics. For example, if the metric goes from 30% to 50% and its current value is 40%, it has achieved 50% progress given its "starting point" and "target".

This progress is calculated as follows:

Let "S "be the "Starting" metric and "T" be the "Target" you’d like to achieve. "P" is the value of the progress you’ve made so far.

- S = 30 (Starting value)
- T = 50 (Target)
- P = 40 (Progress made)

Here’s how the key result’s progress is used to calculate scaled progress:

[P−S/T−S]∗100

So for this key result, the scaled progress would be [10/20]∗100 =50%.

## Roll-up of progress for objectives tracked by KPI

You can use a KPI (Key Performance Indicator) metric when you want to set custom "start" and "target" values to your objective. Objectives tracked using KPI metrics are associated with "Units". Units represent the method of measuring an objective’s progress. Viva Goals supports two types of units - **Numeric** and **% based**. The roll-up of progress for each of these units is calculated differently.

The calculation methods are described in the following table:

|Method  |Description  |
|---------|---------|
|Numeric Units     |     For objectives tracked based on a numeric unit, the progress of the objective will be the **sum of numeric key results**.     |
|% Units |    For objectives tracked based on the % unit, the progress of the objective will be calculated as the **weighted average of all key results**, whether they're metric based, or are just going to reach 100% completion. You can also set individual key results that don't contribute to the parent.     |

### Objectives measured based on the numeric unit

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

### Objectives measured based on the % unit

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

### Objectives measured based on the % unit can have key results that're tracked by % metric or the numeric metric

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

## Different types of Progress modes

Engaging everyone with the company goals and driving greater OKR adoption is the primary responsibility of OKR champions and team managers. Better visibility into how the progress is updated will help them understand the user’s engagement with the objective.

Progress mode indicates how the progress of an OKR is updated. Increased visibility of the progress update helps users in better understanding their engagement with an objective. In addition, you can have greater control over determining the progress mode of an objective, and change it as you see fit. There are three methods of updating the progress, which are described in the following table:

|Method  |Description  |
|---------|---------|
|Manually     |  Progress of the objective will be determined by the objective owner through a registration made manually.        |
|Automatic via rollup from children     |     Progress of the objective will be rolled up automatically from the key results.     |
|Automatically from a data source     |     Progress of the objective will be updated automatically based on the data from an integration.     |

### Identifying the progress mode

If your OKR is measuring progress by percent of completion, it can be in one of the three progress modes described in the following table:

|Mode  |Description  |
|---------|---------|
|Manual     |  In this mode, the progress and status can only be changed by the users making registrations.        |
|Automatic via rollup from children     |     In this mode, the progress and status will be updated as children update their progress and status. This mode is the default mode every OKR starts in.     |
|Automatically from a data source     |     In this mode, progress will come from an integrated data source, and status updates will be based on the progress.     |

> [!NOTE]
> If you have Projects in Viva Goals, you can register yourself on these projects manually. When you switch to the automated mode, the progress will roll up from tasks beneath the projects — these tasks can either be added in Viva Goals directly, or through an integration. For more information on the Projects integrations supported, see [Projects](https://help.ally.io/en/articles/4224975-what-are-projects).

:::image type="content" source="../media/goals/identifying-progress-mode.gif" alt-text="Identifying the progress mode":::

### Setting the progress mode for an OKR

**When creating or editing your objective**

When you create or edit an objective, you can determine how the progress will be updated. If your objective is measured by percent of completion, you'll have three progress modes to choose from — manually, automatic via roll-up from children, automatically from a data source. However, if your objective is measured with a KPI, you won't be able to update the progress via roll-up because we don't want to override the metric. You''ll have to automate the update through an integration, or register manually.

:::image type="content" source="../media/goals/create-or-edit-objective.gif" alt-text="Create or edit an objective":::

**From the list view**

The icon to the left of the progress bar is indicative of the progress mode. You can select the icon to change the progress mode, or you can make a registration instantly by leveraging the slider progress bar.

:::image type="content" source="../media/goals/list-view.gif" alt-text="List view":::

**When making a registration**

If the progress of your objective is updated automatically, you can make a registration and switch to the manual progress mode in which case, the automatic progress will be overridden by the manual registration. You can always switch back to previous progress mode to resume updating the progress automatically from the children or the connected data source.

If the progress is rolled up automatically from the key results, perform the following steps:

1. Select the rollup icon and select the **Check-in** button.
1. Make a registration as you see fit and save it. You'll notice the change in the icon that represents the manual mode.
1. To switch back to the previous mode, select the manual icon and select the **Check-in** button.
1. Save this registration as you'll have the option to resume updating the progress from key results.

If the progress is rolled up automatically through an integration, perform the following steps:

1. Select the integration icon and select the **Check-in** button.
1. Make a registration as you see fit and save it. You'll notice the change in the icon that represents the manual mode.
1. To switch back to the previous mode, select the manual icon and select the **Check-in** button.
1. Save this registration as you'll have the option to resume updating the progress through the connected data source.

### Check-in reminders

If you switch an OKR or a project into the manual override progress mode, you'll receive registration reminders for it as long as it stays in the manual mode. Once you revert it to the automated progress mode, whether by rollup or from integration, you'll no longer receive reminders for registration.

## Shared OKRs/projects - Multiple teams and owners

The Shared OKRs/projects feature in Viva Goals is a great method for multiple teams and owners to collaborate on their key priorities and initiatives with equal ownership.

### When to create shared OKRs/Projects with Multiple Teams/Owners?

- When an OKR is a key priority for two or more functional teams and the team leads need to have shared accountability as the exact contribution cannot be proportioned or separately broken down between them. When both the teams are supposed to commonly own and work toward the outcomes, it's good to tag multiple stakeholders and not just a single team/owner as accountable.


    ```azurepowershell
    Example 1:
    OBJECTIVE: Enhance the onboarding strategy.
    KEY RESULT: Implement a new program to increase the repeat rate of 1st-time bookers. 
    [Entity: Team(s) - CRM Team & Marketing Team]
    [Owners: CRM Lead & Marketing Lead]
    
    Example 2: 
    OBJECTIVE: Build a world class Engineering org.
    KR/INITIATIVE: Invest in 2 Training & Development sessions + Capstone Projects for all 4 engg. teams this quarter
    [Entity: Engineering Department]
    [Owner: VP-Engineering & All Engineering Managers]
    
    Example 3:
    OKR: Facilitate seamless Annual & Quarterly Goal planning across the org.
    [Entity: Org level]
    [Owners: CEO & VP - Strategy & Operations]
    ```

In the above examples, if not for Viva Goals' flexible shared OKR model, it gets cumbersome to create duplicate and redundant OKRs for every team/individual when they're supposed to be commonly owned, worded, and measured.

### What different types of Shared OKRs are possible in Viva Goals?

|Shared OKRs |Description  |
|---------|---------|
|OKRs at an Organizational-entity level     |   These OKRs can have Multiple Owners.      |
|OKRs at team-entity level     |    These OKRs can have multiple teams tagged and respective Team administrators/members tagged as owners.     |
|OKRs at individual-entity level    |    These OKRs can have multiple users assigned as owners.     |

A DRI (Directly Responsible Individual) is accountable for ensuring that OKRs are being properly defined, measured, and accomplished. Multiple owner assignments can hamper accountability and encourage lack of discipline. Check whether it's absolutely essential for your OKR process before adopting it.

### When NOT to create shared OKRs?

- For organizational/team/individual-level OKRs, where there is clarity on the exact key result metrics or projects to be owned by respective teams and owners, don't create a single OKR and share it among all; instead, create an objective at the required entity level and create respective single team-level key results owned by a single DRI so that it's deconflicted.

    ```azurepowershell-interactive
    Example:
    
    OBJECTIVE: Skyrocket revenue in 2021!
    [Entity: Org level]
    [Owner: CEO]
    
    KR1: Double the ARR every quarter.
    [Entity: Sales]
    [Owner: VP-Sales] 
    
    KR2: Maintain a 120% Net Revenue Retention Rate.
    [Entity: Customer Success]
    [Owner: VP-CS]
    ```
- For cross-functional teams where all different stakeholders are part of respective mission teams, the objective can be owned by a single team with KRs being worked upon by respective function-related DRIs within the team.

    ```azurepowershell-interactive
    Example:
    
    OBJECTIVE: Provide best-in-class integration experience for customers.
    [Entity: Team - Integrations & Partnerships Mission team]
    [Owner: Mission Team Owner]
    
    KR1: Go above & beyond on 5 Enterprise & 5 SMB platform integrations.
    [Team: Integrations & Partnerships Mission team]
    [Owner: Product lead]
    KR2: Enhance the Integration sync time performance by 3x.
    [Team: Integrations & Partnerships Mission team]
    [Owner: Engineering lead]
    KR3: Partner with the top 3 industry leading HRIS providers.
    [Team: Integrations & Partnerships Mission team]
    [Owner: Marketing/Partnership lead]
    ```

### Enabling the Shared OKRs feature for your organization

OKR administrators can turn on the "Shared OKRs" feature from the **OKR & Projects** tab within the admin settings.

:::image type="content" source="../media/goals/enable-shared-okrs-feature.png" alt-text="Enable Shared OKRs feature":::

In case you disable the feature, multiple teams and owners who had been assigned to OKRs will continue to exist. Once this feature is disabled, users can only add single owners to OKRs and projects.

### How to create shared OKRs for multiple teams?

1. Log in to Viva Goals and select the **+** button on the top panel to create a new OKR.
1. Once you enter the objective/key result and want to share it with another team, select **Team** from the dropdown list under **Type**. 
1. Scroll down or search in the search bar for the team of choice.
1. Select the team and save the objective/key result. You'll start sharing the OKR with that team.

Users can also assign multiple teams to projects by implementing this procedure.

### How to create shared OKRs with multiple users as owners?

1. Log in to Viva Goals and select the **+** button on the top panel to create a new OKR.
1. Once you enter the objective/key result and want to share it with another individual, select **Owners** from dropdown list under **Owners**. Here, you can assign multiple owners for the OKR.
1. Once you select the owner, save the objective/key result. You'll start sharing the OKR with that individual, and the user who has been assigned as the owner will also receive an in-app notification of the assignation.

### Registrations for single and multiple owners

If there is just one owner or multiple owners assigned to an OKR and you would want a user within the organization to check in and update the progress of the OKR, you can use the "check-in responsibility" feature. The check-in owner will be able to check-in on the OKR (manual check-in) and set up a data link on the OKR (to auto-check-in). This user will be receiving the check-in reminders. In the case of multiple owners, this feature will prevent all of the owners from receiving reminders, and only the user set as 'check-in responsible owner' will receive the reminders.

To assign responsibility for check-ins, perform the following steps:

1. Log in to Viva Goals and select the **+** button on the top panel to create a new OKR.
1. Once you enter the objective/key result and want to share it with another individual, select **Owners** from dropdown list under **Owners**. Here, you can assign multiple owners for the OKR.
1. Once you assign an owner, select the user who will be responsible for making check-ins from the **Who is responsible for making check-ins?** drop-down. Once you make the selection, the user will start receiving the check-in reminders.

By default, the owner (the first owner in the case of multiple owners) is set as the person responsible for check-in and users need not explicitly choose, unless necessary.

## Drag and Drop: Reordering OKRs

To drag and drop an objective, perform the following steps:

1. Hover your mouse left of the objective name until you see the display of the icon depicted in the following image:

   :::image type="content" source="../media/goals/display-of-icon.png" alt-text="Display of icon":::

2. Click and hold your cursor to grab the objective.

3. Drag it to the desired location and alignment.

To make an objective become a key result, drag the cursor to the **+ Add key result** icon under the objective.

:::image type="content" source="../media/goals/making-an-objective-a-key-result.png" alt-text="Making an objective a key result":::

You can just as easily drag a key result out from under an objective to make it become an objective itself. Both examples are covered in the video below.

> [!NOTE]
> Drag-and-drop is available at the organizational, team, and individual levels.

### OKR model configuration settings and how it impacts drag and drop

1. If you've selected the **Objectives are always aspirational, key results are always measurable** option in the Admin Dashboard, you can drag an objective and drop it under a key result when you have additionally enabled the **Allow objectives to be nested under key results** settings.
1. You can drag a key result and drop it to nest it under another key result only when you've enabled the **Allow key results to be nested under key results** option in the Admin Dashboard. 

### FAQs

1: Can I add or edit OKR alignment?

A: You can add or edit OKR alignment on any OKR that hasn't been scored.
   
2. When would I want to keep my objective in manual progress mode instead of having it update automatically?

A: When you choose to update the progress automatically (through an integration or a rollup from children), the progress of the objective will be updated automatically based on the data fetched from the data source, or will roll up based on the progress of children. However, in some cases, this automated progress update might not accurately reflect the progress made on the objective. In such cases, you can override the automated progress update, and make a registration as you see fit. This registration that you make manually will not be overridden by the data from the integrated source or from the children until you change the progress mode back to automated. This registration will give you the much-needed control over progress updates to present accurate data during reviews.

3. Can I make a check-in by simply adding a note and changing the values of progress and status, without changing the progress mode?

A: Yes, you can make a manual registration to override the automatic values, and still choose to retain the automated progress mode. When you make a manual registration, you'll find a checkbox to stop updating the progress automatically. By not checking this checkbox, you can retain the automated progress mode.
