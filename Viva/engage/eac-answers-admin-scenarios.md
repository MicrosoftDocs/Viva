---
title: "Answers admin scenarios in Viva"
description: "Viva Engage is a new employee experience that connects people across the company—wherever and whenever they work—so that everyone is included and engaged."
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

Administration of Answers will involve the Microsoft 365 Global admin, the Engage admin, and a new role of the Answers admin. The new role of Answers admin will be designated by [adding Knowledge Managers in AAD](/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal?context=%2Fazure%2Factive-directory%2Froles%2Fcontext%2Fugr-context). All Knowledge Managers will become Answers admins and will have elevated permissions over end users. To better align the experiences of Viva Topics management and Answers administration, you can assign the same users that manage Viva Topics to manage Answers. More information about assigning a [AAD role to a group](/azure/active-directory/roles/groups-pim-eligible), or [creating a role-assignable group in Azure AD](/azure/active-directory/roles/groups-create-eligible).  

## Permissions

The table below shows the range of actions available to an unlicensed user, Viva Engage Knowledge service plan entitled user, Answers admin (AAD Knowledge Manager), Engage admin (Yammer administrator), and Microsoft 365 Global admin.

|Answers actions|User not assigned Viva Engage Knowledge service plan|User assigned Viva Engage Knowledge service plan|Engage (Yammer) admin|Answers admin (Knowledge Manager)|M365 Global admin|
|--------------------|-----------------|----------------|----------|------------|-----------|
|**Answer, upvote, and react to a question thread**|Questions they are mentioned in |✓|✓|✓|✓|
|**Receive notifications in the Viva Engage Teams app**|Questions they are mentioned in |✓|✓|✓|✓|
|**Ask a question**| |✓|✓|✓|✓|
|**Create a suggested Topic for Answers**| |✓|✓|✓|✓|
|**Mark Best answer**| | ✓ (own posts)|✓|✓|✓|
|**See global insights**| | |✓|✓|✓|
|**Delete and close posts**| | ✓ (own posts)|✓|✓|✓|
|**Feature Topics**| | | |✓|✓|
|**Remove Topic from Answers**| | | |✓|✓|
|**Approve suggested Topics**| | | |✓|✓|
|**Enable Answers**| | | | |✓|
|**Enable Badges**| | |✓| |✓|

## Manage Topics in Answers

### **Feature topics in Answers**

As an Answers admin, you can feature a topic or create a topic from the topic browse page. Featuring a topic allows you to curate Viva Topics to be promoted for use within Answers.

> [!NOTE]
> The **Feature a topic** button will only be visible to Answers admin or Global admin.  

![Image of the Discover more Topics interface in Viva Engage.](/viva/media/engage/admin/feature-a-topic.png)

1. When you start typing the topic you want to feature, existing Viva Topics will appear, and you can choose one to feature.  
![Image of the editable summary for your topic in Viva Engage.](/viva/media/engage/admin/type-topic.png)
2. After you select a topic to feature, you can edit the summary field that will be displayed as the short description of that topic in Answers. The summary will help people understand what the topic is about and if it’s the appropriate topic to attach to their questions.

![Image of the editable summary for your topic in Viva Engage.](/viva/media/engage/admin/edit-topic-summary.png)

>[!NOTE]
> All Viva Topics that are featured in Answers will have their title and summary visible to all licensed users with access to use Answers.

### **Review pending topics suggested by employees**

To ensure the topics suggested by employees are relevant and appropriate, there's a review process for Answers admin to follow. As an Answers admin, you have access to a fourth tab labeled **Needs Review** on the topic browse page. The **Needs Review** tab is only visible to Answers admin and will display topics that have been user created or suggested. Any non-featured topic that is added on a question or created by the user will show up in this tab for a Knowledge Manager to review. You can select **Review** on a topic to check and edit the summary.

![Image of the Topics needing review in Answers in Viva.](/viva/media/engage/admin/needs-review-topic.png)

If the topic is relevant and appropriate, then you can choose to feature the topic or ignore the topic, which will move the topic out of the Review tab.  

- **Ignore**: Ignoring the topic will allow the topic to still remain visible with the questions that it has been used with but it won't become featured - which makes a topic more prominent in the publisher’s topic picker.  
- **Feature**: When topics are featured, they will no longer appear in the **Needs Review** tab.

![Image of the interface for reviewing a topic in Answers in Viva.](/viva/media/engage/admin/feature-reviewed-topic.png)

**Remove topics in Answers**

To remove a topic in Answers, Answers admin (Knowledge Managers) should complete the following steps:  

1. Navigate to the browse topics page in Answers.
2. Select the ellipsis button on a topic, which will prompt you to remove the topic in Answers.

![Image of the Remove a topic button admin will see in the topic browse page in Answers in Viva.](/viva/media/engage/admin/remove-topic-hover.png)

3. Once a topic is removed, it will disappear in Answers and will no longer be associated with any questions where it was previously used.

![Image of the interface and confirmation screen for removing a topic in Answers in Viva.](/viva/media/engage/admin/confirm-remove-topic.png)

>[!NOTE]
> When a topic is removed in Answers, you'll still be able to see the topic in the topic center. If you wish to remove the topic entirely, you can delete it directly in the topic center.

## View Global Answers analytics

As an Answers admin, you can access Global Answers analytics by selecting the analytics icon from the top navigation bar of Viva Engage, then navigating to the Global Answers analytics tab. You'll see a dashboard of analytics providing an overview and relevant insights on knowledge sharing activity across Answers in Viva.

For more details on how to manage analytics in the [Engage admin center](/Viva/engage/eac-overview), see the comprehensive documentation for [viewing and managing analytics in Viva Engage](/Viva/engage/analytics) .

![Image of the Global Answers analytics dashboard in Viva Engage.](/viva/media/engage/admin/global-answers-analytics.png)

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
- **Top questions across your organization**: A table with the top questions with the most views, votes, reactions, and answers across your org.
- **User engagement distribution**: A distribution of all users split by active engagements (ask, answer, vote, reactions, comments) and passive engagements (question views).

Global time saved shows the collective time saved across the organization. This is based on Yammer research that shows each question-and-answer pair can save people an average of 15 minutes. As more people discover existing answers to their questions, the organization saves more time.

>[!NOTE]
> Analytics are not live but are updated every 24 hours.

## See also

[Answers in Viva: Frequently asked questions (FAQ)](/Viva/engage/eac-answers-faq)

[Rewards and recognition in Viva Engage](/Viva/engage/badges)

[Key admin roles and permissions in Viva Engage](/Viva/engage/eac-key-admin-roles-permissions)

[View and manage analytics in Viva Engage](/Viva/engage/analytics)
