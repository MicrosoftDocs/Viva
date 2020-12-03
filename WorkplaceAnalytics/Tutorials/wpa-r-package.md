---

title: wpa R package
description: Describes the "wpa R package," an open-source package of 100+ functions in the R data-analysis language for use with Workplace Analytics 
author: paul9955
ms.author: v-pausch
ms.topic: troubleshooting
localization_priority: normal 
ms.prod: wpa
---

# The open-source wpa R package 

The wpa R package is an open-source repository of more than 100 functions that provide low-code pre-built analyses. Analysts can use this package to execute custom analyses that go beyond the insights that [Power BI templates](power-bi-intro.md) and Workplace Analytics [queries](query-basics.md) make available. These analyses can help leaders go deeper into the data that Workplace Analytics provides to solve more specific problems. 

> [!Note] 
> R is an open-source statistical programming language and one of the most popular toolkits for data analysis and data science. For users of the R language, a "package" is a unit of sharable code that's organized into libraries.  

## Capabilities for analysts

This R package is intended for use by analysts and data scientists who are intermediate-to-advanced users of R or Python. With the wpa R package, an analyst can do the following: 

* **Run prebuilt analysis and visualizations** of Workplace Analytics data with the ability to make settings to use organizational data variables and maintain privacy thresholds. They can easily export these outputs into any format required, including clipboard (copy & paste), Excel, .csv, and – for plots – .png, .svg, and .pdf.  
 
* **Validate data prior to analysis** by running a data validation report, which performs systematic checks on, for example, metrics, organizational attributes, and meeting subject lines. The data-validation functions promote good practices of checking for patterns such as public holidays, non-knowledge workers, outliers, and missing values in the data to improve the quality and reliability of analysis.   

* **Generate prebuilt interactive HTML reports**, which includes reports on data validation, subject-line text mining, and key collaboration metrics. 

* Make use of **advanced analytics functions**, such as text mining, network analysis, and hierarchical clustering, all designed specifically for Workplace Analytics metrics.  

In the following illustration, R functions show a visualization of collaboration hours:

![wpa R package visualization](../images/wpa/tutorials/wpa-r-package-visual.gif)

## Analyst resources

The wpa R package and its documentation are available on GitHub. You can find its elements in the following locations: 

* _wpa R package_ source code: https://github.com/microsoft/wpa/
* _wpa R package_ documentation: https://microsoft.github.io/wpa/.  This documentation includes a quick-start guide, code examples, information about the structure of the package, and other information specifically for developers.   
