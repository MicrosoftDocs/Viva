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

# Meeting exclusion rules: Concepts

This section describes concepts whose understanding could help you complete tasks related to creating and using meeting exclusion rules. Those tasks are described in the step-by-step walkthrough for creating a rule, [Exclude meetings from analysis](meeting-exclusion-rules.md).

<!-- ??? Where did these sections come from? ??? -->
## Interactive tools for creating meeting exclusions 

At each step in the exclusion-creation flow, you see a page such as the following: 

![Interactive tools](../images/wpa/tutorials/08-interactive-tools.png)
 
On these pages, the following sections help you create meeting exclusions in an informed way:

### Progress bar

The progress bar at the top of the page track the step in the flow that you are currently on: 

![Progress bar](../images/wpa/tutorials/12-progress-bar.png)

### Summary of meetings that remain

This area at the top of the page tracks how many meetings and meeting hours remain in your analysis as you exclude meetings. This view updates every time you advance to the next step in the flow. 

Before you apply any filters, 100% of meeting hours are still available for analysis, as are 100% of the meetings that have been held in the time since Workplace Analytics began to use data from Office 365.

![Meeting hours summary (before)](../images/wpa/tutorials/09-summary-meetings-hours.png)

In a step, after you choose to use an exclusion and select **Next**, you see the number of meeting hours and meetings drop as the exclusion is applied to your data: 

![Meeting hours summary (after)](../images/wpa/tutorials/10-summary-meetings-hours-remain.png)

### Summary of the current exclusion step



The middle section of the page shows you a summary of the current exclusion step.

![Middle of page](../images/wpa/tutorials/11-mid-page.png)
 
 * On the left, you see what kinds of meetings this step addresses. The exclusion description helps you understand the purpose of the current step.
 * In the center, you see details about the meetings that this exclusion would remove from analysis. This section helps you keep track of the customizations you have made to the current exclusion. <!-- 
 ![Customizations](../images/wpa/tutorials/04-exclude-meetings-where.png)
 -->
 * The section on the right displays the effects of the current exclusion step if you were to apply it, namely: what percentage of meeting hours and of meetings would it exclude? In other words, what impact would this step have on the remaining meeting data?
  
   >[!Tip] 
   >Pay particular attention to the number shown for _Excluded meeting hours_. This metric is usually more important than the percentage of meetings because time spent in meetings is a more important indicator when analyzing meeting behavior than the sheer number of meetings, which can vary greatly in length. 

### Customization working area

On the bottom part of the page, you customize exclusions for appointments, large meetings, long meetings, and meetings by topic. This section is not available for the cancelled meetings step.

### Customization UI for appointments, large meetings, and long meetings

[What is this section?]

### Customization UI for meetings by topic

>[!Note] 
> At each stage in this flow, Workplace Analytics displays a summary that presents two sets of numbers. These numbers help you understand the effects of the exclusions that are already in place and of the exclusion that you can introduce in the current step. These displays help you confirm whether to remove these meetings and decide which meetings, if any, that you want to keep in your analysis. 

 * **Summary of meetings that remain.** An area at the top of the page displays a summary of the meetings that remain for analysis after Workplace Analytics applies the rule's current filters. For example, before you apply any filters, 100% of meeting hours are still available for analysis, as are 100% of the meetings that have been held in the time since Workplace Analytics began to use data from Office 365.
 
 * **Potential impact of exclusion.** An area below the middle of the page displays the effects of the current exclusion step if you were to apply it, namely: what percentage of meeting hours and of meetings would it exclude? In other words, what impact would this step have on the remaining meeting data? 

   ![Potential impact of this exclusion](../images/wpa/tutorials/17-potential-impact.png)

  * **Word cloud and phrase table.** In three of the four steps, you can use a word cloud and a phrase table to select phrases to remove from the exclusion that you are defining. For more information, see the descriptions under **Step 2: Exclude small meetings**.

