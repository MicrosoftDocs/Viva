---

title: Influence insights dashboard
description: Learn how to set up and use the Influence insights dashboard in Power BI
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Influence insights

The Influence insights dashboard uses a Power BI template that’s populated by data from Workplace Analytics to gain insights into influencers, who are well connected people in your company. This dashboard lets you visualize and explore answers to the following business questions that leaders ask:

* **Where are the influencers in your company?** - Shows which organizations have concentrated influencer presence and have limited influencer presence.
* **Who is involved in decision-making processes?** - Shows if business decisions are made in a top-down or in a more decentralized manner and if employees at various levels in the hierarchy are empowered to make decisions.
* **How are influencers adapting to the remote work situation?** - Shows how influencers’ collaboration patterns are changing in response to this disruption and what impact this disruption is having on the key roles that influencers play.

Before you can use the Influence insights dashboard in Power BI, it must be populated with data. To do this, set up and run the predefined Influence insights and Standard query queries in Workplace Analytics. The results of these queries will refresh your downloaded Power BI dashboard on a weekly basis.

After you successfully run these queries, you'll see the Influence insights Power BI template as an available download option for the Influence insights query. You’ll need this template to create the Influence insights dashboard in Power BI. After you download the Power BI template, you can then connect the query data from Workplace Analytics to the dashboard in Power BI.

After the Influence insights dashboard is populated with data, you can use it to visualize, explore, and report about your organization's workplace patterns and trends.

## Demonstration

<br><iframe width="800" height="486" src="https://msit.powerbi.com/view?r=eyJrIjoiZWMyNTJmNzktOWQzYy00OTEwLTgxZmQtZDZmMGI1OTJjYjYwIiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9&embedImagePlaceholder=true" frameborder="0" allowFullScreen="true"></iframe>

>[!Note]
>The following demo uses sample data and is only representative of this dashboard, which might not be exactly what you see in a live dashboard specific to your organization's unique data.

## Prerequisites

Before you can run the queries and populate the dashboard in Power BI, you must:

* Be assigned the role of [analyst](../use/user-roles.md) in Workplace Analytics.
* Have the latest version of Power BI Desktop installed. If you have an older version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t?activetab=pivot:overviewtab) to download and install the latest version.

## Set up the dashboard

This dashboard requires results from two queries. For this reason, in the following procedure, you first run one query (**Influence insights**), and then you repeat some steps to run the second query, the **Standard person** query.  

