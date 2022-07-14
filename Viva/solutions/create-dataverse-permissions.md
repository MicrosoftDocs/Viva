---
title: Step 3-Create Dataverse permissions
description: Learn how to create dataverse permissions
author: v-smandalika
ms.author: v-smandalika
ms.topic: article
ms.localizationpriority: medium 
search.appverid:
- MET150
ms.service: viva 
ms.subservice: viva-insights
ms.collection: 
- M365-analytics
- viva-insights
manager: dansimp
audience: Admin
---

# Step 3-Create Dataverse permissions

To create Dataverse permissions, perform the following steps:

1. Launch the URL https://admin.powerplatform.microsoft.com/environments. 
1. Select the environment for which you want to create Dataverse permissions.
1. Select **Users and permissions > Security Roles**.
   The following roles are the ones you can create:
    - **Basic User role (for access to User table and Yume tables)**: Updated to include user rights for tables. This role provides read-only access for the card data table and other rights for the other Yume tables.
    
      :::image type="content" source="../media/basic-user-role-permissions.png" alt-text="Basic permissions for a user role":::

    - **YumeContentAdmin (custom role)**: This role is permissive so should only be accounts that need access across all the data (for example, nudges from Power Automate).
        - Yume Cards::: Parent: Child Business Units
        - Yume Meeting Notes ::: Parent: Child Business Units
        - Yume User Options ::: Parent: Child Business Units
    
      :::image type="content" source="../media/yume-content-admin-role.png" alt-text="Yume content admin role":::