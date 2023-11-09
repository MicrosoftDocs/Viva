---
title: "Overview and setup of Answers in Viva"
description: "Overview and setup of Answers in Viva, including licensing, technical requirements, and data management."
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: dmillerdyson
ms.date: 07/18/2023
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

**Answers in Microsoft Viva** is a new experience for people in large organizations to learn from each other by asking and answering questions. Access is through the **Answers** tab in the Viva Engage Teams app.

Answers let employees ask questions and connect to crowdsourced answers. Natural language processing helps match questions with available answers, and the experience rewards people who contribute to Answers.

Answers work to connect employees based on their subject matter expertise captured in Viva Topics. It helps users get their questions answered, connect with subject matter experts, and increase their learning.

## Licensing
When you enable Answers in the Viva Engage admin center, users who are assigned the Viva Engage Knowledge service plan can use the full Answers experience in the Viva Engage Teams app, including rewards and recognition. The Viva Engage Knowledge service plan is available as part of the *Microsoft Viva Suite* and *Viva Topics* products.

Users who aren't assigned the Viva Engage Knowledge service plan receive notifications to questions or answers where they're mentioned and can visit those threads. But they can't navigate the rest of the Answers experience.

> [!NOTE]
> As a prerequisite, the tenant must have Viva Engage enabled, and the user must have access to Viva Engage services.

## Technical requirements

By default, the Answers experience is enabled for customers that meet the following technical requirements:

1) **Migrated the Viva Engage network to Native Mode**

    [Native Mode](overview-native-mode.md) is a state of a Viva Engage network where all users are in Microsoft Entra ID. All communities are Microsoft 365 groups, and all files are stored in SharePoint Online. This setup ensures that the service can appropriately apply topic permissions and management. For more information, see the [guide to migrate](native-mode-guide.md) the network to Native Mode.

