---
title: Set up Viva Glint for a multitenant organization (preview)
description: Multitenant organization (MTO) is a Microsoft 365 feature that enables you to form a tenant group within your organization.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: MTO, multitenant organization, B2B collaboration, cross-tenant sync, FAQ
ms.collection:  
- Microsoft 365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 09/11/2024
ROBOTS: NOINDEX, NOFOLLOW
---

# Set up Viva Glint for a multitenant organization (preview)

> [!NOTE]
> Multitenant organization for Viva Glint is available to preview customers only. Features described here are subject to change.

Multitenant organization (MTO) is a Microsoft 365 feature that enables your company to form a tenant group in your organization. MTO allows users in a tenant group to access an instance of Microsoft Viva Glint installed in only one tenant. Glint admins can survey and grant report access to employees across the tenant group for an organization-wide view of employee sentiment. Use the guidance in this article to learn more about multitenant organization setup, syncing users between tenants, and ensuring all users exist in the Glint application. [Learn more about MTO](/entra/identity/multi-tenant-organizations/multi-tenant-organization-overview).

#### Terminology

- **Target tenant:** The tenant where Glint is installed and where the Microsoft 365 global admin sets up an MTO policy. 
- **Source tenant:** Any other tenants with users that access Glint in the target tenant.

### Get started

Select a step to jump to instructions for a specific part of multitenant organization setup for Viva Glint. 

