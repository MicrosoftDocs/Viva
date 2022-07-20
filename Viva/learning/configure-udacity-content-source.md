---
title: Configure Udacity as a content source for Microsoft Viva Learning
ms.author: daisyfeller
author: daisyfell
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 7/11/2022
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.collection: 
    - enabler-strategic
    - m365initiative-viva-learning
localization_priority: medium
description: Learn how to configure Udacity as a learning content source for Microsoft Viva Learning.
---

# Configure Udacity as a content source for Microsoft Viva Learning

This article shows you how to configure Udacity as a third-party learning content source for Microsoft Viva Learning. You'll need an active Udacity license, as well as a Microsoft Viva Suite or Viva Learning license to add Udacity as a content source for your organization.

>[!NOTE]
>Content accessible through Viva Learning is subject to terms other than the Microsoft Product Terms. Udacity content and any associated services are subject to Udacity's privacy and service terms.

Eliminate your talent gaps in digital technologies like data science, ML, cloud, cybersecurity, and more. Create job ready talent to accelerate your most critical initiatives, unlocking innovation that fuels growth. [Learn more about Udacity](https://www.udacity.com/) and [see the full catalog here](https://enterprise.udacity.com/udacity-catalog).

## Configure in your Udacity portal

>[!NOTE]
>You'll need to have admin permissions in Udacity to complete these steps. You’ll also need an identity provider (IdP), as this integration uses SAML Single Sign-On (SSO) authentication.

1. Sign in to EMC.
2. Navigate to the **Settings** tab, then choose **API Tokens**, then select **Create New Token**.
3. Give your token a name and choose **Create**.
4. Copy your token. This is the only opportunity to copy or save your token.
5. You can generate multiple tokens and can validate or invalidate your tokens at any time by selecting **Invalidate Token**.
6. Request your company's Customer Company ID from your Udacity Customer Success Manager.
7. For more details, you can view [Udacity's PDF walkthrough guide](/download.microsoft.com/download/8/9/8/898ce39c-03b0-4c9b-88c0-a4da1c8435f6/EMC%20Catalog%20API-merged.pdf).

You can [contact Udacity Support](mailto:strategicalliances@udacity.com) for help with getting in touch with your Customer Success Manager. If you aren't yet a customer, you can [explore Udacity further here](https://www.udacity.com/enterprise/overview).

## Configure in your Microsoft 365 admin center

>[!NOTE]
>You'll need to have admin permissions in Microsoft 365 to complete these steps.

After you've received the required configuration details from Udemy portal by using the previous steps, the tenant admin needs to configure Udemy as a learning source in the Microsoft 365 admin center by using the following steps.

1. Navigate to the [Microsoft 365 admin center](https://admin.microsoft.com).
2. Navigate to **Settings**, then **Org settings**. Search for Viva Learning and enable Udacity in the panel.
3. Fill in the Udacity Customer Company ID you got from your Udacity Customer Success Manager or Implementation Specialist.
4. Select **Save** to activate Udacity content in Microsoft Viva Learning. It may take up to 24 hours for the content to display in the Viva Learning app.
