---
title: Add the Viva Topics app in the Teams Admin Center
ms.author: ruthhollands
author: ruthholls
manager: pamgreen
ms.reviewer: cjtan
audience: admin
ms.topic: article
ms.collection: m365initiative-viva-topics
ms.service: viva 
ms.subservice: viva-topics 
search.appverid:
    - MET150  
ms.localizationpriority:  medium
description: Learn how to Add the Viva Topics app in the Teams Admin Center.
---

# Add the Viva Topics app in the Teams Admin Center

This article covers the steps to deploy the Viva Topics app, which is a custom app for Microsoft Teams. When the app is added to Teams, the Viva Topics icon will appear in the left navigation rail of Teams and will direct users to your organization's topic center.

The app is built using a PowerShell script provided by Microsoft.

You must be a SharePoint admin and a site owner for the topic center to create the Viva Topics app in PowerShell. You must be a Teams admin to upload and manage the app in the Teams Admin Center.

> [!NOTE]
> Viva Topics is not supported in the Teams mobile app.

## Create the manifest file

The Viva Topics app is provisioned by running a PowerShell script. The script creates an app manifest file which you then upload as an app in the Teams Admin Center. 

Download the [Viva Topics for desktop PowerShell script (Viva-Topics-Teams-Desktop-App.zip)](https://www.microsoft.com/download/details.aspx?id=103906) from the Microsoft download center. Note that Microsoft does not have access to any information provided by you while running this script.

Run the script and provide the following inputs:

- URL of your organization's topic center (starting with "https://"). 
- The name of the app as it should appear in Teams app bar. For example, "Viva Topics."
- App short description for the app which will appear in Teams app catalog. For example, "Access your topic center to see the topics relevant to you."
- App long description (4000 characters) which will appear in the Teams app catalog. For example, "Access your topic center to see the topics relevant to you, confirm your connections to topics, and keep your topics up to date."
- The privacy policy for custom Teams apps in your company (starting with https://). If you do not have a separate privacy policy, press Enter and the script will use the default Teams privacy policy from Microsoft.
- The terms of use for custom Teams apps in your organization (starting with https://). If you do not have separate terms of use, press Enter and the script will use the default Teams terms of use from Microsoft.
- Your organization name. This will be visible on the app page in Teams app catalog in "Created By" section.
- Your organization's public website (starting with https://). This will be linked to your company's app name on the app page in the Teams app catalog in "Created By" section.
- Icons: Default icons are provided in the zip file. When the script runs you can select to use the default icons or [provide your own](/microsoftteams/platform/concepts/build-and-test/apps-package#app-icons).

The script creates a Teams app manifest (.zip) file which you must upload in the Teams admin center.

## Upload the manifest file

To upload the app:
1. In the left navigation of the Teams admin center, go to **Teams apps** > **Manage apps**.
2. Click **Upload**, click **Upload**, and then select the manifest file and click **Open**.

Once the Viva Topics app package is successfully uploaded in the Teams admin center, it can be managed like any other app. You can configure user permissions to make this app available to a specific set of users. Permitted users can then find this app in Teams app catalog.

We highly recommend that you [pin this app by default for users in your organization](/microsoftteams/teams-app-setup-policies#pin-apps) so that they can easily access the topic center and the topics they are related to without having to discover the app in Teams app catalog.

## Related topics

[Set up Microsoft Viva Topics](/viva/topics/set-up-topic-experiences)

[Apps, bots, & connectors in Microsoft Teams](/microsoftteams/deploy-apps-microsoft-teams-landing-page)
