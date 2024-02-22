---
title: "Set up Answers in Viva"
description: "Overview and setup of Answers in Viva, including licensing, technical requirements, and data management."
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 01/17/2024
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Set up Answers in Viva

**Answers in Microsoft Viva** is a new experience for people in large organizations to learn from each other by asking and answering questions. Access is through the Viva Engage Teams app, both on the **Answers** tab and on the **Communities** tab in communities of which the user is a member.

Answers lets employees ask questions and connect to crowdsourced answers. Natural language processing helps match questions with available answers, and the experience rewards people who contribute to Answers.

Answers helps users get their questions answered, connect with subject matter experts, and increase their learning.

## Licensing

Users who are assigned the Viva Engage Knowledge service plan, which is part of the Microsoft Viva Suite and Viva Employee Communications and Communities licenses, have access to the Answers experience in the Viva Engage Teams app. These users can ask and answer questions in communities and on the Answers tab, find similar questions, and receive rewards and recognition.  

Users who aren't assigned the Viva Engage Knowledge service plan won't have the full Answers experience, but can ask questions and view, vote, and respond to questions others have written from the communities in which they’re a member. Anytime their name is mentioned in Answers, they receive notifications to those questions and can visit those threads.

For more information about permissions, see [Administrator scenarios for Answers in Viva Engage](eac-answers-admin-scenarios.md).

## Technical requirements

By default, the Answers experience is enabled for networks that meet the following technical requirements:

