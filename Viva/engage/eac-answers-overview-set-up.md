---
title: "Overview and setup of Answers in Viva"
description: "Overview and setup of Answers in Viva, including licensing, technical requirements, and data management."
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: pamgreen
ms.date: 11/08/2023
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

# Overview and setup of Answers in Viva Engage

**Answers in Microsoft Viva** is a new experience for people in large organizations to learn from each other by asking and answering questions. Access is through the **Answers** tab in the Viva Engage Teams app.

Answers let employees ask questions and connect to crowdsourced answers. Natural language processing helps match questions with available answers, and the experience rewards people who contribute to Answers.

Answers work to connect employees based on their subject matter expertise captured in Topics. It helps users get their questions answered, connect with subject matter experts, and increase their learning.

## Licensing
When you enable Answers in the Viva Engage admin center, users who are assigned the Viva Engage Knowledge service plan can use the full Answers experience in the Viva Engage Teams app, including rewards and recognition. The Viva Engage Knowledge service plan is available as part of the *Microsoft Viva Suite* and *Topics* products.

Users who aren't assigned the Viva Engage Knowledge service plan receive notifications to questions or answers where they're mentioned and can visit those threads. But they can't navigate the rest of the Answers experience.

> [!NOTE]
> As a prerequisite, the tenant must have Viva Engage enabled, and the user must have access to Viva Engage services.

## Technical requirements

By default, the Answers experience is enabled for customers that meet the following technical requirements:

1) **Viva Engage network is in Native Mode**

    [Native Mode](overview-native-mode.md) is a state of a Viva Engage network where all users are in Microsoft Entra ID. All communities are Microsoft 365 groups, and all files are stored in SharePoint Online. This setup ensures that the service can appropriately apply topic permissions and management. For more information, see the [guide to migrate](native-mode-guide.md) the network to Native Mode.

