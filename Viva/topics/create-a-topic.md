---
ms.date: 11/15/2021
title: Create a new topic in Microsoft Viva Topics
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
ms.localizationpriority:  medium
description: Learn how to create a new topic in Microsoft Viva Topics.

---

# Create a new topic in Microsoft Viva Topics

In Viva Topics, you can create a new topic if one is not discovered through indexing or if the AI technology did not find enough evidence to establish it as a topic.

> [!NOTE]
> While information in a topic that is gathered by AI is [security trimmed](topic-experiences-security-trimming.md), note that topic description and people information in a manually created topic is visible to all users who have permissions to view the topic.

## Requirements

To create a new topic, you need to:

- Have a Viva Topics license.
- Have permissions to [**Who can create or edit topics**](./topic-experiences-user-permissions.md). Knowledge admins can give users this permission in the Viva Topics topic permissions settings.

> [!NOTE]
> Users who have permission to manage topics in the topic center (knowledge managers) already have permissions to create and edit topics.

## To create a topic

You can create a new topic from two locations:

- Topic center home page: Any licensed user with the **Who can create or edit topics** permission (contributors) can create a new topic from the topic center by selecting the **New** menu and select **Topic Page**.

    ![Screenshot of the topic center home page with Topic Page selected in the New menu.](../media/knowledge-management/new-topic.png)  

- **Manage topics** page: Any licensed user who has **Who can manage topics** permission (knowledge managers) can create a new topic from the **Manage topics** page in the topic center by selecting **New topic page**.

    ![Screenshot of the Manage topics page with New topic page selected.](../media/knowledge-management/new-topic-topic-center.png)  

### To create a new topic

1. Select the option to create a new Topic Page from the ribbon on the **Manage topics** page.

2. In the **Name this topic** section, type the name of the new topic.

    ![Screenshot of the Name this topic section.](../media/knowledge-management/k-new-topic-page.png)  

3. In the **Alternate Names** section, type any other names that the topic might be referred to.

    ![Screenshot of the Alternate names section.](../media/knowledge-management/alt-names.png)  

4. In the **Description** section, type a couple of sentences that describe the topic.

    ![Screenshot of the topic description section.](../media/knowledge-management/description.png)

5. In the **Pinned people** section, you can "pin" a person to show them as having a connection to the topic (for example, an owner of a connected resource). Begin by typing their name or email address in the **add a new user** box, and then select the user you want to add from the search results. You can also "unpin" them by selecting the **Remove from list** icon on the user card. You can also drag the person to another place in the list.

    ![Screenshot of the Pinned people section.](../media/knowledge-management/pinned-people.png)

6. In the **Pinned files and pages** section, you can add or "pin" a file or SharePoint site page that is associated to the topic.

   ![Screenshot of the pinned files and pages section.](../media/knowledge-management/pinned-files-and-pages.png)

    To add a new file, select **Add**, select the SharePoint site from your Frequent or Followed sites, and then select the file from the site's document library.

    You can also use the **From a link** option to add a file or page by providing the URL.

    > [!NOTE]
    > Files and pages that you add must be located within the same Microsoft 365 tenant. If you want to add a link to an external resource in the topic, you can add it through the canvas icon in step 8.

7. The **Related sites** section shows sites that have information about the topic.

    ![Screenshot of the related sites section.](../media/knowledge-management/related-sites.png)

    You can add a related site by selecting **Add** and then either searching for the site, or selecting it from your list of Frequent or Recent sites.

    ![Select site.](../media/knowledge-management/sites.png)

8. The **Related topics** section shows connections that exist between topics.

With the topic page in edit mode, you can add, edit, or remove connections in the Related Topics web part. You can only add or modify first-degree connections because modifying a second-degree connection would be tantamount to directly editing a different topic page, which we don't allow.

You can add a connection to a different topic by selecting the Connect to a related topic button, typing the name of the related topic, and selecting it from the search results.

[IMAGE]

You can then give a description of how the topics are related. Select **Update**

[IMAGE]

The related topic added will display as a connected topic.

When a connection between Topic A and Topic B is manually created on Topic Page A, the connection between these topics is represented as a suggested connection (dotted line) on Topic Page B. Representing this as a manual connection on Topic Page B would be equivalent to making a direct change to Topic Page B from Topic Page A, which is not allowed.

To remove a related topic, select the line segment corresponding to the topic you want to remove, then select the Remove relationship icon.

[IMAGE]

Dotted lines represent connections suggested by AI. Users can optionally confirm or remove these connections by selecting the line segment between two nodes.

[IMAGE]

9. You can also add static items to the page (such as text, images, or links) by selecting the canvas icon, which you can find below the short description. Selecting it opens the SharePoint toolbox from which you can choose the item you want to add to the page.

   ![Screenshot of the available canvas icons.](../media/knowledge-management/webpart-library.png) 

10. Select **Publish** to save your changes.

After you publish the page, the topic name, alternate name, description, and pinned people will display to all licensed users who view the topic. Specific files, pages, and sites will only appear on the topic page if the viewer has Microsoft 365 permissions to the item.
