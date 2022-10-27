---
ROBOTS: NOINDEX,FOLLOW
title: Summary of data-protection considerations
description: Data-protection considerations summary when using Microsoft Viva Insights 
author: madehmer
ms.author: helayne
ms.topic: conceptual
ms.localizationpriority: medium 
ms.collection:
- viva-insights-advanced
- viva-insights-leader
- viva-insights-manager 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Data-protection considerations summary

Microsoft Viva Insights analyzes Microsoft 365 collaboration data and organizational (HR) data that you provide. Those who control and process this data have a responsibility to understand how it is analyzed and stored and to carefully plan how to protect it.

>[!Note]
>For more in-depth information, see [Data-protection considerations](Data-protection-considerations.md).

Data that's available within Viva Insights:

* Is not designed or intended to enable employee evaluation, tracking, automated decision-making, profiling, or monitoring.
* Is not intended to give employees access to new personally identifiable information on other coworkers.
* Processes and stores customer data and personal data in accordance with the [Microsoft Online Services Terms](https://www.microsoft.com/licensing/product-licensing/products) and Microsoft's obligations as a [data processor](data-protection-considerations.md#data-processor) under the European Union General Data Protection Regulation (GDPR).
* Can easily be used by customers in compliance with the GDPR.

## Roles and responsibilities

The concepts of _data controller_, _data processor_, and _data subject_ provide a useful framework for thinking about data protection when using Viva Insights.

* **Your organization’s role as Data controller** - The data controller determines the purposes and means of processing a data subject’s personal data. When using Viva Insights, your organization is the data controller because it determines whether, how, and why Viva Insights will process any personal data. For more information, see [Data controller](Data-protection-considerations.md#data-controller).
* **Microsoft’s role as Data processor** - The data processor is a party that processes personal data on behalf of the data controller. When your organization uses Viva Insights, Microsoft is the data processor. For more information, see [Data processor](Data-protection-considerations.md#data-processor).
* **Data subject and personal data** - A data subject is an individual who can be identified through personal data. In the context of Viva Insights, the data subject is an employee or other user in your organization whose personal information is being processed. Personal data is any information that directly or indirectly identifies a person (the data subject).

## Data-privacy recommendations

Consider implementing the following data-privacy recommendations before you begin using Viva Insights.

* **Decide which data types to include** - Before you start an analysis in Viva Insights, consider whether you must include personal data or whether you could use other data that cannot be used to identify specific individuals. For more information, see [Types of data for analysis](Data-protection-considerations.md#types-of-data-used-in-analysis).
* **Develop a clear analysis plan** - You must understand clearly what you want to analyze and why. After you determine what specific questions about your organization you want to answer, consider how Viva Insights might help you find those answers. For more information, see [Develop a clear analysis plan](Data-protection-considerations.md#develop-a-clear-analysis-plan).
* **Consider a DPIA** - If your proposed use of Viva Insights involves processing personal data in a way that could lead to high risks to the rights of employees and other users in your organization, consider completing a data protection impact assessment (DPIA). For more information, see [Determine whether to complete a data protection impact assessment (DPIA)](Data-protection-considerations.md#determine-whether-to-complete-a-data-protection-impact-assessment-dpia).
* **Use aggregated or de-identified data** - To minimize privacy risk, use the minimum data necessary to conduct your research. Note the inherent trade-off: You can, for example, adopt a strict policy that never uses personal data, but this restricts the analyses that Viva Insights can perform. For more information, see [Use aggregated or de-identified data whenever possible](Data-protection-considerations.md#use-aggregated-or-de-identified-data-whenever-possible).

## Decide what data to use

You have full control over what data to include in analysis using Viva Insights. The primary data source is Microsoft 365, but you supplement it with HR and other data from your organization so that you can group information by job title, location, or other attributes.

* **Data provided by Microsoft 365** - Viva Insights uses header information from Microsoft 365 email and calendar items. This information includes sender and recipients and date and subject lines for email; and organizer, attendees, and duration of meetings. For more information, see [Data provided by Microsoft Microsoft 365](Data-protection-considerations.md#data-provided-by-microsoft-365).
* **Privacy capabilities in your control** - You decide which users’ mailboxes to include in your Viva Insights study. You can apply multiple controls over this data to limit it further. For more information, see [Privacy capabilities in your control](Data-protection-considerations.md#privacy-capabilities-in-your-control), [Privacy and data access](/viva/insights/privacy/privacy-and-data-access?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json), and [Assign roles to admins and analysts](../Setup/Set-up-Workplace-Analytics.md#setup-steps).
* **Data provided by your organization** - You control what other information you want to be included in Viva Insights analyses. You must balance the benefits of analyzing along organizational lines with the risks of including the data required to make those analyses. For more information, see [Data provided by your organization](Data-protection-considerations.md#data-provided-by-your-organization).
* **Who can see the data** - You control who gets to see the data and the results of the analysis. Like other products that work with sensitive data, such as HR systems, Viva Insights is not meant for the general workforce. Rather, its users are expected to have been trained in the handling sensitive information. For more information, see [Who can see the data](Data-protection-considerations.md#who-can-see-the-data).

## Handle data-subject requests

Under the General Data Protection Regulation (GDPR), data subjects may have rights to request exclusion from processing, access, and correction, or deletion of their personal data. As the data controller, your organization must evaluate whether a particular data-subject request is valid and then, if appropriate, take action to fulfill it.
For more information about the following request types and how to fulfill them, see [Viva Insights support for handling data subject requests](Data-protection-considerations.md#support-for-handling-data-subject-requests).

* **Exclusion from processing** - Data subjects have the right to have their personal information excluded from processing.
* **Access** - Data subjects have the right to demand what personal information is being processed, and Viva Insights gives you the ability to export the raw data, which may contain personal data.
* **Correction** - Data subjects have the right to rectify their personal data. Viva Insights only performs operations (mostly arithmetic) on data provided to it from other sources, such as email and meeting data from Microsoft 365 or the organizational data that you upload. This data is not corrected through Viva Insights.
* **Deletion** - Data subjects can ask for their personal data to be erased. If a user wishes to have their data removed from a study after the study is completed, then you can expunge that user’s personal data from the raw datasets that were previously processed.
* **Transparency regarding processing** - [Metric descriptions](/viva/insights/Use/metric-definitions?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) discusses in detail the metrics calculated by Viva Insights, and what they mean.

## Additional Resources

* [Viva Insights privacy documentation](/viva/insights/privacy/privacy-and-data-access?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)
* Article 29 Working Party [Opinion 2/2017 on data processing at work](http://ec.europa.eu/newsroom/document.cfm?doc_id=4563)
* EU [General Data Protection Regulation](http://eur-lex.europa.eu/legal-content/EN/TXT/?uri=uriserv:OJ.L_.2016.119.01.0001.01.ENG&toc=OJ:L:2016:119:TOC)
