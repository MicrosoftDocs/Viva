---
title: "Understand how privacy works in Microsoft Viva"
ms.reviewer: loreenl
ms.author: elizapo
author: lizap
manager: elizapo
ms.date: 10/02/2023
audience: Admin
f1.keywords:
- NOCSH
ms.topic: solution-overview
ms.service: viva-suite
ms.localizationpriority: medium
ms.custom:
ms.collection:  
- M365initiative-viva
- m365solution-overview
- highpri
- tier1
- essentials-privacy
search.appverid:
- MET150
description: "Find Microsoft Viva privacy information."
---

# Understand how privacy works in Microsoft Viva

Microsoft is transparent about the specific policies, operational practices, and technologies that help you ensure the privacy of your data across Microsoft Viva.

- You control your data.
- We're transparent about where data is located and how it's used.
- We secure data at rest and in transit.
- We defend your data.

Privacy is built into all Microsoft Viva experiences. Microsoft Viva and the Viva apps adhere to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement) and follow Microsoft's compliance with [General Data Protection Regulation](/compliance/regulatory/gdpr) and the [Microsoft EU Data Boundary](https://www.microsoft.com/trust-center/privacy/european-data-boundary-eudb).

Microsoft Viva inherits privacy features and settings from Microsoft 365, Teams, SharePoint, and Viva Engage, where applicable.

In addition to the inherited controls, each Viva app has its own set of privacy controls that lets you customize the information you share. The following information describes how the Viva apps handle and store data, who can access it, and, if applicable, how you can manage it. 

## GDPR compliance
Microsoft Viva and the Viva apps support compliance with [General Data Protection Regulation](/compliance/regulatory/gdpr) (GDPR) requirements.

Additionally, see the following GDPR information for specific apps:

