---
# Metadata Sample
# required metadata

title: Power BI templates
description: Use a Power BI template to run a query, export its results, and visualize them in Power BI
author: paul9955
ms.author: v-pascha
ms.date: 09/18/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Power BI templates in Workplace Analytics 

The Workplace Analytics Queries page now provides a Power BI template that analysts can use to visualize areas of collaboration overload in your organization. This template performs two tasks: it pre-populates a Workplace Analytics query and it selects the proper Power BI charts to display the results of that query. 

**To use the Collaboration overload Power BI template**

1.      In Workplace Analytics, select **Solutions**.

2.      On the Solutions page, notice the template query card called Collaboration Overload. You can identify Power BI templates in that they display the Power BI logo in the upper-right corner:

3.      Select the Collaboration Overload query card. This opens a preset query that contains all the required metrics to properly populate the PBI template. 

4.       Review the displayed metrics. If you notice a metric that does not apply to your analysis, you can select the delete icon (trash can) to delete it. 

> [!Note] 
> Attempting to delete a metric displays a warning that this deletion could disable portions of the Power BI template and reduce query results, which in turn can limit your eventual ability to visualize collaboration-overload patterns. Depending on the metric you delete, you might disable a single Power BI chart, several charts, or all of the possible charts. In the warning dialog box, select **cancel** to retain the metric or **delete** to delete it.  

5.       Select **Run**. This opens the Query &gt; Results page. This page displays a row for every run of a query, including the
query that you just ran.

6.       Select the download (down-arrow) icon. This lets you choose what to download, a CSV file or a Power BI template: 

7.       Select **PBI template**. This displays a dialog
box that informs you that the OData link for this query has been copied to the clipboard. You will use this OData link in Power BI. 

8.       Select **OK** to dismiss the dialog box. The
Power BI template query results file is now downloaded. 

9.       In your browser, select the downloaded Power BI template query results file to open it:

10.         If a dialog box prompts you to select a program,
choose **Power BI**:

11.       The Power BI template query results file opens in Power BI. You are prompted to paste the OData link:

12.       Paste the OData link and select **Load**. It could take several minutes or more to open the data display in Power BI. After the data loads, Power BI displays it in charts that provide visualization into your organization’s collaboration patterns: 

## Available Power BI templates
Workplace Analytics makes the following query templates available for use with Power BI:
  * Collaboration overload 