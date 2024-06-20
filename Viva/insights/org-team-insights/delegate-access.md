---
ms.date: 06/21/2024
title: Delegate access to organizational insights and Copilot Dashboard
description: Learn how to delegate access to organization insights and Copilot Dashboard in Viva Insights.
author: Laura-Pen
ms.author: v-penlaura
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
The Copilot Dashboard Delegation feature is gradually rolling out to our customers so it may not be available to everyone right away.

You can delegate access to your organizational insights and Copilot Dashboard to other people within your company. In contrast to organizational insights, holding the group manager role isn’t required to delegate access to the Copilot Dashboard.  

By granting delegate access, someone else at your company, such as your chief of staff or one of your direct reports, would have the same access you have to organizational insights. They can view them and operationalize business decisions based on the data and insights.

There are no changes to the metrics, aggregation, or filtering tools available to the delegate. However, the delegate doesn't have access to your personal insights or personal recommended actions, like sharing insights or sending praise to a recent collaborator.

If you use this optional feature, here are a few other things to note:

* You can only delegate access for organizational insights to people who have a Viva Insights license.

* Delegates for Copilot dashboard no longer require a Viva Insights subscription.

* You can delegate access to whomever you want and to as many people as you want (maximum limit of 75), so long as they are in your tenant.

* You can revoke access to whomever you want at any time.

* A delegate can't delegate access to others.

* If you assign delegates, and you’re removed as a group manager from Viva Insights, the delegates you assigned are also removed along with their access.

## How to assign a delegate
### Organizational insights & Copilot Dashboard:   
*Applies to: People with access to [organizational insights](../org-team-insights/org-insights.md#organization-insights-in-viva-insights) or [Copilot Dashboard](../org-team-insights/copilot-dashboard-advanced-features.md).*

1. Select the feature you wish to delegate access to, then select the ellipses (…) at the top right.  
2. Select **Delegate access.**
3. Under **Share with**, type in the name or names of the people you want to assign as delegates. You can also add a personal note, but it’s not required.
4. Select **Submit**.

:::image type="content" source="images/delegate-access-1.png" alt-text="Screenshot showing delegate access box for Copilot Dashboard." lightbox="images/.png":::

## Second method for assigning delegates

This method not only allows you to assign delegates but add and remove delegates all on the same screen.

### Organizational insights & Copilot Dashboard:  

*Applies to: People with access to organizational insights or Copilot dashboard.*

1. In the Viva Insights app, select the ellipses (…) at the top right.
2. Select **Settings.**
3. Select **Delegate access.**
4. Here you can find your delegates and the start date of their access.
5. To add a new delegate, at the top right, select **Add new.**
6. To revoke access for an existing delegate, select the **Delete** (trashcan) icon.

:::image type="content" source="images/delegate-access-2.png" alt-text="Screenshot showing alternate method for delegating access." lightbox="images/.png":::

Whenever a delegate has been added, they will be notified in Team Chat of their current access status.

## Delegate access view

### Organizational Insights and Copilot Dashboard

*Applies to: People given delegate access*

1. If you're given delegate access, you receive an automated message in Teams from the manager who gave you access.
2. On the message, **select View insights**. You are then redirected to the manager’s view of the respective dashboard.  
3. In either dashboard on the top left, you will see a banner designed to inform you of which leader’s insights you’re viewing. Select either **View insights for** or **View Copilot Dashboard for**, in respective dashboard. If you're given delegate access by multiple leaders, select the banner to switch between different dashboards.

:::image type="content" source="images/delegate-access-3.png" alt-text="Screenshot showing whose insights you're viewing." lightbox="images/.png":::

>[!Note]
>The View Copilot Dashboard banner is only accessible from the Copilot dashboard and can’t be viewed anywhere else in the Viva app.

## Remove access to delegate Copilot Dashboard with Powershell

[Follow these steps to manage access to the delegate feature in Microsoft 365 admin center](/viva/feature-access-management).

>[!Important]
>Policies to disable delegation for Copilot dashboard can only be applied for the entire tenant level at this time.

You can set a policy to disable delegation for Copilot Dashboard for the tenant using Powershell cmdlets. This is a tenant-level policy, not a user or group-level policy. No users can delegate access to Copilot Dashboard until you remove or update the policy. Before you can use the cmdlet, you need to install a module and sign in to be authenticated. [Learn more about how to set these policies](/viva/feature-access-management).

1. [Connect to Exchange Online](../advanced/setup-maint/configure-personal-insights.md#connect-to-exchange-online) and when prompted, sign in with your admin credentials.

2. After you’ve signed in, you can manage access for your tenant using the Add-VivaModuleFeaturePolicy cmdlet:[Add-VivaModuleFeaturePolicy](/powershell/module/exchange/add-vivamodulefeaturepolicy). <!--Link not working-->

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

## Related topics
[Organization insights](org-insights.md)