- Viva Connections and Viva Learning (SharePoint): [Safeguarding your SharePoint data](/sharepoint/safeguarding-your-data)
- Viva Engage (Yammer): [Manage GDPR data subject requests in Viva Engage](/viva/engage/manage-security-and-compliance/gdpr-requests-in-viva-engage-enterprise)
- Viva Goals: [Viva Goals security, privacy, and compliance](./goals/vg-privacy-and-security.md#viva-goals-gdpr-requests)
- Viva Insights: [Personal Insights privacy guide](insights/personal/overview/privacy-guide-admins.md#gdpr-compliance)

## Data residency
Data residency refers to the geographic location where data is stored at rest. The way that data is transferred and stored in Microsoft Viva is defined in the [Microsoft Products and Services Data Protection Addendum (DPA)](https://www.microsoft.com/licensing/docs/view/Microsoft-Products-and-Services-Data-Protection-Addendum-DPA).


If you are using [Viva Connections](/microsoft-365/enterprise/m365-dr-workload-viva-connections), you can purchase the [Advanced Data Residency add-on in Microsoft 365](/microsoft-365/enterprise/advanced-data-residency), which provides more tools to address data residency requirements. 

All data within Viva is stored within the customer tenant for any given Viva application and follows the standard Microsoft 365 data storage guidelines by available geography. The following table provides information about where the data for each app resides, along with links to more information.

|Viva app|Where the data resides|More information|
|-|-|-|
|Viva Amplify|Data is stored in the data center where the associated Microsoft 365 tenant resides. If your organization is using SharePoint, Amplify follows the [SharePoint data residency policy](/microsoft-365/enterprise/m365-dr-workload-spo).|[Privacy and security in Microsoft Viva Amplify](/viva/amplify/privacy-security)|
|Viva Connections|Data is stored in the data center where the associated Microsoft 365 tenant resides. For tenants located in Germany or the EU, none of the data is transferred to a third country.<br><br>**Note:** Data from third-party apps is governed by the data and privacy agreements for those apps. This information applies to data from Microsoft apps.|[Data Residency for Viva Connections](/microsoft-365/enterprise/m365-dr-workload-viva-connections)|
|Viva Engage|Committed to storing message bodies and files attached to messages at rest within a specific geographical area (Geo). Data is stored in either Yammer cloud storage or SharePoint. Files saved in SharePoint are stored in SharePoint Online per your SharePoint Online data residency policy. <br><br>Mobile push notifications require sending data to a third party notification service (Apple or Google), which might be outside your Geo.|[Data residency - Yammer](/yammer/manage-security-and-compliance/data-residency)|
|Viva Glint|The data region for Viva Glint is determined by the default geography of the tenant, not individual users, and is stored in US or EU data centers based on central tenant location.||
|Viva Goals|Data for customers located in the European Union Data Boundary (EUDB) or the United Kingdom is stored in data centers located in the EU. The data for all other tenants is stored in data centers located in the United States.|[Viva Goals data residency](./goals/vg-privacy-and-security.md#viva-goals-data-residency)|
|Viva Insights|**Personal insights** - Processed and stored in the employee’s Exchange Online mailbox. Data residency is based on the employee's mailbox location.<br>**Manager/Leader/Advanced Insights** - The data region for Manager/Leader and Advanced is determined by the Default Geography of the tenant, not individual users.<br><br>Data at Rest (header info and metadata sourced from Exchange Online and Teams, but not message content or attachments) is stored in US, EU, EMEA, APAC based on central tenant location.|[Viva Insights - Advanced/Manager/Leader](/microsoft-365/enterprise/m365-dr-workload-other#viva-insights--advanced-mgr-leader)<br><br>[Viva Insights - Personal](/microsoft-365/enterprise/m365-dr-workload-other#viva-insights--personal)
|Viva Learning|Viva Learning doesn’t store any personal data since usage and consumption data is aggregated.<br><br>Integration with SharePoint is currently only supported for sites hosted from the home geography of the tenant. For example, a French tenant can only link SharePoint sites hosted in France to Viva Learning.|[Viva Learning data residency](/microsoft-365/enterprise/m365-dr-workload-other)|
|Viva Pulse|Data for customers located in the European Union Data Boundary (EUDB) is stored in data centers located in the EU. The data for all other tenants is stored in data centers located in the United States|[Data residency for Viva Pulse](/viva/pulse/get-started/data-residency-for-viva-pulse)

For more information, see:
- [Microsoft 365 data locations](/microsoft-365/enterprise/o365-data-locations)
- [Microsoft Privacy - Where is Your Data Located](https://www.microsoft.com/trust-center/privacy/data-location)
- [Licensing Documents (microsoft.com)](https://www.microsoft.com/licensing/docs/view/Licensing-Use-Rights)

## How Microsoft Viva uses AI
> [!IMPORTANT]
> We’re extending [Copilot to Microsoft Viva](https://techcommunity.microsoft.com/t5/viva-goals-blog/the-future-of-goal-setting-with-viva-goals-copilot-customized/ba-p/3800587) to help leaders boost employee engagement and improve business performance. The Copilot System combines the power of large language models (LLMs), including GPT-4, with the Microsoft 365 and Microsoft Viva apps, as well as your business data in the Microsoft Graph—and makes it accessible through natural language. <br><br>More information about additional AI capabilities in Microsoft Viva and the Viva apps will be available soon.

Viva Connections uses AI to rank content in the feed. Microsoft's use of artificial intelligence is governed by the [Responsible AI Standard](https://www.microsoft.com/ai/responsible-ai).

For more information on how Viva uses AI, see the following:
- [Get answers to common questions about the Viva Connections Feed](connections/faqs-viva-connections-feed.md)

## App-specific data information
Each of the Viva apps collects and stores data in different ways, based on the intent of the app. You control your data, but how you control it differs depending on the app.

### Viva Amplify
Viva Amplify campaigns are set as private by default because campaigns are designed to be a private collaborative space for campaign team members to work and build their communications. Changing this setting is not recommended.

For more information about Viva Amplify, see [Overview of Microsoft Viva Amplify](/viva/amplify/overview-viva-amplify).

### Viva Connections
Privacy and security controls:
- You control what content is available through the app.
- Privacy settings inherited from SharePoint, Teams, Viva Engage/Viva

|What info is available?|Who can access it?|How is it managed?|
|-|-|-|
|Conversations, resources, and apps from Microsoft services (like Teams and SharePoint) and third-party apps (by using the SharePoint Framework)<br><br>For users with elevated permissions, aggregated analytics data about traffic, usage by experience, and usage by platform.|Users with access to the SharePoint resources<br><br>For analytics, users with site member or higher access to the SharePoint home site that supports the Connections instance.|Information is visible to users based on the setting and their role in the organization<br><br>Different permission levels are required based on the content creator role (for example Home site or Dashboard).<br><br>Dashboard authors can target the cards to specific audiences by using Microsoft Entra groups.|

For more information about Viva Connections, see [Overview of Viva Connections](connections/viva-connections-overview.md).

### Viva Engage
Privacy and security controls:
- Security and privacy settings are managed as a part of Viva Engage.
- Role-based access

|What info is available?|Who can access it?|How is it managed?|
|-|-|-|
|Public announcements, private messages, posts, polls, and videos shared in communities, the inbox, and the Storyline.<br>User profiles (through Viva Engage)<br>Questions and answers<br>Rewards and recognition<br>Sentiment/usage analysis (personal analytics, audience analytics, campaign analytics, Answers analytics)|All users with a paid Microsoft or Office 365 subscription (as part of the Viva Engage license) and accessible through Microsoft Teams.<br><br>By default, private content is restricted to the participants in the content (for example, the sender and recipient of a private message); however, admins can be temporarily granted access to private content. (You'll need to manually remove this access as well.)|The Engage admin can set up and configure Viva Engage through the Engage admin center (present in the Teams app).|

For more information about privacy in Viva Engage, see [Overview of security and compliance in Viva Engage](engage/manage-security-and-compliance/security-and-compliance.md).

### Viva Goals
For information about privacy in Viva Goals, see [Viva Goals security, privacy, and compliance](./goals/vg-privacy-and-security.md).

### Viva Insights
Privacy and security controls:
- Role-based access
- Everyone's data is kept private
- Mailbox security through Exchange

|What info is available?|Who can access it?|How is it managed?|
|-|-|-|
|Personal insights (visible only to the individual)<br>Manager and leader insights (always aggregated and deidentified)<br>Organization insights (aggregated and deidentified, with data access restricted to assigned analysts)<br><br>**Note:** A manager or leader needs to have nine direct reports for the data to be aggregated. The admin can increase this threshold.|Insights only available to licensed users (Personal Insights) and assigned analysts or managers (Manager / Leader / Organization insights)|Admins can configure what information to include in insights, set access levels, and opt individual users in or out by using the Microsoft 365 admin center.<br><br>Individual users can opt in or out by going to the Settings > Privacy menu in the Viva Insights app in Teams or on the web.|

For more information on how to manage access to data in Viva Insights, see [Managing who has access to data](insights/advanced/privacy/privacy.md#managing-who-has-access-to-data).

For more information about privacy and data protection in Viva Insights, see the following articles:
- [Privacy guide for the Insights app](insights/personal/teams/privacy.md)
- [Privacy guide for admins](insights/personal/overview/privacy-guide-admins.md)
- [Technical privacy guide for organization insights and advanced insights](insights/advanced/privacy/privacy.md)


### Viva Learning
Privacy and security controls:
- SharePoint integration supports local content
- Role-based access

|What info is available?|Who can access it?|How is it managed?|
|-|-|-|
|Training content from Microsoft, third party providers, and customer-owned content.<br>Learning object content metadata, such as title, description, author, and language<br>User data, such as bookmarks, recently viewed, recommended courses, assigned courses, and completion records<br>Required service data, such as error logs<br>Diagnostic data|The Viva Learning app is discoverable to all users with a paid Microsoft or Office 365 subscription and access to Microsoft Teams.<br><br>Individual completion data and recommendations are available to those individuals and anyone that they share recommendations with.|Admins can control whether individual users can use Viva Learning and what they can do by changing user and group settings in the Teams admin center.<br><br>Admins can also turn on or off the storage of diagnostic data.|

For more information about Viva Learning, see [Microsoft Viva Learning](/viva/learning/).



## More resources

- [Microsoft Viva compliance](./viva-compliance.md)
- [Microsoft Viva security](./microsoft-viva-security.md)
- [Viva admin roles and tasks](./microsoft-viva-admin-roles.md)
