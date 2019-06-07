---
# Metadata Sample
# required metadata

title: Organizational effectiveness query 
description: Describes the organizational effectiveness query of Workplace Analytics
author: paul9955
ms.author: v-pascha
ms.date: 06/06/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
---

# Organizational effectiveness

The organizational effectiveness query helps you find answers to the question: How do the most effective people – the best performing people in a company – collaborate differently from their peers? (Note: In this article, we’ll refer to these people as the reference group.) The immediate goal is to discover what unique workplace-collaboration traits make these people different. The larger goal is then to use these insights to try to spread these behaviors so that they can benefit these people’s peers and others in the company. 

You can work towards the first goal by creating an analysis of organizational effectiveness. To do this, you open the organizational effectiveness panel, add necessary data, submit the analysis request, wait for it to complete, and then view the results. 
For a complete walkthrough of these steps, see Start an organizational effectiveness solution. This end-to-end procedure consists of the following tasks:

1.	[Start an analysis](#start-an-analysis). 
2.	[Identify the reference group](). You do this either by using filters or by uploading a .csv file that contains the email addresses of the members of the group. 
3.	[Select the peer group](). After you’ve identified the reference group, you next identify one or more peer groups. This, too, you can do either with filters or by uploading a .csv file. 
4.	(Optional) [Apply conditions](). In this step, you help assure that your comparison makes sense for the groups that you’ve selected. 
5.	[Submit the analysis]().
6.	[View results](). View the results of your analysis. 

### Privacy note

The organizational effectiveness feature, of course, robustly enforces the minimum group size settings for your organization. In other words, if the number of members on a team that you select is smaller than the minimum group size, the analysis is halted and cannot continue. 

## Start an analysis

In this task, you take the first steps to start an organizational effectiveness analysis. 

**Role:** analyst, limited analyst

1.	Open Workplace Analytics.
2.	Expand **Analyze** and open the **Explore** page. This page has two sections: **Metrics overview** and **Analyze and start Solutions**.

    ![Explore page](../images/wpa/use/select-org-eff.png)

3.	Under **Analyze and start Solutions**, select **Organizational effectiveness**. 

    This displays a table of the organizational effectiveness analyses that have been started or completed. 
 
    ![New analysis](../images/wpa/use/explore-new-analysis-3.png)

4.	Select **New analysis** to initiate a new analysis. This opens a panel for creating the new analysis: 

    ![New analysis panel](../images/wpa/use/new-analysis.png)
 
The top of this panel shows the four steps for creating an organizational effectiveness analysis: _Top performers_, _Peers_, _Conditions_, and _Submit_.

5.	For **Analysis name**, type a name for this analysis. 

6.	Selecting a date range for the analysis.

7.	Go on to Identify the reference group.  

## Identify the reference group

Before you complete these steps, you should have decided which group within your organizational that you’d like to use for the reference group. 

**Role:** analyst, limited analyst

1.	In the **Reference group** section, identify the members of this group. This is a group of your choosing; its members need not be on the same team. You can identify them in either of the following two ways:

    * [Upload a .csv file](#upload-a-csv-file). For this, you’ll use a file that has been prepared with email addresses.  
    * [Use filters](#use-filters). To do this, you filter by HR (organizational) attributes. 

    > [!Note] 
    > For more information about which way to identify this group, see [Why use filters?](#why-use-filters)

2.	After you’ve successfully identified the reference group, select **Next** and go to [Select the peer group](#select-the-peer-group). 

## Select the peer group

In this task, you identify one or more peer groups that might benefit from a solution plan. 

**Role:** analyst, limited analyst

1.	In the **Peers** section, identify the members of the peer group. As with the reference group, you choose the peer group; its members need not be on the same team. You can identify them in either of the following two ways:

    * [Upload a .csv file](#upload-a-csv-file). For this, you’ll use a file that has been prepared with email addresses.  
    * [Use filters](#use-filters). To do this, you filter by HR (organizational) attributes. 

    > [!Note] 
    > For more information about which way to identify this group, see [Why use filters?](#why-use-filters)

2.	After you’ve successfully identified the reference group, select **Next** and go to [Apply conditions](#apply-conditions). 

## Apply conditions

In this optional step, you make sure that the right people in each of your selected groups are being compared. 

After you selected **Next** in the Peer group section, the **Conditions** page opens:
 
![New analysis panel](../images/wpa/use/analysis-conditions-2.png)

_[This section to be written.]_

For more information, see [Why apply conditions?](#why-apply-conditions)

## Submit the analysis

_[Give steps here. What do you click?]_
_How do you know that the analysis has completed? Do you need to _

## View results

After your analysis completes, its status is updated in the Organizational effectiveness analysis table with a check mark: 

![Table of analyses](../images/wpa/use/table-of-analyses.png)
 
You can do several things on this page:
 * <u>In the rows of analyses:</u>
   * Select **View** (eye icon) to open an analysis to see its results.
   * Select **Delete** (trash can icon) to delete an analysis that’s no longer needed.
 * <u>Above the table:</u> 
   * Select **New analysis** to create a new Organizational effectiveness analysis.
   * Refresh the list of analyses by selecting **Update list**.

Selecting **View** opens the **Result** page:
 
![Result page](../images/wpa/use/result-1-2.png)

At the top of this page,  you see the following information about your analysis: the analysis name, date rage, name of the reference group, and name of the peer group. 

The **Highlights** area displays the results of your analysis. The upper area presents summaries of the top three variant metrics for the groups. (Workplace Analytics selects these three metrics from among 20 metrics that are highly correlated.) The results you see are comparisons of raw averages between the reference group and the peer group. 

In this example, they are _External network size_, _1:1 meeting hours with direct manager_, and _Percentage of network from external relationships_.
 
Below these metrics summaries, the results for each metric are described in detail. Each detail section contains a description called **Why it matters**. This section explains why this metric analysis result is useful.
 
Although the **Result** page is read-only, you can download it into a file that you can open in Microsoft Excel or share with others.

## Task details

### Upload a .csv file

Follow these steps to upload a file that contains email addresses: 

1.	Select **Upload .csv file**: 
 
    ![Upload .csv file](../images/wpa/use/upload-csv-file.png)

2.	Browse to the file on disk and select **Open**. After the file uploads, Workplace Analytics automatically validates the uploaded data and displays the results:

    ![Validation results](../images/wpa/use/validation-results.png)
 
    In this example, the validation results contain the errors of invalid email addresses and a person who has no Workplace Analytics license. You can choose to fix these errors by correcting or deleting the invalid email addresses, or having an admin assign the missing license. (To participate, a person needs only a Workplace Analytics [license assigned](../setup/assign-licenses-to-population.md), not a Workplace Analytics [role](../setup/assign-roles-to-wpa-admind.md).) 

    Even if errors were found, you can proceed with the analysis if the group size meets or exceeds the minimum group size. In this example, the actual group size (25) exceeds the minimum group size (5), so you can start the analysis with this group. 

    > [!Note] 
    > In addition to the minimum group size, a maximum group size is also in effect. The maximum group size for organizational effectiveness queries is 150. 

3.	Return to [Identify the reference group](#identify-the-reference-group) or to [Select the peer group](#select-the-peer-group).
 
### Use filters

1.	To identify a group by filtering, select **Use filters**: 

    ![Use filters](../images/wpa/use/use-filters.png)
 
2.	Add filters and parameters.

In this step, you use organizational data in filters to refine your group selection. For example, in the left box, select **Organization** and in the right box, type an org name or a manager’s identifier. Add more filters to refine the selection further, if you want. The results of filtering are shown in a chart. You can then select groups by clicking the columns that represent them in the chart. You can select multiple groups. 

For more information about what happens with selected groups when you make other settings on this page, see [Persistence of group selections](../tutorials/solutions-conceptual.md#persistence-of-group-selections). 

Now, you could proceed with the analysis if the group size meets or exceeds the minimum group size. In this example, the actual group size (25) exceeds the minimum group size (5), so you can start the analysis with this group. 

> [!Note] 
> In addition to the minimum group size, a maximum group size is also in effect. The maximum group size for organizational effectiveness queries is 150.

3.	Return to [Identify the reference group](#identify-the-reference-group) or to [Select the peer group](#select-the-peer-group).  

## Concepts

### Why use filters?

A typical use case for using filters would be if your organizational uses outcome metrics such as sales quotas or performance or engagement ratings. If you admin has uploaded this data, you can build filters for this and for other types of Workplace Analytics queries. For example, while defining your reference group, you could filter to include employees who have achieved a particular sales quota or above. Then, one of your filters for the peer group could specify sales quota below the level that you chose for the reference group. Of course, if for some reason these metrics cannot be uploaded for your organization, you can always upload a .csv file that contains email addresses. 

### Why apply conditions? 

When you compare two groups of people, the purpose is to arrive at a meaningful comparison. For example, depending on your organization, it might not make sense to compare IT admins with software engineers. Their roles are different and so are the ways they are rated in performance evaluations and the expectations of how they interact with customers. 

For this reason, it usually makes no sense for an analyst to make a direct, unrefined comparison of groups of employees. For this reason, Workplace Analytics provides a means to improve the value of your comparisons: If any of the users that are being provided for analysis&mdash;either in the initial (highly effective) group or in the peers group&mdash;differ in a way that would render your analysis irrelevant, Workplace Analytics can inform you upfront how to avoid this roadblock. 

What we are providing here is a way to control for that. Let’s say we’re looking at people in the software engineering discipline. You now want to make sure that both groups consist entirely of software engineers. What you can do here is use a filter to establish a condition such as: _Discipline_ = _software engineer_. 

Workplace Analytics will then make sure that every user in all of the groups that you selected in the preceding steps (the example group and the peer groups) match this condition. If they do not, we show this error message:

![Use filters](../images/wpa/use/conditions-error-msg.png)
 
Note that, for privacy reasons, Workplace Analytics cannot inform you which user or users do not match the conditions. At this point, you select **Back** and return to the preceding steps to check the content of your groups, and make the necessary changes to eliminate this error.  
