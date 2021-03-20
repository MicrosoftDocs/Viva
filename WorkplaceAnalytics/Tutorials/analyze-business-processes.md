---

title: Analyze business processes 
description: Analyze business processes -- Introduction and walkthrough   
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: wpa
manager: scott.ruble

---

# Analyze business processes

When you and your co-workers perform an organized series of steps to reach a goal, you've participated in a business process. For example, your organization's hiring process might consist of obtaining leads, screening candidates, conducting interviews, making an offer, and sending new hires to HR for onboarding. Later business processes might have goals of training or coaching.

You can improve your business processes by analyzing them; for example, by measuring their cost &ndash; in time and money. For example, your business might conduct an information-security audit from time to time. Your CFO or CIO might want to know whether too little, too much, or just the right amount of time is being spent on these audits, and whether the right roles of employees are participating in them.

To make these determinations, conduct an analysis by running a Workplace Analytics query in which you designate the business process (in this case, auditing) as a [metric filter](../use/metric-filters.md) for the query. <!-- *** CALL THESE NEW FILTERS OUT IN THAT TOPIC *** --> To improve the query's accuracy, you first define a _data set_ to limit the data that the query examines.

Here are the procedures to follow to analyze a business process:

1. [Define a data set](#define-a-data-set) &ndash; Make sure that you're analyzing only data that is relevant in every aspect, such as organizationally and geographically.

2. [Define a business process](#define-a-business-process) &ndash; Define the business process that you want to analyze.

3. [Analyze a business process](#analyze-a-business-process) &ndash; Compose and run a Workplace Analytics query in which you select the data set and business process as parameters.
 
This illustration shows these procedures and the types of data that they involve: 

![Add a Meeting filter](../images/wpa/tutorials/steps-2-70.png)

The following sections describe these procedures.

> [!Note]
> After you define a data set, it becomes available to all other analysts in your partition. Similarly, after you define a business process, it also becomes available to all other analysts in your partition.

## Define a data set

Before you define a business process, you need to select the data set that's applicable to that process. For example, your company might have a global footprint, but you want to analyze only the processes of one subsidiary. You limit the data set for your query by filtering out organizational data that does not apply &ndash; for example, data from subsidiaries in other locations.

To define a data set, use the following procedure:

### Data set steps

**Role:** Analyst

Every business process that you create must be based on a data set. For that reason, creating at least one data set is mandatory before you can proceed to [Define a business process](#define-a-business-process). 

In this example, we restrict the analysis data to meetings of a particular length that took place in a particular city.

1. In Workplace Analytics, on the left navigation pane, expand **Settings** and select **Analysis settings**.

1. On the **Analysis settings** page, select **Data sets** and then, on the right side of the page, select **Add data set**.

1. On the **New data set** page, type a name and, optionally, a description for your new data set. (In this example, we'll give **Bangalore** as the name of the data set.) Select **Continue**.

1. Under **Time period** select start and end dates. All meetings that took place outside of this time period will be excluded from the data set.

1. Under **Meeting exclusions**, specify a [meeting exclusion rule](meeting-exclusions-intro.md) or accept the default, the [Tenant default meeting exclusion rule](meeting-exclusion-concept.md#default-meeting-exclusion-rule).

1. Under **Which meetings do you want to include in your query results?**, define filters to scope the data set to the business-process analysis that you want to perform. You'll use these filters to filter out meetings. Select **Add filter**.

1. Select **Meeting**:

   ![Add a Meeting filter](../images/wpa/tutorials/meeting-filter-1.png)

1. In the boxes to the right of **Meeting's**, select **Duration (in hours)**, **<** (less than), and **30** minutes.

1. On the next line, select **Organizer**. This lets us choose a geographic location for the meetings.

   ![Add an Organizer filter](../images/wpa/tutorials/organizer.png)

1. In the boxes to the right of **Organizer's**, select **city**, **Equals**, and **Bangalore**. (The choices that are available are determined by the [organizational data](../setup/prepare-organizational-data.md) that the Workplace Analytics admin has uploaded.)

1. Select **Submit**.

   This starts the creation of a data set that will contain data that matches these criteria (and no other data). The time required to process the data set depends on its size.

### Data set statuses

Right after you select **Submit**, the data set has a status of "In progress"; after it is created, its status changes to "Ready" and you can use it in business-definition processes and analyses. If data-set creation fails, the data set obtains "Failed" status. (If a data set that you've submitted shows "Failed" status, you can request help by [contacting Workplace Analytics support](../overview/getting-support.md).)

You can find a list of existing data sets and their statuses on the **Analysis settings** > **Data sets** page of Workplace Analytics:

![Data sets page](../images/wpa/tutorials/data-set-statuses.png)

### Data set actions

After a data set has been created, it can be viewed, used, or deleted, but it cannot be edited. A dataset can be deleted only if no business processes are using it. After you delete a data set, it cannot be recovered.

To view or delete a data set, first find it on the **Analysis settings** > **Data sets** page of Workplace Analytics.

## Define a business process

Before you can run queries to analyze a business process within your organization, you need to define it. You define a business process by selecting meetings in which people contributed to the furtherance of the process. This set of selected meetings provides the data that constitutes the business-process filter. Meetings are selected on the **New business process** page in the **Analyze** area of Workplace Analytics:  

![Biz process start page](../images/wpa/tutorials/start-page.png)

To select meetings, you assemble a list of keywords that match words in the subject lines of meetings in your data set. The set of keywords determines which meetings constitute the business process.

>[!Note]
>Currently, you can use only English keywords in the process of defining a business process. This holds true even if your instance of Workplace Analytics is in a language other than English.

### Business process steps

In this example, we want to examine the hiring process that's in place in the Bangalore subsidiary. To make sure that the data we use is restricted to the correct geographic area, we'll use the "Bangalore" data set that we defined in [Data set steps](#data-set-steps).

We will describe the creation of a business process in two procedures:

1. [Create a new business process](#create-a-new-business-process)
2. [Add meeting filters](#add-meeting-filters)

#### Create a new business process

**Role:** Analyst

In these steps, we create and name an empty business process.

1. In Workplace Analytics, on the left navigation pane, expand **Analysis settings** and select **Business processes**.

2. On the **Analysis settings** > **Business processes** page, select **Add Business process**.

3. On the **New Business process** page, type a name and, optionally, a description for your new business process. (In this example, we'll give  **Bangalore hiring** for the name of the business process.) Select **Continue**.

4. For **Data set**, select the data set that we recently created, **Bangalore**.

5. For **Content type**, leave **Meetings** selected, and select **Continue**.

6. Go to the following procedure.

#### Add meeting filters

**Role:** Analyst

Now, add restrictions to limit the analysis to data that relates to hiring. The data consists of meetings that have taken place. The goal, therefore, is to examine meetings that took place for the purpose of hiring or recruitment.

Start on the **New business process** page:

![Biz process start page](../images/wpa/tutorials/keyword-page.png)

As an analyst, your goal is to find the keywords that most effectively filter out meetings that don't apply. The **New business process** mechanisms help you find those keywords. You start by typing words that you think might work. In this example, that means words related to hiring and recruitment.

1. In the field marked **Enter a search term**, type **interview** and press Enter. The system searches for content that's related to "interview" and displays the results in a table.

   ![Results table](../images/wpa/tutorials/result-words.png)

2. (Optional) You might find it helpful to sort the values in the table's columns. Do this by selecting a header in the table (**Rank**, **Phrase**, **Attendee meeting hours**, or **Meeting count**).

3. Scan the words in the **Phrase** column. Which ones do you find relate most closely to the concept of "hiring in Bangalore" (the business process to be analyzed)?

   If it's not immediately evident which words to select as keywords, there are two ways you can examine them more closely:

   * <u>Find related meetings.</u> Select the word. This opens a pane on the right side of the page that lists meetings whose subject lines contained this exact phrase. If these meetings are relevant to the business process, you might want to select this word as a keyword. 

   * <u>Find related phrases</u>. Expand the entry of the word by selecting the arrow to its left. This shows phrases that included the expanded terms in meeting subject lines. For example, if you expand **developer**, you might see the phrases "developer interviews," "developer hiring schedule," or, simply, "developer." For each phrase, you can see the number of meetings (**Meeting count**) that contained it in its subject line, and the amount of time spent in those meetings (**Attendee meeting hours**).

4. After you decide that a phrase is relevant, designate it as a keyword by using these steps:

   a. Hover your mouse over the phrase's row to see an unselected checkbox to the left of the phrase. 

   ![Unselected term](../images/wpa/tutorials/unchecked-box.png)

   b. Then, select the checkbox:

   ![Select term](../images/wpa/tutorials/select-terms.png)

5. With one or more terms checked, select **Add selected to** and then select **Included keywords**.

   ![Add terms to list](../images/wpa/tutorials/add-terms-to.png)

   After you include a term, it appears in the **Included keywords** list to the right of the results table:

   ![Term added to list](../images/wpa/tutorials/added-to-list-50.png)

6. (Optional) To explicitly _exclude_ terms from the keyword list, repeat the preceding step but after you select **Add selected to**, select **Excluded keywords**.

   >[!Note]
   >As you add keywords, the system becomes more context-aware. It automatically begins to uncover more content that's relevant to the keywords that you've added. It shows this new content in the results list.  

7. You might be aware of phrases that your company uses for the business process and you'd like to add them as keywords directly, without first conducting a search (as described in the preceding steps). In this case, add phrases directly to the keyword list. To do this, under **Included keywords**, select **Add**, type the phrase you want to add (or multiple phrases selected by semicolons), and press Enter.

8. Look at the numbers of meeting hours and meetings at the top of the page:

   ![Meeting hours](../images/wpa/tutorials/meeting-hours.png)

   The totals (229.5K and 409K) reflect the meeting hours and meetings in the entire data set. The smaller numbers reflect the numbers of meeting hours (11.K) and meetings (20K) in the data associated with the keywords that you currently have selected. These smaller numbers change as you add or delete keywords.

   If you are familiar with the hiring process, these numbers could indicate that your selection of keywords is too narrow (too few meetings and hours) or too broad (too many), after which you can adjust accordingly by adding or deleting keywords.
 
9. You might have added some keywords and feel you're not finished but you have no more time. In this case, you can select **Save as draft**, return later, and resume where you left off.

10. When you're finished defining the business process, select **Submit**. The system starts processing your new business process and gives it a [status](#business-process-statuses) of "In progress."

### Business process statuses

Business processes can have the following status:
 
* <u>Draft</u> &ndash; You are creating or editing the business process but you have not selected **Submit**.  
 
* <u>In progress</u> &ndash; You've selected **Submit** and the business process is being processed by the system.

* <u>Ready</u> &ndash; The business process has been successfully published and can be used in Workplace Analytics by an analyst in the same partition.

* <u>Error</u> &ndash; The processing of the business process failed. (If a business process that you've submitted shows "Error" status, you can request help by [contacting Workplace Analytics support](../overview/getting-support.md).)

You can find a list of existing business processes and their statuses on the **Analyze** > **Business process analysis** page of Workplace Analytics:

![Data sets page](../images/wpa/tutorials/business-processes.png)

## Analyze a business process

You analyze business processes by using Workplace Analytics [queries](query-basics.md). You can use the following query types in this kind of analysis:

* [Meeting queries](meeting-queries.md)

* [Person queries](person-queries.md)

## Related topics

* [Prepare organizational data](../setup/prepare-organizational-data.md)

* [Meeting queries](meeting-queries.md)

* [Person queries](person-queries.md)
