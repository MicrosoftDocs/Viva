---
title: Access the Viva Glint platform
description: Access Microsoft Viva Glint with a Microsoft Entra ID user account and review supported browsers and session timeout information.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: platform, access, session, browser, glint access
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/30/2024
---

# Access the Viva Glint platform

Access Microsoft Viva Glint with a Microsoft Entra ID user account and review supported browsers and session timeout information.

## Select a supported browser

Glint users access surveys and dashboards with various internet browsers. Use this information to verify that your preferred browser is supported for accessing Glint.

> [!IMPORTANT]
> All users must access Glint from a browser that supports TLS 1.2, which includes the latest versions of Microsoft Edge, Google Chrome, Safari, and Mozilla Firefox.

|Browser  |Survey  |Dashboard|
|----------|-----------|------------|
|Microsoft Edge     |Supported       |Supported        |
|Google Chrome   |Supported       |Supported        |
|Safari     |Supported       |Supported        |
|Mozilla Firefox |Supported       |Supported        |
|iOS - Safari (Mobile)     |Supported       |Supported        |
|Android - Chrome (Mobile)|Supported       |Supported        |

> [!IMPORTANT]
> Internet Explorer isn't a supported browser.

## Access with a Microsoft Entra ID user account

Your Entra or other IT admins choose [authentication methods in Microsoft Entra ID](/entra/identity/authentication/concept-authentication-methods) for Glint and other resources. For example: username and password + multifactor authentication with an app like Microsoft Authenticator. Select a link based on the region that your organization's Glint tenant sits in and follow prompts to log in.

- US - [http://app.us1.glint.cloud.microsoft](http://app.us1.glint.cloud.microsoft)
- EU - [http://app.eu1.glint.cloud.microsoft](http://app.eu1.glint.cloud.microsoft)

## Session timeout

After 20 minutes of inactivity, you're prompted with an initial **Are you still here?** message. A Glint session ends after another 10 minutes inactivity.

:::image type="content" source="../../media/glint/setup/glint-inactive-session-message.png" alt-text="Screenshot of a message that appears when a user is inactive in their survey session.":::

## Connection issue

If you see a message indicating that a connection can’t be made to the Glint service, there's likely an issue with matching your information between the Glint application and Microsoft Entra ID. Contact your Glint or Entra admin to confirm that your data matches between systems.

:::image type="content" source="../../media/glint/setup/glint-mgr-no-connection.png" alt-text="Screenshot of a Viva Glint error message for a connection issue.":::
