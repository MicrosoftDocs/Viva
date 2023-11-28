---
title: "Set up a multitenant organization for Viva Engage"
description: "How to set up Viva Engage as a multitenant organization."
ms.reviewer: ahosford
ms.author: v-bvrana
author: Starshine89
manager: pamgreen
ms.date: 11/27/2023
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Set up Viva Engage as a multitenant organization

[!NOTE] This experience is only available by cohort-based rollout.
Microsoft multitenant organization is a Microsoft 365 feature that allows complex and distributed organizations to communicate across tenants as a unified network. Each configuration task must be performed in the order it appears. Administrator role requirements are called out for each task.

#### Tenants connect in hub-and-spoke model

Viva Engage uses a hub-and-spoke model to communicate across tenants. In this model, the designated "hub" is the central tenant that generates official communication to the other "spoke" tenants. Leaders, corporate communicators, and policy makers reside on the hub tenant.

After the hub tenant is configured for multitenant organization, all tenants can communicate as a single unified network. Instead of posting a message in multiple places to ensure everyone’s notified, a leader can post an announcement from the hub tenant and simultaneously reach everyone across spoke tenants as if they were in the same tenant. (Note: Only Storyline and Leadership corner are available for multitenant organization.)

### Requirements

To access the multiple tenant organization feature for Viva Engage, your organization must meet these requirements across all tenants.

**Microsoft 365 requirements**
- Microsoft 365 E3 and Microsoft Entra ID P1. Or, Microsoft 365 E5 license (includes Microsoft Entra ID P2)
- Microsoft Entra ID manages all networks
- Microsoft Graph API

**Viva Engage requirements**
- Viva Engage is managed by an internal communications manager or your IT department
- Networks are in Native Mode
- Networks are not in a one-to-many state. Each tenant can have only one Viva Engage network. See [Network migration - Consolidate multiple Viva Engage networks](/viva/engage/configure-your-viva-engage-network/consolidate-multiple-networks).
- Full trust is established between all tenants. To establish full trust, [configure your organizational settings](/training/modules/secure-b2b-collaboration-cross-tenant-access/4-exercise-configure-organizational-settings).
- All users in all tenants have access to Microsoft Viva Suite or Communications and Communities
- Storyline is enabled

## 1: Prepare to set up a multitenant organization

*Applies to Microsoft 365 Global administrators* 

This task assumes that all requirements for Microsoft 365 and Viva Engage are met.
When designing an effective multitenant organization, it’s crucial to establish the hub within the tenant where most essential communication originates. Leaders, corporate communicators, human resources, and policy makers drive most of the messaging for the organization; therefore, they need to be in the hub tenant. Multitenant organization controls are available only to users internal to the hub tenant.

|Task description|Instructions|
|----------------|----------------|
|A. Plan out your multitenant organization.|See [Plan for multitenant organizations](/microsoft-365/enterprise/plan-multi-tenant-org-overview).|
|B. Determine the network configuration model for your organization.<br><br><br><br><br><br>|<ol><li>List all Microsoft Entra ID managed tenants in the organization.</li><li> Of the tenants in your organization, decide which one is the hub. Other tenants are considered spoke tenants.</li><li> For each spoke tenant, clarify the scope of users to synchronize to the Hub tenant.</li>|
|C. Create a hub tenant network administrator role in the Microsoft 365 admin center. The assigned user must reside in the hub tenant.|Assign a new admin role in [Microsoft 365 admin center](/microsoft-365/admin/add-users/assign-admin-roles) or with [PowerShell](/microsoft-365/enterprise/assign-roles-to-user-accounts-with-microsoft-365-powershell).|

## 2: Configure the multitenant organization in Microsoft 365

*Applies to Microsoft 365 Global administrators*

