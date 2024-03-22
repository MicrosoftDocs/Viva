---
title: "Set up Copilot in Viva Engage [Public Preview] "
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 03/22/2024
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
>Copilot in Viva Engage is currently available through public preview, and will be generally available on April 29th. The features described here are subject to change.

Copilot in Viva Engage is a partner for communicating in ways that create value for oneself and one’s organization. Copilot provides users access to Large Language Model (LLM) technology with Microsoft Responsible AI protections, to assist them to get the most out of Viva Engage.
A large language model is a type of AI that can process and produce natural language text. Copilot helps users get the most out of Viva Engage by collaborating on written communications and suggesting where to post.

## Licensing requirements

At the end of April 2024, Copilot in Viva Engage will be enabled for all users assigned a premium Viva Engage license (purchased as part of _Microsoft Viva Suite_ or _Microsoft Viva Employee Communications and Communities_). For details on Microsoft Viva plans and pricing, visit the [Employee Experience Platform Plans and Pricing page](https://www.microsoft.com/microsoft-viva/pricing). AI-powered Summarization will also be enabled at the same time for all users in the premium licensed tenant. AI Summarization includes AI-powered summarization, theme extraction, and sentiment analysis.

Viva Engage must be [in Native Mode](overview-native-mode.md) to support feature access.

[Microsoft 365 Copilot](/microsoft-365-copilot/microsoft-365-copilot-setup) is available separately.

## Data processing and storage

:::image type="content" source="/viva/media/engage/admin/copilot-engage-dataflow.png" alt-text="Graph that shows how data flows between Copilot services while staying within the boundary of the Viva Engage app." lightbox="/viva/media/engage/admin/copilot-engage-dataflow.png":::

| **Data process** | **How it works** |
|---|---|
|**Message processing and storage for summarization**| **Summarization** starts background processing of Engage threads across the tenant network to support summarization features in Copilot and Network analytics. These features present summaries *only from posts to which the user already has access*. Results from summarization are stored in alignment with GDPR deletion requirements. To export this data, use the [Engage network export feature](/Viva/engage/eac-as-manage-data#export-tenant-data-by-date-range). | 
|**Processing of user commands to Copilot**|User interactions with Copilot during chat collaboration are currently processed, but not stored, with services aligned to Data center regional elections (US/EU Region).|

## Manage Copilot and AI Summarization with feature access policies

Global admins and Engage admins can now make changes to Copilot availability and AI Summarization data processing for users in the tenant through feature access management PowerShell cmdlets. Through cmdlets, admins can use the Viva feature access management platform to control availability of these premium features for the entire tenant and users or groups they deem appropriate.  

Copilot and AI Summarization are controlled separately and can be turned on or off. Additionally, for AI Summarization, admins can create granular access policies that support a third state–-on with user opt out.

Policy settings apply anytime a user signs in, allowing them access to features that haven't been disabled.
Because you can set multiple access policies, targeting the tenant, groups, and individual users, a user might be impacted by more than one policy. Individual user and group level policies always take priority over a tenant-level policy. For instructions, see [Control access to features in Viva](/viva/feature-access-management).

### Copilot and AI Summarization states

You can create feature access policies using the following enablement states.

>[!NOTE]
>AI Summarization is used by Copilot and [Network analytics](/viva/engage/analytics#network-analytics) in Engage. Summarization services help with conversation summarization in Copilot, and theme extraction, summarization, and sentiment analysis in Network Analytics which is only available to assigned admins and corporate communicators. network theme extraction, conversation summarization, and network sentiment analys.

|**Engage feature**|**State**|**Description**|
|:-------------|:------------------:|:----------------------|
|**Copilot**|Enabled|When Copilot is enabled, users can access Copilot in Engage through their home feed, storyline, community feed, and campaign pages.|
| | Disabled| Copilot is not available anywhere in Viva Engage|
|**AI Summarization** | Enabled| This state enables background processing for Engage threads within the tenant.|
| |Enabled with user opt out| This state allows users to turn off background processing from their personal analytics page in Viva Engage.|
| |Disabled|When you disable AI Summarization, the users' Engage threads won't be processed. If you disable AI Summarization for the entire tenant and have no user or group access policy in place that enables the feature, all historic background processing data is deleted retroactively. To avoid deletion of summarization data for all users in the tenant, accompany this setting change with a policy that enables the feature for at least each group.|

#### Example

If an admin needs to  disable Copilot only for users in Germany, they can accomplish that in feature access management using the following steps:

1. Create a group access policy in feature access management using PowerShell cmdlets.
1. Assign the Microsoft 365 group that contains all Germany users to the group policy.  
1. Set the group policy to OFF (disabled).

As a result, all remaining users in the organizations (except Germany) can now use Copilot in Viva Engage. 

#### Important considerations for feature access management

- There can only be a maximum of 1 tenant policy per Viva Engage feature. In other words, there can only be 1 tenant policy for Copilot and only one tenant policy for Summarization.

- Creating a disabled (OFF) tenant policy for Summarization will delete all history data within the tenant.

    To avoid deletion of Summarization data for all users within the tenant, admins should ensure that the feature disable (OFF) tenant policy is immediately accompanied with at least 1 feature enable (ON) group policy.

## How to access Copilot

Users can access Copilot anywhere they write posts. On the Engage Home page, Copilot also generates proactive suggestions about what they might like to write about and where they might benefit from engaging.

:::image type="content" source="/viva/media/engage/admin/copilot-engage-home-start.png" alt-text="Screenshot shows the Open Copilot link on the Viva Engage Home page.":::

### Copilot as Viva Engage guide

Copilot makes personalized suggestions of what to post on Viva Engage, and where. These suggestions, or Conversation Starters, are personalized based on the viewing user’s activity and what is trending in their organization’s network.

:::image type="content" source="/viva/media/engage/admin/copilot-engage-writing-coach.png" alt-text="Screenshot shows how Copilot provides helpful tips for writing a great post." lightbox="/viva/media/engage/admin/copilot-engage-writing-coach.png":::

The Conversation Starters bring together information from across Viva Engage to help people:

- Be an active voice in their Viva Engage communities. Copilot summarizes the community’s purpose and recent trending posts to help people to create posts for the audience.

- Participate in Viva Engage campaigns. Copilot suggests campaigns sponsored by one's leaders and aligned with one’s interests, summarizing the campaign’s purpose and recent posts to help people contribute to these shared initiatives.

- Communicate on storyline in ways that improve culture and productivity for oneself and others. Viva Engage has partnered with experts in employee experience to create a library of research-backed post suggestions that encourage best practices like recognizing one’s teammates, sharing one's knowledge or learning goals, and communicating plans for the future.

    >[!NOTE]
    >Copilot AI-generated summaries are only shown to users who have access to the underlying posts.

### Copilot as communication partner

Copilot also offers collaboration on writing Viva Engage posts. Users can chat with Copilot to access the power and flexibility of Large Language Models with Microsoft Responsible AI protections. Whether a writer is starting from scratch or a draft, Engage Copilot can help draft, edit, give feedback, and more, to create a post that aligns with the user’s goals.

:::image type="content" source="/viva/media/engage/admin/copilot-engage-writing-prompt.png" alt-text="Screenshot shows options you can use to have Copilot write a draft for you." lightbox="/viva/media/engage/admin/copilot-engage-writing-prompt.png":::

For users who are new to AI collaboration, or even experienced users looking for fresh ideas, the sparkle menu provides examples of prompts that can be sent to Copilot. This prompt guide is designed to help users collaborate with Copilot in ways particularly useful to the task at hand–writing a post that is engaging and expresses what they intend.

:::image type="content" source="/viva/media/engage/admin/copilot-engage-sparkly.png" alt-text="Screenshot shows the sparkle menu. "lightbox="/viva/media/engage/admin/copilot-sparkle-crop.png":::

The sparkle menu provides examples of ways users can ask Copilot for help drafting or rewriting their post, examples of ways to ask Copilot for feedback, and more.

During collaboration, Copilot provides proactive coaching to help maintain authenticity in Copiloted content, and the expression of unique perspective, knowledge, and insight in posts to enhance the creation of value across the Viva Engage network.

## See also

[Data, Privacy, and Security for Copilot in Viva Engage](/Viva/engage/manage-security-and-compliance/data-privacy-security-copilot-engage)
