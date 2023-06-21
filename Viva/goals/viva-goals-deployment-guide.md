---
ms.date: 03/30/2023
title: Viva Goals Setup and Administration Deployment Guide
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager: Liz.Pierce
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:  
- Strat_SP_modern
- M365-collaboration
- m365initiative-viva-goals
- highpri
search.appverid:
- MET150
description: "Learn how to get started with Viva Goals and set up a Viva Goals tenant."
---

# Viva Goals setup and administration deployment guide

This guide enables IT administrators to configure Viva Goals and help initial users get started using the program via the Setup and Administration guide. Additionally, it enables organization and team admins to understand how to configure their teams and organization so users can manage Objectives and Key Results (OKRs) using Viva Goals.

## Licensing requirements

To deploy Viva Goals, you must have one of the following licenses:

- Viva Suite license (or)
- Viva Goals license

## Configure tenant

The following admin target role(s) are used throughout this deployment guide. Learn more about the different [Microsoft 365 Admin roles](/microsoft-365/admin/add-users/about-admin-roles).

- Global Administrator
- License Administrator
- User Administrator
- Viva Goals Administrator

This section covers the following steps:

1. Assign Licenses
    1. Target role(s): Global or User Administrator

2. Assign Viva Goals Administrator (optional)
    1. Target role(s): Global or User Administrator

3. Configure Tenant settings
    1. Target role(s): Global or Viva Goals Administrator

## Assign licenses

To enable users to start using Viva Goals, Global or User Admins must assign licenses to the members of the relevant organizations or departments. Only users with a license can sign in and use Viva Goals.

To assign licenses to user:

1. In Microsoft 365 admin center click**Users -> Active users**.
1. Select the users or user group that you want to assign licenses to and select **Licenses and apps**.
1. Under Licenses, select **Viva Goals**

For more information on assigning licenses, check [assigning Microsoft 365 licenses to users](/microsoft-365/admin/manage/assign-licenses-to-users).

> [!TIP]
> Other ways of assigning licenses: 
>
> 1. To assign licenses via group-based licensing, see [Assign licenses to users by group in Azure Active Directory](/azure/active-directory/enterprise-users/licensing-groups-assign).
> 2. Target admin roles can also [assign Microsoft 365 licenses to user accounts with PowerShell](/microsoft-365/enterprise/assign-licenses-to-user-accounts-with-microsoft-365-powershell).

## Assign Viva Goals administrator (optional)

Viva Goals Administrators are assigned by Global admins or user admins from the Microsoft 365 Admin Center or Azure Active Directory. These are users typically from the IT team and manage the policy settings for Viva Goals for the entire company. 

This role is optional. It provides the minimal permissions required to manage Viva Goals and can be assigned to the person tasked with deploying and administering Viva Goals. In the absence of a separate Viva Goals Administrator, the Global admin can manage the Viva Goals policy settings for the company. 

For more information on various roles and their responsibilities on Viva Goals check [Roles and Permissions in Viva Goals](roles-permissions-in-viva-goals.md).

> [!NOTE]
> **Related content:** 
>
> - [Assign admin roles](/microsoft-365/admin/add-users/assign-admin-roles). 
> - [Azure AD roles in the Microsoft 365 admin center](/azure/active-directory/roles/permissions-reference)

### How to assign a Viva Goals administrator

1. In the Microsoft 365 admin center, go to **Role Assignments** section.
1. Search for **“Viva Goals Administrator"** on the role assignments page. Select Viva Goals Administrator from the search result.
1. In the flyout (right pane) that opens, select on the **Assigned** tab to assign licenses.
1. You can choose the **Add users** option to assign licenses to specific users. If you want to assign the license to a group choose the **Add groups** option. Users who haven't yet been assigned licenses can't be made administrators.

## Configure tenant settings

Once the Viva Goals Administrators have been assigned, a Viva Goals Administrator (or Global Administrator) can configure the tenant. To configure the tenant, complete the following steps:

- Review or Manage Org Creation Permissions
- Enable the Integrations applicable for the tenant
- Pin VG in Teams App

### Sign-in to Viva Goals

1. **Target role:** Viva Goals Administrator Or Global Administrator
1. After assigning yourself a license, sign in to Viva Goals using https://goals.microsoft.com

### Review or manage organization creation permissions

1. **Target role:** Viva Goals Administrator Or Global Administrator 
1. An Organization in Viva Goals resembles the topmost entity in an enterprise at which the organizational OKRs are set up and every team in that org aligns their OKRs with those organizational OKRs. Learn more about [Organizations in Viva Goals](understand-orgs-and-teams.md). 
1. Initially, there will be no organization created as the Viva Goals tenant is new. Select on the settings icon on top right corner of the screen to choose the type of permission you want to set for the overall tenant to control the creation of organization. 
    1. **Anyone in <Tenant_Name>:** This would allow any valid Viva Goals user to create Organizations.  
    1. **Specific users:** Sometimes, specific users may need to have Org creation permissions. Choose this option, and select the users who should have this capability.  
    1. **Only global administrators:** This option restricts Org creation to Global Admins, only.  