>[!Tip] 
>Pay particular attention to the number shown for _Excluded meeting hours_. This metric is usually more important than the percentage of meetings because time spent in meetings is a more important indicator when analyzing meeting behavior than the sheer number of meetings, which can vary greatly in length. 

>[!Note] 
>You complete the following steps by selecting **Next**. It's possible to forego adding the exclusion that the current step defines. To do this, clear the **Use this exclusion** check box before you click **Next**:

  ![Skip this exclusion](../images/wpa/tutorials/18-use-this-exclusion.png)

<!--
#### Excluding meetings by keywords and topics
-->

# Customizing rules with the word cloud and phrase table 

## Word cloud
Below the heading **Identify exceptions** is a word cloud that displays keywords from meeting subject lines. It includes only keywords for meetings that meet the filter criteria that are being applied on the current step. In a word cloud, the larger the size of text of a keyword, the more meeting hours the keyword represents.

In this step (_Exclude small meetings_), these keywords in the word cloud are taken from the subject lines of meeting invitations where the number of attendees is less than or equal to one. The filter context of the word cloud always reflects the filter context for the step that you are on. If you adjust that filter context, the word cloud is re-filtered accordingly. 

To remove a keyword from this exclusion, select the keyword in the word cloud and then click **Make an exception**. Before you remove it, you might want to learn more about it and its impact on the data. To learn more, do one of the following: 
 * Hover over the keyword. This displays a text box that shows meeting hours and meeting count.
 * Click the keyword. This selects the keyword and displays details about its impact on meeting hours in the Phrase table. The Phrase table is described later in this step.

## Keyword search
You might have a specific word in mind that you want to retain in your analysis (that is, remove from the exclusion). If cannot find that word in the word cloud, search for it in the field marked **Search for a keyword**. You can search for phrases that contain one, two, or three words. If the keyword is found, Workplace Analytics display data in the Phrase table about removing this keyword from the exclusion. To remove it from the exclusion, click **Make an exception**. 

## Phrase table
Workplace Analytics shows a table called **Phrases that contain the selected keyword**. Through this table, you can better understand the context of the meetings that are associated with this keyword or subject-line phrase. 

### Example 1
The words "business" or "marketing" in the word cloud represent meetings that you might not want to exclude. To help you decide, you can view data about the effect of removing this keyword (and its meetings) from the exclusion. For example, select **business**. Workplace Analytics shows what percentage of meetings have this word in their subject line and how many hours those meetings contain:

![Percentages](../images/wpa/tutorials/02-word-cloud-business.png)
 
### Example 2
The word cloud contains the word "soccer," which you select. Now, if the Phrase table shows phrases such as "soccer practice" or "soccer league," this might indicate that the meetings with "soccer" in the subject line were not work-related and therefore are appropriate to exclude from analysis. 

However, if you work for an athletic-equipment supplier and this table displays phrases such as "soccer product review," these meetings are probably work related and you do not want to exclude them. To retain such a keyword and its associated meetings, you make it an exception to the exclusion rule. To do this, select the **Make an exception** check box adjacent to the word cloud. 

In the following illustration, the word "business" has been excepted from the exclusion, which means that meetings with "business" in their invitations' subject lines will be _retained_ in your analysis: 

![Selected keyword](../images/wpa/tutorials/03-selected-keyword.png)
 
If you notice other words in the cloud that you might want to retain in your analysis, click them, review the **Phrases that contain the selected keyword** table, and, when appropriate, select **Make an exception**. 

>[!Note] 
>After you make an exception of a word, it appears above the word cloud. If you change your mind, you can remove the word from the exception list. This returns it to the group of keywords whose meetings will be excluded. To do this, click the 'X' next to the word: 
   ![Exclude meetings where](../images/wpa/tutorials/04-exclude-meetings-where.png)
 
>[!Tip] 
> You can also remove all of your exceptions to this exclusion at once. To do this, select **Reset**. 

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

