---

title: Data-protection considerations when using Workplace Analytics  
description: Data-protection considerations when using Workplace Analytics.
author: paul9955
ms.author: paul9955
ms.topic: conceptual
localization_priority: normal 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Data-protection considerations when using Workplace Analytics

## Workplace Analytics and data protection in your organization

Microsoft Workplace Analytics produces powerful insights about how your organization functions. It does this by analyzing Office 365 collaboration data and organizational (HR) data that you provide. Given the novelty of the Workplace Analytics service and the potential sensitivity about how data could be used, successful implementation and use of Workplace Analytics require careful thought and planning with regard to data protection.  

This section provides a basic overview of roles, responsibilities, types of data, and data-privacy recommendations. The general suggestions offered here are a starting point for planning your data-protection strategy and deployment. They are not intended as a substitute for addressing your organization’s unique needs by engaging with legal, privacy, human-resources, and other subject matter experts within your organization.

## Roles and responsibilities

### Data controller, data processor, and data subjects

The concepts of _data controller_, _data processor_, and _data subject_ originate in European privacy law. Regardless of where your organization is located or whether any personal data of European Union citizens is involved, these concepts provide a useful framework for thinking about data protection when using Workplace Analytics.

The following illustration shows the central position of the data controller (your organization) between the data subject (left) and the data processor, Microsoft (on the right):  

<img src="../Images/data-subject-controller-processor.PNG" alt="Roles in data protection">

To protect personal data and honor the rights of data subjects and before setting up Workplace Analytics, first consider the respective roles and responsibilities of your organization and of Microsoft.

### Your organization’s role: Data controller

The data controller is a party that determines the purposes and means of processing a data subject’s personal data.

When using Workplace Analytics, your organization is the data controller because your organization determines if, how, and why Workplace Analytics will process any personal data.

As a data controller, your organization should:

* Determine the scope of data to analyze and the purpose and objectives of the analysis.
* Work with your organization’s legal, privacy, and human resources teams to do the following:

  * Determine whether you should obtain consent from employees in your company;
  * Determine what information you provide to employees about how your organization will process their personal data in Workplace Analytics; and
  * Take local considerations into account (for example, obtain approval from local works councils, if applicable).

* Use Workplace Analytics privacy controls to direct what data will be analyzed, how data will appear in results, and who will have access to both raw data and the results of analysis.
* Review and be familiar with this document and other Workplace Analytics [privacy documentation](../Privacy/Privacy-And-Data-Access.md) provided by Microsoft.

### Microsoft’s role: Data processor

The data processor is a party that processes personal data on behalf of the data controller. When your organization uses Workplace Analytics, Microsoft is the data processor.

As a data processor, Microsoft will:

