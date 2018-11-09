---
# Metadata Sample
# required metadata

title: Meeting exclusion rules (concepts)
description: Meeting exclusion rules -- Concepts   
author: paul9955
ms.author: v-pascha
ms.date: 11/06/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Meeting exclusion rules: Tools and concepts

This article describes screen elements and concepts whose understanding can help you create and use meeting exclusion rules. Those tasks are described in the step-by-step walkthroughs in [Exclude meetings from analysis](meeting-exclusion-rules.md).

## Progress summaries  

At each step in the exclusion-creation flow, you see a page such as the following: 

![Interactive tools](../images/wpa/tutorials/08-interactive-tools.png)
 
On these pages, the following sections help you create meeting exclusions in an informed way:

### Progress bar

The progress bar at the top of the page track the step in the flow that you are currently on: 

![Progress bar](../images/wpa/tutorials/12-progress-bar.png)

### Summary of meetings that remain

This area at the top of the page tracks how many meetings and meeting hours remain in your analysis as you exclude meetings. This view updates every time you advance to the next step in the flow. 

These numbers help you understand the effects of the exclusions that are already in place and the effect of the exclusion created in the current step. This helps you confirm whether to remove these meetings and decide which meetings, if any, that you want to keep in your analysis. 

Before you apply any filters, 100% of meeting hours are still available for analysis, as are 100% of the meetings that have been held in the time since Workplace Analytics began to use data from Office 365.

![Meeting hours summary (before)](../images/wpa/tutorials/09-summary-meetings-hours.png)

As the [Create a meeting exclusion rule](meeting-exclusion-rules.md) walkthrough describes, you create a meeting exclusion rule in five steps. As you complete one of those steps and move on (by selecting **Next**), you see the number of meeting hours and meetings decrease as the exclusion is applied to your data: 

![Meeting hours summary (after)](../images/wpa/tutorials/10-summary-meetings-hours-remain.png)

## Customization working area

Below the **Summary of meetings that remain**, you can customize four of the five exclusion types: appointments, large meetings, long meetings, and meetings by topic. (The first exclusion type, cancelled meetings, cannot be customized.) 

>[!Note] 
> When you first add an exclusion to your rule, the exclusion removes an entire class of meetings (such as long ones) from analysis. _Customizing_ an exclusion means to selectively remove meetings from the exclusion, which _returns_ those selected meetings _to_ analysis. 

