---
ms.date: 11/15/2021
title: Restrict access to topics in Microsoft Viva Topics
ms.author: ruthhollands
author: ruthholls
manager: pamgreen
ms.reviewer: cjtan
audience: admin
ms.topic: article
ms.collection: m365initiative-viva-topics
ms.service: viva 
ms.subservice: viva-topics 
search.appverid:
    - MET150  
ms.localizationpriority: medium
description: Learn how to exclude topics to prevent them from being discovered in Viva Topics.

---

# Restrict access to topics in Microsoft Viva Topics

In Viva Topics, stakeholders in your organization might want to make sure that specific topics aren't discovered and exposed to your licensed users. For example, you might be working on a project that you don't want to expose any information about yet. While Microsoft 365 permissions on sites, files, and other resources will prevent users from viewing sensitive information in topics, there are additional safeguards to prevent specific topics from ever being discovered.

While knowledge admins control the settings to prevent topics from being discovered, knowledge managers and other stakeholders need to know how it is done so that they can work collaboratively.

> [!Important] 
> This article describes ways to prevent topics from being identified through AI or viewed in your environment as an additional security safeguard. It is important to note that in Viva Topics, users aren't allowed to view anything in a topic that they aren't allowed to access through Microsoft 365 permissions. Even if a user is able to view a topic, its files, sites, and pages they do not have Microsoft 365 permissions to view won't be visible to the user. Making sure that permissions to sensitive files are correctly set should be your primary security safeguard.

## Prevent topics from being identified

Knowledge admins can restrict access to specific topics by preventing them from being found in initial indexing. There are two ways to do this task in the Viva Topics admin settings in the Microsoft 365 admin center.
 
- [Select SharePoint sites to exclude from topic discovery](./topic-experiences-discovery.md#select-sharepoint-topic-sources): You can use this setting to prevent specific SharePoint sites from being crawled for topics.
- [Exclude topics by name](./topic-experiences-discovery.md#exclude-topics-by-name): Admins can use this setting to prevent specific topics from being discovered by name. In the Viva Topics admin settings, an admin can upload a list of topics to be excluded in a CSV file. You can exclude topics that have exact or partial matches of a topic name.

## Prevent topics from being viewed by specific users

Knowledge admins can also [select who can view topics in your organization](./topic-experiences-knowledge-rules.md). This setting lets you select which licensed users can view all topics. For example, in a pilot environment, you might want to only allow a small group of users to be able to view topics.

## Remove topics from being viewed

Knowledge managers can choose to [remove topics](./manage-topics.md) so that users can no longer see them. On the **Manage topics** page in the topic center, knowledge managers can choose to reject specific topics to prevent them from being viewed. Topics can be removed regardless if they are in a suggested or confirmed state.

Removed topics can later be added back as viewable topics if needed. 


## See also

[Security trimming in Viva Topics](topic-experiences-security-trimming.md)




