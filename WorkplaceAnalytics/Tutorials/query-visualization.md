---
# Metadata Sample
# required metadata

title: Visualize person queries
description: View query results in charts without leaving Workplace Analytics
author: paul9955
ms.author: v-pascha
ms.date: 06/19/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Visualize person queries

Analysts can be tasked with finding ways to improve teamwork in their organization. For example, you might want to discover teams whose members regularly work longer after hours or who don’t seem to have enough focus time. To help you in this task, Workplace Analytics offers the [Person query](person-queries.md), which includes a number of standard and custom metrics that can help you perform analyses of this kind.  

After you create and run a Person query, you can view its results (in charts) without leaving Workplace Analytics. You can refine your results view by focusing the charts on any of the metrics that you used in the query or on any organizational data attribute that have been uploaded. 

These query results might indicate groups of employees that could benefit from a [Teamwork solution](solutionsv2-intro.md) plan. You can create such a plan by starting with the displayed query results. In a chart, select the group that you identified and complete the subsequent steps to create a Solutions plan.

In addition to these capabilities, you still have the option of exporting results to view them in a data visualization tool such as [Power BI](../use/view-download-and-export-query-results.md#use-workplace-analytics-data-in-power-bi-excel-or-other-data-analysis-tool). 

This article describes how to view these results in the following steps:

1. [Run a query and view results](#run-a-query-and-view-results) 
2. [Customize your data visualization](#customize-your-data-visualization)

   As you examine your results, you might uncover a group of employees who could benefit from a Solutions plan. If this is the case, you can start the process by submitting and validating that group: 

3. [Submit a group ](#submit-a-group)
4. [Validate](#validate)

   After the group has been submitted and successfully validated, you can start the plan for the submitted group:
 
5. [Start the plan](#start-the-plan)

## Run a query and view results 

**Role:** analyst 

1. Open [Workplace Analytics](https://workplaceanalytics.office.com/). If prompted, enter your work credentials.

2. Expand **Analyze**, select **Queries**, and select **Person query**.

3. Define and run a person query. For more information, see [Person queries](person-queries.md). 

4. After the query finishes, open the **Results** tab.

5. In the row of the query's results, select the **Visualize** option: 

   ![Query row with Visualize](../images/wpa/tutorials/visualize-option-results-row.png)

   This opens a page in the **Analyze &gt; Queries &gt; Results** area of Workplace Analytics. The title of the page matches that of the query. The following illustration shows the results page of a person query that was named "Collaboration Overload": 

   ![Results chart](../images/wpa/tutorials/collab-overload-q-results.png)

   This interactive results page lets you use a variety of charts to explore the output of your query. Go on to the next procedure,[Customize your data visualization](#customize-your-data-visualization).

## Customize your data visualization 

**Role:** analyst 

The following steps are all optional. You can use them to refine your view of the query results in various ways. 

1. **Modify filters and metrics.** Use the **Page settings**
panel to modify the date range, the filters that are applied, and the metrics that you want included in your chart. Note that the kind of chart you are viewing could affect the view options that are available to you. For more information about using these settings, see [Page settings and filters](../use/chart-types.md#page-settings-and-filters). 

2. **Change chart attributes.** Use the chart toolbar to change the chart type, the chart's sort order, and the number of groups that are displayed. Some options are available only with certain chart types.  

3. **Investigate groups.** Select particular groups in the chart to activate options for drilling down or for excluding. The groups that you select will be reflected in both the chart display and also in the settings panel. Groups will reset if you change the chart type or the sort order.  

As you add and apply filters and select groups, the chart section of the results page updates its overview of the population that you are working with. You can now select a group of employees who might benefit from participating in a Solutions plan. See the following section, [Submit a group](#submit-a-group).  

## Submit a group 

Queries often serve as a means to identify opportunities for improvement and the groups who would benefit. Query visualization lets you find and save the opportunities that you discover in the query results. Then, you can act on those opportunities by using them to create a plan in the Solutions area of Workplace Analytics. 

For more information about solutions, see [Teamwork solution introduction](solutionsv2-intro.md). 

**Role:** analyst 

1. While visualizing a query result, in a chart, select one or more groups by clicking them in a chart. In the following example, the Marketing group is selected:

   ![Query results chart with group selected](../images/wpa/tutorials/q-viz-chart-marketing-group.png)

Note the size of the selected group, which is displayed to the right of the **Selected group** bar near the bottom of the page. In this case, it has 50 members. 

The group size is important because query visualization, along with Workplace Analytics queries in general, adheres to the [minimum group size](../use/settings.md#minimum-group-size) that has been set for your organization. If you've selected a group smaller than the minimum group size, you see a warning that the "filter group is below the minimum size." 

2. Once you have a group selected that meets or exceeds the minimum group size, select **Submit group**. This opens the **Set up new plan** pane:

   ![Set up new plan](../images/wpa/tutorials/set-up-new-plan-qv.png)

Go on to [Validate](#validate).

## Validate

1. For **Plan type**, choose an appropriate plan type for that group that you designated and select **Start now**.

2. (Optional) Type a description of your new plan

3. Select **Validate** to validate the group that you've selected. Workplace Analytics displays warnings if the email addresses of plan participants are faulty or if participants' licenses are missing. (For more information, see [Validation](solutionsv2-conceptual.md#validation).)

   If validation fails, you might decide to return to your query results and select a different group or additional groups, or to start over. After any subsequent group selection, you must select **Validate** again. 

After validation succeeds, go to [Start the plan](#start-the-plan).

## Start the plan

After the group that you’ve selected validates successfully (even if there are validation warnings), if your group size meets or exceeds the minimum group size, you can finish setting up your plan. 

![Set up new plan](../images/wpa/tutorials/set-up-new-plan-qv-final.png)

1.	(Optional) Change the **Plan name** to a name more meaningful to you than the suggested value.
2.	(Optional) Set the **Plan duration**. To do this, set the start date. (You must choose a Sunday because all plans start on Sundays.) The plan’s end date is then calculated and displayed.
3.	(Optional) Change the **Plan target** to a different value. Note that you can select only percentage-based targets, such as a 10% decrease in after-hours work. 
4.	Select **Create plan**. This schedules the plan you chose for the group you selected to start and end on the dates displayed for **Plan duration**. 
