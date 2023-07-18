---
title: Enable notifications for your organization
description: "Enable notifications for your organization"
ms.reviewer: 
ms.author: michellehu
author: michellehu-msft
manager: alisaliddle
audience: Admin
f1.keywords: NOCSH
ms.date: 07/12/2023
ms.topic: article
ms.service: viva
ms.subservice: viva-pulse
ms.localizationpriority: medium
ms.collection: m365initiative-viva-pulse  
search.appverid: MET150
---

# Enable notifications for your organization  

Viva Pulse leverages the email to deliver notifications. As an admin, you need to execute a script in PowerShell for these notifications to appear. After the script is executed successfully, users will receive email notifications when a feedback author requests a Pulse, when feedback providers are reminded to respond, when a feedback author is notified their Pulse request has closed, and when a feedback author shares a Pulse report.

Enable email notifications for your tenant and ensure you have [PowerShell installed](/powershell/scripting/install/installing-powershell-on-windows):

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

Note that if email notifications are not enabled by running this script, feedback authors may not receive enough responses to their Pulses to review their team’s feedback and notifications increase the likelihood that more responses are generated. Alternatively, feedback authors can copy links to their Pulse requests or generated reports and share them directly through a personal email or Teams message.