This process requires that you use Microsoft Graph API, an API with separate [requirements and prerequisites](/entra/identity/multi-tenant-organizations/multi-tenant-organization-overview). Learn more about [the Microsoft Graph API](https://techcommunity.microsoft.com/t5/intune-customer-success/support-tip-getting-started-with-microsoft-graph-api/ba-p/364257).

|Task description|Instructions|
|----------------|----------------|
|A. Configure the multitenant organization and participating tenants in the Microsoft 365 admin center.|<ol><li>Sign into the owner tenant and create a multitenant organization.</li><li>Add all tenants to the multitenant organization. See [Configure a multitenant organization using the Microsoft Graph API](/entra/identity/multi-tenant-organizations/multi-tenant-organization-configure-graph).</li>|
|B.	Generate the multitenant organization trust policy. Configure the policy template to correspond to partner configurations.|See [Cross-tenant access policy partner template](/entra/identity/multi-tenant-organizations/multi-tenant-organization-configure-templates#cross-tenant-access-policy-partner-template).|
|C. Synchronize across the multitenant organization.|See [Configure cross-tenant synchronization](/azure/active-directory/multi-tenant-organizations/cross-tenant-synchronization-configure).|
|D. If you run into problems, troubleshoot the issue.|See [Known issues for multitenant organizations](/entra/identity/multi-tenant-organizations/multi-tenant-organization-known-issues).|

### 3: Configure Viva Engage for multitenant organization

*Applies to Microsoft 365 Global administrators*

After you establish the multitenant organization in Microsoft 365, configure multitenant organization controls for Viva Engage from the designated hub tenant.
[!NOTE] Licensing and other tenant-specific controls remain under control of that tenant’s admin. However, the spoke user license applies to the hub network.

|Task description|Instructions|
|----------------|----------------|
|Designate the hub tenant in Viva Engage.<br><br><br><br><br><br>|<ol><li>Sign in as administrator.</li><li>In the Viva Engage Teams application, select the ellipses button from the top navigation menu and select **Admin**. </li><li>On the **Feature management** tab,  select the **MTO policy** tile.</li><li>Select the hub tenant.</li>

### 4: Configure the hub tenant for Storyline

*Applies to hub tenant network administrators*

From the tenant that’s designated as the hub tenant of the multitenant organization, configure Storyline settings to make announcements and leadership posts available across all tenants.

|Task description|Instructions|
|----------------|----------------|
|A.	Enable storylines for Viva Engage. |<ol><li>Sign in to as administrator.</li><li>Go to the [Viva Engage Admin center](/viva/engage/eac-as-access-eac).</li><li>On the Feature management tab, select **Storyline**.</li><li>Turn on the **Enable Storyline** toggle.</li>|
|B. Enable storylines for multitenant organization.|<ol><li>Follow the preceding steps 1-3 to go to the Storylines settings.</li><li>Select **Advanced settings**.</li><li>Select **Multitenant organization for storylines**. For more details, see [Enable storyline](/viva/engage/eac-storyline#enable-storyline).</li>|

### 5: Manage leadership for the multitenant organization

*Applies to Engage administrators, verified administrators, network administrators, and corporate communicators*

Specify the leaders whose storyline posts reach all tenants in the multitenant organization. Perform this task in the designated hub tenant of the multitenant organization.

|Task description|Instructions|
|----------------|----------------|
| A. Identify leaders in the multitenant organization<br><br><br><br><br><br><br><br><br><br><br><br>|<ol><li>Go to the [Viva Engage Admin center](/viva/engage/eac-as-access-eac).</li><li>On the Feature management tab, select **Leadership identification and audiences**.</li><li>On the **Manage leaders** page, select **Add leader**, and type the leader’s name. When the name appears in the search, select the **Add** button next to it.</li><li>Select the **Edit** button next to that leader’s name.</li><li>Turn on **Entire organization:** [*TENANT_NAME*]. *Entire organization* refers only to the tenant that you're configuring. This option only enables the leader to communicate on the hub tenant.</li><li>Turn on **Multiple organizations** to enable the leader to communicate across all tenants in the multitenant organization from their storyline.</li>

