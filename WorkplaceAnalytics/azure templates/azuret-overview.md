---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Workplace Analytics Azure Templates overview
description: About Workplace Analytics Azure Templates and how to use it for advanced data analysis
author: madehmer
ms.author: madehmer
ms.date: 11/26/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---
# Workplace Analytics Azure Templates overview

Workplace Analytics Azure Templates extend and accelerate advanced analysis of your organizational data. These templates are built on and compliant with secure Azure Services. These templates include automated configuration and connectivity to Power BI and Azure Services.
You can easily customize this extension to meet your unique organizational needs, including the following functionality.

* **Reference templates** enable you to customize visuals or filter by data attributes, share updates across your team, and push actionable insights and recommendations to PowerPoint. The following templates are included by default:

  * Organizational Network Analysis
  * Topic Analysis
  * Sales Effectiveness

* **Analytic framework support** enables you to merge Workplace Analytics query output with other [Azure data sources](https://docs.microsoft.com/azure/index) outside Workplace Analytics (such as Azure Blob storage, Azure SQL database, Azure Databricks, and Azure Analysis Services) for custom metric calculations, advanced and interactive visuals, and automated data management.
* **Predictive models** enable you to deploy or plug in your own machine-learning models, such as top performer analysis, anomaly detection, sales forecasting, and churn modeling. You can also use larger data sets to improve the performance of machine-learning models and interact with a parameter-based interface (no scripting necessary).

The following shows how the Workplace Analytics Azure Templates fit into your existing organizational system.

![Workplace Analytics Azure Templates architecture](./images/azuret-architecture.png)

The following are the Azure components that Workplace Analytics Azure Templates work with in your existing organizational system.

|Component Name |Description |
|--------------|---------------------|
|[Resource Group](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-overview#resource-groups) |This is where all resources will be deployed under |
|[Azure Blob Storage](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction) |Used to store the WpA Data and any computations |
|[Azure SQL Database](https://docs.microsoft.com/azure/sql-database/) |Used to store Configuration settings and some metrics |
|[Azure KeyVault](https://docs.microsoft.com/azure/key-vault/key-vault-whatis) |Used for Secret Management throughout the entire service |
|[Azure Databricks](https://docs.microsoft.com/azure/azure-databricks/) |Used for joins, Machine Learning and other computations |
|[Azure Analysis Services](https://docs.microsoft.com/azure/analysis-services/) |In-memory model used to compute metrics |
|[Azure Web application](https://docs.microsoft.com/azure/app-service/) |Used for configuration and user experiences related to analytics |

## Related topic

[Deploy and configure the Workplace Analytics Azure Templates](./azuret-deploy-configure.md)
