---
title: Error accessing Viva Connections app from Teams desktop client
description: Provides resolution for error message received when accessing the Viva Connections app from the Teams desktop client.
author: cloud-writer
ms.author: meerak
manager: dcscontentpm
audience: ITPro 
ms.topic: troubleshooting 
ms.service: viva
ms.subservice: viva-connections
localization_priority: Normal
ms.custom: 
- CI 159609
- CSSTroubleshoot
ms.reviewer: bpeterse
search.appverid: 
- MET150
---

# Error accessing Viva Connections app from Teams desktop client

## Symptoms

Your organization has followed the steps to set up and start Viva Connections. However, when you try to access the Viva Connections app from the Microsoft Teams desktop client, you receive the following error message:

> Something went wrong. We couldn’t sign you in. If the error persists, contact your system administrator and provide error code CAA20004.

When you select Additional problem information in the error message, you see the following details:

> AADSTS650057: Invalid resource. The client has requested access to a resource which is not listed in the requested permissions in the client’s application registration.

    :::image type="content" source="media/error-accessing-app-from-teams-desktop/error-accessing-app.png" alt-text="Screenshot of error message with additional information.":::

**Note:** This issue occurs only when you access the Viva Connections app from the Teams desktop client. You will not see this error if you access the Viva Connections app from the Teams web client.

## Cause

This error occurs if a SharePoint Framework (SPFx) web part is added to Viva Connections. Because of the web part addition, the **SharePoint Online Client Extensibility Web Application Principal** object that’s available under **Azure Active Directory** > **App Registrations** is not configured correctly to trust the Teams desktop client.

## Resolution

To resolve this issue, add the app ID for the Teams desktop client to the list of authorized client applications in Azure Active Directory:

1. Sign in to the [Azure portal](https://portal.azure.com/).
1. Select **Azure Active Directory** > **App Registrations**.
1. Select **SharePoint Online Client Extensibility Web Application Principal**.
1. Select **Expose an API**.
1. Select **Add a client application**.
1. Enter the Teams client app ID of 1fec8e78-bce4-4aaf-ab1b-5451cc387264 and a scope value of 1.

    :::image type="content" source="media/error-accessing-app-from-teams-desktop/add-app-id.png" alt-text="Screenshot of the Teams client app ID added to the list of authorized client applications.":::

1. Select **Add application** to save the app ID.
