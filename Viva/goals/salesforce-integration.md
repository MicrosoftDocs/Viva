---
ms.date: 04/17/2022
title: "Salesforce Integration"
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

description: "Learn how to integrate your Viva Goals OKRs with Salesforce reports."
---

# Salesforce integration

Viva Goals integrates with Salesforce lets you automatically update your objectives and key results (OKRs). For example, say you have a Salesforce report that tracks converted leads. You have a goal to increase the value of converted leads to a certain amount. Salesforce integration will automatically update your progress in Viva Goals.

## How to set up Salesforce integration 

An admin can follow these steps to set up Salesforce integration in Viva Goals. 

1. Go to the Viva Goals integrations page: **Admin** -> **Integrations**.
  
    :::image type="content" source="../media/goals/9/viva-goals-integrations-page.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/9/viva-goals-integrations-page.png":::

2. Scroll through the list until you reach **Salesforce**. Select **Enable** or select **Manage** if a connection was made previously.
  
    :::image type="content" source="../media/goals/9/salesforce-enable-button.png" alt-text="Screenshot shows where you enable Salesforce in Viva Goals." lightbox="../media/goals/9/salesforce-enable-button.png":::

3. Select **"New Connection"** and follow the prompts to sign in to your Salesforce account.
  
    :::image type="content" source="../media/goals/9/salesforce-new-connection-button.png" alt-text="Screenshot shows where you select New Connection for Salesforce in Viva Goals." lightbox="../media/goals/9/salesforce-new-connection-button.png":::

4. Select **"Next"** to finish setup.

Viva Goals allows you to connect with multiple Salesforce accounts. Select **New connection** to add another account. You differentiate connections by name. The names are displayed to users when they link their OKRs to Salesforce reports.

## How to use Salesforce integration

After setup is complete, users in your organization can link the success of their OKRs  to fields in Salesforce reports.

1. When you create (or edit) an objective or key result, go to the **Progress** section and select **Connect to a Data Source**.

2. From the list of integrations, select **Salesforce**.
  
    :::image type="content" source="../media/goals/9/select-salesforce-datasource.png" alt-text="Screenshot shows where you select Salesforce as the data source in Viva Goals." lightbox="../media/goals/9/select-salesforce-datasource.png":::

3. Search for the report you want to connect to. If you have multiple Salesforce connections, select the connection that your report is associated with before you search for the report.
  
    :::image type="content" source="../media/goals/9/salesforce-report-selection.png" alt-text="Screnshot shows where you select a Salesforce report in Viva Goals." lightbox="../media/goals/9/salesforce-report-selection.png":::  

4. Select the field you want to designate as the measure of success. The available fields will vary based on the configuration of the report you select.
  
    :::image type="content" source="../media/goals/9/salesforce-field-selection.png" alt-text="Screenshot shows where you select a Salesforce field as your measure of success." lightbox="../media/goals/9/salesforce-field-selection.png":::

5. Select **Next** and then **Save** to complete the update of your OKR.

You should now see a Salesforce icon next to the OKR. The OKR will sync automatically every hour. To refresh it manually, go to the cloud icon and select **Sync**.

