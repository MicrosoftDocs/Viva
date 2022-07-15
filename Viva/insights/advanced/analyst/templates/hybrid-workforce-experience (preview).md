---
ROBOTS: NOINDEX,FOLLOW
title: Hybrid Workforce Experience Power BI report (preview)
description: Learn how to use the Microsoft Viva Insights Power BI template to know about your organization's hybrid workforce experience
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


# Hybrid workforce experience report (preview)

*This experience is available only through private preview.*

As leaders figure out their organization’s new working models, the Hybrid workforce experience Power BI report in Microsoft Viva Insights helps organizations understand how hybrid work affects employees in various work modes differently. The report identifies opportunities to improve the experience of employees working in the following ways:

* Mostly onsite
* Mostly remote
* Onsite some days of the week and remote on others (hybrid)

The classification of employees in these different groups is customizable and is based on the average number of days per week the employee is detected to be working onsite (meaning from the company’s corporate network). The detection of an employee onsite days is based on Azure Active Directory (AD) log-in information. Note that the algorithm only uses 3 out of 4 octets of an IP address for the classification of employees as either onsite or not. It never uses the employee’s actual physical location.  

The report has six sections, which each address different facets of the employee experience that hybrid working models may impact. Key metrics provide a deep-dive into each topic, along with a **Why it matters** interpretation and **recommended actions**.

![Hybrid workforce experience Power BI report, Report settings](/viva/insights/advanced/images/hwfe-preview-PBI-summary.png)

To populate the report in Power BI, you’ll need to set up and successfully run the predefined Hybrid workforce experience (preview) query  in Viva Insights.
<!--waiting for embed link
## Demonstration

The following demonstration uses sample data that’s only representative of this report and might not be exactly what you see in a live report specific to your organization's unique data.

[iframe]

-->

## Prerequisites

Your organization qualifies for this preview because:

* The analyzed population is using Azure Active Directory to access Microsoft 365 applications.
* The analyzed population is not on a virtual private network (VPN), or it has [VPN split-tunneling](/microsoft-365/enterprise/microsoft-365-vpn-implement-split-tunnel) for Azure Active Directory configured.

Before you can run the queries and populate the report in Power BI, you’ll need to:

* Be assigned the role of Insights Analyst in Viva Insights.
* Have the June 2022 (or newer) version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://powerbi.microsoft.com/en-us/getting-started-with-power-bi/) to download and install the latest version.
* Have the following attributes uploaded as part of your organizational data:
  * **SupervisorIndicator**, an attribute indicating whether someone is a manager.
  * **HireDate**, an attribute indicating the person’s hire date is required to be able to load the New hire onboarding insights. Without this attribute, however, the rest of the report will still load.

## Report setup

### Run query

>[!Note]
> For this release of Viva Insights, this report is currently only available in English and will only work with data generated from the English version of Viva Insights.

1. In the analyst experience in Viva Insights, **Analysis**.

2. Under **Power BI templates**, navigate to **Hybrid workforce experience (preview)** and select **Start analysis**. To get more information about the Hybrid workforce experience template before running your analysis, select **Learn more**.
![Start query](/viva/insights/advanced/images/hwfe-preview-pbi-start.png)
3. Under **Query setup**:
    1. Type a **Query name**.
    1. Select a **Time period**. **Time period** defaults to **Last 3 months**.
    1. Optional: You can set the query to automatically update by checking the **Auto-refresh** box. When you select the **Auto-refresh** option, your query automatically runs and computes a new result every Viva Insights gets updated collaboration data for licensed people.

    >[!NOTE]
    >If the organizational data used in an auto-refreshing query changes (for example, an attribute name is altered or an attribute is removed), you might see an error when you run the query.

    4. Optional: Type a **Description**.
![Start query](/viva/insights/advanced/images/hwfe-preview-pbi-setup1.png)
        Selecting **More settings** brings you to a pane, but there’s nothing you need to change there.

        In this pane:
    
        * Power BI queries are set to **Group by Week**. Do not change this **Group by** designation.
         * The **Metric rules** field defaults to **Meeting exclusions rule (preferred rule)**. This field isn’t customizable in this release; for more information, refer to **Metric rules**.

4. Under **Predefined template metrics**, leave prepopulated metrics as they appear.  

    ![Start query](/viva/insights/advanced/images/hwfe-preview-pbi-predefined-metrics.png)

>[!NOTE]
> Metrics in Power BI templates can't be edited in this release of Viva Insights. To expand the full list of metrics included in the Power BI template, select the arrow in the box beneath Metrics, filters, and organizational attributes.

