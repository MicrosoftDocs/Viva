---
ROBOTS: NOINDEX,FOLLOW
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

This integration enables you to export and combine Microsoft Viva Insights collaboration data with partner application data within Azure. You can then use the combined analysis for a more advanced, customer analysis, such as to identify behaviors and patterns behind key metrics.

## Viva Insights data

[My organization in Teams](../../use/viva-insights-my-org.md) shows what kind of Viva Insights data can be integrated with your partner application data. For details about the metrics used within Viva Insights data, see [Viva Insights metrics](metrics.md).

## Partner prerequisites

* To use this integration as a partner, you must complete [the program form](https://aka.ms/GraphTAPForm) to join the "Microsoft Graph TAP partner program" for support of the Azure APIs used to access Viva Insights:

  * For **Microsoft Graph workload**, select **Data Connect**.
  * In **Justification for TAP entry**, enter what partner data you want to integrate with Viva Insights data through a Microsoft Graph API.

* Before you can access the sample data, you need to set up a test Azure environment to build your solution. Go to [Create your free Azure account today](https://azure.microsoft.com/free/) and select **Start free** to get started.

## Customer prerequisites

* Have an [Azure tenant](/azure/active-directory/fundamentals/active-directory-access-create-new-tenant) and an administrator account set up.
* Have the tenant set up with a [Consent Request Approvers group](/azure/active-directory/manage-apps/configure-admin-consent-workflow) in the Microsoft 365 admin center.
* Enable [Microsoft Graph Data Connect](/graph/data-connect-concept-overview) for the tenant, which is the platform you'll use to export the Microsoft 365 data.

## Flow overview

The following steps describe the flow that's required by you as a Viva Insights partner and your customer for this integration. These steps include the previously described prerequisites for both you and your customer.

1. Edit the sample [Azure Resource Manager (ARM) Template](https://github.com/niblak/dataconnect-solutions/blob/vivaarmtemplates/ARMTemplates/VivaInsights/SamplePipelineWithAzureFunction/mainTemplate.json) for your specific use case. The ARM template defines the Azure Data Factory pipeline and associated resources that will be deployed to Azure, in your customer’s Azure subscription, to move data from their subscription to yours.
1. On your partner tenant:
    1. Create a Blob storage account resource. This resource will be used to deliver the final data drop from the customer tenant to yours.
    1. Create a container and navigate to the **Shared Access Tokens** blade.
    1. Create a token with **Write** permissions for the container and note down the  Blob SAS URL that was generated.
  
  > [!Note]
  > The requirement to create a SAS URL will be removed in an upcoming release.

3. On the customer tenant, create a new registration:
    1. Select **Azure Active Directory**.
    1. Navigate to the Application registrations blade and select **App registrations**, then **New registration**.
    1. Provide a name for your application, leave the other settings on the defaults, then select **Register**.
1. On the customer tenant, the customer must provision a client secret for the application created in the previous step. The customer should store the secret in a secure location, such as an Azure Key Vault. For more details, refer to [Move data](#move-data).

  > [!Note]
  > The requirement to create an application registration and client secret on the customer tenant will be removed in an upcoming release.

5. On the customer tenant, deploy the template:
    1. In the Azure portal, select **Deploy a custom template**.
    1. Select **Build your own template** in the editor and copy the contents of your ARM template.
    1. Select a **Resource group** and **Region** to deploy to.
    1. Provide values for the parameters specified in your ARM template:
        * For the sample template, the **SAS Url** is the URL that was generated in step 2.
        * The **App Id** is the Application (Client ID) of the application created in step 3.
        * The **App Secret** is the secret generated in step 4.

        ![Screenshot of the Custom deployment screen with fields mentioned in step 5d above](/Viva/insights/Images/advanced/custom-deployment.png)

        > [!Note]
        > The ARM template will be able to be deployed directly to your partner tenant, instead of the customer’s, in an upcoming release.

1. As the partner, you must call the Partner key through the [Viva Insights API](api.md) to create a unique RSA-2048 bit key for your customer. For more details, see [Customer onboarding](#customer-onboarding).
1. The customer approves the consent request to kick-off the data extraction, and then the data drops in your partner data store.
1. Viva Insights then generates an encryption key. See [Encryption and compression](#encryption-and-compression) for details.
1. As the partner, you then can decrypt the customer data with the encryption key. See [Join Viva Insights data with other data](#join-viva-insights-data-with-other-data) for details and next steps to push and pull data for the integration.

## Move data

With this integration, behavioral analytics data is moved between Azure and your partner application through an [Azure Data Factory pipeline](/azure/data-factory/concepts-pipelines-activities).

This pipeline needs to be configured by a *partner-provided* Azure Data Factory template in the customer’s Azure tenant. The pipeline must do the following tasks:

1. Extract data from Microsoft 365 to a temporary storage location in the customer’s tenant.
1. Copy data from the temporary location to a Blob Storage account owned by your application, with a [Shared Access Signature (SAS) key](/azure/storage/common/storage-sas-overview) that you generate, and is entered when the application is installed by the customer.
1. (Optional) Notify your partner application that new data is available for processing.

See the [sample Data Factory pipeline](https://github.com/niblak/dataconnect-solutions/tree/vivaarmtemplates/ARMTemplates/VivaInsights/SamplePipelineWithAzureFunction) as an example of how to move data (described in the previous steps).

### Metadata file

Each data drop includes a **Metadata.json** file, with the path of **metadata/JobMetadata** in the root directory. The JSON file includes details about the copy activity with the following schema:

|Field |Description |
|-------|----------|
|CopyActivityId |A unique identifier for the copy operation that you can use to get a decryption key for the file. |
|JobSubmissionTime |The time that the Data Factory pipeline started. |
|JobCompletionTime |The time that the Data Factory pipeline ended. |
|RequestStartDate |The starting time period for which behavioral analytics data was extracted. |
|RequestEndDate |The ending time period for which behavioral analytics data was extracted. |
|ColumnsRequested |A comma-separated list of the columns included in the output.
|NumberOfRowsExtracted |The number of rows in the output. |
|DataFactoryName |The name of the Data Factory pipeline. |
|TenantId |The Azure Active Directory tenant that the partner analytics data was extracted for. |
|Errors |A string describing errors encountered while processing the copy operation. If the property is non-empty, no output file will be present. |

## Customer onboarding

To enable data extraction for a customer, your application must call the Partner key through the [Viva Insights API](api.md) to provide the Azure Active Directory tenant ID of your customer and the **public key** of a unique [RSA-2048](https://en.wikipedia.org/wiki/RSA_numbers) key pair that you have generated for this customer. Your application can securely generate and store RSA-2048 certificates (containing such a key pair) using [Azure Key Vault](/azure/key-vault/), or you may use a custom solution.

>[!Important]
>Do not reuse certificates for multiple customers. The Partner key API will reject duplicate keys as a security risk.

The public key is used to encrypt the **decryption keys** described in the following section. Microsoft can then safely store your decryption keys because only your application can decrypt the keys by using the private key that only you have access to.

## Encryption and compression

Behavioral analytics data is first compressed with [GZIP compression](https://datatracker.ietf.org/doc/html/rfc1952), and then it's encrypted in two stages before being delivered to your application. Sensitive, personally identifiable information, such as the Azure Active Directory Object ID, is encrypted with a **column encryption key**. The file is then encrypted with a **file encryption key**.

The two keys are unique to each pipeline run. Your application must request these keys from the Decryption key, as described in [Viva Insights API](api.md), by using the **CopyActivityId** located in the metadata file. The Decryption keys are symmetric [AES-256 keys](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard).

Your application must reverse the encryption and compression process to access the original data, as described in this section:

1. Decompress the file ([C# sample](/dotnet/api/system.io.compression.gzipstream/)).
1. Call the Decryption key through the [Viva Insights API](api.md) to retrieve the file and column encryption keys.
1. Decrypt the entire file with the file encryption key ([C# sample](/dotnet/api/system.io.compression.gzipstream/)).
1. Stream the file into your application. When encrypted properties (such as Object ID) are encountered in the JSON object, decrypt the property with the column encryption key.

>[!Note]
>In a future release, your customers will be able to choose whether your application receives the column encryption key or not. If this setting isn't enabled, your application cannot decrypt identifying information about users and will only have access to aggregated analytics data. For the *Private Preview release*, this setting must always be **On**.

## Pipeline cadence and configuration

Behavioral analytics data is processed by Viva Insights once a week. Your pipeline might run more frequently, but the same output will be returned until the following week.

The sample Data Factory pipeline includes a [Trigger](/azure/data-factory/concepts-pipeline-execution-triggers) that will execute the pipeline once every seven days, which is the recommended frequency.

## Join Viva Insights data with other data

The analytics data includes the Azure Active Directory Object ID of each user that generated a row of data. The Object ID can be used to correlate a directory user with a user in your application.

While identifying users by the Object ID is the preferred path, not every application may have access to the customer tenant’s directory information. You can do this with the following steps.

### Export the directory information along with the analytics data

1. Configure your Azure Data Factory pipeline to add an additional step to export Azure Active Directory user data.
1. This will create an additional output file from your pipeline that includes basic information about each user in the customer’s tenant. This file can be used to correlate user information between Azure and your application by joining on a common field, such as e-mail address. See the Microsoft Graph Data Connect documentation for details on the [User Schema](https://github.com/microsoftgraph/dataconnect-solutions/blob/main/datasetschemas/User_v1.md) and a [Sample of the output](https://github.com/microsoftgraph/dataconnect-solutions/blob/main/sampledatasets/BasicDataSet_v0.User_v1.json).

The [sample Data Factory pipeline](https://github.com/niblak/dataconnect-solutions/tree/vivaarmtemplates/ARMTemplates/VivaInsights/SamplePipelineWithAzureFunction) includes an example of a pipeline that exports directory information.

## Consume analytics data

To process analytics data sent to your application, you have the option of using either a “push” or a “pull” model to start processing.

### Push

In this model, the Azure Data Factory pipeline powering the data movement notifies your application when new data is available. This can be done through several means:

1. An Azure function can be invoked when data in your Blob Storage account changes. See the [Azure Function Overview](https://github.com/microsoftgraph/dataconnect-solutions/tree/VIvaInsightsARM/ARMTemplates/genericPipelineWithAzureFunctionTrigger) and [Blob Storage Trigger Sample](/azure/azure-functions/functions-bindings-storage-blob-trigger?tabs=in-process%2Cextensionv5&pivots=programming-language-csharp) to understand how this can be configured.
1. The Azure Data Factory pipeline can invoke a [Web Activity](/azure/data-factory/control-flow-web-activity) that makes a REST call to your application’s backend, notifying it that new data is available.

The sample [Data Factory Pipeline](https://github.com/microsoftgraph/dataconnect-solutions/tree/VIvaInsightsARM/ARMTemplates/genericPipelineWithAzureFunctionTrigger) includes an example of an Azure Function with a Blob Storage Trigger.

### Pull

Your application can continuously poll the Blob Storage account for changes using the [Blob Storage SDK](/azure/storage/blobs/storage-quickstart-blobs-dotnet) or [REST API](/rest/api/storageservices/). To do this, your application can maintain a “watermark” of the last processed folder’s timestamp so that failed processing can be retried.

You can use the SDK or REST API to download data from your Blob Storage account to a local destination (or cloud storage outside of Azure).

## Supported metrics

The supported metrics for the *Private Preview release* are listed below.

| Metric Name | Column Name | Data Type | Precision/Format |
|--------|-------------|-----------|-----------------|
|MetricDate | MetricDate | DateTime | UTC Format |
|IsActive | IsActive | Boolean | Not applicable |
|After hours collaboration hours | AfterHoursCollaboration | Float | 6-9 digits |
|After hours email hours | AfterHoursCollaborationEmails | Float | 6-9 digits |
|After hours instant messages | AfterHoursCollaborationInstantMessages | Float | 6-9 digits |
|After hours meeting hours | AfterHoursCollaborationMeetings | Float | 6-9 digits |
|After hours in scheduled calls | AfterHoursCollaborationScheduledCalls | Float | 6-9 digits |
|After hours in unscheduled calls | AfterHoursCollaborationAdhocCalls | Float | 6-9 digits |
|Collaboration hours | CollaborationHours | Float | 6-9 digits |
|Email hours | CollaborationHoursEmails | Float | 6-9 digits |
|External collaboration hours | CollaborationHoursExternal | Float | 6-9 digits |
|Instant message hours | CollaborationHoursInstantMessages | Float | 6-9 digits |
|Meeting hours | CollaborationHoursMeetings | Float | 6-9 digits |
|Scheduled call hours | CollaborationHoursScheduledCalls | Float | 6-9 digits |
|Unscheduled call hours | CollaborationHoursAdhocCalls | Float | 6-9 digits |
|Conflicting meeting hours | ConflictingMeetingHours | Float | 6-9 digits |
|Meeting hours with manager | DirectManagerMeetingHours | Float | 6-9 digits |
|Meeting hours with manager 1 on 1 | OneOnOneMeetingHours | Float | 6-9 digits |
|Meeting hours with skip level | SkipLevelMeetingHours | Float | 6-9 digits |
|Available to focus | TotalFocusHours | Float | 6-9 digits |

## Sample data

To quickly prototype an application built on the Viva Insights integration, you can use sample data to simulate a data drop received from a customer.

* Upload Viva Insights sample data to a Storage Account in your test environment. See [How to upload data to Azure](/azure/storage/blobs/storage-quickstart-blobs-portal/) for more details.
* Build your application to retrieve the behavioral analytics data, as follows:

  * Download the data from your Azure Storage Account. To do this, you can use the [SDK](/azure/storage/blobs/storage-quickstart-blobs-dotnet/) or the [REST API](/rest/api/storageservices/).
  * Ingest the data into your application. Steps will vary based on what your application requires.

## Diagnose pipeline problems

If there is a problem extracting behavioral analytics data from Viva Insights, the **Errors** property in the metadata file will be set. **Errors** will contain detailed information about the failure. No output file will be generated if the **Errors** property is set.

Contact Microsoft support to get help resolving the issue.

## Best practices for storing customer data

1. **Do not permanently store decrypted files in Azure or on-premises storage.** Your application should decrypt the behavioral analytics data in real-time as it is being processed. The decrypted contents should not be written to the disk.
1. Ensure that your Azure Data Factory pipeline includes a step to clean up analytics data on the customer’s storage account after it has been transferred to your application’s storage. The sample Data Factory pipeline includes this step.

## Deployment to a customer tenant

This *Private Preview release* is primarily aimed at partners who are interested in experimenting with building an integration on top of Viva Insights using synthetic (or test) customer data. The experience is not currently optimized for deployment to a retail customer.

Your Azure Data Factory pipeline can be deployed to a customer tenant during the *Private Preview release*, but it involves more steps than upcoming releases will. Instead of deploying an ARM template directly as described in the [Flow overview](#flow-overview) section, you can instead choose to package your template as a *Managed application* that is hosted in your Azure tenant. The customer can download and install the Managed application through a simplified process that is more user-friendly than deploying an ARM template, but still does not represent the final experience.

*If you want to package your template as a Managed application, perform the following steps **instead of** steps 1 – 5 in [Flow overview](#flow-overview):*

1. As a partner, you can author a Managed application containing your Azure Data Factory pipeline definition following the steps described here: Create and Publish a Managed Application Definition.  
1. Upload the Managed application source code package to a storage account within your Azure subscription. The source code package must include:  
    * The ARM template file with details for the Azure Data Factory and associated resources that control the data movement. This file must be named **mainTemplate.json**.  
    * UI definition file that defines your customer’s UI experience, such as which options or customizations they can make to the app. This file must be named **createUiDefinition.json**.  

>[!Important]
>You must store the source code package in a publicly accessible location for your customers to use it in the following steps. You can configure the blob container to host the package for anonymous read access.  

3. Your customer then needs to define and deploy the Managed application in their Service Catalog from the source code with a Shared Access Signature (SAS) key URI that you share with the customer. For details, see [Customer onboarding](#customer-onboarding).

## FAQ

**Q1. How large will my output file be?**

A1. The following are estimates of final output size for analytics data, which are extrapolated from a real-world 175K of Microsoft tenant data as a baseline:

|Tenant size (licensed users) |Date range |Compressed size |Uncompressed size
|-------|----------|----------|----------
|400K |3 months |189 MB |985 MB
|200K |3 months |94 MB |492 MB
|175K |3 months |83 MB |430 MB
|100K |3 months |47 MB |245 MB
|50K |3 months |23 MB |123 MB
|25K |3 months |11 MB |61 MB

**Q2. Does the analytics data received from Viva Insights include all users in the customer’s tenant?**

A2. Analytics data is only calculated for users who are assigned a Viva Insights license. Unlicensed users aren't included in the data.

**Q3. How frequently is analytics data calculated?**

A3. Currently, analytics data is calculated once a week. For subsequent runs of an existing pipeline, new data will be available every Monday.

**Q4. Given the potentially large file size, how can the data be processed efficiently?**

A4. Though the output format is JSON, it isn't a fully-formed JSON document. Each row of analytics data is modeled as a single JSON object. This allows the file to stream, instead of parse the entire JSON tree and consequently loading the full file into memory.

The recommended approach is to stream in analytics data line-by-line. Do not attempt to load the entire file into memory. To further improve read performance, your application can divide the stream into segments that are processed by separate threads to leverage multiple cores.

## Related topics

* [Viva Insights API](api.md)
* [Advanced insights metrics](metrics.md)