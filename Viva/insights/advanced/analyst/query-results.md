---
ms.date: 01/11/2023
title: Access query results and modify existing queries
description: Learn how to access query results in the advanced insights app
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

# Access query results and modify existing queries

In the advanced insights app's Analyst experience, the **Query results** page lists all the results available for your organization. In addition to seeing basic information about each query, use this page to:

* Create a copy of (clone) a query.
* Edit, rename, and delete a query.
* Favorite a query to find it later.
* Download query results as a .csv file.
* Get a link to access results as data in Power BI or Excel.

This article talks about each of these capabilities, and it also provides some information about permissions and your downloaded query results file.

## Permissions

To view, download, rename, edit, delete, favorite, or clone query results, you need to have the **Insights Analyst** role assigned.

>[!Important]
>Only the analyst who originally ran the query can edit, rename, or delete its results. Other analysts in the organization can view, favorite, and clone results.

## To use the query results page

### Results statuses

After you run your query, you might see a few different statuses in the **Status** column.

#### Running

A blue square within a blue circle means that the query is running. The analyst who ran the query can cancel the query by selecting **Stop**.

#### Stop, Stopping, and Stopped

Selecting this blue circle (**Stop** when hovered over) freezes the query. While stopping is in progress, the query status shows **Stopping**; after the query is fully stopped, the status shows **Stopped**. If the analyst who ran the query wants to run this query again later, they can select **Rerun** from the **More options** menu.

:::image type="content" source="../images/query-results-stop.png" alt-text="Screenshot that shows query statuses 'Stop,' 'Stopping...', and 'Stopped.'":::

>[!Note]
>Other analysts in the organization can see a query is running, but they aren't able to stop it.

#### Success

When a query successfully runs, you’ll see a green checkmark within a green circle labeled **Success**. If you ran the query, you can now edit, delete, or rename it. All other analysts can now clone or favorite it.

:::image type="content" source="../images/query-results-status-success.png" alt-text="Screenshot that shows a query's Success status.":::

#### Failed

If an error occurs while a query is running, you’ll see a **Failed** status. 

:::image type="content" source="../images/query-results-status-failed2.png" alt-text="Screenshot that shows a query's Failed status.":::

### Results filters

#### Predefined filters

There are some predefined views on the **Query results** page:

* **My results** – Queries only you’ve run
* **All results** – Queries all analysts in your organization have run
* **Favorites** – Queries you’ve marked as **Favorite**
* **Power BI templates** – Predefined queries all analysts in your organization have run for Power BI templates (for example, Ways of working)
* **Custom queries** – Custom person queries all analysts in your organization have run

#### Content filters

In addition to predefined results filters, you can also add a custom content filter. With a content filter, narrow results by who ran the query, which Power BI template it's for, whether auto-refresh is on, and query type.

To access content filters, select the **+** icon to the right of the **Custom queries** filter button. 

:::image type="content" source="../images/query-results-add-content-filter.png" alt-text="Screenshot that shows the five content filters with the add button highlighted.":::


Then, use the dropdown menus to select your filter.

:::image type="content" source="../images/query-results-select-content-filter.png" alt-text="Screenshot that shows the new content filter button selected and the Power BI templates option expanded below.":::

While you can only use one content filter active at a time, you can have up to five filters available. Filters won’t carry over from one session to the next.

### Setting the query to auto-refresh

If you ran a query and want it to recur on a certain schedule, you can set the **Auto-Refresh** toggle key to **On**. Analysts who didn’t run a query can’t turn on auto-refresh for it.

### More options

When you select the **More options** ellipses—located in the far-right column of the **Query results** page—you’ll see a few different options based on whether you ran the query or are another analyst in the organization: **Edit query name**, **Edit query**, **Clone query**, **Favorite**, and **Delete query**.

:::image type="content" source="../images/query-results-contextual-menu.png" alt-text="Screenshot that shows the More options contextual menu.":::

Let’s explore these options in more detail.

#### Edit query name

