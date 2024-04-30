---
title: "Set up Viva Engage for a multitenant organization"
description: "How to set up Viva Engage for a multitenant organization."
ms.reviewer: ahosford
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 12/06/2023
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Set up Viva Engage for a multitenant organization

>[!IMPORTANT]
>Multitenant organization is available for Viva Engage on a roll-out basis. To configure this feature for your organization, contact your Microsoft Account Manager or Support.

Multitenant organization is a Microsoft 365 feature that allows complex and distributed organizations to communicate as a unified network. By configuring a tenant group in Microsoft 365 of trusted tenants in your organization, cross-tenant engagement is possible in Viva Engage. [Learn more about multitenant organizations](/entra/identity/multi-tenant-organizations/).

Complete these tasks in the order they appear. Administrator role requirements vary by task and are called out in each section.

> [!NOTE]
> This experience is only available by cohort-based rollout.

---

#### Tenants connect in hub-and-spoke model

Viva Engage uses a hub-and-spoke model to communicate across tenants. The *hub* rests at the center and is the tenant that generates most of the organization's content. The hub should be the tenant where your identified leaders (for example, corporate communicators, HR, and policy makers) reside.

*Spoke* tenants are the remaining networks. By using storyline and Leadership corner, leaders on the hub can broadcast content to all spoke tenants simultaneously, ensuring that information is distributed in a timely and efficient manner.

After the hub tenant is configured for multitenant organization, all tenants can communicate as a single, unified network.  

> [!NOTE]
> Only Storyline and Leadership corner are available for multi-tenant organization.

## Requirements

To access the multiple tenant organization feature for Viva Engage, your organization must meet these requirements across all tenants.

**Microsoft 365 requirements**
- Microsoft 365 E3 and Microsoft Entra ID P1. Or, Microsoft 365 E5 license (includes Microsoft Entra ID P2)
- Microsoft Entra ID manages all networks
- Microsoft Graph API

**Viva Engage requirements**

- Internal communications or IT manages Viva Engage
- Networks are in Native Mode
- Networks are not in a one-to-many state. Each tenant can have only one Viva Engage network. See [Network migration - Consolidate multiple Viva Engage networks](/viva/engage/configure-your-viva-engage-network/consolidate-multiple-networks).
- Full trust is established between all tenants. To establish full trust, [configure your organizational settings](/training/modules/secure-b2b-collaboration-cross-tenant-access/4-exercise-configure-organizational-settings).
- All users in all tenants have access to Microsoft Viva Suite or Communications and Communities
- Storyline is enabled on the hub tenant

## Prepare to set up a multitenant organization

*For Microsoft 365 Global administrators* 

This task assumes that all requirements for Microsoft 365 and Viva Engage are met.
When designing an effective multitenant organization, it’s crucial to establish a hub within the tenant where most essential communication originates. Leaders, corporate communicators, human resources, and policy makers drive most of the messaging for the organization. Therefore, these roles need to be in the hub tenant. Multitenant organization controls are available only to users internal to the hub tenant.

|Task description|Instructions|
|----------------|----------------|
|A. Plan out your multitenant organization.|See [Plan for multitenant organizations](/microsoft-365/enterprise/plan-multi-tenant-org-overview).|
|B. Determine the network configuration model for your organization.<br><br><br><br><br><br>|<ol><li>List all Microsoft Entra ID managed tenants in the organization.</li><li> Of the tenants in your organization, decide which one is the hub. Other tenants are considered spoke tenants.</li><li> For each spoke tenant, clarify the scope of users to synchronize to the Hub tenant. How you [configure multitenant organization in Microsoft Entra ID](/entra/identity/multi-tenant-organizations/) affects which users are able to participate in each tenant.</li>|
|C. Designate an Engage, global, or network administrator to configure the multitenant organization. This role must reside in the hub tenant.|If you need a new admin role, see how to [assign admin roles in Microsoft 365 admin center](/microsoft-365/admin/add-users/assign-admin-roles) or [PowerShell](/microsoft-365/enterprise/assign-roles-to-user-accounts-with-microsoft-365-powershell).|

## Configure the multitenant organization in Microsoft 365

*For Microsoft 365 Global administrators*

