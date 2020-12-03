---

title: Opportunities scan in Workplace Analytics
description: Learn how to scan for opportunities in Workplace Analytics
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Analyst
---

# Opportunities scan

An analyst who uses Workplace Analytics sometimes has in mind a goal or problem that they want to solve. For example, they might know of a problem to examine and which pockets of people are suffering from it, whether it is collaboration overload, excessive time worked after work hours, or something else.

Sometimes opportunities are less obvious. For this, it's possible to take advantage of the many workplace metrics that Workplace Analytics tracks. These metrics are calculated from data that Workplace Analytics extracts, on a regular basis, from available Office 365 data.

Workplace Analytics automatically scans to determine whether any [groups](#what-is-a-group) show unusual numbers in particular metrics. It then points out which groups show unusual activity on those metrics – for example, an excess of low-quality meetings, or a lack of focus time.

Then, as an Workplace Analytics user with the analyst, limited analyst, or PM role, you can start a plan to respond to this unusual activity. To do this, you'd use the Opportunities scan feature to create such a plan for the affected group.

## Use Opportunities scan to find potential opportunities

Workplace Analytics runs AI-based detection every week as part of the standard weekly data processing. This detection seeks outliers and anomalies in the data – in particular, it scans to determine whether any groups show unusual numbers for the following metrics:

 * Focus hours
 * Attendee meeting hours
 * Conflicting meeting hours
 * Multitasking meeting hours
 * Low quality meeting hours
 * After hours collaboration hours

### To find an opportunity

Scans are run weekly as part of standard Workplace Analytics processing runs, and newly discovered opportunities are surfaced as soon as they are available. To find one or more newly discovered opportunities, check the **Opportunities** page.

**Role:** analyst, limited analyst, or program manager

1. Open [Workplace Analytics](https://workplaceanalytics.office.com/). If prompted, sign in with your work account.

2. On the **Plans** page, select **Opportunities**.

    ![Select Opportunities](../images/wpa/use/opportunities.png)
 
    This page shows the most recent scan results, which are presented as opportunities for one or more groups.
 
    > [!Note]
    > If Workplace Analytics cannot detect anything in the data that would present an opportunity, it displays a notice that reads, "No opportunities could be loaded. Please check back later."

3. Consider which of the opportunities you would like to pursue. After you've decided to start a plan from an opportunity, go to [Create a plan](#create-a-plan).

## Create a plan

In the following example walkthrough, we look at the _Increase focus_ opportunity to see how to take advantage of an opportunity to create a plan for a group.

### To start a plan from an opportunity

**Role:** analyst, limited analyst, or program manager

1. Locate and select the **Increase focus** opportunity.

    ![Opportunities area](../images/wpa/use/increase-focus.png)

	For this opportunity, this page briefly describes the purpose of the opportunity (gain time for the work that matters most) and highlights possible benefits by taking advantage of the opportunity. For this example, Workplace Analytics identified five groups in the company that have limited focus hours.

    By taking advantage of this opportunity, the members of the [group](#what-is-a-group) could gain up to an aggregate of 98.4 hours per week of new focus time. (The more focus time, the better.)

2. The **Plans > Opportunities > Result** page has details about the opportunity.
 
    ![Increase focus potential](../images/wpa/use/opportunity-increase-focus-3.png)

    (The other opportunities, such as _Better meeting effectiveness_, follow this same model of data presentation.)

	The groups that are shown under **Select a group to analyze** are identified as potentially benefiting from a plan. If a group has appeared in this list for multiple weeks, they get a notification about this opportunity.
<!--    ![A group reappears](../images/wpa/use/multiple-weeks.png)-->
3. (Optional) Use the thumbs-up or thumbs-down icons at the right on the bottom of the page to indicate the relevance of this opportunity to your organization.

4. To create a plan for the group that you have selected, select **Start plan**.

    ![Create plan](../images/wpa/use/create-plan.png)

    This opens the **Set up new plan** panel that shows the default settings for this plan.

    ![Set up a new plan](../images/wpa/use/set-up-new-plan.png)

5. (Optional) Change the settings of the plan. You can edit its name, the start date, and the target. Once you're finished with the settings, select **Validate**. Note that the number of participants cannot be edited. It is determined by the organizational data that your admin has uploaded.

   Workplace Analytics reports whether the group successfully validated, and it also displays any warnings that are generated. For more information about these warnings and about the options upon a validation failure, see [Validation](#validation).

6. After the group validates successfully, you can now [create a plan](#to-create-the-plan).

### To create the plan

**Role:** analyst, limited analyst, or program manager

After the group that you've selected validates successfully, Workplace Analytics displays insights about the group. They show you how the group's numbers differ from company averages for the context that you chose. For example, if you chose to create a _Focus time_ plan, Workplace Analytics displays metrics&mdash;such as the number of hours in meetings per week&mdash;that illustrate why the people in this group could benefit from more focus time. (Although these insights are informative, they are not interactive.)

Workplace Analytics also displays default settings for the plan, which you can edit as follows:

1. (Optional) Change the **Plan name** to a name more meaningful to you than the suggested value.

2. (Optional) Change the **Plan target** to a different value. Note that you can select only percentage-based targets, such as a 10% decrease in after-hours work.

3. (Optional) Set the **Plan duration**. To do this, set the start date. (You must choose a Sunday because all plans start on Sundays.) The plan's end date is then calculated and displayed.

4. (Optional) Scroll down to the **How Plans will help** section, which contains cards for **Book and protect**, **Stay focused**, and **Track progress**.

    ![How the plan will help](../images/wpa/use/how-plan-helps.png)

    To see how this plan will appear for participants, select **See preview**. Here, you see examples of the inline suggestions, the personal dashboard, and the weekly digest that people will experience while participating in the plan. Similar to the insights, these previews are informative but not interactive.

    In these previews, you can see a brief description of "habits" that participants will learn about. Following these habits can help them reach their plan’s target. For example, rescheduling meetings that conflict with their focus time is a habit that can help a participant reach a target of increased focus time. Three habits are suggested for each plan type.

5. Select **Create plan**. This schedules the plan you chose for the group you selected to start and end on the dates displayed for **Plan duration**.

After the scheduled plan starts, data about its progress is collected. You can view this data by tracking the plan. See [Track plans](#track-plans).

## Track plans

**Role:** analyst, limited analyst, or program manager

You can track plans on the **Manage** page. Use this page to measure progress on the target since the plan started, as well as ROI for the plan.

### To track an active plan

1. The table on the **Plans > Manage** page shows plans that can be either scheduled or active. To see active plans, select **Active** in the toolbar above the table.

2. In the row of the plan you want to investigate, select **Track** to see the tracking dashboard, which shows information about the progress of the plan up to this point.

## Concepts

The following sections provide information that can help you as you use the Opportunities scan feature of Workplace Analytics:  

### What is a group?

You assign plans to groups, but just what constitutes a group? For Opportunities scan, a group is a team of individual contributors who all report to the same manager.

Managers are represented by the ManagerId attribute that admins upload regularly in organizational (HR) data. ManagerId is one of the five mandatory attributes in the organizational data file. As Workplace Analytics processes this data, it generates a management hierarchy that represents the entire organizational structure. 

Groups are defined from this organizational data structure and represented by their manager names. Manager names are obtained from Active Directory by using the values that you provided for the ManagerID attribute in the [uploaded organizational data](../setup/upload-organizational-data-1st.md) file. These manager names are then displayed in the **Result** page to represent the groups. 

> [!Important]
> Data for a group includes only the data for a manager's team. It does _not_ include the manager's data.

### Validation

During validation, Workplace Analytics checks the following about each potential participant:

 * <u>Valid address?</u> Is their email address valid? This check helps verify that the person still works for the company. An "invalid" email address means that the email address was formatted incorrectly or that the person is not a measured employee (they have no Workplace Analytics license or their data could not be processed). <!-- RE-ADD THIS AFTER WE PUBLISH THE DOC ON PARTITIONS (FORMERLY SCOPE), or the person is not in the partition that the user is currently working in. -->
 * <u>Have licenses?</u> Do they have a MyAnalytics license and a Workplace Analytics license? To participate in a plan, they must have both.
 * <u>In a plan?</u> Are they already enrolled in a plan? A person can be in only one plan at a time.
 * <u>Opted out?</u> Have they opted out of MyAnalytics? If the person has opted out, they cannot participate in plans.

After validation, Workplace Analytics reports the results, including the number of qualified participants. The results also show any warnings, which include the numbers of participants who’ve failed any tests.

![Validation warnings](../images/wpa/use/participants-warnings.png)

Three of the possible errors are shown here. If your number of qualified participants (25, in this case) is above the minimum group size, you can move forward with [starting a plan](../tutorials/solutionsv2-task#start-the-plan).

If the number of qualified participants falls below the minimum group size, you cannot proceed with this group as it is. To move forward, you need to make changes outside of Workplace Analytics. For example, you could ask an admin to assign licenses to those who are missing them, or you could try a different group.

As for employees who have opted out or are already in a plan, you cannot enroll them in a plan at this time.

<!-- REMOVE THIS FOR NOW, AS IT LINKS TO THE PARTITION DOC. REPUBLISH IT AFTER NITHIN HAS US PUBLISH THE PARTITION DOC.

### Opportunities scan adheres to partitions

In the following trend-line chart, the key to the black line indicates that it shows the median in the current partition: 

![Email hours as percent](../images/wpa/use/email-hours-as-percent.png)
 
This statement identifies the source of the data. That is, the data that was used to calculate this line was drawn from the partition (set of data) that is visible to the analyst who sees this page. For example, the person who sees this page might be logged in to Workplace Analytics as an analyst with "HR" partition. That HR partition&mdash;that HR set of data&mdash;is what produced this exact trend line.

A different analyst with a different partition would see a different trend line because that line would be calculated from different data. 

All of the opportunities that are presented and all of the data that is presented for each opportunity are drawn from the partition of the analyst who is viewing this page. Scopes are defined by admins; for more information, see [Scope in Workplace Analytics](https://docs.microsoft.com/Workplace-Analytics/setup/partition-in-wpa). 

-->
