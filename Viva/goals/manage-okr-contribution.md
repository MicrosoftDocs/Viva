---
title: Manage OKR contribution
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: 
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
description: "Learn how to customize your OKRs’ weight and contribution to fine tune your OKR scores."
---

# Manage OKR contribution

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## What is OKR contribution

Viva Goals’ OKR contribution feature provides users (objective owners and creators) more flexibility and customizability in specifying weights and measuring progress. Users will now be able to define and control contribution at the parent level. All the contributions add up to a total of 100% and objective owners/creators have an option to mark a child’s contribution as "fixed". This feature is available only for OKRs that've progress mode as **Updated via roll-up from key results**.

### How do I enable this feature?

OKR Weights & Contribution is an Enterprise-Only feature. If you want to use this feature, contact Microsoft Support to get this feature enabled.

### Who can manage contribution?

Users who have "edit" permissions for the OKR (including check-in owners) can edit the contributions of children.

### How to manage OKR contribution

You can set or edit your OKRs’ contribution from the **More actions** dropdown list. To do this task, perform the following steps:

1. Select the **Manage children’s contribution** option.

   :::image type="content" source="../media/goals/manage-contributions-of-children.gif" alt-text="Managing the contribution of children":::

   > [!NOTE]
   > You can also open the **Manage children's contribution** modal from the objective quick view by selecting the objective's title and also from the objective's detail view, as depicted in the following two images, respectively.
   > 
   > :::image type="content" source="../media/goals/manage-contribution.png" alt-text="Manage contribution - 1":::
   > 
   > :::image type="content" source="../media/goals/manage-contribution-2.gif" alt-text="Manage contribution - 2":::

   The **Manage contributions** dialog box is displayed.

2. Add or edit the contributions of the children (objectives, key results, or projects)

   :::image type="content" source="../media/goals/add-or-edit-contributions-of-children.png" alt-text="Adding or editing the contributions of the children":::

   > [!NOTE]
   > You can also enable or disable the **New children should start contributing by default** toggle. By enabling this toggle (which is enabled by default), you'll allow a newly created child to contribute to the parent. This enablement will readjust the contributions you’d have assigned to each child.

3. Select **Save** to save all the changes.

### Key points to note

1. OKR contribution is available only for OKRs that have progress mode as **Updated via roll-up from key results**.
1. All the contributions will add up to a total of 100%. The default contribution is automatically assigned by Viva Goals to all the children equally. For example, if an objective has three key results (children), the default contribution assigned to each child will be 33.33%.
1. As soon as a child’s contribution is edited, the contribution is considered as “fixed”. This rule means, if a new child gets added or if an existing child gets removed, the contributions marked as "fixed" won't be adjusted. For example, if an objective has three key results (children), and the contribution of the first key result is edited as 50%, the contributions of second and third key results will be automatically adjusted to 25% each. In future, if there's a fourth key result that gets added, only the contribution of the second and third key results will be adjusted.
1. You can also reset all the custom contributions to default by selecting the **Reset to default** option.

If you've an enterprise subscription and would like to get this subscription enabled for your organization, ask your account administrator to reach out to **support@ally.io** with the request.
