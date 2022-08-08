---
ROBOTS: NOINDEX,NOFOLLOW
title: Beyond knowledge workers dashboard
description: Use the Beyond knowledge workers reports to visualize predefined data from Viva Insights in Power BI
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Beyond knowledge workers

*This experience is only available through private preview at this time.*

The Beyond knowledge worker dashboard uses a Power BI template that is populated by Viva Insights data to conduct a broad diagnostic of digital collaboration patterns (Teams chats, Teams calls, emails, and meetings) for frontline workers and those workers with hybrid office or field roles. It is designed to highlight collaboration patterns for different groups and to correlate collaboration behaviors to productivity outcomes.

The dashboard helps answer the following questions:

* **Digital Adoption** - What are the trends around how your workforce uses digital tools like Teams meetings and chats and Outlook email to collaborate?
* **Collaboration baseline** - What portion of the employee's workweek is spent using digital collaboration tools?
* **Time Investment** - How much time is spent with internal as compared to external partners, and in interactions of different sizes?
* **Manager habits** - Are your managers investing time with their employees and colleagues?
* **Productivity** - Are there interesting relationships between collaboration activity and business outcomes?

You can customize the analysis population, the time period, and the organizational data attributes in the dashboard. Each report includes a **Why this matters**, **Take action**, and **Explore Further** sections that helps answer your business questions and drive positive changes in your organization change.

To populate the dashboard in Power BI, you must set up and successfully run the predefined **Beyond knowledge workers** query.

After you successfully run these queries, you can download the Power BI template from the **Beyond knowledge workers** query on the **Results** page. After you download the Power BI template, you can then connect the query data to the dashboard in Power BI.

## Demonstration

The following demo uses sample data that is only representative of this dashboard and might not be exactly what you see in a live dashboard specific to your organization's unique data.

<iframe width="800" height="486" src=https://msit.powerbi.com/view?r=eyJrIjoiY2IxN2MxZDgtNzI2NC00MDJkLThjYzUtNDFiYjA3YzFlNDRjIiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9&embedImagePlaceholder=true frameborder="0" allowFullScreen="true"></iframe>

## Prerequisites

Before you can run the queries and populate the dashboard in Power BI, you must:

* Be assigned the role of Analyst in the advanced insights app.
* Have the latest version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t?activetab=pivot:overviewtab) to download and install the latest version.

## Set up the dashboard

>[!Note]
>This dashboard is currently only available in English and will only work with data generated from the English version of the app. Before running the required queries, confirm the browser language in the app's URL includes **en-us**, or change it to include **en-us**: ...office.com/en-us/...

1. In the advanced insights app, select **Analyze** > **Query designer**.
2. Under **Start from preselected filters and metrics**, select **Beyond knowledge workers** to open the predefined query, which contains the required metrics to populate the dashboard.
3. Select or confirm the following query settings:

   * **Name** - Customize or keep the default name
   * **Group by** - Week
   * **Time period** - Select the time period you want to analyze
   * **Auto-refresh** - Keep this setting disabled because this template is not designed to track metrics over time
   * **Meeting exclusions** - Select the preferred rule for your tenant

   >[!Important]
   >If you try to delete a predefined metric, you'll see a warning that the deletion might disable portions of the Power BI dashboard and reduce query results. In turn, this can limit your ability to visualize collaboration patterns. Depending on the metric you delete, you might disable a single Power BI chart, several charts, or all the charts. Select **Cancel** to retain the metric.

