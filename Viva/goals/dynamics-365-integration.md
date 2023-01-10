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

Dynamics 365 is an enterprise resource planning (ERP) and customer relationship management (CRM) solution provider that includes many intelligent business applications such as Sales, Customer Service, Marketing, Project Service, Field Service, Social Engagement, HR, and more.

The Viva Goals integration with Dynamics 365 enables you to automatically update your Key results and Projects with metrics from any of the Dynamics 365 apps, allowing leaders and managers to obtain an holistic view of business operations within Viva Goals. 
  
## How to set up Dynamics 365 integration 

### Tenant admin configuration 

The tenant administrator can enable Dynamics 365 integration for all Viva Goals organizations with their tenant by following the steps below:  

1. Login to Viva Goals as Tenant admin and go to [https://goals.microsoft.com/organizations](https://goals.microsoft.com/organizations).
1. Click **settings.**
1. Under the Integrations section, enable the Dynamics 365 integration by toggling the status. 

Once the tenant admin enables the integration, the Dynamics 365 integration will be available to all the Viva Goals organizations within the tenant.

### Organization admin configuration

An organization admin can follow these steps to enable the Dynamics 365 integration within a specific Viva Goals organization.

1. Login to Viva Goals as an organization admin.
1. Select **Admin** from the navigation side bar, followed by **integrations**.
1. Navigate to Dynamics 365 and select **enable**, or **manage** if the integration is already enabled.
1. Click **New Connection** and follow the prompts to sign-in with your Microsoft credentials.
1. Select **next** to complete setup.

Viva Goals allows you to connect with multiple Dynamics 365 accounts. Select **New connection** to continue adding accounts. Each account should have a unique name. Users will be allowed to swap connections when they link their KRs to Dynamics 365.

## How to connect Dynamics 365 metrics to a Key Result (KR)

After setup is complete, users within your organization can link their KRs to any Dynamics 365 metric by connecting to a view or report in Dynamics 365.

1. When you create (or edit) a KR, go to the Progress section and select **Automatically from a data source**. 
1. From the list of integrations, select Dynamics 365. If you have multiple Dynamics 365 connections, select the connection that your view is associated with before you select the App.
1. In the **App** field, select the Dynamics 365 app of your choice to connect its metrics with a KR.
1. Select the **entity** within the app that measures the metric’s progress.
1. Search for the **View** you want to connect to.
1. Select the **Column** from the view you want to designate as the measure of success. The available fields will vary based on the configuration of the view you select.
1. Select the **Aggregation** based on the type of KR View and how you would like to compute the progress.
1. Select **Next** and then **Save** to complete the update of your OKR.

You should now see a Dynamics 365 icon near to the KR progress bar. The KR will automatically sync every hour. To refresh it manually, click the Dynamics 365 icon and pick **Sync now**.
