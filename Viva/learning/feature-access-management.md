---
title: Feature Access Management
ms.author: bhaswatic
author: bhaswatic
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 08/16/2023
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - Tier1
localization_priority: high
description: See what LinkedIn Learning courses are available on Viva Learning without a premium LinkedIn subscription.
---

# Delegate admin access in Viva Learning


Global admins and knowledge admins can now delegate access to non-admin users for managing features on Viva Learning admin tab.

This can be done using M365 groups. Any user who is part of M365 group assigned to a specific feature will get the feature access in their Viva Learning admin tab.

## Prerequisites

Manage Feature Access is available for global admins and knowledge admins who have a Viva Suite or Viva Learning license.

## Manage Feature Access in Viva Learning

After a global admin or a knowledge admin delegates access using Microsoft 365 groups, users within these groups can edit, update, and delete access for features similarly to a default admin.

Delegated access can be revoked by removing the group from **Edit Feature Access.**

Note: You can create or manage the M365 groups using the [Microsoft Admin Center](https://learn.microsoft.com/microsoft-365/admin/create-groups/manage-groups?view=o365-worldwide)

To manage feature access:

1. Select the edit icon on the feature where you want to add, edit, or delete access.
2. This opens the **Edit feature access** window.
3. Add or delete the Microsoft 365 groups in **Edit feature access**.
4. Select **Save**.

The delegation access changes take place immediately in Viva Learning. The default admin roles continue to have access to the admin features and can’t be revoked.

> [!NOTE]
> The Microsoft 365 group has to be a part of both Learning path and Featured set to also get access to Academies.
