---
ms.date: 09/26/2023
title: Jira Server and Data Center Integration for Viva Goals
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
- vg-integration
search.appverid:
- MET150
description: "Learn how to integrate your OKRs in Viva Goals with Jira servers and data centers."
---

# Jira Server and Data Center Integration

> [!NOTE]
> Tenant administrator must enable both Jira and Jira Server integration from [Viva Goals tenant settings](vg-integrations-administration-overview.md) before it is visible on Viva Goals integration section on your Viva Goals organization.
> :::image type="content" source="../media/goals/jira-enable.png" alt-text="Enable Jira from the Viva Goals tenant settings page" lightbox="../media/goals/jira-enable.png":::

Jira Server and Jira Data Center enables automatic tracking of OKR and Initiative progress in Viva Goals from Jira user-stories or Epics. Any updates on the linked Jira user stories, epics, or projects will automatically update the progress of linked Viva Goals KRs and Initiatives. This ensures your OKR process isn't waiting on manual check-ins and any progress is updated real-time on Viva Goals.

## How to configure Jira Server or Data Center connection

1. The first step in setting up the integration is to connect your Jira Server or Data Center account to Viva Goals. Navigate to your sidebar and select **Admin** and then select **Integrations**.
1. In the integrations section, go to Jira and then select on **Enable**. If Jira is already enabled, you see a Manage button. Select on **Manage.**
1. Select 'New Connection' and in the pop-up dialog box, add the following details:
    1. **Connection name:** Give your connection name.  
    1. **Server:** Add your Jira Server URL.  
    1. **How is this Jira instance hosted?:** select 'Jira Server' option.
    :::image type="content" source="../media/goals/jira-integration/jira-server-with-details.png" alt-text="Screenshot of how to fill in the settings for a Jira server integration." lightbox="../media/goals/jira-integration/jira-server-with-details.png":::
    1. Save the connection by selecting **Next.**
    :::image type="content" source="../media/goals/jira-integration/connection-added.png" alt-text="Screenshot of a successfully connected Jira integration." lightbox="../media/goals/jira-integration/connection-added.png":::
    1. Open the connection by clicking the **Edit** button.
    :::image type="content" source="../media/goals/jira-integration/edit-connection.png" alt-text="Screenshot of how to edit a Jira integration once created." lightbox="../media/goals/jira-integration/edit-connection.png":::
    1. You'll need to use the **Account UUID** and **Access token** in the Jira configuration after you install the **Microsoft Viva Goals for JIRA** app from the Atlassian Marketplace.
    1. Switch to Jira Server or Data Center to install and configure **Microsoft Viva Goals for JIRA.**

## How to install and set up Microsoft Viva Goals for JIRA from the Atlassian Marketplace

1. As a Jira Server or Data Center administrator, search for **Microsoft Viva Goals for JIRA** app from the "Find new Apps" page in JIRA.
1. Select on the install button against the app and follow the steps in the confirm app installation popup.
1. After the installation is completed, select on **Get Started.**
    :::image type="content" source="../media/goals/jira-integration/jira-app.png" alt-text="Screenshot of the Jira app in the marketplace." lightbox="../media/goals/jira-integration/jira-app.png":::
1. Enter the Account UUID and Access Token copied from Viva Goals along with the Jira service account details and select Connect. Entering Jira service account is required so that the Microsoft Viva Goals for JIRA app can access Jira project details on behalf of Viva Goals. Here are the following details to be added:
    - **Jira username** = Add an existing Jira username.  
    - **Jira password** = Give the respective password for the account.

    :::image type="content" source="../media/goals/jira-integration/jira-app-filled-details.png" alt-text="Screenshot of the Jira app filled out." lightbox="../media/goals/jira-integration/jira-app-filled-details.png":::

    :::image type="content" source="../media/goals/jira-integration/connected.png" alt-text="Screenshot of the Jira app successfully connected." lightbox="../media/goals/jira-integration/connected.png":::

   > [!IMPORTANT]
   > Please note Jira service account user should have access to the Jira projects which you want to connect with Viva Goals so that the Microsoft Viva Goals for JIRA app has access to the Jira Server or Data Center project details.

1. Switch back to Viva Goals and check you can see the connection setup is successful by validating the **Verified** on the connection screen.
    :::image type="content" source="../media/goals/jira-integration/verfied.png" alt-text="Screenshot of a verified Jira to Viva Goals integration." lightbox="../media/goals/jira-integration/verfied.png":::

## Current limitations of Jira Server and Data Center integration

- The automatic sync for the first time happens within 10 minutes of connecting Jira with an OKR or Project and progress won’t be synced immediately in the first-time sync. However, you can also manually refresh to pull in all the updates by clicking on the Sync button in the integration pop-up.  
- Jira Server and Data Center integration support progress computation based on Tickets count and Story Points.
- A Jira Server instance can only be connected to one Viva Goals Organization at a time. If there's a need to connect the same Jira Server instance to another Viva Goals Organization, the existing connection must first be disconnected from the current Viva Goals Organization.

To more about latest Jira Server version updates please refer to https://www.atlassian.com/migration/assess/journey-to-cloud.

## Using the JIRA Integration

To understand how to connect a JIRA integration to an OKR, please see: [How to link the Jira connection to an OKR](jira-integration.md).

## FAQ (Frequently Asked Questions)

1. **I see an invalid credentials error though I'm using the right ones.**
    1. Check your service account permissions.
        1. Sign-in as a Service Account user on Jira and ensure the Jira Project(s) you want to query are accessible.
        1. Check the permissions by invoking the following query from one (or all) of the Jira nodes.
        1. Sample curl command (use the credentials of the service account or the respective user): curl -u username:password -X GET -H "Content-Type: application/json" https://test.com/rest/api/2/search?jql=project=ATP Replace https://test.com/rest/api/2/search?jql=project=ATP with Jira server URL along with the project jql

> [!IMPORTANT]
> 1. Firewall/VPN rules will prohibit users from reaching Viva Goals from the Jira server. To overcome that, you need to allowlist goals.microsoft.com.
> 1. We recommend enabling verbose logging for the Microsoft Viva Goals Plugin by following the steps below:
> 1. On the Jira Server, navigate to **Administration > System.**
> 1. Select **Logging and profiling.**
> 1. Scroll down to the **Default loggers** section.
> 1. Select **Configure logging level for another package.**
> 1. Enter “io.ally” as the package name and TRACE as the logging level.
> 1. Restart Jira nodes
> 1. To grep the logs, you may use the following string: tail –f log/atlassian-jira.log | grep “io\.ally”
