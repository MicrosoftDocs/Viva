---
title: Viva Glint for a multitenant organization FAQ (preview)
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

# Viva Glint for a multitenant organization FAQ (preview)

> [!NOTE]
> Multitenant organization for Viva Glint is available to preview customers only. Features described here are subject to change.

Multitenant organization (MTO) is a Microsoft 365 feature that enables your company to form a tenant group for access to Microsoft Viva Glint in your organization. 

## Why does my organization need to enable MTO for Glint?
The [multitenant organization (MTO) capability in Microsoft 365](/entra/identity/multi-tenant-organizations/multi-tenant-organization-overview) allows organizations to manage multiple tenants under a single umbrella enabling secure collaboration and resource sharing across these tenants. Tenant admins create an MTO policy in the target tenant and add source tenants. This option was created for Viva Glint customers to seamlessly access the product like they currently do in LinkedIn Glint.

## Are there any options for organizations who already use B2B collaboration or cross-tenant synchronization (CTS) to access Glint?
Customers with B2B Collab or cross-tenant synchronization (CTS) can access Viva Glint. The following shows the Glint dashboard access and experience for each customer sync type:

|Sync method   |Dashboard access and experience   |
|:----------|:-----------|
|**(Recommended)** An MTO policy and users synced with CTS or B2B collaboration.     |When logging into Glint with an MTO policy, users have to: <br><br> <ol><li>Enter credentials (Email and password)</li><li>Complete two-factor authentication</li><li>Access Glint</li></ol>       |
|No MTO policy and users synced with CTS or B2B collaboration.     |When logging into Glint without an MTO policy, Glint can't identify a user's tenant. Users have to:  <br><br> <ol><li>Choose the "Sign in to an organization" sign in option</li><li>Enter the target tenant domain name</li><li>Enter credentials (Email and password)</li><li>Complete two-factor authentication</li><li>Access Glint</li></ol>      |
|No sync method set up.    |**(Recommended)** Enable MTO and sync users with cross-tenant synchronization. [Learn more](glint-mto.md)    |

## If my organization chooses not to enable MTO, but uses B2B collaboration or CTS, can I send surveys to all users in multiple tenants?
Microsoft 365 admins can install Glint to only one tenant - the target tenant. Glint isn't installed to source tenants. To access Glint to create and send surveys to all tenants:

1. A Glint admin user must be logged into the target tenant, where Glint is installed.
1. All users from source tenants need to be synced to the target tenant with B2B collaboration or CTS and all users (across all tenants) must be imported to the Glint app.
1. Glint admins can send a survey to all synced users or selected users from the target tenant and need to complete all survey setup actions in the target tenant. These users receive the survey but may not be able to access depending on if the organization chooses sign-in using Microsoft Entra ID as a survey access method.

|Users synced with B2B collab or CTS  |HRIS import to Glint app complete  |Require Azure AD (Entra) for links in survey emails |Dashboard access for source tenant users |Survey access for source tenant users|
|:----------|:-----------|:-----------|:-----------|:-----------|
| Yes | No  | Yes | No | No |
| Yes  | No | No | No | No |
| No  | Yes  | Yes | No  | No |
| No  | Yes  | No | No | Yes |
| Yes | Yes  | Yes | Yes  | Yes |
| Yes | Yes  | No | Yes  | Yes |

## My organization doesn't use B2B collaboration or CTS but does have multiple tenants. Can all users access Glint?
No. Consider this scenario, where a customer has two tenants:

- Tenant A: The target tenant where Glint is installed
- Tenant B: The source tenant

If an organization has no sync method or MTO policy, only users in tenant A have access to Glint. All users in tenant B (including admins and dashboard users) don't have access to Glint because they aren't synced to target tenant A.

## My organization doesn't use B2B collaboration or CTS but does have multiple tenants. Can I still survey all users?
Yes, but only under certain circumstances. Consider this scenario, where a customer has two tenants:

- Tenant A: The target tenant where Glint is installed
- Tenant B: The source tenant

