---
title: "Set up Viva Engage for a multitenant organization"
description: "How to set up Viva Engage for a multitenant organization."
ms.reviewer: ahosford
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 09/26/2024
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

Multitenant organization is a Microsoft 365 feature that allows complex and distributed organizations to communicate as a unified network. By configuring a group of trusted tenants in your organization in  Microsoft 365, you can communicate across those tenants in Viva Engage. Learn more about [multitenant organizations](/entra/identity/multi-tenant-organizations/).

#### Tenants connect in hub-and-spoke model

Viva Engage uses a hub-and-spoke model to communicate across tenants. The *hub* rests at the center and is the tenant that generates most of the organization's content. The hub should be the tenant where your identified leaders (for example, corporate communicators, HR, and policy makers) reside.

*Spoke* tenants are the remaining networks. By using storyline and Leadership corner, leaders on the hub can broadcast content to all spoke tenants simultaneously, ensuring that information is distributed in a timely and efficient manner.

After the hub tenant is configured for multitenant organization, all tenants can communicate as a single, unified network.  

> [!NOTE]
> Storyline, Leadership corner, campaigns, and communities are available for cross-tenant engagement in a multitenant organization. More features will be added soon.

## Requirements

To access the multiple tenant organization feature for Viva Engage, your organization must meet these requirements across all tenants.

**Microsoft 365 requirements**

- An Entra P1 or P2 license, which is included in Microsoft 365 E3 or E5, and Microsoft 365 F1 or F3 SKUs
- Microsoft Entra ID manages all networks
- Microsoft Graph API

**Viva Engage requirements**

