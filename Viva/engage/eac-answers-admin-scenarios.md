---
title: "Administrator scenarios for Answers in Viva Engage"
description: "Describes administration of Answers in Viva Engage for the Microsoft 365 Global admin, Engage admin, and Answers admin."
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 10/28/2023
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

Enablement of Answers requires a Microsoft 365 Global administrator. The Answers admin or an Engage admin can perform all other Answers administration tasks.

>[!NOTE]
> To assign an Answers admin, you must [add a Knowledge Manager in Microsoft Entra ID](/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal?context=%2Fazure%2Factive-directory%2Froles%2Fcontext%2Fugr-context). Knowledge managers become Answers admins.

To align Topics management and Answers administration, assign the same users that manage Topics to manage Answers. For more information, see:
- [Assign a role to a group using Privileged Identity Management](/azure/active-directory/roles/groups-pim-eligible)
- [Create a role-assignable group in Microsoft Entra ID](/azure/active-directory/roles/groups-create-eligible)  

## Permissions

The following table shows the actions available to users by role or service plan. All Engage admins, Answers admins, and Microsoft 365 Global admins are assigned Viva Engage Knowledge Service Plan, by default.

|Answers action|User not assigned Viva Engage Knowledge Service Plan|User assigned Viva Engage Knowledge Service Plan|Engage admin|Answers admin |Microsoft 365 Global admin|
|--------------------|-----------------|----------------|----------|------------|-----------|
|**Ask a question**|✓|✓|✓|✓|✓|
|**Answer, upvote, and react to a question thread**|Questions they're mentioned in |✓|✓|✓|✓|
|**View, upvote, and react to questions in one's community**|✓|✓|✓|✓|✓|
|**See related questions when composing a question in Answers or Communities**||✓|||✓|
|**Have your question appear in Answers' recommendations**| |✓|||✓|
|**Get question recommendations through email digests**|✓|✓|✓|✓|✓|
|**Receive notifications in the Viva Engage Teams app**|Questions they're mentioned in |✓|✓|✓|✓|
|**Create a suggested topic for Answers**| |✓|✓|✓|✓|
|**Mark best answer**| | ✓ (own posts)|✓|✓|✓|
|**Earn badges**||✓| | |✓|
|**Delete and close posts**| | ✓ (own posts)|✓|✓|✓|
|**See global insights**| | |✓|✓|✓|
|**See personal Answers analytics**|✓|✓|✓|✓|✓|
|**Update information panel**| | |✓|✓|✓|
|**Feature topics**| | | |✓|✓|
|**Remove topic from Answers**| | | |✓|✓|
|**Approve suggested topics**| | | |✓|✓|
|**Enable answers**| | | | |✓|
|**Enable badges**| | |✓| |✓|


## Update information panel

### Provide guidance using the information panel
As an Answers admin, Engage admin, or global admin, use the information panel to provide guidance to employees on how to use Answers in your organization. The information panel is only visible to administrators in its default state. After an admin saves and publishes the information panel, all other employees with access to Answers can see the information panel.

**Admin view**<br/>
:::image type="content" source="../media/engage/admin/ans-info-pan-admin1.png" lightbox="../media/engage/admin/ans-info-pan-admin1.png" alt-text="Screenshot of the information panel with guidelines option.":::

**User view**<br/>
The Answers tab only appears in Viva Engage for users assigned Viva Engage Knowledge Service Plan. Users not assigned Viva Engage Knowledge Service Plan can access Answers in the communities they belong to.
:::image type="content" source="../media/engage/admin/ans-info-pan-end-user.png" lightbox="../media/engage/admin/ans-info-pan-end-user.png" alt-text="Screenshot of how the information panel looks to end users.":::

### Edit the information panel
1. Select the edit icon from the top left corner of the information panel.
1. Enter the content specific to your organization.
1. Select **Save and publish** to allow all Answers users access to the information panel content.

:::image type="content" source="../media/engage/admin/ans-info-pan-admin2.png" lightbox="../media/engage/admin/ans-info-pan-admin2.png" alt-text="Screenshot of the editing options in the information panel.":::

### Reset the information panel  

1. Select the edit icon from the top left corner of the information panel.
1. Select **Reset** from the bottom-left corner.  

:::image type="content" source="../media/engage/admin/ans-info-pan-admin3.png" lightbox="../media/engage/admin/ans-info-pan-admin3.png" alt-text="Screenshot showing the information panel reset option.":::

### Provide guidance on the Answer user experience

Admins can set appropriate expectations of the Answers experience based on who receives the required Viva Engage Knowledge service plan assignment.

- Users assigned Viva Engage Knowledge Service Plan have a dedicated Answers tab with feeds of Answers-related activity and personalized questions. Their communities also include the Answers experience. Users can earn recognition for contributions and have access to Answers analytics. Each week they receive a digest summarizing questions and Answers activity in their Viva Engage Inbox.

