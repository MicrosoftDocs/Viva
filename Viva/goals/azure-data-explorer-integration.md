---
ms.date: 10/12/2022
title: Azure Data Explorer Integration
ms.reviewer: 
ms.author: daisyfeller
author: daisyfell
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-goals
ms.localizationpriority: high
ms.collection:  
- m365initiative-viva-goals
- vg-integration  
search.appverid:
- MET150
description: "Learn how to integrate your OKRs in Viva Goals with a cluster in Azure Data Explorer"
---

# Azure Data Explorer integration

## Introduction to Azure Data Explorer integration

The Viva Goals integration with Azure Data Explorer (also known as Kusto) allows you to link your OKRs in Viva Goals to a cluster and database in Azure Data Explorer and provides automatic, periodic updates on your OKRs.  

For example, if you have a Key Result to increase visits and the time spent in your app by 60%, then you can directly link this Key Result with the relevant data in Azure Data Explorer. This data is automatically synced with Viva Goals every hour. Whenever there's a change in the underlying dataset, the OKR status is updated. 

Admins also have permission to manage the integration from the admin dashboard. Once the integration is enabled for the Viva Goals instance, all users have access to this integration. 

## How to enable Azure Data Explorer

The Azure Data Explorer integration can be enabled by an admin. To do so,  

1. Go to Azure Data Explorer in the integrations section of the admin console. 

    :::image type="content" source="../media/goals/integrations-page-viva-goals.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/integrations-page-viva-goals.png":::

2. Select **Azure Data Explorer** and then select **Enable**.  

    :::image type="content" source="../media/goals/azure-data-explorer-enable.png" alt-text="Screenshot highlights the option to enable Azure Data Explorer in Viva Goals." lightbox="../media/goals/azure-data-explorer-enable.png":::   

## How to disable the integration 

The Azure Data Explorer integration can be disabled by an admin at any time. To disable the integration,  

1. Go to Azure Data Explorer in the integrations section.  

    :::image type="content" source="../media/goals/integrations-page-viva-goals.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/integrations-page-viva-goals.png":::

2. Select **Azure Data Explorer** and then select **Manage**.  

    :::image type="content" source="../media/goals/azure-data-explorer-manage.png" alt-text="Screenshot highlights the option to manage Azure Data Explorer in Viva Goals." lightbox="../media/goals/azure-data-explorer-manage.png":::

3. In the configurations page, select the **Change** dropdown, select **Disable** and confirm the action. 

    :::image type="content" source="../media/goals/azure-data-explorer-disable.png" alt-text="Screenshot highlights the option to disable Azure Data Explorer in Viva Goals." lightbox="../media/goals/azure-data-explorer-disable.png":::

## How to set up an Azure Data Explorer connection

The first step in setting up the Azure Data Explorer integration is to set up a connection. This can be done by an admin or any user during the create/edit OKR process.  If you’re a Viva Goals Organization admin: 

1. Navigate to your sidebar, and select **Admin** and then select **Integrations**. 

    :::image type="content" source="../media/goals/integrations-page-viva-goals.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/integrations-page-viva-goals.png":::

2. In the integrations section, go to Azure Data Explorer and then select **Enable**. If the integration has already been enabled, you have the option to **Manage** the integration. 

    :::image type="content" source="../media/goals/azure-data-explorer-enable.png" alt-text="Screenshot highlights the option to enable Azure Data Explorer in Viva Goals." lightbox="../media/goals/azure-data-explorer-enable.png":::   