- Internal communications or IT manages Viva Engage
- Networks are in Native Mode
- Networks are not in a one-to-many state. Each tenant can have only one Viva Engage network. See [Network migration - Consolidate multiple Viva Engage networks](/viva/engage/configure-your-viva-engage-network/consolidate-multiple-networks).
- Full trust is established between all tenants. To establish full trust, [configure your organizational settings](/training/modules/secure-b2b-collaboration-cross-tenant-access/4-exercise-configure-organizational-settings).
- All users in both hub and spoke tenants are assigned a *Microsoft Viva Suite* or *Communications and Communities* license
- Storyline is enabled on the hub tenant. Refer to [instructions in this article](/Viva/engage/mto-setup#configure-the-hub-tenant-for-storyline) after the multitenant organization is set up.

## Prepare to set up a multitenant organization

Complete these tasks in the order they appear. Since the role requirement varies by task, it's called out in each section.

*For Microsoft 365 Global administrators*

This task assumes that all requirements for Microsoft 365 and Viva Engage are met.
When designing an effective multitenant organization, it’s crucial to establish a hub within the tenant where most essential communication originates. Leaders, corporate communicators, human resources, and policy makers drive most of the messaging for the organization. Therefore, these roles need to be in the hub tenant. Multitenant organization controls are available only to users internal to the hub tenant.

|Task description|Instructions|
|----------------|----------------|
|A. Plan out your multitenant organization.|See [Plan for multitenant organizations](/microsoft-365/enterprise/plan-multi-tenant-org-overview).|
|B. Determine the network configuration model for your organization.<br><br><br><br><br><br>|<ol><li>List all Microsoft Entra ID managed tenants in the organization.</li><li> Of the tenants in your organization, decide which one is the hub. Other tenants are considered spoke tenants.</li><li> For each spoke tenant, clarify the scope of users to synchronize to the hub tenant. How you [configure multitenant organization in Microsoft Entra ID](/entra/identity/multi-tenant-organizations/) affects which users are able to participate in each tenant.</li>|
|C. Designate an Engage or network administrator on the hub tenant to configure the multitenant organization.|If you need a new admin role, see [Assign admin roles in Microsoft 365 admin center](/microsoft-365/admin/add-users/assign-admin-roles) or with [PowerShell](/microsoft-365/enterprise/assign-roles-to-user-accounts-with-microsoft-365-powershell).|

## Configure the multitenant organization in Microsoft 365

*For Microsoft 365 Global administrators*

Configuring the multitenant organization in Microsoft 365 requires Microsoft Graph API, which has its own [requirements and prerequisites](/entra/identity/multi-tenant-organizations/multi-tenant-organization-overview). Learn more about the [Microsoft Graph API](https://techcommunity.microsoft.com/t5/intune-customer-success/support-tip-getting-started-with-microsoft-graph-api/ba-p/364257).

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
> Licensing and other tenant-specific controls remain under control of that tenant’s admin. Hub users do not need a duplicate license in the spoke tenants, and spoke users do not need a duplicate license in the hub tenant.

|Task description|Instructions|
|----------------|----------------|
|On the designated hub tenant, configure Viva Engage to recognize the tenant as the hub.|<ol><li>In the Viva Engage Teams application, select the ellipses button from the top navigation menu and select **Admin**.</li><li>On the **Feature management** tab,  select the **MTO policy** tile.</li><li>Select the hub tenant.</li>|

## Configure the hub tenant for Storyline

*For the Engage or network admin on the hub tenant*

From the hub tenant, configure Storyline settings to make announcements and leadership posts available across all tenants.

|Task description|Instructions|
|----------------|----------------|
|A.	Enable storylines for Viva Engage. |<ol><li>Sign in to as administrator.</li><li>Go to the [Viva Engage Admin center](/viva/engage/eac-overview).</li><li>On the Feature management tab, select **Storyline**.</li><li>Turn on the **Enable Storyline** toggle.</li>|
|B. Configure storylines for multitenant organization.|<ol><li>Follow the preceding steps 1-3 to go to the Storylines settings.</li><li>Select **Advanced settings**.</li><li>Under **Multi-tenant organizations (MTO)**, select the check box for **Let users on spoke tenants engage in storyline posts from this network**. For more details, see [Enable storyline](/viva/engage/eac-storyline#enable-storyline).</li>|

## Configure leadership on the hub tenant

*For the Engage admin, verified admin, network admin, or corporate communicator*

On the hub tenant, enable audiences and specify the leaders whose storyline posts reach all tenants in the multitenant organization.  

|Task description|Instructions|
|----------------|----------------|
| A. Add leaders to the multitenant organization|<ol><li>Sign in to as administrator.</li><li>Go to the [Viva Engage Admin center](/viva/engage/eac-overview).</li><li>On the Feature management tab, select **Leadership identification and audiences**.</li><li>On the **Manage leaders** page, select **Add leader**, and type the leader’s name. When the name appears in the search, select the **Add** button next to it.</li><li>Select the **Edit** button next to that leader’s name.</li><li>Turn on **Entire organization:** [*TENANT_NAME*]. *Entire organization* refers only to the tenant that you're configuring. This option only enables the leader to communicate on the hub tenant.</li><li>Turn on **Multiple organizations** to enable the leader to communicate across all tenants in the multitenant organization from their storyline.</li>|
|B. Enable audiences for the multitenant organization|<ol><li>On the Feature management tab, go to **Leadership identification and audiences**, and select the **Manage audiences** page.</li><li>Turn on **Entire organization:** *[TENANT_NAME]*. *Entire organization* refers only to the tenant that you're configuring. In other words, this option enables the leader to communicate with the hub tenant.</li><li>Turn on **Multiple organizations** to let leader posts and announcements reach across all spoke tenants in the multitenant organization.|

## Enable communities for multitenant engagement

*For the Engage admin*

Only pre-existing communities on the hub tenant can be enabled for cross-tenant engagement. Once enabled, the community becomes private. Learn more about [Multitenant communities in Viva Engage](https://support.microsoft.com/en-us/topic/multitenant-communities-in-viva-engage-51462784-c566-44d0-a2cd-4d59dfc55fff).

|Task description|Instructions|
|----------------|----------------|
|A. Enable a community for a multitenant organization.|1. In the hub tenant, go to the community landing page.<br>2. From the options menu in the community header, select **Make visible to all organizations**.<br>3. Confirm the change. The community is now available to all tenants as a private community, which requires community members to be approved by the community admin.|
| B. Add community members|The Engage admin or the community admin can [add members in Microsoft 365 groups, with a CSV, or manually](https://support.microsoft.com/en-us/topic/manage-a-community-in-viva-engage-3e75fbe9-1b3e-48b5-8e4b-af2716b7873a). Alternatively, users on the hub and spoke tenants can request to join.|

## See also

[Limitations of multitenant organizations](/entra/identity/multi-tenant-organizations/multi-tenant-organization-known-issues)

[Microsoft Entra ID multitenant documentation](/entra/identity/multi-tenant-organizations/)
