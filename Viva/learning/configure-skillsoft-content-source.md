---
title: Configure Skillsoft as a content source for Microsoft Viva Learning
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
description: Learn how to configure Skillsoft as a learning content source for Microsoft Viva Learning.
---

# Configure Skillsoft as a content source for Microsoft Viva Learning

This article shows you how to configure Skillsoft as a third-party learning content source in Viva Learning. You need a Microsoft Viva Suite or Viva Learning license to add Skillsoft as a content source for your organization.

>[!NOTE]
>Content accessible through Viva Learning is subject to terms other than the Microsoft Product Terms. Skillsoft content and any associated services are subject to Skillsoft's privacy and service terms.

## Configure in your Skillsoft portal

Contact your Skillsoft account team to enable Viva Learning integration. Your account team provides you with the Organization ID and Service Account Key for the next step.

For help with getting in touch with your account team, contact [Skillsoft Support](https://support.skillsoft.com/percipio/). If you aren't yet a customer, you can [contact Skillsoft directly](https://www.skillsoft.com/about/contact-us) to discuss your options.


## Configure in the Viva Learning Admin

> [!NOTE]
> You need M365 admin or Knowledge manager permissions in Microsoft 365 to complete these steps.

1. Open Viva Learning App in Teams or go to the Viva Learning [Web App](https://aka.ms/VivaLearningWeb).

1. Go to the **Admin** tab in Viva Learning and select **Manage Providers** on the left menu. Select **Add Provider**.

1. Select **Skillsoft** from list and select **Next**. 

1. Complete the fields with the configuration information you received from your Skillsoft account team.

1.  Provide your region-specific information in **Data Center End Point URL**.
   
    1. The US data center end point URL is: `api.percipio.com`.
    
    1. The European data center end point URL is: `dew1-api.percipio.com`.

1. Select **Save** to save the configuration details and complete the setup process, including adding the provider to the **Configured Providers** list.

1. You can track the current sync status, last successful sync time, next scheduled sync time, ingestion logs, and trigger full sync for each component in the expanded view.

1. For the content to display in the Viva Learning app may take up to 24 hours.