*Applies to: analyst who ran the query*

To change a query name, select the **Edit query name** option. After you’ve successfully renamed your query, you’ll receive a notification in the upper right corner of your screen.

>[!Important]
>All query names need to be unique. You’ll receive an error if the query name you enter already exists.

#### View query

*Applies to: any analyst in the organization*

If you want to see how a query was set up, but don't want to edit anything, select **View query**. This option takes you to the query's setup screen. You can clone a query from here, too.

#### Edit query

*Applies to: analyst who ran the query*

If you want to change your query’s setup information (like **Query name** and **Time period**), metrics, conditions and condition groups, and employee attributes, edit the query and run it again. When you select **Edit query**, you’re prompted to confirm whether you want to overwrite your existing results or want to clone the query instead. If you select **Edit query** in this box, the app takes you to the query setup screen, where you can then make changes and rerun the original query. If you choose **Clone**, the app takes you to a new query setup screen with the same settings as the original.

>[!Caution]
>The **Edit query** option permanently deletes and replaces the query’s existing results. To keep a query’s existing results, use the **Clone option** instead and make changes in a new query.

#### Clone query

*Applies to: any analyst in the organization*

The **Clone** option makes an identical copy of an existing query. Use **Clone** when you want to start a new query using the same settings (**Time period**, **Group by**, metrics, conditions and condition groups, and employee attributes) as an existing query.

>[!Tip]
>
>You can reach the **Edit** and **Clone** options through the query setup screen, too.

#### Favorite query

*Applies to: any analyst in the organization*

Favoriting a query saves it in your **Favorites** view so you can find it later. 

#### Delete query

*Applies to: analyst who ran the query*

Deleting a query removes it from the results list for everyone in the organization. After you select **Delete query**, you’ll need to confirm you’re ready to delete before proceeding. After your query is deleted, you’ll receive a notification in the upper right corner of your screen.

>[!Caution]
>Deleting queries is permanent. If you delete a query that’s set to auto-refresh, you’re also disabling that query’s future updates.



## To access query results

### About query results

When you define a query, you select metrics and employee attributes. After the query runs, its results are organized into columns and rows. The column headers in the results match the attribute names and metric names that you selected while defining the query. To learn how to download these results, read on.

#### Downloading and connecting to results

##### Download and import results in Excel

1.	In **Query results**, next to the results you want, select the CSV icon.
2.	Select to open and right-click the zip file, which contains a .csv version of the data, and then select **Extract All** and extract the .csv to a local folder.
3. Open the extracted .csv file using Excel. 

    Here's an example of a results file:

Here's an example of a results file:

:::image type="content" source="../images/query-csv-output.png" alt-text="Screenshot that an example .csv results file.":::


##### Connect through the Power BI Connector

1.	In Power BI Desktop, select **Get Data**.
2.	Select **Online Services**, select **Viva Insights**, and then select **Connect**.
3.	In the **Analyst > Query results** page, find your query and select **Copy link**.
    >[!Note]
    >The link contains two pieces of information: the partition identifier and the query identifier, which are separated by a slash.

4.	In **Connect to Viva Insights Data**, enter the partition identifier and the query identifier.

    >[!Note]
    >Query name isn't supported right now.

5.	In **Advanced parameters > Data granularity**, select **Row-level data**.
6.	Select **Import** under **Data Connectivity mode**, and then select **OK**. 
7.	If you're prompted to sign in, select **Sign in**, enter your Microsoft 365 credentials, and then select **Connect**.
8.	In the preview window, select **Load**. Optionally, select **Transform Data** to transform and shape the data in the Power Query editor before loading it into Power BI.

>[!Note]
>Have a question about your query results? Our [Query results FAQ](query-results-faq.md) article might have the answer you're looking for.

## Related topics

[Query results FAQ](query-results-faq.md)

[Power BI tips, FAQ, and troubleshooting](./templates/power-bi-faq-troubleshoot.md)

[User roles in Viva Insights](../setup-maint/user-roles.md)