2) **Migrated Viva Engage Topics to Viva Topics**

    Viva Engage topics have begun to migrate to Viva Topics. Over the next months, all existing Viva Engage networks will be migrated. Answers use Viva Topics to organize questions posted and identify the people associated with certain Viva Topics to help route those questions. Because Viva Topics works across services in Microsoft 365, we require that your Viva Engage network uses Viva Topics to ensure the best experience with Answers.

   Customers who are awaiting topics migration can request to get Answers enablement prioritized, which may include Native Mode support or Viva Engage Topics migration to Viva Topics. Contact your customer account manager or Microsoft Viva Engage support to file a support ticket.

    Learn more about Viva Engage Topics migration to Viva Topics:
    - [Viva Topics in Viva Engage](/viva/topics/topic-experiences-yammer)
    - [Viva Topics experience in Viva Engage](https://support.microsoft.com/topic/viva-topics-experience-in-yammer-8e85bc0d-086e-49a2-974b-39f60129257d)

3. **Set up the Viva Engage app**

    For the best Answers experience, we recommend that all organizations install the Viva Engage app in Teams. Follow these [steps to setup Viva Engage app](/viva/engage/setup).

## Data storage, export, and compliance

A group in Office 365 backs up Answers and follows the default data [retention policies](/microsoft-365/compliance/retention-policies-yammer) set by your organization, unless a unique policy is set for Answers. The Answers backing group is autoprovisioned when the first question is posted or first the question attachment is created. At the time of creation, all Global admins are assigned as owners of the backing group, which is called *Group for Answers in Viva Engage – DO NOT DELETE.*

Owners of the backing group should ensure that Answers remains compliant with network policies and doesn't get accidentally deleted. Admins can export data if you want to delete the backing group in Office 365. If the backing group is deleted, Answers won't be functional.

>[!NOTE]
> A soft delete is recoverable within 30 days. A hard delete results in *permanent* data loss.

Answers data is available in [eDiscovery](/viva/engage/manage-security-and-compliance/overview-of-ediscovery), so you can identify and deliver electronic information that can be used as evidence in legal cases.

**General Data Protection Regulation (GDPR) information**

For a GDPR user data export, verified Viva Engage admins and Engage admins can follow the [Viva Engage GDPR export guidance](/Viva/engage/eac-as-manage-data.md). Answers data is bundled with Viva Engage data. To comply with GDPR data subject requests, you can erase all information about a Viva Engage user. Learn [how to manage GDPR data subject requests in Viva Engage](./manage-security-and-compliance/gdpr-requests-in-viva-engage-enterprise.md).

## Enable Answers  

All users that have the Viva Engage Knowledge service plan assigned can view Answers, as it's on by default. You can turn off Answers to remove it from view in the Viva Engage Teams app. Users will still be able to access Answers content through existing links. However, they can't contribute to threads or navigate the Answers experience.  

Only a Microsoft 365 Global admin can change Answers state of enablement. Here's how:

1. Go to the Viva Engage Teams app.  
2. Select the ellipses button from the top right navigation bar to expose admin options.  
3. Select **Admin** to navigate to the Viva Engage admin center.

   [![Screenshot of the admin entrypoint into the Viva Engage admin center.](/viva/media/engage/admin/admin-entrypoint.png)](/viva/media/engage/admin/admin-entrypoint.png#lightbox)

4. On the **Feature management** tab, select the **Answers** button  to open the Answers configuration options.

   [![Screenshot of the admin entrypoint into Answers feature management in the Viva Engage admin center.](/viva/media/engage/admin/answers-eac.png)](/viva/media/engage/admin/answers-eac.png#lightbox)

5. In Answers feature management, you can enable or disable Answers for your organization. Answers is turned on by default for all Viva suite and Viva Topics licensed users.  

   [![Screenshot of the Answers enablement toggle in the Viva Engage admin center.](/viva/media/engage/admin/enable-answers.png)](/viva/media/engage/admin/enable-answers.png#lightbox)

>[!NOTE]
> If Answers is disabled, the backing group will respect the default data [retention policies](/microsoft-365/compliance/retention-policies-viva-engage) set by your organization, unless a unique policy is set for Answers.

## Show Viva Engage Experience

Answers resides within Viva Engage. Organizations that aren't ready to begin using all the Viva Engage features can choose to enter an Answers-focused experience and hide other Viva Engage features such as storylines, communities and leadership. Hidden Viva Engage content can still be accessed through existing links, but users can't navigate to Viva Engage features other than Answers.

For this feature to be available, the network is required to have two or fewer Engage communities. Only a Microsoft 365 Global admin can change Viva Engage state of enablement.

1. Go to the Viva Engage Teams app.

2. Select the ellipses button from the top right navigation bar to expose admin options.

3. Select **Admin** to navigate to the Viva Engage admin center.

 :::image type="content" source="../media/engage/admin/admin-entry-point.png" lightbox="../media/engage/admin/admin-entry-point.png" alt-text="Screenshot of entry point to the admin center.":::

4. On the **Feature management** tab, select the **Answers** button to open the Answers configuration options.

 :::image type="content" source="../media/engage/admin/answers-eac.png" lightbox="../media/engage/admin/answers-eac.png" alt-text="Screenshot showing how to get to Answers options.":::

5. In Answers feature management, you can switch **Show Engage Experience** on or off for your organization.

 :::image type="content" source="../media/engage/admin/answers-eac-default-controls.png" lightbox="../media/engage/admin/answers-eac-default-controls.png" alt-text="Screenshot showing the Show Engage Experience setting.":::

 The Viva Engage Experience can't be hidden if Answers is turned off, or if the tenant has more than two active communities.
    
 :::image type="content" source="../media/engage/admin/answers-eac-show-exp-off.png" lightbox="../media/engage/admin/answers-eac-show-exp-off.png" alt-text="Screenshot shows that Answers must be enabled to turn off the Show Engage Experience setting.":::

> [!NOTE]
> If the Viva Engage Experience is hidden, the backing group respects the [data retention policies](/microsoft-365/compliance/retention-policies-yammer?view=o365-worldwide&preserve-view=true) set by your organization. The admin can still [export and manage their data](/rest/api/yammmer/network-data-export.md).  

## See also

[Answers admin scenarios in Viva](/viva/engage/eac-answers-admin-scenarios)

[Answers in Viva: Frequently asked questions (FAQ)](/viva/engage/eac-answers-faq)

[Key admin roles and permissions in Viva Engage](/viva/engage/eac-key-admin-roles-permissions)
