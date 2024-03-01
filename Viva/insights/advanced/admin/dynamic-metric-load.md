---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 3/1/2024
title: Export Viva Insights data using MGDC
description: Use Microsoft Graph Data Connect (MGDC) to transfer backend Viva Insights data to Azure
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Export Viva Insights data using MGDC

*Applies to: private preview customers only*

If you want to use and analyze Viva Insights data outside of the Viva Insights app, you can use Microsoft Graph Data Connect (MGDC) to transfer the backend data to Azure. This process allows users to export whatever subset of metrics they want from Viva Insights, which can include both system metrics and customized metrics.

### Prerequisite steps

1. Provide the Tenant ID to the Viva Insights team. The Tenant ID can be found in the [Azure portal](https://portal.azure.com). Under **Azure services**, select **Microsoft Entra ID**, then find the **Tenant ID** on the **Overview** page.
1. The [Global Administrator](/azure/active-directory/roles/permissions-reference#global-administrator) will need to assign the relevant roles for the steps below, if they are not already assigned.

### Process overview

| Task | Role | Resources required |
|---|---|---|
| 1. Create Azure Active Directory Application  |  Application Administrator or Application Developer   |  |
| 2. Provision Storage Account  |  Application Administrator or Application Developer   |  |
| 3. Provision Key Vault and store client secret  |  Application Administrator or Application Developer   | App secret |
| 4. Enable MGDC for tenant  |  Global Administrator   |  |
| 5. Mark a Viva Insights query for export  |  Insights Analyst   |  |
| 6. Register MGDC application  |  Azure AD Application Owner, with Insights Analyst role   | Storage account, Azure AD Application  |
| 7. Consent to application/dataset  |  Global Administrator   |  |
| 8. Deploy ARM template  |  Application Administrator or Application Developer, with Insights Analyst role  | MGDC app, App secret, Container |
| 9. Execute pipeline  |  Application Administrator or Application Developer   | Data factory |
| 10. Find the output of your extraction |  Application Administrator or Application Developer   | Container name  |

## Steps

<a name='1-create-azure-active-directory-application'></a>

### 1. Create Microsoft Entra Application

*Applies to: [Application Administrator](/azure/active-directory/roles/permissions-reference#application-administrator) or [Application Developer](/azure/active-directory/roles/permissions-reference#application-developer)*

Follow steps 1-10 outlined [here](/graph/data-connect-quickstart?source=recommendations&tabs=NewConsentFlow%2CPAMMicrosoft365%2CAzureSynapsePipeline&tutorial-step=2) to create your app service principal. Be sure to store the app secret to use in a later step in this process. You can skip steps 11-13.

### 2. Provision Storage Account

*Applies to: Application Administrator or Application Developer*

Follow all steps outlined [here](/graph/data-connect-quickstart?source=recommendations&tabs=NewConsentFlow%2CPAMMicrosoft365%2CAzureSynapsePipeline&tutorial-step=3) to create your Storage Account. To select your region, [use these steps](/microsoft-365/enterprise/m365-dr-workload-other).

After you've followed the steps above and your Storage account is set up:

1. In your Storage account, under **Properties**, select the link to the right of **Blob soft delete**.

   :::image type="content" source="../images/dynamic-metric-load-step02.png" lightbox="../images/dynamic-metric-load-step02.png" alt-text="Screenshot that shows setting storage properties":::

2. Clear **Enable soft delete for blobs** and **Enable soft delete for containers** and select **Save**.

### 3. Provision Key vault and store client secret

*Applies to: Application Administrator or Application Developer*

1. Open a browser and sign in to your [Azure portal](https://portal.azure.com).
1. Under **Azure services**, select **Create a resource**.
1. Select **Create** on the **Key Vault** resource type and use the following values:
    * **Subscription:** Select your Azure subscription
    * **Resource group:** mgdc-app-resource (or select an existing resource group)
    * **Key vault name:** mgdcdemokeyvault (or you can name and select your own)
    * **Region:** Select region [using these steps](/microsoft-365/enterprise/m365-dr-workload-other).
    * **Pricing tier:** Standard
    * **Days to retain deleted vaults:** Default
    * **Purge protection:** Default

   :::image type="content" source="../images/dynamic-metric-load-step0301.png" alt-text="Screenshot that shows fields for creating a key vault":::

4. Select **Review + create**.
1. To complete Steps 6 and 7, assign yourself the Key Vault Secrets Officer or Key Vault Administrator role using [these instructions](/azure/key-vault/general/rbac-guide?tabs=azure-cli"%20%5Cl%20"azure-built-in-roles-for-key-vault-data-plane-operations#key-vault-scope-role-assignment).
1. In the **mgdcdemokeyvault** Key vault, on the sidebar menu, select **Secrets** under the **Objects** section. Select **+Generate/Import** and use the following values:
    * **Upload options:** Manual
    * **Name:** mgdc-app-secret (or you can name and select your own)
    * **Secret value:** Paste the app secret you stored in Step 1
    * **Set activation date:** Leave cleared
    * **Set expiration date:** Leave cleared
    * **Enabled:** Yes
    * **Tags:** 0 tags

6. Select **Create**.

### 4. Enable MGDC for tenant

*Applies to: Global Administrator*

1. Open a browser and sign in to your [Microsoft 365 Admin Portal](https://admin.microsoft.com/adminportal).
1. Under **Settings**, select **Org settings**. You may have to select **Show all** to see the **Settings** option. 
1. Under Services, select **Microsoft Graph data connect**.

   :::image type="content" source="../images/dynamic-metric-load-step0401.png" lightbox="../images/dynamic-metric-load-step0401.png" alt-text="Screenshot that shows how to enable the MGDC app for the tenant":::

4. Select **Turn Microsoft Graph Data Connect on or off for your entire organization** to enable Data Connect. (Make sure **Viva Insights** is selected.)

   :::image type="content" source="../images/dynamic-metric-load-step0402.png" alt-text="Screenshot that shows how to turn MGDC on or off":::

5. Select **Save**.

If you have already enabled MGDC, you will need to:

1. Follow steps 1-3 above.
1. Clear **Turn Microsoft Graph Data Connect on or off for your entire organization** to disable Data Connect.
1. Select **Save**.
1. Refresh the page.
1. Follow steps 3-5 above.

### 5. Mark a Viva Insights query for export
*Applies to: [Insights Analyst](../../advanced/setup-maint/user-roles.md)*
> [!IMPORTANT]
> Make sure you have the correct Insights Analyst role. Previous users of the legacy Workplace Analytics platform might have the "Analyst" role. To complete this process, you need the "Insights Analyst" role. Use [these steps](/azure/active-directory/privileged-identity-management/pim-how-to-add-role-to-user#assign-a-role) to enable the Insights Analyst role.

1. Open a browser and sign in to the [Advanced Insights app](https://analysis.insights.viva.office.com).
1. To run a new query, in the **Analysis** tab, select **Start analysis** on a [Power BI template](../analyst/templates/introduction-to-templates.md) or [custom query](../analyst/person-query-overview.md). (If you already have query results to export, you can skip this step.)
1. On the left navigation menu, select **Query results**.
1. Once query results are available for a new or existing query, select the Azure icon to mark for egress.

   > [!NOTE]
   > This feature is only available on queries run by the analyst that are part of the [global partition](../admin/partitions.md).

   :::image type="content" source="../images/dynamic-metric-load-step0501.png" lightbox="../images/dynamic-metric-load-step0501.png" alt-text="Screenshot that shows marking query results for Egress":::

5. Select **Export to Azure**.

### 6. Register MGDC application

*Applies to: [Microsoft Entra Application owner](/azure/active-directory/manage-apps/overview-assign-app-owners), with Insights Analyst role*

Use [these steps](/graph/app-registration#register-a-new-app) to register your app with Data Connect.

There are a few unique steps, however, that are specific to this process for dynamic loads. When filling out the registration info page, be sure to use these values:

* **Subscription** (required): Select a subscription in the tenant that will be used exclusively to filter the next four sections that relate to data destination configuration.
* **Resource group** (required): mgdc-app-resource (or select an existing resource group) 
* **Destination type**: Select **Azure Storage Account**
* **Storage Account** (required): Select the Azure Storage Account created in Step 2 
* **Storage Account Uri** (required): Select the Uri in the form: https://**[storage account name]**.dfs.core.windows.net/ (rather than the **...blob.core.windows.net/**) 
* **Application ID**: Select your App service principal from Step 1
* **Publish type**: Single-tenant

Also, when you specify the datasets that the app registration needs to query, for a dynamic Viva Insights dataset, the name should be: **VivaInsightsDataset_Report_v1_[Viva Insights query name]**.

> [!NOTE]
> If you want to edit properties or datasets associated with the app, [use these steps](/graph/app-registration#update-app-registration-entry).

### 7. Consent to application/dataset

*Applies to: Global Administrator (App approver must be different from the app developer)*

1. Open a browser and sign in to your [Microsoft 365 Admin Portal](https://admin.microsoft.com/adminportal).
1. Under **Settings**, select **Org settings**. You may have to select **Show all** to see the **Settings** option.
1. Select the **Security & privacy** tab.
1. Select **Microsoft Graph Data Connect applications**.

   :::image type="content" source="../images/dynamic-metric-load-step07.png" lightbox="../images/dynamic-metric-load-step07.png" alt-text="Screenshot that shows steps for consent":::

5. Double-click to select the app in the list, verify the dataset and column names, then select **Approve**.

   :::image type="content" source="../images/dynamic-metric-load-step0702b.png" lightbox="../images/dynamic-metric-load-step0702.png" alt-text="Screenshot that shows how to approve the dataset":::

### 8. Deploy ARM template

*Applies to: Application Administrator or Application Developer, with Insights Analyst role*

Use [these steps](/graph/data-connect-templates-overview) to generate a quick start template to set up the data pipeline. Use [these steps](/microsoft-365/enterprise/m365-dr-workload-other) to select your region.

### 9. Execute pipeline

*Applies to: Application Administrator or Application Developer*

1. Open a browser window and sign in to your [Azure portal](https://portal.azure.com). 
2. Search for “Data factories."
1. Select **mgdcdemodatafactory** (unless you named your own).
1. Select **Launch studio**.
1. Select the pencil icon on the left.
1. Under Pipelines, select **ExportO365DataEvents**.
1. Select **Debug**. 

   :::image type="content" source="../images/dynamic-metric-load-step0901.png" lightbox="../images/dynamic-metric-load-step0901.png" alt-text="Screenshot that shows how to execute pipeline":::

8. If there are any errors on the dataset, they will be specified on the bottom right under **Status**. To edit the dataset column names and data types, select the **[Dataset name]** tab at the top. Select the bracket icons on the right. Edit “name” and “type” as needed.
1. Once the pipeline is complete, data should appear in your Storage account. Select **Containers**, then **datasets** as shown below, where the container name is the Pipeline Execution ID.

   :::image type="content" source="../images/dynamic-metric-load-step0902b.png" lightbox="../images/dynamic-metric-load-step0902.png" alt-text="Screenshot that shows where data appears in your storage account":::

   > [!NOTE]
   > If the pipeline execution fails, please save the Activity run ID from the Data Factory pipeline studio, as shown below. This will help our team debug for you.

   :::image type="content" source="../images/dynamic-metric-load-step0903b.png" lightbox="../images/dynamic-metric-load-step0903.png" alt-text="Screenshot that shows the Activity run ID":::

### 10. Find the output of your extraction

*Applies to: Application Administrator or Application Developer*

If you would like to find the metadata, go to your **Azure portal**. In your Storage account, select **Containers**, then **datasets**. Then follow the following folder path:

* Output file
    * /[Pipeline Execution ID] / VivaInsights / [TenantID] / [.gzip file]
    * .gzip file contains the metric output associated with this pipeline execution

    :::image type="content" source="../images/dynamic-metric-load-step1001.png" lightbox="../images/dynamic-metric-load-step1001.png" alt-text="Screenshot that shows the output file":::

* Metadata 
    * /[Pipeline Execution ID] / VivaInsights / [TenantID] / metadata / JobMetadata / metadata.json 
    * Metadata.json contains the metadata associated with this pipeline execution

    :::image type="content" source="../images/dynamic-metric-load-step1002.png" lightbox="../images/dynamic-metric-load-step1002.png" alt-text="Screenshot that shows the metadata of the output file":::

* If you would like to update the file path, go to **Azure portal**, then **[Your Data factory]**. Select **Launch studio** then **VivaInsightsSink**, and edit the **File path**. 

  :::image type="content" source="../images/dynamic-metric-load-step1003.png" lightbox="../images/dynamic-metric-load-step1003.png" alt-text="Screenshot that shows how to update the file path":::

> [!NOTE]
> If you want to delete an app registration entry, [use these steps](/graph/app-registration#delete-an-app-registration-entry). *(Applies to Microsoft Entra Application owner with Insights Analyst role, or Global Administrator.)*
