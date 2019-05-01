---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Process Explorer Azure Template for Workplace Analytics 
description: Learn about the Process Explorer Azure Template for Workplace Analytics and how to use it
author: madehmer
ms.author: v-midehm
ms.date: 04/25/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Process Explorer Azure Template for Workplace Analytics

_These templates are only available as part of a Microsoft service engagement._

Workplace Analytics Azure Templates includes the Process Explorer template that helps you understand where your organization or team is investing or expending valuable time. You can use this template to categorize processes, projects, meetings, and other activities.

## To add a new dataset

1. In Workplace Analytics Azure Templates, select **Process Explorer**.
2. Select **Add New Dataset** (top right).
3. For **Select Dataset Type**, select either a .csv file to upload or a blob storage location.

   ![Select a dataset type](./images/process-explorer.png)

4. When prompted, select OK. The upload will take a few minutes to complete.
5. After the upload succeeds, the dataset list will include this new dataset.

## To add categories for analysis

1. On the **Process Explorer** page, select the dataset name from the list.
2. For new datasets, you're prompted to enter a classification title and set the probability threshold for the first category. Each dataset requires at least one category for analysis.
3. If prompted, you can select to either auto-classify or auto-categorize the dataset. You can also type a new category to add at the end of the list or select **Add New Categorization** to add additional categories for analysis.

   ![Auto-classify the dataset](./images/process-explorer-auto-classify.png)

## To view analysis

1. On the **Process Explorer** page, select the dataset name from the list.
2. Select the analysis name from the list.
3. Select **Open Query Builder** to query the dataset. You can also select:
   * Type a new category to add at the end of the category list
   * The **dataset parameters** icon to view parameter details
   * The **information** (i) icon to view the job details
   * Hover your cursor over the category in the list to view and select the **delete** icon to remove a category
4. To search for keywords in meeting subjects or titles, enter one or more keywords, separated by commas, in one of the **Keyword** boxes. To search for word phrases, separate the phrase with an underline (for example **product_marketing**). Or to search for word phrases in any order, separate the words with spaces (for example **product marketing managers**)
   * **Keywords OR**: Includes meeting titles with words that contain any of the words entered or any combination of these words (phrases separated with spaces).
   * **Keywords NOT**: Meeting titles with these words are excluded from the search and data analysis.
5. Select **Run query**.
6. In the **Word Cloud**, you can select other keywords to add to the **Keywords OR** box, and then select **Run query** again to update the cloud view to include the additional words you added, as shown in the following graphic.

   ![Process Explorer Word Cloud](./images/pexp-word-cloud.png)

7. You can then select to export the query as a .csv file.

## Related topics

* [Workplace Analytics Azure Templates overview](./overview.md)
* [Deploy and configure Workplace Analytics Azure Templates](./deploy-configure.md)