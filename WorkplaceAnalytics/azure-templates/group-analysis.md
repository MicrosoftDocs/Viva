---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Group Analysis Azure Template for Workplace Analytics 
description: Learn about the Group Analysis Azure Template for Workplace Analytics and how to use it for advanced data analysis
author: madehmer
ms.author: v-midehm
ms.date: 07/11/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---
# Workplace Analytics Group Analysis Azure Template

_These templates are only available as part of a Microsoft service engagement._

Workplace Analytics Azure Templates includes the Group Analysis template that enables you to compare two groups, such as managers and individual contributors, and determine the major differences between them.

You can choose which metrics to analyze and which attributes remain the same between the groups to foster a more robust comparison. This type of analysis can help proactively discover and address areas that need improvement in your organization.

After you upload a dataset, you can use the template tools to view data for the two groups with visual charts and lists, as shown in the following graphic.

   ![Group analysis](./images/group-analysis.png)

## To add a new dataset

1. In Workplace Analytics Azure Templates, select **Group analysis**.
2. Select **Add New Dataset** at top right of the table.
3. For **Upload Dataset**, type a dataset name, select the .csv file to upload, and then select **Upload Dataset**.

   ![Select a dataset type](./images/group-dataset.png)

4. After the upload succeeds, it'll be available in the Group Analysis list.

## To configure new analysis

1. Select the new dataset from the list.
2. Select **Add New Analysis**.
3. In **Configure New Analysis**, type a name for the **Dataset Info**.
4. In **Specify Group to compare**, select the filters for the group that you want to evaluate.
5. In **Choose Group name**, type a name for the group you want to evaluate.
6. In **Specify KPIs to compare the group on**, select all the metrics that you want to compare between the evaluated group and the control group.
7. In **Choose confounding attributes**, select the attributes that define the evaluated group and the control group and that the two groups have in common. Note these must be different than the filter or filters selected in the **Specify Group to compare** section.
8. Select **Run Analysis**.

## Analyze KPIs

You can use the group analysis to view the key performance indicators (KPIs) between the defined group you chose to analyze and the control group you're comparing with. The KPIs help distinguish the differences between the two groups.

The Match verification helps you confirm that you have sufficient overlap of confounding attributes between the evaluated group and the control group. You must have sufficient overlap between the two groups to get good data results. If there's no overlap, that means you've already identified one of the confounding attributes that distinguishes the differences between the two groups and you need to go back and choose different filters or confounding attributes for helpful analysis.

The Group Analysis shows the Absolute and Standardized differences between the two groups. This gives you an overall picture of what the important differences are between the evaluated and control groups.

## To view analysis

1. Select the dataset that has the analysis you want to view from the list.
2. Select the name of the analysis that you want to view.
3. In **Match verification**, compare the data in the box plots for **Before Match** and **After Match**.

   * **Before Match**: Before any matching occurred, the **Propensity scores** are the distributions between the two groups, which are the result of comparing the confounding attributes to show how likely a person is to be in the evaluated group based on those attributes. You can hover the cursor over the data in the graph to view the details.
   * **After Match**: After the matching procedure occurs, this shows how well aligned the distributions are between the two groups, which helps you decide if the match worked and the results will be helpful.

4. In **Group Analysis**, you can view the analysis results in bar graphs with a **Cohen Rank Color Legend** that defines how big of an affect the differences are between the two groups. The data shows the Absolute KPI Difference, which is the absolute differences between the two groups. The Standardized KPI Difference shows how important the differences are based on their size.
5. In **Sensitivity**, shows the least sensitive to unobserved biases in a bar graph with a **Cohen Rank Color Legend** as well. This shows a subset of the most sensitive KPIs based on sensitivity analysis of unobserved biases found in the standardized KPIs. 

## Related topics

* [Workplace Analytics Azure Templates overview](./overview.md)
* [Deploy and configure Workplace Analytics Azure Templates](./deploy-configure.md)
