---
title: "Manage user privileges with view-only mode in Viva Engage (Private Preview)"
description: "View-only mode is a tool that Viva Engage admins can use to remove content creation privileges from  users when needed."
ROBOTS: NOINDEX, NOFOLLOW
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 05/17/2024
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: medium
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---
# Manage user privileges with view-only mode in Viva Engage (Private Preview)

>[!IMPORTANT]
>View-only mode for Viva Engage is currently available only for private preview customers. The features described here are subject to change.

Microsoft 365 Global admins, Engage admins, and network admins can use view-only mode to prevent a user from contributing content to the Viva Engage network.

## User experience in view-only mode

In view-only mode, an information banner appears at the top of the Viva Engage experience, and publisher and creation features are unavailable. Users assigned to view-only mode can continue to follow others, receive and manage notifications, view analytics, report conversations, and bookmark threads. Users can also view announcements and browse content in any Viva Engage app (desktop, web, mobile, Teams, Outlook, or SharePoint).

## Limitations of view-only mode

When a user is in view-only mode, they have **no access** to the following features in Viva Engage, regardless of where they access the app (desktop, web, mobile, Teams, Outlook, and SharePoint):

- Creation of new posts, comments, or replies to posts

- Editing capability on existing posts, comments, or replies

- Content sharing between storylines or communities (public or private)

## Manage users in view-only mode

Admins can set view-only mode from the Engage admin center. This control works by assigning specific users to view-only mode. Once assigned, a user remains in view-only mode until removed at the admin's discretion. Engage admins can add or remove view-only mode for a user at any time.

While view-only mode only affects the user's experience and privileges in Engage, users can still access linked SharePoint sites and files shared in Engage.

**To assign a user to view-only mode:**

1. Go to the [Viva Engage admin center](/viva/engage/eac-overview).

2. From the **Governance and compliance tab**, select the **View-only mode** option.

3. Select **Add a user**.

    :::image type="content" source="../media/engage/admin/eac-viewonlymode-fullscreen.png" alt-text="Screenshot shows the View-only mode list in the Engage admin center." lightbox="../media/engage/admin/eac-view-only-mode.png#lightbox":::

4. Use the search function to find and select the user name you want, and then confirm your selection.<br>

    The user's name appears in the list of users in view-only mode with the date the status was applied and the admin who applied the status.

**To unassign a user from view-only mode:**

- In the **View-only mode** list, select the trash icon next to the user's name.

>[!NOTE]
>When you add or remove a user to view-only mode, the feature doesn't send a notification or inform the user that their Viva Engage network access has changed. Therefore, admins must find another way to communicate this change to users if needed.

## Track activity in the Microsoft 365 user audit log

All activity from the view-only mode feature is available through the user audit logs, including:

- User ID of the user in view-only mode
- User ID of the admin who assigned the user to view-only mode or removed view-only status
- Date and time the user was placed in view-only mode or removed status
