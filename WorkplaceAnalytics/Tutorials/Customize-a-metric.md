---
# Metadata Sample
# required metadata

title: Customize a base metric in a Workplace Analytics query
description: How to customize and change a base metric in a Workplace Analytics query. 
author: paul9955
ms.author: v-pascha
ms.date: 07/16/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Customize a base metric in a query

Analysts create queries to determine workplace patterns and behaviors. An important step in the creation of a query is the selection of a metric. This defines the area of focus of the query. 

As an analyst, you select metrics as you build queries. The metrics that you see on the page for building a query are "base metrics"; this means that when you first select one, it appears in a simple, unfiltered form, such as "email hours." 

## Work with metrics in a query

You can change metric use within a query in three ways: customize a base metric, change a base metric, and add more base metrics. 

### Customize the base metric 

After you select a metric you can _customize_ it. A customized metric produces more refined results used in the query. You customize a metric by applying filters to it. Although you do this on the query-builder page, these filters apply only to the metric and function independently from any filters that you apply to the query itself. 

Example: You might start with the base metric "Email hours." You can customize it so that it becomes the more targeted metric: "Email hours where at least all attendee's and/or recipient's FunctionType equals R&D."  

### Change the base metric

You can also change the base metric. This means swapping it out, selecting a different base metric to use in place of the one that you chose originally.

#### Customizations are retained when you change the base metric

In our example, you customized the "Email hours" base metric to become "Email hours where at least all attendee's and/or recipient's FunctionType equals R&D." 

Now, after you have applied a customization, you _change_ the base metric from "Email hours" to "Total emails sent during meeting." 

This change gives you a new metric that has kept the same customization. Your final, customized metric becomes: "Total emails sent during meeting where at least all attendee's and/or recipient's FunctionType equals R&D."

In other words, the customization that you applied to the original base metric was not lost when you changed from the that base metric to a different base metric. 

### Add more base metrics

You can also add more base metrics to your query. You would do this to modify the area of focus of the query. 

## Walkthrough: Customize and change a base metric

In the following steps, you first customize and then change a base metric. 

1. Open [Workplace Analytics](https://workplaceanalytics.office.com). If prompted, enter your Microsoft credentials.

2. Select **Queries** and then select the type of query you want to create: Person query or Meeting query. (You can customize metrics only when working in a Person query or Meeting query.)

3. Type a name for the query, and optionally, type a description.

4. Select a date range and a meeting exclusions rule. 

5. Add the base metric: In the Metrics area, click the (+) sign next to Add metric and then select a metric from the list:
 
   ![select a metric](../Images/WpA/Tutorials/custom-metric-01.png)

   > [!Note] 
   > You can select more than one metric from the list. When you are finished, click elsewhere on the page to close the list. 

   In this example, we will select only one metric, **Conflicting meeting hours**:

   ![selected metric](../Images/WpA/Tutorials/custom-metric-02.png)

   The metric you select becomes the _base metric_ for the query. It represents the area of focus for the analysis that you will carry out. 

6. Customize the metric. To do this, follow these steps:

   a. Select the edit icon (![edit icon](../Images/WpA/Tutorials/edit-icon.png)). This displays the option to apply filters to the base metric: 

   ![selected metric](../Images/WpA/Tutorials/custom-metric-03.png)

   b. Select the (+) sign next to **Add filter**. A filter is added. In our example, it's the Initiator filter:
   
   ![selected metric](../Images/WpA/Tutorials/custom-metric-04.png)

   c. Click the filter name -- in this case, **Initiator**. This displays options for defining filters about email initiators. 

   ![selected metric](../Images/WpA/Tutorials/custom-metric-05.png)

   d. Define the filter by adding details in the three boxes. Optionally, define other filters (if others are available) by clicking AND or OR and adding details to the additional filters.

   e. When you are finished customizing the metric (adding filters), select the **confirm** option at the right side of the page. 

   You have now added a base metric and customized it. 

7. Optionally, you can now change the base metric to a different one. To do this, follow these steps:

    * Select the drop-down arrow that is displayed next to the name of the base metric, and then select the name of a different metric. This changes the metric to the new selection.
   
   >[!Note] 
     * Any base metric that can be changed displays a drop-down menu whose options represent the possible changes.
     * Not all base metrics can be changed. If no drop-down menu is available, this metric cannot be changed. 
     * Changes are not always 1-1. For example, you can change from Conflicting meeting hours to Email hours, but, due to variations in the available filters, the opposite change is not possible.

   If you select a new base metric for which the filter options are identical, the metric will change and you'll see no additional changes. If you select a new base metric for which the filter options are a subset, additional available filters appear. If you have edited the display name of the metric and then change the base metric, the display name that you edited is deleted.

8. After you have created or edited all the metrics you want, confirm or cancel your changes: If you select **Confirm**, all changes to the metric are saved. If you select **Cancel**, all changes are discarded (reverted to the original state). If you neither confirm nor cancel the changes, the changes are automatically confirmed.
 
9. Select **Run** to run the query. The query runs with all confirmed metrics and customizations that you have applied. 