|:::image type="icon" source="/office/media/icons/task-list-planning-blue.png" ::: |[Plan for MTO](#plan-for-mto)| :::image type="icon" source="/office/media/icons/administrator.png" ::: |[Set up MTO](#set-up-mto)| :::image type="icon" source="/office/media/icons/migration-blue.png" ::: |[Sync users](#sync-users) |:::image type="icon" source="/office/media/icons/users-people.png" ::: |[Import users from all tenants to the Glint app](#import-users-from-all-tenants-to-the-glint-app) |
|:---|:---|:---|:---|:---|:---|:---|:---|

### Plan for MTO

Meet internally with your MTO stakeholders, review requirements, and consider Glint survey access methods to plan for your MTO setup.

> [!NOTE]
> Multiple installations of Glint on one tenant aren’t currently supported.

| :::image type="icon" source="/office/media/icons/task-list-planning-blue.png" ::: |Step<br> <br> _roles involved_| More information |
|:---|:---|:---|
|:::image type="icon" source="/office/media/icons/meeting.png" ::: | **Meet with stakeholders** <br> <br>_Microsoft 365 global admin_ <br> <br>_Viva Glint admin_ <br> <br>_IT team members_ <br> <br>_Glint project team members_| Determine:<br> <br> <ul><li>How many tenants your organization uses</li> <li>Whether employees exist in different tenants</li> <li>What your Glint survey needs are across different tenants and employee populations</li> <li>How you currently use Glint for organization-wide surveys</li></ul>|
| :::image type="icon" source="/office/media/icons/compliance-blue.png" ::: | **Review requirements** <br> <br>_Microsoft 365 global admin_ | <ul><li>All tenants exist in the same cloud</li><li>All tenants use Microsoft Entra ID </li><li>Glint is installed in one tenant where all Glint licenses used in the MTO are purchased (regardless of the home tenant of the user)</li> <li>[Target and source tenant prerequisites](https://go.microsoft.com/fwlink/?linkid=2282429)</li><li>[License requirements](https://go.microsoft.com/fwlink/?linkid=2282509)<li>[Learn about MTO limitations](/entra/identity/multi-tenant-organizations/multi-tenant-organization-known-issues)</li> </ul>|
|:::image type="icon" source="/office/media/icons/users-settings.png" ::: | **Determine survey access methods and users to sync** <br> <br>_Viva Glint admin_ <br> <br>_Glint project team_ | <ul><li>**Authentication with Microsoft Entra ID**<br> _Survey takers must exist in Entra and in the Glint app_ <br></li> <li>**Personalized links**<br> _Survey takers need to exist in the Glint app only_ <br></li> <li>**Attribute-based survey access**<br> _Survey takers need to exist in the Glint app only_</li> <li>[Learn more about Glint survey access methods](/viva/glint/setup/understand-survey-access-methods)</li></ul><br> **All users that access survey results must exist in Entra**|

> [!TIP]
> See [Viva Glint for a multitenant organization FAQ](mto-faq.md) for answers to commonly asked MTO, cross-tenant sync, and B2B collaboration questions.

### Set up MTO

Microsoft 365 global admins can set up MTO in the Microsoft 365 admin center (MAC) or using the Microsoft Graph API. Setup in the Microsoft 365 admin center offers a user-friendly experience with simple and quick configuration steps. Microsoft Graph API configuration gives admins more granular control and advanced customization and automation options. Consider your organization’s level of complexity across tenants when choosing an MTO setup method.

> [!TIP]
> MTO setup in the Microsoft 365 admin center is recommended and is the most commonly used setup method.

> [!IMPORTANT]
> If your organization already uses B2B collaboration or cross-tenant synchronization to sync users, an MTO setup is still required. MTO and (an included MTO policy) identifies trusted domains and tenants.

| :::image type="icon" source="/office/media/icons/administrator.png" ::: |Step <br> <br> _roles involved_ | More information |
|:---|:---|:---|
|:::image type="icon" source="/office/media/icons/api.png" ::: | **Option 1: Set up MTO in MAC** <br> <br>_Target tenant Microsoft 365 global admin_ <br> <br>_Source tenant Microsoft 365 global admin_ | <ol><li>[As the target tenant admin, set up a new MTO in MAC](https://go.microsoft.com/fwlink/?linkid=2282609)</li> <li>[As the target tenant admin, add tenants to your MTO in MAC](https://go.microsoft.com/fwlink/?linkid=2282610)</li> <li>[As a source tenant admin, join an MTO](https://go.microsoft.com/fwlink/?linkid=2282430)</li></ol>|
|:::image type="icon" source="/office/media/icons/api.png" ::: | **Option 2: Set up MTO with the Microsoft Graph API** <br> <br>_Target tenant Microsoft 365 global admin_ <br> <br>_Source tenant Microsoft 365 global admin_ | <ol><li>As the target tenant admin, [sign in to the target tenant](https://go.microsoft.com/fwlink/?linkid=2282257) and [create an MTO](https://go.microsoft.com/fwlink/?linkid=2282047)</li> <li> [As the target tenant admin, add tenants to the MTO](https://go.microsoft.com/fwlink/?linkid=2282346)</li><li> As the source tenant admin, [sign in to the source tenant](https://go.microsoft.com/fwlink/?linkid=2282048) and [join the MTO](https://go.microsoft.com/fwlink/?linkid=2282347)</li><li> As the target tenant admin, [setup a cross-tenant access policy](https://go.microsoft.com/fwlink/?linkid=2282049) and [configure inbound user sync](https://go.microsoft.com/fwlink/?linkid=2282348)</li></ul>|


### Sync users

There are two options to sync users for MTO and Viva Glint: B2B collaboration or cross-tenant synchronization. Both options result in the creation of [B2B collaboration users](/entra/external-id/user-properties). Cross-tenant synchronization automatically updates users and removes them when they leave the organization. Review prerequisites for each method:

- [cross-tenant synchronization prerequisites](https://go.microsoft.com/fwlink/?linkid=2282614)
- [B2B collaboration prerequisites](https://go.microsoft.com/fwlink/?linkid=2282432)

> [!TIP]
> Cross-tenant synchronization is recommended and offers a more automated and streamlined user sync method.

> [!IMPORTANT]
> - If your organization already has cross-tenant synchronization set up for users that need to access Glint in the target tenant, skip this step.
> - If your organization uses [B2B direct connect](/entra/external-id/b2b-direct-connect-overview), accounts for source tenant users aren't created in the target tenant. Cross-tenant synchronization is still needed to sync users and doesn't affect any existing B2B direct connect setups. 

| :::image type="icon" source="/office/media/icons/migration-blue.png" ::: |Sync option <br> <br> _roles involved_| More information |
|:---|:---|:---|
|:::image type="icon" source="/office/media/icons/users-people.png" ::: | **Option 1: cross-tenant synchronization (CTS)** <br> <br>_Target tenant Microsoft 365 global admin_ <br> <br>_Source tenant Microsoft 365 global admin_ | <ol><li>As the target tenant admin, [enable CTS in the target tenant](https://go.microsoft.com/fwlink/?linkid=2282434)</li> <li>As target tenant admin, [enable autoredemption in the target tenant](https://go.microsoft.com/fwlink/?linkid=2282510) </li><li>As the source tenant admin, [enable autoredemption in the source tenant](https://go.microsoft.com/fwlink/?linkid=2282616)</li><li>As the source tenant admin, [set up CTS in the source tenant](https://go.microsoft.com/fwlink/?linkid=2282511) and [test the connection to the target tenant](https://go.microsoft.com/fwlink/?linkid=2282617)</li> <li>As the source tenant admin, [define who's in scope for provisioning](https://go.microsoft.com/fwlink/?linkid=2282435) and [test on demand provisioning](https://go.microsoft.com/fwlink/?linkid=2282512)</li><li>As the source tenant admin, [start the provisioning job](https://go.microsoft.com/fwlink/?linkid=2282436) to sync users to the target tenant</li> <li>As target and source tenant admins, [verify users in the target tenant and monitor the provisioning job](https://go.microsoft.com/fwlink/?linkid=2282437)</li></ol>|
|:::image type="icon" source="/office/media/icons/upload-blue.png" ::: | **Option 2: B2B collaboration** <br> <br>_Target tenant Microsoft 365 global admin_ <br> <br>_Source tenant Microsoft 365 global admin_ | <ol><li>In the target and source tenants, [confirm that autoredemption is selected in cross-tenant access settings](https://go.microsoft.com/fwlink/?linkid=2282349)</li><li>As the target tenant admin, [prepare a comma-separated value (.csv) file with user information](https://go.microsoft.com/fwlink/?linkid=2282050)</li> <li>As the target tenant admin, [upload the file to Microsoft Entra ID](https://go.microsoft.com/fwlink/?linkid=2282051)</li><li>As the target tenant admin, [confirm that users are added to the directory](https://go.microsoft.com/fwlink/?linkid=2282052)</li></ol>|


### Import users from all tenants to the Glint app

To successfully access surveys and results, all users need to be imported to the Glint application, regardless of their home tenant. Glint offers two methods to import users:

| :::image type="icon" source="/office/media/icons/users-people.png" ::: |Import method <br> <br> _roles involved_| More information|
|:---|:---|:---|
|:::image type="icon" source="/office/media/icons/database.png" ::: | **Secure File Transfer Protocol (SFTP)** <br> <br>_Viva Glint admin_ <br> <br>_HR information system team_| <ul><li>[SFTP and data automation](/viva/glint/setup/sftp-data-automation)</li></ul> |
|:::image type="icon" source="/office/media/icons/files-blue.png" ::: | **People page import** <br> <br>_Viva Glint admin_ | <ul><li>[People page import in the Glint platform](/viva/glint/setup/upload-employee-attributes)</li> </ul>|

### Related resources

**Cross-tenant access and multitenant organization**: 

- [Cross-tenant access overview](/entra/external-id/cross-tenant-access-overview), especially the **Important considerations** section.
- [Configure B2B collaboration cross-tenant access](/entra/external-id/cross-tenant-access-settings-b2b-collaboration).
- [Enable B2B external collaboration settings](/entra/external-id/external-collaboration-settings-configure).
- [Plan for multitenant organizations in Microsoft 365](/microsoft-365/enterprise/plan-multi-tenant-org-overview)
- [Configure a multitenant organization using PowerShell or Microsoft Graph API](/entra/identity/multi-tenant-organizations/multi-tenant-organization-configure-graph?tabs=ms-powershell)
- [What is a multitenant organization in Microsoft Entra ID?](/entra/identity/multi-tenant-organizations/multi-tenant-organization-overview)
- [Manage tenants in your Microsoft Customer Agreement billing account](/azure/cost-management-billing/microsoft-customer-agreement/manage-tenants#whats-a-tenant) 
- [Multitenant organization scenario and Microsoft Entra capabilities](/entra/identity/multi-tenant-organizations/overview)
- [Viva Glint for a multitenant organization FAQ](mto-faq.md)

**B2B collaboration**: 

- [Configure cross-tenant access settings for B2B collaboration](/entra/external-id/cross-tenant-access-settings-b2b-collaboration)
- [Bulk invite guest users for B2B collaboration](/entra/external-id/tutorial-bulk-invite)
- [B2B monthly active user (MAU) licensing](/entra/external-id/external-identities-pricing)

**Cross-tenant synchronization**: 

- [Configure cross-tenant synchronization](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure) 
- [Configure cross-tenant synchronization using PowerShell or Microsoft Graph API](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure-graph?tabs=ms-powershell)
- [B2B monthly active user (MAU) licensing](/entra/external-id/external-identities-pricing)
- [Cross-tenant synchronization licensing](https://go.microsoft.com/fwlink/?linkid=2272785)
