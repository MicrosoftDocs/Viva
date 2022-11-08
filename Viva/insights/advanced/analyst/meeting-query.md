---
title: Meeting query
description: Learn how to run a custom meeting query in the Microsoft Viva Insights advanced insights app
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Create a custom meeting query

>[!Tip]
> You can find a demo video, download sample results, and go through a **Show me how** explanation while you’re building your query. Select these options just above **Query setup**.
:::image type="content" source="../images/person-query-setup-help.png" alt-text="Setup help with link to video, sample, and walk-through above Query setup":::

Set up, select data for, and run your query by following the steps and guidance in this section.

### Query setup

In **Query setup**, you define some basic information about your query, like its name, the time period it will analyze, and whether it will refresh on its own.

#### To set up your query

1. From the [advanced insights app's](https://go.microsoft.com/fwlink/?linkid=2201482) **Analysis** page, navigate to **Custom queries > Meeting query** and select **Start analysis**.
    >[!Note]
    >If you're an existing Viva Insights customer, refer to the note in the [Introduction](../introduction-to-advanced-insights.md) for more information about using the new platform.

2. Under **Query setup**:

    1. Optional: Name your query. Queries are assigned a default name, which follows this format: Query type, user ID, date, and time. Make sure the name is unique.
    1. Optional: Select a **Time period**. This field defaults to **Last 3 months**, but you can select another time period you want your query to analyze. Pick from **Last 1 year**, **Last 6 months**, **Last 1 month**, or a **Custom** date range. If you choose a **Custom** date range, use the date picker to select the range.
    :::image type="content" source="../images/person-query-timeperiod.png" alt-text="Time period dropdown.":::
    :::image type="content" source="../images/person-query-timeperiod-datepicker.png" alt-text="Time period with date pickers highlighted.":::
    1. Optional: Set the query to automatically update by selecting the **Auto-Refresh** box. When you select the auto-refresh option, your query automatically runs and computes a new result every Viva Insights gets updated collaboration data for licensed people. This option is deselected by default, but you can select it on any query where the **Time period** isn’t customized.
        :::image type="content" source="../images/person-query-auto-refresh1.png" alt-text="Time period with Auto-Refresh highlighted.":::
    >[!Note]
    >If the organizational data used in an auto-refreshing query changes (for example, an attribute name is altered or an attribute is removed), you might see an error when you run the query.

    4. Optional: Type a **Description**.

        Selecting **More Settings** brings you to the **More Settings** pane. This pane shows the metric rules that apply to your query. To find out more about metric rules that apply to your query, select **See metric rule details**.
    >[!Note]
    > Metrics are criteria used to measure the productivity and wellbeing of employees, and metric rules are rules Viva Insights uses to improve the accuracy of your query results.
    >
    > To learn more about metrics used in Viva Insights, refer to [Metric definitions](../reference/metrics.md). To learn more about metric rules, refer to [Metric rules](./metric-rules.md).

### Metrics 

In **Select metrics for what you want to know about your meetings**, you specify what you want to find out about the meetings you’re analyzing, and also define the meetings you’re including in your query. 

#### About metrics

Metrics are criteria used to measure the productivity and wellbeing of employees. In the case of meeting queries, metrics describe employee wellbeing as related to meetings. For example, if you’re wondering how much time employees spend multitasking during meetings, you could use the **Multitasking hours** metric in your query.

##### Select metrics pane

###### Metric categories

In the **Select metrics** pane, metrics are grouped by *metric category*. Expand the categories to see which metrics they contain. Let’s say you were looking for how many hours attendees spent in meetings.  You'd find the **Attendee meeting hours** metric under the **Meeting impact metrics** category. 

:::image type="content" source="../images/meeting-query-metric-pane1.png" alt-text="Add metrics pane":::

<!--address capitalization-->

###### Keyword search and more information

While you're adding meeting query metrics metrics, you can use the search bar at the top of the pane. Enter keywords or related Power BI templates to find the metrics you're looking for.

To learn more about a metric, hover over its information icon.

### To add metrics to your query

Here’s how you add metrics to your query:

3. Under **Select metrics for what you want to know about your meetings**, select the **Add metrics** button.

    :::image type="content" source="../images/meeting-query-select-metrics.png" alt-text="Add metrics pane":::

4. The **Add metrics** button brings you to the **Select metrics** pane. Using the check marks and the tools described earlier (like search) select the metrics you want to use in the query, then select **Add to query**.

    The **Add to query** button adds these metrics into your query and takes you back to the setup screen. The metrics you selected appear as tags in the box beneath the section description. 

### Meetings and employees

Once you determine what you want to know about meetings, you select which meetings and employees you want to include in your query. In **Select which meetings and employees you want to include in the query**, define the employees you want to analyze through *conditions* and *condition groups*.

#### About conditions and condition groups

A condition is a statement about one attribute you want to analyze in your query. A condition only extracts rows from your organizational data that meet certain criteria, which you specify in the condition statement. For example, if your condition statement read, “Organization = Contoso.com,” the query would only extract rows that equal Contoso.com” under the **Organization** column. A condition group is a combination of conditions connected with a conjunction ("and" or "or"). In the following image, the condition group is in the block to the right of the conjunction "and."

:::image type="content" source="../images/meeting-query-condition-group2.png" alt-text="Condition group":::


#### To add employees to your query

5. Select the **Add condition** or **Add condition group** button.
    :::image type="content" source="../images/meeting-query-condition-buttons.png" alt-text="Screenshot that shows the Add condition button.":::

6. Using conditions and condition groups, add one or multiple filters to narrow down your analysis. 

    Refer to our sample meeting query for an example of using conditions and condition groups.

>[!Note]
>
>The default conjunction for conditions and condition groups is “and.” To select “or” instead, use the dropdown menu.


### Meeting and employee attributes

#### About meeting and employee attributes

Meeting and employee attributes are the data fields—or columns—that appear in your query output. These attributes are broken up into two categories: the first is about the meeting itself (for example, Sensitivity, Duration, Importance), and the second is attributes from the organizational data you've uploaded to Viva Insights. In **Select which meeting and employee attributes you want to include in the query**, you narrow down which data fields your query includes—for example, **Job level** or **Hire date**—to prevent your output (.csv) file from being larger than necessary. Making selections here:

* Improves data analysis with fewer columns in a smaller file.
* Further protects private data by excluding columns from the file.
* Enables you to select **Clear all** to clear the selected columns.

#### To add meeting and employee attributes to your query

6.	Select the **Select attributes** button, then:
    1. On the right pane, use the checklist to make selections.
    1. When you're done picking attributes, select the **Add to query** button.
        :::image type="content" source="../images/meeting-query-add-attributes.png" alt-text="Select meeting and employee attributes pane, with 'Add to query' button highlighted":::
    
    Attributes appear as tags in the box above the **Select attributes** button.

    >[!Note]
    >
    >If an attribute appears as a red tag, that attribute might have been removed or renamed. You might see red tags if you’re cloning or editing a query and the attributes have changed since the query was last run. You can remove these marked attributes to get the query to run properly.

## Running the query

7.	After you’ve set up your query, selected metrics, set conditions and condition groups, and selected meeting and employee attributes, you’re ready to run your query. Select the **Run** button in the screen’s upper right.

### To access your query results

After your query runs, access its results in the **Query results** page. On the **Query results** page, you can also edit and clone your query. For further information, refer to [Access query results and modify existing queries](./query-results.md).

## Example meeting query

Let’s say you wanted to run a meeting query to find out how often attendees are multitasking during large, recurring meetings.

Here’s how you might do that:

1. Set up your query.
    1.  **Query name**: Give your query a custom name by typing in something like “Multitasking in large meetings.”
    1. **Time period**: Select **Last 6 months**.
    1. **Auto-Refresh**: You just want to have this run once, so leave the **Auto-Refresh** box deselected.
    1. **Description**: Other analysts in your organization might want to know more about this query, so give it a brief description.
            :::image type="content" source="../images/meeting-query-sample-setup.png" alt-text="Select meeting and employee attributes pane, with 'Add to query' button highlighted":::
1. Add metrics.
    1. Under **Select metrics for what you want to know about your meetings**, select the **Add metrics** button.
    1. You want to know how many hours attendees spend in these meetings, so you select **Attendee meeting hours** from the **Meeting impact metrics** category. 
    1. You want to know how many attendees are multitasking and whether this might be because they have conflicting meetings. You select **Number of attendees multitasking** and **Number of attendees with conflicting meeting** from the **Meeting quality metrics** category.
    1. When you're done picking metrics, you select the **Add to query** button.
     :::image type="content" source="../images/meeting-query-sample-metrics.png" alt-text="Select meeting and employee attributes pane, with 'Add to query' button highlighted":::
1. Specify the meetings and employees you want to analyze.
    1. Under **Select which meetings employees you want to include in the query**,  select the **Add condition group** button, then **Add condition group**.
    1. Because you want this query to analyze large meetings (which your company defines as having 20 or more participants), you select **Participant count** from the **Meeting attribute** dropdown menu, set the **Operator** to **>=**, and enter **20** for the **Value**.
    1. Because you want to analyze recurring meetings, add a new condition, then set **Meeting attribute** to **Recurring**, leave the **Operator** at **=**, and leave the **Value** at **true**.
     :::image type="content" source="../images/meeting-query-sample-filter.png" alt-text="Select meeting and employee attributes pane, with 'Add to query' button highlighted":::
1. Choose the meeting and employee attributes you want to include in your output file.
    1. Under **Select which meeting and employee attributes you want to include in the query**, select the **Select attributes** button.
    1. Because you want to know how big each meeting is, select **Participant count** from the right pane, under the **Meetings** category.
    1. You also want to know how many multitaskers are supervisors. In the organizational data you upload to Viva Insights, you include an indicator of whether someone is a supervisor. Select that attribute under the **Organizational data** button.
    1. Select the **Add to query** button.
         :::image type="content" source="../images/meeting-query-sample-attributes.png" alt-text="Select meeting and employee attributes pane, with 'Add to query' button highlighted":::
1. Run the query. On the upper right of the screen, select the **Run button**.
1. After the query successfully runs, find its results in the **Query results** page. To:
    1. Download the .csv output file: Select the CSV icon from the **Downloads** column. If you want to connect the query to another file, like a Power BI visualization, you can select the copy link icon.
    1. **Edit**, **Edit query name**, **Clone**, **Favorite**, or **Delete** the query: Select the ellipses to the right of the **Downloads** column, then select the appropriate choice. 

    > [!Caution]
    > Editing queries overwrites existing results. If you want to keep your query’s results, use the **Clone** feature—which creates an identical copy of the query—instead.

    >[!Note]
    > Only the analyst who originally ran the query can **Edit query name**, **Edit**, or **Delete** the query. Other analysts in the organization can **View**, **Clone**, and **Favorite** the query.

## Related topics

[Metric descriptions](./metrics.md)

[Access query results and modify existing queries](./query-results.md)
