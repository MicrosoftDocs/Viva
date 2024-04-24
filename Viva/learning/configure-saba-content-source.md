---
title: Configure Saba as a content source for Microsoft Viva Learning
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 11/30/2023
audience: admin
ms.topic: article
ms.service: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - Tier1
ms.localizationpriority: medium
description: Learn how to configure Saba as a learning content source for Microsoft Viva Learning.
---

# Configure Saba as a content source for Microsoft Viva Learning

This article shows you how to configure Saba as a third-party learning content source for Microsoft Viva Learning. You must be a Saba System Admin or Super User to perform these steps. You'll need a Microsoft Viva Suite or Viva Learning license to add Saba as a content source for your organization.

>[!NOTE]
>Content accessible through Viva Learning is subject to terms other than the Microsoft Product Terms. Saba content and any associated services are subject to Saba's privacy and service terms.

>[!NOTE]
>Viva Learning integration with Saba will use APIs from your bucket of API calls per month and count towards your throttle limit.

## Configure in your Saba portal

>[!NOTE]
>You'll need to have admin permissions in Saba to complete these steps.

### Permissions

The account used for Saba setup must have the following security roles:

- **Learning Admin** - Catalog builder in the world domain*. 
    - To remove privileges to create or update courses, then make a copy of this security role and remove New and Edit privileges on Courses and other catalog objects. 
    
-	**Human Capital Admin** in the world domain*  
    - To remove privileges to create or update people records, make a copy of this security role and remove the New and Edit privileges on People and other HR objects.

*Or the highest domain that encompasses all learning you wish to send to Viva. 
 

### Client’s Host URL

1. Identify your primary Saba Cloud URL (for example "org".sabacloud.com). If your API dashboard URL is org-api.sabacloud.com, your Host URL will be org.sabacloud.com.
2. Identify your API Dashboard URL by going to **Saba Cloud** > **Admin** > **System Admin** > **Manage Integrations** > **API Dashboard**. Find the API Dashboard URL, then remove "https://" and "-api" to get your Host URL.

    ![Image of your API dashboard.](../media/learning/saba-a.png)

### Client ID and Client Secret

1. On the same screen where you got the host URL, copy the Client ID and Client Secret if they've already been generated.

2. If the Client Secret isn't there yet, select the **GENERATE** button to generate it.

    ![Image of the API dashboard with the cursor hovering over the Generate button.](../media/learning/saba-b.png)

## Configure in the Viva Learning Admin tab

>[!NOTE]
>You'll need to have admin permissions in Microsoft 365 to complete these steps.

1. Open **Viva Learning App** in Teams or go to the Viva Learning [web app](https://aka.ms/VivaLearningWeb)
2. Go to the **Admin tab** in Viva Learning and select **Manage Providers** on the left menu. 
3. Select **Add Provider**. 
4. Select **Saba** from the Provider list and select **Next**. 
5. Fill in the details that you got from your Saba portal.
    > [!NOTE]
    > Display name is the name of the carousel under which Saba learning content will appear for users in your organization in Viva Learning. If you don't enter a new name, it will display the default name "Saba Cloud".
6. Select **Save** to activate Saba Cloud content in Microsoft Viva Learning. It may take up to 24 hours for the content to display in Viva Learning.
7. Once configured, Saba will start appearing automatically in configured providers list. You can track the sync status and export sync log. 
8. You can edit or delete the configuration directly from manage provider.

> [!NOTE]
> For Saba Cloud integration, you need to have a sabacloud.com domain in your Host URL. If you have a different domain name, you'll need to raise a support ticket to allow your domain name.

> [!NOTE]
> Currently, all the users within an organization can discover all the tenant-specific courses but they will only be able to consume the courses that they have access to. User-specific content discovery based on roles and permissions is planned for future releases.

## Learner record sync

Select **Enable Learner Record Sync** to enable assignments and course completion records to sync from the learning management system to Viva Learning. Users from your organization will then be able to see their assigned and completed courses from your LMS within Viva Learning.  

By enabling this, you're allowing Viva Learning to fetch user information, user assignments, and completed courses. The user information from the LMS is only used for user mapping, and doesn't remain in storage. Only mapping-related information is deduced. Viva Learning fetches the following fields from the LMS:

- FirstName
- LastName
- Username

## Pre-requisite for enabling SSO

Refer to the [Azure Active Directory (AAD) single sign-on (SSO) integration with Saba Cloud](/azure/active-directory/saas-apps/saba-cloud-tutorial) topic for configuration information on enabling SSO.

Ensure that the SSO configuration on AAD and Saba is same and that the users login method on Saba is set to "SSO."

>[!NOTE]
> If the SSO on both AAD and Saba are already configured in the tenant, as described in the above documentation, then no action is required.
