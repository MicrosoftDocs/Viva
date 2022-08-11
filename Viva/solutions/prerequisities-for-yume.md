---
title: Step 1-Prerequisites for setup of Yume
description: Learn about the prerequisites for the setup of Yume
author: v-smandalika
ms.author: v-smandalika
ms.topic: article
ms.localizationpriority: medium 
search.appverid:
- MET150
ms.service: viva 
ms.subservice: viva-insights
ms.collection: 
- M365-analytics
- viva-insights
manager: dansimp
audience: Admin
---

# Step 1 - Prerequisites for setup of Yume

To set up Yume, perform the following steps:

- [Download the Yume accelerator](#download-the-yume-accelerator)
- [Create an Azure AD Application registration](#create-an-azure-ad-application-registration)
- [Import the PowerApps Custom Connector](#import-the-powerapps-custom-connector)
- [Set working hours and days for users mailbox settings](#set-working-hours-and-days-for-users-mailbox-settings)

## Download the Yume accelerator

Download the Yume accelerator from the samples in the [VivaSolutions GitHub repository](https://github.com/microsoft/VivaSolutions/tree/main/Sample%20Solutions) from the server itself.

Another option is to clone this repository to your local machine and then download the samples in VivaSolutions GitHub repository.

## Create an Azure AD Application registration

Create an Azure Active Directory (Azure AD) Application registration by performing the following steps:

1. For the attribute **Name**, provide the value **vsol-yume-connector**.
1. Configure the following delegated permissions for the "Microsoft Graph" API:
    - Analytics.Read
    - MailboxSettings.Read
    - User.Read
    - Profile
1. Authenticate using the Web Redirect URL: https://global.consent.azure-apim.net/redirect
1. Create a client secret and make a note of its value.
1. Make a note of the Application ID (also known as the client ID).
   The value of the client secret and the client ID will be used during the PowerApps Custom Connector creation.

## Import the PowerApps Custom Connector

To import the PowerApps Custom Connector, perform the following steps:
1. Sign in to https://powerapps.microsoft.com.
1. Select **Data** (or **Dataverse**) on the left navigation menu.
1. Select **Custom connectors**.
1. Choose **+ New custom connector**.
1. For the **Connector name** field, enter **vsol-graph-analytics-connector**.
1. Select **Import**.
1. Select the *vsol-yume-connector.swagger.json* file and select **Open**. The **General** page that is displayed.
1. Leave all the values as is and select **Security**. The **Security** page is displayed.
1. On the **Security** page, perform the following substeps:
    1. For the **Client ID** field, enter the client ID (application ID) from the Azure AD application registration process.
    1. For the **Client secret** field, enter the client secret value from the Azure AD application registration process.
    1. For the Resource URL field, enter **https://developer.microsoft.com/graph/**.
    1. For the Scope field, leave the populated value as is.
    1. Select **Create connector** at the top-right of the menu-items bar.
    1. Select **Close** at the top-right of the menu-items bar. The connector should now be listed in the **custom connector** section.
1. Share the connector with the organization (as needed).

## Set working hours and days for users mailbox settings

We recommend the working hours and days to be set for the users who will be using the application for more accurate working hours calculations. For information on how to set working hours and days for user mailbox settings, see [Set-MailboxCalendarConfiguration](/powershell/module/exchange/set-mailboxcalendarconfiguration). If not set, a default value of 45 hours will be used.