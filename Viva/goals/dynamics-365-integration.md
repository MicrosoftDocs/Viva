---
ms.date: 03/28/2024
title: Dynamics 365 integration
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
description: "Learn how to integrate Dynamics 365 with Viva Goals."
---

# Dynamics 365 integration

Dynamics 365 is an enterprise resource planning (ERP) and customer relationship management (CRM) solution provider that includes many intelligent business applications, such as Sales, Customer Service, Marketing, Project Service, Field Service, Social Engagement, HR, and more.

Integrating Viva Goals with Dynamics 365 allows you to automatically update key results and initiatives with metrics from any Dynamics 365 app, enabling leaders and managers to obtain a holistic view of business operations from within Viva Goals.
  
## Set up Dynamics 365 integration

### Tenant admin configuration

A tenant administrator can enable Dynamics 365 integration for all Viva Goals organizations in their tenant by following the steps below:

1. Log in to Viva Goals as a tenant admin.

1. In the top right corner, select the **Viva Goals Admin Center** icon to go to the Admin portal.

1. In the left-hand navigation, select **Integrations**.

1. Find the Dynamics 365 integration and toggle its status to **On**, then select **Save**.
 :::image type="content" source="../media/goals/dynmaics-365-integration/tenant-admin-settings.png" alt-text="Screenshot of tenant admin settings page." lightbox="../media/goals/dynmaics-365-integration/tenant-admin-settings.png":::

Once the tenant admin enables the integration, the Dynamics 365 integration will be available to all the Viva Goals organizations within the tenant.

### Organization admin configuration

An organization admin can use these steps to enable the Dynamics 365 integration within their specific Viva Goals organization:

1. Log in to Viva Goals as an organization admin.

1. Starting from the navigation sidebar, go to **Admin** > **Integrations**.
 :::image type="content" source="../media/goals/dynmaics-365-integration/admin-integrations.png" alt-text="Screenshot of the integration page in the admin area of Viva Goals." lightbox="../media/goals/dynmaics-365-integration/admin-integrations.png":::

1. Navigate to Dynamics 365 and select **Enable** (or **Manage** if the integration has already been enabled).
 :::image type="content" source="../media/goals/dynmaics-365-integration/admin-list-page.png" alt-text="Screenshot of Dynamics 365 integration." lightbox="../media/goals/dynmaics-365-integration/admin-list-page.png":::

1. Select **New Connection** and follow the prompts to sign in with your Microsoft credentials.
 :::image type="content" source="../media/goals/dynmaics-365-integration/admin-detail-page.png" alt-text="Screenshot showing the admin detail page when setting up the Dynamics 365 integration." lightbox="../media/goals/dynmaics-365-integration/admin-detail-page.png":::
 :::image type="content" source="../media/goals/dynmaics-365-integration/admin-connection-form.png" alt-text="Screenshot of how to log in." lightbox="../media/goals/dynmaics-365-integration/admin-connection-form.png":::

1. Select **Next** to complete the setup.

Viva Goals allows you to connect with multiple Dynamics 365 accounts. Select **New Connection** to continue adding accounts. Each account should have a unique name. Users will be allowed to swap connections when they link their key results to Dynamics 365.

## Connect Dynamics 365 metrics to a key result

After setup is complete, users within your organization can link their key results (KRs) to any Dynamics 365 metric by connecting to a view or report in Dynamics 365.

1. Add a new key result or edit an existing key result by selecting that key result's **More options** (**...**) > **Edit**.

1. Under **Progress and Status**, there's a section with the text "Connect to a data source for automatic progress updates" followed by a list of integration icons. Select the **Dynamics 365** icon. If you have multiple Dynamics 365 connections, select the connection that your view is associated with before proceeding to the next step.

    :::image type="content" source="../media/goals/dynmaics-365-integration/automate-data-source.png" alt-text="Screenshot of selecting the Dynamics 365 option for a key result." lightbox="../media/goals/dynmaics-365-integration/automate-data-source.png":::

1. In the **App** field, select the Dynamics 365 app of your choice to connect its metrics to the KR.
 :::image type="content" source="../media/goals/dynmaics-365-integration/app.png" alt-text="Screenshot of configuring the app." lightbox="../media/goals/dynmaics-365-integration/app.png":::

1. In the **Site map entity** field, select the entity within the app that measures the metric’s progress.
 :::image type="content" source="../media/goals/dynmaics-365-integration/site-map.png" alt-text="Screenshot of configuring the site map." lightbox="../media/goals/dynmaics-365-integration/site-map.png":::

1. In the **View** field, select the view you want to connect to.
 :::image type="content" source="../media/goals/dynmaics-365-integration/view.png" alt-text="Screentshot of configuring the view." lightbox="../media/goals/dynmaics-365-integration/view.png":::

1. In the **Column** field, select the column (of the view) that you want to designate as the metric for success. The available fields will vary based on the configuration of the view you select.
 :::image type="content" source="../media/goals/dynmaics-365-integration/column.png" alt-text="Screenshot of configuring the column." lightbox="../media/goals/dynmaics-365-integration/column.png":::

1. In the **Aggregation** field, choose an aggregation based on the type of KR view and how you want to calculate progress.
 :::image type="content" source="../media/goals/dynmaics-365-integration/aggregation.png" alt-text="Screenshot of configuring the aggregation." lightbox="../media/goals/dynmaics-365-integration/aggregation.png":::

1. Select **Next** and then **Save** to finish updating your key result.
 :::image type="content" source="../media/goals/dynmaics-365-integration/post-connection.png" alt-text="Screenshot of an integrated key result." lightbox="../media/goals/dynmaics-365-integration/post-connection.png":::

You should now see a Dynamics 365 icon next to the key result's progress bar. The key result will automatically sync every hour. To refresh it manually, select the Dynamics 365 icon and choose **Sync**.

:::image type="content" source="../media/goals/dynmaics-365-integration/integration-details.png" alt-text="Screenshot of the integration details for a key result." lightbox="../media/goals/dynmaics-365-integration/integration-details.png":::
