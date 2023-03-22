---
title: "Answers admin scenarios in Viva"
description: "Describes administration of Answers in Viva Engage for the Microsoft 365 Global admin, Engage admin, and Answers admin."
ms.reviewer: ethli
ms.author: mamiejohnson
author: mamiepjohnson
manager: dmillerdyson
ms.date: 02/15/2023
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

# Answers admin scenarios in Viva

Administration of Answers involves the Microsoft 365 Global admin, the Engage admin, and a new role of the Answers admin. The new role of Answers admin is designated by [adding Knowledge Managers in Azure Active Directory](/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal?context=%2Fazure%2Factive-directory%2Froles%2Fcontext%2Fugr-context). All Knowledge Managers become Answers admins and have elevated permissions over end users. To better align the experiences of Viva Topics management and Answers administration, you can assign the same users that manage Viva Topics to manage Answers. More information see:
- [Assign a role to a group using Privileged Identity Management](/azure/active-directory/roles/groups-pim-eligible)
- [creating a role-assignable group in Azure AD](/azure/active-directory/roles/groups-create-eligible)  

## Permissions

The following table shows the range of actions available to users and admins.

|Answers actions|User not assigned Viva Engage Knowledge service plan|User assigned Viva Engage Knowledge service plan|Engage (Yammer) admin|Answers admin (Knowledge Manager)|Microsoft 365 Global admin|
|--------------------|-----------------|----------------|----------|------------|-----------|
|**Answer, upvote, and react to a question thread**|Questions they're mentioned in |✓|✓|✓|✓|
|**Receive notifications in the Viva Engage Teams app**|Questions they're mentioned in |✓|✓|✓|✓|
|**Ask a question**| |✓|✓|✓|✓|
|**Create a suggested topic for Answers**| |✓|✓|✓|✓|
|**Mark best answer**| | ✓ (own posts)|✓|✓|✓|
|**See global insights**| | |✓|✓|✓|
|**Delete and close posts**| | ✓ (own posts)|✓|✓|✓|
|**Feature topics**| | | |✓|✓|
|**Remove topic from Answers**| | | |✓|✓|
|**Approve suggested topics**| | | |✓|✓|
|**Enable answers**| | | | |✓|
|**Enable badges**| | |✓| |✓|

## Manage topics in Answers

### **Feature topics in Answers**

As an Answers admin, you can feature a topic or create a topic from the topic browse page. When you feature topics, you curate Viva Topics to be promoted for use in Answers.

> [!NOTE]
> The **Feature a topic** button is only isible to the Answers admin or Global admin.  

