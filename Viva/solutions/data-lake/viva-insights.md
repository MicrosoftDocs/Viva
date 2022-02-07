---

title: Microsoft Viva Insights Data Lake Solution overview
description: Learn how to set up and use the Viva Insights Data Lake Solution
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Viva Insights Data Lake Solution

This walkthrough is an end-to-end data lake solution to extract, transform, and load Viva Insights data into a database and then report it through Power BI as an end-user platform. The key features of this workload:

- Automated pipeline to avoid manual interaction with the Viva Insights query builder platform.
- Instructions and guidelines on managing and loading Viva Insights historical data.
- Utilizing an open source scripting language (Spark) to enable reusability of the script in other platforms and tools.
- Leveraging Azure Synapse for a seamless, easy-to-manage workspace to implement the solution.

## Example use cases

Several scenarios can benefit from this workload through layering an advanced ETL pipeline on top of Viva Insights:

- You can use two native out-of-the-box approaches with Viva Insights’ queries:

  - Download the query results file manually.
  - Use the OData links with a secondary tool like Microsoft Power BI to connect through the OData links. To avoid manual downloads and using unnecessary tools, a program (script) is required to load and ingest the data.

In fact, many advanced workplace analytics use cases might require the Viva Insights data to be used in production by automatically ingesting into an existing data warehouse, combined with other data sources to have a comprehensive view of the organization.

- Business intelligence (BI) solutions with Power BI or other tools might not scale properly through the OData link provided for Viva Insights queries. This walkthrough with the combination of SQL Database and Power BI (or any other tool connecting though OData) will help with this limitation.
- The Viva Insights queries have limitations in the time period. Having an additional work stream to ingest and store the historical data over time might be necessary for some organizations and some scenarios.

## Architecture

 Components

- Azure Synapse Analytics is an analytics service that combines data integration, enterprise data warehousing, and big data analytics. In this solution:

  - An Azure Synapse Workspace promotes collaboration between data engineers, data scientists, data analysts, and BI professionals.
  - Azure Synapse pipelines orchestrate and ingest data into SQL Database and Data Lake Storage.
  - Azure Synapse SQL pools run queries and analytics at massive scale once data is stored in relational tables with columnar storage.
  - Azure Synapse serverless Apache Spark pools do code-first explorations in Data Lake Storage with Spark languages like Spark SQL, pySpark, and Scala.

## Alternatives

- You can use Azure Data Factory for data integration instead of Azure Synapse pipelines. The choice depends on several factors:

  - Azure Synapse pipelines keep the solution design simpler, and allow collaboration inside a single Azure Synapse workspace.
  - Azure Synapse pipelines don't support SSIS packages rehosting, which is available in Azure Data Factory.
  - Synapse Monitor Hub monitors Azure Synapse pipelines, while Azure Monitor can monitor Data Factory.
 
For more information and a feature comparison between Azure Synapse pipelines and Data Factory, see Data integration in Azure Synapse Analytics versus Azure Data Factory.

- You can use SQL Database instead of the Synapse Analytics dedicated SQL pools for storing enterprise data. 
- You can use Databricks instead of Synapse Spark Pool to transform the data. The link for Databricks notebooks is also available in the GitHub repository.

## Availability and pricing

SQL Database (standalone or as Synapse dedicated SQL Pool) is a PaaS service that can meet your high availability (HA) and disaster recovery (DR) requirements. Be sure to pick the SKU that meets your requirements. For guidance, see High availability for Azure SQL Database.

You can use the Azure Pricing Calculator to get an estimate for this workflow. Azure Synapse allows you to scale your compute and storage levels independently. Compute resources are charged per hour, and you can scale or pause these resources on demand. Storage resources are billed per terabyte, so your costs will increase as you ingest more data.

- SQL database bases costs on the selected Compute and Service tiers, and the number of vCores and Database Transaction Units (DTUs).
- Data Lake Storage pricing depends on the amount of data you store and how often you use the data.
- Azure Synapse pipelines base costs on the number of data pipeline activities, integration runtime hours, data flow cluster size, and execution and operation charges. Pipeline costs increase with additional data sources and amounts of data processed.
- Azure Synapse Spark pool bases pricing on node size, number of instances, and uptime.

## Prerequisites

- Viva Insights or Workplace Analytics analyst – Must be assigned a license and an Analyst role for Viva Insights or Workplace Analytics and be able to setup and run queries.
- Microsoft Azure subscription – If you don't have an Azure subscription, create a free account now. You’ll be using Azure Active Directory, OData connector, and Data Factory for this setup.
- Azure data store – Your data store must be supported by the OData connector.
- Azure admin – You need Azure admin privileges to create and register the app in Azure. You also need to ask the Azure global admin to grant you permissions in Azure Data Factory to connect your new app to the Azure data store.

