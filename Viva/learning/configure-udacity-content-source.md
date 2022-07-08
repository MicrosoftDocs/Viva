---
title: Configure Udacity as a content source for Microsoft Viva Learning
ms.author: daisyfeller
author: daisyfell
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 7/08/2022
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

Eliminate your talent gaps in digital technologies like data science, ML, cloud, cybersecurity, and more. Create job ready talent to accelerate your most critical initiatives, unlocking innovation that fuels growth. [Learn more about Udacity](https://www.udacity.com/) and [see the full catalogue here](https://enterprise.udacity.com/udacity-catalog).

## Configure in your Udacity portal

>[!NOTE]
>You'll need to have admin permissions in Udacity to complete these steps. You’ll also need an identity provider (IdP), as this integration uses SAML Single Sign-On (SSO) authentication.

You'll need to reach out to your Udacity Customer Success Manager or Implementation Specialist to enable integration with Viva Learning. They'll also provide your Udacity Customer Integration ID, which you'll need for the next step.

You can [contact Udacity Support](mailto:strategicalliances@udacity.com) for help with getting in touch with your Customer Success Manager. If you aren't yet a customer, you can [explore Udacity further here](https://www.udacity.com/enterprise/overview).

## Configure in your Microsoft 365 admin center

>[!NOTE]
>You'll need to have admin permissions in Microsoft 365 to complete these steps.

After you've received the required configuration details from Udemy portal by using the previous steps, the tenant admin needs to configure Udemy as a learning source in the Microsoft 365 admin center by using the following steps.

1. Navigate to the [Microsoft 365 admin center](https://admin.microsoft.com).
2. Navigate to **Settings**, then **Org settings**. Search for Viva Learning and enable Udacity in the panel.
3. Fill in the Udacity Customer Integration ID you got from your Udacity Customer Success Manager or Implementation Specialist.
4. Select **Save** to activate Udacity content in Microsoft Viva Learning. It may take up to 24 hours for the content to be available in Viva Learning.
