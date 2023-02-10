---
title: "Overview and setup of Answers in Viva"
description: "Viva Engage is a new employee experience that connects people across the company—wherever and whenever they work—so that everyone is included and engaged."
ms.reviewer: ethli
ms.author: mamiejohnson
author: mamiepjohnson
manager: dmillerdyson
ms.date: 2/15/2023
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
localization_priority: Priority
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Overview and setup of Answers in Viva

Accessible through the **Answers** tab in the Viva Engage Teams app, **Answers in Microsoft Viva** is a new experience for people in large organizations to learn from each other by asking and answering questions. Answers is a conversational experience for asking questions and connecting employees to crowdsourced answers. Natural language processing helps match questions with any existing answers, and the experience rewards people who contribute back to Answers.

Answers works to connect employees based on their subject matter expertise captured in Viva Topics, to get their questions answered, connect with subject matter experts, and increase their learning.

## Licensing
If Answers is enabled in the Viva Engage admin center, users assigned the Viva Engage Knowledge service plan can use the full Answers experience in the Viva Engage Teams app, including rewards and recognition. The Viva Engage Knowledge service plan is available as part of the *Microsoft Viva Suite or Viva Topics SKUs.*

Users who haven't been assigned the Viva Engage Knowledge service plan will receive notifications to questions or answers they've been mentioned in and can visit those threads but won't be able to navigate to the rest of the Answers experience.

> [!NOTE]
> As a prerequisite, the tenant must have Yammer enabled and the user must have access to Yammer services.

## Technical requirements

Answers will be enabled by default for customers that meet the following technical requirements:

1) **Migrate the Yammer network to Native Mode**

    [Native Mode](/yammer/configure-your-yammer-network/overview-native-mode) is a state of a Yammer network where all users are in Azure AD, all communities are Microsoft 365 groups, and all files are stored in SharePoint Online. This ensures that we can appropriately apply topic permissions and management. Access the [guide to migrate](/yammer/configure-your-yammer-network/native-mode-step-by-step-guide) the network to Native Mode.

2) **Migrate Yammer Topics to Viva Topics**

    Yammer topics have begun to migrate to Viva Topics. Over the next months, all existing Yammer networks will have migrated. Answers uses Viva Topics to organize question posts and identify the people associated with certain Topics to help route the questions posted. Since Viva Topics work across services in Microsoft 365, we require that your Yammer network is using Viva Topics to ensure the best experience with Answers.

    All Yammers tenants in Native mode will be migrated to use Viva Topics and there are no additional licensing requirements for this migration.

    For customers awaiting topics migration:  
    - Microsoft will inform existing Yammer customers with purchased Viva Topics or Viva Suite SKUs when Yammer Topics have been migrated to Viva Topics. Customers will be notified through email when the migration is complete.
    - Interested tenants can request prioritizing Answers enablement (may include Native Mode Support or Yammer Topics Migration to Viva Topics) by working with their customer account managers / Microsoft support staff for Yammer and filing a support ticket. Microsoft will review these requests and accordingly prioritize the Answers enablement for the tenants requesting them.

    Learn more about Yammer Topics migration to Viva Topics:
    - [Viva Topics in Yammer](/viva/topics/topic-experiences-yammer)
    - [Viva Topics experience in Yammer](https://support.microsoft.com/topic/viva-topics-experience-in-yammer-8e85bc0d-086e-49a2-974b-39f60129257d)

3. **Set up the Viva Engage app**

    Installing the Viva Engage app in Teams will provide the best experience for Answers. We recommend all organizations that would like to use Answers install the Viva Engage app. Follow these [steps to setup Viva Engage app](/viva/engage/setup).

## Data storage, export, and compliance

Answers is backed by an Office 365 group and will follow the default data [retention policies](/microsoft-365/compliance/retention-policies-yammer?view=o365-worldwide) set by your organization, unless a unique policy is set for Answers. The Answers backing group will be auto-provisioned when the first question is posted or first question attachment is created. At the time of creation, all Global admins will be assigned as owners of the backing group, titled **Group for Answers in Viva Engage – DO NOT DELETE.**

Owners of the backing group should ensure Answers maintains compliance with your network policies and does not get accidentally deleted. Data can be exported by admins if deleting the backing Office 365 group is desired. If the backing group is deleted, Answers will not be functional.

>[!NOTE]
> A soft delete can be recoverable if remediated within 30 days but a hard delete will result in *permanent* loss of data.

Answers data will be available in [eDiscovery](/yammer/manage-security-and-compliance/overview-of-ediscovery) for identifying and delivering electronic information that can be used as evidence in legal cases.  

**GDPR information**

For GDPR user data export, verified Yammer admins and Engage admins can follow the [Yammer GDPR export guidance](/yammer/manage-security-and-compliance/export-yammer-enterprise-data). Answers data will be bundled together with Yammer data. Erase all information about a Yammer user to comply with GDPR data subject requests. Learn [how to manage GDPR data subject requests in Yammer Enterprise](/yammer/manage-security-and-compliance/gdpr-requests-in-yammer-enterprise).

## Enable Answers  

Answers will be enabled by default and visible to all users that have the Viva Engage Knowledge service plan assigned. Answers can be disabled and hidden from the Viva Engage Teams app. When disabled, Answers content can still be accessed through existing links, but users will not be able to contribute to the thread or navigate the Answers experience.  

Only an Microsoft 365 Global admin can change Answers state of enablement:

1. As a Global admin, navigate to the Viva Engage Teams app.  
2. Select the ellipses button from the top right navigation bar to expose admin options.  
3. Select **Admin** to navigate to the Engage admin center.

![Image of the admin entrypoint into the Engage admin center.](/Viva/media/engage/admin/admin-entrypoint.png)

4. Select the **Answers** button within the **Feature management** tab to open Answers configuration options.

![Image of the admin entrypoint into Answers feature management in the Engage admin center.](/Viva/media/engage/admin/answers-eac.png)

5. In Answers feature management, you can enable or disable Answers for your organization. Answers will be on by default for all Viva suite and Viva Topics licensed users.  

![Image of the Answers enablement toggle in the Engage admin center.](/Viva/media/engage/admin/enable-answers.png)

>[!NOTE]
> If Answers is disabled, the backing group will respect the default data [retention policies](/microsoft-365/compliance/retention-policies-yammer?view=o365-worldwide) set by your organization, unless a unique policy is set for Answers.

## See also

[Answers admin scenarios in Viva](/Viva/engage/eac-answers-admin-scenarios)

[Answers in Viva: Frequently asked questions (FAQ)](/Viva/engage/eac-answers-faq)

[Key admin roles and permissions in Viva Engage](/viva/engage/eac-key-admin-roles-permissions)