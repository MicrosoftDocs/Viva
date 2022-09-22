---
title: Install and pin Viva Sales in Teams
description: Learn how to install and pin Viva Sales in Teams
ms.date: 08/01/2022
ms.topic: article
ms.service: viva
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# Install and pin Viva Sales in Teams

> [!IMPORTANT]
> Viva Sales is currently available only for public preview customers, and only in English. The features described here are subject to change.

The Viva Sales app is enabled in Teams but isn't installed automatically. You need to go to the Teams admin center and create setup policies to install the app and assign users. We also recommend that you pin it to increase discoverability and encourage your sellers to use it.

To install and pin the app in Teams, you'll [create a custom Teams app setup policy](disable-viva-sales.md) and [assign the policy to a user group](disable-viva-sales.md) (security group, organizational unit, or distribution list).

> [!NOTE]
> The Teams meeting must be recorded and transcribed for Viva Sales to generate insights. For information about enabling recording transcription for your organization, go to [Turn on or turn off recording transcription](/microsoftteams/cloud-recording#turn-on-or-turn-off-recording-transcription).

## Create a custom Teams app setup policy

1.  Sign in to the [Teams admin center](https://admin.teams.microsoft.com/dashboard).

2.  In the left pane, select **Teams apps** &gt; **Setup policies**.

3.  On the **Manage policies** tab, select **Add**.

4.  Enter a name and description for the policy.

5.  Turn on **User pinning**.

6.  Under **Installed apps**, select **Add apps**.

7.  In the **Add installed apps** panel, search for the **Viva Sales (Preview)** app. You can also filter apps by app permission policy.

8.  Select **Add** to add Viva Sales to the list of apps to install.

9.  Select **Add** again to install the listed apps.

10. Under **Pinned apps**, select **Add apps**.

11. In the **Add pinned apps** panel, search for the **Viva Sales (Preview)** app. You can also filter apps by app permission policy.

12. Select **Add** to add Viva Sales to the list of apps to pin.

13. Select **Add** again to pin the listed apps.

14. Under **App bar** or **Messaging extensions**, arrange the apps in the order that you want them to appear in Teams.

15. Select **Save**.

For more information about managing Teams app setup policies, go to [Manage app setup policies in Microsoft Teams](/microsoftteams/teams-app-setup-policies).

## Assign the custom Teams app setup policy to a user group

1.  Sign in to the [Teams admin center](https://admin.teams.microsoft.com/dashboard).

2.  In the left pane, select **Teams apps** &gt; **Setup policies**.

3.  On the **Group policy assignment** tab, select **Add**.

4.  Search for and add the group you want to assign the policy to.  
    Ideally, this is the group that sellers belong to. If your sellers are spread across multiple groups, you'll need to create multiple group policy assignments.

5.  Set the ranking for the group assignment.

6.  Select the policy you created earlier.

7.  Select **Apply**.

For more information about assigning user and group policies, go to [Assign policies to users and groups](/microsoftteams/assign-policies-users-and-groups).


### See also

[Install Viva Sales from Microsoft 365 admin center](install-viva-sales-individual-add-in-admin-center.md)<br>
[Install Viva Sales from AppSource](install-viva-sales-individual-add-in-appsource.md)