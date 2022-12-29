---
title: Manage Catalog Access
ms.author: bhaswatic
author: bhaswatic
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 12/28/2022
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.collection: 
    - enabler-strategic
    - m365initiative-viva-learning
localization_priority: medium
description: Learn how to manage catalog access in Microsoft Viva Learning.
---

# Manage Catalog Access in Viva Learning

All content available in Viva learning is discoverable by all users in the organization by default.  
Catalog access management allows you to restrict the ability of select users to view and discover courses. Organizations can control of a learning object is visible to a learning in Viva Learning. 

Depending on your integration with Viva Learning, there are two methods by which the organization can control the access permissions:

### Create and manage permissions within Viva Learning

Using the SAP SuccessFactors Learning Management System (LMS), organizations can set access permissions using assignment profiles. During the SuccessFactors  integration with Viva Learning, organizations can choose to enable a sync of permissions in SuccessFactors with Viva Learning 
Refer to the [Catalog permissions sync](https://learn.microsoft.com/en-us/viva/learning/configure-successfactors-content-source#catalog-permissions-sync) for detailed steps and requirements.

Once the sync is complete, Learning admins can view the courses for which permissions are applied within the Admin tab, by clicking **Manage Permissions** and then the **See View permissions** section below for further details.

## Configure in your EdCast portal

>[!NOTE]
>Your organization must have an active subscription to EdCast as well as a premium license for Microsoft Viva Learning.

You'll need Your EdCast API key, Secret, Client Host URL and User Email for Viva Learning to surface content from your EdCast instance.

1. Your organization's EdCast administrator can obtain your EdCast API key and Secret by reaching out to your dedicated EdCast Customer Success Manager.

2. Your Client host URL will be the same as your EdCast instance URL. It should look like "[subdomain].edcast.com".

## Configure in your Microsoft 365 admin center

>[!NOTE]
>You'll need to have admin permissions in Microsoft 365 to complete these steps.

1. Sign in to your [Microsoft 365 admin center](https://admin.microsoft.com).
2. Navigate to **Settings**, then **Org settings**. Select Viva Learning, and enable EdCast in the panel.
3. Fill in the configuration details that you got from your EdCast Customer Success Manager.
4. Select **Save** to activate EdCast content in Viva Learning. It may take up to 24 hours for the content to display in the Viva Learning app.
