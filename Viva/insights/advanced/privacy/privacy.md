---
ms.date: 03/09/2023
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

# Technical privacy guide for organization insights and advanced insights 

Microsoft Viva Insights produces useful insights about how your organization and employees function. It does this by analyzing Microsoft 365 collaboration data and organizational (HR) data that you provide. Because of the potential sensitivity about how data could be used, successful implementation and use of Viva Insights require careful attention to data and privacy protection.  

This is particularly true for organization insights and advanced insights, which, depending on configuration, could give users insights about others which they wouldn’t already be able to access. Leaders and managers with access to organization insights can find them in the email and Viva Insights Teams app. Analysts with access to advanced insights can use the analysis workbench to create their own insights. 

This resource explains how Microsoft provides the customer administrator with controls to manage sensitive data, and implements protections within Viva Insights to maintain employee privacy. These controls and protections support compliance with local regulations, such as the European Union General Data Protection Regulation (GDPR), for Viva Insights.  

This document is specific to advanced insights and organization insights and provides a technical overview of how data and privacy are protected. For information about how privacy is handled for personal insights, refer to: 

* [Personal insights user privacy guide](/viva/insights/personal/overview/privacy-guide-users)
* [Personal insights technical privacy guide](/viva/insights/personal/overview/privacy-guide-admins) 

## Privacy fundamentals

This section discusses concepts that provide a framework for understanding how Viva Insights approaches data protection.

### Data entity fundamentals 

European privacy law outlines fundamental roles and responsibilities for thinking about data protection. These concepts help illustrate the respective responsibilities of the customer, Microsoft, and employees when it comes to processing and managing sensitive data.

