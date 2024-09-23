---
ms.date: 05/30/2024
title: Viva Goals admin portal
ms.reviewer: 
ms.author: daisyfeller
author: daisyfell
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-goals
ms.localizationpriority: medium
ms.collection:  
- Strat_SP_modern
- M365-collaboration
- m365initiative-viva-goals
- highpri
search.appverid:
- MET150
description: "Learn how to access the admin portal for Viva Goals"
---

# Viva Goals admin portal

Viva Goals administrators can configure the Viva Goals policy settings for their companies from the Viva Goals admin portal page.

> [!NOTE]
> To lean more about the different roles and permissions available on Viva Goals, visit [Roles and permissions in Viva Goals](roles-permissions-in-viva-goals.md)

Settings that are managed from the Viva Goals admin portal include:

- [Configuring who can create organizations](restrict-organization-creation-permissions.md) within Viva Goals
- [Configuring integrations](vg-integrations-administration-overview.md) available for all Viva Goals organizations in the tenant
- Controlling the URLs that can be embedded in Viva Goals Dashboards
- Creating new organizations or managing existing organizations

## Access the Viva Goals admin portal

Only individuals with the permissions of Viva Goals administrators can access the admin portal. If you are an admin, you can open the admin portal by selecting the **Viva Goals Admin Center** icon in the top right corner of Viva Goals.

If you are using the Viva Goals app for Microsoft Teams, you can access the Viva Goals admin portal by selecting the icon on the title bar.

:::image type="content" source="../media/goals/admin-portal/admin-portal-ingress.png" alt-text="Screenshot highlighting the Admin Center icon in Viva Goals." lightbox="../media/goals/admin-portal/admin-portal-ingress.png":::

:::image type="content" source="../media/goals/admin-portal/teams.png" alt-text="Screenshot of accessing the admin portal from Teams." lightbox="../media/goals/admin-portal/teams.png":::

## Navigating the admin portal

The admin portal has three sections: General, Integrations, and Organizations.

### General

As a Viva Goals administrator, you can use this section to:

- [Choose who can create organizations](restrict-organization-creation-permissions.md).
- [Configure whether users are required to assign a team when creating an OKR](mandate-okr-team-assignment.md).
- [Approve domains to be embedded in dashboards](custom-url-widget.md).
- [Configure who can see Microsoft 365 Copilot in Viva Goals](copilot-intro.md#configuring-copilot-access-using-viva-feature-access-management).
- Configure whether OKRs are shared with Microsoft 365.
- Choose who can see Viva Goals in profile cards.
- Configure sharing permissions.

### Integrations

As a Viva Goals administrator, you can [choose which integrations](vg-integrations-administration-overview.md) are available for all Viva Goals organizations in the tenant.

### Organizations

As a Viva Goals administrator, you can use this section to:

- View the list of all organizations in the tenant. Select a record to view the organization information, such as the owner, admins, join access, number of teams, and members in the organization.
:::image type="content" source="../media/goals/admin-portal/organization-list-page.png" alt-text="Screenshot showing the list of all organizations in the tenant." lightbox="../media/goals/admin-portal/organization-list-page.png":::

- Modify the org owner or org admin for any organization in the list. For example, to add or remove owners for an organization, select the organization's name within the list, then select the current organization owner in the resulting pane. After that, search for and select (or deselect) anyone you want to be (or not be) an owner for the org.

- Assign yourself as an owner or admin should there be a need to directly administrate the org. This gives you complete managerial control over an organization.
:::image type="content" source="../media/goals/admin-portal/organization-list-update-owners.png" alt-text="Screenshot showing how to update owners for an org." lightbox="../media/goals/admin-portal/organization-list-update-owners.png":::

**Deactivate or delete an organization**

- You can deactivate an organization in Viva Goals using the steps below. Once you deactivate an organization, members of the org will not be able to access the org or change any of its content.
:::image type="content" source="../media/goals/admin-portal/deactivate-option.png" alt-text="Screenshot showing how to deactivate an org." lightbox="../media/goals/admin-portal/deactivate-option.png":::
:::image type="content" source="../media/goals/admin-portal/deactivation-confirmation-prompt.png" alt-text="Screenshot showing the org deactivation dialog." lightbox="../media/goals/admin-portal/deactivation-confirmation-prompt.png":::

- You can reactivate the deactivated organization within 90 days if you want to allow members to use the org again. If you don't, the organization and all its contents will be permanently deleted 90 days after deactivation.

- If you know you won't have any further use for the organization, you can delete it immediately. Note that company-wide organizations can't be deleted.

- You have the option to notify the organization owners via email during deactivation or reactivation. Upon deactivating an org, org owners will receive email notifications after deactivation, 15 days prior to deletion, and after permanent deletion.
:::image type="content" source="../media/goals/admin-portal/delete-and-reactivate-option.png" alt-text="Screenshot showing how to delete or reactivate a deactivated org." lightbox="../media/goals/admin-portal/delete-and-reactivate-option.png":::

**Automatically deactivate inactive organizations**

- You can configure settings such that organizations that have been inactive for more than a period of 60 days are automatically deactivated. To enable this automatic deactivation, select the **Organization Retention** menu from the left panel, then enable **Automatically deactivate organizations that are inactive for 60 days** within the page.

- You can also choose to notify the org owners. Upon the deactivation of an org, org owners will receive email notifications after deactivation, 15 days prior to deletion, and after permanent deletion.
:::image type="content" source="../media/goals/admin-portal/automatic-deactivation.png" alt-text="Screenshot showing how to toggle the automatic deactivation option." lightbox="../media/goals/admin-portal/automatic-deactivation.png":::