1. In [Workplace Analytics](https://workplaceanalytics.office.com/), select **Analyze** > **Queries**.

2. Under **Start from preselected filters and metrics**, select **Influence insights** (or select **Standard person query**, per Step 7) to open the predefined query, which contains the required metrics to populate the dashboard.

    ![Influence insights query option](../Images/WpA/Tutorials/influence-insights-step-2.png)

3. Select or confirm the following query settings:

   * **Name**: Customize or keep the default name
   * **Group by**:
     * When you configure the **Influence insights** query, select **Aggregated**.
     * When you configure the **Standard person** query, select **Month**.
   * **Time period**: Last 6 months
   * **Meeting exclusions**:
      * When you configure the **Influence insights** query, this choice is not available.
      * When you configure the **Standard person** query, select a meeting exclusion rule.

   > [!Important]
   > * The dashboard can show you how a disruption can change your influencers’ work patterns. For best results, select **Last 6 months** for the **Time period** to include time before and after the disruption.
   > * In this procedure, there is no step to select metrics because the metrics for this query are preselected. If you try to delete a predefined metric, you'll see a warning that the deletion might disable portions of the Power BI dashboard and reduce query results. In turn, this can limit your ability to visualize collaboration patterns. Depending on the metric you delete, you might disable a single Power BI chart, several charts, or all the charts. Select **Cancel** to retain the metric.

      ![Influence insights query selections](../Images/WpA/Tutorials/influence-insights-step-3.png)
 
4. In **Select filters**, for "**Which measured employees do you want to include?**" you can filter the employees in scope for the dashboard. For more details about filter and metric options, see [Create a Network: Person Query](./ona-person-query.md).
5. In **Organizational data**, keep the preselected **Organization**, **LevelDesignation**, and **FunctionType** attributes that the dashboard requires. You can then select any other additional (columns) to include in the dashboard. The **SupervisorIndicator** attribute, while preselected, is optional.

   > [!Important]
   > If you remove any of these preselected organizational data attributes, you might disable one or more Power BI charts and some insights might not appear.

6. Select **Run** to run the query. This might take several minutes to complete.

7. Repeat **Steps 2-6**; this time, specify the **Standard person query**. Make the same selections that you made for the Influence insights query but with the exceptions noted in step 3.

8. In **Queries** > **Results**, after both queries successfully run, select the **Download** icon for the **Influence insights** query results, select **PBI template**, and then select **OK** to download the template.

   ![Influence insights template download](../Images/WpA/Tutorials/influence-insights-step-8.png)

9. Open the downloaded **Influence insights Power BI template**.
10. If prompted to select a program, select **Power BI**.
11. When prompted by Power BI, copy and paste the OData links for both queries into their respective fields.

    * In the Workplace Analytics **Queries** > **Results** page, select the **Link** icon for each query, and select to copy the generated OData URL link.
    * In Power BI, paste each copied link into its respective field. These fields are labeled **Influence insights query URL** and **Standard person query URL**.

      ![Query URLs for Influence insights](../Images/WpA/Tutorials/influence-insights-step-11.png)

    * Set the [**Minimum group size**](../use/settings.md#minimum-group-size) for data aggregation within this report's visualizations in accordance with your company's policy for viewing Workplace Analytics data.
    * The **Column name of Manager Indicator** field captures which column in your dataset represents whether a person is a manager or not. Usually, the column is **SupervisorIndicator** but if it has some other name, enter that name here.
    * The **Values in the Manager Indicator column representing a manager** field indicates the values in the column that represent whether a person is a manager. Usually it is "Mngr" or "Mgr". You can provide multiple values here, including spaces, as long as they are delimited by semi-colons or commas. Example: **Mgr, Mngr**
    * The **Values in the Manager Indicator column representing a manager+** field indicates the values in the column that represent whether a person is a manager’s manager or not. Usually it is "Mngr+" or "Mgr+". You can provide multiple values here, including spaces, as long as they are delimited by semi-colons or commas. Example: **Mgr+, Mngr+**
    * The **Values in the Manager Indicator column representing an individual contributor** field indicates the values in the column that represent whether a person is an IC or not. Usually it is "IC". You can provide multiple values here, including spaces, as long as they are delimited by semi-colons or commas. Example: **IC, Individual contributor**

    > [!Note]
    > If the optional values on this page are not provided or incorrectly provided, some insights might show up with a message such as, "This insight requires the Manager Indicator column to be configured while loading the Power BI template." However, the rest of the PBI loads and is functional.

    * Finally, select **Load** to import the query results into Power BI. Loading these large files might take some time to complete.

12. If you're already signed in to Power BI with your Workplace Analytics organizational account, the dashboard visualizations will populate with your data. You are done and can skip the following steps. If not, proceed to the next step.
13. If you're not signed in to Power BI, or if an error occurs when updating the data, sign in to your organizational account again. In the **OData feed** dialog box, select **Organizational account**, and then select **Sign in**.

    ![Power BI sign in](../Images/WpA/Tutorials/pbi-sign-in.png)

14. Select and enter credentials for the organizational account that you use to sign in to Workplace Analytics, and then select **Save**.

    >[!Important]
    >You must sign in to Power BI with the same account you use to access Workplace Analytics.

15. Select **Connect** to prepare and load the data, which can take a few minutes to complete.

## About the dashboard reports

After the Influence insights dashboard is set up and populated with Workplace Analytics data, you can use the Power BI visualization charts to analyze your organization's influence insights.

The following dashboard reports highlight unique insights about influencers and their impact. They can trigger discussion points for leaders on leveraging influencers' impressive networking capability to drive change or disseminate information more effectively across the company.

The Glossary report at the end of the dashboard provides information about the underlying metric that drives the dashboard. An interpretation is provided in the text box of each report. Here are the influencers reports, with nuances to consider for each:

* **Your influencers at a glance** - Frames the data and gives an overview of the various reports. Select the "i" icon next to each business question to view the related report.
* **Where are the influencers in your company?** - Shows where influencers are present at the organization level. You can select to focus on the top 5, 10, 15 or 20% of influencers. (After you make this  selection, it applies to all of the dashboard reports.) You can further filter and slice across other available attributes.
* **Who is involved in decision making processes** - Shows you how employees at various levels are empowered to make decisions. You can view this at the organization level or by any other available attribute.
* **How are influencers adapting to remote work situations?** - Unlike the other reports, this one shows changes between the baseline and current time periods. It shows the trend in collaboration hours by channel for influencers and can demonstrate the slippage between work and life balance.

## Power BI tips, troubleshooting, and FAQs

For details about how to share the dashboard and other Power BI tips, troubleshoot any issues, or review the most frequently asked questions, see [Power BI templates in Workplace Analytics](../tutorials/power-bi-templates.md).

## Related topic

[View, download, and export query results](../use/view-download-and-export-query-results.md)
