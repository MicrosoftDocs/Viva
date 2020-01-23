---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Release Notes for Workplace Analytics Azure Templates
description: Learn about what new Azure Templates or new functionality has been released for Workplace Analytics
author: madehmer
ms.author: madehmer
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# What's new in Workplace Analytics Azure Templates

Azure templates for Workplace Analytics will continue to develop new templates and add new features and enhancements to the current set of templates. This page will be updated monthly with each new release.

## January 2020

The following new template enhancements and changes are in this month's release.

* The **Job Details** information for datasets now includes an **Error Message** column (last on the right) with more information about dataset failures for both the Organizational Network Analysis and the Process Explorer Azure Templates.

### Organizational Network Analysis Azure Template

* A new **Download interaction matrix** option to download a .csv file with the person interactions and related data, such as date range and connection weights by hours and counts.
* When viewing Density graph data in a metrics download (.csv) file, the higher density (*orange*) and lower density (*blue*) cells are highlighted based on the modularity. The color indicates whether or not a group is more or less connected in the network, as compared to what's expected with a random network. See [Density](./organization-network-analysis.md#density) for more details.
* New option for monthly metrics generated for chart data, which computes both individual and group metrics for the set time period and for each month within that time period.
* Reach Index is no longer a chart option.

To learn more, see [Organizational Network Analysis Azure Template](./organization-network-analysis.md).

### Process Explorer Azure Template

* New meeting participants filter option in the **Query Builder** > **Filter Dataset** section for selecting which meetings you want to include in your query results for training the model for categorization purposes. You can use this to filter out meetings where the meeting organizer is outside the filter population.
* A new option to save a set of categorization training models to reuse. After categorizing a good representation of data to train the categorization model for a specific dataset, you can save that model to reuse later by selecting the **Save Categorization Model** option, which appears below the table on the **Dataset** > **Dashboard** page. And then when creating a new dataset, or a subgroup of a dataset, you can use one of these saved categorization training models to help you categorize the new dataset more efficiently.
* Pie chart visuals of categorized data now exclude the **Uncategorized** category, which enables you to focus on and analyze the data that you spent time categorizing.

To learn more, see [Process Explorer Azure Template](./process-explorer.md).

## December 2019

The following new template enhancements are now available.

### Organizational Network Analysis Azure Template

The following enhancements and features are included in the Organizational Network Analysis (ONA) Azure Template.

* Updated UX for Node Measures, including renaming some of the measures, such as:
  * Eigen Centrality is now Influence Index
  * Closeness is now Reach Index
  * Network size is now Degrees
* Preliminary analysis now defaults to the Combined view of the graph. The Network view is only available when the node or link counts are less than the threshold settings defined by your Azure Templates admin in **Admin** > **Configuration**. For details, see [Configuration](./deploy-configure.md#configuration).
* Improved UX for defining analysis and saving subsets of data within the graph view. For details, see [To add new subgroup analysis](./organization-network-analysis.md#to-add-new-subgroup-analysis).
* New metrics available for subgroup analysis, including Boundary Spanning, Bridging Index, Influence Index, and Reach Index.
* New in-depth information about [Measure calculations](./ona-metric-calculations.md) for the Organizational Network Analysis Azure Template.

To learn more, see [Organizational Network Analysis Azure Template](./organization-network-analysis.md).

### Process Explorer Azure Template

The following enhancements and features are included in the Process Explorer Azure Template.

* New download option for datasets.
* Additional options (filters, time range) that help reduce the size of the training dataset for cloud storage, which is required to be less than five million meetings and emails, for improved interactivity when building and training the template model(s) for auto-categorization of the full dataset.
* New Process Explorer Admin setting that specifies if the template shows email subjects and requires categorization to train emails by using a distinct model, or if it trains both email and meetings by using only meeting data.

    ![Categorize email admin setting](./images/pexp-admin-settings.png)

To learn more, see [Process Explorer Azure Template](./process-explorer.md).

## September 2019

The following new template enhancements are now available.

### Process Explorer Azure Template

The following enhancements and features are included in the Process Explorer Azure Template.

* The following new **Admin Classification** options where after you select and save the option in **Admin** > **Configuration**, it'll persist for the life of that scenario:
  * Surface email subjects and classify email and meetings based on distinct models.
  * Do not surface email subjects and classify email based on model training exclusively on meeting data.  
* Improved UX with a new dashboard layout for adding and editing categories, for categorizing meetings and email separately in different dashboards, and for analyzing data.
* If a dataset fails with the **Status** of a red x, you can use the new **Undo** action to revert to the last successfully saved version of the dataset.

To learn more, see [Process Explorer Azure Template](./process-explorer.md).

### Organizational Network Analysis Azure Template

The following enhancements and features are included in the Organizational Network Analysis (ONA) Azure Template.

* Improved UX for adding new analysis.
* New date range options for improved data and graph analysis.
* New **Download metrics** option for the last saved version of the analysis that aligns with the time range, filters, and other values selected.
* Select the new **Parameters** icon to view the parameter details for a listed dataset.

To learn more, see [Organizational Network Analysis Azure Template](./organization-network-analysis.md).

### Admin logs

As an admin, you can now audit user activity in **Admin** > **Logs**. Select the **information** (i) icon in the **Message** column to see more details about a specific  activity.


## August 2019

The following new template and template enhancements are now available.

### Process Explorer Azure Template

This release adds a new Process Explorer template that helps you understand where your organization or team is investing or expending valuable time. You can use this template to categorize processes, projects, meetings, and other activities. You can either upload a .csv dataset for meeting activity or connect to a blob storage location for meeting and email activity.

To learn more, see [Process Explorer Azure Template](./process-explorer.md).

### Organizational Network Analysis Azure Template

The following enhancements and features are included in the Organizational Network Analysis (ONA) Azure Template.

#### Comparative analysis

With the ONA template, you can now view and compare two networks side by side with two browser windows, such as to compare:

* Two different time periods to see how a network has evolved (before and after analysis)
* Between different metrics, such as betweenness and intersectionality, for the same time period
* Two different filters, such as by job title and level designation, for the same time period

#### Density measure

You can now analyze cohesion within groups and across groups by density, which is a new measure in the ONA template. This table view depicts the density score within and across the respective groups.

#### Save and view saved graphs

You can now save a data analysis graph in the template, and then view it as a saved graph later.

To learn more, see [Organizational Network Analysis Azure Template](./organization-network-analysis.md).

## Related topics

* [Workplace Analytics Azure Templates overview](./overview.md)
* [Deploy and configure Workplace Analytics Azure Templates](./deploy-configure.md)