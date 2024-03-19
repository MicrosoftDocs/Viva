---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 3/14/2024
title: Use Microsoft Copilot Dashboard advanced features with a Viva Insights subscription
description: Explains how to use the Microsoft Copilot Dashboard's advanced features, including filters and Copilot metrics, with a Viva Insights subscription.
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.collection: viva-insights-personal
ms.localizationpriority: medium 
ms.service: viva
ms.subservice: viva-insights
manager: anirudhbajaj
audience: user
---

# Use Microsoft Copilot Dashboard advanced features with a Viva Insights subscription

>[!Important]
>This feature is in private preview. Features in preview might not be complete and could undergo changes before becoming available in the broader public release.

The Microsoft Copilot Dashboard provides actionable insights to help your organization get ready to deploy AI, drive adoption based on how AI is transforming workplace behavior, and measure the impact of Copilot.

Some of the dashboard’s metrics and functionalities are available to any customer with a Microsoft 365 or Office 365 subscription for business or enterprise. [Learn about these features here](./copilot-dashboard.md).

But, if you have a Viva Insights subscription, the dashboard provides an additional set of metrics, filtering options, and other features.

With a Viva or a Viva Insights subscription, the dashboard provides the same categories of metrics as the non-subscription dashboard, but the adoption, impact, and sentiment categories provide additional metrics and filters. [There are also new features for analysts to incorporate Copilot metrics into their person queries](#add-copilot-metrics-to-your-custom-person-query).

>[!Note]
>For these new metrics to appear in the dashboard, the employees being analyzed must be assigned a Viva or Viva Insights license. And, to protect individual privacy, you’ll only see insights when there are at least 25 employees with a Viva or Viva Insights license.

Let's dive in to this advanced set of features.

### Prerequisites

* The advanced dashboard is available to customers who have a Microsoft 365 or Office 365 subscription for business or enterprise, as well as a Viva Insights subscription.

* A Viva Insights license is required to view the app in Teams for leaders, and the analyst tool bench is required for custom reports. Requires Viva Insights, Workplace Analytics and Feedback, or Viva Suite SKUs.

* At least 25 licenses of Viva Insights SKUs should be assigned before the dashboard is enabled. [Learn how to assign licenses](../advanced/setup-maint/assign-licenses.md). To see more meaningful insights, you should enable at least 100 licenses.

### Manage access to the dashboard

*Applies to: Microsoft 365 global admin or Privileged Role Administrator*

[Use these steps to manage user access to the dashboard's metrics](./copilot-dashboard.md#manage-user-access-to-the-dashboard-in-viva-insights).

### Select the Scope of your analysis

At the top left of the adoption and impact page, next to **Scope**, select the dropdown to choose between viewing insights for individual teams within your entire company, or teams just within your group. You can also filter by team by selecting **View by** above the various metric reports.

:::image type="content" source="images/copilot-dash-scope.png" alt-text="Screenshot that shows the Scope tool.":::

To protect individual privacy, you can only view aggregated metrics for teams that have at least 25 users.

## Interpreting the data

### Adoption

After you've deployed Copilot in your organization, this page allows you to track user adoption trends per Microsoft 365 app and Copilot feature. 

The page included with an M365 subscription displays aggregate metrics at the tenant level. [Learn about these metrics](./copilot-dashboard.md#adoption).  

With a Viva Insights subscription, the page consists of metrics for employees who have a Viva or Viva Insights license. With this version of the dashboard, three main insights are covered.

At the top of the page, you’ll see tallies for **Copilot licensed employees**, and **Active Copilot users**. Let’s define these terms.

* **Copilot licensed employees**: The total number of employees with a Copilot license.

* **Active Copilot users**: Employees who performed at least one Copilot activity in the previous 28 days.

Now let’s look at the insights provided by this page.

**Insight #1: High-level overview of Copilot usage across the organization**

:::image type="complex" source="images/copilot-dash-adoption-01.png" alt-text="Screenshot that shows the first group of adoption metrics." lightbox="images/copilot-dash-adoption-01.png":::
Screenshot that shows the first group of adoption metrics.
:::image-end:::

**Insight #2: Breakdown of Copilot usage across different M365 apps**

:::image type="complex" source="images/copilot-dash-adoption-02.png" alt-text="Screenshot that shows the second group of adoption metrics." lightbox="images/copilot-dash-adoption-02.png":::
Screenshot that shows the second group of adoption metrics.
:::image-end:::

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

* **Copilot actions taken**: The total number of actions taken using Copilot across M365 apps.

* **Copilot assisted hours**: This is an estimate of the total time employees were assisted by using Copilot over the past 28 days. Employees can re-invest time savings from Copilot in learning, training, skilling, and having a greater business impact. The metric is computed based on your employees’ actions in Copilot and multipliers derived from [Microsoft’s research on Copilot users](https://www.microsoft.com/worklab/work-trend-index/copilots-earliest-users-teach-us-about-generative-ai-at-work). The metric should be viewed as a general estimate based on the most relevant Copilot usage data and research currently available. The underlying calculation methodology will evolve over time as new information becomes available. See more information on the calculation below.

#### Details on the "Copilot assisted hours" metric
 
The **Copilot assisted hours** metric is a general estimate that tries to leverage the latest research on AI and productivity to describe your employees’ use of three types of Copilot capabilities described in the table below. Copilot usage metrics are aggregated within each category, then multiplied by an assistance factor to determine hours assisted per category. The three resulting values are then added together to produce the final **Copilot assisted hours** metric. Please note that these are broad approximations based on the [best available research rather than precise calculations](https://www.microsoft.com/research/project/the-new-future-of-work). As more research becomes available, we will update our approach.

| Copilot capability | Metric(s) counted | Assistance factor | Source of assistance factor (if applicable) |
|---|---|---|---|
| Meeting summaries | Meeting hours summarized by Copilot | The full duration of each meeting summarized is counted towards total assisted hours (e.g. if a user summarizes an hour-long meeting after it has ended, that counts as one assisted hour). | N/A |
| Search and summaries | Copilot chat queries submitted <br> <br/> Email thread summaries created by Copilot <br> <br/> Document summaries generated by Copilot <br> <br/> Presentations summarized by Copilot <br> <br/> Spreadsheet analyses completed using Copilot <br> <br/> Chat threads summarized by Copilot | 6 minutes per search or summary action  | In a study of 163 knowledge workers, users were able to retrieve information across files, emails, and calendars 6 minutes faster with Copilot versus without Copilot. See study #4 in section 2 of [this blog post](https://www.microsoft.com/worklab/work-trend-index/copilots-earliest-users-teach-us-about-generative-ai-at-work). |
| Creation | Email coaching actions using Copilot <br> <br/> Email drafts generated by Copilot <br> <br/> Documents drafted by Copilot <br> <br/> Presentations created using Copilot <br> <br/> Rewrite text actions taken using Copilot <br> <br/> Excel formula calculations completed using Copilot <br> <br/> Excel formatting actions completed using Copilot <br> <br/> Chat messages composed using Copilot | 6 minutes per creation action  | In a study of 147 knowledge workers, people were able to complete a writing task (drafting a blog post) 6 minutes faster with Copilot versus without Copilot. See study #1 in section 2 of [this blog post](https://www.microsoft.com/worklab/work-trend-index/copilots-earliest-users-teach-us-about-generative-ai-at-work). Creation is especially difficult to summarize in a single number, so this number should be in particular understood to be a broad estimate. As research improves, we will adjust our methodology. |

**Key insights for this page:**

On any card, select **Explore more** to dive into these metrics.

##### Actions before and after Copilot

See how employee behaviors have changed before and after Copilot usage.

* **Before Copilot** is computed as the monthly average per user for that metric over the last four weeks from the date of the user’s first activity on Copilot. The population analyzed for these metrics is defined as the users who performed any activity with Copilot at least once in the last 28 days.

* **After Copilot** is computed as the recent 28-day average per user for that metric, where the population analyzed is defined as the users who performed any activity with Copilot at least once in the last 28 days.

* **% Difference after Copilot is computed as**: (Value of the **After Copilot** metric – Value of the **Before Copilot** metric) / Value of the **Before Copilot** metric.

>[!Important]
>For the comparisons described below, please note that correlation does not equal causation. The differences you see might not be driven by Copilot.

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

Located within the Impact page, this section provides information that helps you assess Copilot impact from the perspective of users' subjective experiences. In the main table on this page you’ll see a list of Microsoft’s recommended Copilot survey questions along with the results from your own organization’s latest survey (if an admin chooses to upload results for visualization here) and Microsoft’s own benchmark results from a [study of early Copilot users](https://www.microsoft.com/worklab/work-trend-index/copilots-earliest-users-teach-us-about-generative-ai-at-work).

**Sentiment results by group**

With a Viva Insights subscription, this section of the dashboard also lets you explore the breakdown of sentiment across organizational attributes. You can use custom filters to isolate the results for specific parts of the organization or for specific employee groups. The results are shown in a “heat map.” 

:::image type="complex" source="images/copilot-dash-premium-sentiment.png" alt-text="Screenshot that shows the Sentiment heat map." lightbox="images/copilot-dash-premium-sentiment.png":::
Screenshot that shows the Sentiment heat map.
:::image-end:::

#### Upload survey results with the advanced insights app

If you have a Viva Insights subscription and you’re a Viva Insights admin, you can upload survey results as a .csv file.

Or, you can upload survey results in the Microsoft 365 admin center. [Learn how](/microsoft-365/admin/adoption/ai-assistance).

We recommend delivering a survey to users in which you ask them to indicate the extent to which they agree with the following four statements:

* *Using Copilot helps improve the quality of my work or output*

* *Using Copilot helps me spend less mental effort on mundane or repetitive tasks*

* *Using Copilot allows me to complete tasks faster*

* *When using Copilot I am more productive*

If you upload survey results via .csv file, regardless of the format of survey responses you received, the data needs to be uploaded in a standard format that Viva Insights can understand. It’s possible that different survey tools provide outputs in different formats for the survey. Some tools might provide a 5-point scale, some may provide output as a string (“Strongly agree,” “agree,” “neutral,” “disagree,” or “strongly disagree”), and tools like Glint would provide a precalculated score as the output.

Therefore, the admin must convert the survey responses to a 100-point scale to maintain consistency with Glint, with 100 representing the most positive survey response.

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

For additional guidance on how to format your .csv file, [refer to this example formatted .csv here](https://go.microsoft.com/fwlink/?linkid=2260529).

Once you’ve formatted the .csv file accordingly, use these steps to upload it:

1. In the Viva Insights analyst experience, select **Survey data**.

2. Under Survey data at the top, select **Data connections**, then select **Manage data sources**.

3. Under **M365 Copilot Impact Survey data upload**, select **Start**. If you previously uploaded survey data, this new import will replace the old data.

   :::image type="complex" source="images/copilot-dash-upload-01.png" alt-text="Screenshot that shows the first steps to upload the survey data." lightbox="images/copilot-dash-upload-01.png":::
   Screenshot that shows the first steps to upload the survey data.
   :::image-end:::

4. On the next page, enter an optional survey name and start and end dates. Then browse to find your .csv file, and select **Upload**.

   :::image type="complex" source="images/copilot-dash-upload-02.png" alt-text="Screenshot that shows the final steps to upload the survey data." lightbox="images/copilot-dash-upload-02.png":::
   Screenshot that shows the final steps to upload the survey data.
   :::image-end:::

### News & research

Under the Learning tab, here you’ll find research around the impacts of AI on workplace productivity. With a Viva Insights subscription, you’ll also find exclusive content. Use this page to stay up to speed on the latest findings from Microsoft’s own AI research teams.

## Add Copilot metrics to your custom person query

*Applies to: Viva Insights analyst*

You can also add Microsoft 365 Copilot metrics to your custom person query. These metrics provide insights around how employees are using Microsoft Copilot with Microsoft 365 apps, and they’re part of your .csv output file. To include these metrics when you’re setting up your query, select **Include Microsoft 365 Copilot metrics in this query**.

[Learn more about how to set up custom person queries](../advanced/analyst/person-query.md).

Here is a list of these Copilot metrics that you can use for your query:

| Metric | Description | Date from when the data is available and the customers can view |
|---|---|---|
| Meetings summarized by Copilot |  The number of meetings summarized by Copilot.  | 10/15/2023 |
| Chat conversation summaries created by Copilot | The number of times users summarized chats and channel conversations in Teams using Copilot. | 10/15/2023 |
| Chat message drafts composed using Copilot  | The number of chat and channel message drafts created in Teams using Copilot. | 10/15/2023 |
|  Email drafts generated by Copilot  |  The number email drafts users generated using Copilot.  | 11/15/2023 |
|  Email coaching actions taken using Copilot  | Number of times users selected email coaching with Copilot.  | 11/15/2023 |
| Email thread summaries created by Copilot  | Number of times users summarized email conversations with Copilot.  | 11/15/2023 |
| Document drafts created by Copilot | The number of times users drafted Word documents with Copilot. | 10/15/2023 | 
| Document summaries created by Copilot |  The number of times users summarized Word documents using Copilot.  | 10/15/2023 | 
|  Presentations created by Copilot  | Number of times users created PowerPoint presentations with Copilot.  | 10/15/2023 |
|  Rewrite text actions taken using Copilot  | Number of times users  modified Word documents with Copilot.  | 10/15/2023 |
|  Presentation summaries created by Copilot  | Number of times users  summarized PowerPoint presentations with Copilot.  | 10/15/2023 | 
|  Excel analysis actions taken using Copilot  | Number of times users analyzed data to show insights as charts, PivotTable objects, summaries, trends, or outliers in Excel with Copilot.  | 10/15/2023 |
| Excel formulas created by Copilot | Number of times users generated new columns with formulas based on Excel data with Copilot.  | 10/15/2023 | 
| Excel formatting actions taken using Copilot | Number of times each user highlighted, sorted, and filtered tables in Excel with Copilot.  | 10/15/2023 | 
|  Meetings summarized by Copilot  | Number of meetings summarized with Copilot per user.  | 12/18/2023 |
| Meeting hours summarized by Copilot  | The number of hours of meetings summarized by Copilot. | 12/18/2023 |
| Chat conversations summarized by Copilot |  The number of chats and channel conversations summarized by Copilot.  | 12/18/2023 |
| Emails sent using Copilot | The number of emails sent with assistance from Copilot. | 11/15/2023  |
| Copilot actions taken in Copilot chat  | The number of Copilot actions completed by active Copilot users in Copilot chat. | 10/15/2023 |
| Copilot actions taken in Excel  | The number of Copilot actions completed by active Copilot users in Excel.  | 10/15/2023 |
| Copilot actions taken in Outlook  | The number of Copilot actions completed by active Copilot users in Outlook.  | 10/15/2023 |
| Copilot actions taken in PowerPoint  | The number of Copilot actions completed by active Copilot users in PowerPoint.  | 10/15/2023 |
| Copilot actions taken in Teams  | The number of Copilot actions completed by active Copilot users in Teams.  | 10/15/2023 |
| Copilot actions taken in Word  | The number of Copilot actions completed by active Copilot users in Word.  | 10/15/2023 |
| Copilot active days in Excel | The number of days the user actively used Copilot in Excel.  | 10/15/2023 |
| Days of active Copilot usage in Loop | The number of days the user was actively using Copilot in Loop.  | 10/15/2023 |
|  Days of active Copilot usage in OneNote  |  The number of days the user was actively using Copilot in OneNote.  | 10/15/2023 |
|  Days of active Copilot usage in Outlook  |  The number of days the user was actively using Copilot in Outlook.  | 10/15/2023 |
| Days of active Copilot usage in PowerPoint | The number of days the user was actively using Copilot in PowerPoint. | 10/15/2023 |
|  Days of active Copilot usage in Teams  |  The number of days the user was actively using Copilot in Microsoft Teams.  | 10/15/2023 |
| Days of active Copilot usage in Word |  The number of days the user was actively using Copilot in Word.  | 10/15/2023 |
|  Days of active Copilot usage in Copilot chat  |  The number of days the user was actively using Copilot chat.  | 10/15/2023 |
| Copilot enabled days for Copilot chat  |  The number of days the user had Copilot with Graph-grounded chat enabled.  | 10/15/2023 |
| Copilot enabled days for Power Platform connectors | The number of days the user had Power Platform Connectors in Copilot for Microsoft 365 enabled. | 10/15/2023 |
| Copilot enabled days for productivity apps  | The number of days the user had a Microsoft Copilot apps service plan enabled.  | 10/15/2023 |
| Copilot enabled days for Intelligent Search | The number of days the user had an Intelligent search service plan enabled.  | 10/15/2023 |
| Copilot enabled days for Teams  | The number of days the user had a Microsoft Copilot Teams service plan enabled.  | 10/15/2023 |


### FAQs

**Where can users access the Microsoft Copilot Dashboard?**
Employees can view the dashboard in the Viva Insights Teams or web app.

**What can enabled users see in the dashboard?**
The dashboard’s advanced features provide more granular views of Copilot adoption, usage patterns, user sentiment, and return on investment across groups, functional roles, and more. Business leaders who have a Viva Insights license and access to the dashboard can apply filters and group the Copilot adoption and impact metrics by organizational attributes such as organization and job function. And, Viva Insights analysts can create custom reports based on these metrics.

**How often is the default-on enablement updated?**
To capture organizational changes, we refresh the default-on enablement on a weekly basis.

**If a user is removed, will the default-on enablement refresh impact their access settings?**
No. Once an admin disables a user, that setting is permanent until the admin enables them again. In the Microsoft 365 admin center, the admin can view a list of who has been disabled in the Deleted tab.

**The values I'm seeing are just "--," with a banner that reads, "It looks like your organization doesn’t use Copilot in Microsoft 365 yet." What's happening?**
In this scenario, your employees have a Viva Insights license, but they do not have a Copilot license.

**For the Copilot metric reports with filters, the values I'm seeing are just "--," but I see the other data. What’s happening?**
To protect individual privacy, you’ll only see insights when there are at least 25 employees with a Viva or Viva Insights license. This is the minimum amount for viewing insights across groups.

**The values I'm seeing are just "--," with a banner that reads, "Not enough activity data to show insights." What's happening?**
In this scenario, there are fewer than 25 employees with a Viva or Viva Insights license, and there are fewer than 25 employees with a Copilot license.

**Why can't I see my senior leadership members as a selectable option within the Scope dropdown menu?**
In this scenario, your Entra data is not reliable.