---
title: Microsoft Viva Insights setup
description: Learn what's required to set up Microsoft Viva Insights 
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Set up advanced insights

Although the Microsoft 365 admin and the Viva Insights admin do most of these steps, others in your organization help make decisions that relate to setup.

**Prerequisites** - See [Environment requirements](/viva/insights/Setup/Environment-Requirements?toc=/viva/insights/advanced/toc.json&bc=/viva/insights/breadcrumb/toc.json) to learn about Viva Insights licenses and other related requirements.

## Setup steps

* Owner – The following key personas perform the setup steps in this article:
    * Viva Insights admin does most of the setup tasks and is the person referred to as "you" in the following steps.
    * Microsoft 365 admin assigns licenses and roles in Step 1.
    * Viva Insights processes and validates data in a few of the steps.

* Task – Complete steps to set up and configure the Viva Insights applications.

* Outcome – In your organization, people have been assigned licenses and roles. Those roles grant access to data that the people can use to analyze work habits and implement change in how employees spend their time. Also, you've set system defaults and privacy settings and an admin has uploaded organizational data.

## To set up the app

1. **Licenses and roles (required)**: Verify that your Microsoft 365 admin has assigned licenses and roles to people in the organization. For more information, see [Assign licenses](./assign-licenses.md) and [Assign roles](./assign-user-roles.md). The **Insights Administrator** role is required to perform the following steps.

2. **Privacy settings (optional)**:
    1. Set the **Minimum group size**.
    1. Select **Save changes**.

    After you've finished making both the system defaults and the privacy settings, select **Save changes**.
    
:::image type="content" source="../images/privacy-settings1.png" alt-text="Screenshot of the privacy settings page." lightbox="../images/privacy-settings1.png":::

3. **Prepare organizational data (optional)**: Export organizational data from your HR system into a UTF-8 encoded .csv file. For information about what data to export and how to structure it, see Prepare organizational data.
    1. Map data – Map the uploaded data to the applicable field names. For details, refer to [Field mapping](../admin/upload-org-data-first.md#field-mapping).
    1. Data validation – When the upload is validated, you'll see a confirmation message. If validation was not successful, you are advised what to do next. For details, refer to [Validation](../admin/upload-org-data-first.md#validation).
    1. Data processing – The validated data is processed. When the processing finishes, you'll see a message that setup is complete.

