---
ms.date: 09/12/2024
title: Delegate access to organizational insights and Copilot Dashboard
description: Learn how to delegate access to organization insights and Copilot Dashboard in Viva Insights.
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva-insights
search.appverid: 
- MET150 
manager: abelutk
audience: Admin
---
# Delegate access to organizational insights and Copilot Dashboard

You can delegate access to your organizational insights or the Copilot Dashboard to other people within your company.

By granting delegate access, someone else at your company, such as your chief of staff or one of your direct reports, would have the same access you have to the insights. They can view them and operationalize business decisions based on the data.

There are no changes to the metrics, aggregation, or filtering tools available to the delegate. However, the delegate doesn't have access to your personal insights or personal recommended actions, like sharing insights or sending praise to a recent collaborator.

>[!Note]
>To view and delegate access to organizational insights, you need a Viva Insights subscription and must be assigned the Group Manager role. [Learn more about roles and access for organizational insights](org-insights.md#subscriptions-roles-and-access).
>
>To view and delegate access to the Copilot dashboard, you need to have access to the dashboard, but neither the Group Manager role nor a Viva Insights subscription is required. [Learn more about how access to the Copilot dashboard is determined](copilot-dashboard.md#how-access-to-the-copilot-dashboard-is-determined).

Here are a few other things to note:

* You can only delegate access to organizational insights to people who have a Viva Insights license.

* You can delegate access to whomever you want and to as many people as you want (maximum limit of 75), as long as they're in your tenant.

* You can revoke access to whomever you want at any time.

* A delegate can't delegate access to others.

* If you assign delegates for organizational insights, and you’re removed as a group manager from Viva Insights, the delegates you assigned are also removed along with their access.

## How to assign a delegate

### Organizational insights & Copilot Dashboard:   
*Applies to: People with access to [organizational insights](../org-team-insights/org-insights.md#organization-insights-in-viva-insights) or [Copilot Dashboard](../org-team-insights/copilot-dashboard-advanced-features.md)*

1. Select the feature you wish to delegate access to, then select the ellipses (…) at the top right.  
2. Select **Delegate access.**
3. Under **Share with**, type in the name or names of the people you want to assign as delegates. You can also add a personal note, but it’s not required.
4. Select **Submit**.

:::image type="content" source="images/delegate-access-1.png" alt-text="Screenshot showing delegate access box for Copilot Dashboard." lightbox="images/delegate-access-1.png":::

## Second method for assigning delegates

This method not only allows you to assign delegates but add and remove delegates all on the same screen.

### Organizational insights & Copilot Dashboard:  

*Applies to: People with access to organizational insights or Copilot dashboard*

1. In the Viva Insights app, select the ellipses (…) at the top right.
2. Select **Settings.**
3. Select **Delegate access.**
4. Here you can find your delegates and the start date of their access.
5. To add a new delegate, at the top right, select **Add new.**
6. To revoke access for an existing delegate, select the **Delete** (trashcan) icon.

:::image type="content" source="images/delegate-access-2.png" alt-text="Screenshot showing alternate method for delegating access." lightbox="images/delegate-access-2.png":::

Whenever a delegate has been added, they'll be notified in Teams Chat of their current access status.

## Delegate access view

### Organizational Insights and Copilot Dashboard

*Applies to: People given delegate access*

1. If you're given delegate access, you receive an automated message in Teams from the manager who gave you access.
2. On the message, **select View insights**. You are then redirected to the manager’s view of the respective dashboard.  
3. In either dashboard on the top left, you will see a banner designed to inform you of which leader’s insights you’re viewing. Select either **View insights for** or **View Copilot Dashboard for**, in respective dashboard. If you're given delegate access by multiple leaders, select the banner to switch between different dashboards.

:::image type="content" source="images/delegate-access-3.png" alt-text="Screenshot showing whose insights you're viewing.":::

>[!Note]
>The View Copilot Dashboard banner is only accessible from the Copilot dashboard and can’t be viewed anywhere else in the Viva app.

## Remove access to delegate Copilot Dashboard with Powershell

[Learn more about using policies to control access to features in Viva](/viva/feature-access-management).

>[!Important]
>Policies to disable delegation for Copilot dashboard can only be applied for the entire tenant level at this time.

You can set a policy to disable delegation for Copilot Dashboard for the tenant using Powershell cmdlets. This is a tenant-level policy, not a user or group-level policy. No users can delegate access to Copilot Dashboard until you remove or update the policy. Before you can use the cmdlet, you need to install a module and sign in to be authenticated. [Learn more about how to set these policies](/viva/feature-access-management).

1. [Connect to Exchange Online](../advanced/setup-maint/configure-personal-insights.md#connect-to-exchange-online) and when prompted, sign in with your admin credentials.

2. After you’ve signed in, you can manage access for your tenant using the Add-VivaModuleFeaturePolicy cmdlet:[Add-VivaModuleFeaturePolicy](/powershell/module/exchange/add-vivamodulefeaturepolicy).

**Example: Turn off delegation for Copilot Dashboard for all users in your tenant.**

```powershell
 ModuleId : VivaInsights
 FeatureId : CopilotDashboardDelegation  
 Name : DisableFeatureForAll
 IsFeatureEnabled : false
 Everyone
```

>[!Note]
>After disabling the delegate feature for Copilot Dashboard, it may take up to 12 hours to reflect the change.

## Audit who has delegate access

Admins can use audit logs to identify which users have access to Viva Insights through delegation. [Learn more about how to search the audit log](/purview/audit-search).

| Friendly name | Operation | Actor | Target | Modified properties name | Modified properties value | 
|---|---|---|---|---|---|
| Added delegate access | AddDelegates | The user who provided access | The user whose access was changed | Leader Insights delegate | Enabled |
| Removed delegate access | RemoveDelegates |  The user who provided access | The user whose access was changed  | Copilot Dashboard delegate | Disabled |


### Related topics

- [Learn more about organization insights](org-insights.md)
- [Learn more about the Copilot dashboard](copilot-dashboard.md)
