---
title: Troubleshoot and resolve error messages
description: "Troubleshoot and resolve error messages"
ms.reviewer: 
ms.author: michellehu
author: michellehu-msft
manager: alisaliddle
audience: Admin
f1.keywords: NOCSH
ms.date: 03/08/2023
ms.topic: article
ms.service: viva
ms.localizationpriority: medium
ms.collection: m365initiative-viva-pulse  
search.appverid: MET150
---

# Troubleshoot and resolve error messages

> [!NOTE]
> This article applies to a preview version of Microsoft Viva Pulse. You must be in the Public Preview program to access it. See [Set up Viva Pulse Public Preview](./setup-admin-access/set-up-viva-pulse-public-preview-for-your-organization.md) to enable the Viva Pulse Public Preview for your organization and enable Teams Activity feed notifications for users in your tenant. Also, please note that customer support will only be available in English for Public Preview. Features are subject to change.

As you navigate the setup process in Viva Pulse, you might experience errors. The following table outlines the error messages you might see, a description of when they’re displayed, and the next steps you can take to resolve those errors. This is not an exhaustive list, and more error messages may be added in the future.

| Error Message | Where the error appears | How to fix it |
| ----------- | ----------- | ----------- |
| “We couldn’t delete [x] right now. Try again later.” | When the admin types in a person’s name to delete their Pulse data, and that person could not be deleted. | The admin needs to repeat the steps and try to delete the person again to delete their Pulse data. |
| “There was an error saving your settings. Try again later.” | When the admin changes the customization toggle, but the save was not completed. | The user should refresh the page or try again later. |
| “There was an error saving your privacy link. Please try again later.” | When the admin tries to change the privacy link, but the link could not be saved. | The admin would refresh the page or try again later. |
| “Please use a valid URL that’s 2000 characters or less with permitted special characters.” | When the admin tries to add a privacy link, but the link has invalid characters. | The user should try again, and follow these guidelines:<br><br>Check that the URL starts with http:// or https://, and contains a valid domain name with at least one dot (.) (tinyurl.com) and does not contain any illegal characters.<br><br>The permitted special characters in a URL are: a-z, A-Z, 0-9, hyphen (-), underscore (_), period (.), tilde (~), exclamation mark (!), asterisk (*), single quote ('), left parenthesis ((), right parenthesis ()), and forward slash (/). The privacy policy should be under 2000 characters to ensure compatibility with most web browsers. |
| “You don’t have access to this feature.” | When a user without a Global Admin role accesses Viva Pulse during Public Preview, but the preview has not been enabled for the tenant. | The tenant Global Admin can enable the Viva Pulse Public Preview for their tenant so all users can access Viva Pulse capabilities. |
| “You need to turn on access for public preview.” | When a user with a Global Admin role accesses Viva Pulse, but the preview has not been enabled for the tenant. | The tenant Global Admin can enable the Viva Pulse Public Preview for their tenant by using the “Manage Access” link so all users can access Viva Pulse capabilities. |