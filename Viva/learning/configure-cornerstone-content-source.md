---
title: Configure Cornerstone OnDemand as a content source for Microsoft Viva Learning
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
description: Learn how to configure Cornerstone OnDemand as a learning content source for Microsoft Viva Learning.
---

# Configure Cornerstone OnDemand as a content source for Microsoft Viva Learning

This article shows you how to configure Cornerstone OnDemand as a third-party learning content source in Viva Learning. First, enable Viva Learning and get your details from your Cornerstone Portal, and then configure the Viva Learning Admin tab.

A Microsoft Viva Suite or Viva Learning license is required to add Cornerstone OnDemand as a content source for your organization.

> [!NOTE]
> Content accessible through Viva Learning is subject to terms other than the Microsoft Product Terms. Cornerstone OnDemand content and any associated services are subject to Cornerstone OnDemand's privacy and service terms.

> [!NOTE]
> Viva Learning doesn't support the following content types from Cornerstone:
> - Events and Sessions 
> - Certifications
> - Question Banks 

## Configure in your Cornerstone Portal

1. Sign in to your Cornerstone Portal as an admin.

   ![Screenshot of the Cornerstone Portal.](../media/learning/csod-1.png)

2. Choose **Edge**.

   ![Screenshot of the Edge pane.](../media/learning/csod-2.png)

3. Go to **Marketplace** and search for Viva.

   ![Screenshot of the Marketplace.](../media/learning/csod-3.png)

4. Select the Viva Learning tile.

   ![Screenshot of the cursor hovering over the Viva Learning tile in the Marketplace.](../media/learning/csod-4.png)

5. Choose **Install**.

   ![Screenshot of the cursor hovering over the Install button after selecting the Viva Learning tile.](../media/learning/csod-5.png)

6. Check the box to confirm you agree to the Terms and Conditions, and choose **Install**.

   ![Screenshot of the Install screen with the Terms and Conditions box checked.](../media/learning/csod-6.png)

7. Select **Configure Now**.

   ![Screenshot of the installation popup with a button that says Configure Now on the right and one that says Later on the left.](../media/learning/csod-7.png)

8. Copy the Client ID, Secret, Portal name, and base URL. Then go back and search for Viva.

   ![Screenshot of the configuration screen where you can find your Client ID, Client Secret, Portal name, and Base URL.](../media/learning/csod-8.png)

9. Slide the toggle to enable Viva Learning integration.

   ![Screenshot of the Viva Learning integration toggle in the on position.](../media/learning/csod-10.png)

## Configure in the Viva Learning Admin tab

1. Open **Viva Learning App** in Teams or go to the Viva Learning [web app](https://aka.ms/VivaLearningWeb)

1. Go to the **Admin tab** in Viva Learning and select **Manage Providers** on the left menu. 

1. Select **Add Provider**. 

1. Select **Cornerstone OnDemand** from the Provider list and select **Next**. 

1. Fill in the following required configuration details:

  1. **Display Name**: This carousel lists the Cornerstone learning content for your organization in Viva Learning. If you don’t enter a name, the name “Cornerstone OnDemand” displays.
     > [!NOTE]
     > The display name is the name of the carousel that lists Cornerstone learning content for your organization in Viva Learning. If you don't enter a name, the default name "Cornerstone OnDemand" displays.
  1. **Client's Host URL**: This is the Base URL gathered from Cornerstone portal in step 8. If the Base URL is "https://integration-stg.csod.com", then the Client’s Host URL is "integration-stg.csod.com".
  1. **Client ID**: This is the Client ID gathered from Cornerstone portal in step 8.
  1. **Client Secret**: This is the Client Secret gathered from Cornerstone portal in step 8.

1. Select **Save** to activate Cornerstone content in Viva Learning. It may take up to 24 hours for the content to display in the Viva Learning app.
   - Once configured, Cornerstone configured providers list Cornerstone automatically. You can track the sync status and export sync log. 
   - You can edit or delete the configuration directly from manage provider as well. 

> [!IMPORTANT]
> **Guidance for Cornerstone Content Sync**: 
> To avoid confusion and potential issues with course visibility in Viva Learning, follow the correct procedure when setting up a Cornerstone provider for content sync:
>  - If test environment credentials are used initially, and later the source path is edited to the production (prod) environment, courses from both environments may appear in Viva Learning. 
>  - To ensure a seamless experience, add only a single instance of the desired environment. If both instances are added, delete both and then set up the desired environment to prevent any confusion or unintended content duplication. 

> [!NOTE]
> Currently, all the users within an organization can discover all the tenant-specific courses but are able to consume only the courses that they have access to. User-specific content discovery based on roles and permissions is planned for future releases.

> [!NOTE]
> Content Type Limitation: Viva Learning doesn't support the "Events and Sessions" content type from Cornerstone LMS.

## Learner record sync

Check **Enable Learner Record Sync** to enable assignments and course completion records to sync from the learning management system to Viva Learning. Users from your organization can see their assigned and completed courses from your LMS within Viva Learning.  

> [!NOTE]
> Ensure that user mappings between Cornerstone and Microsoft Entra ID are accurately configured, linking each user's identity correctly. 

By enabling Learner record sync, you allow Viva Learning to fetch user information, user assignments, and completed courses. The user information from the LMS is used only for user mapping and doesn't remain in storage. Only mapping-related information is deduced. Viva Learning fetches the following fields from the LMS:

- FirstName
- LastName
- Email
