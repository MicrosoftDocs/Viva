---
ms.date: 05/04/2023
title: Azure DevOps Extension
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
- m365initiative-viva-goals 
- vg-integration 
search.appverid:
- MET150
description: "With Viva Goals and Azure DevOps, you can automatically track progress of initiatives and key results in Viva Goals while ensuring that everyone using Azure DevOps has transparency to how their work items connect to the bigger picture. "
---

# Azure DevOps Extension

Automatically track progress of initiatives and key results in Viva Goals while ensuring that everyone using Azure DevOps has transparency to how their work items connect to the bigger picture.

> [!NOTE]
> To use the Azure DevOps Extension, the [Azure DevOps integration](/Viva/goals/azure-devops-integration) needs to be enabled. To do this, a Microsoft 365 Viva Goals admin must first enable the Azure DevOps integration for their tenant. Once enabled at the tenant level, a Viva Goals Organization admin must then [enable it for their organization](/viva/goals/vg-integrations-administration-overview).

## Install the Azure DevOps extension
You need permissions in Azure DevOps to install the extension. Learn more about [managing extension permissions](/azure/devops/marketplace/grant-permissions).

1. Go to the extension in the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=VivaGoals.viva-goals).
1. Select **Get it free**.
1. Select your Azure DevOps organization.
1. Select **Install**.

## Use the Viva Goals Extension
1. In Viva Goals, select **Create Initiative** (“Initiative” may be “Project” depending on your Viva Goals settings) and follow the steps in [How to enable Azure DevOps Integrations with Initiatives](/viva/goals/azure-devops-integration#how-to-enable-azure-devops-integration-with-initiative) to connect and automatically track progress in Viva Goals with data from Azure DevOps.
2. Go to an Azure DevOps work item.
3. Select the **Viva Goals** tab.
:::image type="content" source="../media/goals/azure-devops1.png" alt-text="Screenshot of a work item showing Viva Goals tab.":::

> [!NOTE]
> If you don't see the Viva Goals tab it could be because of one of two reasons:
>
> - Your work item form has a custom layout. Follow the steps in [Add extensions in work item form via work item type definition xml](/azure/devops/extend/develop/configure-workitemform-extensions).
> - A custom process is blocking the extension. From Azure DevOps Organization Settings, go to **Boards** and select **Process**. Then enable Viva Goals to **Show on layout**.

4. If the work item is directly connected or aligned to a work item that is connected to an initiative in Viva Goals, you'll see alignment information under **Viva Goals**. You can select any aligned OKR to view progress, perform check-ins, add comments, and directly from Azure DevOps.

   :::image type="content" source="../media/goals/azure-devops2.png" alt-text="Screenshot of a work item showing Viva Goals alignment information.":::

If your work item is not aligned to a Viva Goals initiative, select **Add Project in Viva Goals** to go to Viva Goals in a browser. Refer back to steps 1 and 2 to get started.

