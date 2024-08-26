---
title: Granular access controls for Viva Pulse
description: "Granular access controls for Viva Pulse"
ms.reviewer: 
ms.author: hasrivas
author: hasrivas
manager: alisaliddle
audience: Admin
f1.keywords: NOCSH
ms.date: 8/26/2024
ms.topic: article
ms.service: viva-pulse
ms.localizationpriority: medium
ms.collection:
- m365initiative-viva-pulse
- essentials-security  
search.appverid: MET150
---

# Granular access controls for Viva Pulse

As a Viva Pulse administrator, you can use access policies to manage which users can access specific features in Viva Pulse. Feature access management gives you the ability to enable or disable specific features in Viva Pulse for particular groups or users in your tenant and tailor Viva Pulse to meet your local regulatory and business requirements. See [Control access to features in Viva](https://go.microsoft.com/fwlink/p/?linkid=2245618) to learn more.

## Customization

You can control whether feedback authors can add their own questions to existing stock templates or edit existing stock questions through centralized feature access management, which allows you to configure access to customization capabilities at the tenant level, group level (using AAD groups or M365 groups), or at the user level for maximum flexibility. The customization control will be default turned on for your tenant. Use the FeatureID value **CustomizationControl** to configure customization capability for your tenant. 

## Customization

You can control whether feedback authors can respond to open text responses in their Pulse reports and have a deidentified conversation with the Pulse participant as part of their Pulse reports. Using centralized feature access management, you can decide for this capability to be available at the tenant level, group level (using AAD groups or M365 groups), or at the user level for maximum flexibility. This capability will be default turned on for your tenant. Use the FeatureID value **PulseConversation** to configure conversations in Pulse reports for your tenant. 

## Resources

To configure these capabilities, you need to use a PowerShell cmdlet:

1. Use the **Add-VivaModuleFeaturePolicy cmdlet** to create a new access policy to disable the customization or conversation capability in Viva Pulse. See [Add-VivaModuleFeaturePolicy cmdlet](/powershell/module/exchange/add-vivamodulefeaturepolicy) for detailed documentation.
2. Use the **Update-VivaModuleFeaturePolicy cmdlet** to update your access policy control the customization or conversation capability in Viva Pulse. See [Update-VivaModuleFeaturePolicy cmdlet](/powershell/module/exchange/update-vivamodulefeaturepolicy) for detailed documentation.
3. Use the **Get-VivaModuleFeaturePolicy cmdlet** to view your access policies for customization or conversation capability in Viva Pulse. See [Get-VivaModuleFeaturePolicy cmdlet](/powershell/module/exchange/get-vivamodulefeaturepolicy) for detailed documentation.
4. Use the **Remove-VivaModuleFeaturePolicy cmdlet** to delete an access policy for customization or conversation capability in Viva Pulse. See [Remove-VivaModuleFeaturePolicy cmdlet](/powershell/module/exchange/remove-vivamodulefeaturepolicy) for detailed documentation.
