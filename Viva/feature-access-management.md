---
title: "Microsoft Viva - Feature access management"
ms.reviewer: elizapo
ms.author: elizapo
author: lizap
manager: elizapo
ms.date: 03/22/2024
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-suite
ms.localizationpriority: medium
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

You can use access policies in Viva to manage which users can access specific features in Viva apps. Feature access management gives you the ability to enable or disable specific features in Viva for specific groups or users in your tenant and so tailor your deployments to meet your local regulatory and business requirements.  

> [!IMPORTANT]
> You can have multiple access policies for a feature active in your organization. That means that a user or group could be impacted by multiple policies. In that case, the most restrictive policy assigned directly to a user or group takes precedence. For more information, see [How access policies work in Viva](#how-access-policies-work-in-viva).

An authorized admin (for example, a global admin) in your tenant can create, assign, and manage access policies from PowerShell. When a user signs into Viva, the policy settings are applied, and they only see the features that haven't been disabled.

> [!NOTE]
> You can only disable a subset of features in Viva apps by using feature access management. Restricting the use of one feature might impact the functionality of other features in the app. Be sure to check the app documentation on the specific feature to understand the implications of disabling or enabling access to a feature.

## Features available for feature access management

You can use feature access management to manage access to the following features:

> [!NOTE]
> Only some features will have controls available for admins to provide users with the option to opt out.

|App|Feature|Control for user opt-out?|Who can manage access|ModuleID|
|-|-|-|-|-|
|Insights|[Copilot Dashboard](/viva/insights/org-team-insights/copilot-dashboard)|No|Global admin|VivaInsights|
||[Copilot Dashboard Auto Enablement](/viva/insights/org-team-insights/copilot-dashboard-advanced-features)|No|Global admin|VivaInsights|
||[Digest Welcome Email](/viva/insights/advanced/setup-maint/configure-personal-insights#configure-access-at-the-tenant-level)|No| Global admin|VivaInsights|
||[Reflection](https://support.microsoft.com/topic/reflect-in-viva-insights-55379cb7-cf2a-408d-b740-2b2082eb3743)|No|Global admin, Insights admin|VivaInsights|
|Pulse|[Customization](/viva/pulse/setup-admin-access/set-up-in-app-pulse-experience#customization)|No|Global admin|VivaPulse|
|Skills|[Skill suggestions](/viva/skills/skills-overview)*|Yes|Global admin, Knowledge admin|VivaSkills| 


\* The feature or feature control might not yet be available for all tenants. Support will be added soon.

> [!NOTE]
> You can only control access to features that support access policies *and* that are available in your tenant. For example, if you have an EDU-based tenant, you cannot use policies to gain access to features that are not available to EDU tenants. The same applies for features that are unavailable in specific geographies. Check the documentation for the specific feature that you'd like to use for more information about its availability.

## Requirements

Before you can create an access policy in Viva, you need:

- A [supported version of Microsoft 365 or a Viva Suite license](https://www.microsoft.com/microsoft-viva/pricing)
- Access to [Exchange Online PowerShell Version 3.2.0](https://www.powershellgallery.com/packages/ExchangeOnlineManagement/3.2.0) or later
- User accounts created in or synchronized to Microsoft Entra ID
- Microsoft 365 groups and Microsoft Entra security groups created in or synchronized to Microsoft Entra ID. The membership type can be either dynamic or assigned.
- The global administrator role in Microsoft Entra ID or [the role required for the specific app and feature](#features-available-for-feature-access-management).


> [!IMPORTANT]
> Viva feature access management isn’t available to customers who have Microsoft 365 GCC, GCC High, or DOD plans.

## Create and manage access policies for Viva features

### Get the featureID for the feature
Before you can create an access policy, you need to get the **featureID** for the specific feature you want to control access to.

Use the [**Get-VivaModuleFeature**](/powershell/module/exchange/get-vivamodulefeature) PowerShell cmdlet to get a list of all of the features available in a specific Viva app and their associated IDs.

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
4. Find the feature that you'd like to create an access policy for and make note of its **featureID**.

### Create an access policy

Now that you have the **featureID**, use the [**Add-VivaModuleFeaturePolicy**](/powershell/module/exchange/add-vivamodulefeaturepolicy) PowerShell cmdlet to create an access policy for the feature.

You can assign a maximum of 10 policies per feature to users and groups. Each policy can be assigned to a maximum of 20 users or groups. You can assign one additional policy per feature to the entire tenant by using the *-Everyone* parameter, which will function as a global default state for that feature across your organization.

Run the [Add-VivaModuleFeaturePolicy](/powershell/module/exchange/add-vivamodulefeaturepolicy) cmdlet to create a new access policy.

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
> Values that you specify for the *-UserIds* and *-GroupIds* parameters or the *-Everyone* parameter overwrite any existing users or groups. To preserve the existing users and groups, you need to specify those existing users or groups *and* any additional users or groups that you want to add. Not including existing users or groups in the command effectively removes those specific users or groups from the policy. You can't update a policy for a particular user or group to include the entire tenant if a policy for the entire tenant already exists for the feature - only one tenant-wide policy is supported.

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
### Troubleshooting

If you have issues creating or using access policies for Viva app features, confirm the feature you are trying to set a policy for is listed in the [feature table](#features-available-for-feature-access-management) and is available to your tenant.

## How access policies work in Viva

Here's how access policies work in Viva:

:::image type="content" source="./media/vfam-workflow.png" alt-text="Workflow diagram that shows the steps for applying a feature access policy." lightbox="./media/vfam-workflow.png":::

- When a user signs in and accesses Viva, a check is immediately made to see if there’s a policy that applies to the user.
- If the user is assigned to a policy directly or is a member of a Microsoft Entra group or Microsoft 365 group with an assigned policy, then the policy setting is applied.
- If the user isn’t assigned a policy directly or isn’t a member of a Microsoft Entra group or Microsoft 365 group that is assigned a policy, then the global default policy is applied. If there is no global default policy, the default enablement state for the feature is applied.
- If the user has multiple policies assigned to them directly or as a group, then the most restrictive policy applies. (Note that not all features include the ability for a user to opt out.) Here's the order of precedence:
   1. Feature is disabled.
   2. Feature is enabled.
   3. Feature is enabled, and the user can opt out.
- If users are in nested groups and you apply access policies to the parent group, the users in the nested groups receive the policies. The nested groups and the users in those nested groups must be created in or synchronized to Microsoft Entra ID.
- Changes to access policies take effect for the user within 24 hours, unless otherwise noted for a specific feature.
- When you add users to or remove them from a Microsoft Entra ID or Microsoft 365 Group, it can take 24 hours before changes to their feature access take effect.
- When an admin removes the option for users to opt out by fully enabling or disabling the feature, the user’s opt in/out preference isn't preserved and will be reset to the default state. If an admin re-enables the option allowing a user to opt out of a feature, users will need to select to opt out of the feature again.
- Quick changes to the enablement state for a feature in less than 24 hours after making the change may not result in the resetting of user opt in/out preferences.
- For a history of policy creation, updates, and deletions, see the Viva Feature Access Management (VFAM) change logs for your organization in [Microsoft Purview](/purview/tutorial-purview-audit-logs-diagnostics).

## Additional information and best practices

- Policies are evaluated on a per-user basis.
- Only one policy per feature can be assigned to *'everyone'.* This policy serves as the global default state for that feature in your organization.
- As new feature controls are made available in Viva to manage user and group access, they're added to Viva feature access management.
- When user identities in Microsoft Entra ID are deleted, user data is deleted from Viva feature access management. If user identities are re-enabled during the soft-deleted period, the admin needs to reassign policies to the user.
- When groups in Microsoft Entra ID and Microsoft 365 are deleted, they're deleted from the stored policies. If groups are re-enabled during the soft-deleted period, the admin needs to reassign policies to the groups.

## More resources

[Microsoft Viva Privacy](/Viva/viva-privacy)

[Microsoft Viva Security](/Viva/microsoft-viva-security)

[Viva admin roles and tasks](/viva/microsoft-viva-admin-roles)
