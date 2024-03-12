---
ms.date: 11/14/2022
title: Security, privacy, and compliance in Viva Goals
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager: Liz.Pierce
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals
- highpri
- essentials-privacy
- essentials-security
- essentials-compliance
search.appverid:
- MET150
description: "Learn about Viva Goals security, privacy, and compliance."
---

# Security, privacy, and compliance in Viva Goals

Security, Privacy, and Compliance are core tenets of how we serve our customers and how we empower organizations to serve their customers. This article presents the Security, Privacy, and Compliance questions customers have shared which relate to how Microsoft Viva Goals handles data that they share and store in the Microsoft Cloud.  

This document is not intended to provide legal advice and should not be relied upon to assess your legal rights, obligations, or risks.

## Overview

The Viva Goals service is governed by the [Microsoft Product Terms](https://www.microsoft.com/licensing/terms), and the [Microsoft Privacy Statement](https://www.microsoft.com/privacystatement/OnlineServices/Default.aspx). For the obligations related to processing and security of Customer Data and Personal Data, see the [Data Protection Addendum](https://www.microsoft.com/licensing/docs/view/Microsoft-Products-and-Services-Data-Protection-Addendum-DPA). For compliance information, the [Microsoft Trust Center](https://www.microsoft.com/trustcenter) is the primary resource for Viva Goals.

The Microsoft Product Terms outline a shared responsibility model between Microsoft and its customers. Microsoft works to ensure that we are compliant with industry and international standards, and customers are responsible for ensuring their data within the [Microsoft Cloud](https://www.microsoft.com/microsoft-cloud#What-is-the-Microsoft-Cloud) is protected in a manner that is compliant with the standards and regulations imposed on the customer. Microsoft is responsible for maintaining the implementation and test information associated with Microsoft Managed Controls. Customers are responsible for maintaining the implementation and test information associated with Customer Managed Controls. The Microsoft Product Terms binds us and our joint responsibilities.

:::image type="content" source="../media/goals/security-privacy/prod-preamble-online-service-terms-dpa.png" alt-text="Infographic showing Microsoft's online service terms and data protection agreement." lightbox="../media/goals/security-privacy/prod-preamble-online-service-terms-dpa.png":::

For information about policies, tools, and best practices for all of Office 365, see [Overview of security and compliance in Office 365](https://support.office.com/article/dcb83b2c-ac66-4ced-925d-50eb9698a0b2). Viva Goals documentation can be found at [Intro to Viva Goals](intro-to-ms-viva-goals.md)

## Introduction

Microsoft Viva Goals is a goal-alignment solution that connects teams to your organization’s strategic priorities, unites them around your mission and purpose, and drives business results. Because Viva Goals is a part of Microsoft Viva, it integrates into the employee experience, empowering teams to be their best from anywhere. Viva Goals supports integration with industry-leading tools and platforms you use every day, so you can automatically update OKRs when your work gets done and foster ongoing feedback on your goals.

:::image type="content" source="../media/goals/security-privacy/prod-introduction-viva.png" alt-text="Infographic of Viva Goals in the hierarchy of Viva." lightbox="../media/goals/security-privacy/prod-introduction-viva.png":::

## Viva Goals Security and Compliance

The Viva Goals service follows the Security Development Lifecycle (SDL), strict security practices that support security assurance and compliance requirements. The SDL helps developers build more secure software by reducing the number and severity of vulnerabilities in software, while reducing development costs. Learn more at [Microsoft Security Development Lifecycle Practices](https://www.microsoft.com/securityengineering/sdl/practices).

### Viva Goals Architecture

The Viva Goals architecture is a multi-tier application with front ends, a Web Application layer, Background job processing, Integration APIs, and Storage systems to name a few. Viva Goals is implemented as a multi-tenant architecture deployed in the M365 public cloud with Security, Scalability, Updatability, Operability, Compliance, Performance, Privacy, and Availability in mind.  

Viva Goals ensures high availability of dependent services through a fault-tolerant architecture. In addition, monitoring and Incident Response processes are set up to operate at a high availability. We maintain separate standby regions for Disaster Recovery to withstand regional failure.

Viva Goals is constantly modernizing the technical architecture to innovate and meet the growing needs of customers. However, we also strive to ensure that none of these changes impact new or existing customers. Changes will not require our customers to upgrade software/hardware.

:::image type="content" source="../media/goals/security-privacy/prod-architecture.png" alt-text="Infographic showing how data moves from the client to different data bases." lightbox="../media/goals/security-privacy/prod-architecture.png":::

Users can use the Web Client or Teams app to connect to and use Viva Goals. HTTPS requests go through Azure Front Door, which acts as the single point of entry for all web requests to the Viva Goals application. Azure Front Door is used for its Web Application Firewall (WAF) as well as Content Delivery Network (CDN) capabilities for Viva Goals. The CDN is used to deliver static assets such as images, icons, JavaScript files, style sheets, etc. The requests received by Azure Front Door are routed to the API Management service and a load balancer. This service acts as the proxy between Azure Front Door and the Web Application layer, which resides within a private virtual network. Viva Goals also uses session-based rate limiting configured on the API management service to protect the service. The secrets required during the application lifecycle are stored in our service’s Azure Key Vault and are retrieved at runtime. Viva Goal’s primary data store is Azure PostgreSQL, but other compliant Azure data stores are also leveraged where necessary (see table below):

|Storage Service   |Usage  |
|---------|---------|
|Azure Cosmos DB for PostgreSQL      |The primary relational data store for user content like Objectives, Key Results, Projects, and others. Powered by the Citus open-source extension to PostgreSQL. Sharding solution layered on PostgreSQL for scale out.          |
|Azure Cosmos DB      |Cached, serialized view of content for fast reads.          |
|Azure Cognitive Search      |Search engine to enable user search of OKR content.          |
|Azure Synapse and Data Lake      |Used to power Insights dashboard within Viva Goals.          |
|Azure Cache for Redis      |Used to store asynchronous job information.          |
|Azure Blob Storage      |Blob storage for user’s profile pictures, file exports such as OKR reports, and others.           |

## FAQs (Frequently Asked Questions)

- [General questions](#general-questions)
- [Viva Goals Data Handling](#viva-goals-data-handling)
- [Viva Goals Data Residency](#viva-goals-data-residency)
- [Viva Goals Data Retention](#viva-goals-data-retention)
- [Viva Goals GDPR Requests](#viva-goals-gdpr-requests)
- [Copilot in Viva Goals](#copilot-in-viva-goals)

### General questions

#### Who can access the Viva Goals network?

Only users with a valid and verified company email address who are authorized through Microsoft Entra ID (either direct or federated) can access Viva Goals.

#### What endpoints need to be reachable for Viva Goals users?

For complete Office 365 URL and IP address ranges info, see [Microsoft 365 endpoints](/office365/enterprise/office-365-endpoints).

#### What is Viva Goals privacy policy? How do you treat my data?

Our privacy policy is publicly shared and available in the ‘Enterprise and developer products’ section of the [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?LinkID=331314).

#### What is Viva Goals’ security policy?

Viva Goals is included in the [Microsoft Trust Center](https://go.microsoft.com/fwlink/?linkid=2083681).

#### Is Viva Goals’ security independently verified?

Yes. As part of Office 365 practices, Viva Goals has undergone an independent Audit. For details, refer to "Microsoft 365 Microservices T1 - SSAE 18 SOC 2 Type 1 Report (2022)" available on the [Service Trust Portal](https://servicetrust.microsoft.com/).

#### What security procedures do you implement?

Viva Goals implements change management/change control process, Code deployment, patch management program including high-risk security patch application, and system hardening. <br></br> Viva Goals performs periodic Information Security Management System (ISMS) reviews and reviews results with management. This involves monitoring ongoing effectiveness and improvement of the ISMS control environment by reviewing security issues, audit results, and monitoring status, and by planning and tracking necessary corrective actions. <br></br> Standard Operating Procedures (SOPs), which define the procedures required to operate and maintain the Service environment have been established and communicated to employees. SOPs are reviewed and approved annually by appropriate management. <br></br> Administrative access to the Service environment is controlled through defined interfaces that require authentication and authorization using isolated identity. Privileges (i.e., reading and writing) are restricted to authorized personnel through designated channels based on job responsibilities. <br></br> Finally, a compliance program is managed with representation from various cross-functional teams and external parties to identify and manage compliance with relevant statutory, regulatory, and contractual requirements. We have a dedicated team that regularly monitors security risks and address them on a proactive basis.

#### What technical and organizational security measures do you implement?
Viva Goals follows Office 365 practices and implements several security measures such as User access control, Storage control, Transmission control, Input control, Recoverability, Data integrity, Availability control, and Separability. Additionally, automated, and internal trust audits evaluate the following checks and controls for each feature release:

- Classifying all new data and performing GDPR, DSR, with data retention checks.
- Automated internal data access controls and validates Azure component data flows.
- Encrypt data at rest and in transit.
- Check cookies, telemetry, and logs for sensitive data and consumer content.
- Automated scans for content security policy, vulnerability, and code/library scan.

#### What malware controls do you implement?

Viva Goals follows Office 365 practices and implements Antivirus checks for all the export and import processes in the application. In addition, all endpoint devices are centrally managed and malware controls are in place.

#### What vulnerability management procedures do you implement?

Viva Goals follows Office 365 practices and leverages yearly penetration tests, security testing (red team), assessments, security validation, and automated vulnerability scans. Auditing and logging are enabled and captured on systems and network devices with centralized logging solutions that correlate events and alerts for potential security incidents 24/7.

#### Can we get the security event logs? Can we audit all activities in Viva Goals?

Viva Goals does not send security event logs to a third-party Security Information and Event Management (SIEM) service. However, the Global admin can audit activities on Viva Goals by searching for Viva Goals activities in the audit section of the [Microsoft compliance portal](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fcompliance.microsoft.com%2F&data=05%7C01%7Csusbhatia%40microsoft.com%7Cfe608d17064441d9162308db152377d1%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C638127014381975186%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=3sf6iXmnIV1JUmfwymJOQkjWW%2BAUFBVxj58GX6e5w9k%3D&reserved=0). To learn more about how to search the audit log, see [Audit Log Search](/microsoft-365/compliance/audit-log-search). The list of user and admin activities in Viva Goals that are logged for auditing can be seen at [Viva Goals Activities](/microsoft-365/compliance/audit-log-activities?).  

#### How can Security incidents be reported?

Security incidents can be reported at https://www.microsoft.com/msrc.  

#### Is there an information security policy?

Yes. Please see [Microsoft Viva Security](../microsoft-viva-security.md).  

#### Where can I learn more about the Viva Goals settings?

Please see the following:

- For Admin content: [Intro to Microsoft Viva Goals](intro-to-ms-viva-goals.md)
- For User content: https://support.microsoft.com/office/introducing-microsoft-viva-goals-bd651be7-472a-4f40-8fdd-6fcead79f3ad

#### How does Viva Goals protect the service from the internet?

Viva Goals uses Azure Front Door to provide necessary Firewall controls and WAF (Web Application Firewall) capabilities. Viva Goals also uses Endpoint protection services managed by Microsoft Entra ID. [A conditional access policy](/azure/active-directory/conditional-access/overview) with Just-In-Time elevated access is used to manage write access to Azure portal which manages the production subscription(s).

#### What Authentication/Authorization mechanism is used by Viva Goals?

Viva Goals uses Role Based Access Control (RBAC) through Microsoft Entra ID and application specific roles. Each role has specific read, write, and administrative access. To learn more about Roles and Permissions, see [Roles and Permissions in Viva Goals](roles-permissions-in-viva-goals.md).

#### What Authentication/Authorization mechanism is used for data integrations with Viva Goals?

Data integrations in Viva Goals enable you to create connections with data sources that will automatically update key results and projects, enabling you to have a single source of truth for progress. Viva Goals uses oAuth 2.0-based authentication when available, otherwise user’s API token or username/password is used to connect to the data integration service. Credentials provided such as username/password or OAuth tokens are encrypted and stored in the database. The keys to encrypt (unique to an organization) are in turn encrypted and stored in the database using Key Encryption Key (KEK) that resides in Azure managed HSM Key vault. Viva Goals utilizes public APIs to retrieve data from third-party integrations. Viva Goals does not share data from your tenant with third parties to support data integrations by default. To learn more about setting up integrations, see [Integrations Administration Overview](vg-integrations-administration-overview.md).

#### Can I configure multifactor authentication (MFA) with Viva Goals?

Yes. MFA can be configured using Microsoft Entra ID. To learn more about MFA with Microsoft Entra ID, see [Microsoft Entra multifactor authentication](/azure/active-directory/authentication/concept-mfa-howitworks).

### Viva Goals Data Handling

#### Is Data at rest encrypted?

Yes. The Azure Cosmos DB for PostgreSQL service uses the FIPS 140-2 validated cryptographic module for storage encryption of data at-rest. Data, including backups, are encrypted on disk, including the temporary files created while running queries. The service uses the AES 256-bit cipher included in Azure storage encryption, and the keys are system-managed. Storage encryption is always on and cannot be disabled. Data persisted in other data stores is encrypted by default with AES 256-bit key encryption using Microsoft managed keys. In addition, we use other data stores provided by Azure and secured with Microsoft and O365 practices. All the data is stored within a private virtual network and does not leave Microsoft's trust boundary.

#### Is Data in transit encrypted?

Yes. Viva Goals requires all incoming HTTP traffic to be encrypted using TLS 1.2 or above. Any requests attempting to use the service with TLS 1.1 or lower will be rejected.

#### Who has access to the data?

Only employees with a legitimate business need can access customer data, and all access is on an approval‐only basis. All access is logged and regularly audited.

#### Do you have a Data Protection Officer?

Yes. DPO can be reached via https://www.microsoft.com/concern/privacy.  

#### Can we perform an on‐site visit or audit of your facilities?

Viva Goals doesn't permit customers to perform on‐site audits as they pose a risk to the security of the service. We will answer any security questions openly and transparently.

#### Do you conduct third‐party penetration testing?

Penetration tests of the Viva Goals infrastructure are conducted yearly as part of Office 365 practices.

#### Do you comply with the data protection act in my country?

As the data controller, it is your responsibility to ensure you comply with the data protection regulation that applies to you. However, Viva Goals has controls in place to help you meet your regulatory obligations. You must independently assess your regulatory obligations and ensure your use and configuration of Viva Goals meets them.

#### How is data separated from other tenants?

Viva Goals implements a multi-tenant model. As such, customers' data is logically separated with strict controls to ensure separation of tenant data. The web application servers of Viva Goals are physically and logically separated from servers that store customer data.

#### Does Viva Goals sell our data?

No. Viva Goals does not mine or sell any customer data. All data belongs to the customer.

#### Can I export all my data?

In Viva Goals, Organization Admins can designate Admins, Team Admins, or a set of specific users who are allowed to export OKR related data, along with their metadata.

#### What are Viva Goals’ business continuity features / data recovery?

Your data is backed up multiple times a day, stored in Azure storage, and protected with strong encryption at rest. Additionally, data is continually replicated in Azure regions separate to the primary region to withstand region outages. Viva Goals runs periodic disaster recovery drills to test recoverability of data and dependent services upon failure.

#### How is data managed through Viva Goals’ integrations?

There is over forty-five different 1P and 3P integrations, most of which focus on pulling data from external services into Viva Goals. Data integrations (that automatically update OKRs when your work gets done) pull data from external systems into Viva Goals (one-way sync). Integration such as Slack/Teams uses a bi-directional sync and enable Viva Goals to be in the flow of work of the user (two-way sync). <br></br> The Integration authentication mechanism is oAuth2-based when available; otherwise, a user’s API token or username/password is utilized to connect to other services. Credentials provided, such as username/password or OAuth tokens, are encrypted and stored in the database. The keys to encrypt are unique to an org and are in turn encrypted and stored in the database using Key Encryption Key (KEK) that resides in Azure managed HSM Key vault.

#### What kind of personal data do you process?

Viva Goals abides by the Microsoft Trust policies and procedures to minimize the use of personal data for any processing activity. Viva Goals only consumes personal data from Microsoft Entra ID. Additionally, customer content related to 3P integrations will be captured and processed (all such data is encrypted and stored in our database). The following are examples of personal information required by Viva Goals for application-specific purposes: Name, Addresses, Job Title, Department, City Country, User Type, Preferred Language, Profile Photo, Manager. In addition to this, some third-party integrations may push fields (e.g., Employee cost center, Department/Team/Organization) with the consent of customers.

#### Who has access to personal data?

Microsoft personnel have no standing access to customer data. Access to such data is safeguarded by controls including approval workflows only when required to support the customer. IT admin can reach out to Microsoft support through Admin centers to raise queries for their personal data. Please refer to “how to contact us” section in Privacy statement [here](https://privacy.microsoft.com/privacystatement#mainnoticetoendusersmodule).

#### How long will personal data be retained before being erased?

When a tenant subscription to Viva Goals is canceled, the personal data along with other data is retained for a minimum of 90 days and purged within180 days from the date of cancellation.

#### Does Viva Goals use web cookies? If so, how long is the data stored?

Yes. See the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement#maincookiessimilartechnologiesmodule) for more about cookies.

#### How do you ensure that sub-processors meet data handling standards?

See the [Subprocessors and Data Privacy article](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fwww.microsoft.com%2Fen-us%2Ftrust-center%2Fprivacy%2Fdata-access%23howdoesmicrosofthandleyourdatainthecloud&data=05%7C01%7Crasanders%40microsoft.com%7Cf43d2000d60f44fd36ba08db34619004%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C638161365867484615%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=%2FNDeHFZP%2FHJZKslHI%2FluJIn5PzJKWQKghZAv%2BFsFzTI%3D&reserved=0) for how Microsoft handles your data.

### Viva Goals Data Residency

#### Where is the data hosted?

Viva Goals data is hosted in Microsoft-managed datacenters. See [Where your Microsoft 365 customer data is stored](/microsoft-365/enterprise/o365-data-locations) to find the datacenters for the country in which your company is located. Viva Goals operates out of Microsoft's global network of datacenters. These centers have 24/7/365 video surveillance, biometric and pin-based locks, strict personnel access controls and detailed visitor-entry logs.

#### Can we control where data gets stored?

No. This capability is not provided currently. See [Where your Microsoft 365 customer data is stored](/microsoft-365/enterprise/o365-data-locations) to learn more about how data is stored and in which datacenters.

#### Does Viva Goals offer local data residency?

No. Local data residency within a country is not available currently.

### Viva Goals Data Retention

#### How long is my data kept for? How is it deleted?

Viva Goals keeps your data in line with Microsoft’s contractual commitments. At all times during the term of Customer’s subscription, the customer will have the ability to access, extract and delete Customer Data stored in each Online Service. Microsoft will retain Customer Data that remains stored in Online Services in a limited function account for 90 days after expiration or termination of Customer’s subscription so that Customer may extract the data. After the 90-day retention period ends, Microsoft will disable the Customer’s account and delete the Customer Data and Personal Data within an additional 90 days in accordance with [Microsoft 365 Data Handling Standard](/office365/Enterprise/office-365-data-retention-deletion-and-destruction-overview). To learn more, see https://www.microsoft.com/licensing/docs/view/Microsoft-Products-and-Services-Data-Protection-Addendum-DPA.

#### What is the data retention after a license is removed?

If the Viva Goals license is removed from a user, Viva Goals retains that user's data that was collected during the period the license was assigned. Admins can continue to query the collaboration activity that this user participated in before they left. The person's collaboration data stays with the tenant and will be deleted according to the overall tenant retention policy in accordance with [Microsoft 365 Data Handling Standard](/office365/Enterprise/office-365-data-retention-deletion-and-destruction-overview).

### Viva Goals GDPR Requests

#### Does Microsoft make commitments to its customers with regard to the General Data Protection Regulation (GDPR)?

Yes. The GDPR requires controllers (such as organizations using Microsoft's enterprise online services) only use processors (such as Microsoft) that provide sufficient guarantees to meet key requirements of the GDPR. Microsoft has taken the proactive step of providing these commitments to all Volume Licensing customers as part of their agreements. <br></br> Microsoft provides tools and documentation to support your GDPR accountability. This includes support for Data Subject Rights (DSRs), performing your own Data Protection Impact Assessments, and working together to resolve personal data breaches. <br></br> Viva Goals supports the GDPR-compliancy data deletion/retention and DSR practices (subjects’ right to access, delete, edit, export, restrict, or object to processing of the Personal Data of that Data Subject). To learn more about GDPR compliance at Microsoft, see [General Data Protection Regulation Summary](/compliance/regulatory/gdpr).

#### Does Microsoft have a Chief Privacy Officer?

Yes. The office of the privacy officer is involved in the impact assessment for all Microsoft products. To meet GDPR requirements, Microsoft also has designated a European Union Data Protection Officer (DPO) to be an independent advisor for Microsoft's engineering and business groups and to help ensure that all proposed processing of personal data meets EU legal requirements and Microsoft's corporate standards. The role was designed to meet the GDPR criteria set out in Articles 37-39. To learn more, see [Microsoft's data protection officer](/compliance/regulatory/gdpr-data-protection-officer).  

#### How does Microsoft handle security breaches?

As a data processor, Microsoft will ensure that our customers can meet the GDPR's breach notification requirements as data controllers. To learn more, see [GDPR Breach Notification](/compliance/regulatory/ccpa-faq).

#### Can Viva Goals help me be compliant with the California Customer Privacy Act (CCPA)?

Microsoft has implemented GDPR-related DSR capabilities globally. Microsoft has also reviewed our third-party data sharing agreements and taken steps to establish that the necessary contractual terms are in place to ensure that we do not "sell" personal information. To learn more, see [California Consumer Privacy Act (CCPA) Frequently Asked Questions](/compliance/regulatory/ccpa-faq).

### Copilot in Viva Goals

#### Does Copilot in Viva Goals use customer data to train its model?

No. Copilot in Viva Goals uses a foundational model, operating through prompts based on sample Viva Goals data and common instructions. Prompts, responses, and data accessed through Copilot in Viva Goals aren't used to train LLMs.

#### How does Copilot in Viva Goals use my organizational data?

Copilot in Viva Goals provides value by connecting LLMs to your organizational data, which includes content and context accessed through Microsoft Graph. It can generate responses based on organizational data like user strategy documents, goals, and check-ins. Copilot in Viva Goals combines this content with the user’s working context, time period, and teams to help provide accurate, relevant, and contextual responses.

Copilot in Viva Goals can access organizational goals data that individual users have permission to view. It's important that you're using the permission models available in Microsoft 365 services, such as SharePoint, to help ensure the right users and groups have the right access to the right goals within your organization. This includes permissions you give to users outside your organization through inter-tenant collaboration solutions, like shared channels in Microsoft Teams.

When you enter prompts using Microsoft Copilot in Viva Goals, the information contained within your prompts, the data retrieved when responding to the prompts, and the responses generated to the prompts all remain within the Microsoft 365 service boundary.

#### What privacy policy does Copilot in Viva Goals use?

Our privacy policy is publicly shared and available as part of the [Microsoft Privacy Statement](https://privacy.microsoft.com/en-us/privacystatement). Copilot in Viva Goals follows the [privacy and data compliance](#security-privacy-and-compliance-in-viva-goals) currently in place for Viva Goals.

## Further reading

- [Introduction to Microsoft Viva Goals](intro-to-ms-viva-goals.md)

- [Overview of security and compliance in Microsoft Viva](../microsoft-viva-security.md)

- [Employee Privacy and Data Protection](https://www.microsoft.com/microsoft-viva/privacy)

- [Microsoft Compliance](/compliance/)

- [Microsoft 365 roadmap](https://aka.ms/m365roadmap)
