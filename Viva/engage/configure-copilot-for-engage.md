---
title: "Overview and set up Copilot in Viva Engage [Public Preview] "
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 01/16/2024
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
>Copilot in Viva Engage is currently available through public preview. The features described here are subject to change. Administrators can enable Copilot in the Viva Engage admin center.

Copilot in Viva Engage is a partner for communicating in ways that create value for oneself and one’s organization. Copilot provides users access to Large Language Model (LLM) technology with Microsoft Responsible AI protections, to assist them to get the most out of Viva Engage. A large language model is a type of AI that can process and produce natural language text. Learn more about [responsible AI practices at Microsoft](/ai/responsible-ai). Copilot helps users get the most out of Viva Engage by suggesting where to engage and collaborating on writing communications.

[Learn more about Copilot in Viva Engage.](https://go.microsoft.com/fwlink/?linkid=2258512)

## Licensing requirements (Public preview)

Customers with a *Viva Suite* or *Communications & Communities* license, or a trial version of one of these, can opt in to activate Copilot through the Viva Engage admin center. Licensing requirements for these features may change after the preview period. Teams must be in Native Mode to support feature access.

>[!NOTE]
>[Microsoft 365 Copilot](/microsoft-365/enterprise/copilot-for-microsoft-365) is available separately.

## Data processing and storage 

:::image type="content" source="/viva/media/engage/admin/copilot-engage-dataflow.png" alt-text="Graph that shows how data flows between Copilot services while staying within the boundary of the Viva Engage app." lightbox="/viva/media/engage/admin/copilot-engage-dataflow.png":::

| Data process | How it works |
|---|---|
|**Message processing and storage for summarization**| The **Summarization** control starts background processing of Engage threads across the tenant network to support summarization features in Copilot. Copilot presents summaries *from only those posts to which the user already has access*. When Copilot is generally available, admin controls will allow enabling or disabling of summarization per user or group. Results from summarization and theme extraction are stored in alignment with GDPR deletion requirements. Use the [Engage Network Export feature](/Viva/engage/eac-as-manage-data.md#export-tenant-data-by-date-range) to export this data. | 
|**Processing of user commands to Copilot**|User interactions with Copilot during chat collaboration are currently processed, but not stored, with services aligned to Data center regional elections (US/EU Region). When Copilot in Engage is generally available, the system will support logging of Copilot chat input and output and admins will also have controls to enable/disable Copilot access per user group.|

## Configure Copilot for Viva Engage

Microsoft 365 Global administrators and Engage admins can control Copilot from the Viva Engage admin center. During public preview, Copilot is off by default.

When you enable Copilot, it’s available to all users in the tenant with a premium license. Teams must be in Native Mode to support feature access. Licensing requirements for these features may change after the preview period.

>[!NOTE]
>When Copilot is generally available in 2024, admins will be able to control Copilot for users or groups and set different policies for user groups.  Additional controls for AI summarization will enable the same.

1.	To enable Copilot, go to the [Viva Engage admin center](/Viva/engage/eac-as-access-eac).
1.	On the **Setup and configuration** tab, select **Manage analytics**.
    :::image type="content" source="/viva/media/engage/admin/admin-center-analytics1.png" alt-text="Screen shows Analytics settings in the Viva Engage admin center.":::
1. From the **Analytics and AI controls**, select the dropdown menu to turn on **Summarization**. Or, to allow users to turn off summarization in Viva Engage, select **On with user-level opt in/out**.
**Summarization** must be on to enable Copilot. This control starts the background processing of Engage threads across the tenant network to support summarization features in Copilot.
    :::image type="content" source="/viva/media/engage/admin/admin-center-copilot-crop2.png" alt-text="Screenshot shows Copilot controls within the Analytics and AI controls.":::

    >[!NOTE] 
    >Depending on the volume of data represented by Engage threads in your tenant, the summarization process may require anywhere from a few hours to a few days. If Engage threads aren’t processed, some aspects of Copilot won’t function optimally.

1. Use the toggle to turn on the **Copilot** control.

## How to access Copilot

Users can access Copilot from the Viva Engage Home page by selecting the Open Copilot link. 
When Copilot is generally available in 2024, users will be available to access Copilot within Viva Engage communities, campaigns, storyline, and articles.

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
