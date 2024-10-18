---
ms.date: 08/07/2024
title: Hybrid Workforce Experience Power BI report
description: Learn how to use the Microsoft Viva Insights Power BI template to know about your organization's hybrid workforce experience
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva-insights
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Hybrid experience report (manual)

As leaders figure out their organization’s new working models, the Hybrid workforce experience Power BI report helps organizations understand how hybrid work affects employees in various work modes differently. The report identifies opportunities to improve the experience of employees working in the following ways:

* Mostly onsite
* Mostly remote
* Onsite some days of the week and remote on others (hybrid)

The report has six sections, which each address different facets of the employee experience that hybrid working models may impact. Key metrics provide a deep-dive into each topic, along with a **Why it matters** interpretation and **recommended actions**.

To populate the report in Power BI, you’ll need to set up and successfully run the predefined **Hybrid workforce experience** query  in Viva Insights.

[!INCLUDE [Demonstration](includes/demonstration.md)]

> [!VIDEO https://msit.powerbi.com/view?r=eyJrIjoiMTI3OTdkZDQtYTllYy00MDUwLTk4NzEtYTljM2I1YjIyZjEyIiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9]

[!INCLUDE [Prerequisites](includes/prerequisites.md)]

* Have the following attributes uploaded as part of your organizational data:

  * **WeeklyBadgeOnsiteDays**, an attribute identifying the number of days someone works onsite. This could be based on behavioral data such as badge data or Wi-Fi data, or other sources such as a tag in the HR system identifying the number of days an employee intends to work onsite. You might get this data in one of two ways—through a weekly update of onsite days or by using a monthly update of onsite days to calculate the weekly number:
    * If an employee’s number of onsite days is available on a weekly basis (that is, values are between 0 and 5), make sure to include a row with an **EffectiveDate** and **WeeklyBadgeOnsiteDays** value per person per week in your organizational data. You can choose the frequency with which you like to update this data—weekly or monthly.
    * If you’re using an employee’s number of onsite days per month, you can upload the monthly number of onsite days in Viva Insights on a monthly basis.
  * **SupervisorIndicator**, an attribute indicating whether someone is a manager.
  * **HireDate**, an attribute indicating the person’s hire date is required to be able to load the **New hire onboarding insights**. Without this attribute, however, the rest of the report will still load.

> [!NOTE]
> The “OnsiteDays” field is now “WeeklyBadgeOnsiteDays." The values of the "OnsiteDays" field have been copied to a new reserved optional field called "WeeklyBadgeOnsiteDays," and the old "OnsiteDays" is a custom column. The valid values you previously uploaded are present both in "WeeklyBadgeOnsiteDays" and "OnsiteDays."

For more details on organizational data preparation and upload, download our [step-by-step guide](https://go.microsoft.com/fwlink/?linkid=2205161).

You can add new attributes to your organizational data at any time. For more details on how to add new data for existing employees, review the documentation on [subsequent uploads](../../admin/upload-org-data-subsequent.md).

[!INCLUDE [Report setup and run query](includes/report-setup-run-query.md)]

1. In the analyst experience in Viva Insights, select **Analysis**.
1. Under **Power BI templates**, navigate to **Hybrid workforce experience** and select **Start analysis**. For more information about the Hybrid workforce experience template before running your analysis, select **Learn more**.

 3. Under **Query setup**:
    
    1. Type a **Query name**.
    1. Select a **Time period**. **Time period** defaults to **Last 6 months**.
    1. Set **Auto-refresh** (optional). You can set the query to automatically update by checking the **Auto-refresh** box. When you select the **Auto-refresh** option, your query automatically runs and computes a new result every time Viva Insights gets updated collaboration data for licensed people.
       > [!NOTE]
       > If organizational data used in an auto-refreshing query changes (for example, an attribute name is altered or an attribute is removed), the query might stop auto-refreshing.
     4. Type a **Description** (optional).   
     5. Change the metric rule (optional). To set a new metric rule, select **More settings**. Then, pick a new rule from the list. For more information about metric rules, refer to [Metric rules](../../analyst/metric-rules.md).
        > [!NOTE]
        > The **More settings** pane also contains **Group by** settings. Power BI queries are set to **Group by Week**, and you're not able to edit this field.

 1. Under **Predefined template metrics**, view the list of preselected metrics, which appear as gray tags. These metrics are required to set up the Power BI report and you can’t remove them. You can add other metrics by selecting **Add metrics**.
    > [!IMPORTANT]
    > Low-quality or missing organizational data might affect your metrics and result in warnings or errors. Learn more about data-quality notifications in [Data quality in the analyst experience](../../analyst/data-quality-analyst-experience.md).

 1. In **Select which employees you want to include in the query**, add filters to narrow down the employees in scope for your report. Don’t remove the predefined “Is Active” filter. For more details about filter and metric options, refer to [Filters](../../analyst/filters.md). If you notice a warning or error here, it's because one of your attributes is missing from your organizational data or is of low quality.
 1. Under **Select which employee attributes you want to include in the query**, add up to 14 organizational attributes, including the required **Organization** and **HireDate** attributes, and the optional **LevelDesignation** attributes. Once the query runs, you can use these attributes to group and filter the reports.
    > [!IMPORTANT]
    > This PowerBI query needs some specific attributes to run, and we've preselected them for you. These attributes appear in gray and you can't remove them. We might also include some attributes that help your template, but aren't required for your query to run. These attributes appear in blue and you can remove them.
    >
    > If you notice attributes marked with yellow warnings, that attribute's quality is low. If you notice attributes marked in red and the query's **Run** button disabled, then your organizational data is missing that attribute. 
    >
    > Learn more about attributes and data quality in [Data quality in the analyst experience](../../analyst/data-quality-analyst-experience.md).
 1. Under **Select which spotlight attributes you want to include in the query**, add at least one and up to five attributes to use as a legend for insights in the report. You’ll also be able to focus on a specific group of employees in the report. Insights for this group will be highlighted.
 1. Under **Select an attribute that indicates the employee’s engagement score**, you can optionally select an attribute that represents how engaged employees are. 
1. Select **Run** on the upper right side of the screen. The query might take a few minutes to run.
 1. When your query results are ready, go to the **Query results page** and select the Power BI icon. Download the Power BI template and get the partition and query identifiers. You’ll need these identifiers later.

> [!NOTE]
> If you’re setting up a new Hybrid workforce experience (manual) PBI, this PBI now uses WeeklyBadgeOnsiteDays. Therefore, you must upload badge data into the WeeklyBadgeOnsiteDays column during the HR upload.
>
> For recurring Hybrid workforce experience (manual) PBI queries previously set up, they'll continue to use the OnsiteDays attribute and they won't fail. However, you should still set up a new recurring query and upload badge data into the WeeklyBadgeOnsiteDays column.
>
> For Recurring Custom Person queries that use the OnsiteDays attribute, they won't fail either. Still, you should recreate these queries to use the new WeeklyBadgeOnsiteDays attribute.


### Link report to query

1. Open the downloaded template.
1. If you're prompted to select a program, select **Power BI**.
1. When you're prompted by Power BI:
   1. Paste in the partition and query identifiers.
   1. Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Viva Insights data.
   1. Select **Load** to import the query results into Power BI.
1. If prompted by Power BI, sign in using your organizational account. Power BI then loads and prepares the data. For large files, this process might take a few minutes.
    > [!IMPORTANT]
    > You need to sign in to Power BI with the same account you use to access Viva Insights. If available, select **Organizational account** from the left. You might have to sign in more than once.
:::image type="content" source="../../images/analyst-pbi-org-account1.png" alt-text="Screenshot that shows signing into to Power BI on the Organizational account tab":::



## Report settings

After the **Hybrid workforce experience report** is set up and populated with Viva Insights data in Power BI, map values as prompted, which are listed below:

|Attribute value| Prompt|
|---------------|-------|
|Mostly onsite  | Select the number of average % of onsite work days that best describe the work mode of employees that work mostly onsite (that is, from the company’s main worksite). |
|Hybrid | Select the average number of onsite work days that best describe the work mode of employees that work onsite some days during the week and remote on others.|
|Mostly remote| Select the  average number of onsite work days that best describe the work mode of employees that work mostly remote (that is, from home or some other location outside the company’s main worksite).|
|Individual contributors| Select the attribute values that identify employees as individual contributors who do not manage people within your organization.|
|Managers| Select the attribute values that identify managers who manage people within your organization, such as **Mgr** and **Mgr+**.|

After this initial prompt, you can then select **Settings** at top right of any page to view and change the following parameters:

|Setting|Description|
|--------|----------|
|**Select the time period for the report** | Select the time period for which you want to view data in the report.|
|**Select an attribute to group data by** | Select the primary group-by attribute shown in all the reports. You can change this attribute at any time and all report pages will show group values by the new attribute.|
|**Select optional report filter** | Select the organizational attribute and values you want to filter the employees in the report.|
|**Exclusions** | Use the check boxes to: <ul><li>Exclude employees who are likely non-knowledge workers (that is, those spending less than five hours per week on average in meetings, emails, and/or Teams calls and chats). <li>Exclude weeks that are likely holiday or paid-time-off weeks, or weeks that individuals are on other types of leave.|
|**Select the preferred language for your report** | Change the language for your report.|

## About this report

This section:

* Provides metrics specific to this report.
* Lists the six main report pages. For each report page, this section provides the business question the page seeks to answer and describes the type of insights and data the page contains.
* Describes the report’s **Track changes** page.

### Pages

#### Employee work mode

**Does the distribution of employees by work mode meet expectations and is there a potential disconnect between management and individual contributors?**

View the percent of employees by work mode (that is, Mostly onsite, Hybrid, Mostly remote, or Unclassified*) according to the latest week of data, split out by group. You can also discover whether there's a potential disconnect between the share of managers and individual contributors working Mostly onsite, Hybrid, or Mostly remote. In case the **WeeklyBadgeOnsiteDays** data is updated periodically, the **Explore the trends** button allows you to review the trend of percent of employees tagged as “Mostly onsite,” “Hybrid,” “Mostly remote,” and “Unclassified.”

>[!Note]
>*If an employee is categorized as “Unclassified,” it means that there was no numerical **WeeklyBadgeOnsiteDays** value found in the organizational data. The “Unclassified” employee category is not displayed in the remainder of this report.

#### Collaboration habits

**How does hybrid work impact meeting engagement and collaboration patterns throughout the week?**

View the average weekly time employees in different work modes spend collaborating in meetings, emails, Teams calls, or Teams chats on different days of the week. The numbers allow you to analyze whether employees in different work modes have equitable access to collaboration opportunities and tools. You can also see, by work mode, the average share of meeting time during which employees multitask by sending emails or Teams chats.

#### Connectivity and belonging

**How does hybrid work impact the employees’ connectivity and sense of belonging?**

Get the average internal employee network size, split by work mode, including a three-month time trend. This page also shows the average weekly hours employees spent collaborating in small groups (with fewer than eight people), broken out by work mode.

#### Work-life balance and flex work

**How does hybrid work impact flexible schedules and the employees’ ability to unplug?**

Understand, by work mode, the percent of employees collaborating outside of their working hours as set in Outlook for more than five hours per week. The chart on the right takes into account both the number of distinct daily hours employees participate in meetings, emails, and Teams chats or calls, as well as the average weekly hours employees spend collaborating outside of their set working hours. By combining both metrics, the page shows the following working patterns:

* Long non-standard hours – Employees with more than nine distinct active hours a day and spending more than five hours a week in collaboration outside of set working hours.
* Long hours – Employees with more than nine active hours a day but fewer than five hours a week in collaboration outside of set working hours.
* Flexible hours – Employees with nine or fewer active hours a day, but who spend more than five hours a week outside of typical or set working hours.
* Low-collaboration & standard hours – Employees with nine or fewer active hours a day and fewer than five hours per week spent in collaboration outside of set working hours. These employees are either successfully keeping their hours in check or depend less on collaboration to get their jobs done.

#### New hire onboarding

**How fast are new hires integrating into the organization’s network and are they getting the manager support they need?**

Discover the average weekly time new hires get with their manager, broken out by work mode. New hires are defined as employees with tenure of less than one year. The toggle key allows you to review all time spent in meetings or calls where both the employee and their manager are present. This information can help a manager:

* Provide support and mentoring.
* Focus on the time spent in 1:1s with the employee, which presents a great opportunity for new-hire coaching and providing direction.

The chart on the right shows the average internal new-hire network size in an employee’s first couple of months, broken out by work mode. This chart indicates the pace at which new hires in different work modes are building their networks and integrating in the organization.

#### Manager connection

**How does the employee and manager work mode impact the employees’ access to manager coaching?**

Find out, by work mode, the average 1:1 time employees get with their manager. The chart on the right explores whether a manager’s work mode affects the 1:1 time employees get with their manager. If the correlation is **Large**, Mostly onsite managers might have an unconscious tendency to give preferential treatment to those employees in the immediate vicinity.
  
#### Track changes

**How are behaviors evolving for employees in different work modes?**

View trends for key leading indicator metrics that were introduced throughout the report, including metrics about collaboration habits, employee networks, work-life balance, new hire onboarding, and the manager connection.

### Other features

The report also includes the following features:

* **Break out by group** panes, which allow you to do further drill-throughs on the report pages and group data by different organizational attributes.
* **Take action** panes, which list opportunity areas and recommended actions for each section in the report.
* **Settings**, where you can:
    * Select the time period and organizational attribute by which to view the reports.
    * Select which employees to include in the reports.
    * Use exclusion options.

* **Glossary** that describes the metrics used in the different reports.

[!INCLUDE [Power BI tips and troubleshooting and Related topics](includes/powerbi-tips-related-topic.md)]

