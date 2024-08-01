---
title: Set up Viva Glint for a multitenant organization (preview)
description: Multitenant organization (MTO) is a Microsoft 365 feature that enables you to form a tenant group within your organization.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: 
ms.collection:  
- Microsoft 365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 06/06/2024
ROBOTS: NOINDEX, NOFOLLOW
---

# Set up Viva Glint for a multitenant organization (Preview)

> [!NOTE]
> Multitenant organization for Viva Glint is available to preview customers only. Features described here are subject to change.

## Multitenant organization (MTO) 

Multitenant organization (MTO) is a Microsoft 365 feature that enables you to form a tenant group within your organization. By using MTO, users in a tenant group can access one instance of Microsoft Viva Glint installed in one tenant. Glint admins can survey and grant report access to employees across the tenant group for an organization-wide view of employee sentiment. Use the guidance in this article to learn more about multitenant organization, syncing users between tenants, requirements, and supported scenarios and how to implement them.  

Here are the primary reasons why an organization might have multiple tenants with more than one Microsoft Entra ID: conglomerates, mergers and acquisitions, divestiture activity, multiple clouds, multiple geographical boundaries, test or staging tenants, or department or employee-created tenants.  

Regardless of the reason for multiple tenants, users can experience access issues for applications that only exist in another tenant. Multitenant organization with cross-tenant synchronization or B2B collaboration provides a seamless experience for users that need to access Glint from another tenant.  

Meet with your Microsoft 365 Global Admin, IT, and HR stakeholders to determine your organization’s current tenant setup and consider:

- How many tenants your organization uses.
- Whether your employees exist in different tenants.
- What your Glint survey needs are across different tenants and employee populations.
- How you currently use Glint for organizational wide surveys.

### Requirements

- All tenants use Microsoft Entra ID.
- Glint is installed in one tenant where all Glint licenses used in the MTO are purchased (regardless of the home tenant of the user).

### Terminology

- Target tenant: The tenant where Glint is installed and where the Microsoft 365 global admin sets up an MTO policy.
- Source tenant: Any tenants with users that access Glint in the target tenant.

> [!IMPORTANT]
> - [Learn more about MTO limitations](/entra/identity/multi-tenant-organizations/multi-tenant-organization-known-issues).
> - Multiple installations of Glint on one tenant aren’t currently supported.

## Two options to sync users

There are two options to allow users from source tenants to access Glint on the target tenant: B2B collaboration or cross-tenant synchronization. Both options result in the creation of B2B collaboration users. Cross-tenant synchronization has the benefit of automatically updating users and removing them when they leave the organization.

### B2B collaboration

Manage users manually by uploading and inviting new users in bulk in the Microsoft Entra admin center.

#### Requirements:

For the **target tenant**:

