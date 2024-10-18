---
title: "AI Summarization in Viva Engage"
f1.keywords:
- NOCSH
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 09/16/2024
audience: Admin
ms.topic: concept-article
ms.service: viva-engage
ms.collection: magic-ai-copilot
ms.localizationpriority: medium
search.appverid:
- MET150
- MOE150
- YAE150
description: "Microsoft Copilot 365 in Viva Engage and other features leverage AI Summarization"
---

# AI Summarization in Viva Engage

AI Summarization is a Viva Engage service that processes and stores conversation threads in the background. Certain features, such as Microsoft 365 Copilot in Viva Engage, require access to processed conversation threads to produce insights, trends, and other helpful information to users. When a feature requests summarized data, AI Summarization returns summaries from processed conversation threads to which the user has access.

The [data, privacy, and security guidelines](/viva/engage/manage-security-and-compliance/data-privacy-security-copilot-engage) that apply to Copilot also apply to AI Summarization. Processed conversation threads are stored in alignment with General Data Protection Regulation (GDPR) requirements and are accessed the same as other Viva Engage data.

## Which features use AI Summarization?

Copilot and Analytics (Networks, Conversation, and Audiences) use AI Summarization. Other Viva Engage features are likely to incorporate AI Summarization services in the coming year.

Network analytics draws upon stored summaries to derive network theme extraction, network sentiment analysis, and conversation summarization.

## How do I control AI Summarization?

By default, Viva Engage enables AI Summarization to process threads from all users in the network. Only premium users with a Microsoft Viva Suite license can access the summaries and enhancements that AI Summarization provides.

Engage admins can turn off AI Summarization for the entire network, or for select groups and individuals by [creating policies in PowerShell](/viva/feature-access-management#create-and-manage-access-policies-for-viva-features). You can have multiple user and group-level policies to control AI Summarization use. Network-level policies are limited to one per tenant.  

Policy settings apply anytime a user signs in, and determine which enabled features that user has access to. Because you can set multiple access policies, a user might be impacted by more than one policy. Individual user and group level policies always take priority over a tenant-level policy.

## Enablement states for AI Summarization

>[!NOTE]
>Changes to the AI Summarization control generally take effect within 24 hours.

|State| Functionality| In Copilot| In analytics|
|--------|------------|----------|-------------|
|**Enabled** (Default)| Processes Engage threads within the tenant.|Enhances Copilot conversation starters on the Home page. Summarizations provide insights and recaps, and  posting suggestions based on network activity.|Required for sentiment analysis in Network analytics.|
|**Enabled with user opt out**|Provides the same functionality as **Enabled**, except that users who have access to AI Summarization can turn it off for their user account through the setting in their personal analytics.|If a user opts out, Copilot lacks summarization data for the network and is unable to provide insights and recaps, or posting suggestions based on network activity.|If an admin or corporate communicator opts out, they turn off sentiment analysis in Network analytics. If enough users opt out, the network may not meet the minimum required data for Network analytics.|
|**Disabled**|Stops all processing of Engage threads. If you disable AI Summarization for the tenant, without creating either a user or group enablement policy or a disabled tenant policy, all history data in the tenant is deleted retroactively. To prevent deletion of all summarization data, accompany this setting change with one of the aforementioned policies.|Disables Copilot conversation starters on the Home page and Copilot responses for posts and insights that require summarization posts across the network.|Disables all Network analytics (theme, sentiment analysis, and conversation summarization).|

## See also

[Data, Privacy, and Security for Microsoft 365 Copilot in Viva Engage](/viva/engage/manage-security-and-compliance/data-privacy-security-copilot-engage)

[Set up Microsoft 365 Copilot in Viva Engage](/viva/engage/configure-copilot-for-engage)
