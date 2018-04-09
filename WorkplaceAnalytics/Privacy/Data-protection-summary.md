---
# Metadata Sample
# required metadata

title: Data-protection considerations when using Workplace Analytics (short) 
description: Data-protection considerations (GDPR) summary -- shortened version
author: paul9955
ms.author: v-pascha
ms.date: 04/04/2018
ms.topic: get-started-article
ms.prod: wpa
---

# Data-protection considerations when using Workplace Analytics 

Workplace Analytics and data protection in your organization
Microsoft Workplace Analytics produces powerful insights about how your organization functions. It does this by analyzing email and meeting data from Office 365 and organizational data that you provide. 

Individuals have every right to be concerned about how their data is used. Those who control and process this data have a serious responsibility to understand how it is analyzed and stored and to carefully consider and plan how to protect it.  

## Roles and responsibilities

Regardless of where your organization is located, the concepts of data controller, data processor, and data subject provide a useful framework for thinking about data protection when using Workplace Analytics.

 * **Your organization’s role -- Data controller:** The data controller is a party that determines the purposes and means of processing a data subject’s personal data. When using Workplace Analytics, your organization is the data controller because your organization determines if, how, and why Workplace Analytics will process any personal data.
 * **Microsoft’s role -- Data processor:** The data processor is a party that processes personal data on behalf of the data controller. When your organization uses Workplace Analytics, Microsoft is the data processor. 
 * **Data subject and personal data:** A data subject is a person who can be identified through personal data. In the context of Workplace Analytics, the data subject is an employee or other user in your organization whose personal information is being processed. Personal data is any information that directly or indirectly identifies a person (the data subject).

## Data-privacy recommendations

Consider implementing the following data-privacy recommendations before you begin using Workplace Analytics.

## Develop a clear analysis plan

You must understand clearly what you want to analyze and why. After you determine what specific questions about your organization you want to answer, consider how Workplace Analytics might help you find those answers.

## Consider a data protection impact assessment (DPIA)

If your proposed use of Workplace Analytics involves processing personal data in a way that could lead to high risks to the rights of employees and other users in your organization, completing a DPIA might be warranted. If you are unsure whether a DPIA is required, consult your organization’s privacy subject matter experts, such as legal or HR personnel. For more help in deciding whether you need a DPIA, see DPIA – What it is, when is it needed, and why. 

Use aggregated or anonymized data whenever possible
To minimize privacy risk, use the minimum data necessary to conduct your research. While adopting a strict policy of never using personal data and minimizing use of pseudonymized data in combination with identifying attributes can help address many of the risks inherent in using such data, such a policy can restrict the types of analyses that Workplace Analytics can perform. It is up to your organization to decide the best approach and policy for your organization.

## Use and visibility of data

You have full control over what data to include in analysis using Workplace Analytics. The primary data source is collaboration data from Office 365. This is supplemented by human resources or other organizational data that you want to include so that you can group information by job title, location, or other attributes.

## Data provided by Microsoft Office 365

Workplace Analytics uses header information from Office 365 emails and calendar items. This header information includes sender and recipient, date and subject lines for emails, and organizer, attendee, duration, and location for meetings.

## Privacy capabilities in your control

First, you get to decide which users’ mailboxes to include in your Workplace Analytics study. Then, there are multiple controls you can use to further limit the data. 

Workplace Analytics support for handling data subject requests
Under the GDPR, data subjects may have rights to request exclusion from processing, access, correction, or deletion of their personal data. It is your organization’s role as data controller to evaluate whether a particular data subject request is valid and, if appropriate, to take action to fulfill the request. 

 * **Exclusion from processing:** Data subjects have the right to have their personal information excluded from processing.
 * **Access:** Data subjects have the right to demand what personal information is being processed, and Workplace Analytics gives you the ability to export the raw data, which may contain personal data.
 * **Correction:** Data subjects have the right to rectify their personal data. Workplace Analytics only performs operations (mostly arithmetic) on data provided to it from other sources, such as email and meeting data from Office 365 or the organizational data that you upload. This data is not corrected through Workplace Analytics.
 * **Deletion:** Data subjects can ask for their personal data to be erased. If a user wishes to have their data removed from a study after the study is completed, then you can expunge that user’s personal data from the raw datasets that were previously processed.
 * **Transparency regarding processing:** This document goes over in detail the metrics calculated by Workplace Analytics, and what they mean.  