The concepts of [data controller](#data-controller), [data processor](#data-processor), and [data subject](#data-subject) originate in European privacy law. Regardless of where your organization is located or whether any personal data of European Union citizens is involved, these concepts provide a useful framework for thinking about data protection when using Viva Insights.

The following illustration shows the central position of the data controller (your organization) between the data subject (left) and the data processor, Microsoft (on the right):

![Roles in data protection.](../../images/data-subject-controller-processor.png)

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

#### Data processor

The data processor is a party that processes personal data on behalf of the data controller. When your organization uses Viva Insights, Microsoft is the data processor.

As a data processor, Microsoft will:

* Process personal data in accordance with your organization’s instructions as directed through your settings configuration within Viva Insights.
* Through your use of Viva Insights, process all data provided to Microsoft (including personal data) according to the same general privacy and security terms in the [Product Terms](https://www.microsoft.com/licensing/terms/product/PrivacyandSecurityTerms/all) as Microsoft 365.
* As part of Microsoft’s commitments under Product Terms and Microsoft Products and Services [Data Protection Addendum](https://www.microsoft.com/licensing/docs/view/Microsoft-Products-and-Services-Data-Protection-Addendum-DPA), abide by the Standard Contractual Clauses and remain certified under the EU-U.S. and Swiss-U.S. Privacy Shield Frameworks and the commitments that these frameworks entail to legitimize transfers of personal data from the EU and Switzerland to the U.S.
* Contractually commit to abide by applicable provisions of the European Union General Data Protection Regulation (GDPR), effective starting May 25, 2018.
* Provide Viva Insights features that help organizations meet their data-controller obligations and honor data-subject rights under the GDPR, including the right of exclusion from processing, access, and erasure, and including the right of transparency regarding methods of processing.
* Implement technical and organizational security measures to protect the confidentiality of your organization’s (and employees’) data in Viva Insights.

In addition, Microsoft does not use customer data or personal data for advertising nor does it volunteer to provide such data to law enforcement.

#### Data subject

A data subject is a person who can be identified through personal data. In the context of Viva Insights, the data subject is an employee or other user in your organization whose personal information is being processed. Personal data is any information that directly or indirectly identifies a person (the data subject).

>[!Note]
>In most cases in the Viva Insights product and documentation, we refer to a data subject simply as a "user," a "person," an "individual," or an "employee."

## Data classification fundamentals 

Depending on how much detail is available, data can become more or less sensitive. This framework describes different levels of sensitive data formats and where they can appear in Viva Insights. 

|Sensitivity| Classification|Definition|How it's applied in Viva Insights|
|----------|------------|-------------|-----|
Highest | Personal data| Personal data is information that directly or indirectly identifies a person | By default, Viva Insights does not include personal data. When it processes data, it obscures the email addresses from Microsoft 365 that would identify an individual. However, your organization can choose to also provide descriptive employee information for analysis. If that includes personal data (for example, employee names and identification numbers), that personal data can appear to analysts in advanced insights. 
|Higher| De-identified data |De-identified data replaces personal identifiers with a value that does not directly identify a person (such as an encrypted key). These identifiers cannot be mapped back to a specific person without additional information. | Viva Insights automatically replaces email addresses with cryptographically obscured strings of numbers and letters when it processes Microsoft 365 data. These de-identified rows reduce the likelihood that an analyst can identify a specific person. However, the Insights Administrator can upload custom organizational data fields. These custom fields may contain new identifying information, or provide enough descriptive context that an analyst may be able to infer identity. The Insights Administrator should weigh the risk and benefit of custom organizational data fields.  
|Lower | Aggregated data | Aggregated data is represents multiple individuals or sources without attributing to any one individual or source in the group. | Viva Insights often provides averages for groups within your organization. When these groups include many people, it's difficult to derive information about any specific person’s activity from these averages. However, if a user can see results for very small groups or compare averages for overlapping groups, they may still be able to identify a specific person from aggregated data.  <br><br>Aggregated data can be further protected to reduce the possibility of an individual being identified. Organization insights provide leaders and managers with protected results by enforcing three strategies: minimum group sizes, differential privacy, and masked distributions. You can learn more about these techniques in [Protecting sensitive data](#protecting-sensitive-data). 

## Protecting sensitive data 

The [above section](#data-classification-fundamentals) classifies data based on its sensitivity. Viva Insights is designed to provide insights using the least sensitive version of data available. To do this, it includes built-in protections in advanced insights and organizational insights so that users see aggregated, and de-identified information wherever possible. 

### Personal data, de-identified data, and calculated data
 
Some analysts can access row-level employee data in advanced insights. To protect employee identities while preserving the information value of row-level data, Viva Insights applies an algorithm to encrypt employee email addresses. However, depending on the kinds of descriptive employee attributes that the Insights Administrator has chosen to make available to Viva Insights, these attributes might provide enough context or be combined with other information such that an analyst can infer individual identity. For this reason, analyst access is trust-based, and some organizations choose to reinforce that trust by ensuring that those with analyst access have training on proper data handling and usage. 

The following example shows one line from an advanced insights query: 

|Encrypted person identifier| After hours| Email hours| Function|Title|Organization|
|---------------------------|--------------|-------------|---------------|-----------------|-----|
|T5Y07H4VfKWcCC3| 7| 16| HR| Director| HR – Corp |

In this example, Viva Insights calculates **After hours** and **Email hours** for an individual. It prints the results on a row that includes that individual’s attributes from the organizational data provided by the Insights Administrator. The **Person identifier** is a cryptographically generated identifier derived from the person’s Microsoft 365 email address. The other attributes are effectively personal data. While it might not be possible to identify the user with any single one of the other columns (function, title, organization, and region), together these attributes might enable an analyst to identify a person. So, this group of attributes should be treated as potential personal data.

### Minimum group size 

Because it’s easier to guess information about an individual based on results about a smaller group, aggregated insights won’t show results for groups with fewer than 10 people. The Insights Administrator can choose to [increase this threshold](../setup-maint/manager-settings.md). The minimum group size applies to data visualizations in the advanced insights Power BI templates as well as organization insights for leaders and managers in Outlook and Teams. 

### Distribution masking 

Some insights measure how many people have a certain profile, like what percentage of an organization gets enough focus time. Aggregated results are protected by obscuring or masking results that would otherwise reveal that “almost all” or “almost none” of the group fit the profile, because that would effectively give you information about every individual in the group. This masking applies to organization insights for leaders and managers in Outlook and Teams. 

### Differential privacy 

Microsoft Viva Insights is serious about protecting individual privacy. Privacy can always be guaranteed if no information is revealed, which is not very useful. Similarly, making all information available can lead to high-fidelity metrics that compromise individual privacy. 

Differential privacy offers a balance between providing useful information and protecting individual privacy. Using methods from world-class researchers, Viva Insights randomly adjusts individual observations such that the aggregated adjustments offset each other, and the aggregated result that the user sees is still accurate. With differential privacy, users can’t discern true individual results, because the individual results used in the calculation have been changed. For more details, refer to [Differential Privacy for Everyone](https://download.microsoft.com/download/D/1/F/D1F0DFF5-8BA9-4BDF-8924-7816932F6825/Differential_Privacy_for_Everyone.pdf). 

The first application of differential privacy in Viva Insights is organization insights. These insights enable managers to understand how the people in their team are doing and to learn how to drive change by using aggregated collaboration data.  

No matter how aggregated averages are presented or used in organization insights, no manager or team leader can conclude with confidence anything specific about an individual that they couldn’t otherwise already know. 

Refer to [Differential privacy](https://www.microsoft.com/en-us/ai/ai-lab-differential-privacy?rtc=1) to learn more about how Microsoft AI is helping to define and use it. 

## Managing sensitive data 

Viva Insights provides the Microsoft 365 administrator and Insights Administrator with tools to manage what data gets processed, who has access, and specific data subject requests. 

### Managing what data gets processed 

You retain full control over what data is used and how it's used within Viva Insights. Viva Insights uses Microsoft 365 email and calendar metadata and external data defined by your organization (usually exported from an HR system) to compute how much time groups within your organization spend in meetings, emails, calls, and chats, and with whom. 

Viva Insights processes data sourced with organizational data from your own HR system and collaboration data from Microsoft 365 to provide analysts with a unified pool of data on which to perform analyses. 

### Data processed from Microsoft 365 

Viva Insights uses collaboration data from Microsoft 365. By assigning or not assigning a Viva Insights license to a person, the Microsoft 365 administrator controls whether that person's collaboration data is processed by Viva Insights. 

Viva Insights uses header information from Microsoft 365 email and calendar items. This header information includes sender and recipient, date, and subject lines for email, and organizer, attendee, and duration of meetings. Viva Insights never includes attachments and content in email and calendar items.  

It’s important to note that while Viva Insights uses this Microsoft 365 data, most of the header information is never directly available to users within the service. Rather, Viva Insights provides computations and metrics based on this information. Furthermore, using the settings within the service, you get to decide and configure what data to use and who can see it. Review the product privacy features documentation for full details. 

Microsoft 365 email, calendar, call, and instant message metadata provides the foundation for all analysis in Viva Insights, so the first step is to determine which users you want to include. When you choose a user to be included, Viva Insights uses the following information about items in that user's mailbox and calendar:

|Item |Originator |Recipient| Subject| Chronology| Status|
|-------|------------|---------|-----------|------|----|
|**email** | sender | recipients | subject line |sent time 
|**meeting** | organizer | invitees | subject line |scheduled time |attendee status 
|**call**  | organizer | invitees  | scheduled time, call joined time, call duration |call/join status |
|**chat** |sender of initial IM|recipients | IM sent time 

>[!Important]
> Attachments and text in the body of email and meetings are never used by Viva Insights. 

### Data processed from your organization 

To provide context to insights, Viva Insights uses descriptive information about employees. The Insights Administrator controls what descriptive information is available. For organization insights, only the reporting hierarchy (that is, who reports to whom) is available to the end users who are leaders and managers. For advanced insights, analysts can access other available descriptive information, like job function or geography. 

To enable analysis along organizational lines, you can provide HR data like disciplines, titles, locations, and managers. Viva Insights ensures that individual identities are never used in analyzing this information. However, it's important to take care to prevent incidental identification of users based on personal data, like names, employee identification numbers, or specific office locations. 

Additionally, consider risks of including attributes whose specific values might identify some individuals directly (such as the title field containing "CEO"), or might reduce the set of individuals below the aggregation thresholds that make individuals easily identifiable (for example, there might only be only a few Directors). 

Organizational data can come from HR, information systems, or other line-of-business data stores. Viva Insights combines Microsoft 365 email, calendar, call, and instant message metadata with the organizational data that you choose to use to provide rich, actionable insights into your company’s communication and collaboration trends to help you make more effective business decisions. 

The data sets are combined using the email addresses of the users, but the email addresses are never shown in Viva Insights through dashboards or query results. 

Note that other information provided in the organizational data set is exposed in advanced insights. Take care to ensure that the data set doesn't include personal data (for example, employee IDs). For more details, refer to [Prepare organizational data](../admin/prepare-org-data.md).

## Managing who has access to data 

The Microsoft 365 administrator can assign user roles with varying levels of access to organization insights and advanced insights. 

You control who gets to see the data and the results of the analysis.

### Advanced insights 

The following levels of permission provide access to the Viva Insights data: 

* The **Insights Analyst** role has full access to all advanced insights product features except the administrator features. 
* The **Insights Administrator** role has access to administrator features only (like **Organizational data** and **Privacy settings** in Viva Insights). 

Advanced insights, like other products that work with sensitive data (for example, HR systems) isn't meant for the general workforce. Rather, its users are expected to have training on how to handle sensitive information. Training should be specific to your organization. Suggested topics might include your organization’s HR policies, employee privacy policy, how to handle and store sensitive data, and insider trading. 

An Insights Analyst can access information within advanced insights. People assigned this role can run query data with meeting and email information—which falls under the category of non-identifying data—for analysis. However, if you choose to provide personal data, the analyst can discern whose metrics are being computed. So, it's important that these analysts are provided the requisite training before they're given access to Viva Insights. Additionally, Viva Insights logs all queries that analysts author, which allows you to audit them for consistency with your organizational policies and any DPIA that you completed. 

The tenant administrator provisions the Insights Analyst role. 

### Organization insights 

The **Insights Business Leader** role and group manager list govern access to organization insights in Outlook and Teams. 

People with the **Insights Business Leader** role assigned to them can see organization insights that include every person in their tenant. 

People enabled as group managers can see organization insights that only include people who report to them directly or indirectly. The Insights Administrator can assign users as group managers. The reporting hierarchy that determines who reports to whom is based on the required fields **PersonId** and **ManagerId**, which are included in the organizational data maintained by the Insights Administrator.

### Managing data subject requests 

The customer, as the data controller, is responsible for handling certain requests from employees, as data subjects. Microsoft, the data processor, provides controls in Viva Insights to honor data subject rights. 

Under the GDPR, data subjects might have rights to request exclusion from processing, access, correction, or deletion of their personal data. It's your organization’s role as data controller to evaluate whether a particular data subject request is valid and, if appropriate, to take action to fulfill the request. As a data processor, Microsoft provides mechanisms for your organization as the data controller to honor data subject rights through controls that are built into Viva Insights. 

* **Exclusion from processing** – Data subjects have the right to have their personal information excluded from processing. In Viva Insights, you can exclude an employee’s personal information from being processed simply by not assigning a Viva Insights license to that employee. 
* **Access** – Data subjects have the right to demand what personal information is being processed, and Viva Insights gives you the ability to export the raw data, which may contain personal data. The scope of such information is restricted to what's personally associable and doesn't contain aggregate metrics from which no personal information can be gleaned. 
* **Correction** – Data subjects have the right to rectify their personal data. Viva Insights only performs operations (mostly arithmetic) on data provided to it from other sources, like email and meeting data from Microsoft 365 or the organizational data that you upload. This data is not corrected through Viva Insights. 
* **Deletion** – Microsoft supports the GDPR [Right to erasure](/compliance/regulatory/gdpr-dsr-Office365#deleting-personal-data). Additionally, if necessary, customers themselves can also delete reports that identify the data subject. Customers can also delete the data subject from any other data (such as organizational data or CRM data) that they may have provided to Viva Insights. 
* **Transparency regarding processing** – Refer to [Metric definitions](../reference/metrics.md) for detailed information about the metrics calculated by Viva Insights, and what they mean.

## Retaining sensitive data 

Viva Insights doesn't retain any collaboration data that's older than 27 months. Depending on the state of user licenses, Viva Insights might be retaining less data. 

How long does Microsoft Viva Insights and in Teams retain the data that's collected? The answer depends on the state of the Viva Insights user licenses: 

* Data retention for active tenants 
* Data retention after a license is removed 
* Data retention and access after all subscriptions expire 

### Data retention for active tenants 

An active tenant is tenant that has one or more valid Viva Insights user licenses. 

By default, Viva Insights initially collects, processes, and retains 13 months' worth of data. Then, through weekly refreshes, Viva Insights increases this history until 27 months' worth of data is collected. After this point, older collaboration data is deleted as newer collaboration data is collected. 

This means that Viva Insights won't have any collaboration data that's older than 27 months. 

### Data retention after a license is removed 

If the Viva Insights license is removed from a user, Viva Insights retains that user's collaboration data that was collected during the period the license was assigned. Admins can continue to query the collaboration activity that this user participated in before they left. The person's collaboration data will be deleted according to the overall retention policy described in [Data retention for active tenants](#data-retention-for-active-tenants). 

To permanently remove data from users after licenses are removed, you can contact Microsoft customer support to request a collaboration data reset. 

For information about data deletion requests as handled under the GDPR, refer to [Managing data subject requests](#managing-data-subject-requests). 

>[!Note] 
>Microsoft 365 users can determine whether they have a Viva Insights license and, consequently, whether their data is being processed. For more information, refer to [Subscription status](../setup-maint/assign-licenses.md#subscription-status). 

### Data retention and access after all subscriptions expire 

If all of your subscriptions expire, you have until the end of your grace period to download data in the form of results. Refer to [To access query results](../analyst/query-results.md#to-access-query-results) for details. The duration of the grace period varies between countries and plans. Typically, it's either 90 days for volume-licensing purchases or 30 days for other purchase types. All backend data will be deleted in accordance with the [Microsoft 365 Data Handling Standard](/compliance/assurance/assurance-data-retention-deletion-and-destruction-overview). 

After this period has passed, you no longer will have access to Viva Insights. 

To download query results: 

1. Open the advanced insights app. If prompted, sign in with your work account. 
1. Select **Analyst > Query results**. 
1. In the row for the query results, select **Download** to download the results as a .csv file, which is archived as a .zip file.

## Working with sensitive data in advanced insights 

Analysts with access to advanced insights can use the analyst workbench to create their own insights. The following best-practice recommendations can help manage privacy risk associated with creating new insights. 

### Analysis planning 

Clarifying the scope of a project and expected benefits allows you to assess the amount of required and avoid more exposure than needed. 

Advanced insights offers tremendous analytical flexibility, so before you begin, it's important to have a clear purpose about what you want to analyze and why. Determine what specific questions about your organization you want to answer, and then consider how Viva Insights might help you find those answers. 

Having a clear question and then determining how a data analysis from Viva Insights will answer the question serves the following goals: 

* Keeps your efforts focused on a limited purpose and helps prevent your analysts from simply sifting through the analysis data. 
* Helps you scope the data to use and avoid privacy pitfalls such as including more data than is necessary, retaining data for longer than is necessary, and failing to be transparent with employees about how their personal data might be used. 

To the extent your organization is subject to GDPR, planning your analysis is a key step in determining and documenting legitimate interest in processing personal data with Viva Insights. 

### Data protection impact assessments (DPIA) 

Your legal or HR personnel can advise on whether a DPIA is warranted to determine whether the projects benefits outweigh the potential risks. 

The degree of privacy risk to employees and other users in your organization is largely within your control. That risk depends primarily on the organizational dataset that you'll import into Viva Insights and how you'll use that data. 

After you've developed an analysis plan but before you begin processing data in Viva Insights, determine whether you need to complete a DPIA. If your proposed use of Viva Insights involves processing personal data in a manner that could lead to high risks to the rights of employees and other users in your organization, completing a DPIA might be warranted. If you're unsure whether a DPIA is required, consult your organization’s privacy subject matter experts, like legal or HR personnel. 

Higher-risk data includes sensitive demographic data, like racial or ethnic origin, sex or gender, and trade union membership. Higher-risk uses of Viva Insights include using the service for profiling or to make automated decisions or predictions about employees. (Note that Microsoft designed Viva Insights to help people within organizations make data-driven decisions, not to automate those decisions.) 

If you determine that a DPIA is necessary for your proposed use of Viva Insights, you'll need to document several aspects of how you'll use the service to process personal data, including how the data will be collected; how it will be processed; the necessity of the processing in relation to the purpose; what risks the processing presents to employees; the data flows within and outside Viva Insights; feedback that you received from employees regarding the proposed data processing; and any other information that your organization’s data-protection officer (or equivalent) deems necessary for the DPIA. As a data controller, your organization is entirely responsible for determining your organization’s purposes for using Viva Insights. As a data processor, Microsoft informs you how the product functions and processes data pursuant to your configuration of the services. 

### Limiting data sensitivity 

During your project, consider at each step what least sensitive data will allow you to accomplish your goal.  

To minimize privacy risk, use the minimum data necessary to conduct your research. While adopting a strict policy of never using personal data and minimizing use of de-identified data in combination with identifying attributes can help address many of the risks inherent in using such data, such a policy can restrict the types of analyses that Viva Insights can perform. It's up to your organization to decide the best approach and policy for your organization. 

For example, many companies see the benefit of understanding aggregate collaboration patterns between different teams or departments within their organization. Fewer companies might be comfortable analyzing highly sensitive information like health data, real-time location, document content, and certain types of diversity demographics. 

### Subject matter experts 

Privacy and legal subject matter experts can help you stay ahead of potential data protection pitfalls. 

Consult with your organization’s HR, privacy, and legal subject matter experts in the countries where you'd  like to use Viva Insights. Analyses that might be acceptable in one country might be subject to more requirements (for example, notice and consent obligations) or even illegal in other countries. Due diligence is particularly important in highly regulated jurisdictions like the European Union. 

>[!Note]
>Some countries require employers to consult with employee representatives or seek approval from a works council before deploying certain information technology in the workplace, while others restrict when and how employers can process certain employee data. For example, if your company has employees in Germany or Netherlands, then you should consider if works council engagement or approval is required. Moreover, Viva Insights processes data from employee communications, which could be considered “communications data” (including “traffic data”) in Finland. So, if your company has employees in Finland, then you should understand how Finnish laws apply to the processing of employee personal data and communications or traffic data to determine if use of Viva Insights is permissible.  

