---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Process Explorer Azure Template for Workplace Analytics 
description: Learn about the Process Explorer Azure Template for Workplace Analytics and how to use it
author: madehmer
ms.author: v-midehm
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

You can use Process Explorer to categorize processes, projects, meetings, and other activities. You can either upload a .csv dataset to analyze meeting activity or connect to a blob (cloud) storage location to analyze meeting and email activity.

After you upload a dataset, you can use the Query Builder to help you decide what categories to add for analysis. You can select category names or phrases from the word cloud to view those meetings and then categorize them in the dashboard view.

After you categorize a good sample of meetings into the specified categories:

* You can view meeting data based on those categories with visual charts and lists.
* For a .csv dataset, you can select to auto-categorize the full dataset based on the sample meeting categorizations already done by you, as the analyst.
* For a blob storage dataset, the categorization options depend on what the template's admin settings are for email activity:
  
  * If email categorization is enabled, you'll use both the Meeting and Email category pages to manually categorize meeting and email activity separately, which better trains the model for auto-categorizing the full dataset.
  * If no Email category page is shown, you'll only see and use the Meeting category page to manually categorize meetings, which creates distinct models for the two types of content and more accurate overall results.

* You can also use the **Refine Categorization** option to create a copy of the selected analysis and add or change the categories for more in-depth analyses.

## To add a new dataset

Use the following steps to add either a .csv dataset for meeting data analysis or a blob storage dataset for analyzing both meeting and email data.

1. In Workplace Analytics Azure Templates, select **Process Explorer**.
2. Select **Add New Dataset** (top right).
3. For **Select Dataset Type**, select either to upload meeting query output (.csv) to analyze or to connect and classify raw meeting and email data (blob storage), and then select **Next**.

   ![Select a dataset type](./images/pexp-new-dataset.png)

4. What you do next depends on which dataset type you selected:

   * For meeting query output, enter a dataset name, locate and select the dataset file path, and then select **Upload Dataset**.
   * For the raw data option, enter a dataset name, locate and select the path to the dataset, and select the time range to analyze. You can then optionally select any applicable filters to reduce the dataset to use to manually categorize for model training purposes, and then select **Submit**.

5. The dataset upload takes a few minutes to complete depending on the size of the dataset. The name and source for the new dataset will show in the table with the following information and available actions.

   * When the **Status** changes to a green check mark, you can select the dataset to view existing categorizations or add new categorizations.
   * Select the **Job Details** (i) icon next to **Status** to view the job details.
   * Select a table column heading, such as **Name** or **Submitted**, to sort by it.
   * Select the **Parameters** icon to view the parameter details for a listed dataset.
   * Select the **Delete Dataset** (trashcan) icon to delete it from the list.
   * If the dataset fails with a **Status** of a red X, you can select the **Undo** icon to revert to the last successfully saved version of the dataset.

## To categorize meetings for analysis

Use the following steps to manually categorize meetings for both dataset types. Meetings must be categorized for either meeting query output or blob storage data.

1. On the **Process Explorer** page, select the dataset name from the list.
2. What you do next depends on the dataset.

   * **For new datasets**, you're prompted to enter:
      * **Categorization Title** - Each dataset requires at least one category for analysis, which is how you want to categorize the meetings.
      **Probability Threshold** - The threshold option is how likely a meeting must be in a category before it's automatically assigned to that category.
      **Create a new categorization model or use a saved model** - The model option enables you to save time by using an existing training model that you saved while categorizing similar data with the query builder.

   * **For existing datasets**, you can select:

     * **Add New Categorization** and then enter a title, a probability threshold, and then select to either create a new model or use a saved model, same as with new datasets.
     * The name of an *existing draft categorization* to resume work on it.
     * Select the row with the name of an *existing categorization*, and then select **Add New Categorization** to make a copy of it to work from.

