---
title: Use Microsoft Teams for Viva Glint (preview)
description: Bring survey notifications (invites, reminders, results notifications) and Nudges into the flow of work by integrating Microsoft Viva Glint and Microsoft Teams.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: Microsoft Teams, Teams bot, Teams survey invites, Teams Nudges, Glint and Teams integration
ms.collection:  
- Microsoft 365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 10/10/2024
ROBOTS: NOINDEX, NOFOLLOW
---

# Use Microsoft Teams for Viva Glint (preview)

> [!NOTE]
> This feature is available to preview customers only. Features described here are subject to change.

Bring survey notifications (invites, reminders, results notifications) and Nudges into the flow of work by integrating Microsoft Viva Glint and Microsoft Teams. Use the information in this article to have a Microsoft 365 admin install Viva Glint for Teams users in your organization and to enable Teams in the Viva Glint application.

## Install Microsoft Viva Glint for your organization in Teams

In the [Microsoft Teams admin center](https://admin.teams.microsoft.com/), your Microsoft 365 admin can install the Glint application for users in your organization. To install Glint for your organization: 

1. Go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/) and select **Teams Apps** and then **Setup Polices**.
1. Set up a policy (or modify an existing policy) to include the Viva Glint app for all users in your organization or a select group of users: [Manage app setup policies in Microsoft Teams](/microsoftteams/teams-app-setup-policies).
1. When the Glint app is installed for users, they receive a welcome message in Microsoft Teams.
   
   :::image type="content" source="../../media/glint/setup/teams-install-notice.png" alt-text="Screenshot of the Teams message that users receive when Viva Glint is installed to Microsoft Teams.":::

### Install Microsoft Viva Glint in Teams as an individual

Users who have Microsoft Teams licenses can access Viva Glint in Teams. To install the Glint app as a nonadmin user for your own instance of Microsoft Teams:

1. Go to **+ Apps** and search for Viva Glint. 
1. In the search results, select **Add** next to the Viva Glint app. 
1. To pin Viva Glint in the left side of Teams, select the ellipses (...) to view all unpinned apps.
1. Right click Viva Glint and select **Pin**. [Learn more about managing pinned apps](https://support.microsoft.com/office/pin-an-app-for-easy-access-in-microsoft-teams-3045fd44-6604-4ba7-8ecc-1c0d525e89ec).

## Enable Microsoft Teams in Viva Glint 

In the Viva Glint application, admins enable Microsoft Teams as a communication method in three places:

- In General Settings, to have Teams as a notification option overall for your organization.
- In the Communications tab for each survey that should include Teams notifications.
- In Recipient Groups for Nudges that should include Teams notifications. 
  - For organizations that don’t use [Nudges](/viva/glint/communicate/communicate-with-nudges), admins can skip this step.

### General Settings

To enable Microsoft Teams as a Viva Glint admin:

1. Select the **Configuration** symbol and in the **Service Configuration** section, choose **General Settings**. 
1. In the **Communications** section, switch the **Microsoft Teams** toggle to **Yes**.  
1. Select **Save Changes** in the top right of the **General Settings** page.
   
   :::image type="content" source="../../media/glint/setup/enable-teams-gen-settings.png" alt-text="Screenshot of the Microsoft Teams toggle switched to Yes in General Settings.":::

## Survey and Nudges settings

When Viva Glint admins enable Microsoft Teams in General Settings, admins can enable or disable Microsoft Teams as a communication channel in survey programs and Nudges.

> [!NOTE]
> Always-On surveys don’t include a Communications section or any notifications. Emails and Microsoft Teams messages aren’t available for this survey type.

### Survey programs 

To enable Microsoft Teams at the survey program level:

1. Select the **Configuration** symbol and in the **Surveys** section choose **Survey Programs**. 
1. Select a survey and go to the **Communications** section.  
1. In the **Channels** section, switch the **Microsoft Teams** toggle to **On**.
1. Select **Save Changes** in the top right of the **Communications** page.
   
   :::image type="content" source="../../media/glint/setup/enable-teams-surveys.png" alt-text="Screenshot of the Microsoft Teams toggle switched to On in the Communications section of a Glint survey.":::

### Nudges

To enable Microsoft Teams for Nudges:

1. Select the **Configuration** symbol and in the **Notifications** section, choose **Nudges**. 
1. Select **Edit Details** for the **Recipient Group** that should be updated.  
1. In the **Channels** section, switch the **Microsoft Teams** toggle to **On**.
1. Select **Save Changes** in the top left of the **Recipient Group Setup** page.
   
   :::image type="content" source="../../media/glint/setup/enable-teams-nudges.png" alt-text="Screenshot of the Microsoft Teams toggle switched to On in the Recipient Group Setup section for a Nudges recipient group.":::
