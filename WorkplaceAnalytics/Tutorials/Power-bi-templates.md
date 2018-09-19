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

1.      Open the [Workplace Analytics](https://workplaceanalytics.office.com) Home page. If prompted, enter your Microsoft credentials.

2.      In the left navigation pane, select **Queries**.

3.      On the Queries page, notice the template query card called Collaboration Overload. You can identify Power BI templates in that they display the Power BI logo in the upper-right corner:

   ![Power BI logo in query card](../Images/WpA/tutorials/pbi-templates-01.png)

4.      Select the Collaboration Overload query card. This opens a preset query that contains all the required metrics to properly populate the PBI template. 

   ![Opened Power BI template query](../Images/WpA/tutorials/pbi-templates-02.png)

5.       Review the displayed metrics. These metrics are required to populate the Power BI template. 

   > [!Note] 
   > Attempting to delete a metric displays a warning that this deletion could disable portions of the Power BI template and reduce query results, which in turn can limit your eventual ability to visualize collaboration-overload patterns. Depending on the metric you delete, you might disable a single Power BI chart, several charts, or all of the possible charts. In the warning dialog box, select **cancel** to retain the metric or **delete** to delete it.  

6.       Select **Run**. This opens the Query &gt; Results page. This page displays a row for every run of a query, including the query that you just ran.

7.       Select the download (down-arrow) icon. This lets you choose what to download, a CSV file or a Power BI template: 

   ![Select PBI template](../Images/WpA/tutorials/pbi-templates-03.png)

8.       Select **PBI template**. This displays a dialog box that informs you that the OData link for this query has been copied to the clipboard. You will use this OData link in Power BI. 

<!-- REMOVING this for now. It shows typos that are in the UI. Perhaps include this after they've been fixed in the product.  

   ![OData link has been copied](../Images/WpA/tutorials/pbi-templates-04.png)
-->

9.       Select **OK** to dismiss the dialog box. The Power BI template query results file is now downloaded. 

10.       In your browser, select the downloaded Power BI template query results file to open it:

   ![Open downloaded Power BI template file](../Images/WpA/tutorials/pbi-templates-05.png)

11.         If a dialog box prompts you to select a program, choose **Power BI**:

   ![How to open this file type?](../Images/WpA/tutorials/pbi-templates-06.png)

12.       The Power BI template query results file opens in Power BI. You are prompted to paste the OData link:

   ![Paste OData link here](../Images/WpA/tutorials/pbi-templates-07.png)

13.       Paste the OData link and select **Load**. It could take several minutes or more to open the data display in Power BI. After the data loads, Power BI displays it in charts that provide visualization into your organization’s collaboration patterns: 

   ![Results visualized in Power BI](../Images/WpA/tutorials/pbi-templates-08.png)

