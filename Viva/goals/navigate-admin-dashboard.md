---
title: Navigate the admin dashboard
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: 
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Learn how to navigate the admin dashboard"
---
# Navigate the admin Dashboard

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. Viva Goals is only being released to WW tenants. It isn't being released to GCC, GCC High, or DoD environments. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Organization admins have direct access to the Microsoft Viva Goals admin dashboard. The dashboard offers settings that can be customized for your organization, which creates efficiency and confidence in Microsoft Viva Goals.

Like other employees, you need to be familiar with:  
- The OKR framework  
- How to write great OKRs  
- Viva Goals software training 

Review the [Get Started with Viva Goals Learning path](/learn/paths/viva-goals-get-started) to dive deeper into these topics.  

## How to access and use the admin dashboard

To access the Viva Goals admin dashboard, navigate to the bottom of the left side panel and select **Admin** next to the gear icon.  

Organization admins configure the Viva Goals instance and have access to settings in the admin dashboard to set up users, teams, time periods, notifications, integrations, and OKRs, and projects. 

Here's our recommended first five steps for organization admins:  

1. Navigate your settings in the admin dashboard, and configure the instance according to your business rhythms:

1. [Invite users](inviting-and-removing-a-user.md)

1. [Create teams and assign users to them](create-and-edit-teams-and-subteams.md)

1. [Add OKRs](creating-okrs.md)

1. [Set up integrations](integrations-overview.md)
 
## Overview of the tabs in the admin dashboard

### Settings

The **Settings** tab lets you control general settings such as those related to the people and teams in your organization.  

- **Who Can Join This Organization** controls who is allowed to join your instance of Viva Goals and view your organization.  

- **Account Type for New Users** controls the default account type for new users. Viva Goals supports two account types: Regular user and observer. For more information on these account types, see our [roles and permissions article](roles-permissions-in-viva-goals.md). Whatever you choose can be changed later.  

- **Invite Policy** controls who can add users to your Viva Goals instance.  

- **Team Creation** is a feature that allows you to segment your organization into different workgroups and then add employees to those groups in Viva Goals. These groups will own team-level OKRs, and this setting controls who can create teams.  

- **Tag Creation** is a feature that allows you to categorize OKRs in buckets that you can later filter in a report.  
 
### Users  

On the **Users** tab, you'll find a list of all the individuals that have been added to your instance. This page also serves as a report, as you can use the **export** button to download a CSV file with people information. 

All of the information can be filtered using drop down menus such as role, account type, status and Manager.  

For example, if one of your users isn't sure if they got an invite, you could filter for users who have a status of "Pending."  

![Screenshot showing pending users alignment.](../media/goals/2/28/b.png)

As admin, you can use the action menu, marked by three dots, to modify the various settings.

![Screenshot showing the more actions menu.](../media/goals/2/28/b.png)

- **Cancel Invite** retracts an email that you sent.
- **Resend Invite** resends an invitation to join your instance.
- **Deactivate** locks a user out of Viva Goals. All their OKRs and historical information will remain, but they won't be able to log on. You might use this option for someone who has left the company. You can reactivate them if needed. You aren't billed for deactivated users.  
- **Edit** lets you view basic information about the employee, such as name and email, and you can assign teams from this view.  
- **Make Admin** lets you add or remove privileges from a user.  
- **Delete**  permanently deletes a user from Viva Goals.
- **Change to Observer** lets you change the type of user to observer or back to a regular user.  

### Teams

This tab shows all the teams that you've set up, plus the team owner and members. To add a new team, select the **Add Team** button. To modify team settings, select the ellipses next to a given team. Learn more at [Create and edit teams](/viva/goals/create-and-edit-teams-and-subteams).

### Notifications

The **Notifications** tab lets you customize the notifications that are sent to employees. Notifications is a critical feature that helps drive the rhythm of the business. In a perfect world, every employee consistently checks in their OKRs. But we know from experience that sometimes it takes a little nudge. Learn more at [Check in and track progress](/viva/goals/check-ins-and-progress-status).

### Integrations 

The **Integrations** tab lets you manage integrations in three categories:  

- Messaging integrations: MS Teams
- Data integrations: Asana, Jira, Salesforce, and more  
- Authentication integrations: Azure Active Directly only  

To learn more, see [Viva Goals integrations overview](/viva/goals/integrations-overview).

Two steps are required to start using most integrations. As an example, let’s say your company wants to integrate with Excel.

- **Step 1: The Excel integration must be enabled in the admin dashboard.** This option is a one-time, organization-level setting that essentially says, "I authorize the company to use Excel as an integration-with ally."

- **Step 2: The Excel integration can now be used at the individual level.** This option is a one-time, user-level setting that essentially says, "I want a certain OKR to pull data from Excel as an integration with Viva Goals."

As an admin, you can oversee and manage these integrations. To continue our Excel example, you could disable the integration for the whole company, add a new connection, or view existing connections and reauthenticate, edit, or delete them.

For a messaging integration like Microsoft Teams, you can add, edit, or delete notifications. Let's say you want to ring a virtual bell every time the sales team lands a sale. You can add a notification that does the following:

1. For the sales team...
2. Every time there’s a new check-in...  
3. Post that message to a specific sales team channel.

You can also enable private group notifications between users and their managers.

As a best practice, it’s a good idea to take a crawl, walk, run approach with integrations. While it may be tempting to see our long list of options and turn several on right away, first make sure your employees are comfortable with writing OKRs and using Viva Goals. From there, it can be useful to start with one group, such as Jira for the product team, before you roll out integrations to a larger audience.

### Time periods

Viva Goals includes both annual and quarterly time periods. Typically, organizations operate on an annual planning cadence, and departments/teams operate on a quarterly planning cadence. 

Admins can manage OKR time periods and customize them for your organization's requirements. Instead of the default quarterly periods, you could use monthly periods or define a custom time period.

To learn more, see [Manage OKR time periods](/viva/goals/managing-okr-time-periods) article.

### OKR model configuration

Viva Goals understands that every business has its own set of processes and lets you configure and create your own OKR rules to fit your business needs.

To learn more, see [Configure your OKR model in Viva Goals](/viva/goals/configure-okr-model).

### OKRs and projects 

Admins can determine whether to allow multiple teams and OKR owners to collaborate on key objectives and projects. Admins can also establish OKR [approval settings](manage-okrs-better-with-viva-goals-okr-workflows.md).  

To learn more about Projects, see [Projects](projects.md).
