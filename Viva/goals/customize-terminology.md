---
ms.date: 12/14/2023
title: Customize terminology in Viva Goals
ms.reviewer: 
ms.author: daisyfeller
author: daisyfell
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-goals
ms.localizationpriority: medium
ms.collection:  
- Strat_SP_modern
- M365-collaboration
- m365initiative-viva-goals
- vg-integration  
search.appverid:
- MET150
description: "Learn how to customize terminology in Viva Goals."
---

# Customize terminology in Viva Goals

Viva Goals allows admins to customize terminology using pre-defined lists of options so that the words used make sense to everyone in their organizations. Currently, the following terms can be customized:

* **OKR** can be changed to **Goal**.

* **Objective** can be changed to **Goal**, **Outcome**, **Theme**, or **Big Rock**.

* **Key Result** can be changed to **Metric**, **Outcome**, or **Result**.

* **Initiative** can be changed to **Project**, **To Do**, **Deliverable**, **Milestone**, or **Action**.

## Customize terminology at the tenant level

1. In the tenant admin settings, navigate to the **Custom Terminology** tab.

    ![Screenshot that shows a view of the Custom Terminology tab in tenant admin settings.](..\media\goals\customize-terminology\tenant-level-1.png)

1. In the table's **Current terms** column, choose the terms you would like to be used for all organizations in the tenant.

    ![Screenshot that shows an active drop-down menu in the Current terms column.](..\media\goals\customize-terminology\tenant-level-2.png)

1. Optional: Select **Preview** to see what goals will look like to users.

    ![Screenshot that shows a preview of how the selected terminology will look with real goals.](..\media\goals\customize-terminology\tenant-level-3.png)

1. Select **Save** to apply your changes to all organizations in the tenant.

    ![Screenshot that shows a Save changes dialog.](..\media\goals\customize-terminology\tenant-level-4.png)

    ![Screenshot that shows the new Goals terminology in the actual user experience.](..\media\goals\customize-terminology\tenant-level-5.png)

## Allow organization admins to customize their own orgs' terminology

Tenants with multiple organizations can choose to allow organization admins to customize terminology for their own orgs independently.

1. In the tenant admin settings, navigate to the **Custom Terminology** tab.

1. Turn on the toggle to allow organization admins to customize terminology at the org level.

    ![Screenshot that shows the custom terminology toggle turned on.](..\media\goals\customize-terminology\org-admin-1.png)

1. Saving your changes will allow org admins to customize Goals terminology for their organizations. The default settings for new organizations will continue to be the tenant settings.

> [!NOTE]
> Organization-level settings will always override tenant-level settings once customized.
>
> Revoking the ability to customize terminology at the organization level will cause all organizations to reset to the tenant defaults&mdash;even if those orgs already have their own terminology.

## Customize terminology at the organization level

1. Visit the **Custom Terminology** tab in the organization settings page (that is, the admin dashboard accessible by selecting the **Admin** tab in the left-hand nav, as shown below).

    ![Screenshot that shows the Custom Terminology tab in the admin dashboard.](..\media\goals\customize-terminology\org-level-1.png)

1. If the tenant allows individual organizations to customize their Goals terminology, you can select your preferred terms from the dropdown menus in the **Current terms** column.

## Frequently asked questions

### Can users enter their own terms, as opposed to choosing from preset options?

No. At present, users can only select from existing options: they can't add new ones.

### Which users can customize terminology?

At present, only administrators (tenant and organizational) can customize terminology.
