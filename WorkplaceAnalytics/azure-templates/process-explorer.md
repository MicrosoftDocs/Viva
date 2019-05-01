---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Process Explorer Azure Template for Workplace Analytics 
description: Learn about the Process Explorer Azure Template for Workplace Analytics and how to use it
author: madehmer
ms.author: v-midehm
ms.date: 05/01/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Process Explorer Azure Template for Workplace Analytics

_These templates are only available as part of a Microsoft service engagement._

Workplace Analytics Azure Templates includes the Process Explorer template that helps you understand where your organization or team is investing or expending valuable time. You can use this template to categorize processes, projects, meetings, and other activities. You can either upload a .csv dataset for meeting activity or a dataset from a blob storage location meeting and email activity.  

## To add a new dataset

1. In Workplace Analytics Azure Templates, select **Process Explorer**.
2. Select **Add New Dataset** (top right).
3. For **Select Dataset Type**, select either a .csv file to upload or a blob storage location, and then select **Next**. You can use a .csv file to upload meeting data or if you want to upload email and meeting data, use the blob storage option.

   ![Select a dataset type](./images/process-explorer.png)

4. Type a dataset name, locate and select the .csv file or blob storage location, and then select **Upload Dataset** (.csv) or **Run** (blob storage).
5. When prompted, select **OK**. The upload will take a few minutes to complete.
6. After the upload succeeds, the dataset list will include this new one.

## To add categories for analysis

1. On the **Process Explorer** page, select the dataset name from the list.
2. For new datasets, you're prompted to enter a classification title and set the probability threshold for the first category. Each dataset requires at least one category for analysis, which is how you want to categorize the meetings and/or emails by.
3. Type a new category to add at the end of the list or select **Add New Categorization** to add additional categories for analysis.

   ![Auto-classify the dataset](./images/process-explorer-auto-classify.png)

4. The meetings or emails in this dataset are listed below the list of categories. To help train the template to auto-classify or auto-categorize meetings/emails for current and future analysis, select the category from the list, and then select the check box next to each meeting or email that you want to include in that category.
5. After a complete sample of related emails/meetings are selected, select **Apply**, and then select **Auto-classify** and the template will use this sample selection to more accurately categorize the whole dataset for current and future analysis.

## To view, create queries, and export analysis

1. On the **Process Explorer** page, select the dataset name from the list.
2. Select the analysis name from the list.
3. On the analysis page:
   * Select **Open Query Builder** to create a query with the dataset
   * Type a new category to add at the end of the category list
   * Hover your cursor over the category in the list to view and select the **delete** icon to remove a category
4. To search for keywords in meeting and/or email subjects or titles, enter one or more keywords, separated by commas, in one of the **Keyword** boxes.

  * To search for word phrases, separate the phrase with an underline (for example **budget_manager**).
  * To search for word phrases in any order, separate the words with spaces (for example **budget finance manager**).
   * **Keywords OR** includes titles with words that contain any of the words entered or any combination of these words (phrases separated with spaces).
   * **Keywords NOT** excludes titles with these words from the search and data analysis.

5. Select **Run query**.
6. In the **Word Cloud**, you can select other keywords to add to the **Keywords OR** box, and then select **Re-run Query** to update the cloud view. For example, the following shows a word cloud for meetings and emails relating to budget.

   ![Process Explorer Word Cloud](./images/pexp-word-cloud.png)

7. You can then select to export the query as a .csv file for further analysis.

## Related topics

* [Workplace Analytics Azure Templates overview](./overview.md)
* [Deploy and configure Workplace Analytics Azure Templates](./deploy-configure.md)