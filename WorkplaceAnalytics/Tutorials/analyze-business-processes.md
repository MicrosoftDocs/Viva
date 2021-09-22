---

title: Business process analysis in Workplace Analytics 
description: Analyze business processes -- Introduction and walkthrough   
author: paul9955
ms.author: v-pausch
ms.topic: article
ms.localizationpriority: medium 
ms.prod: wpa
manager: scott.ruble
audience: Admin
---

# Business process analysis

When you and your co-workers perform an organized series of steps to reach a goal, you've participated in a business process. For example, your organization's hiring process might consist of obtaining leads, screening candidates, conducting interviews, making an offer, and sending new hires to HR for onboarding. Later business processes might have goals of training or coaching.

You can improve your business processes by analyzing them; for example, by measuring their cost in time and money. For example, your business might conduct an information-security audit from time to time. Your CFO or CIO might want to know whether too little, too much, or just the right amount of time is being spent on these audits, and whether the right roles of employees have been participating in them.

To make these determinations, conduct an analysis by running a Workplace Analytics query in which you designate the business process (such as hiring or auditing) as a query filter or a [metric filter](../use/metric-filters.md) while defining a [query](query-basics.md). <!-- ***  CALL THESE NEW FILTERS OUT IN THAT TOPIC  *** -->

Use the following procedures to analyze a business process:

