---
title: "Zendesk Integration"
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: <TBD>
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

description: "Learn how to use the Zendesk integration with your customer success OKRs."
---

# Zendesk integration

The Viva Goals Zendesk integration allows you to link Objectives and Key Results (OKRs) to customer success metrics available inside Zendesk for automatic real-time updates on the progress. 
    
Let's take this example: you have an objective to increase the customer satisfaction rate this quarter. You can implement a Zendesk integration to save yourself the hassle of repeatedly going back and forth between Zendesk and Viva Goals to update progress. Viva Goals will sync values for you, saving time and keeping your OKRs current.

## How to set up the Zendesk integration

1. Navigate to the Viva Goals integrations page through **Admin > Integrations**.
    
    :::image type="content" source="../media/goals/7/viva-goals-integrations-page.png" alt-text="Integrations page in Viva Goals." lightbox="../media/goals/7/viva-goals-integrations-page.png":::

2. **Enable** the Zendesk integration.
    
    :::image type="content" source="../media/goals/7/zendesk-enable-button-in-viva-goals.png" alt-text="Enabling Zendesk in Viva Goals." lightbox="../media/goals/7/zendesk-enable-button-in-viva-goals.png":::

3. Select **New Connection** and in the popup that follows, enter the Zendesk subdomain and sign into your Zendesk account.
    
     :::image type="content" source="../media/goals/7/zendesk-new-connection-button-in-viva-goals.png" alt-text="Creating a new Zendesk connection in Viva Goals." lightbox="../media/goals/7/zendesk-new-connection-button-in-viva-goals.png":::

4. Name your connection and select **Next** to complete the setup.
    
     :::image type="content" source="../media/goals/7/zendesk-creating-new-connection.png" alt-text="Filling in new Zendesk connection details in Viva Goals." lightbox="../media/goals/7/zendesk-creating-new-connection.png":::

5. Viva Goals allows you to connect with multiple Zendesk accounts. Select **New connection** to add another instance and use names to differentiate them. These names are displayed to members when they link their OKRs to Zendesk.
    
6. The integration may also be disabled at any time from the **Change** dropdown.
    
    :::image type="content" source="../media/goals/7/zendesk-disable-button-in-viva-goals.png" alt-text="Disabling Zendesk in Viva Goals." lightbox="../media/goals/7/zendesk-disable-button-in-viva-goals.png":::

## How to use the Zendesk integration

Now that the integration is enabled, your team can link a Zendesk metric with an OKR.

1. When adding or editing an Objective or Key Result, choose to measure success by **KPI (success metric)**.
    
    :::image type="content" source="../media/goals/7/zendesk-integration-from-the-list-of-integrations-in-viva-goals.png" alt-text="Selecting Zendesk from the list of data sources in Viva goals.png." lightbox="../media/goals/7/zendesk-integration-from-the-list-of-integrations-in-viva-goals.png":::

    > [!NOTE]
    > At this time, you may only track by key performance indicator (KPI), not percentage completed. 

2. Next, select the **Connection** and select the Zendesk metric you want to track the progress of the objective by. We support tracking by % Resolved tickets, % Satisfied Response, % Dissatisfied Response and Number of Dissatisfied Response in Zendesk for the agents in your organization for tickets created between a customizable date range. By default, we consider tickets created for all the agents between the start and end time same as the objective's start and end time.
    
    :::image type="content" source="../media/goals/7/zendesk-new-connection-details.png" alt-text="Adding Zendesk new connection to OKRs in Viva goals." lightbox="../media/goals/7/zendesk-new-connection-details.png":::

3. Select **Next** to finish and save your OKR. You should now see a Zendesk icon next to the OKR. Now Viva Goals will automatically track the % of satisfied response. The OKR syncs automatically every hour, but to refresh it manually select **refresh**.