* Process personal data in accordance with your organization’s instructions as directed via your settings configuration within Workplace Analytics.
* Through your use of Workplace Analytics, process all data provided to Microsoft (including personal data) according to the same [general privacy and security terms in the Online Services Terms (OST)](http://microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46) as Office 365.
* As part of Microsoft’s commitments under the OST, remain certified under the EU-U.S. and Swiss-U.S. Privacy Shield Frameworks and the commitments that these frameworks entail to legitimize transfers of personal data from the EU and Switzerland to the U.S.
* Contractually commit to abide by applicable provisions of the European Union General Data Protection Regulation (GDPR), effective starting May 25, 2018.
* Provide Workplace Analytics features that help organizations meet their data-controller obligations and honor data-subject rights under the GDPR, including the right of exclusion from processing, access, and erasure, and including the right of transparency regarding methods of processing.
* Implement technical and organizational security measures to protect the confidentiality of your organization’s (and employees’) data in Workplace Analytics.

In addition, Microsoft does not use data for advertising nor does it volunteer to provide data to law enforcement.

### Data subject and personal data

A data subject is a person who can be identified through personal data. In the context of Workplace Analytics, the data subject is an employee or other user in your organization whose personal information is being processed. Personal data is any information that directly or indirectly identifies a person (the data subject).

> [!Note]
> In most cases in the Workplace Analytics product and documentation, we refer to a _data subject_ simply as a "user," a "person," an "individual," or an "employee."

## De-identification of personal data

To keep from disclosing personal data, Workplace Analytics de-identifies user data through the use of pseudonymization and other techniques, including aggregation. For examples of how it does this for various types of data, see the Examples column in the table in the [following section](#types-of-data-for-analysis-in-workplace-analytics). This [illustrative example](#illustrative-example) describes how Workplace Analytics secures information in query results. Finally, see the [Glossary](../use/glossary.md) for definitions of the terms related to privacy: aggregation, anonymization, de-identification, hashing, and personal data.

> [!Note] 
> To balance the requirements of protecting individual privacy and providing useful information, Workplace Analytics is gradually incorporating a nuanced approach known as [differential privacy](differential-privacy.md).  

## Types of data for analysis in Workplace Analytics

Before starting an analysis in Workplace Analytics, you should think about the types of data that you will include. Specifically, consider whether the inclusion of personal data is necessary to fulfill the purpose of your analysis, or whether other types of data that cannot be used to identify specific individuals could produce results that are just as effective and insightful as you would get if you had used personal data.

Your organization might have its own data-classification system, but you might wish to consider the following types of data when you implement Workplace Analytics:

| Privacy risk | Data type | Definition | Examples in Workplace Analytics |
| ------------ | --------- | ---------- | ----- |
| Highest | Personal data | Personal data is information that directly or indirectly identifies a person | By default, Workplace Analytics de-identifies email addresses and other information from Office 365 that directly identifies an individual in any in-product dashboard or query result. However, it does show information from the organizational dataset that your organization provides for analysis. Thus, if you upload organizational data that includes personal data (for example, employee names and identification numbers), that personal data will appear in in-product dashboards and query results. |
| Higher | Pseudonymized data | Pseudonymized data is information in which a personal identifier has been replaced with a value that does not directly identify a person (such as a numeric identifier that can no longer be attributed to a specific person without the use of additional information). | Workplace Analytics automatically replaces email addresses with pseudonyms (cryptographically obscured strings of numbers and letters) in the Office 365 collaboration data that you choose to include for analysis. Using pseudonyms can reduce the likelihood that you will identify a specific person, but the risk of identification remains. |
| Lower | Aggregated data | Aggregated data is information that is computed from multiple individuals or sources. | Workplace Analytics calculates averages across your organization. Since the averages are calculated from data sourced from many people, it becomes nearly impossible to derive information about a specific person’s activity. The likelihood of identifying someone from aggregated data depends on the size of the sample. When you implement Workplace Analytics for your organization, you must select the sample-size threshold for aggregation. Smaller sample sizes (such as fewer than ten people) might reveal some insights about individual activity, especially when the individuals are known, and other information (for example, whether the individual was on vacation) can be correlated with changes in the averages over time. |
| Lowest | Anonymized data | Anonymized data is information that does not relate to a specific individual, that does not increase the likelihood that a specific individual can be identified, or that has been rendered in a way so that it cannot be used to identify a specific individual. | When you use the default settings in Workplace Analytics, all the computed metrics that are the output of an analysis will be anonymized data. |

### Illustrative Example

With Workplace Analytics, all metrics that are computed from Office 365 collaboration data and from the organizational data that you choose to include are anonymized and aggregated data. The following example shows one line from a “people” report that Workplace Analytics created:

| Person Identifier | After Hours | Email Hours | Function | Title | Org | Region |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| T5Y07H4VfKWcCC3 | 7 | 6 | HR | Director | HR – Corp | Central |

In this example, Workplace Analytics computes After Hours and Email Hours for some individual, and reports on this information, associating it with the person’s attributes that you choose to include. The computed information is anonymized; that is, you cannot identify the individual from these fields. The Person Identifier is pseudonymized with a cryptographically generated identifier derived from the person’s Office 365 email address. The other attributes (Function, Title, Org, and Region) are effectively personal data. While it might not be possible to identify the user with any single attribute, together these attributes might enable you to identify the user whose metrics have been computed. Therefore, you should treat these attributes as personal data.

## Data-privacy recommendations

Consider implementing the following data-privacy recommendations before you begin using Workplace Analytics.

### Develop a clear analysis plan

By using Workplace Analytics, you can process data in many ways, so before you begin, it is important to have a clear purpose about what you want to analyze and why. You should determine what specific questions about your organization you want to answer, and then consider how Workplace Analytics might help you find those answers.

Having a clear question and then determining how a data analysis from Workplace Analytics will answer the question serves three objectives: First, it focuses your efforts on that limited purpose and helps prevent your Workplace Analytics analysis from becoming a “fishing expedition” with analysts simply sifting through data. Second, it helps you scope the data to use and avoid privacy pitfalls such as including more data than is necessary, retaining data for longer than is necessary, and failing to be transparent with employees about how their personal data might be used. Finally, to the extent your organization is subject to GDPR, planning your analysis can be a key step in determining and documenting your legitimate interest in processing personal data with Workplace Analytics.  

### Determine whether to complete a data protection impact assessment (DPIA)

The degree of privacy risk to employees and other users in your organization is largely within your control. That risk depends primarily on the organizational dataset that you will import into Workplace Analytics and how you will use that data.

After you have developed an analysis plan but before you begin processing data in Workplace Analytics, determine whether you need to complete a DPIA. If your proposed use of Workplace Analytics involves processing personal data in a manner that could lead to high risks to the rights of employees and other users in your organization, completing a DPIA might be warranted. If you are unsure whether a DPIA is required, consult your organization’s privacy subject matter experts, such as legal or HR personnel.

Higher-risk data includes sensitive demographic data, such as racial or ethnic origin, sex or gender, and trade union membership. Higher-risk uses of Workplace Analytics include using the service for profiling or to make automated decisions or predictions about employees. (Note that Microsoft designed Workplace Analytics to help people within organizations _make_ data-driven decisions, not to _automate_ those decisions.)

If you determine that a DPIA is necessary for your proposed use of Workplace Analytics, you will need to document several aspects of how you will use the service to process personal data, including how the data will be collected; how it will be processed; the necessity of the processing in relation to the purpose; what risks the processing presents to employees; the data flows within and outside Workplace Analytics; feedback that you received from employees regarding the proposed data processing; and any other information that your organization’s data-protection officer (or equivalent) deems necessary for the DPIA. As a data controller, your organization is entirely responsible for determining your organization’s purposes for using Workplace Analytics. As a data processor, Microsoft informs you how the product functions and processes data pursuant to your configuration of the services.

### Use aggregated or anonymized data whenever possible

To minimize privacy risk, use the minimum data necessary to conduct your research. While adopting a strict policy of never using personal data and minimizing use of pseudonymized data in combination with identifying attributes can help address many of the risks inherent in using such data, such a policy can restrict the types of analyses that Workplace Analytics can perform. It is up to your organization to decide the best approach and policy for your organization.

For example, many companies see the benefit of understanding aggregate collaboration patterns between different teams or departments within their organization. Fewer companies may be comfortable analyzing highly-sensitive information like health data, real-time location, document content, and certain types of diversity demographics.

### Work closely with subject matter experts

Consult with your organization’s human-resources, privacy, and legal subject matter experts in the countries where you would like to use Workplace Analytics. Analyses that might be acceptable in one country might be subject to additional requirements (for example, notice and consent obligations) or even illegal in other countries. Due diligence is particularly important in highly regulated jurisdictions like the European Union.

## Decide what data is used by Workplace Analytics and who gets to see it

You have full control over what data to include in analysis using Workplace Analytics. The primary data source is collaboration data from Office 365. This is supplemented by human resources or other organizational data that you want to include so that you can group information by job title, location, or other attributes.

### Data provided by Microsoft Office 365

Workplace Analytics uses header information from Office 365 email and calendar items. This header information includes sender and recipient, date and subject lines for email; and organizer, attendee, and duration of meetings. Workplace Analytics never includes attachments and content in email and calendar items. For a full description of what is included and excluded please review [Workplace Analytics privacy and data access](../Privacy/Privacy-And-Data-Access.md).

It’s important to note that while Workplace Analytics uses this Office 365 data, most of the header information is never directly available to users within the service. Rather, Workplace Analytics provides computations and metrics based on this information. Furthermore, using the settings within the service, you get to decide and configure what data to use and who can see it. Please review the product privacy features documentation for full details.

### Privacy capabilities in your control

First, you get to decide which users’ mailboxes to include in your Workplace Analytics study. Then, you can use multiple controls to further limit the data.

* You can control whether analysts have access to email and calendar subject lines.
* You can rule out all meetings and email by keywords (in subject lines) that you deem sensitive.
* You can remove all references to any individual from the initial set of user mailboxes that you have included for analysis.
* You can rule out confidential or private email, or those that are rights protected by using Microsoft's digital rights management technology.

To learn more about privacy, see [Workplace Analytics privacy and data access](../Privacy/Privacy-And-Data-Access.md) and [Assign roles to Workplace Analytics admins and analysts](../Setup/Set-up-Workplace-Analytics.md#setup-steps).

### Data provided by your organization

You control what other information you want to be included in Workplace Analytics analyses.

To enable analysis along organizational lines, you can provide HR data such as disciplines, titles, locations, and managers. Workplace Analytics ensures that individual identities are never used in analyzing this information. However, it is important to take care to prevent incidental identification of users based on personal data, such as names, employee identification numbers, or specific office locations. Additionally, consider risks of including attributes whose specific values may identify some individuals directly (such as the title field containing CEO), or may reduce the set of individuals below the aggregation thresholds that make individuals easily identifiable (for example, there may only be only a small number of Directors).

### Who can see the data

You control who gets to see the data and the results of the analysis. Like other products that work with sensitive data, such as HR systems, Workplace Analytics is not meant for the general workforce. Rather, its users are expected to have training regarding how to handle sensitive information. Training should be specific to your organization. Suggested topics may include your organization’s HR policies, employee privacy policy, how to handle and store sensitive data, and insider trading. 

There are two ways that users provisioned as analysts can access information within Workplace Analytics. One view, Analyst (Limited Access), simply provides an exploratory view into the data and is populated with preset views that only offer aggregated information and share no personal or pseudonymized data. This view is recommended for analysts who do not need the full power of Workplace Analytics to understand the data. The analysis presented in this view suppresses any chance of exposing user-specific information.

The second kind of access Workplace Analytics provides is the full analyst view. Here the analyst can run queries against the meeting and email information to arrive at new metrics, all of which fall under the category of anonymized data. However, if you choose to provide personal data, then the analyst can discern whose metrics are being computed. Thus, it is important that such analysts are provided the requisite training before they are given access to Workplace Analytics. Additionally, Workplace Analytics logs all queries that such analysts author, therefore allowing you to audit them for consistency with your organizational policies and any DPIA that you completed.

Both of these roles are provisioned by the tenant administrator. 

### Workplace Analytics support for handling data subject requests

Under the GDPR, data subjects may have rights to request exclusion from processing, access, correction, or deletion of their personal data. It is your organization’s role as data controller to evaluate whether a particular data subject request is valid and, if appropriate, to take action to fulfill the request. As a data processor, Microsoft provides mechanisms for your organization as the data controller to honor data subject rights through controls that are built into Workplace Analytics.

<!--
ADD THIS BACK IN WHEN WE CAN LINK TO KATE'S DOC:
You can review the details here, but we briefly go over them:
-->

* **Exclusion from processing:** Data subjects have the right to have their personal information excluded from processing. In Workplace Analytics, you can exclude an employee’s personal information from being processed simply by not assigning a Workplace Analytics license to that employee. <!-- DELETED PER PARAMA 16 APRIL 2018: If you have already included an employee in the scope of some analysis, and that employee requests to be excluded from future analysis, then you can configure Workplace Analytics to discontinue the use of data pertaining to that employee. -->
* **Access:** Data subjects have the right to demand what personal information is being processed, and Workplace Analytics gives you the ability to export the raw data, which may contain personal data. The scope of such information is restricted to what is personally associable, and does not contain aggregate metrics from which no personal information can be gleaned.
* **Correction:** Data subjects have the right to rectify their personal data. Workplace Analytics only performs operations (mostly arithmetic) on data provided to it from other sources, such as email and meeting data from Office 365 or the organizational data that you upload. This data is not corrected through Workplace Analytics.  <!-- DELETED PER PARAMA 16 APRIL 2018: If someone requests corrections to Office 365 email and meeting data, then the Office 365 tenant administrator can use the capabilities built into Office 365 to handle these requests. If someone requests corrections to their personal data in the organizational dataset, then as the controller, your organization should provide the means for the data subjects to review and correct such information. -->
* **Deletion:** Data subjects can ask for their personal data to be erased. If a user wishes to have their data removed from a study after the study is completed, then you can expunge that user’s personal data from the raw datasets that were previously processed. You have the option of deciding whether such data needs to be reprocessed without the user’s raw metrics. If you so decide, all reports stored in Workplace Analytics can be deleted and recalculated. 
* **Transparency regarding processing:** See [Metric descriptions](../Use/Metric-definitions.md) for detailed information about the metrics calculated by Workplace Analytics, and what they mean.  

## Additional Resources

* Workplace Analytics [privacy documentation](../Privacy/Privacy-And-Data-Access.md)
* Article 29 Data Protection Working Party [Opinion 2/2017 on data processing at work](http://ec.europa.eu/newsroom/document.cfm?doc_id=45631)
* EU [General Data Protection Regulation](http://eur-lex.europa.eu/legal-content/EN/TXT/?uri=uriserv:OJ.L_.2016.119.01.0001.01.ENG&toc=OJ:L:2016:119:TOC)
