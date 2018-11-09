---
# Metadata Sample
# required metadata

title: Meeting exclusion rules in Workplace Analytics
description: Meeting exclusion rules -- Introduction and walkthrough   
author: paul9955
ms.author: v-pascha
ms.date: 11/05/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Meeting exclusion rules: Walkthroughs

This article describes three ways to work with meeting exclusion rules:
 * [View meeting exclusion rules](#view-meeting-exclusion-rules): Become acquainted with the default rule and with the rules that you or others have published.
 * [Create a meeting exclusion rule](#create-a-meeting-exclusion-rule): Define up to five individual meeting exclusions and then publish them together as a meeting exclusion rule.
 * [Select a rule for use](#select-a-rule-for-use): Select a rule to apply to the **Explore** page or to the **Queries** page of Workplace Analytics.

### For more information

The [Tools and concepts](meeting-exclusion-concept.md) article provides deeper information about screen areas, tools, and ideas that can help you work with meeting exclusion rules. It contains the following sections:

 * [Progress summaries](meeting-exclusion-concept.md#progress-summaries): The upper parts of the meeting exclusion pages display your progress, including which step you are on and the effects of the current and the completed meeting exclusion steps.  
 * [Customization working area](meeting-exclusion-concept.md#customization-working-area): This section describes on-screen tools that you can use to define effective meeting exclusions, including the following:
   * [Word cloud](meeting-exclusion-concept.md#word-cloud): The word cloud consists of keywords taken from subject lines of meetings. Use it to remove a keyword from the exclusion. 
   * [Keyword search](meeting-exclusion-concept.md#keyword-search): To find a particular keyword that you want to remove from exclusion, type it in the keyword search field.  
   * [Phrase table](meeting-exclusion-concept.md#phrase-table): The phrase table shows you the context in which keywords are found. Knowing this context helps you decide whether to retain or exclude the keyword and its associated meetings. 
 * Multiple meeting exclusion rules can exist simultaneously. To learn how they are applied in Workplace Analytics, see [Application of meeting exclusion rules](meeting-exclusion-concept.md#application-of-meeting-exclusion-rules). 

For a high-level overview of meeting exclusion rules, see [Meeting exclusion rules in Workplace Analytics](meeting-exclusions-intro.md).

<!-- _[PUT VIDEO HERE]_ -->

## View meeting exclusion rules

This section describes how to view existing meeting exclusion rules. The section that follows describes how to author a new one. 

**To view existing meeting exclusion rules**

Open the Meeting exclusions page to view existing meeting exclusion rules or to create new ones. 

1. Open [Workplace  Analytics](https://workplaceanalytics.office.com/). If  prompted, enter your Microsoft credentials. 

2. Click **Queries** and then select the tab called **Meeting exclusions**. This opens the Meeting exclusions page. The page displays all meeting-exclusion rules that already exist: 

   * **System default:** Workplace Analytics supplies one meeting exclusion rule by default called **Default meeting exclusion rule**. This rule filters out meetings that are longer than 8 hours or whose number of attendees is 1 or fewer or 50 or more. This default rule is a good start, but if you were to use only it, you would miss the opportunity to verify that this rule didn't exclude any important meetings you wanted to keep, as well as the opportunity to exclude additional meetings based on meeting-subject keywords. 
   * **Your rules:** Rules that you have created.
   * **Others' rules:** Rules that other analysts have created.

>[!Note]
>Remember that you cannot edit any published meeting exclusion rules.

## Create a meeting exclusion rule

A meeting exclusion rule is a filter applied to your meeting data. 

Defining what kind of meeting exclusion to use is part of the data-preparation work that an analyst must do before they start working with Workplace Analytics data. You can create these rules only after you've uploaded your organizational data. 

When you start a new meeting exclusion rule and before you have added any exclusions to it, the set of meetings that will be analyzed includes 100% of the meetings that were found in the Outlook mailboxes of licensed employees who use Office 365. As you add filter terms, or exclusions, to this exclusion rule, you gradually reduce the number of meetings and meeting hours that will be used in metrics calculations while performing analysis in Workplace Analytics.  

### Walkthrough: to add a meeting exclusion rule

Workplace Analytics guides you step-by-step through the creation of a customized meeting exclusion rule. The meeting exclusion flow, which is described in the second task that follows, contains five steps, one for each meeting type that is commonly excluded from analysis.

**To start a meeting exclusion rule**

In this task, you open the meeting exclusions page and name the rule that you will create. 

1. Open [Workplace Analytics](https://workplaceanalytics.office.com/). If prompted, enter your organization credentials. 

2. Click **Queries** and then **Meeting exclusions**.

3. On the right side of the page, click **Add exclusion**. This opens the **Queries &gt; Meeting exclusions &gt; New meeting exclusion** page. This page displays a preview of the five types of meetings that are commonly excluded from analysis. In the steps that follow, you will have the chance to customize each of these exclusions. 

   You can choose to use the system-suggested exclusion on each step or customize the exclusion by retaining or excluding additional meetings. If you don't want to use a system-suggested exclusion, you can always choose not to apply the exclusion. After you have customized exclusions for each of the five steps, you can make edits to your exclusion rule before publishing it for future use. 

   ![Five exclusion steps](../images/wpa/tutorials/01-five-exclusion-steps.png) 

4. Type a name for the  exclusion rule and, optionally, a description. Select **Next**. This starts the flow of steps in which you author your new exclusion rule by defining individual exclusions. Move on to the next task, **To create a meeting exclusion rule**.

**To create a meeting exclusion rule**

Now that you've created a framework for your new rule, you add -- and optionally, customize -- individual exclusions, as described in the following steps.

   >[!Note] 
   >You complete the following steps by selecting **Next**. It's possible to forego adding the exclusion that the current step defines. To do this, clear the **Use this exclusion** check box before you click **Next**:

   ![Skip this exclusion](../images/wpa/tutorials/18-use-this-exclusion.png)

   >[!Caution] 
   > * While you are authoring an exclusion rule (at any time before you select **Publish**), _do not_ close your browser. Any work you've done to create a rule would be lost if you close the browser. 

1. **Step 1: Exclude cancelled meetings.** The first page in the flow is for excluding meetings that have been cancelled. On this page, you cannot change the default filter. Add this exclusion to your rule by clicking **Next**. Workplace Analytics displays the next page in the flow, the page for excluding small meetings.

2. **Step 2: Exclude small meetings.** Just as on the cancelled-meetings page, you cannot change the default filter for this exclusion. However, you can change the way it is applied by specifying exceptions to the exclusion. You do this on the following parts of the page: [Word cloud](meeting-exclusion-concept.md#word-cloud), [Keyword search](meeting-exclusion-concept.md#keyword-search), [Phrase table](meeting-exclusion-concept.md#phrase-table).

   When you have finished making exceptions to the small-meetings exclusion and you are ready to add the exclusion to the rule, click **Next**. Workplace Analytics displays the next step in the flow, the page for excluding large meetings. Notice that the values that are shown near the top of the page for Attendee meeting hours and Number of meetings have been lowered as a result of the exclusions that we've applied earlier in the last two pages.

3. **Step 3: Exclude large meetings.** This exclusion differs from the first two in that you can change the value in the "Exclude meetings where" filter from the default value of 250 attendees. 

   (Optional) Select words from the word cloud, inspect their impact in the **Phrases that contain the selected keyword** table, and designate one or more as exceptions to this exclusion. You can search for additional keywords or phrases that are not present in your word cloud by typing them in the search box above the phrase table.

    >[!Note] 
    > If you change the default filter value after you designate exceptions, the exceptions will be lost. 

    When you have finished making exceptions, click **Apply**.

4. **Step 4: Exclude long meetings.** To exclude meetings by duration, under **Exclude meetings where,** specify the maximum length of meetings that you want your analysis to include. The default value is 8 hours. 

   (Optional) Select words from the word cloud, inspect their impact in the **Phrases that contain the selected keyword** table, and designate one or more as exceptions to this exclusion.  You can search for additional keywords or phrases that are not present in your word cloud by typing them in the search box above the phrase table.

   >[!Note] 
   > If you change the default filter value after you designate exceptions, the exceptions will be lost. 
         
   When you have finished making exceptions, click **Next**.

5. **Page 5: Exclude meetings by topic.** On this page, you use the subject lines of meetings to identify and exclude meetings that are not work related. The left side of the page lists several categories of common keywords, grouped by topic, that you can select for exclusion. 
Workplace Analytics also preselects some topics for you. For example, in the following illustration, **Administrative**, **Medical**, and **Out of Office** are selected for exclusion:

     ![Select topics to exclude](../images/wpa/tutorials/05-select-topics-to-exclude.png)
 
     Each topic that is listed under **List of topics** is also a tab. On an open tab, you can see keywords and phrases that relate to the topic. For example, the **Out of Office** tab contains the phrase "day off." These keywords are excluded from analysis. Click the ‘X' of a keyword to delete it from this list. This exempts the keyword from exclusion; in other words, meetings whose subject line contains this keyword are removed from the exclusion and, therefore, available for analysis. 

     You might have a specific word or phrase in mind that you want to exclude from analysis; that is, to add to this exclusion. If it is not listed under Keywords, search for it by typing it in the **Add a custom keyword** field. See [Keyword search](meeting-exclusion-concept.md#keyword-search).   

     This meetings-by-topic page also offers the **Phrases that contain the selected keyword** table and the functionality described in the step for creating a small-meetings exclusion. 

     Select **Next**. Workplace Analytics now calculates your new meeting-exclusion rule. This could take up to a few minutes.  
 
     After the calculation is finished, Workplace Analytics displays a cumulative summary of the exclusions that you defined on the five preceding steps. This summary explains the effect of your new rule, in particular, the percentages of original meeting hours and of meetings that remain to be analyzed:

     ![Rule summary overview](../images/wpa/tutorials/06-rule-summary-end.png)
 
     The summary lists which exclusions were applied, which ones were not applied, and the effects that each exclusion has. It also shows the cumulative impact of all exclusions on the meetings that remain in analysis. The table of rules shows the individual impact of each rule, so the total will likely not add up to 100%:

     ![Rule summary](../images/wpa/tutorials/07-summary-of-five.png)
 
6.  **Review and edit the rule.** Examine this list of exclusions to make sure they retain the meetings that you want to keep in your analysis and exclude the ones that you want to exclude. If you want to change the settings of an exclusion, select the edit (pencil) icon to re-open that exclusion, and then edit its details. For example, you could re-open the long-meetings exclusion to change the threshold from 8 hours to 6. 

     **Reminder:** While making edits to an exclusion, if you change the default filter value after you designate exceptions, the exceptions will be lost. 

7.  **Publish the rule.** After you have finished editing, select **Apply**. Workplace Analytics re-calculates the meeting-exclusion rule. After it finishes, if you have no more edits, scroll to the bottom of the summary page and select **Publish**. 

     >[!Important] 
     > * Your exclusion rule is not saved by default. It is saved only after you select **Publish**.
     > * After you select **Publish**, you can no longer edit the exclusion rule. 

After Workplace Analytics publishes your new rule, it displays a read-only summary of the rule's exclusions. 

## Select a rule for use

You can have one rule in effect at a time. To select a rule for use on the **Explore** page dashboards, see [Use rules in the Explore dashboards](#use-rules-in-the-explore-dashboards). For the rule to be used in a query, see [Use rules with queries](#use-rules-with-queries).

### Use rules in the Explore dashboards

By default, the dashboards of the **Explore** page use the default meeting-exclusion rule that Workplace Analytics supplies, but you can change this to a different rule. The rule that will be used in the dashboards is known as the _preferred rule_, whether this is the default rule or a different rule that you've selected. 

**To apply a rule to the Explore dashboards**

1.  In Workplace Analytics, open the **Queries** page.

2.  Select **Meeting exclusions**.

3.  In the list of rules, hover over the row of the rule you want to make the preferred rule. The words **Set preferred** appear, as shown here:

   ![Select an exclusion rule](../images/wpa/tutorials/19-choose-a-rule.png)
 
4.  Select **Set preferred**.

>[!Note] 
>If you select a new rule, the selection does not take effect until after the next time that your organization's Office 365 data is refreshed. The reason for this delay is that meeting-exclusion rules are applied to data before it is processed; after the data is uploaded and processed, rules can no longer be applied to it. Office 365 data is refreshed weekly, so it could take up to two weeks to see your rule in place, depending on the timing of your rule selection. 

### Use rules with queries

You can apply a meeting-exclusion rule to a query while you define the query.

<!-- GET THIS ANSWERED! 
HOW CAN A RULE BE SET AS PREFERRED ON THE MEETING EXCLUSIONS PAGE? -->

>[!Note] 
>If you selected a rule as the preferred rule on the Meeting exclusions page, the rule that you selected also becomes your default rule when you work on the **Queries** page.
 
**To apply a rule to a query**

1.  In Workplace Analytics, open the **Queries** page.

2.  Select the rule you want from the Meeting exclusions list box, as shown here:

   ![Apply an exclusion to a query](../images/wpa/tutorials/20-apply-to-query.png)
