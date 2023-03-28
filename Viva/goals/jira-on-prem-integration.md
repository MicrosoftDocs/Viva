---
ms.date: 04/17/2022
title: "Jira Server and Data Center Integration for Viva Goals "
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
- m365initiative-viva-goals
search.appverid:
- MET150

description: "Learn how to integrate your OKRs in Viva Goals with Jira servers and data centers."
---

# Jira Server and Data Center Integration

> [!NOTE]
> Tenant administrator must enable Jira Server integration from [Viva Goals tenant settings](vg-integrations-administration-overview.md) before it is visible on Viva Goals integration section on your Viva Goals organization.

Jira Server and Jira Data Center enables automatic tracking of OKR and Initiative progress in Viva Goals from Jira user-stories or Epics. Any updates on the linked Jira user stories, epics, or projects will automatically update the progress of linked Viva Goals KRs and Initiatives. This ensures your OKR process is not waiting on manual check-ins and any progress is updated real-time on Viva Goals.

## How to configure Jira Server or Data Center connection 

1. The first step in setting up the integration is to connect your Jira Server or Data Center account to Viva Goals. Navigate to your sidebar and click **Admin** and then click **Integrations**.
1. In the integrations section, go to Jira and then click on **Enable**. If Jira is already enabled, you’ll see a Manage button. Click on **Manage.** 
1. Click 'New Connection' and in the pop-up dialog box, add the following details:
    1. **Connection name:** Give your connection name.  
    1. **Server:** Add your Jira Server URL.  
    1. **How is this Jira instance hosted?:** select 'Jira Server' option.
    :::image type="content" source="../media/goals/jira-integration/jira-server-with-details.png" alt-text="Screnshot of how to fill in the settings for a Jira server integration" lightbox="../media/goals/jira-integration/jira-server-with-details.png":::
    1. Save the connection by selecting **Next**
    :::image type="content" source="../media/goals/jira-integration/connection-added.png" alt-text="Screenshot of a successfully connected Jira integration" lightbox="../media/goals/jira-integration/connection-added.png":::
    1. Open the connection by clicking the **Edit** button.
    :::image type="content" source="../media/goals/jira-integration/edit-connection.png" alt-text="Screenshot of how to edit a Jira integration once created." lightbox="../media/goals/jira-integration/edit-connection.png":::
    1. You will need to use the **Account UUID** and **Access token** in the Jira configuration after you install the **Microsoft Viva Goals for JIRA** app from the Atlassian Marketplace. 
    1. Switch to Jira Server or Data Center to install and configure **Microsoft Viva Goals for JIRA.**

## How to install and setup Microsoft Viva Goals for JIRA from the Atlassian Marketplace

1. As a Jira Server or Data Center administrator, search for **Microsoft Viva Goals for JIRA** app from the "Find new Apps" page in JIRA.
1. Click on the install button against the app and follow the steps in the confirm app installation popup. 
1. After the installation is completed, click on **Get Started.**
    :::image type="content" source="../media/goals/jira-integration/jira-app.png" alt-text="Screenshot of the Jira app in the marketplace." lightbox="../media/goals/jira-integration/jira-app.png":::
1. Enter the Account UUID and Access Token copied from Viva Goals along with the Jira service account details and click Connect. Entering Jira service account is required so that the Microsoft Viva Goals for JIRA app can access Jira project details on behalf of Viva Goals. Here are the following details to be added: 
    - **Jira username** = Add an existing Jira username.  
    - **Jira password** = Give the respective password for the account.
    :::image type="content" source="../media/goals/jira-integration/jira-app-filled-details.png" alt-text="Screenshot of the Jira app filled out." lightbox="../media/goals/jira-integration/jira-app-filled-details.png"::: :::image type="content" source="../media/goals/jira-integration/connected.png" alt-text="Screenshot of the Jira app successfully connected." lightbox="../media/goals/jira-integration/connected.png":::

> [!IMPORTANT]
> Please note Jira service account user should have access to the Jira projects which you want to connect with Viva Goals so that the Microsoft Viva Goals for JIRA app has access to the Jira Server or Data Center project details.
>:::image type="content" source="../media/goals/jira-integration/verfied.png" alt-text="Screenshot of a verified Jira to Viva Goals integration." lightbox="../media/goals/jira-integration/verfied.png"::: 

## Current limitations of Jira Server and Data Center integration

- The automatic sync for the first time will happen within 10 minutes of connecting Jira with an OKR or Project and progress won’t be synced immediately in the first-time sync. However, you can also manually refresh to pull in all the updates by clicking on the Sync button in the integration pop-up.  
- Jira Server and Data Center integration will support progress computation based on Tickets count and Story Points 

To more about latest Jira Server version updates please refer to https://www.atlassian.com/migration/assess/journey-to-cloud

## Using the JIRA Integration 

To understand how to connect a JIRA integration to an OKR, please see: [How to link the Jira connection to an OKR](jira-integration.md)