1. **Users have access to Viva Engage services**

   Viva Engage is enabled for the organization and users have access to Viva Engage services. For the best Answers experience, we recommend that all organizations [install the Viva Engage app in Microsoft Teams](/viva/engage/setup#installing-viva-engage). 

1. **Viva Engage network is in Native Mode**

   [Native Mode](overview-native-mode.md) is a state of a Viva Engage network where all users are in Microsoft Entra ID. All communities are Microsoft 365 groups and all files are stored in SharePoint Online. This setup ensures that the service can appropriately apply topic permissions and management. For details, see the [guide to migrate](native-mode-guide.md) the network to Native Mode.

2. **Viva Engage uses Topics**

   Viva Topics will be retired in 2025. As part of that change, Viva Engage will return to a simplified topics mode. During the transition, proactive migrations to use Viva Topics will be paused, but migrations that enable customers to use Answers will continue by request.
  Users aren't required to have a paid Topics license to migrate their topics or to use Answers. Learn more about [the migration](/microsoft-365/topics/topic-experiences-viva-engage), [the Topics experience](https://support.microsoft.com/topic/viva-topics-experience-in-yammer-8e85bc0d-086e-49a2-974b-39f60129257d), and the Topics retirement.
   
   Customers awaiting topics migration can request to get Answers enablement prioritized, which may include Native Mode support or Viva Engage Topics migration to Topics. Contact your customer account manager or Microsoft Viva Engage support to file a support ticket.

## Compliance and Answers data

Unless you’ve set a unique policy for Answers, a group in Microsoft 365 backs up Answers data. This group follows your organization’s default data [retention policies](/microsoft-365/compliance/retention-policies-yammer). The Answers backing group is autoprovisioned when the first question is posted or a question attachment is created. At the time of creation, all Microsoft 365 Global admins are assigned as owners of the backing group, which is called *Group for Answers in Viva Engage – DO NOT DELETE.*

Owners of the backing group should ensure that Answers remains compliant with network policies and doesn't get accidentally deleted. Admins can export data if you want to delete the backing group in Microsoft 365. If the backing group is deleted, Answers won't be functional.

>[!NOTE]
> A soft delete is recoverable within 30 days. A hard delete results in *permanent* data loss.

Answers data is available in [eDiscovery](/viva/engage/manage-security-and-compliance/overview-of-ediscovery), so you can identify and deliver electronic information that can be used as evidence in legal cases.

#### General Data Protection Regulation (GDPR)
For a GDPR user data export, verified Viva Engage admins and Engage admins can follow the [Viva Engage GDPR export guidance](/Viva/engage/eac-as-manage-data). Answers data is bundled with Viva Engage data. To comply with GDPR data subject requests, you can erase all information about a Viva Engage user. Learn [how to manage GDPR data subject requests in Viva Engage](./manage-security-and-compliance/gdpr-requests-in-viva-engage-enterprise.md).

## Configure the Answers experience

> [!NOTE]
> You must be a Microsoft 365 Global admin to configure Answers and Answers-related options.

By default, Answers is turned on. Optionally, you can hide Answers from view in the Viva Engage Teams app, which allows users to access Answers content only through existing links. However, they won't be able to contribute to threads or navigate the Answers experience.

1. In the Viva Engage Teams app, select the ellipses button from the top right navigation bar, and select **Admin** to navigate to the Viva Engage admin center.

   [![Screenshot of the admin entrypoint into the Viva Engage admin center.](/viva/media/engage/admin/admin-entrypoint.png)](/viva/media/engage/admin/admin-entrypoint.png#lightbox)

1. On the **Feature management** tab, select the **Answers** button  to open the Answers configuration options.

   [![Screenshot of the admin entrypoint into Answers feature management in the Viva Engage admin center.](/viva/media/engage/admin/answers-eac.png)](/viva/media/engage/admin/answers-eac.png#lightbox)

1. Use the **Enable Answers** toggle to enable or disable Answers for your organization. Answers is turned on by default.  

   [![Screenshot of the Answers enablement toggle in the Viva Engage admin center.](/viva/media/engage/admin/enable-answers.png)](/viva/media/engage/admin/enable-answers.png#lightbox)

>[!NOTE]
> If Answers is disabled, the backing group complies with the default data [retention policies](/microsoft-365/compliance/retention-policies-viva-engage) set by your organization, unless a unique policy is set for Answers.

## Option: Show Viva Engage experience

Answers resides within Viva Engage. Organizations that aren't ready to begin using all the Viva Engage features can choose to enter an Answers-focused experience and hide other Viva Engage features such as storylines, communities and leadership. Hidden Viva Engage content can still be accessed through existing links, but users can't navigate to Viva Engage features other than Answers.

For this feature to be available, the network must have two or fewer Engage communities.

1. In the Viva Engage Teams app, select the ellipses button from the top right navigation bar, and select **Admin** to navigate to the Viva Engage admin center.

1. On the **Feature management** tab, select the **Answers** button to open the Answers configuration options.

1. Switch **Show Engage Experience** on or off for your organization.
This option is unavailable if Answers if turned off, or if the tenant has more than two active communities.
    
:::image type="content" source="../media/engage/admin/answers-eac-show-exp-off.png" lightbox="../media/engage/admin/answers-eac-show-exp-off.png" alt-text="Screenshot shows that Answers must be enabled to turn off the Show Engage Experience setting.":::

> [!NOTE]
> If the Viva Engage Experience is hidden, the backing group respects the [data retention policies](/microsoft-365/compliance/retention-policies-yammer?view=o365-worldwide&preserve-view=true) set by your organization. The admin can still export and manage their data.

## Option: Enable AI-suggested topics

Users assigned the Viva Engage Knowledge Service Plan have AI-suggested topics in Answers. When a user posts a question on Answers, generative AI returns up to three relevant topics for the user to include with their post.

1. In the Viva Engage Teams app, select the ellipses button from the top right navigation bar, and select **Admin** to navigate to the Viva Engage admin center.

1. On the **Feature management** tab, select the **Answers** button to open the Answers configuration options.  

   :::image type="content" source="../media/engage/admin/ea-answers-ai-1.png" lightbox="../media/engage/admin/ea-answers-ai-1.png" alt-text="Screenshot shows AI-suggested topics turned on.":::

1. In Answers feature management, switch **Enable AI-suggested topics** on or off for your organization.

   :::image type="content" source="../media/engage/admin/ea-answers-ai-2.png" lightbox="../media/engage/admin/ea-answers-ai-2.png" alt-text="Screenshot shows  AI-suggested topics turned off.":::

## Option: Enable rewards and recognition

By contributing to Answers in Viva, users can earn and collect up to five different badges. Badges are available and visible to anyone in the organization who has a Viva Engage Knowledge Service Plan. This feature requires Answers to collect user data, such as votes from fellow employees, which count toward badges.

1. In the Viva Engage Teams app, select the ellipses button from the top-right navigation bar, and select **Admin** to navigate to the Viva Engage admin center.

2. On the **Feature management** tab, select **Rewards and recognition**.

[![Screenshot shows the interface for Answers badges settings in the Viva Engage admin center.](/Viva/media/netnew/badges-settings.png)](/Viva/media/netnew/badges-settings.png#lightbox)

3. Configure badges by selecting from these options:

   - **On** enables badges for the organization.

   - **User Preference** enables badges for the organization while allowing individuals to opt out. The end user can turn off badges in Viva Engage by selecting the ellipses button on the right of their **Achievements and awards** page.
   - **Disabled** turns badges off in Answers in Viva. If you switch this control from **On** to **Disabled**, all badges earned by users are deleted and unrecoverable. Answers stops collecting user data for badges.

[![Screenshot shows the Viva Engage interface where users can turn off Answers badges.](/Viva/media/netnew/badges-turn-off.png)](/Viva/media/netnew/badges-turn-off.png#lightbox)



## See also

[Administrator scenarios for Answers in Viva Engage](/viva/engage/eac-answers-admin-scenarios)

[Answers in Viva: Frequently asked questions (FAQ)](/viva/engage/eac-answers-faq)

[Manage administrator roles in Viva Engage](/viva/engage/eac-key-admin-roles-permissions)
