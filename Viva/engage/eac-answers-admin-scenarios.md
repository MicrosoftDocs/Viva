---
title: "Administrator scenarios for Answers in Viva Engage"
description: "Describes administration of Answers in Viva Engage for the Microsoft 365 Global admin, Engage admin, and Answers admin."
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 01/18/2024
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

# Administrator scenarios for Answers in Viva Engage

Administration of Answers is for the person assigned either a Microsoft 365 Global admin, Engage admin, or Answers admin role. To designate an Answers admin, [add a Knowledge Manager in Microsoft Entra ID](/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal?context=%2Fazure%2Factive-directory%2Froles%2Fcontext%2Fugr-context). All Knowledge managers become Answers admins and have elevated permissions over end users. To better align the experiences of Topics management and Answers administration, you can assign the same users that manage Topics to manage Answers. For more information, see:

- [Assign a role to a group using Privileged Identity Management](/azure/active-directory/roles/groups-pim-eligible)
- [Creating a role-assignable group in Microsoft Entra ID](/azure/active-directory/roles/groups-create-eligible)  

## Permissions

The following table shows the actions available to users and admins. 

>[!NOTE]
>In the following table, _plan_ refers to the _Microsoft Viva Engage Knowledge Service plan_.

|Answers action|User not assigned a plan|User assigned a plan|Community admin|Engage admin|Answers admin|Global admin|
|--------------------|-----------------|----------------|----------|------------|-----------|----------|
|**Answer, upvote, and react to a question thread**|Questions they're mentioned in |✓|✓|✓|✓|✓|
|**Receive notifications in the Viva Engage Teams app**|Questions they're mentioned in |✓|✓|✓|✓|✓|
|**Ask a question**| |✓|✓|✓|✓|✓|
|**Create a suggested topic for Answers**| |✓|✓|✓|✓|✓|
|**Mark best answer**| | ✓ (own posts)|(in their community)|✓|✓|✓|
|**See global insights**| | | |✓|✓|✓|
|**Delete and close posts**| | ✓ (own posts)|✓|✓|✓|✓|
|**Update information panel**| | | |✓|✓|✓|
|**Feature topics**| | | | |✓|✓|
|**Remove topic from Answers**| | | | |✓|✓|
|**Approve suggested topics**| | | | |✓|✓| 
|**Enable answers**| | | | | |✓|
|**Enable badges**| | | |✓| |✓|

## Update information panel

### Provide guidance using the information panel
As an Answers admin, Engage admin, or global admin, use the information panel to provide guidance to employees on how to use Answers in your organization. The information panel is only visible to administrators in its default state. After an admin saves and publishes the information panel, all other employees with access to Answers can see the information panel.

**Admin view**<br/>
:::image type="content" source="../media/engage/admin/ans-info-pan-admin1.png" lightbox="../media/engage/admin/ans-info-pan-admin1.png" alt-text="Screenshot of the information panel with guidelines option.":::

**End user view**<br/>
:::image type="content" source="../media/engage/admin/ans-info-pan-end-user.png" lightbox="../media/engage/admin/ans-info-pan-end-user.png" alt-text="Screenshot of how the information panel looks to end users.":::

### Edit the information panel
1. Select the edit icon from the top left corner of the information panel.
1. Enter the content specific to your organization.
1. Select **Save and publish** to allow all Answers users access to the information panel content.

:::image type="content" source="../media/engage/admin/ans-info-pan-admin2.png" lightbox="../media/engage/admin/ans-info-pan-admin2.png" alt-text="Screenshot of the info panel editing options.":::

### Reset the information panel  

1. Select the edit icon from the top left corner of the information panel.
1. Select **Reset** from the bottom-left corner.  

:::image type="content" source="../media/engage/admin/ans-info-pan-admin3.png" lightbox="../media/engage/admin/ans-info-pan-admin3.png" alt-text="Screenshot showing the info panel reset option.":::

## Manage topics in Answers

### Feature topics in Answers

As an Answers admin, you can feature a topic or create a topic from the topic browse page. When you feature topics, you curate Topics to be promoted for use in Answers.

> [!NOTE]
> The **Feature a topic** button is only visible to the Answers admin or global admin.  

:::image type="content" alt-text="Screenshot of the Discover more Topics interface in Viva Engage." source="/viva/media/engage/admin/feature-a-topic.png" lightbox="/viva/media/engage/admin/feature-a-topic.png":::

1. When you start to type the topic you want to feature, existing Topics appear, and you can choose one to feature.  

   :::image type="content" alt-text="Screenshot  of the editable summary for your topic in Viva Engage." source="/viva/media/engage/admin/type-topic.png" lightbox="/viva/media/engage/admin/type-topic.png":::