4. For **Which measured employees do you want to include in your query results**, select **All employees**. To run the reports for a specific segment of your population, such as frontline workers, scope your population in **Select filters**. For more details about filter and metric options, see [Create a Person Query](/viva/insights/tutorials/person-queries?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

   >[!Important]
   >You must have the preferred segment (example frontline worker) attribute uploaded in the organizational data upload. If the upload does not include this attribute, contact your Viva Insights admin to upload it.

5. In **Organizational data**, keep the preselected **Organization** attribute that the dashboard requires.

   >[!Important]
   >If you remove the required, preselected organizational data attributes, you might disable one or more Power BI charts.

6. Locate and select the organizational attribute that identifies people managers in your company (those who have employees who report to them directly or indirectly) as opposed to individual contributors (ICs). Because this field is not a required organizational attribute, your organization might not have included it when setting up the advanced insights app. If you cannot find the field in the menu, contact your Viva Insights admin to confirm whether the field was included in the Organizational HR data upload and made available for query output.

   >[!Important]
   >You can still set up the dashboard without the people manager attribute. However, some of the Power BI charts and filtering capabilities will be disabled.

7. Locate and select the organizational attribute that identifies numerical outcome data (such as, performance ratings, store sales figures, engagement results, safety, or quality scores) to explore relationships between collaboration activity and business outcomes. Because this field is not a required organizational attribute, your organization might not have included it when setting up the advanced insights app. If you cannot find the field in the menu, contact your admin to confirm whether the field was included in the Organizational HR data upload and made available for query output.

   >[!Important]
   >You can still set up the dashboard without the people manager attribute. However, some of the Power BI charts and filtering capabilities will be disabled.

8. You can then select any additional attributes (columns) that you want to include in the reports.
9. Select **Run** to run the query, which can take a few minutes to complete.
10. In **Queries** > **Results**, after both queries successfully run, select the **Download** icon for the **Beyond knowledge workers** query results, select **PBI template**, and then select **OK** to download the template.
11. Open the downloaded **Beyond knowledge workers** template.
12. If prompted to select a program, select **Power BI**.
13. When prompted by Power BI, copy and paste the OData links for both queries into their respective fields.

    1. In **Query designer** > **Results** page, select the **Link** icon for each query, and select to copy the generated OData URL link.
    2. In Power BI, paste each copied link into its respective field.
    3. Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Viva Insights data.
    4. In **SupervisorIndicator** field, enter the exact name of the organizational attribute that you selected in **Step 6**, which designates who in the organization is a people manager. If your organization has not uploaded this field in the organization data file, you don’t have to complete this field. However, some visuals and filtering capabilities will be disabled.
    5. Select **Load** to import the query results into Power BI. Loading these large files may take some time to complete.

14. If you're already signed in to Power BI with your Viva Insights organizational account, the dashboard visualizations will populate with your data. You are done and can skip the following steps. If not, proceed to the next step.
15. If you're not signed in to Power BI, or if an error occurs when updating the data, sign in to your organizational account again. In the **OData feed** dialog box, select Organizational account, and then select **Sign in**. See [Troubleshooting](/viva/insights/tutorials/power-bi-templates?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#troubleshooting) for more details.

    ![Power BI sign in.](../Images/WpA/Tutorials/pbi-sign-in.png)

16. Select and enter credentials for the organizational account that you use to sign in to Viva Insights, and then select **Save**.

   >[!Important]
   >You must sign in to Power BI with the same account you use to access the advanced insights app.

17. Select **Connect** to prepare and load the data, which can take a few minutes to complete.

## Dashboard settings

After the Beyond knowledge workers dashboard is set up and populated with Viva Insights data in Power BI, you are ready to view the report. Optionally, you can set the following parameters in the **Customize report** pane.

* **Time period** - This is the time period that you want to analyze.
* **Exclude specific weeks** – You can select one or more weeks to exclude from analysis, such as those that include company holidays.
* **Organizational attribute to view the report by** - The primary “group-by” attribute shown in all subsequent reports. You can change this attribute at any time and all subsequent report pages will show group values by the new attribute.
* **Organizational attribute to filter by** – To filter the measured employee population, you can filter by any selected Organizational attribute, and then filter by any of the values for these attributes. If you use filters, the measured employees count will reflect a reduced number.

After you have customized the report, you can use the following flexible features in each section to make the insights most relevant to your analysis population:

* **Collaboration baseline** - The default average workweek hours is set to 40 hours. If this does not reflect your organization, you can set a custom workweek below, from 0 to 80. Changing this value will change the value of the metrics and the charts on this page.

    ![Baseline workweek setting.](../Images/WpA/Tutorials/pbi-baseline-workweek.png)

* **Time investment** - The default collaboration tool is set to meetings for the interaction size insight. You can choose to calculate the insight for total collaboration time or any of the individual collaboration types (meetings, email, chats and ad-hoc calls). The default is preset to measure meetings.

    ![Time investment filter.](../Images/WpA/Tutorials/pbi-collab-filter.png)

* **Manager habits** - For best results, your organizational data should include an attribute that identifies people managers, like Supervisor indicator. Filter the values of Supervisor Indicator to identify people managers.

    ![Manager habits settings.](../Images/WpA/Tutorials/pbi-manager-habits.png)

   >[!Important]
   >If you are unable find the required values, reach out to your admin to upload organizational data to include an attribute that identifies people managers. The supervisor indicator filter only applies to the two greyed out visuals on this page. Without this attribute, insights regarding manager habits will not be accurate.

* **Productivity** - If you loaded outcomes related data to your organizational data file you can select Outcome measure from the Y-axis dropdown and compare your success metric with various collaboration metrics on the X-axis. Confirm the outcome data is numerical (such as, performance ratings, store sales figures, engagement results, safety, or quality scores).

    ![Productivity settings.](../Images/WpA/Tutorials/pbi-productivity.png)

Your admin must do the following steps to upload (import) organizational data to the advanced insights app.

1. Prepare and upload the required organizational data in the advanced insights app.
2. Map the fields in the app.
3. Allow the app to validate the data.

For detailed instructions, see [Subsequent organizational data uploads](/viva/insights/setup/upload-organizational-data2?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

## Power BI tips, troubleshooting, and FAQs

For details about how to share the dashboard and other Power BI tips, troubleshoot any issues, or review the FAQ, see [Power BI templates](/viva/insights/tutorials/power-bi-templates?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

## Related topic

[View, download, and export query results](../use/view-download-and-export-query-results.md)
