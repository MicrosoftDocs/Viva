---
ms.date: 04/18/2024
title: Organization-level permissions for creating OKRs and initiatives
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager: Liz.Pierce
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals
- highpri  
search.appverid:
- MET150
description: "Learn how to configure your OKR creation rules in Viva Goals"
---

# Organization-level permissions for creating OKRs and initiatives

Organization owners can set OKR creation permissions at the organization level, and both org owners and team owners can set create permissions at the team level. These permission settings determine which members can create OKRs and initiatives at the org level and at the team level.

## Organization-level OKR creation permissions

Organization owners configure permissions to determine who is allowed to create organization-level OKRs. They can decide to provide this permission to everyone in their org or only to specific people by choosing from the following options in the organization's settings:

* **Anyone in ORGANIZATION:** This is a good option for smaller organizations with evolving OKR needs.

* **Only team owners:** This is the default setting. Restricting OKR creation permissions to only Team owners is a safe option, as you're able to maintain a structured OKR planning and creation workflow.

* **Specific people (along with org admins & org owner):** This option is valuable when specific people or delegates are tasked with creating and managing OKRs for the organization.

> [!NOTE]
> Organization owners will always have the ability to create organizational OKRs and initiatives, regardless of which of the above options is selected.

## Set or manage OKR creation permissions for an organization

1. Navigate to the organization's OKRs page.

1. Select the **Settings** tab at the top of the page.

1. Under **Who can create organization OKR or Initiative?**, choose your preferred option and select **Save**.

:::image type="content" alt-text="Screenshot showing the options for organization-level OKR permissions." source="../media/goals/configure-okr-create-permissions/who-can-create-org-okr.png" lightbox="../media/goals/configure-okr-create-permissions/who-can-create-org-okr.png":::

## Team-level OKR creation permissions

Organization owners and team owners can set creation permissions at the team level to control who can create OKRs and initiatives for a specific team. You can learn more about the different types of teams in Viva Goals [here](viva-goals-teams-intro.md).

### Microsoft 365 group-connected teams

If the team is an M365 group-connected team, team owners can choose to provide OKR creation access to either of the following member subsets from the team's settings page.  

* **All team members:** Choose this option if the team is small and cross-functional, where every member of the team needs to create their own OKRs.

* **Only team owners:** Restricting OKR creation permissions to only the team owners is the default option, as team owners can maintain a structured OKR planning and creation workflow process.

### Native teams

For teams created within Viva Goals and not connected to any existing Microsoft 365 groups, team owners have the following options to choose from for OKR creation permissions:

* **Anyone in the organization:** Choose this option if the organization is small and cross-functional, where every user contributes to every team in the organization.

* **Team owners:** Restricting OKR creation permissions to only the team owners is the default option, as owners can maintain a structured OKR planning and creation workflow process.

* **Specific people (along with team owners):** This option helps admins keep a structured OKR planning and creation workflow by choosing specific people to have creation permissions for the team. For example:

  * **All members of this team:** This gives all members of this specific team creation permissions for that team, meaning that members of other teams in the org can't create OKRs for this team.

  * **Custom:** This lets you search for and select specific users anywhere in the organization and grant them the ability to create OKRs for this team.

> [!NOTE]
> Team owners will always have the ability to create OKRs and initiatives for their own teams, regardless of which of the above options is selected. Additionally, organization owners have the ability to create OKRs and initiatives for all teams within their organizations.

## Set or update OKR creation permissions for a team

1. Navigate to the specific team you want to set creation permissions for.  

1. Navigate to the team's settings by selecting the ellipsis (three dots) and choosing **Team settings**.

    :::image type="content" alt-text="Screenshot showing how to access a team's settings page." source="../media/goals/configure-okr-create-permissions/team-settings.png" lightbox="../media/goals/configure-okr-create-permissions/team-settings.png":::

1. Open the **Permissions** tab and navigate to the **Who can create OKR or Initiative for this team?** section. Select your preferred option.

    :::image type="content" alt-text="Screenshot showing the options for group-connected team-level OKR permissions.." source="../media/goals/configure-okr-create-permissions/who-can-create-team-okr.png" lightbox="../media/goals/configure-okr-create-permissions/who-can-create-team-okr.png":::

1. Select **Save**.

> [!NOTE]
> While the default team-level permission options are as described above, newly created teams with defined parent teams will inherit their parents' permissions as their defaults, even if the parent's permissions are different from the usual defaults.
