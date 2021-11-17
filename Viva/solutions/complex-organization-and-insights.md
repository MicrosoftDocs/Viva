---

title: Complex organization and insights
description: Learn about a complex organization and its associated Viva Insights
author: v-smandalika
ms.author: v-smandalika
ms.topic: article
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: dansimp
audience: Admin
---

# What is a complex organization?

Complex organizations are Microsoft Azure Active Directory (AAD) customers who use multiple Office365 tenants. There are primarily two reasons for this type of configuration:

- [Mergers and acquisitions](#mergers-and-acquisitions)
- [Conglomerates](#conglomerates)

## Mergers and acquisitions

A business merger between two companies resulting in an organization made up with multiple Office365 tenants and separate AADs. The tenants either choose to remain separate and collaborate together or merge into a single tenant (Fo8r example, M&A: Bayer & Monsanto).

The concept of Mergers and acquisitions is depicted in the screenshot below.

:::image type="content" source="images/merger-and-acquisition.png" alt-text="mergers and acquisitions":::


## Conglomerates

A conglomerate is a corporation made up of several independent subsidiaries. The subsidiaries are tenants that have separate AAD and will collaborate together and remain separate (For example, The Walt Disney Company, Honeywell).

The concept of conglomerates is depicted in the screenshot below.

:::image type="content" source="images/conglomerate.png" alt-text="conglomerates":::

## What is the purpose of this article?

Complex organizations represent challenges for deriving insights. Often, the task falls to analyzing each of the tenants that make up the complex organization independently and comparing them manually. The process can be highly manual in nature. This article provides a growing number of examples that explain how to overcome manual processes. These examples also include those that lead to output visualizations.

## Complex organizations and Viva Insights

Microsoft Viva Insights provide information and research-based behavioral insights into:

- The tasks an organization has to execute to get work done. For example:
    - how to enhance organizational agility
    - how to boost employee engagement
    - how to improve agility
    - how to foster innovation

Advanced analytics for organizations comprised of multiple Viva Insights tenants can be enabled by:

- combining the data in a central location, and
- combining that data with other data sources.

A few starter use cases that would be enabled by this data combination strategy are:

- Identify collaboration patterns between two distinct business groups (tenants)
  :::image type="content" source="images/use case - 1.png" alt-text="Illustration of the collaboration patterns between two distinct business groups":::
- Distinguish collaboration patterns between cross business groups (tenants) VS true external interactions.
- Data combined from Viva Insights with external sources to address headcount planning, employee well-being, permanent remote work, inclusion and diversity, and so on.
  
  :::image type="content" source="images/use case - 3.png" alt-text="Data combined from Viva Insights with external sources":::

There are different ways to create a data pipeline to copy data from the source to the destination. There are also different data storage locations that can be used, such as storage accounts, SQL databases, synapse, and so on. An example leveraging Azure data factory, Viva Insights organizational data, and Azure blob storage will be described below using the [Business Continuity](../insights/Tutorials/power-bi-bc.md) use case.

## Preconditions

The following preconditions are to be fulfilled, prior to continuing with its analytical process using Microsoft Viva Insights:

### Organizational data

Organizational data is a key requirement for Viva Insights and further advanced analysis. The organizational data relates to attributes such as employee's title, manager, group, level, and so on. The data with these attributes is referred to as general required organizational data. General required organizational data is further described in [Viva Insights prepare organizational data](../insights/Use/organizational-data.md).

It is essential that only such data (with the attributes mentioned above) is uploaded into Viva Insights for analysis. Only then, the analysis output can integrate with other data sources (for example, sales data and survey data) for advanced analysis.

For an insight into advanced analysis, the following schema can be used in the file that is uploaded into Viva Insights.

|Attribute Name  |Attribute Description  |
|---------|---------|
|EffectiveDate     |      Date for which the given attribute value applies for the employee. The attribute applies until another record for the same attribute with a different effective date is specified.   |
|PersonId    | Unique identifier for the employee record. This identifier can be the employee's primary SMTP address or email alias. It must be in a simplified format that contains no spaces. For example,  the format **person.name@xyz.com** is allowed; however, the format **<Name, Person> (person.name@xyz.com)** is not allowed.     |
|ManagerId    |  Unique identifier for the employee’s manager, which is needed to correctly calculate metrics for time spent with managers and their direct reports.
This identifier can be the manager's primary SMTP address or email alias. It must be in a simplified format that contains no spaces. For example,  the format **person.name@xyz.com** is allowed; however, the format **<Name, Person> (person.name@xyz.com)** is not allowed.      |
|Organization    |    The internal organization that the employee belongs to. An employee’s organization will be specific to the individual needs and could be identified by the leader of the organization, or by another naming convention. This data is needed to correctly calculate metrics for redundancy and insularity.     |
|FunctionType  |    The job function that the employee performs. This job function is specific to the organization. This data is used to filter and group reports, and for grouping of data in [Explore the stats](../insights/Use/explore-intro.md) features.     |
|LevelDesignation    |      The employee’s level, which is represented as a string. This level is specific to the organization and can represent an employee’s experience or management level, or seniority within the organization. This data is needed to correctly calculate metrics for redundancy and insularity.   |
|Layer     |      The place where the employee is within the organizational hierarchy. Layer is represented as an integer and expressed as the distance the employee is from the top leader of the organization. For example, the CEO is at layer 0. This data is used to filter and group reports, and for grouping of data in [Explore the stats](../insights/Use/explore-intro.md) features.   |
|SupervisorIndicator     |    The attribute used to view the habits of people managers or influencers in the organization in Power BI visualizations. This attribute powers the Overview table, the Workload charts that are generated when you use a [template](../insights/Tutorials/Power-bi-templates.md) that requires this attribute.
This attribute indicates the manager status of each employee as **IC** (individual contributor), **Mngr** (manager), or **Mngr+** (manager of managers); however, if a different nomenclature is used in the file, you must update the Power BI chart filters accordingly. If you include SupervisorIndicator, you must also include the values **IC**, **Mngr**, or **Mngr+** in the organizational data. |
|TimeZone     |    Time zone in which the employee works. This attribute must be one of the time zones in [Time zones for Workplace Analytics](../insights/Use/Timezones-for-workplace-analytics.md). If no time zone is mapped to for an employee, the system will use the default time zone, which is Pacific Standard Time.     |
|TenantInd     |    Unique name for the Tenant. For example, TenantA, TenantB, TenantC, and so on.     |
|Location   |     Geographic region or other location detail.    |
|HashId    |      Unique Hashed identifier for the employee. This attribute enables further advanced analysis on the Viva Insights query results.   |

> [!NOTE]
> The schema should be the same between tenants.

The descriptions for other attributes for Viva Insights are available [here](../insights/Setup/Prepare-organizational-data.md). 


**Example:  Sample of an organizational data file**

:::image type="content" source="images/sample-organizational-data-file.png" alt-text="A sample of a file that contains organizational data":::


### Viva Insights Business Continuity dashboard

Set up the [Business Continuity](../insights/Tutorials/power-bi-bc.md) dashboard for your tenant with the following modification:

-	In the **Organizational data** section of the **Business Continuity and Hourly Collaboration** report, add **HashId** and **TenantInd** columns to the list. More columns can be added for this report if needed, for analysis. The below screenshot illustrates the report:
    :::image type="content" source="images/organizational-data.png" alt-text="Organizational data section of the Business Continuity and Hourly Collaboration report":::

### Azure

For [Adhoc with oData](#adhoc-using-odata-approach) and [Automated Data Pipeline](#automated-data-pipeline), you will need:

- An application registration
- Registered application's secret for each tenant from which you are planning to pull Viva Insights query results.

You will also need an Azure subscription to host the data from the two tenants.

1. To register an application, accomplish Steps 1 to 5 in the [Automate Exports](automate-exports.md) for each tenant.
    1. To obtain a secret for the registered application, click **Certificates & secrets** from your newly registered application in Azure Active Directory.
        1. For Key authentication, click **New client** secret and in **Add a client** secret, enter a description, select when it expires, and then click **Add**. In **Client** secrets, select the new secret value, and then click the **Copy** icon to copy the value.
    2. Make a note of the Application ID and secret that are created for each tenant.
2. In the case of Microsoft Azure subscription, perform the following steps:
    1. Deploy custom deployment from arm template.
    1. Configure the deployed resources.

The template creates the following resources: 
- Resource group
- Key vault
- Storage Account
- Azure data factory using managed identity

(The example of a privilege that allows for creation of the above resources is Azure Administrator.)

## Solution option samples

Using the case for the need to pull query data from Viva Insights from multiple tenants, there are a few sample solutions as described below:

### Adhoc manual approach

Viva Insights queries can be executed and the output can be downloaded and further analyzed offline. 
This sample will be using the **Business Continuity** report listed in the **Requirements** section. 
There are no other pipeline setup requirements. To visualize it in the sample Business Continuity PowerBi, click [here](#manual-approach-on-adhoc-basis).

:::image type="content" source="images/adhoc-manual-approach.png" alt-text="Illustration of the instance of adhoc manual approach":::

### Adhoc using oData approach

Viva Insights queries can be scheduled to auto refresh and accessed via oData links to provide further analysis or to be visualized in PowerBi reports. 
This sample will be using the **Business Continuity** report listed in the **Requirements** section.
There are no other pipeline setup requirements. To visualize it in the sample Business Continuity PowerBi, click [here](#adhoc-with-odata-approach).

:::image type="content" source="images/adhoc-using-odata-approach.png" alt-text="Illustration of the instance of adhoc using OData approach":::

### Automated data pipeline

Viva Insights queries can be scheduled to auto refresh and downloaded to a central data store location for further analysis or visualizations. The solution sample uses Azure blob storage. 
This sample will be using the **Business Continuity** report listed in the **Requirements** section.
The setup details are available [here](#data-pipeline---automated).

:::image type="content" source="images/automated-data-pipeline.png" alt-text="Illustration of the instance of automated data pipeline":::

## Solution Sample Pipeline Setup

### Data pipeline - Automated

1. Deploy the arm template for data factory creation for MultiTenant by performing the following steps:

    1. Launch the Azure portal for the subscription you want to use.
       :::image type="content" source="images/azure-portal-home-screen.png" alt-text="The Azure portal home screen":::
    1. Search for **Deploy from a custom template** in the search bar.
    1. Once **Deploy from a custom template** is displayed (under **Services** pane), click on it.
       :::image type="content" source="images/deploy-from-custom-template.png" alt-text="Deploy from a Custom Template option":::
       The screen on clicking **Deploy from a custom template** is depicted in the below screenshot.
       :::image type="content" source="images/select-template.png" alt-text="The screen on which the template is chosen":::
    1. Click **Build your own template in the editor**. The **Edit template screen appears.
       :::image type="content" source="images/build-your-own-template.png" alt-text="The Edit template screen":::
    1. Click **Load file**. 
       :::image type="content" source="images/load-file.png" alt-text="The screen displaying the Load file option":::
       The browser window is displayed, from which you can navigate to the location of the downloaded `JSON` file.
    1. Select the **DataFactory_oData_arm_template.json** file (a download location needed for this>, and click **Open**.
    1. On the resultant screen, click **Save**.
       :::image type="content" source="images/load-file-2.png" alt-text="Screen on which the file is saved to get uploaded":::
    1. Provide values for the highlighted items.
       :::image type="content" source="images/filling-selecting-highlighted-fields.png" alt-text="The screen on which the fields to be filled are highlighted":::.
       An example of filled values for the highlighted items is shown in the below screenshot.
       :::image type="content" source="images/highlighted-fields-filled.png" alt-text="The screen displaying the filled values for the highlighted fields":::
    1. Click the **Review + create** tab, and click **Create**.
       :::image type="content" source="images/review-plus-create-and-create.png" alt-text="The screen on which you can click Create":::
       :::image type="content" source="images/deployment-completion-notification.png" alt-text="The screen on which the notification message of deployment completion is displayed":::
1. Grant access to the data factory managed service identity to the key vault and the storage account by performing the following steps:
    1. Launch the resource group (**wuarmdfrg1**) by clicking its link. The screen displaying details of the resource group appears.
       > [!NOTE]
       > The resource group **wuarmdfrg1** has been defined in th4e **Custom deployment** screen; see the second screenshot under Step-9 in [Data pipeline - Automated](#data-pipeline---automated).
       :::image type="content" source="images/properties-screen.png" alt-text="The screen displaying properties data for the launched resource group":::
    1. Launch the Data factory (V2) resource by clicking its link
       > [!NOTE]
       > The Data factory (V2) resource in this instance is **wuarmdf1**.
       The screen displaying details of the **wuarmdf1** Data factory resource appears.
       :::image type="content" source="images/data-factory-launch-screen.png" alt-text="The screen containing details of the chosen data factory":::
    1. Click **Properties**. The screen displaying details of the chosen Data factory appears.
       :::image type="content" source="images/copying-managed-identity-application-id.png" alt-text="The screen on which the value of Managed Identity Application ID is displayed to copy":::
    1. Copy the value of the **Managed Identity Application ID** attribute.
    1. Navigate back to the screen of the resource group **wuarmdfrg1** by selecting **Overview**, the **Resources** tab and **wuarmdfrg1** under it.
    1. Launch the Key Vault (**wuarmdfkv1**) by clicking its link.
       :::image type="content" source="images/properties-screen.png" alt-text="The screen from which you select the keyvault":::
       The screen displaying details of the chosen keyvault appears.
       :::image type="content" source="images/key-vault-resource-screen.png" alt-text="The screen containing details of the chosen keyvault":::
    1. Click **Access policies** from the left pane.
       :::image type="content" source="images/selecting-access-policies.png" alt-text="The screen on which the Access policies are displayed to select":::
       :::image type="content" source="images/adding-access-policy.png" alt-text="The screen on which the option to add an access policy is displayed":::
    1. Click **+ Add access policy** and add your own account by setting values as described below:
    1. From the **Configure from template** drop-down list, choose **Key, Secret, & Certificate Management**.
    1. **Select principal**
    1. Search for your ID, and once it is displayed, select it. Your ID is displayed under the **Selected items** pane.
       :::image type="content" source="images/adding-access-policy-add-your-account.png" alt-text="The screen on which you can search for your ID and select it":::
    1. Click **Add**.
       :::image type="content" source="images/clicking-add-in-adding-access-policy.png" alt-text="The screen on which you can add an access policy":::
    1. Click **Save** on the top-left of the screen.
       :::image type="content" source="images/clicking-save-in-adding-access-policy.png" alt-text="The screen on which save the access policy":::
1. Grant Storage Account permissions to the Data Factory Managed Service Identity.
    1. Launch the resource group (**wuarmdfrg1**). The screen displaying details of the chosen resource group appears.
       :::image type="content" source="images/properties-screen.png" alt-text="The screen displaying properties data for the launched resource group":::
    1. Launch the storage account (**wuarmdfsa1**). The screen displaying details of the chosen storage account appears.
    1. Click **Access Control (IAM)** on the left pane.
       :::image type="content" source="images/access-control-iam.png" alt-text="The screen on which the Access control (IAM) option is displayed":::
    1. Click the **Role assignments** tab.
       :::image type="content" source="images/adding-role-assignment.png" alt-text="The screen on which the tab to add a role assignment is displayed":::
    1. Click **+ Add** and select **Add role assignment**. The **Add role assignment** screen appears.
    1. Select **Storage Blob Data Contributor**, and click **Next**.
       :::image type="content" source="images/selecting-role-assignment.png" alt-text="The role assignment screen":::
    1. Under **Assign access to**, choose the **Managed identity** radio button.
       :::image type="content" source="images/choosing-managed-identity.png" alt-text="The screen on which the Managed identity radio button is chosen":::
    1. Click **+ Select members** tab. The **Select managed identities** screen appears.
       :::image type="content" source="images/select-members.png" alt-text="The Select managed identities screen":::
    1. From the **Managed identity** drop-down list, choose **Data factory (V2)**.
       :::image type="content" source="images/choosing-data-factory-v2-value.png" alt-text="The screen on which you choose the Data factory parameter":::
    1. Search for the Data factory name (**wuarmdf1**) from the **Select** field.
       > [!NOTE]
       > The Data factory **wuarmdf1** has been defined in th4e **Custom deployment** screen; see the second screenshot under Step-9 in [Data pipeline - Automated](#data-pipeline---automated).
       :::image type="content" source="images/selecting-factory-name.png" alt-text="The screen on which you select the Data factory value":::
    1. Click **Select**. The **Add role assignment** screen appears.
    1. Click **Review + assign**.
       :::image type="content" source="images/review-plus-assign-on-add-role-assignment-screen.png" alt-text="Add role assignment screen that displays the Review + assign option":::
    1. Refresh the browser to view the **Role assignments** screen again, in which you can view the Data factory application you have just added.
       :::image type="content" source="images/role-reflection-screen.png" alt-text="The screen that displays the Data factory application":::
1. Create a file named **odatasources.txt**.
    1. Create a `.txt` file with the below comma-delimited schema for each oData source and the tenant reference information that will be stored in keyvault.

    |Column name  |Description  |
    |---------|---------|
    |odataurl    |   oData URL from viva insights query      |
    |tenantid     |   Name of the secret in the Keyvault for the TenantID (aka omstenantid, aad tenantid)      |
    |aadresource       |  The aadresource for the oData       |
    |servicePrincipal     |  Name of the secret in the Keyvault for the application ID that will be used to access the oData URL      |
    |secretName     |  Name of the secret in Keyvault for the secret for the application ID that will be used to access the oData URL       |
    |path     | oData path of the oData URL        |
    |fileName    |    Pre-fix name of the file     |

    > [!NOTE]
    > The content in the `.txt` file will be a comma-delimited one. This content is built using the schema in the above table. This schema-based content is created for each oData source.

1. Upload the **odatasources.txt** file to the storage account in the wpaexports container by performing the below steps:
    1. Launch the storage account (**wuarmdfsa1**).
       :::image type="content" source="images/storage-account-screen-while-uploading-odata-file.png" alt-text="The storage account screen at the stage of oData file upload":::
    1. Click **Containers** on the left pane.
       :::image type="content" source="images/containers-screen.png" alt-text="The screen on which you can click the Containers option":::
    1. Click **wpaexports**. The screen displaying details/options in **wpaexports** is displayed.
       :::image type="content" source="images/containers-wpaexports.png" alt-text="The screen displaying the Upload option":::
    1. Click **Upload**. The screen displaying the uploaded file appears.
       :::image type="content" source="images/containers-wpaexports-upload.png" alt-text="THe screen displaying the odatasources.txt file":::
1. Generate the secrets in Key Vault by performing the following steps:
    1. Launch the Key Vault (**wuarmdfkv1)**.
       :::image type="content" source="images/properties-screen.png" alt-text="The screen from which you select the keyvault":::
    1. Click **Secrets** on the left pane, and click **+ Generate/Import**.
       :::image type="content" source="images/secrets-generate-import.png" alt-text="The Secrets screen on which the Generate/Import option is available":::
    1. Create the secrets using the names in the below table.
       > [!NOTE]
       > The two examples below the table describe the process of creating a secret.
 
    |Secret Name (based on the examples Tenant 1 and Tenant 2)  |Value description  |
    |---------|---------|
    |tenantid1     |    AAD TenantId for Tenant 1. Example: bd382938-yyyy-yyyy-yyyy-yyyyyyyyyyyy     |
    |servicePrincipal1     |    Service Principal for tenant 1. Example: lld32e908-yyyy-yyyy-yyyy-yyyyyyyyyyyy     |
    |MTWpaSecret1     |  Credential for servicePrincipal1 for tenant 1. Example: dsfUELk23r7912!#       |
    |tenantid2     |     AAD TenantId for tenant 2. Example: bd382938-xxxx-xxxx-xxxx-xxxxxxxxxxxx    |
    |servicePrincipal2     |   Service Principal for tenant 2. Example: hh2bd38d-xxxx-xxxx-xxxx-xxxxxxxxxxxx      |
    |SPSecret2     |    Credential for servicePrincipal2 for tenant 2. Example: bjdIOLUE.j23iu2!#     |

    **Example 1**: This example provides a sample oData URL for each of the tenants, namely Tenant 1 and Tenant 2, in which the names of the secrets to be created are present.

    **Tenant 1**: In this example, the **tenantid1**, **servicePrincipal1**, and **MTWpaSecret1** values are the secrets to be created in the keyvault.

    https://workplaceanalytics.office.com/2de6681a-42d5-46fa-a858-2660f5743815/scopes/e0d8d313-6075-4c25-b714-98843532ae61/jobsodata/a6ca4178-f30b-4c7a-8c8e-38f53fe1d2d0/GroupToGroup,tenantid1,https://workplaceanalytics.office.com,servicePrincipal1,MTWpaSecret1,GroupToGroup,GroupToGroup

    **Tenant 2**: In this example, the values **tenantid2**, **servicePrincipal2**, and **SPSecret2** are the secrets to be created in the keyvault.

    https://workplaceanalytics.office.com/10c5ca3c-a4d2-424d-8af3-f0efd6c79c99/scopes/217c5147-e12b-448c-9672-25b79a9ec0f0/jobsodata/ae3270dc-ba5a-4c40-b6b9-81fd9b5a4eac/GroupToGroup,tenantid2,https://workplaceanalytics.office.com,servicePrincipal2,SPSecret2,GroupToGroup,WpAAIGroupToGroup

    **Example 2**: This example describes (in a pictorial form) the step involved in creating a secret, using the **tenantid1** value from the **Tenant 1** example.

**Creating a secret**

:::image type="content" source="images/create-secret-example-1.png" alt-text="The screen on which the name for a secret is defined":::

**Created secret (above) in the key vault**

:::image type="content" source="images/create-secret-using-example-in-screenshot.png" alt-text="The screen displaying the created secret in the keyvault":::

A newly created secret is used by an Odata URL that is mapped to a specific tenant. For more information, see [Organizational data file](#organizational-data-file).

#### Organizational data file
An organizational data file contains information about a company and its employees. An example of this file is one named `odatasources.txt`. It is uploaded into Viva Insights. It contains details of two tenants, who are each assigned two sets of oData URLs they govern. Each oData URL for a tenant uses the keyvault secret created specifically for that tenant.

A sample organizational data file is depicted in the below screenshot.

:::image type="content" source="images/example-file-contents.png" alt-text="The content of the sample organizational data file":::

#### To set trigger for pipeline

A trigger can be created in the Azure data factory to execute the pipeline on a schedule. This schedule is dependent on the needs and the report granularity. For the Business Continuity, it is at a week grain. The minimum timeframe would be on a weekly basis, for example, every Tuesday.

Creation of a trigger for a pipeline is depicted in the below screenshot.

:::image type="content" source="images/example-trigger-for-pipeline.png" alt-text="The screen on which a trigger for a pipeline can be created":::

#### To execute the pipeline manually

1. Launch the data factory created earlier, and click **Open the Azure Data Factory Studio**.
> [!NOTE]
> Data factory is the one created during deployment of arm template for data factory creation for MultiTenant.

:::image type="content" source="images/launching-azure-data-factory-studio.png" alt-text="The screen that displays option to launch Azure Data factory studio":::

1. Click **Author** on the left pane.
1. Expand the **Pipeline** pane and select **CopyPipeline_MTBCDPipeline**.
   :::image type="content" source="images/selecting-CopyPipeline-MTBCDPipeline.png" alt-text="The screen on which the resource is selected":::
1. Click **Debug**. The below screenshot illustrates a successful execution of a debug operation.
   :::image type="content" source="images/debug-successful-execution.png" alt-text="The screen on which a debug operation is successfully executed":::
   
   The output is available to view in the storage account in **wpaexports > rawdata1**.
   :::image type="content" source="images/rawdata1-folder-to-select.png" alt-text="The screen displaying the **rawdata1** folder in which the output is available":::

## Visualize with PowerBi

Visualization with PowerBi can be implemented in the following methods:

- [Manual approach on adhoc basis](#manual-approach-on-adhoc-basis)
- [Adhoc with oData approach](#adhoc-with-odata-approach)

### Manual approach on adhoc basis

#### Requirements

The following requirements are to be fulfilled prior to viewing the dashboard that contains data downloaded from the two tenants.

- Execution of Business Continuity Queries on the two tenants
- Download of the results in CSV format in a local location and decompressed of the results into unique names.
- Installation of the latest version of PowerBi Desktop.
    -  If you have an earlier version of PowerBi installed, uninstall it before installing the new version. Go to [Get Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t) to download and install the latest version.
 
#### Information gathering

Information needed for this PowerBi are the .csv files downloaded from the Business Continuity Dashboard reports. The reports are what is executed as part of the Business Continuity setup in [Viva Insights business continuity dashboard](#viva-insights-business-continuity-dashboard).

1. Click **Query designer** on the left pane, and click the **Results** tab.
   :::image type="content" source="images/query-designer-results-tab.png" alt-text="The Query designer screen":::

1. Click the **Download** icon corresponding to each of query.
   :::image type="content" source="images/query-data-download.png" alt-text="The screen from which data can be downloaded":::

#### Launch PowerBi template

1. Launch the PowerBi report provided by a Viva Solutions team member (a download location needed for this)
   :::image type="content" source="images/MultiTenant-BCD-LocalStore-Example.png" alt-text="The screen containing the report to launch":::
   << MultiTenant_BCD_LocalStore_Example.pbit>>

   > [!NOTE]
   > Hover over the **Information** icon for further details on the parameter requirement.
  :::image type="content" source="images/hover-over-information-icon.png" alt-text="The screen on which you can hover over the Information icon":::

2. Update the **Parameters** request with the links copied from each tenant, as shown in the below screenshot.
   :::image type="content" source="images/updating-parameters-request.png" alt-text="The screen on which parameters are updated":::
3. Click **Load**.

> [!NOTE]
> Once the PowerBi report has refreshed successfully, you can view the results from your dataset by changing filters and navigating to the report.

### Adhoc with oData approach

#### Conditions

The following conditions are to be complied with prior to visualizing the dashboard with the oData links from 2 tenants:

- Execution of Business Continuity Queries on the two tenants, and availability of the [links to query results](#gathering-of-information)
- Maintenance of an organizational account for each tenant
- Installation of the latest version of Power BI Desktop
    - If you have an earlier version of PowerBi installed, uninstall it before installing the new version. Go to [Get Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t) to download and install the latest version.

#### Gathering of information

Information needed for this PowerBi will be the **Get results** links for the Business Continuity Dashboard reports. The reports are what is executed as part of the Business Continuity setup in [Viva Insights business continuity dashboard](#viva-insights-business-continuity-dashboard).

1. Click **Query designer** on the left pane, and click the **Results** tab.
   :::image type="content" source="images/query-designer-results-tab.png" alt-text="The Query designer screen":::
1. Click the **Link** icon corresponding to each of query.
1. Click **Copy** to copy the generated oData URL link.
   :::image type="content" source="images/copy-odata-url-link.png" alt-text="The screen on which you can copy the link of the oData URL":::

#### Launch template of PowerBi

1. Launch the PowerBi report provided by Viva Solutions team member (a download location needed for this).
   << MultiTenant_BCD_oData_Example.pbit>>
   :::image type="content" source="images/MultiTenant-BCD-oData-Example.png" alt-text="The screen displaying a report to launch":::

   > [!NOTE]
   > Hover over the **Information** icon for further details on the parameter requirement.
  :::image type="content" source="images/MultiTenant-BCD-oData-Example-information.png" alt-text="The screen displaying the Hover-over option":::

2. Update the **Parameters** request with the links copied from each tenant, as shown in the below screenshot.
   :::image type="content" source="images/MultiTenant-BCD-oData-Example-links-copied.png" alt-text="The screen on which parameters values are updated":::
3. Click **Load**.
4. If prompted for privacy levels, select **Organizational**.
   :::image type="content" source="images/selecting-organizational-as-privacy-level.png" alt-text="The screen on which values for privacy levels are chosen":::
5. When prompted with the sign-in page, select **Organizational account** on the left pane.
6. From the **Select which level to apply these settings to** drop-down list, choose the tenant-level link.
   
7. Click **Sign in** and click **User other account**.
   :::image type="content" source="images/use-another-account-option.png" alt-text="The screen from which you can choose to sign in as another user":::

   The **OData feed** screen post-signing in as another user is depicted in the below screenshot.
   :::image type="content" source="images/post-sign-in-odata-feed.png" alt-text="The OData feed screen after signing in as a different user":::
8. Repeat the sign-in step for each tenant's oData connection.
9. Click **Connect**.

   > [!NOTE]
   > Once the PowerBi report has refreshed successfully, you can view the results from your dataset by changing filters and navigating to the report.

### Automated pipeline approach

#### Prerequisites
The following prerequisites are to be fulfilled prior to visualizing the dashboard with the outputs of the Azure storage.

- Completion of setup and execution of data factory
- Creation of [access to the Azure storage](#information-gathering-process) during the setup, using the Azure portal. The following information will be gathered from it:
    - Account access key (obtained from the one created during the setup)
    - Storage account container URL for the wpaexports container created during the setup
    - Names of the files created in the storage account (in the path **wpaexports > rawdata1 location**)
- Installation of the latest version of Power BI Desktop
    - If you have an earlier version of PowerBi installed, uninstall it before installing the new version. Go to [Get Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t) to download and install the latest version.

#### Information gathering process

Obtain the storage account information by performing the following steps:

1. Launch the [Azure portal](https://ms.portal.azure.com/#home) for the subscription that you will use.
1. Search for the storage accounts in the search bar. The **Storage accounts** option is listed under the **Services** pane.
   :::image type="content" source="images/searching-for-storage-accounts.png" alt-text="The screen on which you search for and view storage accounts":::
1. Click **Storage accounts** and filter for the storage account (**wuarmdfsa1**).
   :::image type="content" source="images/filtering-for-storage-account.png" alt-text="The screen on which you filter for a specific storage account to select it":::
1. Click the link of the storage account. The screen containing the details of the chosen storage account appears.
1. Click **+ Container**.

   :::image type="content" source="images/containers-screen.png" alt-text="The Containers screen regarding a specific storage account":::

1. Click **...** and select the **Container properties**. The screen displaying the data of properties of the container appears.
   :::image type="content" source="images/selecting-container-properties.png" alt-text="The screen displaying properties data for the container":::
1. Make a note of the value in the **URL** text box. This is the **StorageContainerURL** that will be used during the PowerBi parameter prompt.

1. Click **Overview** on the left pane, and click on the **rawdata1** folder.
   :::image type="content" source="images/rawdata1-folder-to-select.png" alt-text="The screen displaying the rawdata1 folder to select":::
1. Copy the names of the four listed files.
    1. Prepend **rawdata1/** to the names you have copied, for example, rawdata1/PD4_Business Continuity_ZID.csv.  The combined name will be the name of the files which will be used during the PowerBi parameter prompt.
1. Click **Access keys** on the left pane.
    1. Select **Show keys**.
       :::image type="content" source="images/selecting-show-keys.png" alt-text="The screen on which you select Show keys":::
    1. Copy the value of one of the listed keys. This is the value that will be used during the PowerBi parameter prompt.

#### Launch the  template of PowerBi

1. Launch the PowerBi report provided by Viva Solutions team member (a download location needed for this).

   << MultiTenant_BCD_StorageAccount_Example.pbit>>
   :::image type="content" source="images/MultiTenant-BCD-StorageAccount-Example.png" alt-text="The screen displaying the PowerBi report":::
   > [!NOTE]
   > Hover over the **Information** icon for further details on the parameter requirement.
  :::image type="content" source="images/MultiTenant-BCD-StorageAccount-Example-information.png" alt-text="The screen displaying the option to hover over Information icon":::

2. Update the **Parameters** request.  Based on the previous example, **PubD** and **PD4** are the values for **Tenant 1** and **Tenant 2**, respectively; the **StorageContainerURL** is what was recorded earlier (in a step in [Information gathering process](#information-gathering-process)).
   :::image type="content" source="images/MultiTenant-BCD-Example-filled-values.png" alt-text="Filled values for a PowerBi report":::
1. Click **Load**.
1. Enter the storage key when prompted.
   :::image type="content" source="images/entering-storage-key.png" alt-text="The screen on which storage key is entered":::
1. Click **Connect**.

> [!NOTE]
> Once the PowerBi report has refreshed successfully, you can view the results from your dataset by changing filters and navigating to the report.

**Example 1**

To obtain an insight the look of the report by a tenant, perform the following steps:

1. On the **Settings** screen, from the **Select an organizational attribute to view the report by**  drop-down list, choose the Tenant identifier attribute.
   :::image type="content" source="images/selecting-tenant-identifier-pages.png" alt-text="The screen on which you select tenant attributes":::
2. Select one of the PowerBi report pages.
   The below screenshot depicts one of the selected pages.
   :::image type="content" source="images/selecting-powerbi-report-pages.png" alt-text="The screen from which PowerBi reports are selected":::

You can go with any number of settings combinations for different perspectives on the insights.

**Example 2**

To view the Tenant 1 organization insights, perform the following steps:

1. On the **Settings** screen, from the **Select an organizational attribute to view the report by** drop-down list, choose **Organization**.
1.  Under the **To filter employees, select the organizational attribute and values you would like to filter by** pane, from the **Organizational Attribute** drop-down list, choose **TenantInd**.
    1. From the **Select filter values** drop-down list, choose one of the tenants.
       :::image type="content" source="images/settings-to-view-tenant-1-insights.png" alt-text="The screen on which value of a tenant is selected as a filter criteria":::
1. Select one of the report pages.
   :::image type="content" source="images/settings-to-view-tenant-1-insights-selecting-report-pages.png" alt-text="The screen displaying pages of a chosen report":::



 




