3. Each dataset requires at least one category for analysis, which is how you want to categorize the meetings. In **Dashboard** > **Add a New Category**, enter the name of a category you want to add, and then press **Enter** to add it to the list.
4. Select **Meeting** > **Open Query Builder** > **Discover Topics**, enter one or more keywords, separated by commas, in one of the applicable **Keyword** boxes to view meetings with these keywords, and then select **Run query**. You can also select a word from the word cloud to add it as a keyword.

   ![Process Explorer Word Cloud](./images/pexp-word-cloud.png)

   * To search for word phrases, separate the phrase with an underline (for example **budget_manager**).
   * To search for word phrases in any order, separate the words with spaces (for example **budget finance manager**).
   * Use **Keywords OR** to include titles with words that contain any of the words entered or any combination of these words (phrases separated with spaces).
   * Use **Keywords NOT** to exclude titles with these words from the search and data analysis.
   * **Max Meetings to Show** to set the maximum number of meetings to include in the list or show in the word cloud.

5. In **Meeting** > **Open Query Builder** > **Filter Dataset**, you can filter the meetings shown in the list with the following options, and then select **Run Query**.

   * **Filter by Sources** to select the analyst and/or the model to filter the meetings by, which are those meetings that were categorized manually by the analyst or those categorized automatically by the model.
   * **Filter by Categories** to select one or more categories to filter the meetings by, such as budget, as shown in the following graphic.
   * **Probability Range** to adjust the minimum and maximum probability range to filter the word cloud and meeting list to include.
   * **Max Results to Show** to set how many results to show in the list.
   * **Which Meetings do you want to include in your query results?** You can select specific meetings to include or exclude from the data to categorize. For example, you could exclude meetings where the organizer is outside the filter population. Or you could only include meetings equal to or greater than one hour in the list.

   ![Process Explorer filter options](./images/pexp-meeting-query-filters.png)

