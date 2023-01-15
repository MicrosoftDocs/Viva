---
title: "Answers admin scenarios in Viva Engage"
description: "Viva Engage is a new employee experience that connects people across the company—wherever and whenever they work—so that everyone is included and engaged."
ms.reviewer: ethli
ms.author: mamiejohnson
author: mamiepjohnson
manager: dmillerdyson
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

# Answers admin scenarios in Viva Engage

Administration of Answers will involve the Tenant admin, the Engage admin and a new role of the Answers admin. The new role of Answers admin will be designated by [adding Knowledge Managers in AAD](https://learn.microsoft.com/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal?context=%2Fazure%2Factive-directory%2Froles%2Fcontext%2Fugr-context). All Knowledge Managers will become Answers admins and will have elevated permissions over end users. To better align the experiences of Viva Topics management and Answers administration, you can assign the same users that manage Viva Topics to manage Answers. More information about assigning a [AAD role to a group](https://learn.microsoft.com/azure/active-directory/roles/groups-pim-eligible), or [creating a role-assignable group in Azure AD](https://learn.microsoft.com/azure/active-directory/roles/groups-create-eligible).  

## Permissions 

The table below shows the range of actions available to an unlicensed user, Viva Engage Knowledge service plan entitled user, Answers admin (AAD Knowledge Manager), Engage admin (Yammer administrator), and Office 365 (Global) admin. 

< Table of admin permissions >

## Admin actions in Answers

### Topics

**Feature topics in Answers**

As an Answers admin, you can feature a topic or create a topic from the topic browse page. Featuring a topic allows you to curate Viva Topics to be promoted for use within Answers.  

The **Feature a topic** button will only be visible to Answers admins or global admins.  

< image > 

1. When you start typing the topic you want to feature, existing Viva Topics will display, and you can choose one to feature.  

2. After you select a topic to feature, you can edit the summary field that will be displayed as the short description of that topic in Answers. The summary will help people understand what the topic is about and if it’s the appropriate topic to attach to their questions. 

>[!NOTE]
> All Viva Topics that are featured in Answers will have their title and summary visible to all licensed users with access to use Answers.  

< image >
 
### Review pending topics suggested by employees 

To ensure the topics suggested by employees are relevant and appropriate, there is a review process for Answers admin to follow. As an Answers admin, you have access to a fourth tab on the discover topics page labeled **Needs Review** on the topic browse page. The **Needs Review** tab is only visible to Answers admins and will display topics that have been user created or suggested. Any non-featured topic that is added on a question or created by the user will show up in this tab for a knowledge manager to review. You can select **Review** on a topic to check and edit the summary.  

If the topic is relevant and appropriate, then you can choose to feature the topic or ignore the topic, which will move the topic out of the Review tab.  

- **Ignore**: Ignoring the topic will allow the topic to still remain visible with the questions that it has been used with but it will not become featured - which makes a topic more prominent in the publisher’s topic picker.  
- **Feature**: When topics are featured, they will no longer appear in the **Needs Review** tab.  

< image > 

### Remove topics in Answers 

To remove a topic in Answers, Answers admin (Knowledge Managers) should complete the following steps:  

1. Navigate to the browse topics page and select the **All** tab. 
2. Select the ellipsis menu on a topic, which will prompt you to remove the topic in Answers. 
3. Once a topic is removed, it will disappear in Answers and will no longer be associated with any questions where it was previously used.  

>[!NOTE]
> Once a topic is removed in Answers, you will still be able to see the topic in the topic center. If you wish to remove the topic entirely, you can delete it directly in the topic center. 

< image > 

## See also 
[Answers in Viva Engage overview](https://support.microsoft.com/en-us/topic/getting-started-with-microsoft-viva-engage-729f9fce-3aa6-4478-888c-a1543918c284)