This process requires that you use Microsoft Graph API, an API with separate [requirements and prerequisites](/entra/identity/multi-tenant-organizations/multi-tenant-organization-overview). Learn more about [the Microsoft Graph API](https://techcommunity.microsoft.com/t5/intune-customer-success/support-tip-getting-started-with-microsoft-graph-api/ba-p/364257).

|Task description|Instructions|
|----------------|----------------|
|A. Configure the multitenant organization and participating tenants in the Microsoft 365 admin center.|<ol><li>Sign into the owner tenant and create a multitenant organization.</li><li>Add all tenants to the multitenant organization. See [Configure a multitenant organization using the Microsoft Graph API](/graph/use-the-api)|
|B.	Generate the multitenant organization trust policy. Configure the policy template to correspond to partner configurations.| Configure a policy from [these templates](/entra/identity/multi-tenant-organizations/multi-tenant-organization-configure-templates). |
|C. Synchronize across the multitenant organization.|See [Configure cross-tenant synchronization](/azure/active-directory/multi-tenant-organizations/cross-tenant-synchronization-configure).|
|D. If you run into problems, troubleshoot the issue.|See [Known issues for multitenant organizations](/entra/identity/multi-tenant-organizations/multi-tenant-organization-known-issues).|

## Configure Viva Engage for multitenant organization

*For Microsoft 365 Global administrators*

After you establish the multitenant organization in Microsoft 365, configure multitenant organization controls for Viva Engage on the tenant you've designated as the hub.
> [!NOTE]
> Licensing and other tenant-specific controls remain under control of that tenant’s admin. However, the spoke user license applies to the hub network.

|Task description|Instructions|
|----------------|----------------|
|On the designated hub tenant, configure Viva Engage to recognize the tenant as the hub.|<ol><li>In the Viva Engage Teams application, select the ellipses button from the top navigation menu and select **Admin**.</li><li>On the **Feature management** tab,  select the **MTO policy** tile.</li><li>Select the hub tenant.</li>|

## Configure the hub tenant for Storyline

*For the Engage, global, or network admin on the hub tenant*

From the hub tenant, configure Storyline settings to make announcements and leadership posts available across all tenants.

|Task description|Instructions|
|----------------|----------------|
|A.	Enable storylines for Viva Engage. |<ol><li>Sign in to as administrator.</li><li>Go to the [Viva Engage Admin center](/viva/engage/eac-as-access-eac).</li><li>On the Feature management tab, select **Storyline**.</li><li>Turn on the **Enable Storyline** toggle.</li>|
|B. Configure storylines for multitenant organization.|<ol><li>Follow the preceding steps 1-3 to go to the Storylines settings.</li><li>Select **Advanced settings**.</li><li>Under **Multi-tenant organizations (MTO)**, select the check box for **Let users on spoke tenants engage in storyline posts from this network**. For more details, see [Enable storyline](/viva/engage/eac-storyline#enable-storyline).</li>|

### Manage leadership for the multitenant organization

*For the Engage admin, verified admin, network admin, or corporate communicator*

On the hub tenant, enable audiences and specify the leaders whose storyline posts reach all tenants in the multitenant organization.  

|Task description|Instructions|
|----------------|----------------|
| A. Add leaders to the multitenant organization|<ol><li>Sign in to as administrator.</li><li>Go to the [Viva Engage Admin center](/viva/engage/eac-as-access-eac).</li><li>On the Feature management tab, select **Leadership identification and audiences**.</li><li>On the **Manage leaders** page, select **Add leader**, and type the leader’s name. When the name appears in the search, select the **Add** button next to it.</li><li>Select the **Edit** button next to that leader’s name.</li><li>Turn on **Entire organization:** [*TENANT_NAME*]. *Entire organization* refers only to the tenant that you're configuring. This option only enables the leader to communicate on the hub tenant.</li><li>Turn on **Multiple organizations** to enable the leader to communicate across all tenants in the multitenant organization from their storyline.</li>|
|B. Enable audiences for the multitenant organization|<ol><li>On the Feature management tab, go to **Leadership identification and audiences**, and select the **Manage audiences** page.</li><li>Turn on **Entire organization:** *[TENANT_NAME]*. *Entire organization* refers only to the tenant that you're configuring. In other words, this option enables the leader to communicate with the hub tenant.</li><li>Turn on **Multiple organizations** to let leader posts and announcements reach across all spoke tenants in the multitenant organization.|