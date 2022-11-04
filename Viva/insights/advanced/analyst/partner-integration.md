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

Use this integration to export and combine Microsoft Viva Insights collaboration data with partner application data. Then, use the combined data for more advanced customer analysis, like identifying behaviors and patterns behind key metrics.

To facilitate this integration, we use an Azure Data Factory pipeline. Refer to [Process](#process) for further information about how this pipeline works.

## About Viva Insights data

Viva Insights calculates metrics based on Exchange Online mailbox data, like email and calendar data. For details about metrics used in Viva Insights data, refer to [Advanced insights metrics](../reference/metrics.md).

## Prerequisites

### For partners

Before you can use this integration, you’ll need to:

1. Complete the program form to join the Microsoft Graph TAP partner program. Joining the program gives you access to the Azure APIs you use to access Viva Insights. In the form, include these details: 
    1. For **Microsoft Graph workload**, select **Data Connect**. 
    1. In **Justification for TAP entry**, enter what partner data you want to integrate with Viva Insights data through a Microsoft Graph API.
2. Set up a test Azure environment to build your solution within your Microsoft 365 developer environment. Go to [Create your free Azure account today](https://azure.microsoft.com/free/) and select **Start free** to get started. You can access sample data after you set up this test environment.
3. Create an Azure Data Lake Storage Gen2 storage account resource. This account is where we deliver the final data drop to your tenant. 
4. Register a new application on the partner tenant:
    1. Select **Azure Active Directory**. 
    1. Go to the **Application registrations** blade and select **App registrations**, then **New registration**. 
    1. Provide a name for your application, set the application to be multi-tenant, leave the other settings on the defaults, then select **Register**. Learn how to configure multitenancy in [Making your application multi-tenant](/azure/active-directory/develop/howto-convert-app-to-be-multi-tenant#update-registration-to-be-multi-tenant).
5.	Create an Azure Key Vault. You’ll store per-tenant encryption keys here, in the **Keys** section. 
    1. For each customer tenant extraction, create a key and make the name the customer tenant GUID. Make sure each key is unique—that is, you can’t repeat the same key for two different tenants. Learn more about keys in [About keys](/azure/key-vault/keys/about-keys). 
    1. Make sure the key has a valid expiration date. 
    1. On the **Access Policies** page, create a new policy. Under **Key permission**, select **GET**. On the next page, select the app created in the previous step. Finish creating the new policy.
    
    When you fill out the Microsoft Graph Data Connect Application Preview Registration form in the next step, you’ll provide the Azure Key Vault’s URI found in the **Overview** page. All Viva Insights data will be returned encrypted. For more details, refer to this document’s [Customer onboarding](#customer-onboarding) and [Encryption and compression](#encryption-and-compression) sections.
6.	Fill out the [Microsoft Graph Data Connect Application Preview Registration Form](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR-mfqDTQy0ZMj1EdmSbUSwxUOUwyOEVWMkxCTTFTTlVXS1JDQ0xEMjVDUyQlQCN0PWcu).
    1. For question 2, **Organization Type**, select **ISV (Independent Software Vendor)**.
    1. Fill out question 12, **Azure Key Vault URL**, with the Azure Key Vault URL generated earlier (**SourceLinkedService**).
    1. For question 13, **Microsoft Graph Data Connect datasets requested**, select the following:
        1. **BasicDataSet_v0.User_v1**
        1. **VivaInsightsDataset_PersonReport_v1**
        
        *Skip to question 57.*

    1. On question 57, **BasicDataSet_v0.User_v1 dataset columns**, select all checkboxes.
        
        *Skip to question 60.*

    1. On question 60, **VivaInsightsDataset_PersonReport_v1 dataset columns**, select the **All metrics** checkbox.
    1. Complete and submit the form.
1.	Complete customer onboarding as described in the following section.

#### Customer onboarding

>[!Note]
>While private preview is still in effect, Microsoft Graph Data Connect (MGDC) needs to explicitly enable the new MGDC admin center experiences for cross-tenant data movement for *each* customer tenant. For each new customer you onboard, send their tenant ID to dataconnect@microsoft.com. 

As detailed earlier in step 5a, you need to generate a unique RSA-2048 key pair for each customer to extract customer data. Your application can securely generate and store RSA-2048 certificates (containing key pairs) by using [Azure Key Vault](/azure/key-vault) or a custom solution.

>[!IMPORTANT] 
>Don’t reuse certificates for multiple customers. Duplicate keys will be rejected as a security risk.

We use the public portion of the RSA key pair to encrypt the decryption key, and you use its corresponding private portion to decrypt the decryption key after you receive the data drop. This process makes sure that Microsoft can safely store your decryption key—only your application can decrypt the decryption key by using the private key, and only you have access to the private key. The decryption key is an AES 256-bit symmetric key used for encrypting the file. For more details about encryption, refer to [Encryption and compression](#encryption-and-compression).

The customer needs to consent to your application before data extraction can begin. Choose one of two ways to help your customer navigate to your application on their Microsoft 365 Admin Center, where they can approve it:

* **Direct link (recommended):** Send the customer the following link with your app registration information filled in. This link takes your customer admin directly to your MGDC app on the Microsoft 365 Admin Center, where they can review and consent to your application:
`https://admin.microsoft.com/Adminportal/Home#/Settings/MGDCAdminCenter/{PartnerAppRegistrationTenantId}/{PartnerApplicationId}`

    >[!Note]
    >This link is the same for all customers.

* **Tenant and application ID:** Share the partner application’s tenant ID and partner application ID with the customer. They’ll then search for your application manually through the Microsoft Graph Data Connect Admin Center and add a new multi-tenant app. Customers can refer to question 6 in the FAQs for detailed instructions on adding an app through its ID.

### For customers

Before you can use this integration, you’ll need to:

* Set up an [Azure tenant](/azure/active-directory/fundamentals/active-directory-access-create-new-tenant) and an administrator account. We’ll refer to this tenant as the “customer tenant.”
* Set the customer tenant up with a Consent Request Approvers group in the Microsoft 365 admin center.
* Enable Microsoft Graph Data Connect (MGDC) for the customer tenant, which is the platform you’ll use to export the Microsoft 365 data. Refer to the [Overview](/graph/data-connect-concept-overview) page for more information about MGDC.
* Have your tenant admin enable the Viva Insights dataset for the customer tenant. They can enable this dataset from the Microsoft 365 admin center, as we describe in the [FAQ](#q5-how-do-i-enable-viva-insights-dataset-and-cross-tenant-data-movement-as-a-customer).
* Allow cross-tenant data movement so the partner can extract your customer dataset. We’ve provided detailed instructions in the [FAQ](#q5-how-do-i-enable-viva-insights-dataset-and-cross-tenant-data-movement-as-a-customer) about how to allow cross-tenant movement.
* Have your tenant admin approve your partner’s application before data extraction starts. This consent is fetched and validated against when the partner kicks off the data extraction. We provide detailed instructions on how customers can approve your application in the [FAQ](#q6-how-do-i-approve-a-partners-mgdc-application-as-a-customer).

## Process

This integration moves behavioral analytics data between Azure and your partner application through an [Azure Data Factory pipeline](/azure/data-factory/concepts-pipelines-activities?tabs=data-factory). We built a [sample Data Factory Pipeline template](https://github.com/niblak/dataconnect-solutions/tree/vivaarmtemplates/ARMTemplates/VivaInsights/SamplePipelineWithAzureFunction) that you  can edit and deploy to your Azure subscription. After you add your parameters, this template configures the pipeline.

After it’s deployed to your subscription, the pipeline extracts data from Microsoft 365 to the Blob Storage account owned by your application. We recommend that you create a separate container for each customer’s data, using their Azure Active Directory tenant ID as the name.

If you want, you can add an extra step to your pipeline that notifies your external application new data is available for processing. We explain how to do this [later](#process-analytics-data).

### Flow

*Applies to: partners*

To use this integration, here’s what you’ll need to do.

#### Edit the template, provision a client secret, and deploy the template

1.	Edit the sample [Data Factory Pipeline template](https://github.com/niblak/dataconnect-solutions/blob/vivaarmtemplates/ARMTemplates/VivaInsights/SamplePipelineWithAzureFunction/mainTemplateV1.json) (also known as an Azure Resource Manager [ARM] template) from GitHub for your specific use case. This template defines the Azure Data Factory pipeline and associated resources that will be deployed to Azure, in your Azure subscription, to move data to your subscription.
1. Provision a client secret for the application you created [earlier](#for-partners). Store the secret in the Azure Key Vault you made earlier, unless you’re using a custom solution. 
1.	On your Azure subscription, deploy the template:
    1. In the Azure portal, select **Deploy a custom template**.
    1. Select **Build your own template** in the editor and copy the contents of the sample template we provided on GitHub.
    1. Select a **Resource group** and **Region** to deploy to.
    1. Provide values for the parameters specified in the template:
        * The **App Id** is the ID you received when you registered the app in [Prerequisites](#for-partners).  
        * The **App Secret** is the secret generated when you registered the app in [Prerequisites](#for-partners). 
        * The **AzureActiveDirectoryTenant Id** is the Azure Active Directory Tenant Id of the customer whose data needs to be extracted.

    ![Screenshot that shows the Custom deployment screen on Azure. The last three fields (App Id, App Secret, and Azure Active Directory Tenant Id are highlighted.)](/viva/insights/advanced/images/custom-deployment.png)

### Access customer data from the data drop

4. Viva Insights generates an encryption key. Refer to [Encryption and compression](#encryption-and-compression) for details.
1. Begin your MGDC data extraction by triggering the pipeline (either manually or through the template’s automatic run). You’ll receive the encrypted customer data in the storage account that you configured as the destination. 
1. Your application needs to reverse the encryption and compression process to access the original data. To access the customer data from the data drop:
    1. Get the decryption key from the extraction metadata.
    1. Decrypt the encryption key with the partner-customer private key, which is provided in the Azure Key Vault.
    1. Decrypt the entire file with the file encryption key. (Here's a [C# sample](/dotnet/api/system.security.cryptography.aes).)
    1. Decompress the entire file to get the extracted data. (Here's a [C# sample](/dotnet/api/system.io.compression.gzipstream).)

>[!Note]
> You can also perform this decryption and decompression process using a sample application that we share with you. Reach out to the Microsoft Viva team for access to this sample application.

#### Take optional steps

At this point, you’ve completed all required steps and should have access to your decrypted customer data. However, you might need to take a few optional steps, like joining Viva Insights data with other data, or using a pull rather than a push model to process analytics data. If that information applies to you, refer to Optional steps. We also recommend you review best practices for storing customer data in [About storing customer data](#about-storing-customer-data).

## About metadata, encryption and compression, and the pipeline

In this section, we provide some additional information about metadata, encryption and compression, and the Azure Data Factory pipeline.

### Metadata file

As we mentioned earlier, after you extract customer data, you’ll receive a data drop. Each data drop includes a **Metadata.json** file, with the path of **metadata/JobMetadata** in the root directory. This JSON file includes details about the copy activity with the following schema:

|Field|Description|
|---|----|
|**CopyActivityId**	|A unique identifier for the copy operation that you can use to get a decryption key for the file.
**JobSubmissionTime**|	The time that the Data Factory pipeline started.
**JobCompletionTime**	|The time that the Data Factory pipeline ended.
**RequestStartDate**	|The starting time period for which behavioral analytics data was extracted.
**RequestEndDate**	|The ending time period for which behavioral analytics data was extracted.
**ColumnsRequested**	|A comma-separated list of the columns included in the output.
**NumberOfRowsExtracted**	|The number of rows in the output.
**DataFactoryName**	|The name of the Data Factory pipeline.
**TenantId**	|The Azure Active Directory tenant that the partner analytics data was extracted for.
**Errors**	|A string describing errors encountered while processing the copy operation. If this property is non-empty, no output file will be present.
**TableName**	|Viva data set activity name and version. The expected format of the tablename is “VivaInsightsDataset_{activityName}_{datasetVersion}”.
**ApplicationId**  |The ID of the application making the request.
**OfficeGeo**	|The M365 region.
**ExtractionResultId**    | 	The Unique identifier of the extraction operation result.
**PublicKeyVersion**  |	The version of the public key.
**DecryptionKeyDetails**	|The details about the decryption key.

### Encryption and compression

Customer data is compressed with GZIP compression and encrypted with a symmetric AES-256 file encryption key—which is unique to each pipeline run—before being delivered to your application. To access the original data, your application needs to reverse the encryption and compression process. 

#### Where to find the decryption key and public key

Find both the decryption key for your application and the key version of the partner-customer specific public key in the extraction metadata file:

* The **DecryptionKeyDetails** field contains the decryption key. 
* The **PublicKeyVersion** field contains the partner-customer specific public key. The public key version helps you understand which version of the private key you should use to decrypt the decryption key.

#### About decryption keys

The decryption key comes encrypted as a base 64 string with the per-customer tenant public key provided in the Azure Key Vault. Decryption keys consist of the following components:

* **DecryptionKeyType** – Indicates whether the decryption key is intended to be used to decrypt an entire file. The value will be **File**.
* **value** – The Base-64 representation of the decryption key’s value. For example: 
`oF8xFGjrhxC2LsrsrUA3eTCWDl2fYlBkUe886jRLnKFwdbH/9SRA+55ekL42JCcL+iXsQNZdMWmy3LnLgk2nSfZ96ecU/++sOM7QB/6kWrS2Wmg+5XCW5FErodnyBZKCbOo1RETgrxTH8YlcoLX5319VCmBleSMxgitn0Jl+VCM+NjfE87oPWyLo+vifaBtFnIgSOkzKh20dZm/Ue1AxXQlYQ/WptHBRa4Lmza/oXgbTpqk9Y+Mw+4IhVtHbCdcEt0DqQ0FRb/qjlwMPaYqOlZ5GxFTiQFsAtYVTpnvcffkDBp1gzlOL2iLhudc66PP4h6v4cBxHx6RTz8bO4KiaQg==`
* **iv** – The Base-64 representation of the initialization vector used to create the decryption key. For example: `vLvaqqAN8GaYI9gGuX1bsQ==`

#### About storing customer data

Here are a couple of best practices for storing customer data:

* Don’t permanently store decrypted files in Azure or on-premises storage. Your application should decrypt the behavioral analytics data in real-time as it’s being processed. The decrypted contents shouldn’t be written to the disk.
* Make sure that your Azure Data Factory pipeline includes a step to clean up analytics data on the customer’s storage account after it’s has been transferred to your application’s storage. Our sample Data Factory pipeline on GitHub includes this step.

### Pipeline

#### Cadence and configuration

Viva Insights processes behavioral analytics data once a week. You can run your pipeline more frequently than weekly, but you’ll get the same output until the following week. 

The sample Azure Data Factory pipeline we’ve provided on GitHub includes a [trigger](/azure/data-factory/concepts-pipeline-execution-triggers) that executes the pipeline once every seven days, which is the recommended frequency.

### Optional steps

You might need to take one or both of these steps depending on your use case:

* If you don’t have access to your customer’s tenant directory information, you can use the information in [Join Viva Insights data with other data](#join-viva-insights-data-with-other-data) to export Azure Active Directory user data. In the sample Data Factory Pipeline we’ve provided on GitHub, this step is marked as **OPTIONAL**.
* If you want to continuously poll the Blob Storage account (that is, use a pull model) for changes instead of using the sample pipeline’s Azure function, refer to [How to use a pull model](#how-to-use-a-pull-model).

#### Join Viva Insights data with other data

The analytics data includes the Azure Active Directory Object ID of each user that generated a row of data. The Object ID can be used to correlate a directory user with a user in your application. However, while identifying users by the Object ID is the preferred method, not every application has access to the customer tenant’s directory information.

If you don’t have this access, you can export directory information and correlate it with a common field by following these steps:

1.	Configure your Azure Data Factory pipeline to add an additional step to export Azure Active Directory user data. This step is provided, but marked as **OPTIONAL**, in our sample pipeline on GitHub. Adding this step creates an additional output file from your pipeline that includes basic information about each user in the customer’s tenant.
2.	Use this output from step 1 correlate user information between Azure and your application with a join of a common field, such as e-mail address. Refer to the Microsoft Graph Data Connect documentation for details on the [user schema](https://github.com/microsoftgraph/dataconnect-solutions/blob/main/datasetschemas/User_v1.md) and a [sample of the output](https://github.com/microsoftgraph/dataconnect-solutions/blob/main/sampledatasets/BasicDataSet_v0.User_v1.json).

### Process analytics data

To process analytics data sent to your application, you have the option of using either a push or a pull model to start processing. The sample pipeline we provide on GitHub uses a push model, which works like this:

The Azure Data Factory pipeline powering the data movement notifies your application when new data is available. There are a couple of ways the pipeline can do this:

* It can invoke an Azure function when data in your Blob Storage account changes. Refer to the [Azure function overview](https://github.com/microsoftgraph/dataconnect-solutions/tree/VIvaInsightsARM/ARMTemplates/genericPipelineWithAzureFunctionTrigger) and [Blob Storage trigger sample](/azure/azure-functions/functions-bindings-storage-blob-trigger?tabs=in-process%2Cextensionv5&pivots=programming-language-csharp) to understand how this function is configured. This is the method our sample pipeline on GitHub uses.
* The Azure Data Factory pipeline can invoke a web activity that makes a REST call to your application’s backend, notifying it that new data is available. Web activities are described in [Web activity in Azure Data Factory and Azure Synapse Analytics](/azure/data-factory/control-flow-web-activity). You can edit our sample template to include this activity as an extra step.

#### How to use a pull model

Optionally, you can have your application continuously poll the Blob Storage account for changes using the [Blob Storage SDK](/azure/storage/blobs/storage-quickstart-blobs-dotnet) or [REST API](h/rest/api/storageservices/). To do this, your application can maintain a “watermark” of the last processed folder’s timestamp so that failed processing can be retried.

Use the SDK or REST API to download data from your Blob Storage account to a local destination (or cloud storage outside of Azure).

### Related information 

#### Applicable metrics

We list applicable metrics in [Advanced insights metrics](../reference/metrics.md). 

#### How to simulate a data drop with sample data

To quickly prototype an application built on the Viva Insights integration, you can use sample data to simulate a data drop received from a customer. To do so:

1.	Upload [Viva Insights sample data](https://raw.githubusercontent.com/niblak/dataconnect-solutions/vivaarmtemplates/sampledatasets/VivaInsightsDataset_v1.json) to a storage account in your test environment. Refer to [How to upload data to Azure](/azure/storage/blobs/storage-quickstart-blobs-portal) for further details. 
2.	Build your application to retrieve the behavioral analytics data:
    1. Download the data from your Azure Storage Account. To download this data, you can use the [SDK](/azure/storage/blobs/storage-quickstart-blobs-dotnet) or the [REST API](/rest/api/storageservices/).
    1. Ingest the data into your partner application. Steps vary based on what your application requires.

## FAQ

### For partners

#### Q1. How large will my output file be?

A1. The following sizes are *estimates* of final output size for analytics data. These estimates are extrapolated from a real-world baseline—a 175K-person set of Microsoft tenant data.

|Tenant size (licensed users)|	Date range	|Compressed size	|Uncompressed size|
|----|----|----|----|
400K| 3 months| 189 MB | 985 MB
200K | 3 months | 94 MB | 492 MB
175K | 3 months | 83 MB | 430 MB
100K | 3 months | 47 MB | 245 MB
50K | 3 months | 23 MB | 123 MB
25K | 3 months |11 MB |61 MB

#### Q2. Does the analytics data received from Viva Insights include all users in the customer’s tenant?

A2. Viva Insights analytics data is only calculated for users who are assigned a Viva Insights license. Unlicensed users aren’t included in the data.

#### Q3. How frequently is analytics data calculated?

A3. Currently, analytics data is calculated once a week. For subsequent runs of an existing pipeline, new data will be available every Monday.

#### Q4. Given the potentially large file size, how can the data be processed efficiently?

A4. Though the output format is JSON, the output file isn’t a fully formed JSON document. Each row of analytics data is modeled as a single JSON object. This format allows you to stream the file, instead of parsing the entire JSON tree and consequently loading the full file into memory.

We recommend that you stream in analytics data line-by-line. Don’t try to load the entire file into memory. To further improve read performance, your application can divide the stream into segments that are processed by separate threads. This approach leverages multiple cores.

### For customers

#### Q5. How do I enable Viva Insights dataset and Cross-Tenant data movement as a customer?

A6. A global admin for the customer tenant needs to enable the dataset and cross-tenant data movement. In the admin portal (admin.microsoft.com), under **Microsoft Graph Data Connect** settings, they’ll select the option to enable **Viva Insights dataset** and **Cross-Tenant data movement**. This link takes the admin into the Microsoft Graph Data Connect settings page in the admin portal:
https://admin.microsoft.com/Adminportal/Home#/Settings/Services/:/Settings/L1/O365DataPlan.
 
#### Q6. How do I approve a partner’s MGDC application as a customer?

A6. A global admin for the customer tenant needs to consent to the partner’s application. To review the application, they’ll either need a direct link from the partner or the partner’s app details (partner app registration tenant ID and partner application ID). 

To approve a partner’s request:

1. Find the partner’s MGDC application. You can find it in one of two ways:
    1. Option 1: Use the direct link the partner provided.
    1. Option 2: Search for the partner’s MGDC application manually using the partner app registration tenant ID and partner application ID. 
        1. Go to the MGDC admin center: https://admin.microsoft.com/Adminportal/Home#/Settings/MGDCAdminCenter.
        1. Select **Add new multi-tenant app**.
        1. Enter the app registration information that the partner gave you, then select **Find**. 
1. Approve the app by going through each screen: **Overview**, **Datasets**, and **Review**. Carefully review the information on each screen before selecting **Next**.
    1. **Overview**: Review information about the application and data destination.
    1. **Datasets**: Review details about which datasets and columns the application wants to extract. Your approval only allows the application to extract the datasets and columns specified here. Make sure you’re fully reviewing each dataset; for each dataset, expand the list of columns the application is requesting to extract. 
    1. **Review**: After taking another look at the app publisher and the data destination, **Approve** or **Decline** the application to extract the requested datasets. Your approval or denial isn't committed until you select the **Approve** or **Decline** button. If you approve, your approval remains valid for the next 180 days. 
3.	If you approved, return to the Microsoft Graph Data Connect Admin Center landing page. The app you just approved should appear in the summary table. 

## Related topics

[Advanced insights metrics](../reference/metrics.md)

[Sample Azure Data Factory template](https://github.com/niblak/dataconnect-solutions/tree/vivaarmtemplates/ARMTemplates/VivaInsights/SamplePipelineWithAzureFunction)