1. [How to restrict permissions in Viva Goals](restrict-organization-creation-permissions.md)

### Enable integrations for the tenant

1. **Target role:** Viva Goals Administrator or Global Administrator 
1. Viva Goals supports integrations with Microsoft and third-party apps and platforms so that the OKR implementation process is as simple, effective, and seamless as possible. 
1. As a Global or Viva Goals admin, you can control which integrations are available for use across organizations in Viva Goals.  
1. As a recommendation, enabling the integrations for all the tools being used in your company (or your company policy allows) can best empower the teams to run a super-efficient OKR program. 
1. For detailed instructions on enabling integrations, see the following article - [Viva Goals Integrations Administration Overview | Microsoft Learn ](vg-integrations-administration-overview.md)

### Install Viva Goals in Teams app

1. **Target role:** Global Administrator
1. Let users discover Viva Goals app on Microsoft Teams. Viva Goals is available as an app that can be added to MS Teams for users to easily view and manage OKRs right from the Teams app. Refer to this guide to [configure and setup Viva Goals app on MS Teams](configure-ms-teams-integration.md).

## Create Viva Goals organization

As a Global or Viva Goals administrator, you can create Viva Goals Organizations. If you would like to delegate the creation of Organization to specific users, then you can intimate the user to execute this step (provided they have enough permission).

> [!NOTE]
> The permission to create organization on Viva Goals depends on the setting/permission granted in the previous step (Manage Org creation permission)
  
1. Create a new organization for the teams to create, manage and track their OKRs.
1. Select Create Organization, provide a name for and description of the organization. 
1. The user who is creating the Organization is assigned the role of “Organization Owner” for the created organization. Learn more about [roles in Viva Goals](roles-permissions-in-viva-goals.md).
1. Choose who can join the organization 
    1. **Anyone in tenant:** Choose this option if there are no restrictions who in the tenant can join the organization and view or manage OKRs and initiatives. 
    1. **Restricted:** Choose this option if you want to require users to be manually added to organizations before they can start viewing or managing OKRs and initiatives.
1. Invite relevant licensed users who will be required to set up this organization and their OKRs. Viva Goals support adding individual members and user groups to the Organization. Learn more about [inviting users](inviting-and-removing-a-user.md).

### Assign two organization administrators 

1. It's a best practice to assign at least two administrators to an organization, which prevents dependency and bottlenecks to perform super user activities at the organization level.  
1. To create a new Organization administrator, Go to **Admin-> Users**, select the user, select on **Actions …  -> Make Admin**. 
1. If the intended user isn't already invited to the organization, invite the user, and then make them an admin.

### Transfer ownership of the organization 

1. Upon organization creation, Viva Goals sets the creator of the organization as the organization owner.  
1. To transfer ownership of an organization to a new user, identify the new owner of the created Viva Goals organization, invite the user if not done already.
    1. Go to **Admin -> Users**  
    1. Against the identified org owner, select on **Actions (..)**. – choose **Transfer Ownership.**
> [!NOTE]
> After completing this step, the original administrator will still be part of the organization as a regular member

## Configure your Viva Goals organization

**Target role(s):** Organization administrator

### Navigate to admin page

1. You can manage the properties of an organization on the Admin page. Select Admin on the left navigation bar to view and manage the organization-level settings. 
1. Learn more about the [admin dashboard](navigate-admin-dashboard.md). 

### Configure the type of org (Restricted/Public)

1. If you want to change the type of organization that was selected, earlier go to **Admin -> Settings**. 

### Configure integrations

1. Navigate to **Admin > Integrations** 
1. View available integrations 
1. Select **Enable** to activate and set up a connection for a specific integration that you want. Follow the on-screen setup steps. 
1. [Viva Goals integrations overview ](integrations-overview.md)

### Manage OKR time periods

1. To manage OKR time periods, visit: [Manage OKR time periods](managing-okr-time-periods.md)

### Configure usage of initiatives 

1. Initiatives help you keep track the work your organization is executing to achieve your objectives and key results (OKRs). Like key results, initiatives can also be created under objectives and under other key results in Viva Goals, depending on which outcome they help to achieve. 
1. Some organizations may not want to use initiatives and only stick with objectives and key results for simplicity and for other business reasons.  
1. To enable or disable initiatives in your Viva Goals organization, go to **Admin -> OKR Model Configuration**, under initiatives – choose to enable or disable.

### Configure OKR model

1. To configure your OKR model, visit: [Configure your OKR model in Viva Goals](configure-okr-model.md)

### Manage OKR creation permissions 

1. To manage your OKR creation permissions, visit: [Configure OKR create permissions](configure-okr-create-permissions.md)

### Control default user type 

