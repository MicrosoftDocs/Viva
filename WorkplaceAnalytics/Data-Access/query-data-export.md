---
ROBOTS: NOINDEX,NOFOLLOW
title: Automate query data export to Azure with Azure Data Factory UI
description: Steps for admins to set up an automated Workplace Analytics query data export to Azure through Azure Data Factory UI
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Automate query data export to Azure with Azure Data Factory UI

Do you need to combine Workplace Analytics query data with other Azure data sources, such as HR or Sales data for more advanced data analytics and reporting? Are you manually downloading large amounts of static query data from Workplace Analytics and then uploading it into Azure on a routine basis?

With Azure Data Factory and Azure Active Directory, you can automate the export of Workplace Analytics query data through the OData query link to connect and automatically refresh an Azure data store of your choice.

You can then join dynamically refreshed Workplace Analytics query data with other organizational datasets for more advanced analysis and data science projects.

## Pick a setup path

To set up the automated OData connection between Workplace Analytics query data and your choice Azure data store, you can use one of the following paths to create and configure a new Azure analytics app, which needs company-specific information (secrets) about your private network and your choice data store.

* [Set up with Azure Data Factory UI](#to-set-up-with-azure-data-factory-ui) – This path steps you through creating and registering an app and creating a data factory for the data export through the Azure Data Factory UI.
* [Set up with Azure PowerShell](https://github.com/microsoftgraph/M365Insights/blob/master/README.md) – This path automates the process end-to-end through PowerShell with predefined scripts that create and register the app, prompt for your organization’s specific parameters, and create and deploy the data factory.

## Prerequisites

* **Workplace Analytics licensed analyst** – Must be assigned a license and an Analyst role for Workplace Analytics and have query results with the data you want to export.
* **Microsoft Azure subscription** – If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/) now. You’ll be using [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/), [OData connector](https://docs.microsoft.com/azure/data-factory/connector-odata#supported-capabilities), and [Data Factory](https://docs.microsoft.com/rest/api/datafactory/) for this setup.
* **Azure data store** – Your data store must be [supported by the OData connector](https://docs.microsoft.com/azure/data-factory/connector-odata).
* **Azure admin** – You need Azure admin privileges to create and register the app in Azure. You also need to ask the Azure global admin to grant you permissions in Azure Data Factory to connect your new app to the Azure data store.

## To set up with Azure Data Factory UI

The following steps you through how to automate the export of Workplace Analytics query data to your choice Azure data store with the [Azure Data Factory UI](https://docs.microsoft.com/azure/data-factory/introduction). Use the following steps in conjunction with the [Azure documentation](https://docs.microsoft.com/azure/data-factory/introduction) to complete this setup.

1. Follow the steps in [Register an application using the Azure portal](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#register-a-new-application-using-the-azure-portal) to create and register a new analytics app in Azure Active Directory.
2. In **Azure Active Directory App registrations**, select the app from **Step 1**,  and then grant it permissions for accessing Workplace Analytics by selecting **View API permissions**, and then select **Add a permission**. 
3. Enter and search for the **Workplace Analytics App name** or **ID** and then select the applicable **Workplace Analytics app** from the list.

   ![App permissions](./images/app-permissions.png)
 
   To find the Application (client) ID:

   * In **Active Directory**, select **all applications**, and then enter **Workplace Analytics** for the Workplace Analytics enterprise app that you want to use.
   * Select **Workplace Analytics** from the list.
   * In **Workplace Analytics Application ID**, copy the ID and paste it in **APIs my organization uses** search field.

     ![Workplace Analytics Application ID](./images/app-id.png)

4.	In **Request API permissions**, select **Application permissions**, select **Analyst**, and then select **Add permissions**. 
5.	In **API permissions**, the global admin must select **Grant admin consent for [Workplace Analytics…]** before you can continue to the next step.

    ![Grant the app permissions](./images/permissions-grant.png)

6.	Follow the steps in [Create data factory](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal) to create a new analytics data factory within Azure Active Directory. 
7.	In the **Azure Data Factory Overview**, select **Author & Monitor** to open Azure Data Factory.

    > [!Note]
    > Keep all browser windows open because you must switch between them to complete the following steps.

8.	In **Azure Data Factory**, select **Create a pipeline**. 
9.	Select the **ellipsis** (**…**) next **Datasets**, and then select **New dataset**. For more details, see [Datasets in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/concepts-datasets-linked-services).
10. In **Select a data store**, enter **odata**, and then select **OData**. 
11. In **General**, enter a name and description for the Workplace Analytics query data you’re linking to.
12. Select **Connection**, select **New**, and then enter a name and description for the OData link, such as **WPA_Odata_Collab**.

13. In **Connect via integration runtime**, select **AutoResolveIntegrationRuntime**. 
14. In [Workplace Analytics](https://workplaceanalytics.office.com/) > **Queries** > **Results**, copy the OData link for the query data you want to connect to Azure.

    > [!Important]
    > For automatically refreshed data, you must link to a query that uses the [Auto-refresh option](https://docs.microsoft.com/workplace-analytics/tutorials/query-auto-refresh#create-a-query-with-the-auto-refresh-option). For static query results, you’ll need to enter a new OData link each time to update the query data in the connected Azure data store.

     ![Query OData link](./images/query-link.png)

15. In **Service URL**, paste the query OData link that you copied in the previous step. 
16. In **AAD resource**, enter `https://workplaceanalytics.office.com`. 
17. In **Active Directory**, select **Overview** for the new app, and then copy the **Application (client) ID**.

     ![Azure application ID](./images/azure-app-id.png)

18. In **Azure Data Factory** > **New linked service** > **Service principal ID**, copy the client ID. For  details, see [Linked service properties](https://docs.microsoft.com/azure/data-factory/connector-odata#linked-service-properties).

     ![Service principal ID](./images/service-princ-id.png)

19. In **Authentication type**, select either **AAD service principal with Key** or **AAD service principal with Cert**. Keep **New linked service (OData)** open in a separate browser window. For details about these options, see [Use Azure Key Vault secrets in pipeline activities](https://docs.microsoft.com/azure/data-factory/how-to-use-azure-key-vault-secrets-pipeline-activities).
20. In **Azure Active Directory** > **your newly registered analytics app**, select **Certificates & secrets**, and then do one of the following.

    * **For Key authentication**, select **New client secret** and in **Add a client secret**, enter a description, select when it expires, and then select **Add**. In **Client secrets**, select the new secret, and then select the **Copy icon** to copy it.
    * **For Certificate authentication** (preferred for higher security), select a certificate and copy it. 

21. In **Azure Data Factory**, do the following for the applicable authentication type:

    * For Service principal key, paste the new client secret copied in the previous step in **Service principal key**.
    * For **Azure key vault**, copy and paste the certificate and the other required information. See [Set and retrieve a secret from Azure Key Vault](https://docs.microsoft.com/azure/key-vault/secrets/quick-create-portal) for details. 

22.	Select **Test connection** to test the OData linked service. 
23.	After you see **Connection successful**, select **Create**. 
24.	In **Connection** > **Linked service** for the new OData linked service, select the new dataset you just created in the previous steps.
25.	In **Connection** > **Path**, select **Edit**, and then enter the **Entity set name**. To find it, copy the OData query link from [Workplace Analytics](https://workplaceanalytics.office.com/) > **Queries** > **Results**, and open it in a new browser window. Then search for **metadata** to find the entity name, which is shown after **$metadata#**. For example, the entity name shown in this graphic is **Persons**: 

     ![Query entity set name](./images/entity-set-name.png)

26. Select **Preview data** for the path to confirm you entered the correct entity. 
27. In Azure Data Factory > Properties, confirm the name and description for this new dataset. 
28. Select **Publish all** at the top, and then select **Publish**.
29. In **Pipelines**, create a new pipeline that can use the new OData dataset to copy the Workplace Analytics data to the external resource. For details, see [Create a pipeline](https://docs.microsoft.com/azure/data-factory/tutorial-copy-data-portal#create-a-pipeline).
30. For the new pipeline, select **Source**, and in **Source dataset**, select the name of new OData dataset, and in **Use query**, select **Table**. 
31. Create a linked service for the data store you want to export to. For details, see [Linked services](https://docs.microsoft.com/azure/data-factory/author-management-hub#linked-services).
32. In **Sink** > **Sink dataset**, select the linked service name you created in the previous step.

You can then use this new data factory to access query data from Workplace Analytics and copy it to your choice data store (blob storage) by using the Azure Resource Manager template. You can reuse this new app over time for multiple projects without having to repeat these steps. You can also reuse the data factory you created for new pipelines.

## Related topic

[Automate query data export with PowerShell](https://github.com/microsoftgraph/M365Insights/blob/master/README.md)
