---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Process Explorer Azure Template for Workplace Analytics 
description: Learn about the Process Explorer Azure Template for Workplace Analytics and how to use it
author: madehmer
ms.author: v-midehm
ms.date: 05/03/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Process Explorer Azure Template for Workplace Analytics

_These templates are only available as part of a Microsoft service engagement._

Workplace Analytics Azure Templates includes the Process Explorer template that helps you understand where your organization or team is investing or expending valuable time.

You can use this template to categorize processes, projects, meetings, and other activities. You can either upload a .csv dataset for meeting activity or connect to a blob storage location for meeting and email activity.

After you upload a dataset, you can use template tools to categorize a good sample of meetings into the specified categories. The template will then auto-categorize all of the meetings based on that sample. After categorizing meetings, you can view meeting and email data based on those categories with visual charts and lists, as shown in the following graphics. 

You can also select **Refine Analysis** to create a copy of the selected analysis and add one or more new categories for more in-depth analysis focused on a subset of the data.
   ![Process Explorer graphical analysis](./images/pexp-analysis.png)

   ![Process Explorer visual list](./images/pexp-analysis-a.png)

You can use the query builder to view word clouds and view the list of words that are close to matching the category name in the meetings data, which can help you decide what categories to add for analysis. 



## To add a new dataset

1. In Workplace Analytics Azure Templates, select **Process Explorer**.
2. Select **Add New Dataset** (top right).
3. For **Select Dataset Type**, select either a .csv file to upload or a blob storage location, and then select **Next**. You can use a .csv file to upload meeting data or if you want to upload email and meeting data, use the blob storage option.

   ![Select a dataset type](./images/process-explorer.png)

4. Type a dataset name, locate and select the .csv file or blob storage location, and then select **Upload Dataset** (.csv) or **Run** (blob storage).
5. When prompted, select **OK**. The upload will take a few minutes to complete.
6. After the upload succeeds, the list will include this new dataset.

## To add categories for analysis

1. On the **Process Explorer** page, select the dataset name from the list.
2. For new datasets, you're prompted to enter a classification title and set the probability threshold for the first category. The threshold option is to set how likely a meeting must be in a category before it's automatically assigned to that category. Each dataset requires at least one category for analysis, which is how you want to categorize the meetings.
3. Type a new category to add to the end of the list or select **Add New Categorization** to add additional categories for analysis.

   ![Auto-classify the dataset](./images/process-explorer-auto-classify.png)

4. Follow the steps in the next section to use the query builder.

## Query builder

1. On the **Process Explorer** page, select the dataset name from the list.
2. On the analysis page, you can select:

   * The analysis name from the list to view its details
   * The **dataset parameters** icon to view the parameter details
   * The **information** (i) icon to view the job details
   * The **delete** icon to remove the analysis from the list

3. On the analysis details page, depending on the dataset (blob storage or .csv), you can do one or more of the following:

   * Type a new category to add at the end of the category list.
   * Hover your cursor over the category in the list to view and select the **delete** icon to remove it.
   * Select **Refine Analysis** to create a copy of the selected analysis and add one or more new categories for more in-depth analysis focused on a subset of the data.
   * Select **Open Query Builder** to create a query with the dataset.

4. In **Query Builder** > **Discover Topics**, you can create a query based on keywords in meeting subjects or titles, enter one or more keywords, separated by commas, in one of the **Keyword** boxes.

     ![Process Explorer Word Cloud](./images/pexp-word-cloud.png)

   * To search for word phrases, separate the phrase with an underline (for example **budget_manager**).
   * To search for word phrases in any order, separate the words with spaces (for example **budget finance manager**).
   * Use **Keywords OR** to include titles with words that contain any of the words entered or any combination of these words (phrases separated with spaces).
   * Use **Keywords NOT** to exclude titles with these words from the search and data analysis.
   * Use **Filter Meetings** to filter by analyst and/or model, and by one or more categories, such as budget, as shown in this graphic. You can also adjust the probability range to filter by for the word cloud and meeting list.

     ![Process Explorer filter options](./images/pexp-filter-options.png)

5. Select **Run query**.
6. After a query is created and the query data is listed, you can:

     * Select the category from the list, and then select the check box next to each meeting that you want to include in that category. This will help train the system for auto-categorization of the whole dataset. 
     * Select the check box for any uncategorized meetings or emails, select a category, and then select **Apply** to add them to that category.

       ![Assign a category to an uncategorized meeting](./images/pexp-assign-category.png)

   * After you categorize a good sample of related meetings, you can select **auto-categorize** and the template will automatically assign a category to in the whole dataset for meetings and email (for blob storage).
8. You can then select to export the query as a .csv file for further analysis.

## Related topics

* [Workplace Analytics Azure Templates overview](./overview.md)
* [Deploy and configure Workplace Analytics Azure Templates](./deploy-configure.md)