- Users not assigned Viva Engage Knowledge Service Plan can post questions within their communities and react to questions others have posted. They can search all Answers content, and if their name is mentioned in an Answers-related post, they receive a notification.

## Manage topics in Answers

### Feature a topic in Answers

As an Answers admin, you can feature a topic or create a topic from the topic browse page. When you feature topics, you curate Topics to be promoted for use in Answers.

> [!NOTE]
> The **Feature a topic** button is only visible to the Answers admin or Microsoft 365 Global admin.  

:::image type="content" alt-text="Screenshot of the Discover more Topics interface in Viva Engage." source="/viva/media/engage/admin/feature-a-topic.png" lightbox="/viva/media/engage/admin/feature-a-topic.png":::

1. When you start to type the topic you want to feature, existing Topics appear, and you can choose one to feature.  

   :::image type="content" alt-text="Screenshot  of the editable summary for your topic in Viva Engage." source="/viva/media/engage/admin/type-topic.png" lightbox="/viva/media/engage/admin/type-topic.png":::

2. In the summary field of your selected topic, edit the description that appears with the topic in Answers. The summary helps people understand whether it’s the appropriate topic to attach to their questions.

   :::image type="content" alt-text="Screenshot of the editable summary for your topic in Viva Engage." source="/viva/media/engage/admin/edit-topic-summary.png" lightbox="/viva/media/engage/admin/edit-topic-summary.png":::

>[!NOTE]
> The title and summary of all Topics featured in Answers are visible to all licensed users who have access to Answers.

### Review a pending topic suggested by employees

To ensure that topics suggested by employees are relevant and appropriate, there's a review process for Answers admins to follow. Answers admins have a **Needs Review** tab on the topic browse page, which is only visible to them. The tab displays user-created or suggested topics. Any nonfeatured topic that's added to a question or created by the user appears on this tab for a knowledge manager to review.

- Select **Review** to review suggested topics for a category.

:::image type="content" alt-text="Screenshot of the topics that need review in Answers in Viva." source="/viva/media/engage/admin/needs-review-topic.png" lightbox="/viva/media/engage/admin/needs-review-topic.png":::

- In the **Take action** dialog, review and edit the summary as needed, or remove the topic.

:::image type="content" alt-text="Screenshot of the dialog that lets you review  and edit the topic summary or remove the topic from Answers." source="/viva/media/engage/admin/eac-answers-review-topic.png":::

After you review a topic, it no longer appears in the **Needs Review** tab. In addition, topics you remove from Answers no longer appear in any other experience in Viva Engage. To remove a topic completely, the admin must remove the topic from the [Topics management center](/microsoft-365/topics/topic-center-overview).
Removed topics no longer appears in the **Needs Review** tab or in any other experience in Viva Engage. To remove a topics completely, the admin must remove topics from the [Topics management center](/microsoft-365/topics/manage-topics).

### Remove a topic in Answers

To remove a topic in Answers, Answers admins can follow these steps:  

1. Go to the browse topics page in Answers.
2. Select the ellipsis button on a topic, which prompts you to remove the topic in Answers.

   :::image type="content" alt-text="Screenshot of the Remove a topic button that admins see in the topic browse page in Answers in Viva." source="/viva/media/engage/admin/remove-topic-hover.png" lightbox="/viva/media/engage/admin/remove-topic-hover.png":::
   
   When a topic is removed, it disappears from Answers and is no longer associated with any questions where it was previously used.

   :::image type="content" alt-text="Screenshot of the interface and confirmation screen to remove a topic in Answers in Viva." source="/viva/media/engage/admin/confirm-remove-topic.png" lightbox="/viva/media/engage/admin/confirm-remove-topic.png":::


>[!NOTE]
> After a topic is removed in Answers, you can still see the topic in the topic center. To remove the topic completely, the Answers admin (knowledge manager) must remove it from the [Topics management center](/microsoft-365/topics/manage-topics).

## View Global Answers analytics

As an Answers admin, you can access Global Answers analytics:
1. Select the analytics icon from the top navigation bar of Viva Engage.
1. Go to the **Global Answers analytics** tab. The analytics dashboard provides an overview and relevant insights about knowledge sharing activity across Answers in Viva.

For more information, see [View and manage analytics in Viva Engage](/Viva/engage/analytics).

:::image type="content" alt-text="Screenshot of the Global Answers analytics dashboard in Viva Engage." source="/viva/media/engage/admin/global-answers-analytics.png" lightbox="/viva/media/engage/admin/global-answers-analytics.png":::


The following metrics are available for Global Answers analytics:

| Metric | Description |
|---|---------|
|**Total time saved for your organization**|The amount of time the organization saved by using questions and answers|
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

[Manage administrator roles in Viva Engage](/Viva/engage/eac-key-admin-roles-permissions)

[View and manage analytics in Viva Engage](/Viva/engage/analytics)
