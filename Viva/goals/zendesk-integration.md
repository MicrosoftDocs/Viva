---
ms.date: 04/17/2022
title: "Zendesk Integration"
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

description: "Learn how to use the Zendesk integration with your customer success OKRs."
---

# Zendesk integration

Viva Goals Zendesk integration lets you link objectives and key results (OKRs) to customer success metrics available in Zendesk for automatic real-time progress updates. 
    
Let's consider this example: You have an objective to increase the customer satisfaction rate this quarter. You can implement a Zendesk integration to save yourself the hassle of going back and forth between Zendesk and Viva Goals to update progress. Viva Goals will sync values for you, saving time and keeping your OKRs current.

## How to set up Zendesk integration

1. Go to the Viva Goals integrations page:  **Admin** > **Integrations**.
    
    :::image type="content" source="../media/goals/7/viva-goals-integrations-page.png" alt-text="Screenshot shows the integrations page in Viva Goals." lightbox="../media/goals/7/viva-goals-integrations-page.png":::

2. **Enable** Zendesk integration.
    
    :::image type="content" source="../media/goals/7/zendesk-enable-button-in-viva-goals.png" alt-text="Screenshot shows where you enable Zendesk in Viva Goals." lightbox="../media/goals/7/zendesk-enable-button-in-viva-goals.png":::

3. Select **New Connection**. In the dialog that appears, enter the Zendesk subdomain, and sign in to your Zendesk account.
    
     :::image type="content" source="../media/goals/7/zendesk-new-connection-button-in-viva-goals.png" alt-text="Screenshot shows where you opt to create a new connection to configure Zendesk integration." lightbox="../media/goals/7/zendesk-new-connection-button-in-viva-goals.png":::

4. Name your connection, and then select **Next** to complete setup.
    
     :::image type="content" source="../media/goals/7/zendesk-creating-new-connection.png" alt-text="Screenshot shows where you name your new Zendesk connection." lightbox="../media/goals/7/zendesk-creating-new-connection.png":::

5. Viva Goals lets you connect with multiple Zendesk accounts. Select **New connection** to add another instance. You differentiate connections by name. These names are displayed to users when they link their OKRs to Zendesk.

   You can disable the integration at any time from the **Change** dropdown.
    
    :::image type="content" source="../media/goals/7/zendesk-disable-button-in-viva-goals.png" alt-text="Screenshot shows how to disable Zendesk in Viva Goals." lightbox="../media/goals/7/zendesk-disable-button-in-viva-goals.png":::

## How to use Zendesk integration

Now that the integration is enabled, your team can link a Zendesk metric with an OKR.

1. When you add or edit an objective or key result, choose to measure success by **KPI (success metric)**.
    
    :::image type="content" source="../media/goals/7/zendesk-integration-from-the-list-of-integrations-in-viva-goals.png" alt-text="Screenshot shows where you specify Zendesk as the data source." lightbox="../media/goals/7/zendesk-integration-from-the-list-of-integrations-in-viva-goals.png":::

    > [!NOTE]
    > Currently you can only track by KPI, not percentage completed. 

2. Next, select the **Connection** and then select the Zendesk metric you want to track the progress of the objective by. Viva Goals supports tracking by *% resolved tickets*, *% satisfied response*, *% dissatisfied response*, and *number of dissatisfied Responses* in Zendesk for the agents in your organization for tickets created between a customizable date range. By default, Viva Goals considers tickets created for all the agents between the start and end time same as the objective's start and end time.
    
    :::image type="content" source="../media/goals/7/zendesk-new-connection-details.png" alt-text="Screenshot shows where you specify progress tracking details in Zendesk." lightbox="../media/goals/7/zendesk-new-connection-details.png":::

3. Select **Next** to finish and save your OKR. You should now see a Zendesk icon next to the OKR. Viva Goals will now automatically track the percent of satisfied response. The OKR syncs automatically every hour. To refresh it manually, select **refresh**.

