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
localization_priority: Priority
ms.collection:  
- m365initiative-viva-goals
search.appverid:
- MET150

description: "Learn how to use the Zendesk integration with your customer success OKRs."
---

# Zendesk Integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Viva Goals' Zendesk integration allows you to link Objectives and Key Results (OKRs) to customer success metrics available inside Zendesk for automatic real-time updates on the progress. For example, you have an objective to increase the customer satisfaction rate this quarter. You can implement a Zendesk integration to save yourself the hassle of repeatedly going back and forth between Zendesk and Viva Goals to update the progress: Viva Goals will sync the values for you, thus saving time while keeping your OKRs current.

## Set up

1. Navigate to Viva Goals’ integrations page through **Admin > Integrations**.

2. **Enable** the Zendesk Integration.

3. Select **New Connection** and in the popup that follows, enter the Zendesk subdomain and sign into your Zendesk account.

4. Name your connection and select **Next** to complete the setup.

    :::image type="content" source="../media/goals/viva-goals-zendesk-integration-1.png" alt-text="Zendesk Integration 1":::

    Viva Goals allows you to connect with multiple Zendesk accounts. Select **New connection** to add another instance and use names to differentiate them. These names are displayed to members when they link their OKRs to Zendesk.

    The integration may also be disabled at any time from the **Change** dropdown.

## How to use Zendesk Integration?

Now that the integration is enabled, your team can link a Zendesk metric with an OKR.

1. While adding or editing an Objective or Key Result, you should choose to measure success by **KPI (success metric)**.

    > [!NOTE]
    > At this time, you may only track by key performance indicator (KPI), not percentage completed. If you would like to use the Zendesk integration, Go ahead and add the integration.

    :::image type="content" source="../media/goals/viva-goals-zendesk-integration-2.png" alt-text="Zendesk Integration 2":::

2. Next, select the **Connection** and select the Zendesk metric you want to track the progress of the objective by. We support tracking by % Resolved tickets, % Satisfied Response, % Dissatisfied Response and Number of Dissatisfied Response in Zendesk for the agents in your organization for tickets created between a customizable date range. By default, we consider tickets created for all the agents between the start and end time same as the objective's start and end time.

    In the following example, we're tracking the percentage of satisfied responses inside Zendesk for all the agents between the specified time period.

    :::image type="content" source="../media/goals/viva-goals-zendesk-integration-3.png" alt-text="Zendesk Integration 3":::

3. Select **Next** to finish and save your OKR. You should now see a Zendesk icon next to the OKR. Now, Viva Goals will automatically track the % of satisfied response. The OKR syncs automatically every hour, but to refresh it manually select **refresh**.

    The colors of the progress bars indicate the status of the Objective in the following ways:

    - If the progress is 0-25% less than expected progress at any point in time, the status is Behind (orange).

    - If the progress is over 25% less than expected progress at any point in time, the status is At-Risk (red).

    Learn more about Viva Goals’ other integrations [here](http://help.gotoally.com/integrations).
