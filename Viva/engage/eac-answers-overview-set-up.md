---
title: "Overview and setup of Answers in Viva"
description: "Overview and setup of Answers in Viva, including licensing, technical requirements, and data management."
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: pamgreen
ms.date: 09/27/2023
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

**Answers in Microsoft Viva** is an experience for people in large organizations to learn from each other by asking and answering questions. Access Answers in the Viva Engage app from the **Answers** tab.

With Answers, employees can ask questions, get crowdsourced answers, and find subject matter expertise captured in Viva Topics. Natural language processing helps match questions with available answers, and the experience rewards people who contribute to Answers.

## Licensing

When you enable Answers in the Viva Engage admin center, users who are assigned the Viva Engage Knowledge service plan have access to the full Answers experience in the Viva Engage Teams app, including rewards and recognition. The Viva Engage Knowledge service plan is available as part of the *Microsoft Viva Suite* and *Viva Topics* products.

Users who are not assigned the Viva Engage Knowledge service plan receive notifications when they're mentioned in Answers and can visit those threads. But they can't navigate the rest of the Answers experience.

> [!NOTE]
> As a prerequisite, the tenant must have Viva Engage enabled, and the user must have access to Viva Engage services.

## Technical requirements

By default, the Answers experience is enabled for customers who meet the following technical requirements:

- **Viva Engage network is in Native Mode**

    [Native Mode](overview-native-mode.md) is a state of a Viva Engage network where all users are in Microsoft Entra ID (formerly Azure Active Directory). All communities are Microsoft 365 groups, and all files are stored in SharePoint Online. This setup ensures that the service can apply topic permissions and management. For more information, see the [guide to migrate](native-mode-guide.md) the network to Native Mode.

