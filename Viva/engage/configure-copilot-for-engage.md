---
title: "Set up Copilot in Viva Engage [Public Preview] "
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 03/24/2024
audience: Admin
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
ms.localizationpriority: medium
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 
description: "Learn how to configure and incorporate Copilot in Viva Engage [Public Preview] into your organization"
---

# Set up Copilot in Viva Engage (Public Preview) 

>[!IMPORTANT]
>Copilot in Viva Engage is currently available through public preview. The features described here are subject to change.

Copilot in Engage is a partner for communicating in ways that create value for oneself and one’s organization. Copilot provides users access to Large Language Model (LLM) technology with [Microsoft Responsible AI protections](/ai/responsible-ai), to assist them to get the most out of Viva Engage. 
A large language model is a type of AI that can process and produce natural language text. Copilot helps users get the most out of Viva Engage by suggesting where to engage and collaborating on writing communications.

## Licensing requirements

Beginning in late April 2024, Copilot in Engage will be available and enabled for all premium users as part of their Microsoft Viva license plans. AI-powered Summarization will be enabled at the same time for all users in the premium licensed tenant. Viva Engage must be [in Native Mode](overview-native-mode.md) to support feature access.

[Microsoft 365 Copilot](/microsoft-365-copilot/microsoft-365-copilot-setup) is available separately.

## Data processing and storage

:::image type="content" source="/viva/media/engage/admin/copilot-engage-dataflow.png" alt-text="Graph that shows how data flows between Copilot services while staying within the boundary of the Viva Engage app." lightbox="/viva/media/engage/admin/copilot-engage-dataflow.png":::

| **Data process** | **How it works** |
|---|---|
|Message processing and storage for summarization| **Summarization** starts background processing of Engage threads across the tenant network to support summarization features in Copilot and Network analytics. These features present summaries *only from posts to which the user already has access*. Results from summarization are stored in alignment with GDPR deletion requirements. To export this data, use the [Engage network export feature](/Viva/engage/eac-as-manage-data#export-tenant-data-by-date-range). | 
|**Processing of user commands to Copilot**|User interactions with Copilot during chat collaboration are currently processed, but not stored, with services aligned to Data center regional elections (US/EU Region).|

## Manage Copilot and Summarization with feature access policies

While admins can disable Copilot and Summarization in the Engage admin center, we recommend that you use feature access policies to manage access to these features. Microsoft 365 access policies are set independently of your Engage settings and can apply to tenants or groups.

- Tenant policies affect all users in the tenant
- Group/user level policies let you choose individual users and groups to be managed by the policy

Policy settings apply anytime a user signs in, allowing them access to features that haven't been disabled. Because you can set multiple access policies, a user or group might be impacted by more than one policy. Individual user and group level policies always take priority over a tenant-level policy. For details, see [Control access to features in Viva](/viva/feature-access-management).

## Control Copilot and Summarization in the Engage admin center

Microsoft 365 Global administrators and Engage admins can control Copilot from the Viva Engage admin center.   

1.	Go to the [Viva Engage admin center](/Viva/engage/eac-as-access-eac).
1.	On the **Setup and configuration** tab, select **Manage AI and analytics**.
    :::image type="content" source="/viva/media/engage/admin/admin-center-copilot-crop2.png" alt-text="Screenshot shows Copilot controls within the Analytics and AI controls.":::

#### Enable Copilot in Engage

When Copilot is enabled, users can access Copilot in Engage through their home feed, storyline, community feed, and campaign pages.  

#### Enable Summarization in Engage

>[!NOTE]
>Both Copilot and [Network analytics](/viva/engage/analytics#network-analytics) in Engage require  Summarization services to be on to function. Summarization services are used for network theme extraction, summarization, and sentiment analysis.

If Summarization is enabled for a group, user, or tenant, background processing is enabled for Engage threads within the tenant. If Summarization is enabled with user opt out, users can turn off background processing from their personal analytics page in Viva Engage. When Summarization is disabled for the entire tenant without any user/group policies, all historic background processing data is deleted retroactively. To avoid deletion of summarization data for all users in the tenant, admins should immediately accompany this setting change with a tenant policy that enables at least one feature for each group.|

Depending on the volume of data represented by Engage threads in your tenant, summarization may require anywhere from a few hours to a few days to process content. If Engage threads aren’t processed, some aspects of Copilot won’t function optimally.

## How to access Copilot

Users can access Copilot anywhere they write posts. On the Engage Home page, Copilot generates proactive suggestions about what they might like to write about and where they might benefit from engaging.

:::image type="content" source="/viva/media/engage/admin/copilot-engage-home-start.png" alt-text="Screenshot shows the Open Copilot link on the Viva Engage Home page.":::

### Copilot as Viva Engage guide

Copilot makes personalized suggestions of what to post on Viva Engage, and where. These suggestions, or Conversation Starters, are personalized based on the viewing user’s activity and what is trending in their organization’s network.

:::image type="content" source="/viva/media/engage/admin/copilot-engage-writing-coach.png" alt-text="Screenshot shows how Copilot provides helpful tips for writing a great post." lightbox="/viva/media/engage/admin/copilot-engage-writing-coach.png":::

The Conversation Starters bring together information from across Viva Engage to help people:

- Be an active voice in their Viva Engage communities. Copilot summarizes the community’s purpose and recent trending posts to help people to create posts for the audience.

- Participate in Viva Engage campaigns. Copilot suggests campaigns sponsored by one's leaders and aligned with one’s interests, summarizing the campaign’s purpose and recent posts to help people contribute to these shared initiatives.

- Communicate on storyline in ways that improve culture and productivity for oneself and others. Viva Engage has partnered with experts in employee experience to create a library of research-backed post suggestions that encourage best practices like recognizing one’s teammates, sharing one's knowledge or learning goals, and communicating plans for the future.
Copilot AI-generated summaries are only shown to users who have access to the underlying posts.

### Copilot as communication partner

Copilot also offers collaboration on writing Viva Engage posts. Users can chat with Copilot to access the power and flexibility of Large Language Models with Microsoft Responsible AI protections. Whether a writer is starting from scratch or a draft, Engage Copilot can help draft, edit, give feedback, and more, to create a post that aligns with the user’s goals.

:::image type="content" source="/viva/media/engage/admin/copilot-engage-writing-prompt.png" alt-text="Screenshot shows options you can use to have Copilot write a draft for you." lightbox="/viva/media/engage/admin/copilot-engage-writing-prompt.png":::

For users who are new to AI collaboration, or even experienced users looking for fresh ideas, the sparkle menu provides examples of prompts that can be sent to Copilot. This prompt guide is designed to help users collaborate with Copilot in ways particularly useful to the task at hand–writing a post that is engaging and expresses what they intend.

:::image type="content" source="/viva/media/engage/admin/copilot-engage-sparkly.png" alt-text="Screenshot shows the sparkle menu. "lightbox="/viva/media/engage/admin/copilot-sparkle-crop.png":::

The sparkle menu provides examples of ways users can ask Copilot for help drafting or rewriting their post, examples of ways to ask Copilot for feedback, and more.

During collaboration, Copilot provides proactive coaching to help maintain authenticity in Copiloted content, and the expression of unique perspective, knowledge, and insight in posts to enhance the creation of value across the Viva Engage network.

## See also

[Data, Privacy, and Security for Copilot in Viva Engage](/Viva/engage/manage-security-and-compliance/data-privacy-security-copilot-engage)
