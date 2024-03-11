---
title: Enable browser optimized playback
ms.author: bhaswatic
author: bhaswatic
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 03/05/2024
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
description: Enable browser optimized playback to play SAP SuccessFactors courses in Viva Learning.
---

# Enable browser optimized playback

Viva Learning and SAP SuccessFactors integration allows a browser optimized experience.

With this enhancement, learners can experience SuccessFactors content that are **online** and **instructor-led with online** within the SuccessFactors player. This opens SuccessFactors content in a browser tab without headers, footers, or navigation links.

> [!NOTE]
> Viva Learning launches the SuccessFactors content player in the browser. The content player is owned by SAP SuccessFactors.

SAP SuccessFactors doesn't provide support for embedded content player in mobile applications. When using the Teams mobile app, it loads the SAP SuccessFactors details page.

Browser optimized playback is enhanced for Teams desktop and web. It loads the SuccessFactors embedded player.

> [!IMPORTANT]
> - Only the content classified by SAP SuccessFactors as **online** or **instructor-led with online** are enabled for browser optimized playback from Viva Learning. Content of other classifications loads the SAP SuccessFactors details page.
> - For this experience to be available for content classified as **online** or **instructor-led with online** in SAP SuccessFactors, ensure that such content is part of a SuccessFactors library. This experience isn't enabled for content that isn't part of a SuccessFactors library.
> - Content with classification other than **online** or **instructor-led with online** in SAP SuccessFactors will load the SAP SuccessFactors details page and this experience is not applicable for content with such classifications.

## Prerequisite for enabling SSO

Refer to the [Microsoft Entra single sign-on (SSO) integration with SuccessFactors](/entra/identity/saas-apps/successfactors-tutorial) article for configuration information on enabling in-app playback and SSO.

Ensure that the SSO configuration on Microsoft Entra and SAP SuccessFactors is the same and that the user's sign in method on SAP SuccessFactors is set to "SSO."

Sign in to Teams and Windows with the same user account for consumption of SAP SuccessFactors content from Viva Learning.

You might encounter a "refused to connect" error or a blank screen the first time you consume SAP SuccessFactors content from Learning. The content plays successfully on subsequent content launches, however. To resolve this issue, refer to the SAP Knowledge Base Article - [2169861](https://userapps.support.sap.com/sap/support/knowledge/en/2169861).

> [!NOTE]
> If the SSO on both Microsoft Entra and SAP SuccessFactors are already configured in the tenant, as described in the above documentation, then no action is required.

## Prerequisite for enabling browser optimized playback

Ensure that you configure and enable SSO between Microsoft Entra and SAP SuccessFactors before enabling browser optimized playback. Enabling browser optimized playback without enabling SSO prevents consumption of SAP SuccessFactors content.

### Permissions required for the admin role in SAP SuccessFactors

To establish the integration and enable customers to consume SAP SuccessFactors content by launching the SuccessFactors content player from Viva Learning, SuccessFactors admins need the following permissions for the SuccessFactors API (Viva Learning would only access the catalog-service SuccessFactors API).

1. Search library

2. View library

Follow these steps to assign the required permissions to a role and assign that role to an admin in SAP SuccessFactors:

1. Create a role in comprised of the **Search library** and **View library** permissions.
    1. To create a new role, navigate to **System Administration** > **Security** > **Role Management** > **Create a new role** > enable **Search library** and **View library** permissions for the role. Or use an existing role, which has the two permissions already assigned.
2.  Assign the new role to an admin user.
    1. To assign a role to the admin user, navigate to **System Administration** > **Security** > **Administrator** > search for the admin > **Edit summary of an admin** > **Assigned Roles** > Add the created role.

### Properties required from SAP SuccessFactors


Follow the steps documented in the table to get the values of the required three properties from SAP SuccessFactors:

| Properties | Description |
| ---- | ----- | 
| Client’s Admin User ID | This admin user should have a role assigned to **Search Library** and **View Library** permissions assigned to execute the catalog service API successfully. Note, there's no need to provide any other permissions for this admin user in SuccessFactors.| 
| Admin Client Secret | The admin client secret is the generated client secret for the respective admin user. Navigate to **System Administration** > **Security** > **Administrator** and search for the admin.|
| Client ID | The client ID is required to execute the API. Navigate to **System Administration** > **Configuration** > **OAuth Token Server**.|

## Enable SAP SuccessFactors browser optimized playback

:::image type="content" alt-text="Screenshot of the Viva Learning integration with SAP SuccessFactors highlighting the browser optimized playback" source="/viva/media/learning/sfsf-browser-optimized-overview.png" lightbox="/viva/media/learning/sfsf-browser-optimized-overview.png":::


Navigate to **Manage Providers** within the Viva Learning admin tab. Select **SuccessFactors** and then enable the **browser optimized playback** toggle.

Provide the required configuration values to enable browser optimized playback. These values are obtained from SuccessFactors:

- Client's admin user ID

- Admin client secret

- Client ID

Once these three values are saved, they're used to execute the SuccessFactors catalog service API. This further enables browser optimized playback for SuccessFactors content. Once these configurations are provided, it takes 24-36 hours to enable browser optimized playback for SuccessFactors content from Viva Learning.