3. Select **New Connection** and in the pop-up dialog box provide the full Azure Data Explorer URL (for example, ‘https://CLUSTERNAME.REGION.kusto.windows.net’). This cluster, together with the database provided during the OKR setup, will be the “base” cluster (i.e., your query runs from the context of this cluster).

    :::image type="content" source="../media/goals/azure-data-explorer-new-connection.png" alt-text="Screenshot highlights the new connection pop-up dialog." lightbox="../media/goals/azure-data-explorer-new-connection.png":::

4. After providing the URL, sign-in with your Microsoft Entra user credentials.  

>[!NOTE] 
>Viva Goals uses Microsoft Entra authentication to create an Azure Data Explorer Integration connection.  Whomever is setting up the connection must have access to the Azure Data Explorer cluster. 

5. After successful authentication, name your connection.  

    :::image type="content" source="../media/goals/azure-data-explorer-connection-name.png" alt-text="Screenshot highlights the pop-up dialog to provide a name for the connection." lightbox="../media/goals/azure-data-explorer-connection-name.png":::

6. Select **Next** to complete the new connection setup. 

## How to edit an existing Azure Data Explorer connection

Admins can delete existing connections. Users can only create new connections. 

If you're a Viva Goals Organization Admin, and you also own an existing connection, you can edit it as follows:

1. Select the **Edit** icon next to the Azure Data Explorer connection. 

    :::image type="content" source="../media/goals/azure-data-explorer-edit-icon.png" alt-text="Screenshot highlights the option to edit the Azure Data Explorer connection in Viva Goals." lightbox="../media/goals/azure-data-explorer-edit-icon.png":::

2. In the pop-up dialog box that follows, update the parameters as needed and select **Next**. 

## How to connect an existing Azure Data Explorer connection to an OKR

You can measure your OKRs progress by connecting your new or existing OKRs with an Azure Data Explorer database. 

1. Select Azure Data Explorer from the list of integrations available. Using the dropdown at the top of the dialog, select the appropriate connection. This connection defines the Azure Data Explorer cluster that contains your target database. If the connection you require isn't shown, you can create a new connection (see below).

    :::image type="content" source="../media/goals/select-azure-data-explorer-integration.png" alt-text="Screenshot highlights the selection of the Azure Data Explorer integration from the list of all integrations in Viva Goals." lightbox="../media/goals/select-azure-data-explorer-integration.png":::

2. Once you have selected your Azure Data Explorer connection, provide the database name (for example, ‘DataBaseName’) and the KQL query. Your query must return a single numeric value. 

    :::image type="content" source="../media/goals/ado-images/kusto-connection.png" alt-text="Screenshot highlights the details to be provided for the Azure Data Explorer connection." lightbox="../media/goals/ado-images/kusto-connection.png":::

>[!NOTE]
>The connection and the database establishes the context from which your query will be executed.  The user who sets up the connection must have access to any of the clusters/databases called from within the query. 

3. Select Next to finish and save your OKR. You’ll now see the Azure Data Explorer icon next to the OKR‘s progress indicator. This means Viva Goals will automatically measure the progress based on the data updates in the report. 

## How to set up a new Azure Data Explorer connection during the create/edit OKR flow  

If the desired Azure Data Explorer Integration connection isn't already established during the OKR setup, you can set up a new connection. 

1. Select **Azure Data Explorer** from the list of integrations available. Using the dropdown at the top of the dialog, select **Add new connection**. 

    :::image type="content" source="../media/goals/azure-data-explorer-new-connection-dropdown.png" alt-text="Screenshot highlights the dropdown to add the new Azure Data Explorer connection." lightbox="../media/goals/azure-data-explorer-new-connection-dropdown.png":::

2. In the next screen, provide the full Azure Data Explorer URL (for example, ‘https://CLUSTERNAME.kusto.windows.net’). This cluster, together with the database provided during the OKR setup, will be the “base” cluster (i.e., your query runs from the context of this cluster).   

3. After providing the URL, sign-in with your Microsoft Entra user credentials. 

4. Upon successful authentication, you are returned to the integration setup dialog, where you provide your database and KQL query as outlined above. 

## FAQ (Frequently asked questions)

1. **How do I fix sync issues?**
    1. Sync issues could occur due to multiple reasons:
        1. The device you used to create the connection(s) isn't compliant anymore.
        1. When you reset your Kusto password, the existing authentications go invalid automatically.
        1. The user who created the connection(s) isn't part of Microsoft Entra anymore.
    1. You can quickly fix these by reauthenticating the connection from **Account > Preferences > My Integrations >** select on**Manage against Kusto > Reauthenticate.**
