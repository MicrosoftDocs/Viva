---
title: Set up Viva Pulse Public Preview for your organization
description: "Set up Viva Pulse Public Preview for your organization"
ms.reviewer: 
ms.author: michellehu
author: michellehu-msft
manager: alisaliddle
audience: Admin
f1.keywords: NOCSH
ms.date: 06/05/2023
ms.topic: article
ms.service: viva
ms.subservice: viva-pulse
ms.localizationpriority: medium
ms.collection: m365initiative-viva-pulse  
search.appverid: MET150
---

# Set up Viva Pulse Public Preview for your organization

> [!NOTE]
> This article applies to a preview version of Microsoft Viva Pulse. You must be in the Public Preview program to access it. See [Set up Viva Pulse Public Preview](./set-up-viva-pulse-public-preview-for-your-organization.md) to enable the Viva Pulse Public Preview for your organization and enable Teams Activity feed notifications for users in your tenant. Also, please note that customer support will only be available in English for Public Preview. Features are subject to change.

## Prerequisites

You need to have the Microsoft 365 Global Admin role assigned to you to enable Viva Pulse Public Preview for your organization. You need Microsoft Teams deployed for your organization to use Viva Pulse in Microsoft Teams. Viva Pulse is also available as a web experience for which users will not need a Microsoft Teams application.

You also need to execute a script in PowerShell for users in your tenant to receive Teams Activity feed notifications.

## Enable Viva Pulse Public Preview

To enable Viva Pulse Public Preview, follow the steps below:

1. As the Microsoft 365 Global Admin, open the Viva Pulse (Preview) application in Microsoft Teams or go to [Viva Pulse in the web browser](https://pulse.viva.cloud.microsoft/).
2. Select **Manage Access** from the homepage.
3. Use the toggle under Public Preview access option to turn it **On**. Viva Pulse Public Preview is now enabled for your organization.
4. To turn off the Viva Pulse Public Preview, navigate to the **Manage** tab in Viva Pulse and turn off the toggle under the **Preview access** configuration.

Note that if a user installs the app from the Teams apps store, but Public Preview is not yet enabled, they receive a no access error message until Public Preview access is enabled for the tenant.

## Enable Teams Activity feed notifications  

Viva Pulse leverages the Teams Activity feed as one delivery method for notifications. As an admin, you need to execute a script in PowerShell for these notifications to appear in your user’s Teams app. After the script is executed successfully, users will receive Teams Activity feed notifications when a feedback author requests a Pulse, when feedback providers are reminded to respond, when a feedback author is notified their Pulse request has closed, and when a feedback author shares a Pulse report.

Enable Teams Activity feed notifications for your tenant and ensure you have [PowerShell installed](/powershell/scripting/install/installing-powershell-on-windows):

1. Connect to the target tenant in PowerShell\
`Connect-AzureAD -TenantId "[TENANT-ID]"`\
When prompted, login as the **Tenant Admin / Global Admin** for the tenant.
2. Create the service principle\
`New-AzureADServicePrincipal-AppId "56233257-15ee-4d3d-bdcd-9aa975244e4c" -DisplayName "[Viva Pulse (Preview)]"`
3. Validate that the service principle is created\
`Get-AzureADServicePrincipal -ObjectId <objectID>`\
*where objectId = what you get back after running step (2)*\
OR\
`Get-AzureADServicePrincipal`\
And find Viva Pulse in the list returned

Note that if Teams Activity Feed notifications are not enabled by running this script, feedback authors may not receive enough responses to their Pulses to review their team’s feedback and notifications increase the likelihood that more responses are generated. Alternatively, feedback authors can copy links to their Pulse requests or generated reports and share them directly through a personal email or Teams message.