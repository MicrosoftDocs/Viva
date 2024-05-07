---
ms.date: 5/6/2024
title: Use Microsoft Copilot Dashboard advanced features with a Viva Insights subscription
description: Explains how to use the Microsoft Copilot Dashboard's advanced features, including filters and Copilot metric breakdowns, with a Viva Insights subscription.
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.collection:
- viva-insights-personal
- viva-copilot
- magic-ai-copilot
ms.localizationpriority: medium 
ms.service: viva-insights
manager: anirudhbajaj
audience: user
---

# Use Microsoft Copilot Dashboard advanced features with a Viva Insights subscription

The Microsoft Copilot Dashboard provides actionable insights to help your organization get ready to deploy AI, drive adoption based on how AI is transforming workplace behavior, and measure the impact of Copilot.

Some of the dashboard’s metrics and functionalities are available to any customer with a Microsoft 365 or Office 365 subscription for business or enterprise. Learn about these features in [Connect to the Microsoft Copilot Dashboard for Microsoft 365 customers](./copilot-dashboard.md).

But, if you have a [paid Viva Insights subscription](https://www.microsoft.com/microsoft-viva/insights), the dashboard provides an additional set of metrics, filtering options, and other features.

With a Viva or a Viva Insights subscription, the dashboard provides the same categories of metrics as the non-subscription dashboard, but the adoption, impact, and sentiment categories provide additional metrics and filters. [There are also new features for analysts to incorporate Copilot metrics into their person queries](#add-copilot-metrics-to-your-custom-person-query).

>[!Note]
>For these new metrics to appear in the dashboard, the employees being analyzed must be assigned a paid Viva or Viva Insights license.

Let's dive in to this advanced set of features.

### Prerequisites

* The advanced dashboard is available to customers who have a Microsoft 365 or Office 365 subscription for business or enterprise, as well as a Viva Insights subscription.

* A Viva Insights license is required to view the app in Teams for leaders, and the analyst tool bench is required for custom reports. Requires Viva Insights, Workplace Analytics and Feedback, or Viva Suite SKUs.

* At least 10 licenses of Viva Insights SKUs should be assigned before the dashboard is enabled. [Learn how to assign licenses](../advanced/setup-maint/assign-licenses.md). To see more meaningful insights, you should enable at least 100 licenses.

### Access and manage user access to the dashboard

*Applies to: Microsoft 365 global admin*

[Use these steps to access the dashboard and manage user access to the dashboard's metrics](./copilot-dashboard.md#access-the-dashboard-in-viva-insights).

### Minimum group size

On the adoption and impact pages, you can view the aggregated user-level metrics for groups that meet or exceed the [minimum group size set by your Insights admin](../advanced/setup-maint/privacy-settings.md#minimum-group-size), which by default is 10 licensed employees.

## Interpreting the data

*Applies to: Employee users*

### Readiness

>[!Note]
>Readiness data in the dashboard represents data over the previous 28 days. There’s a four-day data delay from the current date. For example, if you viewed the data on Wednesday, March 20, 2024, the dashboard represents activity between Saturday, February 17 and Friday, March 15.

Learn about readiness data in the dashboard in [Interpreting the data](./copilot-dashboard.md#interpreting-the-data).

### Adoption and impact

The adoption and impact pages use different calculations for their tally counts. The illustration and explanation below describes these calculations.

:::image type="content" source="images/copilot-dash-licenses.png" alt-text="Screenshot that shows the count of licenses.":::

* 2,518 employees who have both a Copilot license *and* a Viva Insights subscription will be measured in the dashboard. The 2,518 tally is based on the four complete weeks that ended with the second Saturday before the current date.

* 3,541 Copilot licensed employees represents the tenant level total count. There’s a four day data delay from the current date.

>[!Note]
>Adoption and impact data underneath the filter represents the four complete weeks that ended on the second to last Saturday prior to the current date. For example, if someone viewed their data on Wednesday, March 20, 2024, the second to last Saturday would be March 9, and the dashboard would represent activity between Sunday, February 11 and Saturday, March 9.

### Select the filters for your analysis in the dashboard

*Applies to: Employee users*

:::image type="content" source="images/copilot-dash-filters-ga.png" alt-text="Screenshot that shows the filters tool.":::

At the top left of the adoption and impact page, next to **Scope**, select the dropdown to choose between viewing insights for individual teams within your entire company, or teams just within your group. You can also filter by team by selecting **View by** above the various metric reports.

By default, the **Scope** and **Organization** filters are determined by your [Microsoft Entra ID](../advanced/admin/org-data-overview.md). The advanced insights app can get organizational data in one of two ways: through Microsoft Entra ID, which is the default setting; or through an [organizational data file that your Insights admin uploads](../advanced/admin/org-data-overview.md).

The **Scope** filter is based on the Microsoft Entra ID attribute "ManagerID" to populate "Your company" data and "Your group" data by default. If your Insights admin uploads a .csv file with the attribute of "ManagerID," the "Your group" data in the filter will be updated.

:::image type="content" source="images/copilot-dash-scope-ga-02.png" alt-text="Screenshot that shows the scope filter options.":::

The **Organization** filter corresponds to the Microsoft Entra ID data source field named "Department." If your Insights admin uploads a .csv file with an organizational data attribute of "Organization," it will replace the Microsoft Entra ID data source.

Your Insights admin needs to upload "FunctionType" Viva attributes for you to view the **Job function** dropdowns. The **Job function** filter will only show up if your Insights admin uploads a .csv file with the organizational data attribute of "FunctionType."

### Adoption

After you've deployed Copilot in your organization, this page allows you to track user adoption trends per Microsoft 365 app and Copilot feature.

The page included with a Microsoft 365 subscription displays aggregate metrics at the tenant level. [Learn about these metrics](./copilot-dashboard.md#adoption).  

With a Viva Insights subscription, the page consists of metrics for employees who have a Viva or Viva Insights license. With this version of the dashboard, three main insights are covered.

At the top of the page, you’ll see tallies for **Copilot licensed employees**, and **Active Copilot users**. Let’s define these terms.

* **Copilot licensed employees**: The total number of employees with a Copilot license.

* **Active Copilot users**: Employees who performed at least one Copilot activity in the previous 28 days.

Now let’s look at the insights provided by this page.

**Insight #1: High-level overview of Copilot usage across the organization**

:::image type="content" source="images/copilot-dash-adoption.png" alt-text="Screenshot that shows the first group of adoption metrics." lightbox="images/copilot-dash-adoption.png":::

**Insight #2: Breakdown of Copilot usage across different Microsoft 365 apps**

App totals reflect the total number of adoption metrics in the following Microsoft 365 apps: Microsoft Teams, Outlook, Word, Excel, PowerPoint, OneNote, Loop, and Copilot chat (formerly Microsoft 365 Chat).

Group totals reflect the sum of groups that are above the minimum group size.  

* Group with less than the minimum group size your Insights admin set won’t be included the sum total.

* When a different “View by” attribute is selected, the Group totals might show different numbers. Because there might be people who don’t report to anyone as detected by Entra, there might be people missing the organizational attributes. [Learn more about uploading organizational data](../advanced/admin/upload-org-data-subsequent.md).

:::image type="content" source="images/copilot-dash-adoption-02.png" alt-text="Screenshot that shows the second group of adoption metrics." lightbox="images/copilot-dash-adoption-02.png":::

**Key metrics for this page:**

| Metric | Definition |
|---|---|
| Copilot licensed employees | The number of users who have a Copilot license in the past 28 days. |
| Percentage of Copilot licensed employees | The percentage of Copilot licensed users out of the total measured population in that group (Copilot and non-Copilot users). |
| Active Copilot users | The number of users who used Copilot at least once in any of the following Microsoft 365 apps during the last 28 days: Microsoft Teams, Microsoft Outlook, Microsoft Office, and Microsoft Copilot. |
| Percentage of active Copilot users | The percentage of active Copilot users out of the number of Copilot licensed users for the given time period. |
| Inactive Copilot users | The number of users who have a Copilot license and haven’t been active in Copilot in the last 28 days. |
| Non-Copilot users | The number of users who don't have a Copilot license in the last 28 days. |
| Copilot actions taken | The number of actions in Microsoft Copilot completed by active Copilot users. |
| Meetings summarized by Copilot | The number of meetings summarized by Copilot. |
| Meeting hours summarized by Copilot | The number of hours of meetings summarized by Copilot. |
| Meeting summaries created by Copilot |  The number of times users summarized meetings using Copilot. |
| Emails sent using Copilot | The number of emails sent with assistance from Copilot. |
| Email drafts generated by Copilot |  The number email drafts users generated using Copilot. |
| Email coaching actions taken using Copilot | The number of times users selected coaching by Copilot in Outlook. |
| Email thread summaries created by Copilot | The number of times users summarized email conversations using Copilot. |
| Document drafts created by Copilot | The number of times users drafted Word documents with Copilot. |
| Document summaries created by Copilot | The number of times users summarized Word documents using Copilot. |
| Presentations created by Copilot | The number of times users created PowerPoint presentations using Copilot. |
|  Rewrite text actions taken using Copilot |  The number of times users modified text in Word documents using Copilot. |
|  Presentation summaries created by Copilot | The number of times users summarized PowerPoint presentations using Copilot. |
| Excel formulas created by Copilot | The number of times users generated new columns with formulas based on Excel data using Copilot. |
|  Excel analysis actions taken using Copilot |  The number of times users analyzed data to show insights as charts, PivotTable objects, summaries, trends, or outliers in Excel using Copilot. |
| Excel formatting actions taken using Copilot | The number of times users highlighted, sorted, and filtered tables in Excel using Copilot. |
| Copilot chat queries submitted | Number of Copilot chat queries submitted by users. |
| Chat conversation summaries created by Copilot | The number of times users summarized chats and channel conversations in Teams using Copilot. |
| Chat message drafts composed using Copilot | The number of chat and channel message drafts created in Teams using Copilot. |
| Chat conversations summarized by Copilot | The number of chats and channel conversations summarized by Copilot. |
| Chats sent | The number of chat messages sent by users using Copilot. |

**Key actions users can take in the report:**

| Action | What can they do |
|---|---|
| View by | Default view: Group (with 20 values) <br> </br> Users can change this to view the data by other organizational attributes like Organization and Job function. |
| Filters | Default view: No filters. <br> </br> Users can apply filters on three organizational attributes: Group, Organization, and Job function. |

The organizational attributes described above are generated from either Microsoft Entra ID or the attributes uploaded by your Viva Insights admin. If the attributes are generated from Microsoft Entra ID, only “Organization” attribute will be populated. If you want to use other attributes like Job function, the Viva Insights admin needs to upload this data through HR upload.  

The default attributes available in the dashboard are Organization and Job function. If you need to perform an analysis using different attributes uploaded by your admin, you can [set up a custom person query](../advanced/analyst/person-query.md).

### Impact

This page helps you assess Copilot impact by layering the results of Microsoft's quantitative and qualitative research on top of your organization's Copilot and Microsoft 365 usage patterns. 

At the top of the page, you’ll see tallies for **Active Copilot users**, **Copilot actions taken**, and **Copilot assisted hours**. Let’s define these terms.

* **Active Copilot users**: The total number of employees who performed at least one Copilot activity in the previous 28 days.

* **Copilot actions taken**: The total number of actions taken using Copilot across Microsoft 365 apps.

* **Copilot assisted hours**: This is an estimate of the total time employees were assisted by using Copilot over the past 28 days. Employees can re-invest time savings from Copilot in learning, training, skilling, and having a greater business impact. The metric is computed based on your employees’ actions in Copilot and multipliers derived from [Microsoft’s research on Copilot users](https://www.microsoft.com/worklab/work-trend-index/copilots-earliest-users-teach-us-about-generative-ai-at-work). The metric should be viewed as a general estimate based on the most relevant Copilot usage data and research currently available. The underlying calculation methodology will evolve over time as new information becomes available. See more information on the calculation below.

#### Details on the "Copilot assisted hours" metric
 
The **Copilot assisted hours** metric is a general estimate that tries to leverage the latest research on AI and productivity to describe your employees’ use of three types of Copilot capabilities described in the table below. Copilot usage metrics are aggregated within each category, then multiplied by an assistance factor to determine hours assisted per category. The three resulting values are then added together to produce the final **Copilot assisted hours** metric. Please note that these are broad approximations based on the [best available research rather than precise calculations](https://www.microsoft.com/research/project/the-new-future-of-work). As more research becomes available, we will update our approach.

| Copilot capability | Metric(s) counted | Assistance factor | Source of assistance factor (if applicable) |
|---|---|---|---|
| Meeting summaries | Meeting hours summarized by Copilot | The full duration of each meeting summarized is counted towards total assisted hours (e.g. if a user summarizes an hour-long meeting after it has ended, that counts as one assisted hour). | N/A |
| Search and summaries | Copilot chat queries submitted <br> <br/> Email thread summaries created by Copilot <br> <br/> Document summaries generated by Copilot <br> <br/> Presentations summarized by Copilot <br> <br/> Spreadsheet analyses completed using Copilot <br> <br/> Chat threads summarized by Copilot | 6 minutes per search or summary action  | In a study of 163 knowledge workers, users were able to retrieve information across files, emails, and calendars 6 minutes faster with Copilot versus without Copilot. See study #4 in section 2 of [this blog post](https://www.microsoft.com/en-us/worklab/work-trend-index/copilots-earliest-users-teach-us-about-generative-ai-at-work). |
| Creation | Email coaching actions using Copilot <br> <br/> Email drafts generated by Copilot <br> <br/> Documents drafted by Copilot <br> <br/> Presentations created using Copilot <br> <br/> Rewrite text actions taken using Copilot <br> <br/> Excel formula calculations completed using Copilot <br> <br/> Excel formatting actions completed using Copilot <br> <br/> Chat messages composed using Copilot | 6 minutes per creation action  | In a study of 147 knowledge workers, people were able to complete a writing task (drafting a blog post) 6 minutes faster with Copilot versus without Copilot. See study #1 in section 2 of [this blog post](https://www.microsoft.com/en-us/worklab/work-trend-index/copilots-earliest-users-teach-us-about-generative-ai-at-work). Creation is especially difficult to summarize in a single number, so this number should be in particular understood to be a broad estimate. As research improves, we will adjust our methodology. |

**Key insights for this page:**

On any card, select **Explore more** to dive into these metrics.

>[!Important]
>Copilot is not likely to be solely responsible for any metric differences shown in the dashboard. In addition to Copilot, multiple organizational factors, such as seasonality, role shifts, or organizational changes, may influence changes in these metrics.

**Comparison between groups**

This analysis helps you compare usage patterns between two groups. Analysts can use this to compare usage patterns between Copilot and non-Copilot users, or even two different Copilot user groups.  

There are the four categories of users:

* **Copilot licensed employees**: Employees who have been assigned a Copilot license

* **Non-Copilot users**: Employees who have not been assigned a Copilot license

* **Active Copilot users**: Employees who performed at least one Copilot activity in the previous 28 days  

* **Inactive Copilot users**: Employees assigned a Copilot license but who have not performed at least one Copilot activity in the previous 28 days

**Comparison between Copilot and non-Copilot users**

This analysis helps you compare collaboration activities between employees who use Copilot and those who don’t, based on a specific metric. For instance, you can select **Meeting hours** as your metric to analyze the meeting hours per person for both Copilot users and non-Copilot users across the filters you’ve selected.

**Key metrics for this page:**

| Category | Metric | Definition |
|---|---|---|
| **Meetings** | Meetings summarized by Copilot | The number of meetings summarized by Copilot. |
|  | Attended meetings | The number of meetings users attended in Teams which had two or more attendees. |
|  | Conflicting meeting hours  |  The number of meeting hours where users had overlapping meetings on their calendar. The count includes only the amount of time that overlaps. | 
|  | Meeting hours |  The number of hours users spent in meetings with at least one other person during and outside of working hours.  |
|   |  Multitasking meeting hours |  The number of hours users spent sending or reading emails or chats, posting or replying to Teams channels messages, or visiting Teams channels during a meeting or Teams call. | 
|   | Meeting hours summarized by Copilot | The number of hours of meetings summarized by Copilot. |
| **Chat** | Chat conversation summaries created by Copilot |  The number of times users summarized chats and channel conversations in Teams using Copilot.  | 
|   | Chats sent | The number of chat messages sent by users using Copilot. | 
|   | Chat conversations summarized by Copilot | The number of chats and channel conversations summarized by Copilot.  | 
| **Emails** | Emails sent using Copilot | The number of emails sent with assistance from Copilot. |
|   | Email coaching actions taken using Copilot | The number of times users selected coaching by Copilot in Outlook. | 
|   | Emails sent | The number of emails sent by users. | 
|   | Email drafts generated by Copilot |  The number email drafts users generated using Copilot. | 
|   | Email thread summaries created by Copilot |  The number of times users summarized email conversations using Copilot.  |
| **Documents** | Document drafts created by Copilot |  The number of times users drafted Word documents with Copilot.  |
|   | Document summaries created by Copilot |  The number of times users summarized Word documents using Copilot.  |
|   |  Presentations created by Copilot  |  The number of times users created PowerPoint presentations using Copilot.  | 
|   |  Presentation summaries created by Copilot  |   The number of times users summarized PowerPoint presentations using Copilot.  |
|   |  Excel analysis actions taken using Copilot  |  The number of times users analyzed data to show insights as charts, PivotTable objects, summaries, trends, or outliers in Excel using Copilot.  |
|   | Excel formulas created by Copilot |  The number of times users generated new columns with formulas based on Excel data using Copilot.  |
|   |  Excel formatting actions taken using Copilot  |  The number of times users highlighted, sorted, and filtered tables in Excel using Copilot. |

### Sentiment

Located within the Impact page, this section provides information that helps you assess Copilot impact from the perspective of users' subjective experiences. In the main table on this page you’ll see a list of Microsoft’s recommended Copilot survey questions along with the results from your own organization’s latest survey (if an admin chooses to upload results for visualization here) and Microsoft's own benchmark results from a [study of early Copilot users](https://www.microsoft.com/worklab/work-trend-index/copilots-earliest-users-teach-us-about-generative-ai-at-work).

**Sentiment results by group**

With a Viva Insights subscription, this section of the dashboard also lets you explore the breakdown of sentiment across organizational attributes. You can use custom filters to isolate the results for specific parts of the organization or for specific employee groups. The results are shown in a “heat map.” 

:::image type="content" source="images/copilot-dash-sentiment-ga.png" alt-text="Screenshot that shows the Sentiment heat map." lightbox="images/copilot-dash-sentiment-ga.png":::

#### Upload survey results with the advanced insights app

*Applies to: Viva Insights admin* 

If you have a Viva Insights subscription and you’re a **Viva Insights admin**, you can upload survey results as a .csv file.

Your survey should include each of the following statements:

* *Using Copilot helps improve the quality of my work or output*

* *Using Copilot helps me spend less mental effort on mundane or repetitive tasks*

* *Using Copilot allows me to complete tasks faster*

* *When using Copilot I am more productive*

If you upload survey results via .csv file, regardless of the format of survey responses you received, the data needs to be uploaded in a standard format that Viva Insights can understand. It’s possible that different survey tools provide outputs in different formats for the survey. Some tools might provide a 5-point scale, some may provide output as a string (“Strongly agree,” “agree,” “neutral,” “disagree,” or “strongly disagree”), and tools like Glint would provide a precalculated score as the output.

Therefore, the admin must convert the survey responses to a 100-point scale, with 100 representing the most positive survey response.

This is how they can convert the scores into a 100-point scale:

If the survey output is a 5-point rating:

| Survey output (rating) | Normalized 100-point scale |
|---|---|
| 1 | 0 |
| 2 | 25 |
| 3 | 50 |
| 4 | 75 |
| 5 | 100 |

Or, if the survey output is in a string format:

| Survey output (strings) | Normalized 100-point scale | 
|----|---|
| Strongly disagree | 0 |
| Disagree | 25 |
| Neutral | 50 |
| Agree | 75 |
| Strongly agree | 100 |

>[!Important]
>The admin must upload the questions in the same order in which they’re shown below.

| Column name in CSV file | Actual question | 
|----|----|
| Question 1 | *Using Copilot helps improve the quality of my work or output* |
| Question 2 | *Using Copilot helps me spend less mental effort on mundane or repetitive tasks* |
| Question 3 | *Using Copilot allows me to complete tasks faster* |
| Question 4 | *When using Copilot I am more productive* |

**Format of the .csv file:** The.csv file itself should also be formatted like this:

| User AAD ID/Email address | Question 1 | Question 2 | Question 3 | Question 4 | 
|----|----|----|----|----|
| abc@test.com | 75 (Normalized score) | 25 (Normalized score) | 0 (Normalized score) | 100 (Normalized score) | 
| xyz@test.com | 25 | 75 | N/A | 100 | 

The cells for the responses may contain “N/A” values for employees who did not respond to the question.

For additional guidance on how to format your .csv file, refer to this example formatted .csv: [Impact Dashboard survey sample file](https://go.microsoft.com/fwlink/?linkid=2260529).

Once you’ve formatted the .csv file accordingly, use these steps to upload it:

1. In the Viva Insights analyst experience, select **Survey data**.

2. Under Survey data at the top, select **Data connections**, then select **Manage data sources**.

3. Under **M365 Copilot Impact Survey data upload**, select **Start**. If you previously uploaded survey data, this new import will replace the old data.

   :::image type="content" source="images/copilot-dash-upload-01.png" alt-text="Screenshot that shows the first steps to upload the survey data." lightbox="images/copilot-dash-upload-01.png":::

4. On the next page, enter an optional survey name and start and end dates. Then browse to find your .csv file, and select **Upload**.

   :::image type="content" source="images/copilot-dash-upload-02.png" alt-text="Screenshot that shows the final steps to upload the survey data.":::

### News & research

*Applies to: Employee users* 

Under the Learning tab, here you’ll find research around the impacts of AI on workplace productivity. With a Viva Insights subscription, you’ll also find exclusive content. Use this page to stay up to speed on the latest findings from Microsoft’s own AI research teams.

## Add Copilot metrics to your custom person query

*Applies to: Viva Insights analyst*

You can also add Microsoft 365 Copilot metrics to your custom person query. Learn how in [Add metrics](../advanced/analyst/person-query.md#add-metrics).

## FAQs

### Setup and licenses

**Where can users access the Microsoft Copilot Dashboard?**
Employees can view the dashboard in the Viva Insights Teams or web app.

**How long after enablement can users access the Copilot dashboard?**
Users can access the dashboard less than 24 hours after being enabled.

**Who is considered a Copilot licensed employee?**
Any employee who has been assigned a Copilot license, including the following service plans:

* Microsoft 365 Copilot in Productivity Apps
* Microsoft 365 Copilot in Microsoft Teams
* Connectors and Plugins for Microsoft 365 Copilot
* Business Chat
* Intelligent Search

**After I assign new Viva Insights licenses for the first time, how long will it take for the Copilot Dashboard to turn on with the data?**
To start data processing, you'll need to assign at least 10 licenses. Once you do that, the process will take about three to five days. [Learn how to assign licenses](../advanced/setup-maint/assign-licenses.md#assign-licenses).

**After the dashboard is turned on with the data, if I subsequently assign *new* Viva Insights licenses, how long will it take for the new data to reflect in the dashboard?**
Once you assign a new license to your employees, it will take up to two weeks to update and include the employees with the new assigned license.

**If I assign new Copilot licenses to people with existing Viva Insights licenses, when will I see their data in the dashboard?**
Once you assign a new Copilot license to your employees, it will take up to one week to update and include the employees with the new assigned license.

**If I reassign Copilot licenses to different employees who did not previously have Copilot licenses, how does that impact the measured group on each page of the dashboard?**
The measured period includes all employees who were enabled for Copilot at any point during that time period. This means that employees who had a license that was reassigned will still be included in the metrics. 

**If I don’t assign any new licenses, when and how often does the dashboard data update?**
The dashboard refreshes with updated data every Tuesday.

**What can enabled users see in the dashboard?**
The dashboard’s advanced features provide more granular views of Copilot adoption, usage patterns, user sentiment, and return on investment across groups, functional roles, and more. Business leaders who have a Viva Insights license and access to the dashboard can apply filters and group the Copilot adoption and impact metrics by organizational attributes such as organization and job function. And, Viva Insights analysts can create custom reports based on these metrics.

**How often is the default-on enablement updated?**
To capture organizational changes, we refresh the default-on enablement on a weekly basis.

**If a user is removed, will the default-on enablement refresh impact their access settings?**
No. Once an admin disables a user, that setting is permanent until the admin enables them again. In the Microsoft 365 admin center, the admin can view a list of who has been disabled in the Deleted tab.

**How does data in the Copilot dashboard compare to usage reports in the admin center?**
Both the Microsoft Copilot dashboard and the admin center usage reports leverage the same underlying data set.

Differences in the data are often caused by one of the following:

* Users must be assigned a Viva Insights license to be measured in the Copilot dashboard. This prerequisite is not required for the admin center report.
* The time frame for which the analysis is being applied may be different.  
* Data in the Copilot dashboard is aggregated to meet a minimum privacy threshold.

**Why are the values for Copilot licensed users or Copilot active users different between the Readiness and Adoption pages?** This is because only Viva Insights licensed employees are included in the Adoption and Impact pages.

### Missing data

**The values I'm seeing are just "--," with a banner that reads, "It looks like your organization doesn’t use Copilot in Microsoft 365 yet." What's happening?**
In this scenario, your employees don't have a Copilot license assigned or they haven't used Copilot yet.

**Why can't I see my senior leadership members as a selectable option within the Scope dropdown menu?**
In this scenario, your Entra data is not reliable, or it does not accurately reflect the reporting structure at your company. Please reach out to your global admin to see how your Entra data is set up.

### Metrics

**How are the scope, organization, and job function filters determined?**

* Scope: Scope is populated using the "ManagerID" field from Entra ID by default. If the Insights admin [uploads organizational data](../advanced/admin/prepare-org-data.md), the ManagerID from the uploaded data file is used to populate selections available for “Your group.”

* Organization: If the Insights admin [uploads organizational data](../advanced/admin/prepare-org-data.md), the uploaded "Department" field is used in the dashboard. If the file is not uploaded, the field uses the organization field from Entra ID.

* Job function: If the Insights admin uploads an [organizational data file](../advanced/admin/prepare-org-data.md), the uploaded "FunctionType" field is used in the dashboard. If the file is *not* uploaded, the field is not available as a filter in the dashboard.

**Which apps are the Copilot chat metrics based on?**
Copilot chat metrics are based on use of Copilot with Graph-ground chat across all apps where the capability is available including Teams, Windows, Microsoft365.com, and more. All prompts submitted via Copilot with Graph-grounded chat are counted towards Copilot chat usage in the Copilot Dashboard, in alignment with the [Copilot Usage report in the Microsoft 365 Admin Center](/microsoft-365/admin/activity-reports/microsoft-365-copilot-usage). Copilot chat metrics do *not* include usage of [Microsoft Copilot with commercial data protection](/copilot/manage), which is made available to users with an eligible Microsoft 365 license and does not require a Copilot for Microsoft 365 license. In certain product environments such as Copilot in the Edge browser, users enabled for Copilot for Microsoft 365 may see a “work/web” toggle. The “work” toggle is a feature of Copilot with Graph-grounded chat usage and thus useage of this feature is accounted for in the Copilot Dashboard. The "web” toggle, however, is a feature of Copilot with commercial data protection and use of this feature is not yet accounted for in the Copilot Dashboard.

**Within the Copilot metrics tab of the comparison between groups table, why does the % difference not show what I'm expecting to see?**  
The values under the first two columns (Group 1 & Group 2) are calculated using the sum. To compare groups of different sizes, the percentage difference is calculated using the per user per month average.