You make customizations on the following page areas:

 * The [Interactive summary of the current exclusion step](#interactive-summary-of-the-current-exclusion-step) appears in the middle of the page. 
 * The **Identify exceptions** area is the bottom part of the page. It presents a [Word cloud](#word-cloud), a [Phrase table](#phrase-table), and search capability ([Keyword search](#keyword-search)) that you use to remove phrases from the exclusion that you are defining. 

### Interactive summary of the current exclusion step

The middle section of the page shows you a summary of the current exclusion step:

![Middle of page](../images/wpa/tutorials/11-mid-page.png)

This area has three informative areas: 
 
 * On the left, you see what kinds of meetings this step addresses. The exclusion description helps you understand the purpose of the current step.
 * In the center, you see details about the meetings that this exclusion would remove from analysis. This section helps you keep track of the customizations you have made to the current exclusion. <!-- 
 ![Customizations](../images/wpa/tutorials/04-exclude-meetings-where.png)
 -->
 * On the right, you see the effects of the current exclusion step if you apply it, namely: What percentage of meeting hours and of meetings would it exclude? In other words, what impact would this step have on the remaining meeting data?
  
   >[!Tip] 
   >Pay particular attention to the number shown for _Excluded meeting hours_. This metric is usually more important than the percentage of meetings because time spent in meetings is a more important indicator when analyzing meeting behavior than the sheer number of meetings, which can vary greatly in length. 

### Word cloud

Below the heading **Identify exceptions** is a word cloud that displays keywords from meeting subject lines. It includes only keywords for meetings that meet the filter criteria that are being applied on the current step. In a word cloud, the larger the size of text of a keyword, the more meeting hours the keyword represents.

The filter context of the word cloud always reflects the filter context for the step that you are on. For example, in the _Exclude small meetings_ step, the keywords were found in the invitations where the number of attendees is less than or equal to one. 

While you define the exclusion, if you adjust that filter context, the word cloud is re-filtered accordingly. 

To remove a keyword from this exclusion, select the keyword in the word cloud and then click **Make an exception**. Before you remove it, you might want to learn more about it and its impact on the data. To learn more, do one of the following: 
 * Hover over the keyword. This displays a text box that shows meeting hours and meeting count.
 * Click the keyword. This selects the keyword and displays details about its impact on meeting hours in the Phrase table. The Phrase table is described later in this step.

### Keyword search

You might have a specific word in mind that you want to retain in your analysis (that is, remove from the exclusion). If cannot find that word in the word cloud, search for it in the field marked **Search for a keyword**. You can search for phrases that contain one, two, or three words. If the keyword is found, Workplace Analytics display data in the Phrase table about removing this keyword from the exclusion. To remove it from the exclusion, click **Make an exception**. 

#### Remove an exception

After you make an exception of a word, it appears above the word cloud. If you change your mind, you can remove the word from the exception list. This returns it to the group of keywords whose meetings will be excluded. To do this, click the 'X' next to the word: 
 
![Exclude meetings where](../images/wpa/tutorials/04-exclude-meetings-where.png)
 
You can also remove all of your exceptions to this exclusion at once. To do this, select **Reset**. 

### Phrase table

Workplace Analytics shows a table called **Phrases that contain the selected keyword**. Through this table, you can better understand the context of the meetings that are associated with this keyword or subject-line phrase. 

### Example 1: "business"

The words "business" or "marketing" in the word cloud represent meetings that you might not want to exclude. To help you decide, you can view data about the effect of removing this keyword (and its meetings) from the exclusion. For example, select **business**. Workplace Analytics shows what percentage of meetings have this word in their subject line and how many hours those meetings contain:

![Percentages](../images/wpa/tutorials/02-word-cloud-business.png)

In the following illustration, the word "business" has been excepted from the exclusion, which means that meetings with "business" in their invitations' subject lines will be _retained_ in your analysis: 

![Selected keyword](../images/wpa/tutorials/03-selected-keyword.png)
 
### Example 2: "soccer"

The word cloud contains the word "soccer," which you select. Now, if the Phrase table shows phrases such as "soccer practice" or "soccer league," this might indicate that the meetings with "soccer" in the subject line were not work-related and therefore are appropriate to exclude from analysis. 

However, if you work for an athletic-equipment supplier and this table displays phrases such as "soccer product review," these meetings are probably work related and you do not want to exclude them. To retain such a keyword and its associated meetings, you make it an exception to the exclusion rule. To do this, select the **Make an exception** check box adjacent to the word cloud. 
 
If you notice other words in the cloud that you might want to retain in your analysis, click them, review the **Phrases that contain the selected keyword** table, and, when appropriate, select **Make an exception**. 

## Application of meeting-exclusion rules 

Workplace Analytics provides a default meeting-exclusion rule. You and other analysts can create new rules. Are all these rules available to all analysts? Can you combine your rules with theirs, or with the default rule? This section answers those questions and others. 

Q1. **Scope of meeting-exclusion rules.** You create meeting-exclusion rules on the Meeting exclusions page, which is reached through the Queries page of Workplace Analytics. After you create rules, where in Workplace Analytics are they applied?

A1.  Exclusion rules apply in two areas where analysts work: 

 * **Explore page dashboards.** Exclusion rules work for analysts as they inspect data on the dashboards of the Workplace Analytics Explore page. For information about selecting the rule that you want to take effect, see [Explore page](#explore-page).
 * **Queries.** Creating, refining, and running queries on the query-creation pages that are reached through the Workplace Analytics Queries page. For information about selecting the rule that you want to take effect, see [Queries page](#queries-page).

Q1. **Editing existing rules.** Can you change/edit the default meeting-exclusion rule, or rules that other analysts have created, or rules that you created previously? 

Q2.  No. You cannot change or delete existing rules, regardless of their origin.

Q3. **Sharing rules.** Can rules be viewed and shared by others? If you create one, does it or can it be applied to the data and queries that are used by other analysts? 

A3.  Yes. Anyone in your organization can use the rules that anyone else in the organization has created.

Q4. **Combining rules.** Can you combine rules? For example, can you use the default meeting-exclusion rule and then layer a new rule atop it, so that both are in effect? Can you combine a rule of your own with a rule that another analyst has defined?

A4.  No. You can have only one rule in effect at a time. For information about selecting the rule that you want to use, see [Select a rule](#select-a-rule).

