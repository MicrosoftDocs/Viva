---
# Metadata Sample
# required metadata

title: Workplace Analytics solution walkthrough
description: A walkthrough of the steps required to create a plan by using the Workplace Analytics solution
author: paul9955
ms.author: v-pascha
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Solution walkthrough

You can use the solutions feature of Workplace Analytics to create improvement plans for employees, with the goal of changing their work habits for the better. By using solutions, you can create a plan, track it while it is in progress, and examine it after it completes.
 
People in the following roles can work on improvement plans in various ways:

 * **Analysts**, **limited analysts**, and **program managers** can identify groups of employees and opportunities for change, design and start plans, track plans that are underway, and examine plans that have completed.

<!-- UNCOMMENT THIS AS SOON AS WE RELEASE THE GM ROLE: 
 * **Group managers** can start plans to improve the work habits of employees in their reporting structure. 
-->

 * **MyAnalytics users** participate in plans. For more information, see [The experience of plan participants](solutionsv2-participants.md).  

> [!Note]  
> If you have been assigned multiple roles, your capabilities are expanded. See [User roles in Workplace Analytics](../use/user-roles.md). 

## Create a plan

**Role:** If you have the role of analyst, limited analyst, or program manager, the steps in the following sections apply to you. 
<!-- UNCOMMENT THIS AS SOON AS WE RELEASE THE GM ROLE: If you are a group manager, see [Plan creation for group managers](#plan-creation-for-group-managers). -->

To create a plan, we will follow the steps in these procedures:

1.	[Start the plan definition](#start-the-plan-definition)

2.	[Select a group](#select-a-group)

3.	[Start the plan](#start-the-plan)

### Start the plan definition

**Role:** analyst, limited analyst, or program manager

1. Open [Workplace Analytics](https://workplaceanalytics.office.com). If prompted, sign in with your work account.

2. In the left navigation pane, select **Solutions**. 

3.	On the Solutions page, the plan types are described: _Focus plan_, _Collaboration plan_, and _Wellbeing plan_. Consider the type of plan you want to create:

    ![Pick a plan](../images/wpa/tutorials/pick-a-plan.png)
 
    > [!Note]  
    > On this page, the **Analyze** option is available only to people with the role of Analyst or Limited analyst.

4.	Do you have a group of employees in mind for participation in a plan? If so, select **Start now** for the plan that you want that group to use, and go to step 5. If you do not already have a group picked out, go to [Find the group through analysis](#find-the-group-through-analysis). (The procedure described in [Find the group through analysis](#find-the-group-through-analysis) is available only to people with an analyst role in Workplace Analytics.) 

5.	In this example, we select **Start now** for the _Focus plan_. This opens the **Set up new plan** panel for the Focus plan, which shows default values for the plan, such as its name:

    ![Set up a new plan](../images/wpa/tutorials/set-up-new-plan-panel.png)
 
Go to [Select a group](#select-a-group).

### Select a group

**Role:** analyst, limited analyst, or program manager

If you have a particular group in mind, you can identify the group either by [uploading a .csv file](#upload-a-csv-file) or by [using filters](#use-filters). (If you don’t have a group in mind, go to [Find the group through analysis](#find-the-group-through-analysis).

#### Upload a .csv file

1. Obtain the .csv file to upload. The format of this file is simple: a list of email addresses in a single column. To obtain this file, you might have exported it from an HR system. 

1.	Select **Upload .csv file**.

2.	Select **Browse**, select a .csv file, and then select **Open**.
 
3.	After the file has been uploaded, select **Validate**. 

    ![Validate](../images/wpa/tutorials/browsed-validate.png)

    Workplace Analytics reports whether the group successfully validated, and it also displays any warnings that are generated. For more information, see [Validation](solutionsv2-conceptual.md#validation).

4.	After the group validates successfully, go to [Start the plan](#start-the-plan). 

#### Use filters

1.	Select **Use filters**. This opens the filter controls:

    ![Filter to find a group](../images/wpa/tutorials/filter-to-find-group.png)
 
2.	Add filters to define your group. For example, select **FunctionType**, **Equals**, and **Marketing** in the fields to select the people who work in business strategy as your group. Optionally, add more function types to expand this group, or add more filtering criteria to refine the selection. 

3.	Select **Validate**. 

   Workplace Analytics reports whether the group successfully validated, and it also displays any warnings that are generated. For more information, see [Validation](solutionsv2-conceptual.md#validation).

4.	After the group validates successfully, go to [Start the plan](#start-the-plan). 

### Find the group through analysis

If you do not already have a group in mind for a plan, you can analyze the work habits of a larger segment of your organization to identify a group that could potentially benefit from a plan. 

> [!Tip] 
> These steps work best if you start them after you’ve decided on the type of plan. Where might people in your organization have a problem? The available plans address too few focus hours (Focus plan), too many hours of meetings and other ways of working together (Collaboration plan), or too much collaboration after the workday ends (Wellbeing plan).

   ![Pick a plan](../images/wpa/tutorials/pick-a-plan.png)
 
#### To identify a group by using filters and charts

1.	On the **Solutions** page, in the card for one of the plans under **Available plans**, select **Analyze**. (In this walkthrough, we select **Analyze** on the Focus plan card.) The **Filter and analyze** page appears.

2.	(Optional) Although you just selected a plan type on the preceding page, if you decide that a different type is better, you can change it. To do this, select the text (such as **after hours**) in the **Filter and analyze** banner:

    ![Filter and analyze](../images/wpa/tutorials/filter-and-analyze.png)
 
3.	Scope your data. To start, narrow the focus to specific people by applying filters. You apply filters in the **Page settings** area, in the right column of the page. If this area is not showing, select **Settings and filters** to re-display it:

    ![Filter and analyze](../images/wpa/tutorials/settings-and-filters.png)

    The **Page settings** panel opens:

    ![Page settings](../images/wpa/tutorials/page-settings.png)
      
4.	Use **Page settings** to refine your selection of employees and to change the way the groups of those employees will be displayed. For example, you can add a filter to show only employees in the East and Southeast regions and you can change the maximum number of groups to display to 10. After you have finished adding filters, select **Apply**. The main section of the page changes to reflect your new filter settings.

5.	To select a more precise group of people to include in the plan and continue with your analysis, you can use the **Select a question to change the view of your chart** options, such as: **Which groups attend the highest number of meetings?** 

    ![Select a question](../images/wpa/tutorials/select-a-question.png)

    Selecting a question shows the answer to the question in the chart. By selecting a question that is relevant to the collaboration problem that you want to solve, you will see groups of employees who are most likely to exhibit symptoms of that problem. Selecting a question also orders the groups shown by their metrics (such as meeting hours, focus hours, or number of meetings) based on what the question asks about.

    The chart has vertical bars that represent different groups of people. If a bar that represents a group is displayed, that group meets or exceeds the minimum group size. Any groups smaller than the minimum group size do not show up in the chart because they are too small to analyze. (Also see [Minimum group size](solutionsv2-conceptual.md#minimum-group-size).) 

    <!-- For example, if the organization you are analyzing has a minimum group size of five, you can change it to a level that you consider more relevant for your organization. However, you cannot set the group size lower than five. In the following chart, the Data & Applied Sciences group contains fewer than five people, so its bar is shown as grayed out: -->
 
    See also [Available and selected employees](solutionsv2-conceptual.md#available-and-selected-employees).

6.	Select one or more groups for analysis. To select multiple groups, just click or tap them. To unselect a selected group, click or tap it again. For more information about what happens with selected groups when you make other settings on this page, see [Persistence of group selections](solutionsv2-conceptual.md#persistence-of-group-selections).

7.	After you select a group, Workplace Analytics displays additional information about this group’s work habits, such as the following: 

    ![Three cards](../images/wpa/tutorials/three-cards-start-now.png)

8.	After you have identified the groups, select **Start now**. The **Set up new plan** panel is displayed:

    ![Set up new plan](../images/wpa/tutorials/set-up-new-plan-panel-2-75.png) 
 
    > [!Note]  
    > Because we have chosen to use analysis to find the group and because using filters is an important part of that analysis, this page displays **Use filters** as the default way to proceed. Nevertheless, this page gives you the option to change direction and upload a file, by selecting **Upload .csv file**. 

This page also displays the filters that you have already set in the charts and any filters that you have already applied. 

9.	(Optional) Change the filters that you’ve created, or add new filters to further refine this group. 

10.	Select **Validate**. After validation completes, Workplace Analytics displays the results:

    ![Validation warnings](../images/wpa/tutorials/three-warnings.png)
 
11.	Any warnings reduce the number of potential members in the group. If the remaining group size is above the minimum group size, you can proceed. If you are satisfied with the group at this point, go to [Start the plan](#start-the-plan). 

## Start the plan 

**Role:** analyst, limited analyst, or program manager

After the group that you’ve selected validates successfully, Workplace Analytics displays insights about the group that you've submitted. They show you how the group’s numbers differ from company averages for the context that you chose. For example, if you chose to create a Focus time plan, Workplace Analytics displays metrics – such as the number of hours in meetings per week – that illustrate why the people in this group could benefit from more Focus time. (Although these insights are informative, they are not interactive.)

1.	(Optional) Change the **Plan name** to a name more meaningful to you than the suggested value.

2.	(Optional) Change the **Plan target** to a different value. Note that you can select only percentage-based targets, such as a 10% decrease in after-hours work. 

3.	(Optional) Set the **Plan duration**. To do this, set the start date. (You must choose a Sunday because all plans start on Sundays.) The plan’s end date is then calculated and displayed. 

4.	(Optional) Scroll down to the **How Solution will help** section, which contains cards for **Book and protect**, **Stay focused**, and **Track progress**:

    ![How solutions help](../images/wpa/tutorials/how-solns-help.png)
  
    To see how this plan will appear for participants, select **See preview**. Here, you see examples of the inline suggestions, the personal dashboard, and the digest email that people will experience while participating in the plan. Similar to the insights, these previews are informative but not interactive. 

    In these previews, you can see a brief description of "habits" that participants will learn about. Following these habits can help them reach their plan’s target. For example, rescheduling meetings that conflict with their focus time is a habit that can help a participant reach a target of increased focus time. Three habits are suggested for each plan type. 

5.	Select **Create plan**. This schedules the plan you chose for the group you selected to start and end on the dates displayed for **Plan duration**.

## Track plans 

**Role:** analyst, limited analyst, or program manager. 
<!-- UNCOMMENT THIS AS SOON AS WE RELEASE THE GM ROLE: (For Group managers, see [Track progress (Group manager role)](#track-progress-group-manager-role)) -->

You can track programs on the **Manage** page. Use this page to measure progress on the target since the plan started, as well as ROI for the plan. 

### To track an active plan

1. The table on the **Solutions > Manage** page displays plans that can be either scheduled or active. To see active plans, select **Active** in the toolbar above the table. 

2. In the row of the plan you want to investigate, select **Track** to display the _tracking dashboard_, which shows information about the progress of the plan up to this point. 

<!-- UNCOMMENT THIS AS SOON AS WE RELEASE THE GM ROLE: 
## Plan creation for group managers

The role of group managers (GM) differs from other Workplace Analytics roles in that its scope is predefined and unalterable: All employees in the reporting structure under a GM are automatically assigned to their group. (The GM is also included in this group.)

For more information about roles in Workplace Analytics, see [User roles](../use/user-roles.md). 

### Create a plan (group manager role)

A plan that a GM creates automatically contains the data of the GM's group (the GM's reporting structure). All members of the group, including the GM, are automatically signed up for the plan. 

**Role:** Group manager

1.	As a GM, when you open Workplace Analytics, you go directly to the **Solutions** page: 

    ![Group manager view](../images/wpa/tutorials/gm-view-solns-2.png)
 
    This page shows three plans: _Focus plan_, _Collaboration plan_, and _Wellbeing plan_. Consider the type of plan that you want to create. The card for each plan describes the plan and offers **Start now** and **Analyze** options. 

2.	(Optional) For a particular plan, select **Analyze**. This displays read-only summary data about your team as a whole. This data pertains to that plan’s area of focus. For example, if you select **Analyze** on the _Focus plan_ card, you will see data that pertains to that plan with regard to your team. After you view this information, select **Start now** and then go to step 4.

    > [!Note]  
    > You cannot view summary data about your team if its size does not exceed the minimum group size. Workplace Analytics admins can set a minimum group size for GM teams that differs from the general Workplace Analytics setting for minimum group size. 

3.	For one of the three plans, select **Start now**. This opens the **Set up new plan** panel:

    ![Group manager -- set up new plan](../images/wpa/tutorials/gm-set-up-new-plan.png) 

4.  Check the figure that is shown on this page for **Number of direct and indirect reports**. If this team size looks incorrect, contact your admin. They should examine the organizational data (HR) file and the manager hierarachy within that file for errors.
 
5.	Select **Validate**. 
  
    After validation finishes, Workplace Analytics shows any resulting details, warnings, and insights about the group. The warnings might indicate that some potential participants are ineligible for various reasons. If, after validation, there are enough participants for the plan, select **Start plan**. This displays the _Your plan was successfully submitted_ page: 
    
    ![Group manager -- set up new plan](../images/wpa/tutorials/gm-set-up-new-plan-2.png) 
 
### Track progress (Group manager role)

Once a plan is underway, you can view the **Manage** page to track the plan’s progress. Note that you can see progress for your team only, and only for a single plan. This is because your team can have only one plan underway at a time. (You cannot subdivide your team into smaller groups that run different plans simultaneously.)
-->

## Related topics

[Solution: Introduction](solutionsv2-intro.md)  

[Solution: Participants](solutionsv2-participants.md)  

[Solution: Concepts](solutionsv2-conceptual.md)