2) **Viva Engage uses Topics**

   In the Answers experience, Topics help to organize questions and route them to people who are associated with and knowledgeable on specific Topics. For Viva Engage customers to gain these benefits, we're integrating Topics into Viva Engage experiences, which involves migrating Viva Engage topics to Topics.  There's no requirement for users to have a paid Topics license to migrate their topics or to use Answers.Learn more about [the migration](/microsoft-365/topics/topic-experiences-viva-engage) and [the Viva Topics experience](https://support.microsoft.com/topic/viva-topics-experience-in-yammer-8e85bc0d-086e-49a2-974b-39f60129257d).

   Customers awaiting topics migration can request to get Answers enablement prioritized, which may include Native Mode support or Viva Engage Topics migration to Topics. Contact your customer account manager or Microsoft Viva Engage support to file a support ticket.

3. **Recommended: The Viva Engage app is set up**

    For the best Answers experience, we recommend that all organizations install the Viva Engage app in Teams. Follow these [steps to set up the Viva Engage app](/viva/engage/setup).

## Compliance and Answers data

Unless you’ve set a unique policy for Answers, a group in Microsoft 365 backs up Answers data. This group follows your organization’s default data [retention policies](/microsoft-365/compliance/retention-policies-yammer). The Answers backing group is autoprovisioned when the first question is posted or a question attachment is created. At the time of creation, all global admins are assigned as owners of the backing group, which is called *Group for Answers in Viva Engage – DO NOT DELETE.*

Owners of the backing group should ensure that Answers remains compliant with network policies and doesn't get accidentally deleted. Admins can export data if you want to delete the backing group in Office 365. If the backing group is deleted, Answers won't be functional.

>[!NOTE]
> A soft delete is recoverable within 30 days. A hard delete results in *permanent* data loss.

Answers data is available in [eDiscovery](/viva/engage/manage-security-and-compliance/overview-of-ediscovery), so you can identify and deliver electronic information that can be used as evidence in legal cases.

**General Data Protection Regulation (GDPR) information**

For a GDPR user data export, verified Viva Engage admins and Engage admins can follow the [Viva Engage GDPR export guidance](/Viva/engage/eac-as-manage-data.md). Answers data is bundled with Viva Engage data. To comply with GDPR data subject requests, you can erase all information about a Viva Engage user. Learn [how to manage GDPR data subject requests in Viva Engage](./manage-security-and-compliance/gdpr-requests-in-viva-engage-enterprise.md).

## Procedure: Enable the Answers experience

By default, Answers is turned on and visible in Viva Engage for all Viva Suite and Topics licensed users who have the Viva Engage Knowledge service plan assigned.
Optionally, you can hide Answers from view in the Viva Engage Teams app, which allows users to access Answers content only through existing links. They won't be able to contribute to threads or navigate the Answers experience.  

Only a Microsoft 365 Global admin can enable or disable Answers.

1. Go to the Viva Engage Teams app.  
2. Select the ellipses button from the top right navigation bar to expose admin options.  
3. Select **Admin** to navigate to the Viva Engage admin center.

   [![Screenshot of the admin entrypoint into the Viva Engage admin center.](/viva/media/engage/admin/admin-entrypoint.png)](/viva/media/engage/admin/admin-entrypoint.png#lightbox)

4. On the **Feature management** tab, select the **Answers** button  to open the Answers configuration options.

   [![Screenshot of the admin entrypoint into Answers feature management in the Viva Engage admin center.](/viva/media/engage/admin/answers-eac.png)](/viva/media/engage/admin/answers-eac.png#lightbox)

5. In Answers feature management, you can enable or disable Answers for your organization.

   [![Screenshot of the Answers enablement toggle in the Viva Engage admin center.](/viva/media/engage/admin/enable-answers.png)](/viva/media/engage/admin/enable-answers.png#lightbox)

>[!NOTE]
> If Answers is disabled, the backing group will respect the default data [retention policies](/microsoft-365/compliance/retention-policies-viva-engage) set by your organization, unless a unique policy is set for Answers.

## Option: Show Viva Engage experience

Answers resides within Viva Engage. Organizations that aren't ready to begin using all the Viva Engage features can choose to enter an Answers-focused experience and hide other Viva Engage features such as storylines, communities and leadership. Hidden Viva Engage content can still be accessed through existing links, but users can't navigate to Viva Engage features other than Answers.

For this feature to be available, the network is required to have two or fewer Engage communities. Only a Microsoft 365 Global admin can change the Viva Engage state of enablement.

1. Go to the Viva Engage Teams app.

2. Select the ellipses button from the top right navigation bar to expose admin options.

3. Select **Admin** to navigate to the Viva Engage admin center.

4. On the **Feature management** tab, select the **Answers** button to open the Answers configuration options.

5. In Answers feature management, you can switch **Show Engage Experience** on or off for your organization.

 The Viva Engage Experience can't be hidden if Answers is turned off, or if the tenant has more than two active communities.
    
 :::image type="content" source="../media/engage/admin/answers-eac-show-exp-off.png" lightbox="../media/engage/admin/answers-eac-show-exp-off.png" alt-text="Screenshot shows that Answers must be enabled to turn off the Show Engage Experience setting.":::

> [!NOTE]
> If the Viva Engage Experience is hidden, the backing group respects the [data retention policies](/microsoft-365/compliance/retention-policies-yammer?view=o365-worldwide&preserve-view=true) set by your organization. The admin can still [export and manage their data](/rest/api/yammmer/network-data-export.md).

## Option: Enable AI-suggested topics

All Viva Engage users who have access to Answers also have AI-suggested topics, by default. When a user posts a question on Answers, generative AI returns up to three relevant topics for the user to include with their post. 

Microsoft Global 365 administrators can turn this feature off to hide it from the Answers experience.

Only a Microsoft Global 365 administrator can turn this feature off to hide it from the Answers experience.

1. Go to the Viva Engage Teams app. 
2. Select the ellipses button from the top-right navigation bar to expose admin options. 
3. Select **Admin** to navigate to the Viva Engage admin center. 
4. On the **Feature management** tab, select the **Answers** button to open the Answers configuration options.  

:::image type="content" source="../media/engage/admin/ea-answers-ai-1.png" lightbox="../media/engage/admin/ea-answers-ai-1.png" alt-text="Screenshot shows AI-suggested topics turned on.":::

5. In Answers feature management, switch **Enable AI-suggested topics** on or off for your organization. 

:::image type="content" source="../media/engage/admin/ea-answers-ai-2.png" lightbox="../media/engage/admin/ea-answers-ai-2.png" alt-text="Screenshot shows  AI-suggested topics turned off.":::

## See also

[Administrator scenarios for Answers in Viva Engage](/viva/engage/eac-answers-admin-scenarios)

[Answers in Viva: Frequently asked questions (FAQ)](/viva/engage/eac-answers-faq)

[Key admin roles and permissions in Viva Engage](/viva/engage/eac-key-admin-roles-permissions)
