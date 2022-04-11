---
title: "Share Dashboards"
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: <TBD>
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
localization_priority: Priority
ms.collection:  
- m365initiative-viva-goals
search.appverid:
- MET150

description: "Learn how to share dashboards and determine the privacy while sharing."
---

# Share Dashboards

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Dashboards can be created and shared across every level of the organization. To stay current on what’s happening in the company, and to foster transparency across teams, you can **share a dashboard across the entities – organization, team, and the user-level ones**.  

## How to share a dashboard?

- Navigate to the **Dashboards** page of your desired entity.

- On the top-right corner, select **Share**.

    > [!NOTE]
    > There are two access levels:
    >
    > - **Org-wide view access** — anyone in the organization can view the dashboard. In addition, you can determine who will have edit access to the shared dashboard.  
    > - **Private** — only specific users will have access to the shared dashboard. You can choose the level of access each user will have - view or edit access to the dashboard.

- Select the access level for the shared dashboard — either org-wide view access or private access.

- If you select org-wide view access, you can add users who can make edits to this dashboard. If you select private access, you can add users who can either have view-only access or edit access to the dashboard.

- Use the search box to start adding users, and against each user, you can determine the access level for the specified user.

## Organizational dashboard

:::image type="content" source="../media/goals/Share dashboards - org.gif" alt-text="Share Dashboards":::

## Team dashboard

:::image type="content" source="../media/goals/Share dashboards - team.gif" alt-text="Share Dashboards - Teams":::

## Individual dashboard

:::image type="content" source="../media/goals/Share dashboards - user.gif" alt-text="Share  Dashboards - User":::

### How do I revoke the access?

- Navigate to the **Dashboards** page of your desired entity.

- On the top-right corner, select **Share**.

- Select the access level from which you want to revoke the user-level access.

- Against the user, you will find a dropdown menu. Select **Remove** from this menu to revoke the access for the user.

    :::image type="content" source="../media/goals/Share dashboards - revoke access.gif" alt-text="Share dashboards":::

## Permissions

The applicable permissions can be categorized for two types of dashboards — default and user-created ones. Default dashboards is provided by Viva Goals across every level of the organization, while the user-created dashboards are created and maintained by the users for an organization, team, or an individual.  
  
| Permissions | Organization dashboard | Team dashboard | Individual dashboard |
|---------|---------|---------|---------|
| Permissions for default dashboards | <li>By default, everyone in the organization can view the dashboard, but cannot make edits to it unless they are allowed access.</li> <li>Only the org admin and org owner can view, edit, and share the dashboard.</li> | <li>By default, the team owners, team admins, org owners, and org admins can view, edit, and share the dashboard. </li> <li> All the team members can only view the team dashboard.</li> | <li>The user, org owners, and org admins can view, edit, and share the individual dashboard. </li> <li> Everyone else in the organization can only view the dashboard.</li> |
| Permissions for user-created dashboards | <li>The org owners and org admins can create new organizational dashboards. </li> <li> The respective dashboard owners can share the dashboard, while the view and edit access is determined based on the privacy set while sharing the dashboard.</li> | <li>The team owners, team admins, org owners, and org admins can create new dashboards for the team. </li> <li> Only the respective dashboard owners can share the team dashboard, while the view and edit access is determined based on the permissions granted while sharing the dashboard.</li>        | <li>The user, org owners, and org admins can create user-level dashboards. </li> <li> Either the individual or the org owners/admins can share the individual's dashboard.</li> |

> [!NOTE]
> Within a private dashboard, if you make check-ins on public Objectives and Key Results (OKRs), these check-in updates will still be visible to everyone in the organization from the OKR activity feed, owing to the fact that these are public OKRs.