The tenant B admin doesn't have access to Glint to send surveys. The tenant A Glint admin can send all users across both tenants a survey if:

1. Users' HRIS data are imported to the Glint app.
   1. Without this step, tenant A admins can only send surveys to users in tenant A.
1. The tenant A Glint admin disables the requirement for users to sign in with Microsoft Entra ID to access surveys.
   1. If an organization doesn't disable this access method, tenant B users receive survey emails but aren't able to access the Glint app.

## Can we restrict MTO to just Glint? Does enabling MTO impact other Microsoft applications?
Restricting MTO to specific app isn't currently possible. MTO setup impacts synced users' experience in any apps or features integrated with MTO, such as Microsoft Teams, Search, and People card.

## How long does it take to set up MTO?
One working session of an hour with the Microsoft 365 or Entra Admin should be enough to enable MTO and test. But, factor in another session in case you run into any problems.

## How does MTO impact guest users? Can our organization add guest users without converting them to members?
MTO uses any B2B collaboration or CTS and doesn't automatically change the external user setup.

- B2B collaboration sets up the target tenant members as **external guest users** by default. These users are automatically added as external guests in MTO policy. Most customers don't hit the external guest maximum of 50,000 monthly average users (MAU). If an organization hits this limit, they can choose between keeping their guest users at an extra cost or converting them to member users.
- CTS sets up the target tenant members as **external member users** by default. These users are automatically added as external members in the MTO policy. There's an unlimited number of member users allowed.

Learn more:

- [Workforce tenant overview](/entra/external-id/what-is-b2b)
- [Properties of a B2B guest user](/entra/external-id/user-properties)

## Can I give dashboard access to users outside of my target tenant?
Yes. Admins need to add the users to the target tenant, import the users’ HRIS data to Glint, and share credentials with the users so they can access the Glint Dashboard.

**If source tenants are Microsoft Entra ID tenants:**
- Syncing users to the target tenant alone isn't enough because users still have their source tenant set to the home tenant.
- To allow users to access Glint in the target tenant, implement an MTO policy and a user sync with B2B collaboration or CTS.

**If source tenants aren't Microsoft Entra ID tenants:**
- Add users directly to the target tenant.
- An MTO policy and user sync aren't needed because these users have the target tenant as their home tenant in Entra.

## Can our organization set up one tenant now and add others later?
Yes. If you currently have multiple tenants, you can migrate and access Glint with your primary tenant to start with.

## Are there any licensing requirements?
To access Viva Glint, **a tenant does not need to have a P1 license**. The only requirement is for the target tenant to subscribe to Viva suite or Viva Glint. 

A P1 license is required to set up an MTO policy and if your organization accesses Viva Glint without MTO,  P1 licenses are only needed as required by sync policies. 

|Item |License requirements  |
|:----------|:-----------|
| MTO | Requires Microsoft Entra ID P1 licenses. Only one Microsoft Entra ID P1 license is required per employee per multitenant organization. Also, you must have at least one Microsoft Entra ID P1 license per tenant. [Learn more](https://go.microsoft.com/fwlink/?linkid=2282509).  |
| CTS only | Requires Microsoft Entra ID P1 licenses. Each user who is synchronized with cross-tenant synchronization must have a P1 license in their home/source tenant. [Learn more](https://go.microsoft.com/fwlink/?linkid=2286123). |
| B2B collab only  | Billing is based on monthly active users (MAU), which is the count of unique external users who authenticate to your tenants within a calendar month. To determine the total number of MAUs, we combine MAUs from all workforce and external tenants that are linked to a subscription. <br><br> For B2B collaboration in multitenant organizations, this billing model applies only to external users with a UserType of Guest. It doesn’t apply to external members that originate from within the multitenant organization, which have a UserType of Member.<br><br>External ID consists of a core offer and premium add-ons. The Microsoft Entra External ID core offering is free for the first 50,000 MAU. [Learn more](/entra/external-id/external-identities-pricing)   |
| No sync | No license requirement due to no sync options.  |

## Are there any additional costs associated with enabling MTO?
No.

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
