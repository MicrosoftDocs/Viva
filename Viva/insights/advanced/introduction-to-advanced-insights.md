---
ms.date: 02/12/2024
title: Introduction to advanced insights
description: Get familiar with the new advanced insights app from Microsoft Viva Insights 
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Advanced insights introduction

>[!Note]
>To existing customers:
>
>We’ve launched a new version of the advanced insights app, and we’re excited to have our existing Viva Insights customers try its faster, richer experience while continuing to use the legacy advanced insights app. As you make your decision to try out the new app, here’s what we want you to know:  
>
>* We’re still bringing over more specialized features.
>* If you want to use the new app and the legacy app at the same time, we recommend that you upload your organizational data in the legacy app. Uploading data in the new app while also using the legacy app can lead to data inconsistencies between the two platforms.
>
> Otherwise, if you’re ready to start using the new advanced insights app, welcome aboard!
>
>*The link to documentation for the previous platform can be accessed in the legacy application.*

Microsoft Viva Insights provides scope information and research-based behavioral insights into how  an organization gets work done—for example, whether employees maintain work-life balance, how to protect employee wellbeing, and the ways hybrid work affects the employee experience. 

Viva Insights includes the [advanced insights app](https://go.microsoft.com/fwlink/?linkid=2201482), which has advanced analysis tools for deep-diving into data that's shown both within Microsoft Teams and in the app. The advanced analysis tools available in the app include different ways of analyzing and reporting custom analysis to your company’s business leaders.

* Advanced insights [privacy](./privacy/privacy.md) explains what's important to consider for protecting your company's data and how to keep your employee's personal data private.
* [Set up](./setup-maint/setup.md) describes what's required to set up the app before you can use the advanced insights and analysis tools.
* Other documentation provides information on [preparing](./admin/prepare-org-data.md) and [uploading](./admin/upload-org-data-first.md) data, running [queries](./analyst/person-query.md), accessing query [results](./analyst/query-results.md), and using predefined [Power BI templates](./analyst/templates/introduction-to-templates.md).

## Navigation

### Analyst

#### Analysis

As an analyst, the **Analysis** page is your jumping-off point to view recent queries and templates, find documentation and other help, run a custom query, or run a predefined Power BI query. 

##### Query results

Use the **Query results** page to view the results of queries you and other analysts in your organization have run. 

In **Query results**, you can:

* Download query results as CSV, Power BI, or a direct link copied to your clipboard.
* Check a query’s status.
* **Stop** a running query.
* **Edit** or **Delete** queries if you’re the analyst who originally ran them.
* **Favorite** or **Clone** queries.
* Filter by result types.

For more information about the **Query results** page, refer to [Access query results and modify existing queries](./analyst/query-results.md).

##### Metric rules

Create metric rules to leave out certain non-collaboration events from your analyses. Learn more in [Metric rules](../advanced/analyst/metric-rules.md).

##### Data quality

You as an analyst might receive warning messages related to the quality of uploaded data.  

After you select **View data quality**, the app takes you to the **Organizational data** page, which provides a summary of missing or low-quality data and attribute-specific information.

For information about data quality, refer to [Data quality in the analyst experience](./analyst/data-quality-analyst-experience.md).

##### Video demos

Go to **Video demos** to learn more about what you can do with the advanced insights app. The page provides several video walk-throughs, including those about running custom queries, using each Power BI template, and getting familiar with the Viva Insights interface.

In addition to the left pane, you can reach these videos by selecting **Watch demo videos** on the **Help and documentation** menu on the **Analysis** home page.

#### Other features

##### Send feedback

We welcome your feedback on this new platform! Like in other Microsoft products, you can send us feedback through the feedback icon in the top-right of your screen.

### Admin

#### Data hub

As an admin, use the **Data hub** to:

* Get an overview of your data quality, including how many insights are available, how many are low-quality or missing, and how many days it's been since your data was last refreshed.
* Manage your current data sources, including starting a new update or switching sources. To learn how to upload data into Viva Insights, refer to [Upload organizational data (first upload)](../advanced/admin/upload-org-data-first.md).

#### Organizational data

On the **Organizational data** page, check your upload status, view your field mapping results, and download related errors.

For a tour of the **Organizational data** page, refer to [Organizational data overview](../advanced/admin/org-data-overview.md#organizational-data-in-the-advanced-insights-app).

#### Manager settings

In **[Manager settings](./setup-maint/manager-settings.md)**, control who can see [organization insights](../org-team-insights/org-insights.md) in the Viva Insights app in Teams and on the web. Organization insights show managers aggregated wellbeing and productivity insights about their direct and indirect reports based on organizational hierarchy.

#### Privacy settings

Use [**Privacy settings**](setup-maint/setup.md#customize-privacy-settings) to set the minimum group size, prevent sensitive keywords from appearing in any place that uses Viva Insights data, and allow end users to opt out of personal insights and person queries. To learn more about how Viva Insights keeps personal data private, refer to [Privacy](./privacy/privacy.md).

## Related topics

 [!INCLUDE [Viva Insights community](../personal/includes/insights-community.md)]
