---
ms.date: 02/12/2024
title: Log in to or out of Viva Goals
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager: Liz.Pierce
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Learn how to log in to or out of Viva Goals."
---

Previously "log-in-create-and-join-organizations" (Ask Jim), then split into "log-in-to-or-out-of-viva-goals" and "create-or-join-an-organization".

# Log in to or out of Viva Goals

If your organization has purchased or subscribed to Viva Goals, anyone in the organization can log in to Viva Goals using their Microsoft Entra credentials. You don't need to log in if you're already logged in to another Microsoft 365 product or service.

## Log in to Viva Goals

1. Go to the Viva Goals sign-in page at https://goals.microsoft.com/.

1. Use your Microsoft Entra credentials to log in.

1. One of three/four <!--Editor's Note: Be sure to pick a number.--> things will happen next:

    * If there aren't any existing organizations for you in Viva Goals, you'll be directed to the **No organizations** page and prompted to [create an organization](create-or-join-an-organization.md).

    * If you're a first-time user invited to join your organization via an invite link, you'll be taken directly to your organization's Viva Goals account.

    * If you're logging in for the first time and aren't yet part of an organization, you'll be directed to the **Join Organizations** page to select your organization from a list.

    * If you're a returning user who's already part of an organization, you'll be taken to that organization. <!--Editor's Note: Is this different from the second option in any way other than the context?-->

## Log out of Viva Goals

Logging out of Viva Goals is simple: at the bottom of the left-hand nav, select **Account Settings** > **Log out**.










---
ms.date: 02/12/2024
title: Create or join an organization in Viva Goals
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager: Liz.Pierce
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Learn how to log in to Viva Goals and create or join organizations."
---

Previously "log-in-create-and-join-organizations" (Ask Jim)

# Create or join an organization in Viva Goals

Blah

## Create your first organization

1. [Log in](https://goals.microsoft.com/) to your Viva Goals account  using your Microsoft Entra credentials.

1. You'll be prompted to create an organization. Select **Create Organization**.

1. Enter your organization name and a brief description (optional) and select the organization type: **Public** or **Restricted**.

1. Select **Create Organization**.

As the organization administrator, you can now add users to your organization by inviting members.

## Create another organization

If you're a part of more than one organization and need to create another organization in Viva Goals, follow these steps:

1. Log in to your first organization in Viva Goals.

1. Select your organization's name at the top of the left-hand navigation menu.

1. At the bottom of the organization switcher dropdown that appears, select **Create or join organization**.

1. On the **Join organizations** page, hover over **Create new organization** and select **Create Organization**

1. Repeat the steps you followed to create your first organization.

Once you're a member of multiple organizations in Viva Goals, you can use the organization switcher dropdown to switch between different organizations.

## Join an organization

1. Log in to Viva Goals (https://goals.microsoft.com/) using Microsoft Entra ID.

1. If you're logging in for the first time and aren't yet a part of any organization, you'll be taken to the **Join Organizations** page, where you can select your organization.

1. If your organization is public, you'll see a **Join** button. Select that button to go to your organization's account.

   If your organization is restricted, you'll see a **Request to join** button. Select that button to send a join request to your organization administrator for approval.

1. Use the organization-switcher dropdown to join your other organizations.

1. Select **Create or join new organization**. On the **Join Organizations** page that opens, select the organization you want to join.

## FAQ

### What's an *organization* in Viva Goals and when should the user create it?

An organization in Viva Goals can mean different things to different users. You can create a single organization with all your employees in it if you have a simple hierarchy of organization-level OKRs, followed by department-level OKRs, and team-level OKRs. But in the following cases, it makes sense to create separate organizations:

* If your business unit (BU) or department wants to track a separate set of organization-level OKRs and align all the teams in that BU or department to those OKRs, you should create a separate organization for your BU or department.

* If your organization wants to maintain its own information boundary and doesn't want other department members to see its OKRs, you can create a separate organization for yourself or for those departments.

* If there's a need to administer the rollout and features separately, different departments may want to track OKRs in unique ways. You might want to turn on/off certain customizations or manage different OKR rhythms and cadences (different time periods) or permissions (transparent versus locked). In all these scenarios, it's best to create a new organization.

### What's the difference between an organization with the Public type and one with the Restricted type?

A *Public* organization is one that anyone in your company can join without needing approval. A *Restricted* organization lets you choose which users get to join; Restricted organizations are better when you want a tight-knit group of users to maintain information boundaries.
