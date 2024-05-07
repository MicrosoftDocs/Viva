---
ms.date: 08/07/2023
title: "Cross-collaboration: person-to-group query"
description: Learn how to run a custom cross-collaboration query for collaboration between individuals and groups in your organization
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


# Collaboration between an individual and a group (person-to-group)

Person-to-group queries help you understand how an individual invests their time across different groups. The query results include:

* Individuals, or “primary collaborators,” by their **PersonID**s (de-identified)
* One or more groups you define in the query as "secondary collaborators"
* The amount  of time the primary collaborator invests with the secondary collaborator, and how they spend their time

:::image type="content" source="../images/analyst-xc-p2g-illustration.png" alt-text="Illustration that shows how person-to-group queries work.":::

>[!Important]
>Because individuals are assigned a randomly generated **PersonID** to maintain de-identification, there is no way to identify an individual in the query's results.

### Overview of time investment

You can create better person-to-group queries with an understanding of time investment. Here are the basic concepts:

* Time investment measures how individuals spend their time. For each interaction (a meeting attended, a sent or received email, or a sent or received chat), the time that a person spent on the interaction is invested into each of the groups that participated.
* A person-to-group query can analyze time investment only for employees in the population of measured employees, namely those who are licensed for Viva Insights. People who do not have a license for Viva Insights can be listed as secondary collaborators, but not primary collaborators.
* The time-investment approach assumes that primary collaborators allocate time to their own group, i.e., "within group," if no other groups are participating in the meeting, email, or chat.

## Create a person-to-group query

### Set up your query

1.	In the advanced insights app’s **Analysis** page, go to the **Custom queries** section, find **Cross-collaboration query**, and select **Start analysis**.
1.	Name your query (optional). Queries are assigned a default name, which follows this format: "CrossCollaborationQuery," user ID, date, and time. Make sure the name is unique.
3.	Select a **Time period** (optional). This field defaults to Last 3 months, but you can select another. Pick from **Last 1 year**, **Last 6 months**, **Last 1 month**, or a **Custom date range**. If you choose a Custom date range, use the date picker to select the range.  
4.	Optional: Set the query to automatically update by selecting the **auto-refresh** box. When you turn on the auto-refresh option, your query automatically runs and computes a new result every month. This option is turned off by default, but you can use it on any query where the **Time period** isn’t customized. 
5.	Optional: Type a **Description**.
6.	Optional: To change which metric rule your query uses, select **More Settings** beneath the **Description** box. To find out more about each rule, select **View rule**.

### Select person-to-group query

Select **Collaboration between an individual and a group in your organization** to create a person-to-group query.

:::image type="content" source="../images/analyst-xc-p2g-ui.png" alt-text="Screenshot that shows the UI for selecting person-to-group queries.":::

### Add metrics, filters, and employee attributes

1. Under **Add Metrics**, select the **Add metrics** button, then pick metrics from the **Select metrics** pane.
1. When you're done picking metrics, select **Add to query**.
1. Under **primary collaborator**, define your primary collaborator—that is, those whose collaboration patterns are at the center of your analysis. Select which employees you want to include as primary collaborators using filters.
1. Under **secondary collaborator**, define your secondary collaborator—that is, those whose interactions with the primary collaborator are at the center of your analysis. Select which employees you want to include as secondary collaborators and the attribute you want to group them by.

    >[!Tip]
    > Need more information about collaborators? Learn about primary and secondary collaborators, and how to choose them, [here](collaborators.md).

3.	Under **Organizational data**, select the attributes—or descriptive pieces of information about primary collaborators—that you want to appear in the results along with the metrics you picked in step 1. You can use these attributes to further summarize your results—for example, create analyses that compare and contrast the collaboration of different groups in your organization.

### Run your query

After you’ve set up your query, you’re ready to run it. In the screen’s upper right, select **Run**.

## About query results

### How to access your results

After you run your query, go to the **Query results** page to check your query’s status. When your query is ready, a green checkmark appears under the **Status** column.

To download your results as a .csv file, select the CSV icon under the **Downloads** column.

### What your results show

Your query results show the amount of collaboration time between a de-identified person and a group, as well as the type of collaboration activities.

Here's how columns will appear in your results file:

The first column identifies the primary collaborator in the pair by providing a de-identified ID number. This column appears automatically and is titled **PrimaryCollaborator_PersonId**.

:::image type="content" source="../images/analyst-xc-primary-collab-results.png" alt-text="Screenshot that shows results for the PrimaryCollaborator_PersonId column.":::

The next columns describe the primary collaborator. The column names for these attributes are the organizational attributes you selected while you built the query, with the prefix **PrimaryCollaborator_**. In the graphic below, the analyst selected **FunctionType**, **LevelDesignation**, and **Organization** as their attributes:

:::image type="content" source="../images/analyst-xc-primary-collab-results-attributes.png" alt-text="Screenshot that shows results for the PrimaryCollaborator attribute columns.":::

The following column identifies the secondary collaborator group **SecondaryCollaborator_{GroupByAttribute}**, and provides an org attribute value that defines the group.

:::image type="content" source="../images/analyst-xc-p2g-secondcollab-function.png" alt-text="Screenshot that shows results for the SecondaryCollaborator attribute columns.":::

The last columns in the file give you the metric date and results for the metrics you selected when you built the query.

The **MetricDate** column shows the start date of the aggregated output. This date will be the first day of the month that your data covers. The following columns show values for the metrics you added when you built the query.

:::image type="content" source="../images/analyst-xc-p2g-datecounts.png" alt-text="Screenshot that shows the metric date and query results.":::