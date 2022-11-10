---
ROBOTS: NOINDEX
title: Data-protection considerations for manager, leader, and advanced insights 
description: Data-protection considerations when using Microsoft Viva Insights
author: lilyolason
ms.author: v-lilyolason
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

# Data-protection considerations

By using data generated from everyday work in Microsoft 365, the different Microsoft Viva Insights features help people understand how they spend their limited time and who they spend it with, and then presents intelligent tips on how to work smarter.

The following includes a basic overview of the roles, responsibilities, types of data, and data-privacy recommendations. The general suggestions offered here are a starting point for planning your data-protection strategy and deployment. These are not intended as a substitute for addressing your organization’s unique needs by engaging with legal, privacy, human-resources, and other subject matter experts within your organization.

## Roles and responsibilities

The concepts of [data controller](#data-controller), [data processor](#data-processor), and [data subject](#data-subject) originate in European privacy law. Regardless of where your organization is located or whether any personal data of European Union citizens is involved, these concepts provide a useful framework for thinking about data protection when using Viva Insights.

The following graphic shows the central position of the data controller (your organization) between the data subject (left) and the data processor, Microsoft (right):

![Roles in data protection.](../images/data-subject-controller-processor.png)

Before setting up Viva Insights, first consider the respective roles and responsibilities of your organization and of Microsoft to protect personal data and honor the rights of data subjects.

### Data controller

The data controller is a party that determines the purposes and means of processing a data subject’s personal data.

When using Viva Insights, your organization is the data controller because your organization determines if, how, and why Viva Insights processes any personal data.

As a data controller, your organization should:

* Determine the scope of data to analyze and the purpose and objectives of the analysis.
* Work with your organization’s legal, privacy, and human resources teams for the following tasks:

  * Determining whether you should obtain consent from employees in your company.
  * Determining what information you provide to employees about how your organization will process their personal data in Viva Insights.
  * Accounting for local or country-specific considerations.

>[!Note]
> Some countries require employers to consult with employee representatives or seek approval from a works council before deploying certain information technology in the workplace, while others restrict when and how employers can process certain employee data. For example, if your company has employees in Germany or Netherlands, then you should consider if works council engagement or approval is required. Moreover, Viva Insights processes data from employee communications, which could be considered “communications data” (including “traffic data”) in Finland. Thus, if your company has employees in Finland, then you should understand how Finnish laws apply to the processing of employee personal data and communications or traffic data to determine if use of Viva Insights is permissible.

* Use Viva Insights privacy controls to direct what data will be analyzed, how data will appear in results, and who will have access to both raw data and the results of analysis.
* Review and be familiar with this document and other Viva Insights [privacy documentation](/viva/insights/privacy/privacy-and-data-access?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) provided by Microsoft.

### Data processor

The data processor is a party that processes personal data on behalf of the data controller. When your organization uses Viva Insights, Microsoft is the data processor.

As a data processor, Microsoft will:

* Process personal data in accordance with your organization’s instructions as directed through your settings configuration within Viva Insights.
* Through your use of Viva Insights, process all data provided to Microsoft (including personal data) according to the same [general privacy and security terms in the Online Services Terms (OST)](http://microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46) as Microsoft 365.
* As part of Microsoft’s commitments under the OST, remain certified under the EU-U.S. and Swiss-U.S. Privacy Shield Frameworks and the commitments that these frameworks entail to legitimize transfers of personal data from the EU and Switzerland to the U.S.
* Contractually commit to abide by applicable provisions of the European Union General Data Protection Regulation (GDPR), effective starting May 25, 2018.
* Provide Viva Insights features that help organizations meet their data-controller obligations and honor data-subject rights under the GDPR, including the right of exclusion from processing, access, and erasure, and including the right of transparency regarding methods of processing.
* Implement technical and organizational security measures to protect the confidentiality of your organization’s (and employees’) data in Viva Insights.

In addition, Microsoft does not use data for advertising nor does it volunteer to provide data to law enforcement.

### Data subject

A data subject is a person who can be identified through personal data. In the context of Viva Insights, the data subject is an employee or other user in your organization whose personal information is being processed. Personal data is any information that directly or indirectly identifies a person (the data subject).

>[!Note]
>In most cases in the Viva Insights product and documentation, we refer to a _data subject_ simply as a "user," a "person," an "individual," or an "employee."

## De-identification of data

To keep from disclosing personal data, Viva Insights de-identifies user data. See [De-identification of personal data](/viva/insights/privacy/de-identify-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) for details.  

## Types of data used in analysis

Before using the advanced insights app and its analysis tools or using manager and leader insights, you should think about the types of data that you might see and could include in advanced analysis. Specifically, consider whether the inclusion of personal data is necessary to fulfill the purpose of the analysis, or whether other types of data that cannot be used to identify specific individuals could produce results that are as effective and insightful as you would get if you had used personal data.

Your organization might have its own data-classification system, but you might wish to consider the following types of data when you implement Viva Insights:

| Privacy risk | Data type | Definition | Examples in Viva Insights |
| ------------ | --------- | ---------- | ----- |
| Highest | Personal data | Personal data is information that directly or indirectly identifies a person | By default, Viva Insights de-identifies email addresses and other information from Microsoft 365 or Azure Active Directory that directly identifies an individual in any in-product dashboard or query result. However, it does show information from the organizational dataset that your organization provides for analysis. Thus, if you upload organizational data that includes personal data (for example, employee names and identification numbers), that personal data will appear in the in-product dashboards and in query results. |
| Higher | Pseudonymized data | Pseudonymized data is information in which a personal identifier has been replaced with a value that does not directly identify a person (such as a numeric identifier that can no longer be attributed to a specific person without the use of additional information). | Viva Insights automatically replaces email addresses with pseudonyms (cryptographically obscured strings of numbers and letters) in the Microsoft 365 collaboration data that you choose to include for analysis. Using pseudonyms can reduce the likelihood that you will identify a specific person, but the risk of identification remains. |
| Lower | Aggregated data | Aggregated data is information that is computed from multiple individuals or sources. | Viva Insights calculates averages across your organization. Since the averages are calculated from data sourced from many people, it becomes nearly impossible to derive information about a specific person’s activity. The likelihood of identifying someone from aggregated data depends on the size of the sample. When you implement Viva Insights for your organization, you must select the sample-size threshold for aggregation. Smaller sample sizes (such as fewer than 10 people) might reveal some insights about individual activity, especially when the individuals are known, and other information (for example, whether the individual was on vacation) can be correlated with changes in the averages over time. |
| Lowest | De-identified data | De-identified data is information that does not relate to a specific individual, that does not increase the likelihood that a specific individual can be identified, or that has been rendered in a way so that it cannot be used to identify a specific individual. | When you use the default settings in Viva Insights, all the computed metrics that are the output of an analysis will be de-identified data. |

## Data-privacy recommendations

Consider implementing the following data-privacy recommendations before you begin using Viva Insights.

### Develop a clear analysis plan

By using advanced analysis tools in the advanced insights app, you can process data in many ways, so before you begin, it is important to have a clear purpose about what you want to analyze and why. Determine what specific questions about your organization you want to answer, and then consider how Viva Insights might help you find those answers.

Having a clear question and then determining how a data analysis from Viva Insights will answer the question serves the following goals:

* Keeps your efforts focused on a limited purpose and helps prevent your analysts from simply sifting through the analysis data.
* It helps you scope the data to use and avoid privacy pitfalls such as including more data than is necessary, retaining data for longer than is necessary, and failing to be transparent with employees about how their personal data might be used.
* To the extent your organization is subject to GDPR, planning your analysis is a key step in determining and documenting legitimate interest in processing personal data with Viva Insights.

### Determine whether to complete a data protection impact assessment (DPIA)

The degree of privacy risk to employees and other users in your organization is largely within your control. That risk depends primarily on the organizational dataset that you will import into the advanced insights app and how you will use that data.

After you have developed an analysis plan but before you begin processing data in the advanced insights app, determine whether you need to complete a DPIA. If your proposed use of Viva Insights involves processing personal data in a manner that could lead to high risks to the rights of employees and other users in your organization, completing a DPIA might be warranted. If you are unsure whether a DPIA is required, consult your organization’s privacy subject matter experts, such as legal or HR personnel.

Higher-risk data includes sensitive demographic data, such as racial or ethnic origin, sex or gender, and trade union membership. Higher-risk uses of Viva Insights include using the service for profiling or to make automated decisions or predictions about employees. (Note that Microsoft designed Viva Insights to help people within organizations _make_ data-driven decisions, not to _automate_ those decisions.)

If you determine that a DPIA is necessary for your proposed use of Viva Insights, you will need to document several aspects of how you will use the service to process personal data, including how the data will be collected; how it will be processed; the necessity of the processing in relation to the purpose; what risks the processing presents to employees; the data flows within and outside Viva Insights; feedback that you received from employees regarding the proposed data processing; and any other information that your organization’s data-protection officer (or equivalent) deems necessary for the DPIA. As a data controller, your organization is entirely responsible for determining your organization’s purposes for using Viva Insights. As a data processor, Microsoft informs you how the product functions and processes data pursuant to your configuration of the services.

### Use aggregated or de-identified data whenever possible

To minimize privacy risk, use the minimum data necessary to conduct your research. While adopting a strict policy of never using personal data and minimizing use of pseudonymized data in combination with identifying attributes can help address many of the risks inherent in using such data, such a policy can restrict the types of analyses that Viva Insights can perform. It is up to your organization to decide the best approach and policy for your organization.

For example, many companies see the benefit of understanding aggregate collaboration patterns between different teams or departments within their organization. Fewer companies may be comfortable analyzing highly sensitive information like health data, real-time location, document content, and certain types of diversity demographics.

### Work closely with subject matter experts

Consult with your organization’s human-resources, privacy, and legal subject matter experts in the countries where you would like to use Viva Insights. Analyses that might be acceptable in one country might be subject to more requirements (for example, notice and consent obligations) or even illegal in other countries. Due diligence is particularly important in highly regulated jurisdictions like the European Union.

## Decide what data is used and who gets to see it

You have full control over what data to include in analysis using Viva Insights. The primary data source is collaboration data from Microsoft 365. This data is supplemented by human resources or other organizational data that you want to include so that you can group information by job title, location, or other attributes.

### Data provided by Microsoft 365

Viva Insights uses header information from Microsoft 365 email and calendar items. This header information includes sender and recipient, date, and subject lines for email, and organizer, attendee, and duration of meetings. Viva Insights never includes attachments and content in email and calendar items. For a full description of what is included and excluded, see [Privacy and data access](/viva/insights/privacy/privacy-and-data-access?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

It’s important to note that while Viva Insights uses this Microsoft 365 data, most of the header information is never directly available to users within the service. Rather, Viva Insights provides computations and metrics based on this information. Furthermore, using the settings within the service, you get to decide and configure what data to use and who can see it. Review the product privacy features documentation for full details.

### Privacy capabilities in your control

First, you get to decide which users’ mailboxes to include in your Viva Insights study. Then, you can use multiple controls to further limit the data.

* You can control whether analysts have access to email and calendar subject lines.
* You can rule out all meetings and email by keywords (in subject lines) that you deem sensitive.
* You can remove all references to any individual from the initial set of user mailboxes that you have included for analysis.
* You can rule out confidential or private email, or those that are rights protected by using Microsoft's digital rights management technology.

To learn more about privacy, see [Privacy and data access](/viva/insights/privacy/privacy-and-data-access?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) and [Assign roles to admins and analysts](../Setup/Set-up-Workplace-Analytics.md#setup-steps).

### Data provided by your organization

You control what other information you want to be included in Viva Insights analyses.

To enable analysis along organizational lines, you can provide HR data such as disciplines, titles, locations, and managers. Viva Insights ensures that individual identities are never used in analyzing this information. However, it is important to take care to prevent incidental identification of users based on personal data, such as names, employee identification numbers, or specific office locations. Additionally, consider risks of including attributes whose specific values may identify some individuals directly (such as the title field containing CEO), or may reduce the set of individuals below the aggregation thresholds that make individuals easily identifiable (for example, there might only be only a few Directors).

### Who can see the data

You control who gets to see the data and the results of the analysis. Like other products that work with sensitive data, such as HR systems, Viva Insights is not meant for the general workforce. Rather, its users are expected to have training regarding how to handle sensitive information. Training should be specific to your organization. Suggested topics may include your organization’s HR policies, employee privacy policy, how to handle and store sensitive data, and insider trading.

Two types of analysts can access information within Viva Insights. The first type is Analyst (Limited Access) that provides an exploratory view into the data and is populated with preset views that only offer aggregated information and share no personal data. This view is recommended for analysts who do not need the full power of Viva Insights to understand the data. The analysis presented in this view suppresses any chance of exposing user-specific information.

The second type of access in Viva Insights provides is an Analyst with full access. This type of analyst can run query data with meeting and email information for analysis, all of which fall under the category of de-identified data. However, if you choose to provide personal data, then the analyst can discern whose metrics are being computed. Thus, it is important that these analysts are provided the requisite training before they are given access to Viva Insights. Additionally, Viva Insights logs all queries that such analysts author, therefore allowing you to audit them for consistency with your organizational policies and any DPIA that you completed.

Both of these roles are provisioned by the tenant administrator.

### Support for handling data subject requests

Under the GDPR, data subjects may have rights to request exclusion from processing, access, correction, or deletion of their personal data. It is your organization’s role as data controller to evaluate whether a particular data subject request is valid and, if appropriate, to take action to fulfill the request. As a data processor, Microsoft provides mechanisms for your organization as the data controller to honor data subject rights through controls that are built into Viva Insights.

* **Exclusion from processing** - Data subjects have the right to have their personal information excluded from processing. In Viva Insights, you can exclude an employee’s personal information from being processed simply by not assigning a Viva Insights license to that employee.

* **Access** - Data subjects have the right to demand what personal information is being processed, and Viva Insights gives you the ability to export the raw data, which may contain personal data. The scope of such information is restricted to what is personally associable and does not contain aggregate metrics from which no personal information can be gleaned.

* **Correction** - Data subjects have the right to rectify their personal data. Viva Insights only performs operations (mostly arithmetic) on data provided to it from other sources, such as email and meeting data from Microsoft 365 or the organizational data that you upload. This data is not corrected through Viva Insights.

* **Deletion** - Microsoft supports the GDPR [Right to erasure](/compliance/regulatory/gdpr-dsr-Office365#deleting-personal-data). Additionally, if necessary, customers themselves can also delete reports that identify the data subject. Customers can also delete the data subject from any other data (such as organizational data or CRM data) that they may have provided to Viva Insights.

* **Transparency regarding processing** - See [Metric descriptions](../Use/Metric-definitions.md) for detailed information about the metrics calculated by Viva Insights, and what they mean.  

>[!Note]
>Microsoft 365 users can determine whether they have a Viva Insights license and, consequently, whether their data is being processed. For more information, see [Subscription status](/viva/insights/setup/assign-licenses-to-population?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#subscription-status).

## Additional resources

* [Privacy and data access](/viva/insights/privacy/privacy-and-data-access?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)
* Article 29 Data Protection Working Party [Opinion 2/2017 on data processing at work](http://ec.europa.eu/newsroom/document.cfm?doc_id=45631)
* EU [General Data Protection Regulation](http://eur-lex.europa.eu/legal-content/EN/TXT/?uri=uriserv:OJ.L_.2016.119.01.0001.01.ENG&toc=OJ:L:2016:119:TOC)
