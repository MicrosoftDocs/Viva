---
ms.date: 08/28/2024
title: Copilot in Viva Goals
ms.reviewer: 
ms.author: daisyfeller
author: DefinitelyNotNitza
manager: Liz.Pierce
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-goals
ms.localizationpriority: medium
ms.collection:  
- Strat_SP_modern
- M365-collaboration
- m365initiative-viva-goals
- vg-integration  
search.appverid:
- MET150
description: "Learn how to use Copilot in Viva Goals to create, share, manage, and summarize organizational goals."
---

# Enable Copilot in Viva Goals

Microsoft Copilot in Viva Goals lets you use generative AI to help set business goals and align teams to your organization’s strategic priorities. It also offers in-app guidance to users for creating, refining, and summarizing goals, as well as for sharing goals updates.

Microsoft 365 Global admins and Viva Goals admins can control who has access to Copilot in Viva Goals. You can enable or disable access for specific users, groups, or your entire tenant by using [Viva Feature Access Management (VFAM)](..\feature-access-management.md). VFAM provides a consistent experience across Viva modules to enable or disable access to features, including Microsoft Copilot.  

>[!NOTE]
> Controlling access to Copilot in Viva Goals by using VFAM is available for all Viva Goals customers starting in August 2024. The previous controls in the Viva Goals admin portal for enabling or disabling access to Copilot will be deprecated starting in August 2024. All existing configurations for enabling or disabling Copilot in Viva Goals are automatically moved to VFAM - you do not need to reconfigure your access settings. 


## Licensing requirements

Customers with a *Viva Suite* or *Viva Goals Standalone* license, or a trial version of either, can activate Copilot in the Viva Goals admin center.

## Configuring copilot settings using Viva Feature Access Management 
You can use VFAM in either the Microsoft 365 admin center or by using PowerShell cmdlets. You can enable or disable access to Copilot in Viva Goals for everyone, for specific users, or for specific groups by creating tenant or group level access policies.  

For example, to disable access to Copilot in Viva Goals for only your users in Germany, you do the following: 
- Create a group access policy in VFAM (using PowerShell cmdlets).
- Assign the Microsoft 365 group that contains all Germany users to the group policy.
- Set the group policy to OFF (disabled).

For detailed information about controlling access using VFAM, including the command syntax, see [Microsoft Viva - Feature access management](../feature-access-management.md).

## PowerShell cmdlet reference for use with Copilot in Viva Goals 

The following table provides example PowerShell cmdlets, with parameters, that you can use to enable or disable access to Copilot in Viva Goals.

For these examples, the **ModuleId** is *VivaGoals*, and the **featureId** is *CopilotInVivaGoals*.


|Task|Cmdlet|
|-|-|
|View the existing policy.|`Get-VivaModuleFeaturePolicy -ModuleId VivaGoals -FeatureId CopilotInVivaGoals`|
|Update tenant policy to disable access to Copilot in Viva Goals for everyone.|`Add-VivaModuleFeaturePolicy -ModuleId VivaGoals -FeatureId CopilotInVivaGoals -Name <PolicyName> -IsFeatureEnabled $false -Everyone`|
|Add custom policy to enable Viva Goals co-pilot for specific group or user.|`Add-VivaModuleFeaturePolicy -ModuleId VivaGoals -FeatureId CopilotInVivaGoals -Name <PolicyName> -IsFeatureEnabled $true -UserIds <user_emails> -GroupIds <group_email>`|
|Add a custom policy to disable access for a specific group or user.|`Add-VivaModuleFeaturePolicy -ModuleId VivaGoals -FeatureId CopilotInVivaGoals -Name <PolicyName> -IsFeatureEnabled $false –UserIds <user_email> –GroupIds <group_email>`|
|Check whether a specific user can access Copilot in Viva Goals.|`Get-VivaModuleFeatureEnablement -ModuleId VivaGoals -Featureid CopilotInVivaGoals  -Identity  <user_email>`|

 
## Configuring copilot settings from Microsoft 365 Admin Center  

You can also control access to Copilot in Viva Goals from the Microsoft 365 Admin Center.  

To enable or disable access for everyone in your organization, do the following:
1. In the Microsoft 365 admin center, select **Copilot**, and then select **Viva Goals**. 

   Your Org-wide setting shows whether access is enabled for your entire organization. 
2. To turn this setting on or off, select **Manage**. 
3. Select **On** to enable access for everyone or **Off** to disable access for everyone. 
4. Select **Save**. 

To enable access for select people or groups, do the following: 

1. In the Microsoft 365 admin center, select **Copilot**, and then select **Viva Goals**. 
2. Select **Create policy** under **Custom policies for people and groups**. 
3. Give your policy a descriptive name. For example, "Disable for users in office X." 
4. Select **Off for specific people** if you want to disable access to Copilot in Viva Goals for only people you select. Choose **On for specific people** if you want to enable access only the people you select. 
5. Add the people or groups you want the policy to apply to. 
6. Select **Save**. 

> [!NOTE]
> You can create multiple custom policies to suit your organization's needs. 

You can learn more details about enabling Copilot controls from the Microsoft 365 admin center in [Manage access to Copilot in Viva](../copilot/copilot-access-management.md)


## Important things to keep in mind while using VFAM   

- The policies created by using VFAM can take up to 24 hours to go into effect. 
- The most restrictive policy assigned to a user or group take precedences over other policies within a feature. For example, for Copilot, if you create an OFF-tenant policy and ON group policy (for users in a specific geographic location, for example), the group policy takes precedence over the tenant policy. As a result only users in the group can access Copilot in Viva Goals.

## What happens Viva Goal Copilot settings configured in the Viva Goals admin portal prior to August 2024? 

Now that you can use Viva Feature Access Management to control access to Copilot in Viva Goals, the current control present in the Viva Goals admin portal for users to enable or disable Viva Goals copilot will be deprecated.

All existing configurations set for enabling or disabling the Viva Goals copilot will be automatically moved to VFAM and will work without having to reconfigure it using VFAM. For example, If you have enabled Copilot in Viva Goals for only a specific group of users ('All US employees group') you'll see a corresponding custom access control policy is created on VFAM to allow access only for 'All US employees group'.

Going forward, use VFAM to make changes to access to Copilot in Viva.


## Related

- [Introduction to Microsoft Copilot in Viva Goals](https://support.microsoft.com/en-us/topic/introduction-to-microsoft-copilot-in-viva-goals-a1c1a5f1-9135-495b-969a-6a6172305ecc)

- [Use Copilot in Viva Goals to create, summarize, and understand goals](https://support.microsoft.com/en-us/topic/use-copilot-in-viva-goals-to-create-summarize-and-understand-goals-11bf3612-669c-49b1-99f4-93b942ba5099)

- [Copilot in Viva Goals FAQ](https://support.microsoft.com/en-us/topic/copilot-in-viva-goals-faq-31e9fbac-6214-4052-958f-9e766fd8b0e3)

- [Data, privacy, and security for Copilot in Viva Goals](vg-privacy-and-security.md#copilot-in-viva-goals)
