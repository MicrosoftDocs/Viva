---
title: Configure Go1 as a content source for Microsoft Viva Learning
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 11/30/2023
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - Tier1
ms.localizationpriority: medium
description: Learn how to configure Go1 as a learning content source for Microsoft Viva Learning.
---

# Configure Go1 as a content source for Microsoft Viva Learning

This article shows you how to configure Go1 as a third-party learning content source in Viva Learning. You need a Microsoft Viva Suite or Viva Learning license to add Go1 as a content source for your organization.

>[!NOTE]
>Content accessible through Viva Learning is subject to terms other than the Microsoft Product Terms. Go1 content and any associated services are subject to Go1's privacy and service terms.

Go1 provides access to thousands of courses from top content providers. [Learn more about Go1](https://www.go1.com/go1-microsoft-viva). Follow these steps to add Go1 as a learning source in Viva Learning.

## Configure in your Go1 portal

>[!NOTE]
>You'll need to have admin permissions in Go1 to complete these steps.

Follow these steps to create an app in your Go1 Portal. This app generates your API keys, which you can use to authenticate with Go1 and make requests to the API.

1. Sign in to your Go1 Portal as an administrator.

2. Select **Integrations** from the menu options.

3. Select **Developers**.
   
5. Select the **Create App** button.
   
7. Enter a name for the app, for example, _My-go1-viva-integration_.
   
9. Enter a callback URL, for example, _Mycompany.mygo1.com_.
    
11. Save the information you entered.

13. Your information is displayed with the Secret hidden. Select the ellipses (**...**), then select **View Secret** to display the Secret.
    
15. Copy the following values:

    - **Client's Host URL:** This is your Go1 Portal URL. If the Go1 Portal URL is _https://mycompany.mygo1.com_, then the Client's Host URL is _mycompany.mygo1.com_.
    - **Client ID:** You can find your ID in your Go1 Portal under the **Integrations/Developer** menu options.
    - **Secret:** You can find your Secret in your Go1 Portal under the **Integrations/Developer** menu options.

Learn more about [how to create a private developer's app for Go1](https://help.go1.com/en/articles/4642648-integrate-with-the-go1-api).

## Configure in the Viva Learning Admin tab

> [!NOTE]
> You must have M365 admin or Knowledge manager permissions in Microsoft 365 to complete these steps.

1. Open Viva Learning App in Teams or go to the Viva Learning [Web App](https://aka.ms/VivaLearningWeb).

2. Go to the **Admin** tab in Viva Learning and select **Manage Providers** on the left menu. Select **Add Provider**.

3. Select **Go1** from list and select **Next**. 

4. Add configuration details as applicable and select **Save** to add the provider to the Configured providers list. 

In the expanded view, track the current sync status, last successful sync time, next scheduled sync time, ingestion logs, and trigger full sync for each component.

The Viva Learning app may take up to 24 hours to display the content. 