- **Viva Engage uses Viva Topics**

   The Answers experience uses Viva Topics to organize questions and identify people associated with certain topics to help route those questions.
   For Viva Engage customers to gain these benefits, we're integrating Viva Topics into Viva Engage, which involves migrating Viva Engage Topics to Viva Topics. Users don't need a paid Viva Topics license to migrate their topics or to use Answers. Learn more about [the migration](/viva/topics/topic-experiences-yammer)and the [Viva Topics experience](https://support.microsoft.com/topic/viva-topics-experience-in-yammer-8e85bc0d-086e-49a2-974b-39f60129257d).

   Customers awaiting topics migration can request to prioritize their Answers enablement, which may include Native Mode support or Viva Engage Topics migration to Viva Topics. Contact your customer account manager or Microsoft Viva Engage support to file a support ticket.

- **The Viva Engage app is set up**

    For the best Answers experience, we recommend that all organizations install the Viva Engage app in Teams. Follow these [steps to set up the Viva Engage app](/viva/engage/setup).

## Compliance and Answers data

Unless you've set a unique policy for Answers, a group in Office 365 backs up Answers data in accordance to your organization's default data [retention policies](/microsoft-365/compliance/retention-policies-yammer). The Answers backing group is auto provisioned when the first question is posted or the first question attachment is created. All Global admins are assigned as owners of the Answers backing group, which is called *Group for Answers in Viva Engage – DO NOT DELETE.*

To remain compliant with network policies, owners of the backing group should ensure that the Answers backing group isn't accidentally deleted. If you want to delete the backing group in Microsoft 365, admins can export data. If the backing group is deleted, Answers is non-functional.
>[!NOTE]
> A soft delete is recoverable within 30 days. A hard delete results in *permanent* data loss.

Answers data is available in [eDiscovery](/viva/engage/manage-security-and-compliance/overview-of-ediscovery), so you can identify and deliver electronic information that can be used as evidence in legal cases.

**General Data Protection Regulation (GDPR) information**

To export personally identifiable user data, verified Viva Engage admins and Engage admins can follow the [Viva Engage GDPR export guidance](/Viva/engage/eac-as-manage-data.md). Answers data is bundled with Viva Engage data. To comply with GDPR data subject requests, erase all information about a Viva Engage user. Learn [how to manage GDPR data subject requests in Viva Engage](./manage-security-and-compliance/gdpr-requests-in-viva-engage-enterprise.md).

## Procedure: Enable Answers  

All users who have the Viva Engage Knowledge service plan assigned can view Answers, as it's on by default. You can hide it from the Viva Engage Teams app to prevent users from contributing to threads or navigating the Answers experience. However, users can still access Answers content through existing links.

Only Microsoft 365 Global administrators can change the Answers state of enablement:

1. Go to the Viva Engage Teams app.  
2. Select the ellipses button from the top right navigation bar to expose admin options.  
3. Select **Admin** to navigate to the Viva Engage admin center.

   [![Screenshot of the admin entrypoint into the Viva Engage admin center.](/viva/media/engage/admin/admin-entrypoint.png)](/viva/media/engage/admin/admin-entrypoint.png#lightbox)

4. On the **Feature management** tab, select the **Answers** button  to open the Answers configuration options.

   [![Screenshot of the admin entrypoint into Answers feature management in the Viva Engage admin center.](/viva/media/engage/admin/answers-eac.png)](/viva/media/engage/admin/answers-eac.png#lightbox)

5. In Answers feature management, you can enable or disable Answers for your organization. Answers is turned on by default for all Viva suite and Viva Topics licensed users.  

   [![Screenshot of the Answers enablement toggle in the Viva Engage admin center.](/viva/media/engage/admin/enable-answers.png)](/viva/media/engage/admin/enable-answers.png#lightbox)

> [!NOTE]
> If Answers is disabled, the backing group respects the default data [retention policies](/microsoft-365/compliance/retention-policies-viva-engage) set by your organization, unless a unique policy is set for Answers.

### Option: Show Viva Engage experience

Answers resides within Viva Engage. Organizations that aren't ready to use all Viva Engage features can choose an Answers-focused experience while hiding other Viva Engage features such as storylines, communities, and leadership. Hidden Viva Engage content can still be accessed through existing links, but users can't navigate to Viva Engage features other than Answers.

For this feature to be available, the network is required to have two or fewer Engage communities. Only Microsoft 365 Global administrators can change the Viva Engage state of enablement.

1. Go to the Viva Engage Teams app.

2. Select the ellipses button from the top right navigation bar to expose admin options.

3. Select **Admin** to navigate to the Viva Engage admin center.

4. On the **Feature management** tab, select the **Answers** button to open the Answers configuration options.

5. In Answers feature management, switch **Show Engage Experience** on or off for your organization.

The Viva Engage Experience can't be hidden if Answers is turned off, or if the tenant has more than two active communities.

 :::image type="content" source="../media/engage/admin/answers-eac-default-controls.png" alt-text="Screenshot showing the Show Engage Experience setting.":::

 :::image type="content" source="../media/engage/admin/answers-eac-show-exp-off.png" alt-text="Screenshot shows that Answers must be enabled to turn off the Show Engage Experience setting.":::

> [!NOTE]
> If the Viva Engage experience is hidden, the backing group follows the [data retention policies](/microsoft-365/compliance/retention-policies-yammer?view=o365-worldwide&preserve-view=true) set by your organization. The admin can still [export and manage their data](/rest/api/yammmer/network-data-export.md).

### Option: Show AI suggested topics

All Viva Engage users who have access to Answers also have AI-suggested topics, by default. When a user posts a question on Answers, generative AI returns relevant Viva Topics for the user to choose from and include with their post.  

Only Microsoft 365 Global administrators can turn this feature off to hide it from the Answers experience.

1. Go to the Viva Engage Teams app.  

1. Select the ellipses button from the top-right navigation bar to expose admin options.  

1. Select **Admin** to navigate to the Viva Engage admin center.

1. On the **Feature management** tab, select the Answers button to open the Answers configuration options.

1. In Answers feature management, switch **Enable AI-suggested topics** on or off for your organization.

    :::image type="content" source="../media/engage/admin/ea-answers-ai-1.png" alt-text="Screenshot shows the default setting for AI suggested topics when Answers is enabled.":::

    :::image type="content" source="../media/engage/admin/ea-answers-ai-2.png" alt-text="Screenshot shows how to turn off AI suggested topics.":::

## See also

[Answers admin scenarios in Viva](/viva/engage/eac-answers-admin-scenarios)

[Answers in Viva: Frequently asked questions (FAQ)](/viva/engage/eac-answers-faq)

[Key admin roles and permissions in Viva Engage](/viva/engage/eac-key-admin-roles-permissions)
