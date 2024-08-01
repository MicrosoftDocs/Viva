---
title: Manage Catalog Access
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 05/30/2024
audience: admin
ms.topic: how-to
ms.service: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - Tier1
  - essentials-manage
ms.localizationpriority: medium
description: Learn how to manage catalog access in Microsoft Viva Learning to restrict the ability of select users to view and discover courses.
---

# Manage Catalog Access in Viva Learning

All content available in Viva Learning is discoverable by all users in the organization by default.  
Catalog access management allows you to restrict the ability of select users to view and discover courses. This process lets your organization control whether a learning object is visible to a learner in Viva Learning.

Depending on your integration with Viva Learning, there are two methods by which your organization can control the access permissions:

## Control permissions within the LMS

Organizers can use the SAP SuccessFactors Learning Management System (LMS) to set access permissions using assignment profiles. During the SuccessFactors integration with Viva Learning, you can choose to enable a sync of permissions in SuccessFactors with Viva Learning.
Refer to the [Catalog permissions sync](configure-successfactors-content-source.md#catalog-permissions-sync) article for detailed steps and requirements.

Once the sync is complete, admins can view the courses for which permissions are applied within the **Admin** tab, by clicking **Manage Permissions**. 
For more information, see the **View** permissions section.

## Create and manage permissions within Viva Learning

Use the Viva Learning permissions to restrict access to one or more learning objects to a select group of users 

>[!Note] 
>If you choose to control permissions using the LMS, then permissions can't be set within Viva Learning for courses coming from that LMS.

### Permissions Overview

![Image of the catalog permissions navigation screen under the admin tab.](../media/learning/catalog-access-permissions-1-landing-page.png)

When viewing permissions, you see the **title** of a learning object, the **provider** or source, and the associated **access** type and **permission source**.

There are two types of access: 

- **Private** access indicates that the access to a learning object is restricted.
- **Public** access indicates that there are no permissions associated with a learning object and that it's accessible within Viva Learning to everyone in the organization.

There are two types of permission sources:

- **Catalog provider** indicates that the permissions are coming from the LMS and you need to go to the LMS to views details of the permission.
- **Viva Learning** indicates that the permissions are set in Viva Learning. You can view, edit, or delete the permission by clicking the ellipses (**...**) next to it.



#### Add Permissions
You can select **Add permission** to create a new permission.

![Screenshot of the highlighted Add permissions button.](../media/learning/catalog-access-permissions-2-add-permissions.png)

You can search and choose a maximum of 10 courses on which to apply permissions.

![Screenshot of a popup window that lists options for adding new permissions.](../media/learning/catalog-access-permissions-3-add-new-permissions.png)

You can choose an existing Microsoft 365 group or Mail Enabled Security group. Refer to the support documentation to learn more about [Microsoft 365 groups](https://support.microsoft.com/office/learn-about-microsoft-365-groups-b565caa1-5c40-40ef-9915-60fdb2d97fa2) and [Mail Enabled Security groups](/exchange/recipients/mail-enabled-security-groups)


#### Permission Actions

![Screenshot displaying the various actions users can perform with permissions, including view, edit, and delete.](../media/learning/catalog-access-permissions-4-permissions-actions.png)

For learning objects with permissions created in Viva Learning, you have the following options.

- **View** the user groups that have access to the learning object.

- **Edit** to add or remove user groups that can access the learning object. 

- **Delete** to delete permissions created in Viva Learning. Once a permission is deleted, that learning object is accessible in Viva Learning by all users in the organization.

>[!Note]
> Permissions that originate from a catalog provider can't be deleted.
