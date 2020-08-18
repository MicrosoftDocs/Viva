---

title: Collaboration overload dashboard
description: Use the Collaboration overload dashboard to visualize analyze Workplace Analytics data in Power BI
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Collaboration overload

The Collaboration overload dashboard uses a Power BI template that’s populated by Workplace Analytics data to identify areas of collaboration overload in your organization. The metrics in this dashboard show where overall collaboration patterns, time fragmentation, or meeting quality could be improved.

* **Collaboration Hours by Level** - Shows the collaboration patterns in your organization for the different roles and levels. Viewing these patterns by level can give you the detail and granularity necessary to identify key trends that can be addressed.
* **Meeting Quality Deep Dive** - The charts provide insights about meetings, such as multitasking, double-booked meetings, and redundancy, that could be impacting overall meeting quality throughout your organization.

To populate the dashboard in Power BI, you must set up and successfully run the predefined **Collaboration overload** query in Workplace Analytics.

## Prerequisites

Before you can run the query and populate the dashboard in Power BI, you must:

* Be assigned the role of [Analyst](../use/user-roles.md) in Workplace Analytics.
* Have the latest version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t?activetab=pivot:overviewtab) to download and install the latest version.

## Set up the dashboard

1. In Workplace Analytics, select **Analyze** > **Queries**.
2. Select **Collaboration overload** to open this predefined query, which has all the required metrics to populate the Power BI template.
3. Select or confirm the options for **Group by**, **Time period**, and **Meeting exclusions**.
4. In **Select metrics**, review and select the metrics to include, which are required to populate the Power BI dashboard.
5. In **Select filters**, you can optionally select to filter the data.
6. In **Organizational data**, you can select what columns to include.
7. Select **Run** (at top right). The query might take several minutes up to several hours to complete.
8. After the query successfully runs, in **Queries** > **Results**, select the **Download** icon for the **Collaboration overload** query results, select **PBI template**, and then select **OK** to download the template.
9. In your browser, select the downloaded Power BI template query results file to open it.

    ![Open downloaded Power BI template file](../Images/WpA/tutorials/pbi-templates-05.png)

10. If prompted to select a program, select **Power BI Desktop**.
11. When prompted, paste the OData link from the query results in Workplace Analytics, and then select **Load**.

    ![Paste OData link here](../Images/WpA/tutorials/pbi-templates-07.png)

12. If you are already logged in to Power BI with your Workplace Analytics organizational account, your data loads and Power BI uses visualization charts to show your data. You are done and can _skip the following steps_.

    If you are not logged in to Power BI, you'll see the current sign-in account highlighted in Power BI. For example, the following shows "Anonymous" as the sign-in account.

    ![Anonymous account displayed](../Images/WpA/tutorials/anon-access-to-pbi.png)

    > [!Important]
    > You can view Workplace Analytics data (including query results) in Power BI only if you've been assigned the Analyst role in Workplace Analytics. Also, you must sign in with the correct account with the following steps.

13. In the **OData feed** dialog box, select **Organizational account**.
14. If prompted, select **Sign in**.
15. In the **Office 365** dialog box, select the organizational account that you use to log in to Workplace Analytics. The **OData feed** dialog box shows "you are currently signed in" to Power BI:

    ![You are signed in](../Images/WpA/tutorials/you-are-signed-in.png)

16. Select **Connect** to show the status of the data preparation, which might take several minutes up to several hours to load. After the data loads, Power BI uses visualization charts to show your organization's collaboration patterns.

    ![Results visualized in Power BI](../Images/WpA/tutorials/pbi-templates-08a.png)

## Power BI tips, troubleshooting, and FAQs

For details about how to share the dashboard and other Power BI tips, troubleshoot any issues, or review the most frequently asked questions, see [Power BI templates in Workplace Analytics](../tutorials/power-bi-templates.md).

## Related topic

[View, download, and export query results](../use/view-download-and-export-query-results.md)
