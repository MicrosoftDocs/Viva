---
title: "Overview of security and compliance in Viva Engage"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89 
manager: elizapo
ms.date: 09/26/2024
audience: Admin
ms.topic: reference
ms.localizationpriority: medium
ms.service: viva-engage
ms.collection: essentials-security
ms.custom: Adm_Yammer
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: a2c84111-1da6-4c70-8646-bfe585b93c90
description: "Find answers to questions about Viva Engage security, management, and deployment."
---

# Overview of security and compliance in Viva Engage

Viva Engage Enterprise administrative tools help you protect your Viva Engage data and comply with evolving legal and regulatory standards, including GDPR.

For information about policies, tools, and best practices for all of Microsoft 365, see [Overview of security and compliance in Microsoft 365](https://support.office.com/article/dcb83b2c-ac66-4ced-925d-50eb9698a0b2).

Viva Engage Enterprise offers admins security and compliance tools that aren't part of Viva Engage Basic. Items marked with an asterisk (\*) are only available in Viva Engage Enterprise. The [Security FAQ](security-and-compliance.md#Security) section of this article describes security, privacy, and business continuity features that apply to both Viva Engage Basic and Viva Engage Enterprise.

## Security admin features

| Task <br/> | How To <br/> |
|:-----|:-----|
|Set password policies and logical firewalls to control access to Viva Engage.  <br/> |[Manage Viva Engage security settings](viva-engage-security-settings.md) \*  <br/> |
|Manage users and maintain single identity for users across all of Office 365.  <br/> |[Enforce Microsoft 365 identity for Viva Engage users](../configure-your-viva-engage-network/enforce-office-365-identity.md) \*  <br/> |
|Provide secured access to Viva Engage on iOS and Android devices, and control device access to protect corporate data by using Microsoft Intune.  <br/> |[Manage Viva Engage with Microsoft Intune](manage-viva-engage-with-intune.md) \*  <br/> |
|Use multiple levels of admin roles so you can assign the correct permissions to match employee's roles.  <br/> |[Manage Viva Engage admins](../manage-viva-engage-users/manage-viva-engage-admins.md) \*  <br/> |
|Prevent or limit file uploads.|[Configure your Viva Engage network](../configure-your-viva-engage-network/configure-viva-engage.md) \*|
|Control external network access.  <br/> |[Manage Viva Engage security settings](viva-engage-security-settings.md) \*  <br/> |
|Track changes to users, groups, and admins.  <br/> |[Track Viva Engage events in the Microsoft 365 audit log and with the Management Activity API](../track-engage-events.md) \*  <br/> |

## Compliance admin features

### Legal and regulatory compliance

| Task <br/> | How To <br/> |
|:-----|:-----|
|Comply with GDPR requirements.  <br/> |[Manage GDPR data subject requests in Viva Engage](gdpr-requests-in-viva-engage-enterprise.md) \* |
|View compliance reports. Viva Engage is Tier-C compliant in the Microsoft 365 Compliance Framework, which covers SOC 1, HIPAA, EU Model Clauses, IRAP, and (SEC) Rule 17a-4(f).  <br/> |[Compliance Framework Documentation for Microsoft 365](/compliance/regulatory/offering-home)\* 
|Control data retention policies, and view private messages if needed for discovery purposes.  <br/> |[Manage Viva Engage data compliance](manage-data-compliance.md) \*  <br/> |
|Export data to review compliance issues.  <br/> |[Export data from Viva Engage](../eac-as-manage-data.md) \* |
|Track changes to users, admins, and groups.  <br/> |[Track Viva Engage events in the Microsoft 365 audit log and with the Management Activity API](../track-engage-events.md)\*  <br/>|

### Keep content appropriate and available to only those who should see it

| Task <br/> | How To <br/> |
|:-----|:-----|
|Set up a usage policy to ensure only appropriate content is posted.  <br/> |[Set up a Viva Engage usage policy](../set-up-usage-policy.md) \*  <br/> |
|Monitor keywords for unacceptable or inappropriate content so you can intervene if necessary.  <br/> |[Monitor keywords](manage-data-compliance.md#MonitorKeywords)\* |

### Monitor usage

| Task <br/> | How To <br/> |
|:-----|:-----|
|Monitor Viva Engage admin and user transactions.  <br/> |[Track Viva Engage events in the Microsoft 365 Audit log and with the Management Activity API](../track-engage-events.md) \*  <br/> |
|Gain insight into how people in your organization use Viva Engage. Reports and APIs make information available to admins, and group insights and seen counts are available for community managers, group admins, and members.  <br/> |[Activity Reports in the Microsoft 365 admin center](https://support.office.com/article/0d6dfb17-8582-4172-a9a9-aed798150263)\*  <br/> [Microsoft 365 Adoption content pack](https://support.office.com/article/77ff780d-ab19-4553-adea-09cb65ad0f1f)\*  <br/> [Microsoft Graph reporting APIs](https://go.microsoft.com/fwlink/?linkid=875445) <br/> [View community insights in Viva Engage](https://support.microsoft.com/en-us/office/view-community-insights-in-viva-engage-48bc648e-b567-49d7-b2b5-5fea23777c46?storagetype=live) |

### Stay organized and current with organizational changes

| Task <br/> | How To <br/> |
|:-----|:-----|
|Use Microsoft 365 group naming policies to enforce consistent group naming.  <br/> |[Microsoft 365 Groups naming policy](https://support.office.com/article/6ceca4d3-cad1-4532-9f0f-d469dfbbb552)\*  <br/> |
|For large organizations, use dynamic groups to update group membership automatically as people join, leave, or move within your organization.  <br/> |[Create a dynamic group in Viva Engage](../manage-viva-engage-groups/create-a-dynamic-group.md) \*  <br/> |
|Set expiration policies for Microsoft 365 connected Viva Engage groups. When set, group owners are prompted to renew the groups if they still need them.  <br/> |[Microsoft 365 Group Expiration policy](https://support.office.com/article/8d253fe5-0e09-4b3c-8b5e-f48def064733.aspx)\*  <br/> |

<a name="Security"> </a>
## Security FAQ

### Q: Who can access the Viva Engage network?

A: Only users with a valid and verified company email address can join your Viva Engage network. Viva Engage has functionality to create external networks to collaborate securely with third parties.

### Q: What endpoints need to be reachable for Viva Engage users?

A: As of January 2024, all Viva Engage users need to be able to access
**engage.cloud.microsoft**. We recommend against using a list of IP address ranges to control access since they can change and create access problems for users.

For complete Microsoft 365 URL and IP address ranges info, see [Microsoft 365 endpoints](/microsoft-365/enterprise/microsoft-365-endpoints).

### Q: Where is the data hosted?

A: Viva Engage data is hosted in Microsoft managed datacenters. See [Where is your data located](/microsoft-365/enterprise/o365-data-locations) to find the data centers for the country in which your company is located. Viva Engage operates out of Microsoft's global network of data centers. These centers have 24/7/365 video surveillance, biometric and pin-based locks, strict personnel access controls and detailed visitor-entry logs.

For more information, see [Viva Engage data residency](data-residency.md).

### Q: What's the Viva Engage privacy policy? How do you treat my data?

A: Our privacy policy is publicly shared and available here, as part of the: [Microsoft Online Services Privacy Statement](https://go.microsoft.com/fwlink/?LinkID=331314).

### Q: What is the Viva Engage security policy?
<a name="SecurityPolicy"> </a>

A: Viva Engage is included in the [Microsoft Trust Center](https://go.microsoft.com/fwlink/?linkid=2083681).

### Q: Who has access to the data?

A: Only employees with a legitimate business need can access customer data, and all access is on an approval‐only basis. All access is logged and regularly audited.

### Q: Is the data encrypted?
<a name="Encryption"> </a>

A: All data in transit into and out of the production environment is always encrypted. Communication with Viva Engage is over HTTPS (TLS 1.2 supported) regardless of user endpoint (web, desktop app, mobile app, API). In addition to being encrypted in transit, Viva Engage data is encrypted at rest with AES-256 bit key encryption.

Current versions of the Viva Engage iOS and Android mobile apps use Apple and Google services for final delivery to end user devices. To ensure confidentiality of information between the Viva Engage service and the device, we use Push Notification Encryption to protect notifications in transit. Encrypted notifications are available for the Viva Engage iOS mobile app version 7.36.0 or later. They're also available for the Viva Engage Android mobile app version 5.6.5 or later.

### Q: What is Viva Engage's architecture?

A: The architecture is driven by the needs of an Enterprise Social Network (ESN). An ESN is successful only if users adopt and engage with the platform. As such, Viva Engage is architected and developed in a way to support adoption and engagement, allowing rapid iterations of technology.

Viva Engage is a set of loose components, coupled with APIs. These are developed and released independently using many different best-in-class codes and technologies. Viva Engage is a public cloud, SaaS, multitenant architecture only. We use a data-driven, rapidly iterating development approach to measure the success of the platform using the key metrics of end-user engagement and adoption.

### Q: Who owns the data posted in the Viva Engage network?

A: Data posted into a Viva Engage Basic network is owned by the individuals posting that data. Those users are the data controllers for their content. Under Viva Engage Enterprise, the company is the data controller, and ownership of all data transfers to the company. Viva Engage is a data processor and has no rights to any content or responsibilities for the data posted within a Viva Engage network.

### Q: Do you comply with the data protection act in my country?

A: It's the data controller's responsibility to comply with the data protection legislation that affects them. Viva Engage has controls in place to facilitate data controllers' (individuals and companies) compliance with their data protection legislation.

### Q: Can we perform an on‐site visit or audit of your facilities?

A: Viva Engage doesn't permit customers to perform on‐site audits. With over 200,000 customers, audits aren't feasible. It's also a risk to the security of the service. We'll answer any security questions openly and transparently.

### Q: Do you conduct third‐party audits or testing?

A: Penetration tests of the Viva Engage infrastructure are conducted yearly as part of Microsoft 365.

### Q: How is data separated from other customers?

A: Viva Engage is a true multi-tenant model. As such, customers' data is logically separated with strict controls to ensure separation of tenant data. The web application servers of Viva Engage are physically and logically separated from servers that store customer data.

### Q: What is the difference between the security of an enterprise social network and Facebook?

A: Your Viva Engage network is private to your company. Only users with a valid and verified email address for your company can join your Viva Engage network. Viva Engage was created as an Enterprise Social Network with security built‐in at every level and a high degree of control available. It includes integration with corporate security systems such as Microsoft Entra ID and single sign-on.

### Q: What is the difference between security of Viva Engage Basic and Viva Engage Enterprise?

A: The underlying security of both is identical. Viva Engage Enterprise brings more administrative control. It also provides the ability to integrate with other systems (such as Microsoft Entra ID, Microsoft Entra Federation Services, SharePoint, Microsoft Dynamics CRM, and Salesforce).

For details of the security-related administrative controls available in Viva Engage Enterprise, see the tables at the beginning of this article.

### Q: Does Viva Engage sell our data?

A: No. Viva Engage doesn't mine or sell any customer data. All data belongs to the customer (either the user or the organization, dependent on the Viva Engage version in use).

### Q: Can I export all my data?

A: In Viva Engage Enterprise, verified admins can export messages and uploaded files that are stored in Viva Engage, along with their metadata. The data export can also include any content that has been deleted, if the **Archive** data retention option has been configured.

Viva Engage files that are stored in SharePoint must be exported by using Microsoft 365 content search and export. Use [Content Search in Microsoft 365](/office365/securitycompliance/content-search) to find the files, and then [Export the Content Search Results](/office365/securitycompliance/export-search-results).

### Q: What are Viva Engage's business continuity features?

A: Your data is backed up multiple times a day and protected with strong encryption on disk. Backups are transferred off-site over SSH and properly deleted after six months.

### Q: Is Viva Engage covered under the materials in the Microsoft 365 Trust Center?

A: Yes it is. See [Microsoft 365 Trust Center](https://go.microsoft.com/fwlink/?LinkID=715692).

### Q: Is Viva Engage security independently verified?

A: Yes. [ISO27001](https://www.iso.org/standard/27001) is the global standard in information security. Independent auditors have verified that Viva Engage meets the rigorous set of physical, logical, process, and management controls defined by the ISO 27001 standard.

Viva Engage participates in the [Microsoft Online Services Bug Bounty](https://www.microsoft.com/msrc/bounty-online-services), which allows thousands of security researchers to test Viva Engage and help make our products even safer for users.

## User Management FAQs

#### Can I enforce multifactor authentication?

For Viva Engage Enterprise, if you enforce Microsoft 365 identity in Viva Engage. For more information, see [Set up multi-factor authentication for Microsoft 365 users](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6) and [Enforce Microsoft 365 identity for Viva Engage users](../configure-your-viva-engage-network/enforce-office-365-identity.md).

#### How do I manage Viva Engage on mobile devices?

Viva Engage is available for major mobile platforms, including the iPhone, iPad, and Android. Users can install the Viva Engage application from their respective app store.

Viva Engage Enterprise offers session management capabilities so that a user or administrator can end any Viva Engage session on any device if needed.

Viva Engage Enterprise devices can be managed with Microsoft Intune. For more information, see [Manage Viva Engage with Microsoft Intune](manage-viva-engage-with-intune.md).

#### How can I manage my users?

Only users with a valid and verified company email address can join your Viva Engage network.

In a Viva Engage Basic network, users can invite their colleagues with the same email address suffix to collaborate. Users can also suspend other users from having access to the Viva Engage network.

In Viva Engage Enterprise, administrators can provision and remove users in bulk using a CSV file and also to synchronize with Microsoft Entra ID to automatically add users who aren't already on Viva Engage and remove users from Viva Engage if their Microsoft Entra ID account is disabled or deleted.

#### How can users without email addresses access Viva Engage?

Viva Engage works with many large organizations where it's important to hear the voice of all workers, including those without email addresses. In this case, Viva Engage can grant these users access based on a unique identifier.
