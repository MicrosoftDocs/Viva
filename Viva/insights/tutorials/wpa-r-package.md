---
ROBOTS: NOINDEX,NOFOLLOW
title: wpa R package
description: Describes the wpa R package, an open-source package of 100+ functions in the R data-analysis language for use with Viva Insights 
author: madehmer
ms.author: helayne
ms.topic: troubleshooting
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# The wpa R package 

The [_wpa R package_](https://microsoft.github.io/wpa/) is an open-source repository of more than 100 functions that provide low-code pre-built analyses. Analysts can use this package to execute custom analyses that go beyond the insights that [Templates](/viva/insights/tutorials/power-bi-intro?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) and Viva Insights [Query designer](/viva/insights/tutorials/query-designer?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) make available. These analyses can help leaders go deeper into the data that Viva Insights provides to solve more specific problems.

>[!Note]
>R is an open-source statistical programming language and one of the most popular toolkits for data analysis and data science. For users of the R language, a "package" is a unit of sharable code that's organized into libraries.  

## Capabilities for analysts

This R package is intended for use by analysts and data scientists who are intermediate-to-advanced users of R or Python. By using the _wpa R package_, an analyst can:

* **Run prebuilt analysis and visualizations** of Viva Insights data with the ability to make settings to use organizational data variables and maintain privacy thresholds.

* **Obtain outputs in multiple formats.** Analysts can easily export these outputs into any format required, including clipboard (copy & paste), Excel, .csv, and – for plots – .png, .svg, and .pdf.

* **Validate data prior to analysis** by running a data validation report, which does systematic checks on, for example, metrics, organizational attributes, and meeting subject lines. The data-validation functions check for patterns such as public holidays, non-knowledge workers, outliers, and missing values in the data to improve the quality and reliability of analysis.

* **Generate prebuilt interactive HTML reports**, which includes reports on data validation, subject-line text mining, and key collaboration metrics.

* Make use of **advanced analytics functions**, such as text mining, network analysis, and hierarchical clustering, all designed specifically for Viva Insights metrics.  

The following illustration shows the experience of creating a visualization of collaboration hours with the _wpa R package_:

![wpa R package visualization.](../images/wpa/tutorials/wpa-r-package-visual.gif)

## Analyst resources

The _wpa R package_, its documentation, and other related resources are available on GitHub in the following locations: 

* [_wpa R package_ source code](https://github.com/microsoft/wpa/)
* [_wpa R package_ documentation](https://microsoft.github.io/wpa/), which includes a quick-start guide, code examples, and other information like the structure of the package.   
* [Submit an issue or a feature request](https://github.com/microsoft/wpa/issues)
* [Full list of functions](https://microsoft.github.io/wpa/reference)