1. [Define a data set](#define-a-data-set) &ndash; Make sure that you're analyzing only data that is relevant in every aspect, such as organizationally and geographically.

2. [Define a business process](#define-a-business-process) &ndash; Define the business process that you want to analyze within the data set that you defined in the preceding step.

3. [Analyze a business process](#analyze-a-business-process) &ndash; Compose and run a Workplace Analytics query in which you select the business process as a parameter.

This illustration shows these procedures and the types of data that they involve:

![Conceptual art: three steps.](../images/wpa/tutorials/steps-3.png)

The following sections describe these procedures.

>[!Note]
>After you define a data set, it becomes available to all other analysts in your partition. Similarly, after you define a business process, it also becomes available to all other analysts in your partition.

## Define a data set

Before you define a business process, you need to select the data set that's applicable to that process. For example, you might want to answer this question: "How much time does our sales team spend in sales activities?"

You start by limiting the data set for your query by keeping only the organizational data that applies to the analysis &ndash; in this case, meetings that were attended by at least one sales representative.

To define a data set, use the following procedure:

### Data set steps

**Role:** Analyst

Every business process that you create must be based on a data set. For that reason, creating at least one data set is mandatory before you can proceed to [Define a business process](#define-a-business-process).

In this example, we restrict the analysis data to meetings of a particular length that were attended by at least one sales representative.

1. In Workplace Analytics, on the left navigation pane, expand **Analyze** and select **Business process analysis**.

2. On the **Analyst settings** page, select **Data sets** and then, on the right side of the page, select **Add data set**.

   ![new data set.](../images/wpa/tutorials/new-data-set.png)

3. On the **New data set** page, type a name and, optionally, a description for your new data set. (In this example, we've given **SalesDataSet** as the name of the data set.) Select **Continue**.

   ![data set name given.](../images/wpa/tutorials/data-set-name-in-place.png)

4. Under **Time period** select start and end dates. All meetings that took place outside of this time period will be excluded from the data set.

5. Under **Meeting exclusions**, specify a [meeting exclusion rule](meeting-exclusions-intro.md) or accept the default, the [Tenant default meeting exclusion rule](meeting-exclusion-concept.md#default-meeting-exclusion-rule).

6. Under **Which meetings do you want to include in your query results?**, define filters to scope the data set to the business-process analysis that you want to perform. You'll use these filters to filter out meetings. Select **Add filter**.

7. Select **Meeting**:

   ![Add a Meeting filter.](../images/wpa/tutorials/meeting-filter-1.png)

8. In the boxes to the right of **Meeting's**, select **Duration (in hours)**, **<** (less than), and **0.5** (hours).

9. On the next line, select **Attendee**. This lets us choose the work function (in this case, sales) of meeting attendees.

   ![Add an Attendee filter.](../images/wpa/tutorials/attendee.png)

10. In the boxes to the right of **Organizer's**, select **FunctionType**, **Equals**, and **Sales**. (The choices that are available are determined by the [organizational data](../setup/prepare-organizational-data.md) that the Workplace Analytics admin has uploaded.)

    ![Sales as function type.](../images/wpa/tutorials/function-type-sales.png)

11. Select **Submit**.

   This starts the creation of a data set that will contain data that matches these criteria (and no other data). The time required to process the data set depends on its size.

### Data set statuses

Right after you select **Submit**, the data set has a status of "In progress"; after it is processed (which could take from several minutes to a few hours, depending on the size of the data set), its status changes to "Ready" and you can use it in business-process definitions and analyses. If data-set creation fails, the data set changes to "Failed" status. (If a data set that you've submitted shows "Failed" status, you can request help by [contacting Workplace Analytics support](../overview/getting-support.md).)

You can find a list of existing data sets and their statuses in **Analyze** > **Business process analysis** > **Data sets**:

![Data sets page.](../images/wpa/tutorials/data-set-statuses.png)

### Data set actions

After a data set has been created, it can be viewed, used, or deleted, but it cannot be edited. A dataset can be deleted only if no business processes are using it. After you delete a data set, it cannot be recovered.

To view or delete a data set, first find it on the **Data sets** tab of the **Analyze** > **Business process analysis** page of Workplace Analytics, and then use the **View** or **Delete** options.

## Define a business process

Before you can analyze a business process within your organization, you need to define it. You define a business process by assembling a list of keywords that are typically found in meeting subject lines associated with that process. This list defines the business-process filter. You select these keywords on the **New business process** page in the **Analyze** area of Workplace Analytics:  

![Biz process start page.](../images/wpa/tutorials/start-page.png)

>[!Note]
>Currently, you can use only English keywords in the process of defining a business process. This holds true even if your instance of Workplace Analytics is in a language other than English.

### Business process steps

In this example, we want to examine meetings of a particular length that sales representatives attended. To make sure that the data we use is restricted to the correct division, we'll use the "SalesDataSet" that we defined in [Data set steps](#data-set-steps).

We will describe the creation of a business process in two procedures:

1. [Create a new business process](#create-a-new-business-process)
2. [Assemble a list of keywords](#assemble-a-list-of-keywords)

#### Create a new business process

**Role:** Analyst

In these steps, we create and name an empty business process.

1. In Workplace Analytics, on the left navigation pane, expand **Analyze** and select **Business process analysis**.

   ![business process list view.](../images/wpa/tutorials/add-biz-process.png)

2. Select **Add business process**.

   ![Add a business process.](../images/wpa/tutorials/new-business-process.png)

3. On the **New Business process** page, type a name and, optionally, a description for your new business process. (In this example, we'll give  **Sales interactions** as the name of the business process.) Select **Continue**.

4. For **Data set**, select the data set that we recently created, **SalesDataSet**.

5. For **Content type**, leave **Meetings** selected, and select **Continue**.

6. Go to the following procedure.

#### Assemble a list of keywords

**Role:** Analyst

In this procedure, you assemble the vocabulary that constitutes the business process. Start on the **New business process** page:

![Keyword selection.](../images/wpa/tutorials/keyword-page.png)

As an analyst, your goal now is to find the keywords that most effectively represent the business process. The **New business process** mechanisms help you find those keywords. You start by typing words based on keywords that your users typically use when referring to the process. The system then takes those words as cues to uncover additional content that it deems relevant. In this example, that means words related to sales interactions.

1. In the field marked **Enter a search term**, type **purchase** and press Enter. The system searches for content that's related to "purchase" and displays the results in a table.

   ![Results table.](../images/wpa/tutorials/result-words-2.png)

2. (Optional) You might find it helpful to sort the values in the table's columns. Do this by selecting a header in the table (**Rank**, **Keyword**, **Attendee meeting hours**, or **Number of meetings**).

   >[!Note]
   >The Rank column indicates relevance ranking. In the preceding illustration, a rank of 1 indicates that the "account" keyword is the most relevant to the specified search term "purchase." The concept is similar to the ranking in web-page search results.

3. Scan the words in the **Keyword** column. Which ones do you find relate most closely to the concept of "Sales activities" (the business process to be analyzed)?

   To make sure you're looking at relevant content, you can examine these terms more closely in either of two ways:

   * <u>Find related keywords</u>. Expand the keyword by selecting the ">" (greater-than) sign to its left. This shows multiple-word phrases that included the keyword. For example, if you expand the keyword **lead**, you might see "qualified lead" or "lead generation." For each keyword, you can see the **Number of meetings** that contained it in its subject line, and the amount of time spent in those meetings (**Attendee meeting hours**).

   * <u>View the metadata of actual meetings.</u> Click the keyword. This opens a pane on the right side of the page that lists meetings whose subject lines contained this exact phrase, along with additional information such as number of attendees and whether the meeting is recurring. If these meetings are relevant to the business process, you might want to consider this keyword for your business process.

4. After you decide that a keyword is relevant, include it into the business-process definition by completing these two steps:

   a. Hover your mouse over the keyword's row to see an unselected checkbox to the left of the keyword.

   ![Unselected term.](../images/wpa/tutorials/unchecked-box-2.png)

   b. Then, select the checkbox:

   ![Select term.](../images/wpa/tutorials/select-terms-2.png)

5. With one or more terms checked, select **Add selected to** and then select **Included keywords**.

   ![Add terms to list.](../images/wpa/tutorials/add-terms-to-2.png)

   After you include a term, it appears in the **Included keywords** list to the right of the results table:

   ![Term added to list.](../images/wpa/tutorials/added-to-list-50-2.png)

6. (Optional) To explicitly _exclude_ terms from the keyword list, repeat the preceding step but after you select **Add selected to**, select **Excluded keywords**.

   >[!Note]
   >As you add keywords, the system becomes more context-aware. It automatically begins to uncover more content that's relevant to the keywords that you've added. It shows this new content in the results list.  

7. You might already be aware of words that your company uses for the business process and you'd like to add them as keywords directly, without first conducting a search (as described in the preceding steps). In this case, add keywords directly to the keyword list. To do this, under **Included keywords**, select **Add**, type the keyword that you want to add (or multiple keywords selected by semicolons), and press Enter.

   Similarly, if there are words that you know you want to explicitly exclude, you can exclude them under **Excluded keywords**.

8. Look at the numbers of meeting hours and meetings at the top of the page:

   ![Meeting hours.](../images/wpa/tutorials/meeting-hours.png)

   The totals (229.5K and 409K) reflect the meeting hours and meetings in the entire data set. The smaller numbers reflect the numbers of meeting hours (11.K) and meetings (20K) in the data associated with the keywords that you currently have added to the business process. These smaller numbers change as you add or delete keywords.

   If you are familiar with the hiring process, these numbers could indicate that your selection of keywords is too narrow (too few meetings and hours) or too broad (too many), after which you can adjust accordingly by adding or deleting keywords.

9. You might have added some keywords and feel you're not finished but you have no more time. In this case, you can select **Save draft**, return later, and resume where you left off.

   ![Business process options.](../images/wpa/tutorials/business-process-options.png)

10. When you're finished defining the business process, select **Submit**. (**Submit** is available only if at least one keyword is present in the **Included Keywords** list.) The system starts processing your new business process and gives it a [status](#business-process-statuses) of "In progress."

### Business process statuses

Business processes can have the following status:

* <u>Draft</u> &ndash; You are creating or editing the business process but you have not selected **Submit**.  

* <u>In progress</u> &ndash; You've selected **Submit** and the business process is being processed by the system. The business process completes processing during the regular weekly processing of Workplace Analytics.

* <u>Ready</u> &ndash; The business process has been successfully processed and can be used in queries in Workplace Analytics by an analyst in the same partition.

* <u>Failed</u> &ndash; The processing of the business process failed. (If a business process that you've submitted shows "Failed" status, you can request help by [contacting Workplace Analytics support](../overview/getting-support.md).)

   ![Business process statuses.](../images/wpa/tutorials/business-process-list-2.png)

### Business process actions

After a business process has been created, it can be viewed, used, or deleted, but it cannot be edited (unless it is in Draft state). A business process can be deleted only if no recurring queries are using it. After you delete a business process, it cannot be recovered.

To view or delete a business process, first find it on the **Analyze** > **Business process analysis** page of Workplace Analytics, under the **Business processes** tab, and then use the **View** or **Delete** options.

## Analyze a business process

You analyze _real-world_ business processes by running Workplace Analytics meeting or person queries. As you do this, you use a _digital_ "business process" &mdash; the kind that you defined in [Business process steps](#business-process-steps) &mdash; as a filter.

Design your query and choose its metrics so that filtering by this digital business process focuses the query on the set of collaboration activities (the relevant set of meetings) that you want to analyze.

You can filter by business processes wherever the **Meeting** option is available as a filter or a metric customization. In the first of the following examples (for a meeting query), the **Meeting** option is available as a filter; in the second example (for a person query), the **Meeting** option is available as a metric customization.

### Use a business process in a meeting query

In [meeting queries](Meeting-queries.md#meeting-queries), business processes are only available as filters for meetings, as described in the following steps.

1. In Workplace Analytics, select **Query designer > Meeting** to open a Meeting query.

2. Enter initial information about the query such as its name, time period, and exclusions.

3. Under **Select filters**, select **Meeting**.

   ![Select filters.](../images/wpa/tutorials/select-filters-1.png)

4. Next to **Meeting’s**, select **Business process**.

   ![Select business process.](../images/wpa/tutorials/select-filters-2.png)

5. In the field on the right, select a business process. Only business processes in the "Ready" state are available for selection.

6. Finish defining your query and select **Run**.

#### Interpret your query results

The results of meeting queries in which you’ve specified a business-process filter will contain a column called **BusinessProcesses**. This column will contain the matched business process name for each meeting row in the results. If multiple business processes match a single meeting, this column will contain a comma-delimited list of matched business process names for the meeting.

For general information about examining query results, see [View, download, and export query results](../use/View-download-and-export-query-results.md).

### Use a business process in a person query

In [person queries](Person-queries.md#person-queries), business processes are available as filters for meetings that are used for customizing metrics, as described in the following steps.

1. In Workplace Analytics, select **Query designer > Person** to open a Person query.

2. Enter initial information about the query such as its name, time period, and exclusions.

3. Under **Select metrics**, select a metric. In this example, we’ll use **Collaboration hours**.

   ![Select metrics.](../images/wpa/tutorials/select-metrics-collab.png)

4. Customize the Collaboration hours metric. Start by selecting **Edit** (the pencil icon) .

   ![Customize the metric.](../images/wpa/tutorials/customize-metric.png)

5. Select **Add filter**.

   ![Add a filter.](../images/wpa/tutorials/add-filter.png)

6. For **Collaboration hours where**, select **Meeting**.

   ![Select meeting to customize.](../images/wpa/tutorials/select-meeting-collab.png)

7. Next to **Meeting’s**, select **Business process**.

   ![Select filters for meetings.](../images/wpa/tutorials/select-filters-3.png)

8. In the middle field, select "**=**" and in the field on the right, select a business process. Only business processes in the "Ready" state are available for selection.

9. Finish defining your query and select **Run**.

#### Interpret your query results

The results of meeting queries in which you’ve specified a business-process filter will contain a column called **BusinessProcesses**. This column will contain the matched business process name for each meeting row in the results. If multiple business processes match a single meeting, this column will contain a comma-delimited list of matched business process names for the meeting.

After the query runs, examine its results as described in [Understand and interpret query output](../use/csv-query-output-file.md) and [View, download, and export query results](../use/View-download-and-export-query-results.md).

## Data privacy

The business-process analysis feature follows the data-privacy standards of Workplace Analytics, which are described in [Privacy settings](../use/privacy-settings.md).

To define a business process, you must use meeting subject lines, but access to meeting subject lines is restricted by two of the available data-privacy settings: [Hash subject lines](../use/privacy-settings.md#hash-subject-lines) and [Exclude terms from subject lines](../use/privacy-settings.md#exclude-terms-from-subject-lines). These settings affect your ability to define a business process as described here:

### Hash subject lines

You can use this setting to control whether to show legible or hashed subject lines in [Meeting query](meeting-queries.md) results.

![Hash subject lines.](../images/wpa/tutorials/hash-subject-lines.png)

If your Workplace Analytics admin has chosen to hash subject lines by setting the **Hash subject lines** option to **Yes**, the subject lines of meetings that are shown in query results become unintelligible.

However, this option also makes subject lines unusable for business-process analysis. So, when this setting is in effect, if you select **Add business process** in the procedure to [Create a new business process](#create-a-new-business-process), you'll see a warning stating that business-process analysis is unavailable. To re-enable it, contact your Workplace Analytics admin and ask them to set the **Hash subject lines** option to **No**.

### Exclude terms from subject lines

For data-privacy reasons, you might want to exclude particular meetings from analysis. (For more information, see [Exclude content from subject lines](../use/privacy-settings.md#exclude-terms-from-subject-lines).) You do this by adding words that occur in those meetings' subject lines to the **Exclude terms from subject lines** list on the **Privacy settings** page of Workplace Analytics:

![Exclude terms from subject lines.](../images/wpa/tutorials/exclude-terms-5.png)

How does the exclusion of terms affect your analysis of business processes? It affects your ability to [assemble a list of keywords](#assemble-a-list-of-keywords), which is the central task in defining a business process. This is because you define a business process atop a data set, and within that data set are the words that you can add as keywords. If your admin excludes a word (such as "merger" or "acquisition") from analysis in general, that also excludes it from data sets and consequently from business-process analysis.

The exclusion of terms does not work retroactively; that is, exclusions work only on new data. An exclusion takes effect if all of the following hold true:

* You create the data set after the admin creates the exclusion.
* You create the data set after the weekly data refresh is completed. (The collaboration data that Workplace Analytics uses is refreshed once a week, on Sunday. Workplace Analytics then processes the new data, which appears one day later, on Monday.)
* You define the data set to use new data. That is, as you [define the data set](#define-a-data-set), for **Time period**, select dates that take place entirely after the exclusion was defined and data was refreshed.

The following example shows how this can unfold:

| Date | Event |
| ---- | ----- |
| 1/1/2020 | A customer begins using Workplace Analytics. |
| 4/1/2020 | An admin excludes the term "merger."
| 4/8/2020 | The weekly data refresh has taken place. Any new data that arrived during the refresh will respect the exclusion; this means that any data sets based on this data will exclude the word "merger." (Also, any data that will arrive in the future will respect the exclusion.)
| 4/9/2020 | An analyst defines a data set, called "DS1," for the period 1/1/2020 – 4/1/2020. This data set does NOT respect the exclusion, which means that the word "merger" is _not_ excluded.
| 4/9/2020 | An analyst creates a business process that uses the data set DS1 and they later use it in a query. This business process does _not_ respect the exclusion and therefore still contains the word "merger."
| 8/1/2020 | An analyst defines a data set, called "DS2" for the period 5/1/2020 – 8/1/2020. This data set does respect the exclusion and therefore does _not_ contain the word "merger."
| 8/5/2020 | An analyst defines a business process that uses the data set DS2 and they later use it in a query. This data set (and therefore the business process that uses it) _does_ respect the exclusion and does _not_ contain the word "merger."

## Related topics

* [Prepare organizational data](../setup/prepare-organizational-data.md)
* [Meeting queries](meeting-queries.md)
* [Person queries](person-queries.md)
* [Privacy settings](../use/privacy-settings.md)