5. You can filter the employees in scope for the report under **Select which employees you want to include in the query**. Don’t remove the predefined “Is Active” filter.  For more details about filter and metric options, refer to [Person queries](../person-query.md).

    ![Is active filter](/viva/insights/advanced/images/pbi-templates-isactive-filter.png)


6. Under **Select which employee attributes you want to include in the query**, select the **HireDate** attribute if available. Then, add other organizational attributes—you can add up to seven organizational attributes, including **HireDate**. Once the query runs, you can use these attributes to group and filter the reports.

    >[!IMPORTANT]
    >Some employee attributes are required to set up this Power BI template, which are preselected for you in the query. *Do not remove any preselected attributes.*
    >
    >If you see attributes marked in red and the query’s **Run** button disabled, it means that these required attributes are missing from your organizational data. Contact your admin to upload them.

7. Select **Run** on the upper right side of the screen, which can take a few minutes to complete.

8. When your query results are ready, go to the **Query results** page and select the **Power BI** icon to download the Power BI template and copy the query identifier. You'll need the query identifier later.

### Link report to query

9. Open the downloaded Hybrid workforce experience (preview) template.

10. If prompted to select a program, select **Power BI**.

11. When prompted by Power BI:
    1. Paste in the query identifier.
    1. Set the **Minimum group size** for data aggregation within this report's visualizations in accordance with your company's policy for viewing Viva Insights data.
    1. Select **Load** to import the query results into Power BI.

12. If prompted by Power BI, sign in using your organizational account. Power BI will load and prepare the data, which can take some time to complete for large files.

>[!IMPORTANT]
> You must sign in to Power BI with the same account you use to access Viva Insights.

## Report settings

After the **Hybrid workforce experience report (preview)** is set up and populated with Viva Insights data in Power BI, map values as prompted, which are listed below:

|Attribute value| Prompt|
|---------------|-------|
|Mostly onsite  | Select the number of average % of onsite work days that best describe the work mode of employees that work mostly onsite (that is, from the company’s main worksite). |
|Hybrid | Select the  average % of onsite work days that best describe the work mode of employees that work onsite some days during the week and remote on others.|
|Mostly remote| Select the  average % of onsite work days that best describe the work mode of employees that work mostly remote (that is, from home or some other location outside the company’s main worksite).|
|Individual contributors| Select the attribute values that identify employees as individual contributors who do not manage people within your organization.|
|Managers| Select the attribute values that identify managers who manage people within your organization, such as **Mgr** and **Mgr+**.|

![Hybrid workforce experience Power BI report, Report settings](/viva/insights/advanced/images/hwfe-preview-PBI-questions.png)

After this initial prompt, you can then select **Settings** at top right of any page to view and change the following parameters:

* **Select the time period for the report** – Select the time period for which you want to view data in the report.  
* **Select an attribute to group data by** – Select the primary group-by attribute shown in all the reports. You can change this attribute at any time and all report pages will show group values by the new attribute.
* **Select optional report filter** – Select the organizational attribute and values you want to filter the employees in the report.
* **Exclusions** – Use the check boxes to:
    * Exclude employees who are likely non-knowledge workers (that is, those spending less than five hours per week on average in meetings, emails, and/or Teams calls and chats).
    * Exclude weeks that are likely holiday or paid-time-off weeks, or weeks that individuals are on other types of leave.

    ![Hybrid workforce experience Power BI report, Report settings](/viva/insights/advanced/images/hwfe-preview-PBI1.png)

## About this report

This section:

* Provides metrics specific to this report.
* Lists the six main report pages. For each report page, this section provides the business question the page seeks to answer and describes the type of insights and data the page contains.
* Describes the report’s **Track changes** page.

### Metrics

 Name | Description| Type
|------|------------|------|
|**Remote days**|  Number of days a person spent working remote (not on the company's corporate network). Note that because there’s a one-week delay in computing this metric, the values for the most recent week of data won’t be available.| Count|
|**Manager remote days** | Number of days a person's direct manager spent working remote (not on the company's corporate network). Note that because there’s a one-week delay in computing this metric, the values for the most recent week of data won’t be available.| Count|
|**Onsite days**| Number of days a person spent working onsite (on the company's corporate network). Note that because there’s a one-week delay in computing this metric, the values for the most recent week of data won’t be available.| Count|
|**Manager onsite days**| Number of days a person's direct manager spent working onsite (on the company's corporate network). Note that because there’s a one-week delay in computing this metric, the values for the most recent week of data won’t be available.| Count

