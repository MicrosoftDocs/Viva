---
title: "Set up Copilot in Viva Engage"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 04/29/2024
audience: Admin
ms.topic: article
ms.service: viva-engage
ms.collection: viva-copilot
ms.localizationpriority: medium
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 
description: "Learn how to configure and incorporate Copilot in Viva Engage into your organization."
---

# Set up Copilot in Viva Engage 

Copilot in Viva Engage is your everyday AI partner, empowering you to communicate in ways that create value for you and your organization. Copilot gives users access to Large Language Model (LLM) technology with [Microsoft Responsible AI protections](https://www.microsoft.com/en-us/ai/responsible-ai). LLM is a type of AI that can process and produce natural language text. Copilot helps users get the most out of Viva Engage by collaborating on written communications and suggesting where to post.

## Licensing requirements

Copilot in Viva Engage and AI-powered Summarization is enabled for all users assigned a premium Viva Engage license (purchased as part of _Microsoft Viva Suite_ or _Microsoft Viva Employee Communications and Communities_). AI Summarization includes AI-powered summarization, theme extraction, and sentiment analysis. Both features are on by default.

For details on Microsoft Viva plans and pricing, visit the [Employee Experience Platform Plans and Pricing page](https://www.microsoft.com/microsoft-viva/pricing).

>[!NOTE]
>Viva Engage must be [in Native Mode](overview-native-mode.md) to support feature access.

## Data processing and storage

:::image type="content" source="/viva/media/engage/admin/copilot-engage-dataflow.png" alt-text="Graph that shows how data flows between Copilot services while staying within the boundary of the Viva Engage app." lightbox="/viva/media/engage/admin/copilot-engage-dataflow.png":::

| **Process** | **How it works** |
|---|---|
|**Process and store messages for summarization**| The AI Summarization feature processes Engage threads across the tenant to support summarization features in Copilot and Network Analytics. Summarization presents summaries *only from posts to which the user already has access*. Results from summarization are stored in alignment with GDPR deletion requirements. To export this data, use the [Engage network export feature](/Viva/engage/eac-as-manage-data#export-tenant-data-by-date-range). |
|**Process commands to Copilot**|User interactions with Copilot during chat collaboration are currently processed, but not stored, with services aligned to Data center regional elections (US/EU Region).|

## Control access to Copilot and AI Summarization services

To control access to these services, Microsoft Global administrators and Engage admins must use the [Viva feature access management platform](/viva/feature-access-management). This platform provides a flexible approach to deployment that you can tailor to your organization. You can control the availability of individual premium features by creating multiple access policies for the entire tenant, users, or groups.  

Policy settings apply anytime a user signs in, allowing the user access to all enabled features. Because you can set multiple access policies--targeting the tenant, groups, and individual users--a user might be impacted by more than one policy. Individual user and group level policies always take priority over a tenant-level policy. For instructions, see [Control access to features in Viva](/viva/feature-access-management).

### Copilot and AI Summarization enablement states

Copilot and AI Summarization are controlled separately and can be turned on or off. For AI Summarization, admins can create access policies that support a third enablement state–-enabled with an option for users to opt out.

>[!NOTE]
>Copilot and Network analytics rely on AI Summarization services. In Copilot, summarization services help with conversation summarization. In Network analytics, summarization services are used in network theme extraction, conversation summarization, and network sentiment analysis. [Network analytics](/viva/engage/analytics) is  only available to network admins and corporate communicators.


|**Engage feature**|**State**|**Description**|
|:-------------|:------------------:|:----------------------|
|**Copilot**|**Enabled**|When Copilot is enabled, users can access Copilot in Viva Engage through their home feed, storyline, community feed, and campaign pages.|
| | Disabled| Copilot isn't available anywhere in Viva Engage|
|**AI Summarization** |**Enabled**| This state enables background processing for Engage threads within the tenant.|
| |**Enabled with user opt out**| This state allows users to turn off background processing from their personal analytics page in Viva Engage.|
| |**Disabled|If you disable AI Summarization, it stops processing the users' Engage threads. If you disable AI Summarization for the tenant and provide no enablement policies for user or group access, all historic background processing data is deleted retroactively. To avoid deletion of summarization data for all users in the tenant, accompany this setting change with a policy that enables the feature for at least each group.|

#### Example

If an admin needs to  disable Copilot only for users in Germany, they can accomplish that in feature access management using the following steps:

1. Create a group access policy in feature access management using PowerShell cmdlets.
1. Assign the Microsoft 365 group that contains all Germany users to the group policy.  
1. Set the group policy to OFF (disabled).

    As a result, all remaining users in the organizations (except Germany) can now use Copilot in Viva Engage.

### Important considerations for feature access management

- There can only be a maximum of one tenant policy per Viva Engage feature. In other words, there can only be one tenant policy for Copilot and only one tenant policy for Summarization.

- Creating a disabled (OFF) tenant policy for Summarization deletes all history data within the tenant.

    To avoid deletion of Summarization data for all users within the tenant, admins should immediately accompany the feature _disable_ (OFF) tenant policy with at least one feature _enable_ (ON) group policy.

## Access Copilot in Viva Engage

Users can access Copilot anywhere they write posts in Engage. On the  home page, Copilot generates proactive suggestions for what they might like to write about and where they might benefit from engaging.

:::image type="content" source="/viva/media/engage/admin/copilot-engage-home-start.png" alt-text="Screenshot shows the Open Copilot link on the Viva Engage Home page.":::

- Participate in Viva Engage campaigns. Copilot suggests campaigns sponsored by one's leaders and aligned with one’s interests, summarizing the campaign’s purpose and recent posts to help people contribute to these shared initiatives.

- Communicate on storyline in ways that improve culture and productivity for oneself and others. Viva Engage partnered with experts in employee experience to create a library of research-backed post suggestions. These suggestions encourage best practices like recognizing one’s teammates, sharing one's knowledge or learning goals, and communicating plans for the future.

    >[!NOTE]
    >Copilot AI-generated summaries are only shown to users who have access to the underlying posts.

## Copilot as Viva Engage guide

Copilot makes personalized suggestions of what to post on Viva Engage, and where. These suggestions, or Conversation Starters, are personalized based on the viewing user’s activity and what is trending in their organization’s network.

:::image type="content" source="/viva/media/engage/admin/copilot-engage-writing-coach.png" alt-text="Screenshot shows how Copilot provides helpful tips for writing a great post." lightbox="/viva/media/engage/admin/copilot-engage-writing-coach.png":::

The Conversation Starters bring together information from across Viva Engage to help people:

- Be an active voice in their Viva Engage communities. Copilot summarizes the community’s purpose and recent trending posts to help people to create posts for the audience.

- Participate in Viva Engage campaigns. Copilot suggests campaigns sponsored by one's leaders and aligned with one’s interests, summarizing the campaign’s purpose and recent posts to help people contribute to these shared initiatives.

- Communicate on storyline in ways that improve culture and productivity for oneself and others. Viva Engage has partnered with experts in employee experience to create a library of research-backed post suggestions that encourage best practices like recognizing one’s teammates, sharing one's knowledge or learning goals, and communicating plans for the future.
Copilot AI-generated summaries are only shown to users who have access to the underlying posts.

## Copilot as communication partner

Copilot also offers collaboration on writing Viva Engage posts. Users can chat with Copilot to access the power and flexibility of Large Language Models with Microsoft Responsible AI protections. Whether a writer is starting from scratch or a draft, Engage Copilot can help draft, edit, give feedback, and more, to create a post that aligns with the user’s goals.

:::image type="content" source="/viva/media/engage/admin/copilot-engage-writing-prompt.png" alt-text="Screenshot shows options you can use to have Copilot write a draft for you." lightbox="/viva/media/engage/admin/copilot-engage-writing-prompt.png":::

For users who are new to AI collaboration, or even experienced users looking for fresh ideas, the sparkle menu provides examples of prompts that can be sent to Copilot. This prompt guide is designed to help users collaborate with Copilot with the task at hand–-writing a engaging post that expresses what they intend.

:::image type="content" source="/viva/media/engage/admin/copilot-engage-sparkly.png" alt-text="Screenshot shows the sparkle menu. "lightbox="/viva/media/engage/admin/copilot-sparkle-crop.png":::

The sparkle menu provides examples of how to ask Copilot for help with drafting or rewriting a post, providing feedback, and more.

During collaboration, Copilot provides proactive coaching to help maintain authenticity in Copiloted content, and the expression of unique perspective, knowledge, and insight in posts to enhance the creation of value across the Viva Engage network.

## See also

[Data, Privacy, and Security for Copilot in Viva Engage](/Viva/engage/manage-security-and-compliance/data-privacy-security-copilot-engage)
