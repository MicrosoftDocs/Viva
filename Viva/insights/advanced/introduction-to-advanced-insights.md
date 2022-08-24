---
ROBOTS: NOINDEX,FOLLOW
title: Introduction to advanced insights
description: Get familiar with the new advanced insights app from Microsoft Viva Insights 
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Advanced insights introduction

*The link to documentation for the previous platform can be accessed in the legacy application.*

Microsoft Viva Insights provides scope information and research-based behavioral insights into how  an organization gets works done—for example, whether employees maintain work-life balance, how to protect employee wellbeing, and the ways hybrid work affects the employee experience. 

Viva Insights includes the [advanced insights app](https://go.microsoft.com/fwlink/?linkid=2201482), which has advanced analysis tools for deep-diving into data that's shown both within Microsoft Teams and in the app. The advanced analysis tools available in the app include different ways of analyzing and reporting custom analysis to your company’s business leaders.

* Advanced insights [privacy](./privacy/privacy.md) explains what's important to consider for protecting your company's data and how to keep your employee's personal data private.
* [Set up](./setup-maint/setup.md) describes what's required to set up the app before you can use the advanced insights and analysis tools.
* Other documentation provides information on [preparing](./admin/prepare-org-data.md) and [uploading](./admin/upload-org-data-first.md) data, running [queries](./analyst/person-query.md), accessing query [results](./analyst/query-results.md), and using predefined [Power BI templates](./analyst/templates/introduction-to-templates.md).

## Navigation

### Analyst

### Analysis

As an analyst, the **Analysis** page is your jumping-off point to view recent queries and templates, find documentation and other help, run a custom query, or run a pre-defined Power BI query. 

#### Query results

Use the **Query results** page to view the results of queries you and other analysts in your organization have run. 

In **Query results**, you can:

* Download query results as CSV, Power BI, or a direct link copied to your clipboard.
* Check a query’s status.
* **Stop** a running query.
* **Edit** or **Delete** queries if you’re the analyst who originally ran them.
* **Favorite** or **Clone** queries.
* Filter by result types.
* Mark a query as recurring.

For more information about the **Query results** page, refer to [Access query results and modify existing queries](./analyst/query-results.md)

#### Metric rules

There is one default metric rule for this release of Viva Insights, called **Meeting exclusions**. This rule determines which meetings are excluded from collaboration metrics in Power BI templates, custom queries, and the Viva Insights app in Teams and on the web.

While you can’t customize any metric rules in this release, you’ll be able to soon. For more information about metric rules in Viva Insights, refer to [Metric rules](./analyst/metric-rules.md).

#### Data quality

You as an analyst might receive warning messages related to the quality of uploaded data.  

Once you select **View data quality**, the app takes you to the **Organizational data** page, which provides a summary of missing or low-quality data and attribute-specific information.

For information about data quality, refer to [Data quality in the analyst experience](./analyst/data-quality-analyst-experience.md).

#### Video demos

Go to **Video demos** to learn more about what you can do with the advanced insights app. The page provides several video walk-throughs, including those about running custom queries, using each Power BI template, and getting familiar with the Viva Insights interface.

In addition to the left pane, you can reach these videos by selecting **Watch demo videos** on the **Help and documentation** menu on the **Analysis** home page.

#### Other features

##### Send feedback

We welcome your feedback on this new platform! Like in other Microsoft products, you can send us feedback through the smiley-face icon in the top-right of your screen.

### Admin

The Admin experience in the advanced insights app contains four pages, which are summarized in the following sections.

#### Organizational data

In the **Organizational data** page, you as an admin can check the quality of data that’s already been uploaded, check the status of existing data connections, and upload new data. To learn more about the **Organizational data** page and how to upload data into Viva Insights, refer to [Organizational data overview](../advanced/admin/org-data-overview.md). 

#### Manager settings

On the **[Manager settings](./setup-maint/manager-settings.md)** page, you can enable **Group insights** and control who can see them in the Viva Insights app in Teams and on the web. **Group insights** shows managers aggregated wellbeing and productivity insights about their direct and indirect reports based on organizational hierarchy.

#### Privacy settings

Viva Insights admins can use **Privacy settings** to determine what data your organization wants to exclude from analysis and what data can be visible for advanced insights. To learn more about how Viva Insights keeps personal data private, refer to [Privacy](./privacy/privacy.md).