- [Security Administrator](/entra/identity/role-based-access-control/permissions-reference#security-administrator) role to modify inbound access settings. 
- [User Administrator](/entra/identity/role-based-access-control/permissions-reference#user-administrator) role to bulk invite users.
- Two or more external test email accounts that you can send invitations to.

For the **source tenant**:

- [Security Administrator](/entra/identity/role-based-access-control/permissions-reference#security-administrator) role to modify outbound access settings.

For information on licensing, see: [B2B monthly active user (MAU) licensing](/entra/external-id/external-identities-pricing).

### Cross-tenant synchronization

Cross-tenant synchronization allows for automated B2B collaboration user management. User information from a source tenant is pushed to the target tenant where Glint is installed. 

#### Requirements: 

- Tenants must exist in the [same cloud](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-overview#frequently-asked-questions).
- Users in a source tenant are [internal members](/entra/external-id/user-properties) (syncing external uses isn’t supported).
- For the **source tenant**: 
  - [Security Administrator](/entra/identity/role-based-access-control/permissions-reference#security-administrator) role to set up cross-tenant settings. 
  - [Hybrid Identity Administrator](/entra/identity/role-based-access-control/permissions-reference#hybrid-identity-administrator) role to set up cross-tenant synchronization. 
  - [Cloud Application Administrator](/entra/identity/role-based-access-control/permissions-reference#cloud-application-administrator) or [Application Administrator](/entra/identity/role-based-access-control/permissions-reference#application-administrator) role to assign users to a configuration and delete configurations. 
- For the **target tenant**:  
  - [Security Administrator](/entra/identity/role-based-access-control/permissions-reference#security-administrator) role to set up cross-tenant settings.
 
Cross-tenant synchronization automates creating, updating, and deleting B2B collaboration users. [B2B monthly active user (MAU) licensing](/entra/external-id/external-identities-pricing) and [cross-tenant synchronization licensing](https://go.microsoft.com/fwlink/?linkid=2272785) apply.

## Supported scenarios

Glint supports multiple scenarios for multitenant organization with B2B collaboration or cross-tenant synchronization:

|Scenario   |MTO policy already set up   |User sync method |
|:----------|:-----------|:------------|
|[1](#scenario-1)     |No       |B2B collaboration        |
|[2](#scenario-2)     |No   |Cross-tenant synchronization |
|[3](#scenario-3)     |Yes   |B2B collaboration or cross-tenant synchronization|


> [!CAUTION]
> As a Glint admin, avoid access errors by ensuring that all users in the Microsoft Entra ID tenant - **including users from other tenants** - also exist in the Viva Glint application with an [HRIS upload](choose-upload-method.md).

### Scenario 1

An organization sets up an MTO policy between multiple tenants where Glint is installed on a target tenant (Tenant A). Users from one or more source tenants (Tenant B) are synced to Tenant A with B2B collaboration to access Glint.

:::image type="content" source="../../media/glint/setup/mto-scenario-1.png" alt-text="Diagram of tenant B users syncing to tenant A with B2B collaboration.":::

To set up multitenant organization for this scenario, complete these three tasks:

1. Read these articles, which guide Microsoft 360 Global Admins in specifying non-Viva Glint apps synced users have access to in the target tenant. They also let Microsoft 360 Global Admins what they should see in the target tenant's Microsoft Entra ID directory:
   1. [Cross-tenant access overview](/entra/external-id/cross-tenant-access-overview), especially the **Important considerations** section.
   2. [Configure B2B collaboration cross-tenant access](/entra/external-id/cross-tenant-access-settings-b2b-collaboration).
      > [!IMPORTANT]
      > This article only describes how synced users gain access to non-Viva Glint apps. Viva Glint access is controlled by ensuring that the Microsoft Entra IDs of synced users match employee data uploaded to the Glint app. Syncing users and uploading data to the Glint app are covered in tasks two and three.
   4. [Enable B2B external collaboration settings](/entra/external-id/external-collaboration-settings-configure).
   5. [Plan for multitenant organizations in Microsoft 365](/microsoft-365/enterprise/plan-multi-tenant-org-overview).
   1. [Configure cross-tenant access settings for B2B collaboration](/entra/external-id/cross-tenant-access-settings-b2b-collaboration).
   1. [Bulk invite guest users for B2B collaboration tutorial](/entra/external-id/tutorial-bulk-invite) 
1. Set up an MTO policy between Tenants A and B, and sync users.
1. Set up the Glint application.

Set up an MTO policy and sync users:

|Tenant   |User  |Step |Where to complete |
|:----------|:-----------|:------------|:------------|
|Tenant A     |Tenant A Microsoft 365 global admin   |1. [Set up MTO and add Tenant B](/microsoft-365/enterprise/set-up-multi-tenant-org?view=o365-worldwide#set-up-a-new-multitenant-organization&preserve-view=true) (source) and send info to Tenant B Microsoft 365 admin   |Microsoft 365 Admin Center (MAC)      |
|Tenant B     |Tenant B Microsoft 365 global admin   |2. [Join the MTO](/microsoft-365/enterprise/join-leave-multi-tenant-org?view=o365-worldwide#join-an-existing-multitenant-organization&preserve-view=true) set up by Tenant A  | MAC |
|Tenant A     |Tenant A Microsoft 365 global admin   |3. [Invite users in bulk](/entra/external-id/tutorial-bulk-invite) from Tenant B |Microsoft Entra admin center |
|Tenant A     |Tenant A Microsoft 365 global admin   |4. [Download and fill out csv template](/entra/external-id/tutorial-bulk-invite#understand-the-csv-template), start bulk operation, and confirm success.  | Microsoft Entra admin center |
|Tenant A     |Tenant A Microsoft 365 global admin   |5. [Verify guest users](/entra/external-id/tutorial-bulk-invite#verify-guest-users-in-the-directory) from Tenant B in directory | Microsoft Entra admin center |

Set up the Glint application:

|Tenant   |User  |Step |Where to complete |
|:----------|:-----------|:------------|:------------|
|Tenant A     |Tenant A Microsoft 365 global admin   |1. [Set up Viva Glint](viva-glint-tenant-provision.md) with licenses for all users from Tenants A and B    |[http://app.us1.glint.cloud.microsoft](http://app.us1.glint.cloud.microsoft) or [http://app.eu1.glint.cloud.microsoft](http://app.eu1.glint.cloud.microsoft)       |
|Tenant A     |Tenant A Microsoft 365 global admin   |2. [Assign Viva Glint admins](post-provisioning-next-steps.md)   | MAC |
|Tenant A     |Viva Glint admin   |3. [Upload employee data](choose-upload-method.md) for all users from Tenant A and B  |Glint |
|Tenant A     |Viva Glint admin    |4. [Assign user roles](set-up-user-roles.md)  | Glint |

### Scenario 2 

An organization sets up an MTO policy between multiple tenants where Glint is installed on a target tenant (Tenant A). Users from one or more source tenants (Tenant B) are synced to Tenant A with cross-tenant synchronization to access Glint. 

:::image type="content" source="../../media/glint/setup/mto-scenario-2.png" alt-text="Diagram of tenant B users syncing to tenant A with cross-tenant synchronization.":::

To set up multitenant organization for this scenario, complete these three tasks:

1. Read these articles, which guide Microsoft 360 Global Admins in specifying non-Viva Glint apps synced users have access to in the target tenant. They also let Microsoft 360 Global Admins what they should see in the target tenant's Microsoft Entra ID directory:
   1. [Cross-tenant access overview](/entra/external-id/cross-tenant-access-overview), especially the **Important considerations** section.
   2. [Configure B2B collaboration cross-tenant access](/entra/external-id/cross-tenant-access-settings-b2b-collaboration).
      > [!IMPORTANT]
      > This article only describes how synced users gain access to non-Viva Glint apps. Viva Glint access is controlled by ensuring that the Microsoft Entra IDs of synced users match employee data uploaded to the Glint app. Syncing users and uploading data to the Glint app are covered in tasks two and three.
   3. [Enable B2B external collaboration settings](/entra/external-id/external-collaboration-settings-configure).
   4. [Plan for multitenant organizations in Microsoft 365](/microsoft-365/enterprise/plan-multi-tenant-org-overview).
   1. [Configure cross-tenant synchronization](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure).
1. Set up an MTO policy between Tenants A and B, and sync users.
1. Set up the Glint application.


Set up an MTO policy and sync users:

|Tenant   |User  |Step |Where to complete |
|:----------|:-----------|:------------|:------------|
|Tenant A     |Tenant A Microsoft 365 global admin   |1. [Set up MTO and add Tenant B](/microsoft-365/enterprise/set-up-multi-tenant-org?view=o365-worldwide#set-up-a-new-multitenant-organization&preserve-view=true) (source) and send info to Tenant B Microsoft 365 admin   |Microsoft 365 Admin Center (MAC)      |
|Tenant B     |Tenant B Microsoft 365 global admin   |2. [Join the MTO](/microsoft-365/enterprise/join-leave-multi-tenant-org?view=o365-worldwide#join-an-existing-multitenant-organization&preserve-view=true) set up by Tenant A  | MAC |
|Tenant A     |Tenant A Microsoft 365 global admin   |3. [Enable cross-tenant sync (CTS)](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure#step-2-enable-user-synchronization-in-the-target-tenant), including [auto-redemption](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure#step-3-automatically-redeem-invitations-in-the-target-tenant) |Microsoft Entra admin center |
|Tenant B     |Tenant B Microsoft 365 global admin   |4. [Configure CTS](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure) and identify users to sync to Tenant A (target)  | Microsoft Entra admin center |
|Tenant B     |Tenant B Microsoft 365 global admin   |5. [Start provisioning job](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure#step-12-start-the-provisioning-job) | Microsoft Entra admin center |
|Tenant A     |Tenant A Microsoft 365 global admin   |6. Confirm that Tenant B (source) users exist in Tenant A (target) as B2B collab users | Microsoft Entra admin center |


Set up the Glint application:

|Tenant   |User  |Step |Where to complete |
|:----------|:-----------|:------------|:------------|
|Tenant A     |Tenant A Microsoft 365 global admin   |1. [Set up Viva Glint](viva-glint-tenant-provision.md) with licenses for all users from Tenants A and B    |[http://app.us1.glint.cloud.microsoft](http://app.us1.glint.cloud.microsoft) or [http://app.eu1.glint.cloud.microsoft](http://app.eu1.glint.cloud.microsoft)       |
|Tenant A     |Tenant A Microsoft 365 global admin   |2. [Assign Viva Glint admins](post-provisioning-next-steps.md)   | MAC |
|Tenant A     |Viva Glint admin   |3. [Upload employee data](choose-upload-method.md) for all users from Tenant A and B  |Glint |
|Tenant A     |Viva Glint admin    |4. [Assign user roles](set-up-user-roles.md)  | Glint |

### Scenario 3 

A multitenant organization (MTO) policy already exists between multiple tenants that sync users with B2B collaboration or cross-tenant synchronization. Glint is installed on a target tenant (Tenant A) that acts as owner of the MTO policy or both tenants are the owner of the MTO policy.

:::image type="content" source="../../media/glint/setup/mto-scenario-3.png" alt-text="Diagram of tenant B users syncing to tenant A with B2B collaboration or cross-tenant synchronization.":::

Since the multitenant organization is already set up, no other steps are needed. Here are the steps to set up the Glint application: 

|Tenant   |User  |Step |Where to complete |
|:----------|:-----------|:------------|:------------|
|Tenant A     |Tenant A Microsoft 365 global admin   |1. [Set up Viva Glint](viva-glint-tenant-provision.md) with licenses for all users from Tenants A and B    |[http://app.us1.glint.cloud.microsoft](http://app.us1.glint.cloud.microsoft) or [http://app.eu1.glint.cloud.microsoft](http://app.eu1.glint.cloud.microsoft)       |
|Tenant A     |Tenant A Microsoft 365 global admin   |2. [Assign Viva Glint admins](post-provisioning-next-steps.md)   | MAC |
|Tenant A     |Viva Glint admin   |3. [Upload employee data](choose-upload-method.md) for all users from Tenant A and B  |Glint |
|Tenant A     |Viva Glint admin    |4. [Assign user roles](set-up-user-roles.md)  | Glint |

## Related resources

**Cross-tenant access and multitenant organization**: 

- [Cross-tenant access overview](/entra/external-id/cross-tenant-access-overview), especially the **Important considerations** section.
- [Configure B2B collaboration cross-tenant access](/entra/external-id/cross-tenant-access-settings-b2b-collaboration).
- [Enable B2B external collaboration settings](/entra/external-id/external-collaboration-settings-configure).
- [Plan for multitenant organizations in Microsoft 365](/microsoft-365/enterprise/plan-multi-tenant-org-overview)
- [Configure a multitenant organization using PowerShell or Microsoft Graph API](/entra/identity/multi-tenant-organizations/multi-tenant-organization-configure-graph?tabs=ms-powershell)
- [What is a multitenant organization in Microsoft Entra ID?](/entra/identity/multi-tenant-organizations/multi-tenant-organization-overview)
- [Manage tenants in your Microsoft Customer Agreement billing account](/azure/cost-management-billing/microsoft-customer-agreement/manage-tenants#whats-a-tenant) 
- [Multitenant organization scenario and Microsoft Entra capabilities](/entra/identity/multi-tenant-organizations/overview)

**B2B collaboration**: 

- [Configure cross-tenant access settings for B2B collaboration](/entra/external-id/cross-tenant-access-settings-b2b-collaboration)
- [Bulk invite guest users for B2B collaboration](/entra/external-id/tutorial-bulk-invite)
- [B2B monthly active user (MAU) licensing](/entra/external-id/external-identities-pricing)

**Cross-tenant synchronization**: 

- [Configure cross-tenant synchronization](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure) 
- [Configure cross-tenant synchronization using PowerShell or Microsoft Graph API](/entra/identity/multi-tenant-organizations/cross-tenant-synchronization-configure-graph?tabs=ms-powershell)
- [B2B monthly active user (MAU) licensing](/entra/external-id/external-identities-pricing)
- [Cross-tenant synchronization licensing](https://go.microsoft.com/fwlink/?linkid=2272785)
