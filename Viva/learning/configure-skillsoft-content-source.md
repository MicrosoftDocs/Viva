---
title: Configure Skillsoft as a content source for Microsoft Viva Learning
ms.author: bhaswatic
author: bhaswatic
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 06/28/2023
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - Tier1
localization_priority: medium
description: Learn how to configure Skillsoft as a learning content source for Microsoft Viva Learning.
---

# Configure Skillsoft as a content source for Microsoft Viva Learning

This article shows you how to configure Skillsoft as a third-party learning content source in Viva Learning. You'll need a Microsoft Viva Suite or Viva Learning license to add Skillsoft as a content source for your organization.

>[!NOTE]
>Content accessible through Viva Learning is subject to terms other than the Microsoft Product Terms. Skillsoft content and any associated services are subject to Skillsoft's privacy and service terms.

## Configure in your Skillsoft portal

You'll need to reach out to your Skillsoft account team to enable Viva Learning integration. Your account team will also provide you with the Organization ID and Service Account Key. You'll need these details for the next step.

You can contact [Skillsoft Support](https://support.skillsoft.com/percipio/) for help with getting in touch with your account team. If you aren't yet a customer, you can [contact Skillsoft directly](https://www.skillsoft.com/about/contact-us) to discuss your options.


## Configure in the Viva Learning Admin

> [!NOTE]
> You'll need to have M365 admin or Knowledge manager permissions in Microsoft 365 to complete these steps..

1. Open Viva Learning App in Teams or go to the Viva Learning [Web App](https://aka.ms/VivaLearningWeb)

2. Go to the **Admin** tab in Viva Learning and select **Manage Providers** on the left menu. Select **Add Provider** 

3. Select **Skillsoft** from list and select **Next**. 

3. Fill in the configuration details you got from your Skillsoft account team.
4.  Provide your region-specific information in **Data Center End Point URL**
    1. The US data center end point URL is: `api.percipio.com`
    1. The European data center end point URL is: `dew1-api.percipio.com`


5. Select **Save** to save the configuration details and complete the setup process. This will add the provider in the **Configured Providers** list.
1. You can track the current sync status, last successful sync time, next scheduled sync time, ingestion logs, and trigger full sync for each component in the expanded view.

1. It may take up to 24 hours for the content to display in the Viva Learning app.