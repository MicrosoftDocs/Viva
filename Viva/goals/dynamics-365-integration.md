---
title: "Dynamics 365 Integration"
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager: Liz/Pierce
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

description: "Learn how to integrate Dynamics 365 with Viva Goals."
---

# Dynamics 365 integration

Dynamics 365 is an Enterprise Resource Planning (ERP) and Customer Relationship Management (CRM) solution provider that includes many intelligent business applications such as Sales, Customer Service, Marketing, Project Service, Field Service, Social Engagement, HR, and more.

The Viva Goals integration with Dynamics 365 enables you to automatically update your Key results and Projects with metrics from any of the Dynamics 365 apps, allowing leaders and managers to obtain a holistic view of business operations within Viva Goals. 
  
## How to set up Dynamics 365 integration 

### Tenant admin configuration 

The tenant administrator can enable Dynamics 365 integration for all Viva Goals organizations with their tenant by following the steps below:  

1. Log in to Viva Goals as Tenant admin and go to [https://goals.microsoft.com/organizations](https://goals.microsoft.com/organizations).
1. Click **settings.**
1. Under the Integrations section, enable the Dynamics 365 integration by toggling the status. 
 :::image type="content" source="../media/goals/dynmaics-365-integration/tenant-admin-settings.png" alt-text="Screenshot of tenant admin settings page." lightbox="../media/goals/dynmaics-365-integration/tenant-admin-settings.png":::

Once the tenant admin enables the integration, the Dynamics 365 integration will be available to all the Viva Goals organizations within the tenant.

### Organization admin configuration

An organization admin can follow these steps to enable the Dynamics 365 integration within a specific Viva Goals organization.

1. Log in to Viva Goals as an organization admin.

2. Select **Admin** from the navigation side bar, followed by **integrations**.
 :::image type="content" source="../media/goals/dynmaics-365-integration/admin-integrations.png" alt-text="Screenshot of the integration page in the admin area of Viva Goals." lightbox="../media/goals/dynmaics-365-integration/admin-integrations.png":::

3. Navigate to Dynamics 365 and select **enable**, or **manage** if the integration is already enabled.
 :::image type="content" source="../media/goals/dynmaics-365-integration/admin-list-page.png" alt-text="Screenshot of Dynamics 365 integration." lightbox="../media/goals/dynmaics-365-integration/admin-list-page.png":::

4. Click **New Connection** and follow the prompts to sign-in with your Microsoft credentials.
 :::image type="content" source="../media/goals/dynmaics-365-integration/admin-detail-page.png" alt-text="Screenshot showing the admin detail page when setting up the Dynamics 365 integration." lightbox="../media/goals/dynmaics-365-integration/admin-detail-page.png":::
 :::image type="content" source="../media/goals/dynmaics-365-integration/admin-connection-form.png" alt-text="Screenshot of how to log in." lightbox="../media/goals/dynmaics-365-integration/admin-connection-form.png":::

5. Select **next** to complete setup.

Viva Goals allows you to connect with multiple Dynamics 365 accounts. Select **New connection** to continue adding accounts. Each account should have a unique name. Users will be allowed to swap connections when they link their KRs to Dynamics 365.

## How to connect Dynamics 365 metrics to a Key Result (KR)

After setup is complete, users within your organization can link their KRs to any Dynamics 365 metric by connecting to a view or report in Dynamics 365.

1. When you create (or edit) a KR, go to the Progress section and select **Automatically from a data source**.
 
2. From the list of integrations, select Dynamics 365. If you have multiple Dynamics 365 connections, select the connection that your view is associated with before you select the App.
 :::image type="content" source="../media/goals/dynmaics-365-integration/automate-data-source.png" alt-text="Screenshot of selecting the Dynamics 365 option for a key result." lightbox="../media/goals/dynmaics-365-integration/automate-data-source.png":::

3. In the **App** field, select the Dynamics 365 app of your choice to connect its metrics with a KR.
 :::image type="content" source="../media/goals/dynmaics-365-integration/app.png" alt-text="Screenshot of configuring the app." lightbox="../media/goals/dynmaics-365-integration/app.png":::

4. Select the **entity** within the app that measures the metric’s progress.
 :::image type="content" source="../media/goals/dynmaics-365-integration/site-map.png" alt-text="Screenshot of configuring the site map." lightbox="../media/goals/dynmaics-365-integration/site-map.png":::

5. Search for the **View** you want to connect to.
 :::image type="content" source="../media/goals/dynmaics-365-integration/view.png" alt-text="Screentshot of configuring the view." lightbox="../media/goals/dynmaics-365-integration/view.png":::

6. Select the **Column** from the view you want to designate as the measure of success. The available fields will vary based on the configuration of the view you select.
 :::image type="content" source="../media/goals/dynmaics-365-integration/column.png" alt-text="Screenshot of configuring the column." lightbox="../media/goals/dynmaics-365-integration/column.png":::

7. Select the **Aggregation** based on the type of KR View and how you would like to compute the progress.
 :::image type="content" source="../media/goals/dynmaics-365-integration/aggregation.png" alt-text="Screenshot of configuring the aggregation." lightbox="../media/goals/dynmaics-365-integration/aggregation.png":::

8. Select **Next** and then **Save** to complete the update of your OKR.
 :::image type="content" source="../media/goals/dynmaics-365-integration/post-connection.png" alt-text="Screenshot of an integrated key result." lightbox="../media/goals/dynmaics-365-integration/post-connection.png":::

You should now see a Dynamics 365 icon near to the KR progress bar. The KR will automatically sync every hour. To refresh it manually, click the Dynamics 365 icon and pick **Sync now**.

:::image type="content" source="../media/goals/dynmaics-365-integration/integration-details.png" alt-text="Screenshot of the integration details for a key result." lightbox="../media/goals/dynmaics-365-integration/integration-details.png":::