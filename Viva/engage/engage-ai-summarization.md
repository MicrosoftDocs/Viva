---
title: "AI Summarization in Viva Engage"
f1.keywords:
- NOCSH
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 08/02/2024
audience: Admin
ms.topic: concept-article
ms.service: viva-engage
ms.collection: 
 - magic-ai-copilot
ms.localizationpriority: medium
search.appverid:
- MET150
- MOE150
- YAE150
description: "Copilot in Viva Engage and other features use AI Summarization"
---

# AI Summarization in Viva Engage

AI Summarization is a Viva Engage service that processes and stores conversation threads in the Microsoft Viva Engage network to enable Copilot and analytics capabilities that require summarization.

Processed data from AI Summarization are stored in alignment with GDPR deletion requirements and are accessed the same as other Viva Engage data. AI Summarization is governed by the same [data, privacy, and security guidelines](Viva/engage/manage-security-and-compliance/data-privacy-security-copilot-engage) as Copilot in Viva Engage.

## Which features use AI Summarization?

AI Summarization is used in Network analytics, Conversation analytics, and Copilot in Viva Engage. When a feature requests summarized data, AI Summarization works in the background to return summaries from the relevant threads to which the user has access. Learn more about how Copilot and AI Summarization work together [in this diagram](/viva/engage/configure-copilot-for-engage#data-processing-and-storage).

Network analytics draws upon stored summaries to derive network theme extraction, network sentiment analysis, and conversation summarization.

## Control access to AI Summarization services

By default, Viva Engage networks enable AI Summarization to process threads for all users. However, only premium users with a Microsoft Viva Suite license can access the enhancements that AI Summarization provides.

Engage admins can turn off AI Summarization in the Viva [feature access management platform](/viva/manage-access-policies). From this platform, admins use access policies to control which users, groups, and networks have access to Viva Engage features. You can have multiple user and group policies for AI Summarization, but only one network policy is permitted per tenant.  

Policy settings apply anytime a user signs in, allowing the user access to all enabled features. Because you can set multiple access policies, a user might be impacted by more than one policy. Individual user and group level policies always take priority over a tenant-level policy. Learn how to [control access to other Viva features through policies](/viva/control-access-admin-center).

## AI Summarization enablement states

>[!NOTE]
>Changes to the AI Summarization control generally take effect within 24 hours.

|State| Functionality| In Copilot| In analytics|
|--------|------------|----------|-------------|
|**Enabled** (Default)| Processes Engage threads within the tenant.|Enhances Copilot conversation starters on the Home page. Summarizations provide insights and recaps, and  posting suggestions based on network activity.|Required for sentiment analysis in Network analytics.|
|**Enabled with user opt out**|Provides the same functionality as **Enabled**, except that users who have access to AI Summarization can turn it off for their user account through the setting in their personal analytics.|If a user opts out, Copilot lacks summarization data for the network and is unable to provide insights and recaps, or posting suggestions based on network activity.|If an admin or corporate communicator opts out, they turn off sentiment analysis in Network analytics. If enough users opt out, the network may not meet the minimum required data for Network analytics.|
|**Disabled**|Stops all processing of Engage threads. If you disable AI Summarization for the tenant, without creating either 1) a user or group enablement policy, or 2) a disabled tenant policy, all history data in the tenant is deleted retroactively.To prevent deletion of all summarization data, accompany this setting change with one of the aforementioned policies.|Disables Copilot conversation starters on the Home page and Copilot responses for posts and insights that require summarization posts across the network.|Disables all Network analytics (theme, sentiment analysis, and conversation summarization).|

## See also

[Data, Privacy, and Security for Copilot in Viva Engage](/viva/engage/manage-security-and-compliance/data-privacy-security-copilot-engage)

[Set up Copilot in Viva Engage](/viva/engage/configure-copilot-for-engage)
