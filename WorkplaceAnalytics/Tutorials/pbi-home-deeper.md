---

title: Power BI Home page deeper insights
description: Description and use of the Power BI Home page deep-dive dashboard
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: wpa

---

# View deeper insights in Power BI

As a business decision maker, you can see information on the Workplace Analytics **Home** page that tells you much about current work conditions and trends. By starting on that page, you can identify “opportunity groups” (groups that you might want to act on) and perform detailed analysis by using drill-down capabilities that are provided by Power BI. 

To enable these capabilities, this feature uses the Power BI Connector to combine Workplace Analytics data with the visualization capabilities of Power BI. The information that you view in Power BI remains up to date because its data is automatically refreshed with new data from Workplace Analytics. The connector also enforces privacy by preventing any user who views the report from drilling down and seeing a group smaller than the [minimum group size](../use/settings.md#minimum-group-size) specified by the Workplace Analytics admin. This lets you share reports with confidence that row-level data will not be exposed. 

To set up these visualizations, follow the steps that are described in the following walkthrough. You need not run queries nor select metrics to populate these visualizations. The metrics are preconfigured and communicated to Power BI through the Power BI connector. (For background information, see [Connect through the Power BI Connector](../use/view-download-and-export-query-results.md#connect-through-the-power-bi-connector).)

## View and publish insights in Power BI

In the following walkthrough, you will perform steps as a business decision maker who has been granted the limited analyst role in Workplace Analytics. Your interest in the employee experience at your company is heightened because you’ve become aware of employee attrition, and you want to find out what could be causing this problem. At the end of this walkthrough, you can view custom Power BI visualizations about this issue and optionally share them with team members. 

**Role:** analyst or limited analyst

1.	Open the Workplace Analytics **Home** page:

    ![Home page](../images/wpa/tutorials/new-home-page.png)
 
2.	Select the **Boost employee engagement** outcome. 

     On the **Boost employee engagement** page that appears, you see insights about various behaviors at the company. For example: 
     
     * **Prevent employee burnout** &ndash; This insight tells you what percentage of employees spend more than five hours per week working after-hours.
     
3.	You are concerned about the employee-burnout statistic (too much after-hours work) and you want to learn more. On this card, select **See your insights**:
 
     ![Take action - See insights](../images/wpa/tutorials/burnout-take-action.png)

4.   On the **Best practices** panel, select **Explore in Power BI**: 

     ![Best practices - disconnect](../images/wpa/tutorials/best-practices-disconnect.png)

5.	Follow the instructions on the **Explore in Power BI** page:

     ![Download and connect](../images/wpa/tutorials/explore-in-pbi.png) 
      
     a.	If you do not already have Power BI installed, select the link to download and install it. 
 
     b.	Download the data template for this insight. 
 
     c.	In your web browser or in your Downloads folder, select the downloaded data template file. This opens Power BI.  
 
     d.	Select **Click here to copy the partition identifier**. After you do, a “Copied” indicator is shown:
    
     ![Copied](../images/wpa/tutorials/partition-id-copied.png)    
 
6.	In Power BI, give the information that’s required to make a connection. In the **Connect to Workplace Analytics Data** dialog box, paste the partition identifier that you copied:

     ![Partition ID prompt](../images/wpa/tutorials/partition-id-prompt.png)
 
7.	Select **OK**. The Dive deeper **Home** page opens in Power BI Desktop:
 
     ![Dive deeper -- wellbeing](../images/wpa/tutorials/dive-deeper-wellbeing.png)

**Best-practice recommendation**: In Power BI Desktop, publish your new visualizations to your workspace.

   ![Copied](../images/wpa/tutorials/publish-to-pbi-workspace.png)
 
After you publish, it’s easy to view your visualizations (in read-only mode) in [Power BI Online](https://powerbi.microsoft.com/en-us/). We make this recommendation because the experience of viewing information such as this is optimized for Power BI Online. For more information, see [Publish datasets and reports from Power BI Desktop](https://docs.microsoft.com/power-bi/create-reports/desktop-upload-desktop-files). 

8.	(Optional) Delegate this information to your team members by sharing this report. This lets them dive deeper by slicing and filtering the data to further identify opportunities or track metrics that change over time. 

9.	Go on to the next procedure, [Identify and help opportunity groups](#identify-and-help-opportunity-groups). 

### Identify and help opportunity groups 

These Power BI visualizations will call your attention to the opportunity groups in your organization. In this example, we will examine groups whose members, on average, have less one-on-one time than others in the company. 

**Role:** analyst or limited analyst

1.	On the Dive deeper **Introduction** page, in the **Guided walk-through** insight, select **Start walk-through**:
   
    ![guided walk-through](../images/wpa/tutorials/guided-walkthrough.png)
    
    As you are guided through the walk-through, it opens, in sequence, several other analysis pages that present you with more information about this area (well-being):
      
    ![Pages](../images/wpa/tutorials/pages-toc.png)
   
    Each of these analysis pages gives you a **Group by** choice. For more information, see the next section, Grouping choices. 

### Grouping choices 

Part of the task of identifying groups that might need help is deciding how to define groups. In each of the analysis pages, you can choose a business-attribute pivot to display data; for **Group by**, select either **Organization** or **LevelDesignation**:

![Group by org or level](../images/wpa/tutorials/group-by-choice.png)
 
This choice might help you discover, for example, that a particular trait is evident not in just one or two organizations, but rather for employees at a particular level, across organizations. 

After you make this selection on one page, the graphs on all of the analysis pages switch to that choice. You can then filter the data further to focus your analysis on groups in which you have the most interest. For example, after we selected to **Group by** > **Organization**, we then selected the **Customer Service** group to learn more about it. 

![Group by](../images/wpa/tutorials/distrib-after-hours-collab.png)
  
By using these filtering options, we can see that 8.4% of the employees in the Customer Service group work more than five hours per week in their after-hours time. 

### Explore Advanced analysis

One of your drill-down options is to slice and filter the data in custom ways all in one place, the **Advanced analysis** page. On the **Home** page, in the **Advanced analysis** area, select **Start here**:

![Select Start here](../images/wpa/tutorials/intro-advanced-analysis.png)
 
This opens the **Advanced analysis** page:

![Advanced analysis page](../images/wpa/tutorials/advanced-analysis.png)
 
On this page, for example, you can not only group and filter by **Organization** and by **LevelDesignation**, you can also change the time period for which the data is analyzed, and simultaneously filter by groups in different pivots; that is, for example, you can select **Senior IC** for **LevelDesignation** and at the same time select **Finance-East** and **Finance-South** to view data only for employees at that level in those groups.

After you've identified one or more groups that need help, how can you help them? See [Next steps](#next-steps). 

## Next steps

By using the knowledge that you've gained from these visualizations, you can now take action. For example, you can do the following:

 * Learn more about current behavior and trends by running [queries](query-basics.md). You can also create a dashboard for yourself by importing data that was obtained through Workplace Analytics queries (especially [auto-refresh queries](query-auto-refresh.md)) into [Power BI](../use/view-download-and-export-query-results.md#get-a-link-for-an-odata-feed-to-use-in-power-bi). 

 * Help employees help themselves by pointing them to a pertinent [playbook](../myanalytics/use/mya-adoption/adopt-learning-modules.md). 

 * If you've decided that one or more groups needs help recovering focus time, consider starting a [plan](teamwork-solution.md). 

## Power BI tips, troubleshooting, and FAQs

For details about how to share the dashboard and other Power BI tips, troubleshoot any issues, or review the most frequently asked questions, see [Power BI templates in Workplace Analytics](power-bi-templates.md).

## Related topics

* [Power BI templates in Workplace Analytics](https://review.docs.microsoft.com/en-us/Workplace-Analytics/tutorials/power-bi-templates?branch=pr-en-us-1820)

* [Workplace Analytics Teamwork plans](teamwork-solution.md)

