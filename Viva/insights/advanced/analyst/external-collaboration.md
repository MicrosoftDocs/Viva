---
ms.date: 08/1/2024
title: Collaboration between internal and external individuals
description: Learn how to run an external collaborator query, to understand how groups at your company collaborate with others outside your company.
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva-insights
search.appverid: 
- MET150 
manager: abelubetk
audience: Admin
---


# Collaboration between internal and external individuals 

External collaborator queries help you understand how an individual at your company invests their time with individuals at *other* companies, otherwise known as “external collaborators.” This type of query could be particularly useful for sales teams, who might seek more information about their leads and prospects. For example, this query could provide sales teams with information about contacts who are not in their customer relationship management (CRM) software, and the query could also provide data about different engagement points the sales team had with their contacts.  

The query includes:

* Individuals, or “primary collaborators,” indicated by their PersonIDs (de-identified)

* External Collaborators, or “secondary collaborators," identified by their email address

* The amount of time the primary collaborator invests with the secondary collaborator, and how they spend their time

## How to run an External Collaboration Query

### Set up your query

1.	In the advanced insights app’s **Home** page, select **Custom queries**, find **External collaboration query**, and select **Start analysis**. 
1.	Name your query (optional). Queries are assigned a default name, which follows this format: "External Collaboration Query," user ID, date, and time. Make sure the name is unique.
3.	Select a **Time period** (optional). This field defaults to Last 3 months, but you can select another. Pick from **Last 1 year**, **Last 6 months**, **Last 1 month**, or a **Custom date range**. If you choose a Custom date range, use the date picker to select the range.  
4.	Optional: Set the query to automatically update by selecting the **auto-refresh** box. When you turn on the auto-refresh option, your query automatically runs and computes a new result every month. This option is turned off by default, but you can use it on any query where the **Time period** isn’t customized. 
5.	Optional: Type a **Description**.
6.	Optional: To change which metric rule your query uses, select **More Settings** beneath the **Description** box. To find out more about each rule, select **View rule**.

### Add metrics, filters, and employee attributes

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1lda0]

1.	Under **Add metrics**, select the **Add metrics button**, then pick metrics from the **Select metrics** pane. For person-to-person queries, you’ll choose from network person-to-person metrics, which are:
    * Call Hours with External Collaborators
    * IM Hours with External Collaborators
    * Mail Hours with External Collaborators
    * Meeting Hours with External Collaborators
    * Collaboration Hours with External Collaborators
    * Meeting Count with External Collaborators
    * Mails Sent to External Collaborators
    * Calls with External Collaborators
    * Last Meeting Time
    * Last Call Time
    * Last Mail Time
    * Last IM Time

2. Under **Select filters**, select which employees’ external collaborations to analyze by setting filters using organizational attributes. 

3.	Under **Organizational data**, select the attributes—or descriptive pieces of information about employees—that you want to appear in the results along with the metrics you picked in step 1. You can use these attributes to further summarize your results.

### Run your query

After you’ve set up your query, you’re ready to run it. In the screen’s upper right, select **Run**.

## About query results

### How to access your results

After you run your query, go to the **Query results** page to check your query’s status. When your query is ready, a green checkmark appears under the **Status** column.

To download your results as a .csv file, select the CSV icon under the **Downloads** column.

### What your results show

Your query results show the duration and frequency of collaboration between an internal employee and an external collaborator (a person external to the company). 

Here’s how columns will appear in your results file: 

The first column identifies the primary collaborator, or the internal employee in the pair by providing a de-identified ID number. This column appears automatically and is titled **PrimaryCollaborator_PersonId**. 

:::image type="content" source="../images/external-collab-01.png" alt-text="Screenshot that shows the first column of results.":::

The next columns describe the primary collaborator. The column names for these attributes are the organizational attributes you selected when you built the query, with the prefix **PrimaryCollaborator_**. In the example below, the analyst selected **FunctionType**, **LevelDesignation**, and **Organization** as their attributes: 

:::image type="content" source="../images/external-collab-02.png" alt-text="Screenshot that shows the columns which describe the primary collaborator.":::

 The following column identifies the secondary collaborator, or the external person in the pair. Like the first column in the file, this column appears automatically, is titled **SecondaryCollaborator_Email**, and provides the plain text email address of the external person. 

:::image type="content" source="../images/external-collab-03.png" alt-text="Screenshot that shows the column that identifies the secondary collaborator.":::
 
The last columns in the file provide the metric date and metrics. The **MetricDate** column shows the start date of the aggregated output. This date is the first day of the month or week that your data covers. The following columns show values for the metrics you added when you built the query. 

:::image type="content" source="../images/external-collab-04.png" alt-text="Screenshot that shows the columns that provide the metric date and metrics.":::