>[!NOTE] 
>There’s a one-week delay in computing these metrics. This means that if you run a:
>
> * Weekly query, the last week of data for the four metrics above will be "0."
> * Daily query, the data for the four metrics above will be "0" for the last seven days in your query.
> * Monthly query, the data for the last seven days of the last month in the query will be "0."

### Pages

#### Employee work mode

**Does the distribution of employees by work mode meet expectations and is there a potential disconnect between management and individual contributors?**

This page shows the percent of employees by work mode (that is, Mostly onsite, Hybrid, Mostly remote, or Unclassified*) according to the latest week of data, split out by group. This page also highlights a potential disconnect between the share of managers and individual contributors working Mostly onsite, Hybrid, or Mostly remote. In case the **OnsiteDays** data is updated periodically, the **Explore the trends** button allows you to review the trend of percent of employees tagged as “Mostly onsite,” “Hybrid,” “Mostly remote,” and “Unclassified.”

*If an employee is categorized as “Unclassified,” it means that there was no numerical OnsiteDays value found in the organizational data. The “Unclassified” employee category is not displayed in the remainder of this report.

#### Collaboration habits

**How does hybrid work impact meeting engagement and collaboration patterns throughout the week?**

This page shows the average weekly time employees in different work modes spend collaborating in meetings, emails, Teams calls, or Teams chats on different days of the week. The numbers allow you to analyze whether employees in different work modes have equitable access to collaboration opportunities and tools. This page also shows, by work mode, the average share of meeting time during which employees multitask by sending emails or Teams chats.

#### Connectivity and belonging

**How does hybrid work impact the employees’ connectivity and sense of belonging?**

This page shows the average internal employee network size, split by work mode, including a three-month time trend. This page also shows the average weekly hours employees spent collaborating in small groups (with less than eight people), broken out by work mode.

#### Work-life balance and flex work

**How does hybrid work impact flexible schedules and the employees’ ability to unplug?**

This page shows, by work mode, the percent of employees collaborating outside of their working hours as set in Outlook for more than five hours per week. The chart on the right takes into account both the number of distinct daily hours employees participate in meetings, emails, and Teams chats or calls, as well as the average weekly hours employees spend collaborating outside of their set working hours. By combining both metrics, the following working patterns are identified:

* Long non-standard hours: employees with more than nine distinct active hours a day and spending more than five hours a week in collaboration outside of set working hours.
* Long hours: employees with more than nine active hours a day but fewer than five hours a week in collaboration outside of set working hours.
* Flexible hours: employees with nine or fewer active hours a day, but who spend more than five hours a week outside of typical or set working hours.
* Low-collaboration & standard hours: employees with nine or fewer active hours a day and fewer than five hours per week spent in collaboration outside of set working hours. These employees are either successfully keeping their hours in check or depend less on collaboration to get their jobs done.

#### New hire onboarding

**How fast are new hires integrating into the organization’s network and are they getting the manager support they need?**

This page shows the average weekly time new hires get with their manager, broken out by work mode. New hires are defined as employees with a tenure of less than one year. The toggle key allows you to review all time spent in meetings or calls where both the employee and their manager are present. This information can help a manager:

* Provide support and mentoring.
* Focus on the time spent in 1:1s with the employee, which presents a great opportunity for new-hire coaching and providing direction.

The chart on the right shows the average internal new-hire network size in an employee’s first couple of months, broken out by work mode. This chart indicates the pace at which new hires in different work modes are building their networks and integrating in the organization.

#### Manager connection

**How does the employee and manager work mode impact the employees’ access to manager coaching?**

This page shows, by work mode, the average 1:1 time employees get with their manager. The chart on the right explores whether a manager’s work mode affects the 1:1 time employees get with their manager.
  
#### Track changes

**How are behaviors evolving for employees in different work modes?**

This page shows the trends for key leading indicator metrics that were introduced throughout the report, including metrics about collaboration habits, employee networks, work-life balance, new hire onboarding, and the manager connection.

### Other features

The report also includes the following features:

* **Break out by group** panes, which allow you to do further drill-throughs on the report pages and group data by different organizational attributes.
* **Take action** panes, which list opportunity areas and recommended actions for each section in the report.
* **Settings**, which enables you to:
    * Select the time period and organizational attribute by which to view the reports.
    * Select which employees to include in the reports.
    * Use exclusion options.
* **Glossary** that describes the metrics used in the different reports.

## Power BI tips, FAQs, and troubleshooting

For details about how to share the report and other Power BI tips, troubleshoot any issues, or review the FAQ, see [Power BI tips, FAQ, and troubleshooting](./power-bi-faq-troubleshoot.md).

## Related topic

[Access query results and modify existing queries](/viva/insights/advanced/analyst/query-results.md)
