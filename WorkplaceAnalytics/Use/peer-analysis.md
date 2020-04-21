---
# Metadata Sample
# required metadata

title: Peer analysis 
description: Describes the peer analysis functionality of Workplace Analytics
author: paul9955
ms.author: v-midehm
ms.date: 07/30/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
---

# Peer analysis

Peer analyses help you find answers to the question: How do the most effective people&mdash;the best performing people in a company&mdash;collaborate differently than their peers? (Note: In this article, we’ll refer to these people as the _reference group_, and the people we compare them with&mdash;their peers&mdash;as the _other group_.) 

The immediate goal of this kind of analysis is to help you discover the unique workplace-collaboration traits that help these people succeed. The larger goal is to use these insights to spread these behaviors so that the peers of the reference group, and others in the company, can benefit from them.  

You work towards the first goal through a peer analysis. This procedure consists of the following tasks:

1.	[Start an analysis](#start-an-analysis). 
2.	[Identify the reference group](#identify-the-reference-group). You do this either by using filters or by uploading a .csv file that contains the email addresses of the members of the group. 
3.	[Select the other group](#select-the-other-group). After you've identified the reference group, you next identify the other group for comparison. This, too, you can do either with filters or by uploading a .csv file. 
4.	(Optional) [Apply conditions](#apply-conditions). In this step, you help assure that your comparison makes sense for the groups that you’ve selected. 
5.	[Submit the analysis](#submit-the-analysis).
6.	[View results](#view-results). View the results of your analysis. 

### Roles 

To be able to perform the tasks in this article, you must have either the analyst or the limited analyst role of Workplace Analytics.  

### Privacy notes

Peer analyses enforce the [minimum group size](../privacy/privacy-considerations.md#minimum-group-size) settings for your organization. In other words, if the number of members on a team that you select is smaller than the minimum group size, the analysis is halted and cannot continue. This applies to both the reference group and the other group.

The results of analyses are always presented in aggregate form. No individual's data is ever presented in isolation.

## Start an analysis

In this task, you take the first steps to start a peer analysis. 

1. Open [Workplace Analytics](https://workplaceanalytics.office.com/). If prompted, enter your work credentials. 

2. Expand **Analyze** and open the **Explore** page. This page has two sections: **Metrics overview** and **Analyze and start Plans**.

3. Under **Analyze and start Plans**, select **Peer analysis**. 

   This displays a table of the peer analyses that have been started or completed. 
 
    ![New analysis](../images/wpa/use/explore-new-analysis-3.png)

4. Select **New analysis** to initiate a new analysis. This opens a panel for creating the new analysis: 

    ![New analysis panel](../images/wpa/use/step1-new-request.png)
 
    The top of this panel shows the four steps for creating a peer analysis: _Reference group_, _Other group_, _Conditions_, and _Submit_.

5. For **Analysis name**, type a name for this analysis.  

6. Select a date range for the analysis.

7. Go to [Identify the reference group](#identify-the-reference-group).

## Identify the reference group

> [!Tip] 
> Before you complete this task, you should know the group of people within your organization that you want to use for the reference group.

As you define this group, keep in mind that it has a maximum size. If you upload a .csv file, the group can contain no more than 150 members. If you use filters, the group can contain no more than 1000 members. 

1. In the **Reference group** section, identify the members of this group. This is a group of your choosing; its members need not work together on the same team. You can identify them in either of the following ways:

    * [Upload a .csv file](#upload-a-csv-file). For this, you’ll use a file that contains the email addresses of the people in the reference group.  
    * [Use filters](#use-filters). To do this, you filter by HR (organizational) attributes. 

    > [!Note] 
    > For more information about which way to identify this group, see [Why use filters?](#why-use-filters)

2. After you've successfully identified the reference group, select **Next** and go to [Select the other group](#select-the-other-group). 

## Select the other group

As you define this group, bear in mind that it has a maximum size. If you upload a .csv file, the group can contain no more than 150 members. If you use filters, the group can contain no more than 1000 members.   

![Identify other group](../images/wpa/use/step2-other-group.png)

1. In the **Other group** section, identify the members of the other group. As with the reference group, you choose the other group; its members need not work together on the same team. You can identify them in either of the following two ways:

    * [Upload a .csv file](#upload-a-csv-file). For this, you'll use a file that contains the email addresses of the people in the other group.  
    * [Use filters](#use-filters). To do this, you filter by HR (organizational) attributes. 

    > [!Note] 
    > For more information about which way to identify this group, see [Why use filters?](#why-use-filters)

2. After you've successfully identified the other group, select **Next** and go to [Apply conditions](#apply-conditions). 

## Apply conditions

In this optional step, you make sure that the right people in each of your selected groups are being compared. 

After you select **Next** in the **Other group** section, the **Conditions** page opens:
 
![New analysis panel](../images/wpa/use/step3-conditions.png)

On this page, you filter by organizational (HR) data. These filters automatically apply to each of the groups that you've defined in the preceding steps, namely the reference group and the other group. By applying filters in this step, you refine your selections of employees in those groups so that the analysis can make more appropriate comparisons. For more information, see [Why apply conditions?](#why-apply-conditions).

> [!Note] 
> You can skip this step by selecting **Next**. 

After you have finished applying conditions, select **Next** and go to [Submit the analysis](#submit-the-analysis). 

## Submit the analysis

The fourth and final screen of the sequence summarizes the choices that you've made by showing the analysis name, the date range, and the names and sizes of the reference and other groups. If you want to return to preceding steps to change any of these things, select **Back**:

![Summary page with Submit button](../images/wpa/use/step4-summary-edit.png) 

If you do not need to make changes, select **Submit**.

This opens the page that displays the **Peer analysis** table. The analysis that you just submitted appears at the top of the list with a status of _running_, as shown here: 

![Analysis running](../images/wpa/use/analysis-running.png)

Depending on the size of the analysis, the run time should take between several minutes and one hour. Go on to [View results](#view-results).

## View results

After your analysis completes, its status is updated in the **Peer analysis** table with a check mark. In the following illustration, the second and third analyses have completed:  

![Results with one row](../images/wpa/use/three-analyses.png)
 
You can do the following on this page.

 * <u>In the rows of analyses:</u>
   * Select **View** (eye) icon to open the results for an analysis.
   * Select **Delete** (trashcan) icon to delete an analysis that you no longer need.
   * Select the **Duplicate** (two-sheets-of-paper) icon to make an editable copy of the analysis.
 * <u>Above the table:</u> 
   * Select **New analysis** to create a new peer analysis.
   * Select **Update list** to refresh the list of analyses.

Selecting **View** opens the **Result** page:
 
![Result page](../images/wpa/use/result-1-2.png)

This page includes analysis details, such as: the analysis name, date range, name and size of the reference group, and the name and size of the other group.

The **Highlights** area displays the results of your analysis. The upper area presents summaries of the top three variant metrics for the groups. (Workplace Analytics selects these three metrics from among highly correlated metrics that are unique to this type of analysis.) The results that you see are comparisons of raw averages between the reference group and the other group. 

In this example, they are _Time with leadership_, _External network size_, and _Percentage of meeting hours with direct manager coattending_.
 
Below these metrics summaries, the results for each metric are described in detail. Each detail section contains a description called **Why it matters**. This section explains why this metric analysis result is useful. Each section also contains an information icon &mdash; &#x24D8; &mdash; that you can select to learn more about the metric.
 
Although the **Result** page is read-only, you can download it into an Excel workbook file that you can open in Microsoft Excel or share with others.

## Task details

### Upload a .csv file

Follow these steps to upload a file that contains email addresses: 

1. Create a .csv file that contains the email addresses of the people in the group. This file should contain no header, but consist of a single column, with each email address appearing on a new line.

2. Select **Upload .csv file**: 
 
    ![Upload .csv file](../images/wpa/use/upload-csv-file.png)

3. Browse to the file on disk and select **Open**. After the file uploads, Workplace Analytics automatically validates the uploaded data and displays the results:

    ![Validation results](../images/wpa/use/validation-results.png)
 
    In this example, the validation results contain the errors of invalid email addresses and a person who has no Workplace Analytics license. You can choose to fix these errors by correcting or deleting the invalid email addresses, or having an admin assign the missing license. (To participate, a person needs only a Workplace Analytics [license assigned](../setup/assign-licenses-to-population.md); they do not need a Workplace Analytics [role](../setup/assign-roles-to-wpa-admins.md).)

    If validation errors are found, you cannot proceed with the analysis. After you correct the validation errors (or select a group with other participants), you must re-upload the .csv file to cause Workplace Analytics to validate the file again. After your .csv file successfully validates, you can proceed with the analysis.

    <!-- REMOVE FOR NOW (PER SANJAY, WHO IS CHECKING ON THIS) Even if errors were found, you can proceed with the analysis if the group size meets or exceeds the minimum group size. In this example, the actual group size (25) exceeds the minimum group size (5), so you can start the analysis with this group. -->

    > [!Note] 
    > In addition to the [minimum group size](../privacy/privacy-considerations.md#minimum-group-size), a maximum group size is also in effect. The current maximum group size for peer analyses is 150 if you are uploading a .csv file to define the group, while the limit is 1000 members if you are using filters to define the group. 

4. Return to your current step, either [Identify the reference group](#identify-the-reference-group) or [Select the other group](#select-the-other-group).
 
### Use filters

1. To identify a group by filtering, select **Use filters**: 

    ![Use filters](../images/wpa/use/use-filters.png)
 
2. Add filters and parameters.

    In this step, you use organizational data in filters to refine your group selection. For example, in the left box, select **Organization** and in the right box, type an org name or a manager's identifier. Add more filters to refine the selection further, if you want. The results of filtering are shown in a chart. You can then select groups by clicking the columns that represent them in the chart. You can select multiple groups. 

    For more information about what happens with selected groups when you make other settings on this page, see [Persistence of group selections](../tutorials/solutionsv2-conceptual.md#persistence-of-group-selections). 

    Now, you could proceed with the analysis if the group size falls between the allowed minimum and maximum group sizes. In this example, the actual group size (25) exceeds the minimum group size (five is the default, but it might be set to a higher number for your organization). 

    > [!Note] 
    > In addition to the [minimum group size](../privacy/privacy-considerations.md#minimum-group-size), a maximum group size is also in effect. The current maximum group size for peer analyses is 150 if you are uploading a .csv file to define the group, while the limit is 1000 members if you are using filters to define the group. 

3. Return to your current step, either [Identify the reference group](#identify-the-reference-group) or [Select the other group](#select-the-other-group).  

## Concepts

### Why use filters?

A typical use case for using filters would be if your organization uses outcome metrics such as sales quotas or performance or engagement ratings. If your admin has uploaded this data, you can use corresponding filters in this type of analysis. For example, while defining your reference group, you could filter to include employees who have achieved a particular sales quota or above. Then, one of your filters for the other group could specify sales quota below the level that you chose for the reference group. 

Of course, if performance metrics cannot be or have not been uploaded for your organization, you cannot filter by them to select a group. In this case, remember that you can designate a group by uploading its members in a .csv file that contains email addresses. 

### Why apply conditions? 

When you compare two groups of people, the purpose is to arrive at a meaningful comparison. For example, depending on your organization, it might not make sense to compare IT admins with software engineers. Their roles are different and so are the ways they are rated in performance evaluations and the expectations of how they interact with customers. 

Because of differences such as these, making a direct, unrefined comparison of groups of employees might produce results that are not informative. For this reason, Workplace Analytics provides a way to improve the relevance and value of your comparisons: Add filters on the **Conditions** page:

![Apply conditions](../images/wpa/use/step3-conditions.png)

Let's say you are looking at employees in the software engineering discipline. You might want to make sure that both the reference group and the other group consist entirely of software engineers. On this page, add a filter to define a condition such as: _Discipline_ _Equals_ _Software engineer_. 

Workplace Analytics will then make sure that every user in both of the groups that you selected in the preceding steps (the example group and the peer group) match this condition. If they do not, it displays an error message:

![Use filters](../images/wpa/use/conditions-error-msg.png)
 
For privacy reasons, Workplace Analytics cannot inform you which user or users do not match the conditions. At this point, you'll need to select **Back** to return to the preceding steps and check the content of your groups, and make the necessary changes to eliminate this error.  