2. After you select a topic to feature, you can edit the summary field that will be displayed as the short description of that topic in Answers. The summary helps people understand the topic and whether it’s the appropriate topic to attach to their questions.

   :::image type="content" alt-text="Screenshot of the editable summary for your topic in Viva Engage." source="/viva/media/engage/admin/edit-topic-summary.png" lightbox="/viva/media/engage/admin/edit-topic-summary.png":::

>[!NOTE]
> The title and summary of all Topics featured in Answers are visible to all licensed users who have access to Answers.

### Review pending topics suggested by employees

To ensure that topics suggested by employees are relevant and appropriate, there's a review process for Answers admins to follow. Answers admins have a **Needs Review** tab on the topic browse page, which is only visible to them. The tab displays user-created or suggested topics. Any nonfeatured topic that's added to a question or created by the user appears on this tab for a knowledge manager to review. Select **Review** on a topic to check and edit the summary.

:::image type="content" alt-text="Screenshot of the topics that need review in Answers in Viva." source="/viva/media/engage/admin/needs-review-topic.png" lightbox="/viva/media/engage/admin/needs-review-topic.png":::

You have options to feature or ignore the topic, which removes it from the **Review** tab:  

- **Ignore**: When you ignore a topic, it remains visible with the questions that it's been used with. But it won't get featured, which makes topics more prominent in the publisher’s topic picker.  
- **Feature**: When topics are featured, they no longer appear in the **Needs Review** tab.

:::image type="content" alt-text="Screenshot of the interface for reviewing a topic in Answers in Viva." source="/viva/media/engage/admin/feature-reviewed-topic.png" lightbox="/viva/media/engage/admin/feature-reviewed-topic.png":::

**Remove topics in Answers**

To remove a topic in Answers, Answers admins (knowledge managers) follow these steps:  

1. Go to the browse topics page in Answers.
2. Select the ellipsis button on a topic, which prompts you to remove the topic in Answers.

   :::image type="content" alt-text="Screenshot of the Remove a topic button that admins see in the topic browse page in Answers in Viva." source="/viva/media/engage/admin/remove-topic-hover.png" lightbox="/viva/media/engage/admin/remove-topic-hover.png":::


3. When a topic is removed, it disappears from Answers and is no longer associated with any questions where it was previously used.

   :::image type="content" alt-text="Screenshot of the interface and confirmation screen to remove a topic in Answers in Viva." source="/viva/media/engage/admin/confirm-remove-topic.png" lightbox="/viva/media/engage/admin/confirm-remove-topic.png":::


>[!NOTE]
> After a topic is removed in Answers, you can still see the topic in the topic center. To remove the topic entirely, you must delete it directly in the topic center.

## View Global Answers analytics

As an Answers admin, you can access Global Answers analytics:
1. Select the analytics icon from the top navigation bar of Viva Engage.
1. Go to the **Global Answers analytics** tab. The analytics dashboard provides an overview and relevant insights about knowledge sharing activity across Answers in Viva.

For more details about how to manage analytics in the [Viva Engage admin center](/Viva/engage/eac-overview), see [View and manage analytics in Viva Engage](/Viva/engage/analytics).

:::image type="content" alt-text="Screenshot of the Global Answers analytics dashboard in Viva Engage." source="/viva/media/engage/admin/global-answers-analytics.png" lightbox="/viva/media/engage/admin/global-answers-analytics.png":::


The following metrics are available for Global Answers analytics:

| Metric | Description |
|---|---------|
|**Total time saved for your organization**|Time the organization has saved based on question-and-answer usage|
|**Total questions**|Number of questions asked by users|
|**Question views**| Views across all questions|
|**Total answers**| Number of answers provided by users|
|**Total best answers**|Answers marked as best answer|
|**Answer rate**|The ratio of questions that have answers to total questions|
|**Best answer rate**| The ratio of questions with best answers to total questions|
|**Median time to first answer**|The median time it takes for a question to receive its first answer|
|**Median time to best answer**|The median time it takes for a question to receive its first best answer|
|**Median questions asked per user**|The median number of questions asked by each user|
|**Median questions viewed per user**| The median number of questions viewed by each user|
|**Median answers per user**| The median number of answers provided by each user|
|**Median best answers per user**| The median number of best answers provided by each user|
|**Top questions across your organization**|A table of the top questions with the most views, votes, reactions, and answers across your org|
|**User engagement distribution**|A distribution of all users split by active engagements (ask, answer, vote, reactions, comments) and passive engagements (question views)|
|**Global time saved** |Time saved across the organization. Based on Viva Engage research, this total shows that each question-and-answer pair saves people an average of 15 minutes. As more people discover existing answers to their questions, the organization saves more time.|

>[!NOTE]
> Analytics aren't live. They're updated every 24 hours.

## See also

[Answers in Viva: Frequently asked questions (FAQ)](/Viva/engage/eac-answers-faq)

[Key admin roles and permissions in Viva Engage](/Viva/engage/eac-key-admin-roles-permissions)

[View and manage analytics in Viva Engage](/Viva/engage/analytics)
