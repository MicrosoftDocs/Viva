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
> You can download sample results and go through a **Show me how** explanation while you’re building your query. Select these options just above **Query setup**.
:::image type="content" source="../images/meeting-query-setup-help.png" alt-text="Setup help with link to video, sample, and walk-through above Query setup":::

## Overview

To run a meeting query, you'll follow five basic steps. Each of these steps takes place within one section of the [advanced insights app's](https://go.microsoft.com/fwlink/?linkid=2201482) **Custom queries > Meeting query** page.

>[!Note]
>If you're an existing Viva Insights customer, refer to the note in the [Introduction](../introduction-to-advanced-insights.md) for more information about using the new platform.

1. Set up your query.
1. Add metrics.
1. Add conditions and condition groups.
1. Add meeting and organizer attributes.
1. Run your query.

In this article, we talk about how to complete each of these steps, and also give some important background information about how metrics, conditions, and attributes work.

## Set up your query

*Section: **Query setup***

:::image type="content" source="../images/meeting-query-setup-section.png" alt-text="Screenshot showing the Query setup section, including name, Time period, Description, and Date fields and an Auto-Refresh box.":::

1. Under **Query setup**:

    1. Optional: Name your query. Queries are assigned a default name, which follows this format: "Activity," user ID, date, and time. Make sure the name is unique.
    1. Optional: Select a **Time period**. This field defaults to **Last 3 months**, but you can select another time period you want your query to analyze. Pick from **Last 1 year**, **Last 6 months**, **Last 1 month**, or a **Custom** date range. If you choose a **Custom** date range, use the date picker to select the range.
    :::image type="content" source="../images/custom-date-picker.png" alt-text="Screenshot that shows the Time period field with date-picker button highlighted and selectable calendar expanded.":::
    1. Optional: Set the query to automatically update by selecting the **Auto-Refresh** box. When you select the auto-refresh option, your query automatically runs and computes a new result every day. This option is deselected by default, but you can select it on any query where the **Time period** isn’t customized.
        :::image type="content" source="../images/hover-auto-refresh.png" alt-text="Screenshot that shows the Time period field with Auto-Refresh box.":::

    1. Optional: Type a **Description**.

        Selecting **More Settings** beneath the **Description** box brings you to the **More Settings** pane. This pane shows the metric rules that apply to your query. To find out more about these rules, select **See metric rule details**.
        >[!Note]
        > Metrics are criteria used to measure the productivity and wellbeing of employees, and metric rules are rules Viva Insights uses to improve the accuracy of your query results.
        >
        > To learn more about metrics used in Viva Insights, refer to [Metric definitions](../reference/metrics.md). To learn more about metric rules, refer to [Metric rules](./metric-rules.md).

## Add metrics 

*Section: **Select metrics for what you want to know about your meetings***

:::image type="content" source="../images/meeting-query-section-1.png" alt-text="Screenshot that shows the Select metrics field, with an Add metrics button.":::

2. Select the **Add metrics** button, then pick metrics from the resulting **Select metrics** pane. When you're done picking metrics, select **Add to query**.

    :::image type="content" source="../images/meeting-query-metric-pane2.png" alt-text="Screenshot of the Select metrics pane, with metric categories expanded to show available metrics, and an Add to query button.":::

    The **Add to query** button adds these metrics into your query and takes you back to the setup screen. The metrics you selected appear as tags in the box beneath the section description. 

    :::image type="content" source="../images/meeting-query-metric-tags.png" alt-text="Screenshot that shows selected metrics as tags in the Select metrics field.":::

### About metrics

Metrics are criteria used to measure the productivity and wellbeing of employees. In the case of meeting queries, metrics describe employee wellbeing as related to meetings. For example, if you’re wondering how many chats were sent during meetings, you could use the **Number of chats sent during the meeting** metric in your query.

You can pick from seven meeting-related metrics, which we've broken into two categories: meeting impact metrics and meeting quality metrics. Here are their names and definitions:


|Category|Name|Definition|
|---|----|----
|**Meeting impact metrics**| Attendee meeting hours| Sum of hours each attendee spent in a meeting
||Number of attendees| Number of people who attended a meeting
|**Meeting quality metrics**| Number of attendees multitasking|Number of attendees who sent or read emails or Teams chats during a meeting
|| Number of chats send during the meeting| Number of Teams chats attendees sent during a meeting
|| Number of emails send during the meeting|Number of emails attendees sent during a meeting
|| Number of participants with conflicting meetings|Number of intended participants or meeting organizer who have non-declined meetings that overlap
||Number of redundant attendees| Number of attendees who are redundant in a meeting, meaning that their manager and their manager's manager also attended

#### About the Select metrics pane

In the **Select metrics** pane, metrics are grouped by the metric categories we just described. Expand the categories to see which metrics they contain. Let’s say you were looking for how many hours attendees spent in meetings.  You'd find the **Attendee meeting hours** metric under the **Meeting impact metrics** category. 

While you're adding meeting query metrics metrics, you can use the search bar at the top of the pane. Enter keywords or related Power BI templates to find the metrics you're looking for.

To learn more about a metric, hover over its information icon.

:::image type="content" source="../images/meeting-query-metric-information.png" alt-text="Screenshot that shows hovering over a metric's information icon with pop-up metric definition and information.":::

## Add conditions and condition groups

*Section: **Select which meetings and employees you want to include in the query***

:::image type="content" source="../images/meeting-query-conditions.png" alt-text="Screenshot that shows hovering over a metric's information icon. The popup shows the metric definition and information.":::

3. Select the **Add condition** or **Add condition group** button. Using conditions and condition groups, add one or multiple filters to narrow down your analysis of meetings and employees.

    >[!Note]
    >
    >The default conjunction for conditions and condition groups is “and.” To select “or” instead, use the dropdown menu.

### About conditions and condition groups

When you use filters in a meeting query, you're creating individual condition statements or condition groups to narrow down your query's analysis. We describe which filters are available for meeting queries in the [next section](#predefined-filters).

A *condition* is a statement about one [attribute](#about-meeting-and-organizer-attributes) you want to analyze in your query. A condition only extracts rows from your organizational data that meet certain criteria, which you specify in the condition statement. For example, if your condition statement read, "Recurring = true,” the query would only extract rows that equal "true" under the **Recurring** column. 

:::image type="content" source="../images/meeting-query-sample-condition.png" alt-text="Screenshot that shows a condition filter where the Meeting attribute is Recurring, the Operator is =, and the Value is true.":::

A *condition group* is a combination of conditions connected with a conjunction ("and" or "or"). Condition groups contain multiple conditions, and all of them are true. Instead of considering conditions hierarchically (condition 1, condition 2), Viva Insights considers condition groups altogether when it runs queries.

Here's an example. Let's say that in addition to analyzing whether certain meetings recur, you only want to look at meetings that contain at least one person from the New York timezone *and* contain "Design" in their subject line. You'd add a condition group. The first statement in the group would cover the "at least one person from New York" part. The second statement, with an "and" conjunction, would cover the "'Design in the subject line" part.

:::image type="complex" source="../images/meeting-query-sample-condition-group.png" alt-text="Screenshot that shows a condition and a condition group.":::
   Screenshot of a condition, where Recurring = true. Below the condition, there's a condition group with two conditions.The first condition is where the Aggregation type of Attendees in Timezone = 1 selected (this is America/New_York, which appears as a tag below the condition). The second condition is connected by an "and" statement. The condition is where the Subject contains Design. Beneath the condition group, there is an "Add condition" and "Add condition group" button.
:::image-end:::

When Viva Insights runs your query, it will first check for whether meetings recur (your earlier condition statement). After that, instead of checking for at least one person from New York *then* the "Design" in the subject line, it will only check for meetings where *both* of those conditions are true.

#### Predefined filters

To create conditions and condition groups in meeting queries, you'll pick from 13 predefined filters. 10 of these filters are for meeting attributes, which have to do with characteristics of the meeting (for example, **Duration**). Three of these filters are for person attributes, which have to do with people involved in the meeting (for example, **Attendees**).

If you pick a meeting attribute, an operator (like "=")  appears. Then you fill in either "true" or "false," add a numerical value, or enter a text value. 

If you pick a person attribute, you create a filter based on organizational data with the following components:

* **Aggregation type** – *All*, *AtLeastOne*, or *None*
* **Meeting attribute** – The attribute you picked from the initial dropdown list
* **Organizational data attribute** – An attribute from your company's organizational data
* **Operator** – *=*, *!=*, *>*, *>=*, *<*, or *<=*, depending on which organizational data attribute you picked
* **Value** – One of a list of predefined choices, based on what your company's organizational data contains

>[!Note] 
>Organizational data available for you to use in filters depends on what your organization sends to Viva Insights.

Here's a list of all predefined filters, their type, input format, and an example condition statement that uses that filter.

|Name|Type|Input|Example statement
|----|--------|----|---|
|Subject|Meeting|Text value| Subject = Design review
|All Day Meeting| Meeting| True or false| All Day Meeting = true
|Cancelled| Meeting| True or false| Cancelled = false
|Recurring| Meeting| True or false| Recurring = true
|Intended participants| Person| Organizational data attribute and predefined value choices| All Intended participants Profession = Designer
|Attendees| Person| Organizational data attribute and predefined value choices| AtLeastOne Attendees City = Los Angeles
|Organizer| Person| Organizational data attribute and predefined value choices | Organization = Marketing
Duration| Meeting| Numerical value in the 00:00 format | Duration > 30:00
|Accept count| Meeting| Numerical value| Accept count >= 10
|No response count| Meeting| Numerical value| No response count < 5
|Decline count| Meeting| Numerical value| Decline count != 0
|Tentatively accepted count | Meeting| Numerical value| Tentatively accepted count <= 20
|Intended participant count | Meeting| Numerical value| Intended participant count > 100

#### To move and delete conditions and condition groups

To move a condition or condition group, select the six-dot icon to the right, then drag it above or below other conditions or groups. To delete a condition or condition group, select the trashcan icon to the right.

:::image type="content" source="../images/meeting-query-move-condition.png" alt-text="Screenshot that shows selected metrics in the box beneath Select metrics for what you want to know about your meetings.":::

## Add meeting and organizer attributes

*Section: **Select which meeting and employee attributes of the meeting organizer you want to include in the query***

4.	Select the **Select attributes** button, then:
    1. On the right pane, use the checklist to make selections.
    1. When you're done picking attributes, select the **Add to query** button.
        :::image type="content" source="../images/meeting-query-add-attributes1.png" alt-text="Screenshot that shows the attributes pane with three attributes selected and the Add to query button highlighted.":::
    
    Attributes appear as tags in the box above the **Select attributes** button.

    :::image type="content" source="../images/meeting-query-attribute-tags.png" alt-text="Screenshot of the attribute section of query building, with tags of selected attributes in a box below.":::

### About meeting and organizer attributes

Meeting and organizer attributes are the data fields—or columns—that appear in your query output. These attributes are broken up into two categories: the first is about the meeting itself (for example, Sensitivity, Duration, Importance), and the second is about the meeting organizer—that is, attributes from the organizational data you've uploaded to Viva Insights. 

In **Select which meeting and employee attributes of the meeting organizer you want to include in the query**, you narrow down which data fields your query includes—for example, **Recurring** (a meeting attribute) or **TimeZone** (an organizer attribute)—to prevent your output (.csv) file from being larger than necessary. Making selections here:

* Improves data analysis with fewer columns in a smaller file.
* Further protects private data by excluding columns from the file.
* Enables you to select **Clear all** to clear the selected columns.

#### Attribute errors and warnings

If an attribute appears as a *red* tag, that attribute might have been removed or renamed. You might see red tags if you’re cloning or editing a query and the attributes have changed since the query was last run. You can remove these marked attributes to get the query to run, or contact your admin to add these attributes back into the organizational data.

If an attribute appears as a *yellow* tag with a warning icon, that means the attribute isn't available. If you find a yellow tag on an attribute like "Subject" or "Title," email subject lines and meeting titles might be disabled. Your admin can turn on keywords if your organization wants to use them.

## Run the query

5.	Select the **Run** button in the screen’s upper right.

    :::image type="content" source="../images/run-button.png" alt-text="Screenshot that shows the Run button.":::

### To access your query results

After your query runs, access its results in the **Query results** page. On the **Query results** page, you can also edit and clone your query. For further information, refer to [Access query results and modify existing queries](./query-results.md).

Here's a sample of what a .csv meeting query output looks like:

:::image type="content" source="../images/meeting-query-output1-small.png" alt-text="Screenshot that shows a sample meeting query output .csv file." lightbox="../images/meeting-query-output1.png":::

## Example meeting query

Let’s say you wanted to run a meeting query to find out how often attendees are multitasking during large, recurring meetings.

Here’s how you might do that:

1. Set up your query.
    1.  **Query name**: Give your query a custom name by typing in something like “Multitasking in large meetings.”
    1. **Time period**: Select **Last 6 months**.
    1. **Auto-Refresh**: You just want to have this run once, so leave the **Auto-Refresh** box deselected.
    1. **Description**: Other analysts in your organization might want to know more about this query, so give it a brief description.
            :::image type="content" source="../images/meeting-query-sample-setup.png" alt-text="Screenshot of the Query setup section filled out with sample information.":::
1. Add metrics.
    1. Under **Select metrics for what you want to know about your meetings**, select the **Add metrics** button.
    1. You want to know how many hours attendees spend in these meetings, so you select **Attendee meeting hours** from the **Meeting impact metrics** category. 
    1. You want to know how many attendees are multitasking and whether this might be because they have conflicting meetings. You select **Number of attendees multitasking** and **Number of attendees with conflicting meeting** from the **Meeting quality metrics** category.
    1. When you're done picking metrics, you select the **Add to query** button.
     :::image type="content" source="../images/meeting-query-sample-metrics.png" alt-text="Screenshot of the select metrics section of the query building process, with selected metrics as tags in a box below the section header and subtitle.":::
1. Specify the meetings and employees you want to analyze.
    1. Under **Select which meetings employees you want to include in the query**,  select the **Add condition group** button, then **Add condition group**.
    1. Because you want this query to analyze large meetings (which your company defines as having 20 or more participants), you select **Participant count** from the **Meeting attribute** dropdown menu, set the **Operator** to **>=**, and enter **20** for the **Value**.
    1. Because you want to analyze recurring meetings, add a new condition, then set **Meeting attribute** to **Recurring**, leave the **Operator** at **=**, and leave the **Value** at **true**.
     :::image type="content" source="../images/meeting-query-sample-filter.png" alt-text="Screenshot that shows adding a condition group to the sample query with two conditions.":::
1. Choose the meeting and employee attributes you want to include in your output file.
    1. Under **Select which meeting and employee attributes you want to include in the query**, select the **Select attributes** button.
    1. Because you want to know how big each meeting is, select **Participant count** from the right pane, under the **Meetings** category.
    1. You also want to know how many multitaskers are supervisors. In the organizational data you upload to Viva Insights, you include an indicator of whether someone is a supervisor. Select that attribute under the **Organizational data** button.
    1. Select the **Add to query** button.
         :::image type="content" source="../images/meeting-query-sample-attributes.png" alt-text="Screenshot that shows selected attributes as tags in the box below the attributes section of the query builder.":::
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
