---

title: Microsoft Graph Data Coonnect data lake solution
description: Learn how to set up and use the Microsoft Graph Data Connect data lake solution
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: helayne
audience: Admin
---

# Microsoft Graph Data Connect Data Lake Solution

Using Microsoft Graph Data Connect, you can load and copy data from your Office 365 organization (Microsoft Graph) into your Azure storage account, then extract attributes, ultimately enriched attributes, and knowledge. Microsoft Graph Data Connect usually provides Office 365 data to your Azure storage in JSON lines. However, this walkthrough flattens the data into entity tables, which are represented as CSVs. In addition to flat CSVs, the solution exports data with the Common Data Model (CDM) structure. Follow Microsoft documentation [here](https://docs.microsoft.com/en-us/common-data-model/) to learn more about the CDM.

In this walkthrough you’ll:

1. Provision required resources in your Azure environment to store and process your Office 365 data.

2. Use an Azure Data Factory or Synapse to move your Office 365 data through Microsoft Graph Data Connect into Azure Data Lake Storage Gen2 (ADLSg2) in your environment in JSON lines.

3. Use Azure Synapse Spark pool or Databricks to run a PySpark script, which converts your Office 365 data from JSON lines into flat CSV or CDM entities.

## Prerequisites

Before following the steps in this walkthrough, make sure you have:

* Microsoft Graph Data Connect enabled in your Office 365 organization

* An Azure subscription under the same Azure Active Directory tenant as your Office 365 subscription

Need to enable and configure Microsoft Graph Data Connect in your environment alongside an Azure subscription? Follow the steps in [Set up your Microsoft 365 tenant and enable Microsoft Graph Data Connect](/graph/data-connect-quickstart?tabs=Microsoft365) of our Microsoft Graph Data Connect training module.

## Provision and configure required resources

To complete the conversion, you’ll need to create or provision a few resources in your Azure environment:

* **App registration**: The app registration enables Microsoft Graph Data Connect to extract your Office 365 data into your Azure storage. Follow the steps in [Set up your Azure Active Directory app registration](graph/data-connect-quickstart?tabs=Microsoft365&tutorial-step=2) of our training module to provision the resource.

  * Note down the **application ID**, **tenant ID**, and **application key**; they’ll be used [later](#create-linked-services-within-the-orchestration-tool) in the walkthrough.

  * Ensure the app registration has Storage Blob Data Contributor access to the ADLSg2 account (detailed on the next bullet).

* **ADLSg2 account**: This account stores the JSON lines outputted from Microsoft Graph Data Connect. This storage account can be any new or existing account, or if you're using Synapse pipelines, the default storage linked to Synapse.

    Follow the steps in [Set up your Azure Storage resource](/graph/data-connect-quickstart?tabs=Microsoft365&tutorial-step=3) to set up proper permissions for your storage account.

  * File systems:

    * A file system to store the Office 365 data outputted by Microsoft Graph Data Connect in JSON format (called *json* in this walkthrough and is the default value in the script and pipeline parameters)

    * A file system to store the outputted CDM entities after the conversion is complete (called *cdm* in this walkthrough and is the default value in the script and pipeline parameters)

    * A file system to store the outputted CSV entities after the conversion is complete (called *csv* in this walkthrough and is the default value in the script and pipeline parameters)

* A preferred:

  * **Orchestration tool**: Synapse/Azure Data Factory

  * **Processing engine**: Databricks or Synapse Spark pool

* **The PySpark script**: This script converts the Microsoft Graph Data Connect JSON lines into CDM and CSV format and stores the resulting files.

  * If using **Databricks** as your compute engine: upload the Databricks notebook—located in the [**src**](https://github.com/microsoft/VivaSolutions/tree/main/Sample%20Solutions/Data%20Lake/MGDC/src) directory of this repository—into the Databricks instance.

  * If using **Synapse Spark pool** as your compute engine: Import the Synapse notebook from the [**src**](https://github.com/microsoft/VivaSolutions/tree/main/Sample%20Solutions/Data%20Lake/MGDC/src) directory of this repository into your Synapse workspace (**Develop > Notebooks > import**).

* **CDM library**:

  * **Synapse** has the CDM library installed by default.

  * If you’re using **Databricks**, install the CDM library via Maven:

    1. Under **Install library**, select **Maven** as the source, then select **Search Packages**.

        :::image type="content" source="../images/databricks-library1.png" alt-text="Screenshot of the 'Install library' window with Maven selected and 'Search packages' highlighted.":::

    2. Search for and select `spark-cdm-connector`.

        :::image type="content" source="../images/databricks-library2.png" alt-text="Screenshot of 'Search packages' window with 'spark-cdm-connector' entered in search bar and listed as entry under 'Artifact id'.":::

## Load and convert Office 365 data

Follow these steps to create a pipeline to export your Office 365 data into a storage account, and then transform this data into CDM and CSV formats.

### Create linked services within the orchestration tool

You'll need to create a few linked service entities within the orchestration tool (Azure Data Factory or Synapse) using the Azure resources provisioned [earlier](#provision-required-resources).

In **ADF/Synapse > Manage > Linked Services**:

1. Create an ADLSg2 linked service to allow access the ADLSg2 account:

    1. Select **Azure Data Lake Storage Gen2** and create a new linked service.

    1. In the resulting blade, make sure you‘ve set the **Authentication method** to **Service Principal** and **Account selection method** to **From Azure subscription**.

    1. Select the Azure subscription and account created earlier, then input the **application ID** and **application key** noted in [Provision required resources](#provision-required-resources) that has access to the account..

    1. Select **Create**.

        :::image type="content" source="../images/storage-linked-service.png" alt-text="Screenshot of 'New linked service' blade.":::

2. Create an Office 365 data linked service to allow Microsoft Graph Data Connect to move data into your Azure storage account:

    1. Select **Office 365** and create a new linked service.

    1. In the resulting blade, provide the **application ID** and **application key** noted in [Provision required resources](#provision-required-resources).
    1. Select **Create**. This linked service will automatically be used for all of the Office 365 tables.

        :::image type="content" source="../images/office365-linked-service.png" alt-text="alt text":::

3. Depending on your compute engine, create either a Databricks linked service or a new Synapse Spark pool.

     1. ***If using Databricks***, create a Databricks linked service connected to your existing Databricks instance:

        1. Select **Databricks** under **Compute** and create a new linked service.

        1. In the resulting blade, make sure the appropriate Databricks workspace and cluster is selected. Generate the Access Token from the Azure Databricks workplace. (You can find the steps to do that [here](https://docs.databricks.com/dev-tools/api/latest/authentication.html#generate-token).)

     2. ***If using Synapse with Synapse Spark pool***, create a new pool in **Synapse > Manage > Analytics Pools > Apache Spark Pool**.

### Create a new pipeline

1. Within the orchestration tool (either Azure Data Factory or Synapse), create a new pipeline.

2. Create the following parameters for the pipeline:

    * `OfficeDataFileSystem` - The file system in the ADLSg2 account to place the Office 365 data in JSON lines (for this walkthrough, we use `json`)

    * `DateStartTime` - The start time for the Office 365 data you want to process. The format is *2019-10-22T00:00:00Z*.

    * `DateEndTime` - The end time for the Office 365 data you want to process. The format is *2019-10-28T00:00:00Z*.

    * `StorageAccountName` - The name of the ADLSg2 account

    * `AppID` - The application ID for the app registration provisioned earlier

    * `AppKey` - The application key for the app registration provisioned earlier

    * `TenantId` - The tenant ID for the app registration provisioned earlier

    * `CdmDataFileSystem` - The file system in the ADLSg2 account that will contain the CDM entities (`cdm` for this walkthrough)

    * `CdmModelName` - Sub-directory in the `CdmDataFileSystem` for the CDM entities (`O365-data` for this walkthrough)

    * `MessageDatasetFolder` - Sub-directory in the `OfficeDataFileSystem` for the messages in JSON (`message` for this walkthrough)

    * `EventDatasetFolder` - Sub-directory in the `OfficeDataFileSystem` for events in JSON (`event` for this walkthrough)

    * `UserDatasetFolder` - Sub-directory in the `OfficeDataFileSystem` for user data in JSON (`user` for this walkthrough)

    * `ManagerDatasetFolder` - Sub-directory in the `OfficeDataFileSystem` for manager user data in JSON (`manager`for this walkthrough)

    * `CsvDataFileSystem` - The file system in the ADLSg2 account that will contain the CSV entities (`csv` for this walkthrough)

        :::image type="content" source="../images/pipeline-parameters2.png" alt-text="Screenshot of pipeline Parameters window":::

### Create Copy Data activities and a new Sink dataset

Follow the steps here to create four *Copy Data* activities to load the following four Office 365 tables. For each table, include the respective **Source** parameters from the list below.

>[Note!] The versions provided for each table are current as of time of writing.

1. **Event Table** (BasicDataSet_v0.Event_v1)

    * **Date filter**: input pipeline `DateStartTime` and `DateEndTime` parameters via **Add Dynamic Content**.

       :::image type="content" source="../images/event-tbl-source2.png" alt-text="screenshot of the Event Table Source parameter window with Source tab and Start time (UTC) and End time (UTC) fields highlighted.":::

2. **Message Table** (BasicDataSet_v0.Message_v1)
    * **Date filter**: input pipeline `DateStartTime` and `DateEndTime` parameters via **Add Dynamic Content**.

        :::image type="content" source="../images/message-tbl-source2.png" alt-text="screenshot of the Message Table Source parameter window with Source tab and Start time (UTC) and End time (UTC) fields highlighted.":::

3. **Manager Table** (BasicDataSet_v0.Manager_v0)
    * No **Date filter** is required.

4. **User Table**  (BasicDataSet_v0.User_v1)
    * No **Date filter** is required.

Create a new Sink dataset to be used for all four data tables.

1. Select the storage account provisioned in this walkthrough, then add `OfficeDataFileSystem`, `DatasetPath`, and `PipelineID` as the Sink dataset parameters, and add `@concat(dataset().OfficeDataFileSystem,'/',dataset().PipelineID,'/',dataset().DatasetPath) ` as the **File path** in the **Directory field**.

    :::image type="complex" source="../images/event-tbl-sink-file-path.png" alt-text="Screenshot of the Sink dataset Connection window":::
Screenshot of the Sink dataset Connections window. Screenshot shows a window with three sections--Linked service, Integration runtime, and File path. Each section contains a required field, which is filled in as follows. Linked service: dropdown menu; mgdcvivadatalakeLinkedService is selected.Integrationruntime: field is grayed out with a green checkmark and reads AutoResolveIntegrationRuntime. File path has three free-text fields; the first and last have placeholder values of File system and File and the middle contains the filepath described in step 1.
:::image-end:::

2. In the *Copy Data* activities, set the **Sink** parameters as follows:

    1. `OfficeDataFileSystem`: `@pipeline().parameters.OfficeDataFileSystem`

    2. `DatasetPath`, unique to each activity:

        * **Event Table**: `@pipeline().parameters.EventDatasetFolder`

        * **Message Table**: `@pipeline().parameters.MessageDatasetFolder`

        * **Manager Table**: `@pipeline().parameters.ManagerDatasetFolder`

        * **User Table**: `@pipeline().parameters.UserDatasetFolder`

    3. `PipelineID`: `@pipeline().RunId`

          :::image type="content" source="../images/event-tbl-sink3.png" alt-text="alt text":::

### Add a notebook to the pipeline

Based on your orchestration tool and preferred processing platform, add a Synapse notebook or Databricks notebook to the pipeline. In the settings:

1. Link to the notebook downloaded and imported to the tool [earlier](#provision-required-resources) in this walkthrough.

2. Select the Spark pool or the Databricks linked service.

3. Set the **Base parameters** as follows:

    * **`OfficeDataFileSystem`** - `@pipeline().parameters.OfficeDataFileSystem`

    * **`StorageAccountName`** - `@pipeline().parameters.StorageAccountName`

    * **`AppId`** - `@pipeline().parameters.AppId`

    * **`AppKey`** - `@pipeline().parameters.AppKey`

    * **`TenantId`** - `@pipeline().parameters.TenantId`

    * **`CdmDataFileSystem`** - `@@pipeline().parameters.CdmDataFileSystem`

    * **`CdmModelName`** - `@pipeline().parameters.CdmModelName`

    * **`PipelineId`**  - `@pipeline().parameters.PipelineId`

    * **`EventDatasetFolder`**  - `@pipeline().parameters.EventDatasetFolder`

    * **`ManagerDatasetFolder`**  - `@pipeline().parameters.ManagerDatasetFolder`

    * **`MessageDatasetFolder`**  - `@pipeline().parameters.MessageDatasetFolder`

    * **`UserDatasetFolder`** - `@pipeline().parameters.UserDatasetFolder`

    * **`CsvDataFileSystem`** - `@pipeline().parameters.CsvDataFileSystem`

:::image type="complex" source="../images/sink-connection-parameters.png" alt-text="screenshot of the Sink dataset Parameters window":::
   Screenshot that shows the Sink dataset Parameters window. Screenshot shows a table with three columns--Name, Type, and Default value--and three rows. The values in the Name column are OfficeDataFileSystem, DatasetPath, and PipelineID. Each value in the Type column is the word, String. Each value in the Default value column is the word, Value.
:::image-end:::

At this point, the pipeline should resemble the following image:

:::image type="content" source="../images/pipeline.png" alt-text="Screenshot of diagram in pipeline window showing Copy Data activities flowing into the JsonToCDM-CSV notebook":::

## Publish the pipeline and add triggers

1. Publish the pipeline.

2. After the first trigger, follow steps [here](graph/data-connect-quickstart?tabs=Microsoft365&tutorial-step=5) to monitor and approve data consent requests at in the Microsoft 365 Admin Center or via PowerShell.

> [Note!]: Each approved data consent request is valid for six months unless there is a change in the pipeline (for example, a *Copy Data* activity name change or a  pipeline name change)
