---
title: Use Microsoft 365 Groups permissions with SharePoint content in Viva Learning
ms.author: bhaswatic
author: bhaswatic
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 10/27/2021
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.collection: 
    - enabler-strategic
    - m365initiative-viva-learning
localization_priority: medium
description: Learn how to control access to SharePoint content in Viva Learning by using Microsoft 365 Groups.

---

# Use Microsoft 365 Groups permissions with SharePoint content in Viva Learning

Document library folder URLs can be collected from any SharePoint site in the organization. Viva Learning follows all existing content permissions. Therefore, only content for which a user has permission to access is searchable and visible within Viva Learning. Any content within these folders will be searchable, but only content to which the individual employee has permissions can be used.

>[!NOTE]
> While only **Microsoft 365** and **Mail-enabled security** group types are supported, it's recommended that you use a **Microsoft 365 Group.** Viva Learning doesn't support user-based permissions. Viva Learning won't ingest files that don't have associated Microsoft 365 Groups permissions.

1. Create a group by following the steps in [Create a group in the Microsoft 365 admin center](/microsoft-365/admin/create-groups/create-groups) to create groups in your Microsoft 365 admin center.

>[!NOTE]
> You'll need to add the owners as members in order for them to have access.

2. Go to the folder where you're storing learning content in SharePoint.
3. Select the vertical ellipses (**...**) on the item you want to control access to. If you want to control access to specific items in a folder, go to that folder.
4. Select **Manage access**.

    ![Screenshot of a folder selected in the learning content repository with the cursor hovering over Manage access.](../media/learning/sharepoint-manage-access.png)

5. Select the plus icon (**+**) next to **Direct access**.

    ![Screenshot of the plus icon selected next to Direct access in the Manage access options.](../media/learning/sharepoint-direct-access.png)

6. Start typing the email address of the group you want to give access to, then select the group.

    ![Screenshot of a group being selected in the Direct access pane.](../media/learning/sharepoint-group.png)

7. By default, users in the group are given Edit permissions. Select the pencil icon to choose between Edit and View permissions. The pencil icon will have a slash through it if the group has only view permissions. Users need a minimum of Can View permission.

    ![Screenshot of the pencil icon showing options for Can edit and Can view.](../media/learning/sharepoint-edit-view.png)

8. Select **Grant access** to give your group access to the learning content.

>[!NOTE]
> It will take approximately 24 hours for these changes to show up in the Viva Learning app.

To remove unintentionally surfaced content, follow these steps:

1. To restrict access to the document library, select the **Show actions** option, and then select **Manage access**.

     ![Document library page in SharePoint showing Show actions option with Manage access highlighted.](../media/learning/learning-sharepoint-permissions2.png)

2. Delete the original document within the document library.

For more information, see [Sharing and permissions in the SharePoint modern experience](/sharepoint/modern-experience-sharing-permissions).
