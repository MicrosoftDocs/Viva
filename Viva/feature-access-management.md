---
title: "Microsoft Viva - Feature access management"
ms.reviewer: elizapo
ms.author: elizapo
author: lizap
manager: pamgreen
ms.date: 10/18/2023
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
localization_priority: Priority
ms.custom:
ROBOTS: NOINDEX, NOFOLLOW
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

You can use access policies in Viva to manage which users can access specific features in Viva apps. Feature access management gives you the ability to enable or disable specific features in Viva for specific groups or users in your tenant and so tailor your deployments to meet your local regulatory and business requirements.  

> [!IMPORTANT]
> You can have multiple access policies for a feature active in your organization. That means that a user or group could be impacted by multiple policies. In that case, the most restrictive policy takes precedence. For more information, see [How access policies work in Viva](#how-access-policies-work-in-viva).

An authorized admin (for example, a global admin) in your tenant can create, assign, and manage access policies from PowerShell. When a user signs into Viva, the policy settings are applied, and they only see the features that haven't been disabled.

> [!NOTE]
> You can only disable a subset of features in Viva apps by using feature access management. Restricting the use of one feature might impact the functionality of other features in the app. Be sure to check the app documentation on the specific feature to understand the implications of disabling or enabling access to a feature.

## Features available for feature access management

You can use feature access management to manage access to the following features:

> [!NOTE]
> Only some features will have controls available for admins to provide users with the option to opt out.

|App|Feature|Optional control for user opt-out?|Who can manage access|ModuleID|
|-|-|-|-|-|
|Viva Insights|[Reflection](https://support.microsoft.com/topic/reflect-in-viva-insights-55379cb7-cf2a-408d-b740-2b2082eb3743)*|No|Global admin<br>Insights admin|VivaInsights|
|Viva Pulse|[Customization](/viva/pulse/setup-admin-access/set-up-in-app-pulse-experience#customization)*|No|Global admin|VivaPulse|


\* Not yet available for all tenants. Support will be added soon.

> [!NOTE]
> You can only control access to features that support access policies *and* that are supported in your tenant. For example, if you have an EDU-based tenant, you cannot use policies to gain access to features that are not available to EDU tenants. The same applies for features that are unavailable in specific geographies. Check the documentation for the specific feature that you'd like to use for more information about its availability.

## Requirements

Before you can create an access policy in Viva, you need:

- A [supported version of Microsoft 365 or a Viva Suite license](https://www.microsoft.com/microsoft-viva/pricing)
- Access to [Exchange Online PowerShell Version 3.2.0](https://www.powershellgallery.com/packages/ExchangeOnlineManagement/3.2.0) or later
- User accounts created in or synchronized to Azure Active Directory
- Microsoft 365 groups and Azure AD security groups created in or synchronized to Azure AD. The membership type can be either dynamic or assigned.
- The global administrator role in Azure AD or [the role required for the specific app and feature](#features-available-for-feature-access-management).

> [!IMPORTANT]
> Viva feature access management isn’t available to customers who have Microsoft 365 GCC, GCC High, or DOD plans.

## Create and manage access policies for Viva features

### Create an access policy

Use the [**Add-VivaModuleFeaturePolicy**](/powershell/module/exchange/add-vivamodulefeaturepolicy) PowerShell cmdlet to create an access policy for a Viva feature.

You can assign a maximum of 10 policies per feature. Each policy can be assigned to a maximum of 20 users or groups.

> [!NOTE]
> Creation of the tenant’s first policy may take up to 15 minutes to be able to be queried via cmdlet. Please wait 15 minutes and try again.

1. Install Exchange Online PowerShell Version 3.2.0 or later:

   ```PowerShell
   Install-Module -Name ExchangeOnlineManagement
   ```

2. Connect to Exchange Online with admin credentials:

   ```PowerShell
   Connect-ExchangeOnline
   ```

   Complete the authentication as either a global administrator or the role required for the specific feature you're creating the policy for.

3. Run the [Get-VivaModuleFeature](/powershell/module/exchange/get-vivamodulefeature) cmdlet to see what features are available to manage using an access policy.  

   For example, to see which features are supported in Viva Insights, run the following cmdlet:

   ```PowerShell
   Get-VivaModuleFeature -ModuleId VivaInsights
   ```

4. Run the [Add-VivaModuleFeaturePolicy](/powershell/module/exchange/add-vivamodulefeaturepolicy) cmdlet to create a new access policy.

   For example, run the following to create an access policy, called *UsersAndGroups*, to restrict access to the Reflection feature in Viva Insights.

   ```powershell
   Add-VivaModuleFeaturePolicy -ModuleId VivaInsights -FeatureId Reflection -Name UsersAndGroups -IsFeatureEnabled $false -GroupIds group1@contoso.com,group2@contoso.com -UserIds user1@contoso.com,user2@contoso.com    
   ```
   
    This example adds a policy for the Reflection feature in Viva Insights. The policy disables the feature for the specified users and group members. If you want to disable the feature for all users, use the *-Everyone* parameter instead.

### Manage access policies

You can update an access policy to change whether a feature is enabled or disabled, as well as to change who the policy applies to (everyone, a user, or a group).

For example, building on our last example, to update who the policy applies to, run the following cmdlet:

```powershell
Update-VivaModuleFeaturePolicy -ModuleId VivaInsights -FeatureId Reflection -PolicyId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx -GroupIds group1@contoso.com,group2@contoso.com
```

> [!IMPORTANT]
> Values that you specify for the *-UserIds* and *-GroupIds* parameters or the *-Everyone* parameter overwrite any existing users or groups. To preserve the existing users and groups, you need to specify those existing users or groups *and* any additional users or groups that you want to add. Not including existing users or groups in the command effectively removes those specific users or groups from the policy.

To check what features are disabled for a specific user or group, run the [Get-VivaModuleFeatureEnablement](/powershell/module/exchange/get-vivamodulefeatureenablement) cmdlet. This cmdlet returns what's called the *enablement status* for the user or group.

For example:

```powershell
Get-VivaModuleFeatureEnablement -ModuleId VivaInsights -FeatureId Reflection -Identity user@contoso.com
```

### Delete an access policy

Use the [Remove-VivaModuleFeaturePolicy](/powershell/module/exchange/remove-vivamodulefeaturepolicy) cmdlet to delete an access policy.

For example, to delete the Reflection feature access policy, start by getting the specific UID for the access policy - you can get that by running [Get-VivaModuleFeaturePolicy](/powershell/module/exchange/get-vivamodulefeaturepolicy). Then, run the following cmdlet:

```powershell
Remove-VivaModuleFeaturePolicy -ModuleId VivaInsights -FeatureId Reflection -PolicyId xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
```

## How access policies work in Viva

Here's how access policies work in Viva:

:::image type="content" source="./media/vfam-workflow.png" alt-text="Workflow diagram that shows the steps for applying a feature access policy." lightbox="./media/vfam-workflow.png":::

- When a user signs in and accesses Viva, a check is immediately made to see if there’s a policy that applies to the user.
- If the user isn’t assigned a policy or isn’t a member of an Azure AD group or Microsoft 365 group that is assigned a policy, then the default enablement state for the feature is applied.
- If the user is assigned a policy or is a member of an Azure AD group or Microsoft 365 group with an assigned policy, then the policy setting is applied.
- If a user has multiple policies assigned to them for the same feature, the most restrictive policy is applied (Note that not all features include the ability for a user to opt out.) Here's the order of precedence:
   1. Feature is disabled by policy.
   2. Feature is enabled by policy.
   3. Feature is enabled, and the user can opt out.
   4. Default enablement state for the feature
- If users are in nested groups and you apply access policies to the parent group, the users in the nested groups receive the policies. The nested groups and the users in those nested groups must be created in or synchronized to Azure AD.
- Changes to access policies take effect for the user within 24 hours, unless otherwise noted for a specific feature.
- When you add users to or remove them from an Azure AD or Microsoft 365 group, it can take 24 hours before changes to their feature access take effect.
- When an admin removes the option for users to opt out by fully enabling or disabling the feature, the user’s opt in/out preference isn't preserved and will be reset to the default state. If an admin re-enables the option allowing a user to opt out of a feature, users will need to select to opt out of the feature again.
- Quick changes to the enablement state for a feature in less than 24 hours after making the change may not result in the resetting of user opt in/out preferences.
- For a history of policy creation, updates, and deletions, see the Viva Feature Access Management (VFAM) change logs for your organization in [Microsoft Purview](/purview/tutorial-purview-audit-logs-diagnostics).

## Additional information and best practices

- Only user-based policy settings are available.
- As new user-based policy settings are made available for Viva, they'll be added to Viva feature access management for admins to set policies against.
- When user identities in Azure AD are deleted, user data is deleted from Viva feature access management. If user identities are re-enabled during the soft-deleted period, the admin needs to reassign policies to the user.
- When groups in Azure AD and Microsoft 365 are deleted, they're deleted from the stored policies. If groups are re-enabled during the soft-deleted period, the admin needs to reassign policies to the groups.

## More resources

[Microsoft Viva Privacy](/Viva/viva-privacy)

[Microsoft Viva Security](/Viva/microsoft-viva-security)

[Viva admin roles and tasks](/viva/microsoft-viva-admin-roles)
