---
title: "Microsoft Viva - Feature access management"
ms.reviewer: elizapo
ms.author: elizapo
author: lizap
manager: pamgreen
ms.date: 07/01/2023
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
localization_priority: Priority
ms.custom:
ms.collection:  
- M365initiative-viva
- m365solution-overview
- highpri
- tier1
search.appverid:
- MET150
description: "Control who can access features in Microsoft Viva"
---

# Control access to features in Viva

You can use access policies in Viva to control who can access different features in Viva apps. Feature access management gives you the ability to enable or disable specific features in Viva for specific groups or users in your tenant and so tailor your deployments to your local regulatory and business requirements.  

> [!IMPORTANT]
> You can have multiple access policies active in your organization. That means that a user or group could be impacted by multiple policies. In that case, the most restrictive policy takes precedence. See [How access policies work in Viva](#how-access-policies-work-in-viva) for more information.

A permissioned admin in your tenant can create, assign, and manage access policies from PowerShell. When a user signs into Viva, the policy settings are applied, and they only see the features they're allowed to use. 

> [!NOTE]
> Only a subset of features in Viva apps support feature access management. And for those that do, restricting the use of one feature might impact the functionality of other features in the app. Be sure to check the app documentation on the specific feature to understand the implications of disabling or enabling access to a feature.

## Features available for feature access management
You can use feature access management to manage access to the following features:

|App|Feature|Who can control|
|-|-|-|
|Viva Insights|[Reflection](https://support.microsoft.com/topic/reflect-in-viva-insights-55379cb7-cf2a-408d-b740-2b2082eb3743)|Global admin<br>Insights admin|
| | | |



## Requirements
Before you can create an access policy in viva, you need the following:
- A [supported version of Microsoft 365 or a Viva Suite license](https://www.microsoft.com/microsoft-viva/pricing)   
- Access to [Exchange Online PowerShell Version 3.2.0](https://www.powershellgallery.com/packages/ExchangeOnlineManagement/3.2.0) or later 
- User accounts created in or synchronized to Azure Active Directory 
- Microsoft 365 groups and Azure AD security groups created in or synchronized to Azure AD. The membership type can be either dynamic or assigned. 
- The Global Administrator role in Azure AD or [the role required for the specific app and feature](#features-available-for-feature-access-management). 

> [!IMPORTANT] 
> Viva feature access management isn’t available to customers who have Microsoft 365 GCC, GCC High, or DDD plans.   


## Create and manage access policies for Viva features

### Create an access policy

Use the [**Add-VivaModuleFeaturePolicy**](/powershell/module/exchange/add-vivamodulefeaturepolicy?view=exchange-ps) PowerShell cmdlet to create an access policy for a Viva feature.

1. Install Exchange Online PowerShell Version 3.2.0:

   ```PowerShell
   Install-Module -Name ExchangeOnlineManagement -RequiredVersion 3.2.0
   ```

2. Connect to Exchange Online with admin credentials:

   ```PowerShell
   Connect-ExchangeOnline
   ```

   Complete the authentication as either a global administrator or the role required for the specific feature you're creating the policy for.

3. Run the [Get-VivaModuleFeature](/powershell/module/exchange/get-vivamodulefeature?view=exchange-ps) cmdlet to see what features are available to manage using an access policy.  
   
   For example, to see which features are supported in Viva Insights, run the following:
   ```powershell
   Get-VivaModuleFeature -ModuleId VivaInsights
   ```
4. Run the [Add-VivaModuleFeaturePolicy](/powershell/module/exchange/add-vivamodulefeaturepolicy?view=exchange-ps) cmdlet to create a new access policy.

   For example, run the following to create an access policy, called *DisableFeatureForAll*, to restrict access to the Reflection feature in Viva Insights. 

   ```powershell
   Add-VivaModuleFeaturePolicy -ModuleId VivaInsights -FeatureId Reflection -Name DisableFeatureForAll -IsFeatureEnabled $false -Everyone
   ```
   This example uses the *-Everyone* parameter to disable Reflection for all users. If you want to disable the feature for a specific user or group of users, use the *-UserId* or *-GroupId* parameter instead.



### Manage access policies
You can update an access policy to change whether a feature is enabled or disabled, as well as to change who the policy applies to (everyone, a user, or a group). 

For example, building on our last example, to enable the Reflection feature in Viva Insights for all users, run the following:

```powershell
Update-VivaModuleFeaturePolicy -ModuleId VivaInsights -FeatureId Reflection -Name DisableFeatureForAll -IsFeatureEnabled $true -Everyone
```

> [!IMPORTANT]
> Important: Values that you specify for the *-UserIds* and *-GroupIds* parameters or the *-Everyone* parameter overwrite any existing users or groups. To preserve the existing users and groups, you need to specify those existing users or groups *and* any additional users or groups that you want to add. Not including existing users or groups in the command effectively removes those specific users or groups from the policy. 


To check what features are disabled for a specific user or group, run the Get-VivaModuleFeatureEnablement cmdlet. This cmdlet returns what's called the *enablement status* for the user or group.

For example:

```powershell
Get-VivaModuleFeatureEnablement -ModuleId VivaInsights -FeatureId Reflection -Identity user@contoso.com
```

### Delete an access policy

Use the **Remove-VivaModuleFeaturePolicy** to delete an access policy.

For example, to delete the Reflection feature access policy, start by getting the specific UID for the access policy - you can get that by running **Get-VivaModuleFeaturePolicy**. Then, run the following:

```powershell
Remove-VivaModuleFeaturePolicy -ModuleId VivaInsights -FeatureId Reflection -PolicyId xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
```

## How access policies work in Viva
Here's how access policies work in Viva: 

- When a user signs in and accesses Viva, a check is immediately made to see if there’s a policy that applies to the user. 
- If the user isn’t assigned a policy or isn’t a member of an Azure AD group or Microsoft 365 group that is assigned a policy configuration, then another check is made in X hours or when the user next logs in   . 
- If the user is assigned a policy or is a member of an Azure AD group or Microsoft 365 group that is assigned a policy, then the appropriate policy setting is applied. A check is made again in X hours or when the user next logs in . 
- If a user has multiple policies assigned to them for the same user, the most restrictive policy is applied, as described below. An assigned policy takes precedence over the default policy/ship state for the feature.  
   - Features without user opt in/out preferences: feature is disabled, feature is enabled
   - Features with user opt in/out preference: feature is disabled, feature is enabled, feature is enabled with user opt out on default (in latter case, user’s actioned opt in/out preference takes priority)   
- If users are in nested groups and the parent group is targeted for policies, the users in the nested groups will receive the policies.  The nested groups and the users in those nested groups must be created in or synchronized to Azure AD. 

## Additional information and best practices
- Only user-based policy settings are available. 
- As new user-based policy settings are made available for Viva, they will be automatically added to Viva feature access management for admins to set policies against
- When a policy is created, the user’s experience will be updated to reflect the policy within X hours.    
- When users are added/removed from an Azure AD or Microsoft 365 Group, it may take up to X hours for their Viva experience to reflect any resulting changes from the assigned policy as a result of group membership changes. 
- When user identities in AAD are deleted, user data will be deleted from VFAM. If users identities are re-enabled during the soft-deleted period, the permissioned admin will need to reassign policies to the user. 
- When groups in Azure AD and Microsoft 365 are deleted, they will be deleted from the stored policies.  If groups are re-enabled during the soft-deleted period, the permissioned admin will need to reassign policies to the groups. 

   

## More resources

[Microsoft Viva Privacy](/Viva/viva-privacy)

[Microsoft Viva Security](/Viva/microsoft-viva-security)

[Viva admin roles and tasks](/viva/microsoft-viva-admin-roles)
