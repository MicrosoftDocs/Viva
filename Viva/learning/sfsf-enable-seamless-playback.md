---
title: Enable seamless playback
ms.author: bhaswatic
author: bhaswatic
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 10/05/2023
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
description: Enable seamless playback to play SAP SuccessFactors courses in Viva Learning.
ROBOTS: NO INDEX, UNFOLLOW
---

# Enable seamless playback

Viva Learning and SAP SuccessFactors integration allows seamless authentication (SSO) and browser optimized playback. 

Browser optimized playback is enhanced for Teams desktop and web. It loads the SuccessFactors embedded player.

SAP SuccessFactors doesn't provide support for embedded content player in mobile applications. When using the Teams mobile app, it loads the SAP SuccessFactors details page.

![Screenshot that shows the Azure Active Directory SSO integration with SAP SuccessFactors.](../media/learning/viva-learning-sfsf-sso-content-details-page.png)

Content classified by SAP SuccessFactors as **online** or **instructor-led with online** are enabled for browser optimized playback from Viva Learning. Content of other classifications loads the SAP SuccessFactors details page.

## Prerequisite for enabling SSO

Refer to the [Azure Active Directory (AAD) single sign-on (SSO) integration with SAP SuccessFactors](/azure/active-directory/saas-apps/successfactors-tutorial) article for configuration information on enabling in-app playback and SSO.

Ensure that the SSO configuration on AAD and SAP SuccessFactors is the same and that the user's sign in method on SAP SuccessFactors is set to "SSO."

Sign in to Teams and Windows with the same user account for consumption of SAP SuccessFactors content from Viva Learning.

You may encounter a "refused to connect" error or a blank screen the first time you consume SAP SuccessFactors content inline within Viva Learning. The content plays successfully on subsequent content launches, however. To resolve this issue, refer to the SAP Knowledge Base Article - [2169861](https://userapps.support.sap.com/sap/support/knowledge/en/2169861).

> [!NOTE]
> If the SSO on both AAD and SAP SuccessFactors are already configured in the tenant, as described in the above documentation, then no action is required.

## Prerequisite for enabling browser optimized playback

Ensure that you configure and enable SSO between AAD and SAP SuccessFactors before enabling browser optimized playback. Enabling browser optimized playback without enabling SSO prevents consumption of SAP SuccessFactors content.

### Permissions required for the admin role in SAP SuccessFactors

To establish the integration and enable customers to consume SAP SuccessFactors content from Viva Learning, SuccessFactors admins need the following permissions for the SuccessFactors API (Viva Learning would only access the catalog-service SuccessFactors API).

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

Navigate to **Manage Providers** within the Viva Learning admin tab. Select **SuccessFactors** and then **Enable browser optimized playback.**

Provide the required configuration values to enable browser optimized playback. These values are obtained from SuccessFactors:

- Client's admin user ID

- Admin client secret

- Client ID

Once these three values are saved, they're used to execute the SuccessFactors catalog service API. This will further enable browser optimized playback for SuccessFactors content. Once these configurations have been provided, it takes 24-36 hours to enable browser optimized playback for SuccessFactors content from Viva Learning.

> [!NOTE]
> Ensure that the launch method for the content which needs to played is not set to be launched in a new browser window.