Any user who joins your organization is by default considered as a member or regular user. You can choose to restrict the new users to be added as an observer instead.  

To do this, go to **Admin > Settings > User types** for new users and you can choose Observer.

|Role  |Description  |
|---------|---------|
|Members     |Members (the default role for everyone) can set up and manage their individual OKRs and view all OKRs within the organization.          |
|Observers     |Observers, as opposed to members, can't create, edit, or own OKRs. They can view all OKRs just like members.          |

For more information, visit: [Roles and Permissions](roles-permissions-in-viva-goals.md)

### Configure notification & Check-in rhythm 

1. To configure your notifications and check-in rhythms, visit: [Check-in reminders and notifications](check-in-reminders.md)

### Team creation permission 

A Team in Viva Goals is a group of users working towards a common set of team OKRs. The Team OKRs would directly or indirectly align to the organization OKRs. Learn more about [Viva Goals Teams.](understand-orgs-and-teams.md)

Administrators of the organization can control the team creation permission as follows: 

1. Select on **Admin** from the left side panel.
1. Under **Settings** tab, scroll down to find Team Creation and choose one or few of the following: 
    1. **Any Regular user:** Allow any regular member of the organization to create teams (This is the default selection) 
    1. **Admins:** Team creation is allowed for organization administrators 
    1. **Team Admins:** Team creation is allowed for team administrators 
    1. **Custom:** Chosen users have permission to create teams

### Create or edit teams 

Viva Goals supports multiple levels of hierarchy, from department level down to individual teams and functional units. To achieve this setup, you can use the teams and sub teams functionality. 

Once team is created, [add team admins](create-and-edit-teams-and-subteams.md) to the team who would be responsible to manage the team and its members.  At least two admins are recommended to avoid dependency on just one admin.

## Configure Viva Goals team(s)

**Target role(s):**Team Owner, Admins (primary)  

> [!NOTE]
> Organization admins have all the permissions of a team admin & owner but usually do not configure the teams. The owner or admin of a team is responsible for configuring and managing the team settings to help users manage team level OKRs and initiatives. More on [team admin and owners](roles-permissions-in-viva-goals.md).

### Manage team members 

1. Adding [team members to a team](create-and-edit-teams-and-subteams.md) & promoting a member as admin.

### Team level OKR creation permission

Admins of a team can restrict the OKR and initiative creation permission by following steps:

1. Navigate to the Team and select on the button with three dots (…) on the top right corner. Choose **Team Settings**
2. Under the heading **Who can create OKRs or Initiatives for this team?** Choose one of the following:
    1. **Anyone in <Organization_name>:** This option is the default permission for a Viva Goals Team. This allows any valid user of the Viva Goals organization to create OKRs or initiatives within the team. 
        1. **NOTE**: Users need not be a member of the team to create OKRs or initiatives
    1. **Only team admins and team owner:** This option restricts the OKR or initiatives creation permission only to the admins and owner of the team. Any other user of the organization or team can't create OKRs or initiatives if this option is selected.
    1. Specific people:
        1.  All members of this team:
            1. Along with team admins and owner, all members of the team can create OKRs or initiatives.
            1. **NOTE**: Users should be part of the team to let them create OKR or initiative. Know more on how to add users to a team.
        1. Custom:
            1. Along with team owner and admins, select individuals to assign permission to create OKRs or initiatives.
            1. Start typing the names of the users in the Add people text box and select the user from the list populated (the system would prompt if the user need to be invited to the organization if the entered user isn't found already).
            1. **NOTE**: The users need not be part of the team, but they need to be part of the organization.

### Team level check-in rhythm

Check-in reminder schedule can be tweaked for individual teams and, by default, the schedule set at the Viva Goals organization is applied for the teams.

1. Navigate to the Team.
1. Select on the button with three dots (…) on the top right corner. 
1. Choose **Team Settings**.
1. Under **Check-in Rhythm** section select on **Change schedule**.
1. Choose the interval (every week/two weeks/three weeks/month) and the corresponding day(s) and time on which the reminders should be sent.
1. Just below the interval selection, you can find the updated details about the reminder
1. Select **Change** to update the next check-in reminder date if needed.
1. You can also exempt certain OKRs and Initiatives created within specific number of days (From current date) from the next check-in reminder date to avoid sending the reminder too early. Select on the check box next to Don't include OKRs & Initiatives updated within the last.. - Choose the number of days from the drop-down.
1. Select **Save**

### Changing the parent and owner of a team

Viva Goals allows a team to be added as a child to another existing team and to change the team owner.

1. Navigate to the Team.
1. Select on the button with three dots (…) on the top right corner.
1. Choose **Team Settings**.
1. Under **Team Settings** section, you can find the drop-down for changing the team owner.

> [!NOTE]
> Only the current Team Owner has the permission to perform this action. Team admins do not have permission to change the team ownership.

5. To change the parent team, choose an existing Viva Goals team from the drop down menu under the heading Parent Team
6. Select **Save**