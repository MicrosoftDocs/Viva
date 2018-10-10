---
# Metadata Sample
# required metadata

title: Power BI templates
description: Use a Power BI template to run a query, export its results, and visualize them in Power BI
author: paul9955
ms.author: v-pascha
ms.date: 10/09/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Power BI templates in Workplace Analytics 

Workplace Analytics provides Power BI templates that analysts can use to visualize aspects of workplace patterns and trends. A Power BI template performs two tasks: it pre-populates a custom Workplace Analytics query and it selects the proper Power BI charts to display the results of that query. 

The Queries page of Workplace Analytics makes a number of query templates available. On this page, you can identify Power BI templates in that they display the Power BI logo in the upper-right corner:

   ![Power BI logo in query card](../Images/WpA/tutorials/two-pbi-cards.png)

In the following example procedure, you will use the Collaboration Overload query to identify areas of collaboration overload in your organization. 

**To use a Power BI template**

1.  Open the [Workplace Analytics](https://workplaceanalytics.office.com) Home page. If prompted, enter your Microsoft credentials.

2.  In the left navigation pane, select **Queries**.

3.  On the Queries page, select the **Collaboration Overload** query card. This opens a preset query that contains all the required metrics to properly populate the Power BI template. 

   ![Opened Power BI template query](../Images/WpA/tutorials/pbi-templates-02.png)
   
4.  Review the displayed metrics. These metrics are required to populate the Power BI template. 

   > [!Note] 
   > If you attempt to delete a metric, you'll see a warning that this deletion could disable portions of the Power BI template and reduce query results. In turn, this could limit your eventual ability to visualize collaboration-overload patterns. Depending on the metric you delete, you might disable a single Power BI chart, several charts, or all of the possible charts. In the warning dialog box, select **cancel** to retain the metric or **delete** to delete it.  
  
5.  Select a rule from the Meeting exclusions list. Optionally, select options for Group by, Time period, and Included employees.  

6.  Select **Run**. The query might take several minutes to complete.

7.  Open the Query &gt; Results page. The Results page displays a row for every run of a query, including the query that you just ran. If your query is still running, this row displays the status as "running": 

   ![Query is still running](../Images/WpA/tutorials/query-running.png)

 If the query has finished running, its row displays the download (down-arrow) button:

   ![Query results are ready](../Images/WpA/tutorials/query-results-done.png)
 
8.  Select download. This gives you a choice of what to download, a CSV file or a Power BI template: 

   ![Select PBI template](../Images/WpA/tutorials/pbi-templates-03.png)

9.  Select **PBI template**. This displays a dialog box that informs you that the OData link for this query has been copied to the clipboard. You will use this OData link in Power BI. 

10.  Select **OK** to dismiss the dialog box. The Power BI template query results file is now downloaded. 

11.  In your browser, select the downloaded Power BI template query results file to open it:

   ![Open downloaded Power BI template file](../Images/WpA/tutorials/pbi-templates-05.png)

12.  If a dialog box prompts you to select a program, choose **Power BI**.

13.  The query results file opens in Power BI. You are prompted to paste the OData link:

   ![Paste OData link here](../Images/WpA/tutorials/pbi-templates-07.png)

   Paste the OData link and select **Load**. 

14.  If you are already logged in to Power BI with your Workplace Analytics organizational account, your data loads and Power BI displays your visualizations. <i>Skip the rest of this procedure.</i> 
   
   If you are not logged in to Power BI with your Workplace Analytics organizational account, you will see the OData feed dialog box. Its left panel highlights the account that is currently selected for signing in to Power BI. For example, the following illustration shows "Anonymous" as the sign-in account:
   
   ![Anonymous account displayed](../Images/WpA/tutorials/anon-access-to-pbi.png)   

   > [!Important] 
   > You can view Workplace Analytics data (including query results) in Power BI only if you've been assigned the Analyst role in Workplace Analytics. Also, you must sign in with the correct account. You will do this in the following steps. 

15.  In the OData feed dialog box, select **Organizational account**.

16.  If the dialog box notifies you that you are not signed in, select **Sign in**.

17.  In the Office 365 dialog box, select the organizational account that you use to log in to Workplace Analytics. This signs you in to Power BI and displays the OData feed dialog box, with the notification "You are currently signed in":      
   
   ![You are signed in](../Images/WpA/tutorials/you-are-signed-in.png)

18.  Select **Connect**. A "Refresh" dialog box displays the status of the preparation of your data for display. It could take several minutes or more for Power BI to display your data.  

After the data loads, Power BI displays it in charts that provide visualization into your organization’s collaboration patterns: 

   ![Results visualized in Power BI](../Images/WpA/tutorials/pbi-templates-08a.png)

### Related topics

[View, download, and export query results](../use/view-download-and-export-query-results.md)