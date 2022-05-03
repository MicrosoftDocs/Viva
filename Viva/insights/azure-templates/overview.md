---

ROBOTS: NOINDEX,NOFOLLOW
title: Workplace Analytics Azure Templates overview
description: About Workplace Analytics Azure Templates and how to use it for advanced data analysis
author: madehmer
ms.author: v-lilyolason
ms.topic: conceptual
ms.localizationpriority: medium 
ms.collection: m365initiative-viva-insights 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---
# Workplace Analytics Azure Templates overview

_These templates are only available as part of a Microsoft service engagement._

>[!Important]
>As of February 2022, this product is no longer supported. If you're not using the templates, see [Cancel the service](cancel-service.md) for how-to steps in the Azure portal.

Workplace Analytics Azure Templates extend and accelerate advanced analysis of your organizational data. These templates are built on and are compliant with secure Azure Services. These templates include automated configuration and connectivity to Power BI and Azure Services.

You can easily customize them to meet your unique organizational needs, including the following functionality.

* **Reference templates** - Enable you to customize your data by using attribute filters and various graphical views and interactive options. You can share data updates across your team and push actionable insights and recommendations to other Microsoft 365 products, such as PowerPoint. The following are included by default:

  * [Join Datasets Azure Template](./join-datasets.md)
  * [Organization Network Analysis Azure Template](./organization-network-analysis.md)
  * [Process Explorer Azure Template](./process-explorer.md)
  * [Relationship Intelligence Azure Template and Power BI report](./relation-intel.md)
  * [Workspace Planning Azure Template](space-planning.md)

* **Analytic framework support** - Enables you to merge Workplace Analytics query output with other [Azure data sources](/azure/index) outside of Workplace Analytics (such as with Azure Blob storage, Azure SQL Database, Azure Databricks, and Azure Analysis Services) for custom metric calculations, advanced and interactive visuals, and automated data management.

* **Predictive models** - Enable you to deploy or plug in your own machine-learning models, such as top performer analysis, anomaly detection, sales forecasting, and churn modeling. You can also use larger data sets to improve the performance of machine-learning models and interact with a parameter-based interface (no scripting necessary).

The following shows how Workplace Analytics Azure Templates fit into your existing organizational system.

![Workplace Analytics Azure Templates architecture.](./images/azure-templates-architecture.png)

As shown in the graphic, Workplace Analytics Azure Templates work with the following Azure components within your existing Azure environment.

|Component Name |Description |
|--------------|---------------------|
|[Resource Group](/azure/azure-resource-manager/resource-group-overview#resource-groups) |This is where all resources will be deployed |
|[Azure Blob Storage](/azure/storage/blobs/storage-blobs-introduction) |Used to store the Workplace Analytics data and any computations |
|[Azure SQL Database](/azure/sql-database/) |Used to store configuration settings and data metrics |
|[Azure KeyVault](/azure/key-vault/key-vault-whatis) |Used for Secret Management throughout the entire service |
|[Azure Databricks](/azure/azure-databricks/) |Used for joins, machine learning and other computations |
|[Azure Analysis Services](/azure/analysis-services/) |In-memory models used to compute metrics |
|[Azure Web App](/azure/app-service/) |Used for configuration and user experiences related to analytics |

## Related topics

* [What's new in Workplace Analytics Azure Templates](./release-notes.md)
* To learn more about Microsoft services, email us at `wpaazuretemplates@microsoft.com`
* [Deploy and Configure Workplace Analytics Azure Templates](./deploy-configure.md)