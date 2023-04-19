---
title: "Understand how privacy works in Microsoft Viva"
ms.reviewer: loreenl
ms.author: elizapo
author: lizap
manager: pamgreen
ms.date: 4/20/2023
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
localization_priority: Priority
ms.custom:
ms.collection:  
- M365initiative-viva
- m365solution-overview
- highpri
- tier1
search.appverid:
- MET150
description: "Find Microsoft Viva privacy information."
---

# Understand how privacy works in Microsoft Viva
Microsoft is committed to providing you with the information and controls you need to make choices about how your data is collected and used when you're using Microsoft Viva. Privacy and security are built into all Microsoft Viva experiences. Privacy describes the way that we help protect your data or information, while security describes the way that we help protect your assets and resources.  

Microsoft Viva and the Viva apps adhere to the Microsoft Privacy Statement - Microsoft privacy and Microsoft support for [General Data Protection Regulation - Microsoft GDPR](/compliance/regulatory/gdpr) and [Microsoft EU Data Boundary Overview](https://www.microsoft.com/trust-center/privacy/european-data-boundary-eudb). See [Employee Privacy and Data Protection](https://www.microsoft.com/microsoft-viva/privacy) for more information.

Both privacy and security start with ensuring that only authorized users can access your data and resources. Microsoft Viva inherits privacy and security features and settings from Teams, SharePoint, Yammer, and Azure Active Directory Groups where applicable.

In addition to the inherited controls, each Viva app has its own set of privacy controls that lets you customize the information you share. The following information describes how the Viva apps handle and store data, who can access it, and, if applicable, how you can manage it. 

## GDPR compliance
All Viva apps built on the Microsoft cloud infrastructure support compliance with EU General Data Protection Regulation (GDPR) requirements.

Microsoft is transparent about the specific policies, operational practices, and technologies that help you ensure the security, compliance, and privacy of your data across Microsoft services.

- You control your data.
- We're transparent about where data is located and how it's used.
- We secure data at rest and in transit.
- We defend your data.

To learn more, see [GDPR compliance and General Data Protection Regulation - Microsoft GDPR](https://www.microsoft.com/trustcenter/privacy/gdpr).

Additionally, see the following information for specific apps:

- Viva Connections, Viva Topics, Viva Learning (SharePoint): [Safeguarding your SharePoint data](/sharepoint/safeguarding-your-data)
- Viva Engage (Yammer): [Manage GDPR data subject requests in Yammer Enterprise](/yammer/manage-security-and-compliance/gdpr-requests-in-yammer-enterprise)
- Viva Insights: [Personal Insights privacy guide](insights/personal/overview/privacy-guide-admins.md#gdpr-compliance)
- Viva Goals: [Viva Goals security, privacy, and compliance](./goals/vg-privacy-and-security.md#viva-goals-gdpr-requests)
- Viva Sales: [Responding to Data Subject Rights (DSR) requests for Microsoft Dataverse customer data](/power-platform/admin/common-data-service-gdpr-dsr-guide)

## Data residency
Personal data is transferred and stored as set forth in the [Microsoft Products and Services Data Protection Addendum (DPA)](https://www.microsoft.com/licensing/docs/view/Microsoft-Products-and-Services-Data-Protection-Addendum-DPA).

Data residency refers to the geographic location where data is stored at rest. Many customers, particularly in the public sector and regulated industries, have distinct requirements around protecting personal or sensitive information. In addition, in certain countries, customers are expected to comply with laws and regulations that explicitly govern data storage location.

Viva Connections and Viva Topics are included in the Advanced Data Residency add-on in Microsoft 365, which provides more tools to address data residency requirements. Learn more:
- [Data Residency for Viva Connections](/microsoft-365/enterprise/m365-dr-workload-viva-connections)
- [Data Residency for Viva Topics](/microsoft-365/enterprise/m365-dr-workload-viva-topics)

All data within Viva is stored within the customer tenant for any given Viva application and follows the standard Microsoft 365 data storage guidelines by available geography. The following table provides information about where the data for each app resides, along with links to more information.

|Viva app|Where the data resides|More information|
|-|-|-|
|Viva Connections|Data is stored in the data center where the associated Microsoft 365 tenant resides. For tenants located in Germany or the EU, none of the data is transferred to a third country.<br><br>**Note:** Data from third-party apps is governed by the data and privacy agreements for those apps. This information applies to data from Microsoft apps.|[Data Residency for Viva Connections](/microsoft-365/enterprise/m365-dr-workload-viva-connections)|
|Viva Learning|Viva Learning doesn’t store any personal data or any individually identifiable information since usage and consumption data is aggregated.<br><br>Integration with SharePoint is currently only supported for sites hosted from the home geography of the tenant. For example, a French tenant can only link SharePoint sites hosted in France to Viva Learning.|[Viva Learning data residency](/microsoft-365/enterprise/m365-dr-workload-other)|
|Viva Insights|**Personal insights** - Processed and stored in the employee’s Exchange Online mailbox. Data residency is based on the employee's mailbox location.<br>**Manager/Leader/Advanced Insights** - The data region for Manager/Leader and Advanced is determined by the Default Geography of the tenant, not individual users.<br><br>Data at Rest (header info and metadata sourced from Exchange Online and Teams, but not message content or attachments) is stored in US, EU, EMEA, APAC based on central tenant location.|[Viva Insights - Advanced/Manager/Leader](/microsoft-365/enterprise/m365-dr-workload-other#viva-insights--advanced-mgr-leader)<br><br>[Viva Insights - Personal](/microsoft-365/enterprise/m365-dr-workload-other#viva-insights--personal)
|Viva Topics|Follows the standard Microsoft 365 data storage guidelines by available geography.|[Data Residency for Viva Topics](/microsoft-365/enterprise/m365-dr-workload-viva-topics#how-can-i-determine-customer-data-location)|
|Viva Engage|Committed to storing message bodies and files attached to messages at rest within a specific geographical area (Geo). Data is stored in either Yammer cloud storage or SharePoint. Files saved in SharePoint are stored in SharePoint Online per your SharePoint Online data residency policy. <br><br>Be aware that mobile push notifications require sending data to a third party notification service (Apple or Google), which might be outside your Geo.|[Data residency - Yammer](/yammer/manage-security-and-compliance/data-residency)|
|Viva Goals|Data for customers located in the European Union Data Boundary (EUDB) is stored in data centers located in the EU. The data for all other tenants is stored in data centers located in the United States.|[Viva Goals data residency](/goals/vg-privacy-and-security#viva-goals-data-residency).|
|Viva Sales|When Viva Sales is connected to Dynamics 365, Viva Sales data is stored with the Dynamics 365 Sales Dataverse instance.<br><br>When Viva Sales is connected to a non-Dynamics 365 CRM, a default Dataverse instance specific to Viva Sales is provided to your tenant. Viva Sales data is stored in the default instance in addition to your CRM.|[Data handling in Viva Sales](/viva/sales/data-handling)|

For more information, see:
- [Microsoft 365 data locations](/microsoft-365/enterprise/o365-data-locations)
- [Microsoft Privacy - Where is Your Data Located](https://www.microsoft.com/trust-center/privacy/data-location)
- [Licensing Documents (microsoft.com)](https://www.microsoft.com/licensing/docs/view/Licensing-Use-Rights)

## How Microsoft Viva uses AI

> [!IMPORTANT]
> We’re extending the [Copilot System from Microsoft 365](https://www.youtube.com/watch?v=E5g20qmeKpg) to Microsoft Viva to help leaders boost employee engagement and improve business performance. The Copilot System combines the power of large language models (LLMs), including GPT-4, with the Microsoft 365 and Microsoft Viva apps, as well as your business data in the Microsoft Graph — and makes it accessible through natural language. <br><br>More information about additional AI capabilities in Microsoft Viva and the Viva apps will be available soon.

Viva Connections uses AI to rank content in the feed, while Viva Topics uses it to detect and identify topics. Microsoft's use of artificial intelligence is governed by the [Responsible AI Standard](https://www.microsoft.com/ai/responsible-ai).

For more information on how Viva uses AI, see the following:
- [Get answers to common questions about the Viva Connections Feed](connections/faqs-viva-connections-feed.md)
- [Topic discovery and curation in Microsoft Viva Topics](topics/topic-experiences-discovery-curation.md)

## App-specific data information
Each of the Viva apps collects and stores data in different ways, based on the intent of the app. You remain in charge of what we collect, but how you control it differs depending on the app.

### Viva Connections
Privacy and security controls:
- You control what content is available through the app.
- Privacy settings inherited from SharePoint, Teams, Yammer/Viva

|What info is available?|Who can access it?|How is it managed?|
|-|-|-|
|Conversations, resources, and apps from Microsoft services (like Teams and SharePoint) and third-party apps (by using the SharePoint Framework)<br><br>For users with elevated permissions, aggregated analytics data about traffic, usage by experience, and usage by platform.|Users with access to the SharePoint resources<br><br>For analytics, users with site member or higher access to the SharePoint home site that supports the Connections instance.|Information is visible to users based on the setting and their role in the organization<br><br>Different permission levels are required based on the content creator role (for example Home site or Dashboard).<br><br>Dashboard authors can target the cards to specific audiences by using Azure AD groups.|


For more information about Viva Connections, see [Overview of Viva Connections](connections/viva-connections-overview.md).

### Viva Learning
Privacy and security controls:
- SharePoint integration supports local content
- Role-based access

|What info is available?|Who can access it?|How is it managed?|
|-|-|-|
|Training content from Microsoft, third party providers, and customer-owned content.<br>Learning object content metadata, such as title, description, author, and language<br>User data, such as bookmarks, recently viewed, recommended courses, assigned courses, and completion records<br>Required service data, such as error logs<br>Diagnostic data|The Viva Learning app is discoverable to all users with a paid Microsoft or Office 365 subscription and access to Microsoft Teams.<br><br>Individual completion data and recommendations are available to those individuals and anyone that they share recommendations with.|Admins can control whether individual users can use Viva Learning and what they can do by changing user and group settings in the Teams admin center.<br><br>Admins can also turn on or off the storage of diagnostic data.|

For more information about Viva Learning, see [Microsoft Viva Learning](/viva/learning/).

### Viva Insights
Privacy and security controls:
- Role-based access
- Everyone's data is kept private
- Mailbox security through Exchange

|What info is available?|Who can access it?|How is it managed?|
|-|-|-|
|Personal insights (visible only to the individual)<br>Manager and leader insights (always aggregated and deidentified)<br>Organization insights (aggregated and deidentified, with data access restricted to assigned analysts)<br><br>**Note:** A manager or leader needs to have nine direct reports for the data to be aggregated. The admin can change adjust this threshold.|Insights only available to licensed users (Personal Insights) and assigned analysts or managers (Manager / Leader / Organization insights)|Admins can configure what information to include in insights, set access levels, and opt individual users in or out by using the Microsoft 365 admin center.<br><br>Individual users can opt in or out by going to the Settings > Privacy menu in the Viva Insights app in Teams or on the web.|

For more information on how to manage access to data in Viva Insights, see [Managing who has access to data](insights/advanced/privacy/privacy.md#managing-who-has-access-to-data).

For more information about privacy and data protection in Viva Insights, see the following articles:
- [Privacy guide for the Insights app](insights/personal/teams/privacy.md)
- [Privacy guide for admins](insights/personal/overview/privacy-guide-admins.md)
- [Technical privacy guide for organization insights and advanced insights](insights/advanced/privacy/privacy.md)


### Viva Topics
Privacy and security controls:
- Role-based access control
- You direct Viva Topics where to start discovery

|What info is available?|Who can access it?|How is it managed?|
|-|-|-|
|Topics are generated from documents and other content. Any topic metadata (such as names, descriptions, related people, and docs) follows the access permissions and other policies set up by the tenant. Topics maintains awareness of where topic metadata is inferred from, so only users who have permissions to see the original documents can see the corresponding topic metadata.<br><br>Users can curate topic pages in the knowledge center, and those topic pages follow general SharePoint policies.<br><br>Users can also rate the relevance of topics and various attributes. Feedback is used to reject or confirm topics and topic metadata inferred by AI, which helps ensure knowledge base quality for the enterprise.|Users only see content they already have access to (existing content permissions), with access dependent on the topic generated automatically or manually.|Admins specify which data sources to use to create topics (such as [SharePoint sites](topics/topic-experiences-discovery.md#select-sharepoint-topic-sources) and MS Graph connectors), which content to exclude from topic indexing based on [sensitivity labels](/microsoft-365/compliance/sensitivity-labels), [which people to exclude from topic indexing](topics/topic-experiences-discovery.md#exclude-people-from-being-suggested-for-topics-by-ai), who can view topics (in addition to the read permissions to topic metadata), who can contribute, and who can manage topics.|

For more information about privacy in Viva Topics, see [Security and privacy in Microsoft Viva Topics](topics/topic-experiences-security-privacy.md)

### Viva Engage
Privacy and security controls:
- Security and privacy settings are managed as a part of Yammer.
- Role-based access

|What info is available?|Who can access it?|How is it managed?|
|-|-|-|
|Public announcements, private messages, posts, polls, and videos shared in communities, the inbox, and the Storyline.<br>User profiles (through Yammer)<br>Questions and answers<br>Rewards and recognition<br>Sentiment/usage analysis (personal analytics, audience analytics, campaign analytics, Answers analytics)|All users with a paid Microsoft or Office 365 subscription (as part of the Yammer license) and accessible through Microsoft Teams.<br><br>By default, private content is restricted to the participants in the content (for example, the sender and recipient of a private message); however, admins can be temporarily granted access to private content. (You'll need to manually remove this access as well.)|The Engage admin can setup and configure Yammer and Viva Engage through the Engage admin center (present in the Teams app).|

For more information about privacy in Viva Engage, see [Configure and review privacy and security settings](engage/setup.md#configure-and-review-privacy-and-security-settings).

### Viva Goals
Privacy and security controls:
- Role-based access
- Data encryption

|What info is available?|Who can access it?|How is it managed?|
|-|-|-|
|OKR data<br>User data<br><br>Third-party integrations may have additional information, which is subject to the privacy policies of those third-party apps and programs.|Access to OKRs is based on role.<br><br>Viva Goals users can view, create and perform actions. <br><br>For private OKRs, there are also view permissions. This can be for individual, team and organization OKRs.|Organization admins and tenant admins control the settings via the admin dashboard. The dashboard offers customizable settings to provide flexibility on what works best for your organization.<br><br>Individual users can view, edit, and delegate permissions for their OKRs in Viva Goals, on the **My OKRs** tab.|

For more information about privacy in Viva Goals, see [Viva Goals security, privacy, and compliance](./goals/vg-privacy-and-security.md).


### Viva Sales
Viva Sales respects company security and privacy policies in sharing customer contact information, including CRM access controls and user permissions.

For more information about data handling in Viva Sales, see [Data handling in Viva Sales](/viva/sales/data-handling).

## More resources

- [Microsoft Viva compliance](/Viva/viva-compliance.md)
- [Microsoft Viva security](/Viva/microsoft-viva-security.md)
- [Viva admin roles and tasks](/viva/microsoft-viva-admin-roles)
