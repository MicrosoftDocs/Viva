---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Release Notes for Workplace Analytics Azure Templates
description: Learn about what new Azure Templates or new functionality has been released for Workplace Analytics
author: madehmer
ms.author: v-midehm
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# What's new in Workplace Analytics Azure Templates

Azure templates for Workplace Analytics will continue to develop new templates and add new features and enhancements to the current set of templates. This page will be updated monthly with each new release.

## November 2019

The following new template enhancements are now available.

### Organizational Network Analysis Azure Template

The following enhancements and features are included in the Organizational Network Analysis (ONA) Azure Template.

* Updated UX for Node Measures, including renaming some of the measures, such as:
  * Eigen Centrality is now Influence Index
  * Closeness is now Reach Index
  * Network size is now Degrees
* New UX for saving graphs for subgroup analysis and viewing saved graphs
* Improved UX for defining analysis and saving subsets of data within the graph view.* New metrics available for subgroup analysis, including Boundary Spanning, Bridging Index, Influence Index, and Reach Index.
* New in-depth information about [Measure calculations](./ona-metric-calculations.md) for the Organizational Network Analysis Azure Template.

To learn more, see [Organizational Network Analysis Azure Template](./organization-network-analysis.md).

### Process Explorer Azure Template

The following enhancements and features are included in the Process Explorer Azure Template.

* New download option for datasets.
* New Process Explorer Admin setting that specifies if the template either surfaces and uses, or does not surface or use, email subjects in blob storage datasets to help train the model for categorization:

    ![Categorize email admin setting](./images/pexp-admin-setting.png)

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