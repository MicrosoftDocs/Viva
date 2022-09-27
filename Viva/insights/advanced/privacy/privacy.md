---
ROBOTS: NOINDEX,FOLLOW
title: Advanced insights privacy
description: Learn more about privacy in advanced insights
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

# Data protection with Viva Insights

Microsoft Viva Insights produces useful insights about how your organization and employees function. It does this by analyzing Microsoft 365 collaboration data and organizational (HR) data that you provide. Because of the potential sensitivity about how data could be used, successful implementation and use of Viva Insights require careful thought and planning with regard to data protection.

The following resources help answer key questions about how Microsoft protects employee privacy and supports compliance with local regulations, such as the General Data Protection Regulation (GDPR) when data is processed for Viva Insights.

## Personal insights

Depending on your role, the following guides describe how the data processed in Viva Insights keeps your personal data private and protected.

* For users: [Privacy guide for personal insights](/viva/insights/personal/overview/privacy-guide-users) 
* [For admins: Privacy guide for admins](/viva/insights/personal/overview/privacy-guide-admins)

## Manager, leader, and advanced insights

Based on your role, the following information explains how Microsoft protects employees' privacy when processing the data that the Viva Insights features use for manager, leader, and advanced insights.

* For leaders, admins, program managers, group or people managers, and analysts: [Data-protection considerations](#data-protection-considerations)
* For leaders, admins, and analysts: [Data access after license expiration](#data-retention-and-access-after-all-subscriptions-expire)
* For admins and analysts: [Privacy and data access](#privacy-and-data-access)

## More about advanced insights

If your organization uses advanced insights and analysis in the Viva Insights service, the following information provides more details about different aspects of data protection, privacy, and access.

* [Roles and responsibilities](#roles-and-responsibilities) - Read about the concepts of [data controller](#data-controller), [data processor](#data-processor), and [data subject](#data-subject), and their origins in European privacy law.
* [Types of data used in analysis](#types-of-data-used-in-analysis) - Provides an overview of the different types of data that can be included and used in calculations.
* [De-identification of personal data](#de-identification-of-personal-data) - Describes how Viva Insights de-identify personal data by using pseudonymization and other techniques, such as aggregation.
* [Differential privacy](#differential-privacy) - Describes what differential privacy is and how is it used in Viva Insights to keep individual data private.
* [Data-privacy recommendations](#data-privacy-recommendations) - Guidelines that are based on Microsoft's experience working with customers, worker councils, and legal and privacy teams.
* [Decide who gets to see what data](#decide-who-gets-to-see-what-data) - Describes what adjustments you can make, such as how to change the data your organization provides or how to keep sensitive data (like confidential email or meetings with specific subject lines) from becoming available for analysis.

## Data-protection considerations

Advanced insights in Microsoft Viva Insights produces powerful insights about how your organization functions. It analyzes Microsoft 365 collaboration data and organizational (HR) data that you provide. Given the novelty of Advanced insights in the Viva Insights service and the potential sensitivity about how data could be used, successful implementation and use of Advanced insights require careful data protection planning.

This section provides a basic overview of roles, responsibilities, types of data, and data-privacy recommendations. The general suggestions offered here are a starting point for planning your data-protection strategy and deployment. These are not intended as a substitute for addressing your organization’s unique needs by engaging with legal, privacy, human-resources, and other subject matter experts within your organization.

### Roles and responsibilities

The concepts of [data controller](#data-controller), [data processor](#data-processor), and [data subject](#data-subject) originate in European privacy law. Regardless of where your organization is located or whether any personal data of European Union citizens is involved, these concepts provide a useful framework for thinking about data protection when using Viva Insights.

The following illustration shows the central position of the data controller (your organization) between the data subject (left) and the data processor, Microsoft (on the right):

<!--insert screenshot-->
 
Before setting up Viva Insights, first consider the respective roles and responsibilities of your organization and of Microsoft to protect personal data and honor the rights of data subjects.

#### Data controller

The data controller is a party that determines the purposes and means of processing a data subject’s personal data.

When using Viva Insights, your organization is the data controller because your organization determines if, how, and why Viva Insights processes any personal data.

As a data controller, your organization should:

* Determine the scope of data to analyze and the purpose and objectives of the analysis.
* Work with your organization’s legal, privacy, and human resources teams for the following tasks:
    * Determining whether you should obtain consent from employees in your company.
    * Determining what information you provide to employees about how your organization will process their personal data in Viva Insights.
    * Accounting for local considerations (for example, obtain approval from local works councils, if applicable).
* Use Viva Insights privacy controls to direct what data will be analyzed, how data will appear in results, and who will have access to both raw data and the results of analysis.
* Review and be familiar with this document and other Viva Insights privacy documentation provided by Microsoft.

### Data processor

The data processor is a party that processes personal data on behalf of the data controller. When your organization uses Viva Insights, Microsoft is the data processor.

As a data processor, Microsoft will:

* Process personal data in accordance with your organization’s instructions as directed through your settings configuration within Viva Insights.
* Through your use of Viva Insights, process all data provided to Microsoft (including personal data) according to the same general privacy and security terms in the [Online Services Terms (OST)](http://microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46) as Microsoft 365.
* As part of Microsoft’s commitments under the OST, remain certified under the EU-U.S. and Swiss-U.S. Privacy Shield Frameworks and the commitments that these frameworks entail to legitimize transfers of personal data from the EU and Switzerland to the U.S.
* Contractually commit to abide by applicable provisions of the European Union General Data Protection Regulation (GDPR), effective starting May 25, 2018.
* Provide Viva Insights features that help organizations meet their data-controller obligations and honor data-subject rights under the GDPR, including the right of exclusion from processing, access, and erasure, and including the right of transparency regarding methods of processing.
* Implement technical and organizational security measures to protect the confidentiality of your organization’s (and employees’) data in Viva Insights.

In addition, Microsoft does not use data for advertising nor does it volunteer to provide data to law enforcement.

### Data subject

A data subject is a person who can be identified through personal data. In the context of Viva Insights, the data subject is an employee or other user in your organization whose personal information is being processed. Personal data is any information that directly or indirectly identifies a person (the data subject).

Note: In most cases in the Viva Insights product and documentation, we refer to a data subject simply as a "user," a "person," an "individual," or an "employee."

## De-identification of data

To keep from disclosing personal data, Viva Insights de-identifies user data by using pseudonymization and other techniques, including aggregation. For more information, see [De-identification of personal data](#de-identification-of-personal-data).

## Types of data used in analysis

Before starting an analysis in Viva Insights, you should think about the types of data that you will include. Specifically, consider whether the inclusion of personal data is necessary to fulfill the purpose of the analysis, or whether other types of data that cannot be used to identify specific individuals could produce results that are as effective and insightful as you would get if you had used personal data.

Your organization might have its own data-classification system, but you might wish to consider the following types of data when you implement Viva Insights:

Types of data used in analysis:

|Privacy risk | Data type | Definition | Examples in Viva Insights|
|------------|-----------|------------|--------------------------|
Highest	| Personal data	| Personal data is information that directly or indirectly identifies a person | By default, Viva Insights de-identifies email addresses and other information from Microsoft 365 that directly identifies an individual in any in-product dashboard or query result. However, it does show information from the organizational dataset that your organization provides for analysis. Thus, if you upload organizational data that includes personal data (for example, employee names and identification numbers), that personal data will appear in in-product dashboards and query results.
|Higher	|Pseudonymized data	|Pseudonymized data is information in which a personal identifier has been replaced with a value that does not directly identify a person (such as a numeric identifier that can no longer be attributed to a specific person without the use of additional information). | Viva Insights automatically replaces email addresses with pseudonyms (cryptographically obscured strings of numbers and letters) in the Microsoft 365 collaboration data that you choose to include for analysis. Using pseudonyms can reduce the likelihood that you will identify a specific person, but the risk of identification remains.|
Lower |	Aggregated data |	Aggregated data is information that is computed from multiple individuals or sources.	| Viva Insights calculates averages across your organization. Since the averages are calculated from data sourced from many people, it becomes nearly impossible to derive information about a specific person’s activity. The likelihood of identifying someone from aggregated data depends on the size of the sample. When you implement Viva Insights for your organization, you must select the sample-size threshold for aggregation. Smaller sample sizes (such as fewer than 10 people) might reveal some insights about individual activity, especially when the individuals are known, and other information (for example, whether the individual was on vacation) can be correlated with changes in the averages over time.|
|Lowest	|De-identified data	|De-identified data is information that does not relate to a specific individual, that does not increase the likelihood that a specific individual can be identified, or that has been rendered in a way so that it cannot be used to identify a specific individual.	|When you use the default settings in Viva Insights, all the computed metrics that are the output of an analysis will be de-identified data.|

## Data-privacy recommendations

Consider implementing the following data-privacy recommendations before you begin using Viva Insights.

### Develop a clear analysis plan

By using Viva Insights, you can process data in many ways, so before you begin, it is important to have a clear purpose about what you want to analyze and why. Determine what specific questions about your organization you want to answer, and then consider how Viva Insights might help you find those answers.

Having a clear question and then determining how a data analysis from Viva Insights will answer the question serves the following goals:

* Keeps your efforts focused on a limited purpose and helps prevent your analysts from simply sifting through the analysis data.
* It helps you scope the data to use and avoid privacy pitfalls such as including more data than is necessary, retaining data for longer than is necessary, and failing to be transparent with employees about how their personal data might be used.
* To the extent your organization is subject to GDPR, planning your analysis is a key step in determining and documenting legitimate interest in processing personal data with Viva Insights.

### Determine whether to complete a data protection impact assessment (DPIA)

The degree of privacy risk to employees and other users in your organization is largely within your control. That risk depends primarily on the organizational dataset that you will import into Viva Insights and how you will use that data.

After you have developed an analysis plan but before you begin processing data in Viva Insights, determine whether you need to complete a DPIA. If your proposed use of Viva Insights involves processing personal data in a manner that could lead to high risks to the rights of employees and other users in your organization, completing a DPIA might be warranted. If you are unsure whether a DPIA is required, consult your organization’s privacy subject matter experts, such as legal or HR personnel.

Higher-risk data includes sensitive demographic data, such as racial or ethnic origin, sex or gender, and trade union membership. Higher-risk uses of Viva Insights include using the service for profiling or to make automated decisions or predictions about employees. (Note that Microsoft designed Viva Insights to help people within organizations *make* data-driven decisions, not to *automate* those decisions.)

If you determine that a DPIA is necessary for your proposed use of Viva Insights, you will need to document several aspects of how you will use the service to process personal data, including how the data will be collected; how it will be processed; the necessity of the processing in relation to the purpose; what risks the processing presents to employees; the data flows within and outside Viva Insights; feedback that you received from employees regarding the proposed data processing; and any other information that your organization’s data-protection officer (or equivalent) deems necessary for the DPIA. As a data controller, your organization is entirely responsible for determining your organization’s purposes for using Viva Insights. As a data processor, Microsoft informs you how the product functions and processes data pursuant to your configuration of the services.

### Use aggregated or de-identified data whenever possible

To minimize privacy risk, use the minimum data necessary to conduct your research. While adopting a strict policy of never using personal data and minimizing use of pseudonymized data in combination with identifying attributes can help address many of the risks inherent in using such data, such a policy can restrict the types of analyses that Viva Insights can perform. It is up to your organization to decide the best approach and policy for your organization.

For example, many companies see the benefit of understanding aggregate collaboration patterns between different teams or departments within their organization. Fewer companies may be comfortable analyzing highly sensitive information like health data, real-time location, document content, and certain types of diversity demographics.

### Work closely with subject matter experts

Consult with your organization’s human-resources, privacy, and legal subject matter experts in the countries where you would like to use Viva Insights. Analyses that might be acceptable in one country might be subject to more requirements (for example, notice and consent obligations) or even illegal in other countries. Due diligence is particularly important in highly regulated jurisdictions like the European Union.

## Decide who gets to see what data

You have full control over what data to include in analysis using Viva Insights. The primary data source is collaboration data from Microsoft 365. This data is supplemented by human resources or other organizational data that you want to include so that you can group information by job title, location, or other attributes.

### Data provided by Microsoft 365

Viva Insights uses header information from Microsoft 365 email and calendar items. This header information includes sender and recipient, date, and subject lines for email, and organizer, attendee, and duration of meetings. Viva Insights never includes attachments and content in email and calendar items. For a full description of what is included and excluded, see [Privacy and data access](#privacy-and-data-access).

It’s important to note that while Viva Insights uses this Microsoft 365 data, most of the header information is never directly available to users within the service. Rather, Viva Insights provides computations and metrics based on this information. Furthermore, using the settings within the service, you get to decide and configure what data to use and who can see it. Review the product privacy features documentation for full details.

### Privacy capabilities in your control

First, you get to decide which users’ mailboxes to include in your Viva Insights study. Then, you can use multiple controls to further limit the data.

To learn more about privacy, see [Privacy and data access](#privacy-and-data-access) and [Assign roles](../setup-maint/assign-user-roles.md).

### Data provided by your organization

You control what other information you want to be included in Viva Insights analyses.

To enable analysis along organizational lines, you can provide HR data such as disciplines, titles, locations, and managers. Viva Insights ensures that individual identities are never used in analyzing this information. However, it is important to take care to prevent incidental identification of users based on personal data, such as names, employee identification numbers, or specific office locations. Additionally, consider risks of including attributes whose specific values may identify some individuals directly (such as the title field containing CEO), or may reduce the set of individuals below the aggregation thresholds that make individuals easily identifiable (for example, there might only be only a few Directors).

### Who can see the data

You control who gets to see the data and the results of the analysis. Like other products that work with sensitive data, such as HR systems, Viva Insights is not meant for the general workforce. Rather, its users are expected to have training regarding how to handle sensitive information. Training should be specific to your organization. Suggested topics may include your organization’s HR policies, employee privacy policy, how to handle and store sensitive data, and insider trading.

An Insights Analyst can access information within Viva Insights. This role can run query data with meeting and email information for analysis, all of which fall under the category of de-identified data. However, if you choose to provide personal data, then the analyst can discern whose metrics are being computed. Thus, it is important that these analysts are provided the requisite training before they are given access to Viva Insights. Additionally, Viva Insights logs all queries that such analysts author, therefore allowing you to audit them for consistency with your organizational policies and any DPIA that you completed.

This role is provisioned by the tenant administrator.

### Support for handling data subject requests

Under the GDPR, data subjects may have rights to request exclusion from processing, access, correction, or deletion of their personal data. It is your organization’s role as data controller to evaluate whether a particular data subject request is valid and, if appropriate, to take action to fulfill the request. As a data processor, Microsoft provides mechanisms for your organization as the data controller to honor data subject rights through controls that are built into Viva Insights.

* **Exclusion from processing** – Data subjects have the right to have their personal information excluded from processing. In Viva Insights, you can exclude an employee’s personal information from being processed simply by not assigning a Viva Insights license to that employee.
* **Access** – Data subjects have the right to demand what personal information is being processed, and Viva Insights gives you the ability to export the raw data, which may contain personal data. The scope of such information is restricted to what is personally associable and does not contain aggregate metrics from which no personal information can be gleaned.
* **Correction** – Data subjects have the right to rectify their personal data. Viva Insights only performs operations (mostly arithmetic) on data provided to it from other sources, such as email and meeting data from Microsoft 365 or the organizational data that you upload. This data is not corrected through Viva Insights.
* **Deletion** – Microsoft supports the GDPR [Right to erasure](/compliance/regulatory/gdpr-dsr-Office365#deleting-personal-data).  Additionally, if necessary, customers themselves can also delete reports that identify the data subject. Customers can also delete the data subject from any other data (such as organizational data or CRM data) that they may have provided to Viva Insights.
* **Transparency regarding processing** – See [Metric definitions](../reference/metrics.md) for detailed information about the metrics calculated by Viva Insights, and what they mean.

>[!Note]
> Microsoft 365 users can determine whether they have a Viva Insights license and, consequently, whether their data is being processed. For more information, see Subscription status.

### Additional resources

* [Privacy and data access](#privacy-and-data-access) 
* Article 29 Data Protection Working Party [Opinion 2/2017 on data processing at work](http://ec.europa.eu/newsroom/document.cfm?doc_id=45631)
* EU [General Data Protection Regulation](http://ec.europa.eu/newsroom/document.cfm?doc_id=45631)

## De-identification of personal data

To keep from disclosing personal data, Microsoft Viva Insights de-identifies an individual's data through the use of pseudonymization and other techniques, such as aggregation.

The following [illustrative example](#illustrative-example) describes how Viva Insights secures information in query results. For more examples of how various types of data are de-identified, see Examples in Types of data for analysis.

See the [Glossary](../reference/glossary.md) for definitions of the terms related to privacy, such as: aggregation, anonymization, de-identification, hashing, and personal data.

>[!Note]
>To balance the requirements of protecting individual privacy and providing useful information, Viva Insights is gradually incorporating a nuanced approach known as [differential privacy](#differential-privacy).

### Illustrative example

With Viva Insights, all metrics that are computed from Microsoft 365 collaboration data and from the organizational data that you choose to include are de-identified and aggregated data. The following example shows one line from a “people” report that Viva Insights created:

|Person Identifier	|After Hours	|Email Hours	|Function	|Title	Org	|Region|
|------|-------|------|--------|---------|-------|
|T5Y07H4VfKWcCC3	|7	|6	|HR	|Director	|HR – Corp	|Central|

In this example, Viva Insights computes After Hours and Email Hours for some individual, and reports on this information, associating it with the person’s attributes that you choose to include. The computed information is de-identified; that is, you cannot identify the individual from these fields. The Person Identifier is pseudonymized with a cryptographically generated identifier derived from the person’s Microsoft 365 email address. The other attributes (such as function, title, organization, and region) are effectively personal data. While it might not be possible to identify the user with any single attribute, together these attributes might enable you to identify the user whose metrics have been computed. Therefore, this group of attributes is considered personal data.

## Differential privacy

Microsoft Viva Insights is serious about protecting individual privacy. Privacy can always be guaranteed if no information is revealed, which is not very useful. Similarly, making all information available can lead to high-fidelity metrics that compromise individual privacy.

Differential privacy offers a balance between providing useful information and protecting individual privacy. Viva Insights uses methods from world-class researchers to apply differential privacy. By introducing slight variations to the data, it protects privacy while simultaneously maintaining accuracy. The methods are more sophisticated than this simple description, with numerous options toward balancing fidelity and privacy. For more details, see [Differential Privacy for Everyone](https://download.microsoft.com/download/D/1/F/D1F0DFF5-8BA9-4BDF-8924-7816932F6825/Differential_Privacy_for_Everyone.pdf).

The first application of differential privacy in Viva Insights is within [Manager insights](/viva/insights/org-team-insights/org-trends?toc=%2Fviva%2Finsights%2Fadvanced%2Ftoc.json&bc=%2Fviva%2Finsights%2Fbreadcrumb%2Ftoc.json). These insights enable managers to understand how the people in their team are doing and to learn how to drive change by using aggregated collaboration data.

No matter how the metrics are presented or used in Viva Insights, no individual activity or metric can ever be discerned. The individual activity can never be established with certainty, and no manager or team-leader can conclude with confidence anything specific about any individual.

See [Differential privacy](https://www.microsoft.com/ai/ai-lab-differential-privacy) to learn more about how Microsoft AI is helping to define and use it.

## Privacy and data access

Being aware of employees' rights is a key component to ensuring a successful program using Microsoft Viva Insights. It is important to consider ever-changing laws and regulations regarding employer-employee relationships, privacy, and personal data, as well as company policies, before using Viva Insights.

Viva Insights does not encode any specific policy, instead it provides controls that administrators can use to configure the product to be consistent with applicable laws, regulations, and company policies. Your organization chooses what data to use in Viva Insights.

>[!Important]
>Consult with your legal and human resources teams before enabling Microsoft Viva Insights for your organization.

### You decide who gets to see what data

Organizations decide who has access to what Viva Insights data. You should ensure that primary users receive suitable training in privacy, and in your company’s policies and other applicable subject areas, before being granted access to the data.

The following levels of permission provide access to the Viva Insights data:

* Analyst has full access to all product features except the administrator features.
* Administrator role has access to administrator features only (such as **Organizational data** and **Privacy settings** in Viva Insights).

### You control the data that Viva Insights uses

You retain full control over what data is used and how it is used within Viva Insights. Viva Insights uses Microsoft 365 email and calendar metadata and external data defined by your organization (usually exported from an HR system) to compute how much time groups within your organization spend in meetings, emails, calls, and chats, and with whom.

Viva Insights processes data sourced with organizational data from your own HR system and collaboration data from Microsoft 365 to provide analysts with a unified pool of data on which to perform analyses.

#### Organizational data

Organizational data is contextual information about your employees (for example: job title, level, location) and can come from human resources, information systems, or other line-of-business data stores. Viva Insights combines Microsoft 365 email, calendar, call, and instant message metadata with the organizational data that you choose to use to provide rich, actionable insights into your company’s communication and collaboration trends to help you make more effective business decisions.

The organizational data set is combined with the Microsoft 365 metadata to produce the complete dataset that is analyzed for insights. The data sets are combined using the email addresses of the users, but the email addresses are never shown in Viva Insights through dashboards or query results.

Note that other information provided in the organizational data set is exposed in Viva Insights and in Viva Insights. Take care to ensure that the data set does not include personal data (such as the employee ID). For more details, see [Prepare organizational data](../admin/prepare-org-data.md).

#### Collaboration data from Microsoft 365

Microsoft 365 email, calendar, call, and instant message metadata provides the foundation for all analysis in Viva Insights, so the first step is to determine which users you want to include. When you choose a user to be included, Viva Insights uses the following information about items in that user's mailbox and calendar:

|item| originator |	recipient |subject |chronology |status |venue|
|--------|----------|------|-----------|-----------|---------|-----|
**email** |sender |	recipients | subject line |sent time
**meeting**	|organizer | invitees | subject line |scheduled time |attendee status |scheduled location
**call** |organizer	|invitees | | scheduled time, call joined time, call duration |	call/join status |
**chat** |sender of initial IM|	recipients| |	 IM sent time| |

>[!Important]
>Attachments and text in the body of email and meetings are never used by Viva Insights. 

## Data retention policy

How long does Microsoft Viva Insights and in Teams retain the data that's collected? The answer depends on the state of the Viva Insights user licenses:

* [Data retention for active tenants](#data-retention-for-active-tenants)
* [Data retention after a license is removed](#data-retention-after-a-license-is-removed)
* [Data retention and access after all subscriptions expire](#data-retention-and-access-after-all-subscriptions-expire)

### Data retention for active tenants

An active tenant is tenant that has one or more valid Viva Insights user licenses.

By default, Viva Insights initially collects, processes, and retains 13 months' worth of data. Then, through weekly refreshes, Viva Insights increases this history until 27 months' worth of data is collected. After this point, older collaboration data is deleted as newer collaboration data is collected.

This means that Viva Insights will not have any collaboration data that is older than 27 months.

Customers can file a request to initiate Viva Insights with less than 13 months of data. For this case, the minimum amount that can be collected is one month.

### Data retention after a license is removed

If the Viva Insights license is removed from a user, Viva Insights retains that user's collaboration data that was collected during the period the license was assigned. Admins can continue to query the collaboration activity that this user participated in before they left.  The person's collaboration data will be deleted according to the overall retention policy that is described in Data retention for active tenants.

To permanently remove data from users after licenses are removed, you can contact Microsoft customer support to request a collaboration data reset. 

For information about data deletion requests as handled under the GDPR, see Support for handling data subject requests: 

Under the GDPR, data subjects may have rights to request exclusion from processing, access, correction, or deletion of their personal data. It is your organization’s role as data controller to evaluate whether a particular data subject request is valid and, if appropriate, to take action to fulfill the request. As a data processor, Microsoft provides mechanisms for your organization as the data controller to honor data subject rights through controls that are built into Viva Insights.

* Exclusion from processing - Data subjects have the right to have their personal information excluded from processing. In Viva Insights, you can exclude an employee’s personal information from being processed simply by not assigning a Viva Insights license to that employee.
* Access - Data subjects have the right to demand what personal information is being processed, and Viva Insights gives you the ability to export the raw data, which may contain personal data. The scope of such information is restricted to what is personally associable and does not contain aggregate metrics from which no personal information can be gleaned.
* Correction - Data subjects have the right to rectify their personal data. Viva Insights only performs operations (mostly arithmetic) on data provided to it from other sources, such as email and meeting data from Microsoft 365 or the organizational data that you upload. This data is not corrected through Viva Insights.
* Deletion - Microsoft supports the GDPR Right to erasure. Additionally, if necessary, customers themselves can also delete reports that identify the data subject. Customers can also delete the data subject from any other data (such as organizational data or CRM data) that they may have provided to Viva Insights.
* Transparency regarding processing - See Metric descriptions for detailed information about the metrics calculated by Viva Insights, and what they mean.

>[!Note]
>Microsoft 365 users can determine whether they have a Viva Insights license and, consequently, whether their data is being processed. For more information, see [Subscription status](../setup-maint/assign-licenses.md#subscription-status).

### Data retention and access after all subscriptions expire

If all of your subscriptions expire, you have until the end of your grace period to download data in the form of results. See [To download query results](#to-download-query-results) for details. The duration of the grace period varies between countries and plans. Typically, it is either 90 days for volume-licensing purchases or 30 days for other purchase types. All backend data will be deleted in accordance with the Microsoft 365 Data Handling Standard.

After this period has passed, you will no longer have access to Viva Insights.

#### To download query results

1.	Open the advanced insights app. If prompted, sign in with your work account.
2.	Select **Analyst > Query results**.
3.	In the row for the query results, select **Download** to download the results as a .csv file, which is archived as a .zip file.
