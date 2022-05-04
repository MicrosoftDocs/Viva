---
title: "Google Sheets Integration"
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

description: "Learn how to work smarter by integrating Google Sheets with Viva Goals."
---

# Google Sheets integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

The Viva Goals Google Sheets integration allows you to link Objectives and Key Results (OKRs) to Google Sheet cells for real-time updates of progress. 

Let's take this example: you have a sales sheet used to track revenue. By implementing a Google Sheet integration, you can save yourself the hassle of repeatedly going back and forth between your Google Sheets and Viva Goals to update your progress. Viva Goals will sync the values for you, thus saving time while keeping your OKRs current.

## How to set up the Google Sheets integration

1. Navigate to Viva Goals’ integrations page from **Admin > Integrations**.

2. **Enable** the Google Sheets Integration.

3. Select **New Connection** and in the popup that follows, follow the prompt to sign into Google.

4. Name your connection and hit **Next** to complete setup.

Viva Goals allows you to connect with multiple Google Sheets accounts. Select **New connection** to add another instance and use names to differentiate them. These names are displayed to members when they link their OKRs to Google Sheet cells.

> [!NOTE]
> Connections can be public or private to everyone in the organization with the **Share Connection with all users** option.

The integration may also be disabled at any time from the **Change** dropdown.

## How to use the Google Sheets Integration

Now that the integration is enabled, your team can link a Google Sheet cell with an OKR.

1. While adding or editing an Objective or Key Result, select **track by KPI**.

    > [!NOTE]
    > At this time, you may only track by key performance indicator (KPI), not percentage completed. If you would like to use the Google Sheets integration, go ahead and add the integration.

2. In the popup box, you'll indicate the cell you would like to link the metric with. Select **View** to preview your sheet. In the following example, we'll locate and use Sales Sheet - Column E, Row 4 to indicate Susie's February Sales.

3. Select **Next** to finish and save your OKR. You should now see an icon next to the OKR. The OKR will sync automatically every hour, but to refresh it manually select **refresh**.
