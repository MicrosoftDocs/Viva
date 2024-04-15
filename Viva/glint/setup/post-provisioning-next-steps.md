---
title: Assign Viva Glint admins
description: Take care of assigning Viva Glint admins before you begin your first Viva Glint program journey.
ms.author: judithweiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: Add administrators to Viva Glint, Viva Glint sites, Viva Glint learning paths and modules, training
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 03/19/2024
---

# Assign Viva Glint admins

Welcome to Microsoft Viva Glint! If you have landed on this page, you should already have your tenant provisioned.

- If you haven't already completed tenant provisioning, [set up a Microsoft Viva tenant](viva-glint-tenant-provision.md).
- If you have completed tenant provisioning, follow these next steps to continue Viva Glint deployment:

   > [!IMPORTANT]
   > If you’re migrating from LinkedIn Glint, your M365 admin doesn’t need to assign Glint admins in MAC. Admin users are migrated to the Company Admin role as part of your technical migration to Microsoft Viva Glint.

## Assign Viva Glint admins in the Microsoft Administrator Center (MAC)

As the tenant Global Admin, you're the default Microsoft Viva Glint Service Admin. This means you have ultimate control over the subscriptions in your Viva Glint product and you can access all data. Additionally - **and importantly** - you can assign Viva Glint Service admin roles to other users.

:::image type="content" source="../../media/glint/setup/glint-admins-mac.png" alt-text="Screenshot of Viva Glint in the Microsoft Admin Center.":::

To assign admins:

1. Ensure that all Glint service admin users have their First Name, Last Name, Employee ID, and Email populated in Microsoft Entra. [Manage Entra user profile information](/entra/fundamentals/how-to-manage-user-profile-info).

   > [!IMPORTANT]
   > To prevent duplication errors with future file uploads, ensure that the Employee ID values for these users match the Employee ID from the HR Information System (HRIS) that will be used to transfer data to Viva Glint.

1. Sign in to the [Microsoft Admin Center (MAC)](https://go.microsoft.com/fwlink/?linkid=2264234). 
1. Go to **Settings** and select **Viva**.
2. In the list of applications, select **Viva Glint**.
3. Select **Assign Glint service admin** and choose **Add users**.
4. Search for and select service admin users.
5. Select **Add** to assign users.
6. Newly assigned users appear in the Viva Glint application in the Company Admin role within minutes.

> [!NOTE]
> - To add external users, like Partners or Viva Glint team members, use [Manage external users guidance](add-external-user.md).

## Ongoing Viva Glint admin additions

After initial admins are assigned in the Microsoft Administrator Center, Viva Glint admins can assign and unassign users to the Company Admin role. In the Viva Glint app, admins go to **configure**, select **People**, choose a user, and edit their **User Roles** to include **Company Admin**.

> [!NOTE]
> As a Viva Glint admin, use these steps to remove the M365 global admin from the Viva Glint Company Admin role if this user shouldn't have access to survey results.

## What do I do if I need help?

[Get support from Microsoft 365](/microsoft-365/admin/get-help-support?view=o365-worldwide&preserve-view=true)