[![Screenshot of the Discover more Topics interface in Viva Engage.](/viva/media/engage/admin/feature-a-topic.png)](/viva/media/engage/admin/feature-a-topic.png#lightbox)

1. When you start to type the topic you want to feature, existing Viva Topics appear, and you can choose one to feature.  
[![Screenshot  of the editable summary for your topic in Viva Engage.](/viva/media/engage/admin/type-topic.png)](/viva/media/engage/admin/type-topic.png#lightbox)
2. After you select a topic to feature, you can edit the summary field that will be displayed as the short description of that topic in Answers. The summary helps people understand what the topic and whether it’s the appropriate topic to attach to their questions.

[![Screenshot of the editable summary for your topic in Viva Engage.](/viva/media/engage/admin/edit-topic-summary.png)](/viva/media/engage/admin/edit-topic-summary.png#lightbox)

>[!NOTE]
> The title and summary of all Viva Topics that are featured in Answers are visible to all licensed users who have access to Answers.

### **Review pending topics suggested by employees**

To ensure that topics suggested by employees are relevant and appropriate, there's a review process for Answers admin to follow. Answers admins have access to a fourth tab labeled **Needs Review** on the topic browse page. This tab is only visible to the Answers admin. It displays user-created or suggested topics. Any non-featured topic that is added to a question or created by the user shows up in this tab for a knowledge manager to review. Select **Review** on a topic to check and edit the summary.

[![Screenshot of the topics that need review in Answers in Viva.](/viva/media/engage/admin/needs-review-topic.png)](/viva/media/engage/admin/needs-review-topic.png#lightbox)

You can choose to feature the topic or ignore the topic, which removes it from the Review tab:  

- **Ignore**: When you ignoring a topic, it remains visible with the questions that it has been used with. But it won't become featured, which makes topics more prominent in the publisher’s topic picker.  
- **Feature**: When topics are featured, they no longer appear in the **Needs Review** tab.

[![Screenshot of the interface for reviewing a topic in Answers in Viva.](/viva/media/engage/admin/feature-reviewed-topic.png)](/viva/media/engage/admin/feature-reviewed-topic.png#lightbox)

**Remove topics in Answers**

To remove a topic in Answers, Answers admins (knowledge managers) follow these steps:  

1. Go to the browse topics page in Answers.
2. Select the ellipsis button on a topic, which prompts you to remove the topic in Answers.

   [![Screenshot of the Remove a topic button that admins see in the topic browse page in Answers in Viva.](/viva/media/engage/admin/remove-topic-hover.png)](/viva/media/engage/admin/remove-topic-hover.png#lightbox)

3. Once a topic is removed, it disappears from Answers and will no longer be associated with any questions where it was previously used.

   [![Screenshot of the interface and confirmation screen for removing a topic in Answers in Viva.](/viva/media/engage/admin/confirm-remove-topic.png)](/viva/media/engage/admin/confirm-remove-topic.png#lightbox)

>[!NOTE]
> When a topic is removed in Answers, you'll still be able to see the topic in the topic center. To remove the topic entirely, you can delete it directly in the topic center.

## View Global Answers analytics

As an Answers admin, you can access Global Answers analytics:
1. Selecting the analytics icon from the top navigation bar of Viva Engage.
1. Go to the Global Answers analytics tab.  You'll see a dashboard of analytics that provide an overview and relevant insights about knowledge sharing activity across Answers in Viva.

For more details about how to manage analytics in the [Engage admin center](/Viva/engage/eac-overview), see the comprehensive documentation for [viewing and managing analytics in Viva Engage](/Viva/engage/analytics) .

[![Screenshot of the Global Answers analytics dashboard in Viva Engage.](/viva/media/engage/admin/global-answers-analytics.png)](/viva/media/engage/admin/global-answers-analytics.png#lightbox)

The following metrics are available for Global Answers analytics:

- **Total time saved for your organization**: Total time the organization has saved based on question-and-answer usage.
- **Total questions**: Total number of questions asked by users.
- **Question views**: Total views across all questions
- **Total answers**: Total number of answers provided by users.
- **Total best answers**: Total answers marked as best answer.
- **Answer rate**: The ratio of questions that have answers to total questions.
- **Best answer rate**: The ratio of questions with best answers to total questions.
- **Median time to first answer**: The median time it takes for a question to receive its first answer.
- **Median time to best answer**: The median time it takes for a question to receive its first best answer.
- **Median questions asked per user**: The median number of questions asked by each user.
- **Median questions viewed per user**: The median number of questions viewed by each user.
- **Median answers per user**: The median number of answers provided by each user.
- **Median best answers per user**: The median number of best answers provided by each user.
- **Top questions across your organization**: A table of the top questions with the most views, votes, reactions, and answers across your org.
- **User engagement distribution**: A distribution of all users split by active engagements (ask, answer, vote, reactions, comments) and passive engagements (question views).

**Global time saved** shows the collective time saved across the organization. This total is based on Yammer research that shows each question-and-answer pair saves people an average of 15 minutes. As more people discover existing answers to their questions, the organization saves more time.

>[!NOTE]
> Analytics aren't live. They are updated every 24 hours.

## See also

[Answers in Viva: Frequently asked questions (FAQ)](/Viva/engage/eac-answers-faq)

[Rewards and recognition in Viva Engage](/Viva/engage/badges)

[Key admin roles and permissions in Viva Engage](/Viva/engage/eac-key-admin-roles-permissions)

[View and manage analytics in Viva Engage](/Viva/engage/analytics)
