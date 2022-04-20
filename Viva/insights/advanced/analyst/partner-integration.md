---

title: Viva Insights partner integration
description: Learn how to integrate Microsoft Viva Insights and partner application data for more advanced analysis
author: madehmer
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

# Viva Insights integration

*This experience is only available through private preview.*

This integration enables you to export and combine Microsoft Viva Insights collaboration data with partner application data within Azure. You can then use this combined analysis for a more advanced, customer analysis, such as to identify behaviors and patterns behind key metrics.

## Viva Insights data

[My organization in Teams](viva-insights-my-org.md) shows what kind of Viva Insights data can be integrated with your partner application data. For details about the metrics used within Viva Insights data, see [Viva Insights metrics](metrics.md).

## Get started

To use this integration, you must join the "Microsoft Graph TAP partner program" to get support for the Azure APIs that are used to access Viva Insights. To join the program, complete [the program form](https://aka.ms/GraphTAPForm) with the following details:

* For **Microsoft Graph workload**, select **Data Connect**.
* In **Justification for TAP entry**, enter what partner data that you want to integrate with Viva Insights data through a Microsoft Graph API.

Before you can access the sample data, you’ll need to set up a test Azure environment to build your solution. Go to [Create your free Azure account today](https://azure.microsoft.com/free/) and select **Start free** to get started.

## Access sample data

You can use the following until the release is available to simulate a test environment for this integration.

* Upload this Viva Insights sample data to your test environment to simulate where to enter the data. See Sample data schema and How to upload data to Azure for details about each.
* Build your application to retrieve the behavioral analytics data, as follows:

  * Pull data from Azure with a public API, such as a REST API and an SDK.
  * Use Azure to push data to your storage blob.

* After the data is retrieved, use the Decryption API to read it.
* Configure a managed application to populate your Azure environment with real analytics data through an Azure Managed Application for Data Egress. 

>[!Note]
>Analytics data is not yet available. In the meantime, you can set up the integration to retrieve Outlook meeting data to try it out and see how it works.

## Move data

Behavioral analytics data is moved between Azure and your application through an Azure Data Factory pipeline.

A sample pipeline is available here: <TODO: Add link to Viva Insights specific example>

This pipeline is installed by a Managed Application that you provide in your customer’s Azure tenant. The pipeline is responsible for:

1. Extracting data from Microsoft 365 to a temporary storage location in the customer’s tenant.
1. Copying data from the temporary location to a Blob Storage account owned by your application, using a Shared Access Signature (SAS) key that you generate, and is entered when the application is installed by the customer.
1. (Optional) Notifying your application that new data is available for processing.
A detailed overview of the installation process for customers and partners is available in this slide deck.

Each data drop includes a “metadata” file <TODO: Add final file name> in JSON format which includes details about the copy activity. The format is as follows:

|Field |Description |
|-------|----------|
|CopyActivityId |A unique identifier for the copy operation. This can be used to obtain a decryption key for the file. |
|JobSubmissionTime |The time that the Data Factory pipeline started. |
|JobCompletionTime |The time that the Data Factory pipeline ended. |
|RequestStartDate |The starting time period for which behavioral analytics data was extracted. |
|RequestEndDate |The ending time period for which behavioral analytics data was extracted. |
|ColumnsRequested |A comma-separated list of the columns included in the output.
|NumberOfRowsExtracted |The number of rows in the output. |
|DataFactoryName |The name of the Data Factory pipeline. |
|TenantId |The Azure Active Directory tenant that the partner analytics data was extracted for. |

Data dropped in your Azure Blob Storage account is encrypted. To decrypt the file, call the Viva Insights decryption API <TODO: Add link> with the CopyActivityId in the metadata file.

Behavioral analytics data is processed by Viva Insights once a week. Your pipeline may run more frequently than this, but the same output will be returned until the following week. The sample pipeline includes a Trigger that will execute the pipeline once every 7 days, which is the recommended pattern.
<TODO: Add documentation on how to customize the pipeline (select specific columns, dates, etc.) once feature is ready.>

## Diagnose pipeline problems

If there is a problem extracting behavioral analytics data from Viva Insights, the **Errors** property in the metadata file will be set. **Errors** will contain detailed information about the failure. No output file will be generated if the **Errors** property is set.

<TODO: Add more information about common failures and resolutions.>

## Best practices for using customer data

1. Do not permanently store decrypted files in Azure or on-premises storage. Your application should decrypt the behavioral analytics data in real-time as it is being processed. The decrypted contents should not be written to the disk.
1. Ensure that your Azure Data Factory pipeline includes a step to clean up analytics data on the customer’s storage account after it has been transferred to your application’s storage. The sample managed application includes this step.

## Join Viva Insights data with other data

The analytics data includes the Azure Active Directory Object ID of each user that generated a row of data. The Object ID can be used to correlate a directory user with a user in your application.

While identifying users by the Object ID is the preferred path, not every application may have access to the customer tenant’s directory information. There are several options in this case:

Export directory information along with the analytics data

1. Configure your Azure Data Factory pipeline to add an additional step to export Azure Active Directory user data.
1. This will create an additional output file from your pipeline that includes basic information about each user in the customer’s tenant. This can be used to correlate user information between Azure and your application by joining on a common field, such as e-mail address. See the Microsoft Graph Data Connect documentation for details on the User Schema and a Sample of the output.
1. <TODO: Add link to sample from MGDC CPX team including AAD User export step>
https://github.com/microsoftgraph/dataconnect-solutions/tree/VIvaInsightsARM/ARMTemplates/genericPipelineWithAzureFunctionTrigger

## Consuming analytics data

To process analytics data sent to your application, you have the option of using either a “push” or a “pull” model to start processing.

### Push

In this model, the Azure Data Factory pipeline powering the data movement notifies your application when new data is available. This can be done through several means:

1. An Azure Function can be invoked when data in your Blob Storage account changes. See the Azure Function Overview and Blob Storage Trigger Sample to understand how this can be configured.
1. The Azure Data Factory pipeline can invoke a Web Activity that makes a REST call to your application’s backend, notifying it that new data is available.

The sample Data Factory Pipeline includes an example of an Azure Function with a Blob Storage Trigger.

### Pull

Your application can continuously poll the Blob Storage account for changes using the Blob Storage SDK or REST API. To do this, we recommend that your application maintain a “watermark” of the last processed folder’s timestamp so that failed processing can be retried.

The SDK or REST API can be used to download data from your Blob Storage account to a local destination (or cloud storage outside of Azure).
 
## Use integrated data

Work with your Microsoft Service representative to coordinate who to work with for joint customers that need help with Viva Insights Partner integration pilots.
