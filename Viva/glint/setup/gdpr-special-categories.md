---
title: Advanced privacy guide for data usage and survey item creation
description: At Microsoft Viva Glint, data privacy and trust are key priorities to encourage elevated levels of honest and useful feedback. 
ms.author: SarahBerg
author: SarahAnneBerg
manager: elizapo
audience: admin
f1.keywords: NOCSH
keywords: Confidentiality, personal data, data privacy, privacy, trust, sensitive data, GDPR 
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/10/2023
---

# Advanced privacy guide for data usage and survey item creation

Microsoft Viva Glint helps organizations measure employee engagement and experiences so they can take action to improve them. Grounded in our approach to employee [engagement](https://aka.ms/VivaGlintAModernApproach), Viva Glint offers a flexible surveying approach that enables organizations to gain a greater understanding of key experiences that shape an employee's journey, how those experiences impact engagement, and the resulting impact on individual and business outcomes.

With Viva Glint, organizations capture invaluable employee feedback and transform those insights into actions. Feedback and action-taking are brought directly into the flow of work, empowering managers and their teams to take joint ownership and drive meaningful actions and habits that support happiness, success, and wellbeing at work.

This resource explains how Viva Glint provides the customer admin with controls to manage personal data and implements protections within Viva Glint to maintain employee privacy. These controls and protections support customer compliance with regulations such as the [European Union General Data Protection Regulation (GDPR)](/viva/glint/setup/gdpr-special-categories). This document is specific to Viva Glint and provides a technical overview of how data and privacy are protected.

## Understand the fundamentals of Viva Glint privacy

This section discusses concepts that provide a framework for understanding how Viva Glint approaches data protection.

### Data entity

Contemporary privacy regulations, such as the GDPR, outline roles and responsibilities in thinking about data protection and privacy. These concepts help illustrate the respective responsibilities of the customer, Microsoft, and employees when it comes to processing and managing sensitive data.

The concepts of data controller, data processor, and data subject originate in European privacy law. Regardless of where your organization is located or whether any personal data of European Union citizens is involved, these concepts provide a useful framework for thinking about data protection when using Viva Glint.

The following illustration shows the central position of the data controller (your organization) between the data subject (left) and the data processor, Microsoft (on the right):

:::image type="content" source="../../media/glint/start/data-entity.png" alt-text="Screenshot that displays the data entity of Viva Glint.":::

### Data controller

The data controller is a party that determines the purposes and means of processing a data subject's personal data.

When using Viva Glint, your organization is the data controller because your organization determines if, how, and why Viva Glint processes any personal data.

As the data controller, your organization:

- Determined the scope of data to analyze and the purpose and objectives of the analysis.
- Works with your organization's legal, privacy, and human resources teams for the following tasks:
  - Determining whether you should obtain consent from users in your organization.
  - Determining what information is provided to users about how your organization processes their personal data in Viva Glint.
  - Accounting for local considerations (for example, obtaining approval from local works councils, if applicable).
- Uses Viva Glint privacy controls to direct what data will be analyzed, how data will appear in results, and who will have access to both raw data and the results of analysis.
- Reviews and is familiar with this document and other Viva Glint privacy documentation provided by Microsoft.

### Data processor

The data processor is a party that processes personal data on behalf of the data controller. When your organization uses Viva Glint, Microsoft is the data processor.

As a data processor, Microsoft will:

- Process personal data in accordance with your organization's instructions as directed through your settings configuration within Viva Glint
- Through your use of Viva Glint, process all data provided to Microsoft (including personal data) according to the same general privacy and security terms in the [Product Terms](https://www.microsoft.com/licensing/terms/product/PrivacyandSecurityTerms/all)
- As part of Microsoft's commitments under Product Terms and Microsoft Products and Services [Data Protection Addendum](https://www.microsoft.com/licensing/docs/view/Microsoft-Products-and-Services-Data-Protection-Addendum-DPA) (DPA), abide by the Standard Contractual Clauses and remain certified under the EU-U.S. and Swiss-U.S. Privacy Shield Frameworks and the commitments that these frameworks entail legitimizing transfers of personal data from the EU and Switzerland to the U.S, though Microsoft doesn't rely on the EU-U.S. Privacy Shield Framework as a legal basis for transfers of personal data in light of the judgment of the Court of Justice of the EU in Case C-311/18
- Contractually commit to abide by applicable provisions of applicable regulations such as the GDPR or California Privacy Rights Act (CPRA).
- Provide Viva Glint features that help organizations meet their data controller obligations and honor data subject rights under the GDPR, including the rights of exclusion from processing, access, erasure, and transparency regarding methods of processing
- Implement technical and organizational security measures to protect the confidentiality of your organization's (and employees') data in Viva Glint

In addition, Microsoft doesn't use customer data or personal data for advertising, nor does it volunteer to provide such data to law enforcement.

### Data subject

A data subject is a person who can be identified through personal data. In the context of Viva Glint, the data subject is an employee or other user in your organization whose personal information is being processed. Personal data is any information that directly or indirectly identifies a person (the data subject).

> [!NOTE]
> In most cases in the Viva Glint product and documentation, we refer to a Data Subject simply as a "user," a "person," an "individual," or an "employee."

## Understand which data gets processed

Viva Glint provides the customer with tools to manage the data Viva Glint processes and who has access to that data. Viva Glint also gives customers the ability to receive and respond to [Data Subject Rights](https://www.microsoft.com/en-ww/trust-center/privacy/gdpr-dsr?market=af) requests from employees. Customers control what employee personal data they import to Viva Glint. Viva Glint can then combine this customer-imported data with survey responses to provide extra insights. GDPR "sensitive data" has specific considerations that customers should assess in coordination with their HR, privacy, and legal teams.

> [!TIP]
> Customers should upload the minimum and least sensitive data necessary to achieve their goals. It is the customer's responsibility to assess their privacy and compliance obligations and to determine whether Viva Glint is suitable.

## Manage who has access to survey feedback

The customer admin can assign user roles with varying levels of access to view survey feedback results. The admin also controls who can see the data and at what level of detail.

Viva Glint reporting, like other products that work with sensitive data (for example, HR systems), isn't meant for the general workforce. Rather, its users are expected to have training in how to handle sensitive information. Topics might include your organization's HR policies, your organization's employee privacy policy and how to handle and store sensitive data.

Viva Glint Customer Admins may create the following types of user roles within their organization:

- Managers: These users might need to see the rollup for their teams and perhaps, one attribute. They often don't have the team size to see results by demographic analysis and lack the authority to act on them.

- Senior managers: Due to their organizations' size, they might need to see data for various cohorts. They might need to see organizational demographics such as location, tenure, and job family as those are areas within their authority to act. Special category data, such as ethnicity, is often not provided to these users.
- Human Resources Business Partners (HRBPs) with the ability to see divisions or even organization-wide, and the internal ability to see employee-level data. These users might need access to all attributes.

[Read about why Viva Glint collects employee attributes and how they're used in reporting.](https://go.microsoft.com/fwlink/?linkid=2230738)

## Privacy and legal subject matter experts might be required

Some countries require employers to consult with employee representatives or seek approval from a works council before deploying certain information technology services in the workplace.

## Additional resources

- [Privacy policy requirement of every Microsoft Viva Glint program](https://go.microsoft.com/fwlink/?linkid=2238336)
- [How Viva Glint helps protect confidentiality and privacy](https://go.microsoft.com/fwlink/?linkid=2238614) 
- [Raw data requests and handling](https://go.microsoft.com/fwlink/?linkid=2230875) 
- [Why surveys are confidential rather than anonymous](https://go.microsoft.com/fwlink/?linkid=2238615)
