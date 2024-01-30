---
title:  Manage external users in Viva Glint
description: Grant access to and remove Viva Glint Support users to assist in deployment, advanced insights analysis, and complex Support tasks
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: External user, partner, support, add user
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 01/30/2024
---

# Manage external users in Viva Glint

The Support User role is designed to grant the right permissions to external users, like Microsoft Partners, and allow Viva Glint Admins to quickly audit how many Support users have access to their Viva Glint application. Support users can assist in deployment, advanced insights analysis, and complex support tasks. 

> [!IMPORTANT]
> External support users must be added to Microsoft Entra ID as **members** *with a company email address* for your organization before you can add them to your Viva Glint HRIS.
>
> [Add and delete users in Microsoft Entra ID](https://go.microsoft.com/fwlink/?linkid=2252181)

## Add a Support or Partner user

To add a user:

1. From the admin dashboard, select the **Configure** symbol, then in *Employees*, choose **People**.
2. In the **Actions** dropdown menu, select **Add a Support User**.
3. Enter the First Name, Last Name, and Email on file in Microsoft Entra ID for this user.  
4. The **Company Admin User Role** will be selected by default and grants Support users the required level of access to assist in your Viva Glint account.

    > [!NOTE]
    > For Partner users, add the user to the Partner Employees User Role, as well.

5. Switch the **External user** toggle to **Yes** to flag external users within your organization.
6. Switch the **Grant user advanced configuration access** setting to **Yes** to allow Support users access to **Advanced Configuration** features.
7. Select **Add support user.**

> [!CAUTION]
> Users with access to Advanced Configuration settings can make changes to potentially sensitive areas of your Viva Glint configuration. For an Advanced Configuration overview, see [Understand Advanced Configuration options in Viva Glint.](https://go.microsoft.com/fwlink/?linkid=2240194)

## Remove a Support or Partner user

When an external user no longer needs access to your Viva Glint account:

1. From the admin dashboard, select the **Configure** symbol, then in **Employees**, choose **People**.
2. In the **Search People** field, enter the first and last name or email address of the user.
3. In the search results, select the desired user.
4. On the user's profile, select **Actions** and then **Delete User**.
5. In the dialog, select **Delete User.**

   > [!NOTE]
   > This cannot be undone.
