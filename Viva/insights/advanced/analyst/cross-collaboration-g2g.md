---
ms.date: 08/07/2023
title: "Cross-collaboration: Group-to-group query"
description: Learn how to run a custom cross-collaboration query for collaboration between two groups in your organization
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva-insights
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---


# Collaboration between two groups (group-to-group)

Group-to-group queries help you understand how a team invests their time across the rest of the organization and beyond. The query results identify pairs of groups, as defined by organizational attributes, along with how much time people in the first group (known as “primary collaborators”) allocated to other groups (known as “secondary collaborators”).

:::image type="content" source="../images/analyst-xc-g2g-illustration.png" alt-text="Illustration of how group-to-group queries work.":::

### Overview of time investment

You can create better group queries with an understanding of time investment. Here are the basic concepts:

* Time investment measures how groups spend their time. An interaction is a meeting that was attended, a sent or received email, or a sent or read chat. For each interaction, the total time that one group spent on the interaction is invested into the other groups that participated.
* A group-to-group query can analyze time invested only for employees in the population of measured employees, namely those who are licensed for Viva Insights. People who do not have a license for Viva Insights can be listed as secondary collaborators, but not primary collaborators.
* The time investment approach assumes that a primary collaborator group invests time only to themselves if no other groups participated in the meeting, email, or chat.

In addition, group-to-group queries adhere to these principles: 

Principle 1: Time investment is proportional to time.
* The time invested by a member of the primary collaborator group is proportional to the time they spend in all collaboration activities.

Principle 2: Time investment is proportional to attendance.
* Groups with more people in a collaboration activity are investing more time into the collaboration activities.

Principle 3: Within-group allocation happens when the primary collaborator group and secondary collaborator group are the same, i.e., Primary Collaborator = Secondary Collaborator.
* "Within group" refers to single-team activities. Within-group activities are not possible when primary collaborators and secondary collaborators are grouped by different attributes.

## Create a group-to-group query

### Set up your query

1.	In the advanced insights app’s **Analysis** page, go to the **Custom queries** section, find **Cross-collaboration query**, and select **Start analysis**.
1.	Name your query (optional). Queries are assigned a default name, which follows this format: "CrossCollaborationQuery," user ID, date, and time. Make sure the name is unique.
3.	Select a **Time period** (optional). This field defaults to Last 3 months, but you can select another. Pick from **Last 1 year**, **Last 6 months**, **Last 1 month**, or a **Custom date range**. If you choose a Custom date range, use the date picker to select the range.  
4.	Optional: Set the query to automatically update by selecting the **auto-refresh** box. When you turn on the auto-refresh option, your query automatically runs and computes a new result every month. This option is turned off by default, but you can use it on any query where the **Time period** isn’t customized. 
5.	Optional: Type a **Description**.
6.	Optional: To change which metric rule your query uses, select **More Settings** beneath the **Description** box. To find out more about each rule, select **View rule**.

### Select group-to-group query

Select **Collaboration between two groups in your organization** to create a group-to-group query.

:::image type="content" source="../images/analyst-xc-g2g-setup.png" alt-text="Screenshot showing the UI to set up group-to-group queries." lightbox="../images/analyst-xc-g2g-setup.png":::

### Add metrics, filters, and employee attributes

1. Under **Add metrics**, select the **Add metrics** button, then pick metrics from the **Select metrics** pane. 
1. When you're done picking metrics, select **Add to query**.
1. Under **primary collaborator,** define your collaborator group—that is, those whose collaboration patterns are at the center of your analysis. Select which employees you want to include as primary collaborators and the attribute you want to group them by.
1. Under **secondary collaborator**, define your secondary collaborator—that is, those whose interactions with the primary collaborator are at the center of your analysis. Select which employees you want to include as secondary collaborators and the attributes you want to group them by.

    >[!Tip]
    > Need more information about collaborators? Learn about primary and secondary collaborators, and how to choose them, [here](collaborators.md).


### Run your query

After you’ve set up your query, you’re ready to run it. In the screen’s upper right, select **Run**.

## About query results

### How to access your results

After you run your query, go to the **Query results** page to check your query’s status. When your query is ready, a green checkmark appears under the **Status** column.

To download your results as a .csv file, select the CSV icon under the **Downloads** column.

### What your results show

Your query results show the amount of collaboration time between your primary and secondary collaborator groups, as well as how that time was spent.

Here’s how columns will appear in your results file:

The first two columns identify the primary collaborator and secondary collaborator pairs by providing the organization attribute value that defines the group. The primary collaborator column is titled **PrimaryCollaborator_[GroupByAttribute]** and the secondary collaborator column is titled **SecondaryCollaborator_[GroupByAttribute]**.

:::image type="content" source="../images/analyst-xc-g2g-primarysecondary.png" alt-text="Screenshot showing primary and secondary collaborator pairs in the results.":::

The last columns in the file give you the metric date and results for the metrics you selected when you built the query.

The **MetricDate** column shows the start date of the aggregated output. This date will be the first day of the month that your data covers. The subsequent columns show values for the metrics you added when you built the query.

:::image type="content" source="../images/analyst-xc-p2g-datecounts.png" alt-text="Screenshot showing the metric date and results.":::
