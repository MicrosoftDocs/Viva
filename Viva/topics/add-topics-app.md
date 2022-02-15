---
title: Add the Viva Topics app in the Teams Admin Center
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
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

This article covers the steps to deploy the Viva Topics app, which is a custom line of business app for Microsoft Teams and is built using PowerShell provided by Microsoft. This app includes the desktop experience only.

You must be a Teams admin to create the Viva Topics app in PowerShell and to apply the app in the Teams Admin Center.

> [!NOTE]
> Viva Topics is not supported in the Teams mobile app.

Download the Viva Topics for desktop PowerShell script (Viva-Topics-Teams-Desktop.zip) from the Microsoft download center.

The Viva Topics app is provisioned by using PowerShell and is uploaded as an app in the Teams Admin Center. The Viva Topics icon will appear in the left navigation rail of Team and will direct users to your organization's topic center.


 
Install Instructions:

When you run this script, you will have to provide the following inputs:
- URL of your organization's topic center (starting with "https://"). 
- The name of the app as it should appear in Teams app bar. For example, "Viva Topics."
- App short description for the app which will appear in Teams app catalog. For example, "Access your topic center to see the topics relevant to you."
- App long description (4000 characters) which will appear in the Teams app catalog. For example, "Access your topic center to see the topics relevant to you, confirm your connections to topics, and keep your topics up to date."
- The privacy policy for custom Teams apps in your company (starting with https://). If you do not have a separate privacy policy, press Enter and the script will use the default Teams privacy policy from Microsoft.
- The terms of use for custom Teams apps in your organization (starting with https://). If you do not have separate terms of use, press Enter and the script will use the default Teams terms of use from Microsoft.
- Your organization name. This will be visible on the app page in Teams app catalog in "Created By" section.
- Your organization's public website (starting with https://). This will be linked to your company's app name on the app page in the Teams app catalog in "Created By" section.
- Icons: Default icons are provided in the zip file. When the script runs you can select to use the default icons or provide your own. The app requires two PNG icons which will be used to represent your app in Teams; a 192x192 pixel colored icon for Teams app catalog and a 32x32 pixel monochrome icon for Teams app bar.


The scrip creates a Teams app manifest (.zip file) which you must upload in the Teams admin center.


 
Viva Topics requirements:
•	Global navigation is enabled in SharePoint - It is recommended that global navigation is enabled and customized in the SharePoint app bar so that SharePoint resources appear in Teams.


Step-by-step guide to setting up Viva Topics app in Teams

Complete the following steps to enable Viva Topics app using SharePoint PowerShell:

1.	Topic Center home site: We highly recommend that you use your Topic Center home site as the default landing experience for your users in Teams.
2.	Create a Viva Topics app package in PowerShell: The SharePoint admin needs to download and run PowerShell script from the Microsoft download center to create the Viva Topics app package. Ensure that you are using the latest version of the SharePoint Management Shell tool before running the script.
 Important
o	SharePoint admin credentials are required to use SharePoint PowerShell.
o	The SharePoint admin who creates the Viva Topics app package needs site owner permissions (or higher) to the Topic Center.
o	If your tenant is using an older version of PowerShell, uninstall the older version and replace it with the most up to date version.
o	Icons need to be PNG files.
3.	Provide tenant and site information to create the package: Download the Viva Topics PowerShell script and provide the information below.
When you create a new package in PowerShell, you will be required to complete the following fields:
o	URL of your tenant's Topic Center: Provide the tenant's Topic Center URL starting with "https://". This site will become the default landing experience for the Viva Topics app in Teams.

o	Provide the following details when requested:
- Name: The name of your Viva Topics app package, as it should appear in Teams app bar.
- App short description (80 characters): A short description for your app, which will appear in Teams app catalog.
- App long description (4000 characters): A long description for your app, which will appear in Teams app catalog.
- Privacy policy: The privacy policy for custom Teams apps in your organization (needs to start with https://). If you do not have a separate privacy policy, press Enter and the script will use the default SharePoint privacy policy from Microsoft.
- Terms of use: The terms of use for custom Teams apps in your organization (needs to start with https://). If you do not have separate terms of use, press Enter and the script will use the default SharePoint terms of use from Microsoft.
- Company name: Your organization name that will be visible on the app page in Teams app catalog in "Created By" section.
- Company website: Your company's public website (needs to start with https://) that will be linked to your company's app name on the app page in Teams app catalog in "Created By" section.
- Icons: You are required to provided two PNG icons, which will be used to represent your Viva Topics app in Teams; a 192X192 pixel colored icon for Teams app catalog and a 32X32 pixel monochrome icon for Teams app bar. Learn more about Teams icon guidelines.
Note
Microsoft does not have access to any information provided by you while running this script.
4.	Upload the Viva Topics app package in the Teams Admin Center: Once you successfully provide the details, a Teams app manifest, which is a .zip file, will be created and saved on your device. The Teams administrator of your tenant will then need to upload this app manifest to Teams admin center > Manage apps.
Learn more about how to upload custom apps in Teams admin center.
5.	Manage and pin the app by default for your users: Once the Viva Topics app package is successfully uploaded in the Teams admin center, it can be managed like any other app. You can configure user permissions to make this app available to the right set of users. Permitted users can then find this app in Teams app catalog.
We highly recommend that you pin this app by default for users in your tenant so that they can easily access their company's Topic Center and the topics they are related to without having to discover the app in Teams app catalog. Use Teams app setup policies to pin this app by default in Teams app bar and then apply this policy to a batch of users.


## Related topics

[Set up Microsoft Viva Topics](/viva/topics/set-up-topic-experiences)

[Apps, bots, & connectors in Microsoft Teams](/microsoftteams/deploy-apps-microsoft-teams-landing-page)