6. After the data is queried, close the query builder pane to see the meeting list, and then to help train the model for auto-categorization of the whole dataset:

   * Select a category, select all meetings in the list by selecting the check box next to **Subject**, and then select **Apply** to add these meetings to that category.
   * Or select a category, individually select the check box next to a good sample of related meetings, and then select **Apply** to add them to that category.

    ![Assign a category to an uncategorized meeting](./images/pexp-categorize.png)

   * In **Dashboard** > **Add a New Category**, enter any additional categories needed for grouping the uncategorized meetings.
   * Hover the cursor over an existing category and select the **Rename Category** (pencil) icon to rename it or the **Delete Category** (trashcan) icon to delete it from the list.
   * After you categorize a good sample of related meetings for all the categories you want to evaluate:

     * Below the table on the Dashboard, select **Save Categorization Model** to save this categorization training model to reuse later. And then when creating a new dataset, or a subgroup of this dataset, you can use this same categorization training model to help you categorize the new dataset more efficiently.
     * For .csv datasets, select **Auto-Categorize Full Dataset** to categorize all of the meetings uploaded in the .csv file.
     * For blob storage datasets, select **Auto-Categorize Meetings**, and then see [Step 3 in To categorize email activity for analysis](#to-categorize-email-activity-for-analysis) for next steps to categorize email.

       ![Auto-categorize meetings](./images/pexp-auto.png)

7. To add or change categories for a categorization, such as to focus on a subset of the data, select **Refine Categorization** to create a copy of the selected analysis, and then repeat these steps to add new or change existing categories.

> [!Note]
>Use the Download option (bottom right) to download a .csv of the data shown in the dashboard table.

## Email activity analysis

By using blob storage as the data source, you can get more complete analysis based on all meeting and email activity related to the selected process categories.

Ask your admin what is set for surfacing and classifying email activity for analysis. The admin can go to **Admin** > **Configuration** > **Process Explorer** and confirm which is selected:

  ![Categorize email admin setting](./images/pexp-admin-settings.png)

For blob storage categorization, the system will limit the data used for categorizations to five million emails and meetings to improve interactivity. If you know the subset of data you want to focus on, you can set time range and/or filters to focus the data used.  If not, or if your filtering still results in more than five million values, the system will automatically choose a good representative sample from the complete filtered sample.

For a blob storage dataset, the categorization options depend of what the admin settings are for email activity:
  
* If email categorization is enabled, you'll use both the Meeting and Email category pages to manually categorize meeting and email activity separately, which better trains the model for auto-categorizing the full dataset.
* If no Email category page is shown, you'll only see and use the Meeting category page to manually categorize meetings, which trains the model for auto-categorizing the full dataset, including both meeting and email activity.

### To categorize email activity for analysis

1. If you haven't done so already, follow the steps to [add the blob storage dataset](#to-add-a-new-dataset).
2. If you haven't done so already, complete the steps [to categorize meetings](#to-categorize-meetings-for-analysis) for the blob storage dataset.
3. If no **Email** category page is shown, you can select **Auto-Categorize Full Dataset** and the template will automatically assign a category to all meetings and email in the whole dataset based on the sample meeting categorizations; this will take a few minutes or more depending on the size of the dataset.

4. If the **Email** category page is available, then you can manually  manually categorize email activity by selecting **Email** > **Query Builder** and then entering one or more keywords, separated by commas, in one of the applicable **Keyword** boxes to view email with these keywords, and then select **Run query**.

   * To search for word phrases, separate the phrase with an underline (for example **budget_manager**).
   * To search for word phrases in any order, separate the words with spaces (for example **budget finance manager**).
   * Use **Keywords OR** to include titles with words that contain any of the words entered or any combination of these words (phrases separated with spaces).
   * Use **Keywords NOT** to exclude titles with these words from the search and data analysis.
   * **Max Results to Show** to set the maximum number of email to include in the list or show in the word cloud.
   * **Which Emails do you want to include in your query results?** You can filter the email to include in or exclude from the data list to categorize. For example, you could include only email that the sender spent 10 minutes or more on.

   ![Categorize email](./images/pexp-email-query-filters.png)

5. In **Email** > **Open Query Builder** > **Filter Dataset**, you can filter the email shown in the list with the following options, and then select **Run Query**.

   * **Filter by Sources** to select the analyst and/or the model to filter the email by, which are those meetings that were categorized manually by the analyst or those categorized automatically by the model.
   * **Filter by Categories** to select one or more categories to filter the email by, such as budget, as shown in the following graphic.
   * **Probability Range** to adjust the minimum and maximum probability range to filter the word cloud and email list to include.
   * **Max Results to Show** to set how many results to show in the list.

6. After email is auto-categorized, go to **Email** > **Query Builder** > **Filter Dataset** to show those categorized by the model and confirm that you agree with the model categorizations in all the categories.

7. After confirming the model categorizations:

   * Below the table on the Dashboard, select **Save Categorization Model** to save this categorization training model to reuse later. And then when creating a new dataset, or a subgroup of this dataset, you can use this same categorization training model to help you categorize the new dataset more efficiently.
   * Select **Auto-Categorize Full Dataset** and the template will automatically assign a category to all meetings and email in the whole dataset based on the sample categorizations; this will take some time based on the size of the dataset.

8. To add or change categories for your analysis, such as to focus on a subset of the data, select **Refine Categorization** to create a copy of the selected analysis and then repeat the previous steps [to categorize meetings for analysis](#to-categorize-meetings-for-analysis) and then repeat these steps to categorize email.

You can see data about the categorized email and meetings on the dashboard. Also, you can select **Download** to save a .csv snapshot of the current data shown on the **Dashboard** page.

  ![Email activity included in the analysis](./images/pexp-dashboard.png)

## Related topics

* [Workplace Analytics Azure Templates overview](./overview.md)
* [What's new in Workplace Analytics Azure Templates](./release-notes.md)
* [Deploy and configure Workplace Analytics Azure Templates](./deploy-configure.md)
