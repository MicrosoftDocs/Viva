---

ROBOTS: NOINDEX,NOFOLLOW
title: Deploy and configure Workplace Analytics Azure Templates 
description: Learn how to deploy and configure Workplace Analytics Azure Templates
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---
# Deploy and configure Workplace Analytics Azure Templates

_These templates are only available as part of a Microsoft service engagement._

Before you can use Workplace Analytics Azure Templates for advanced data analysis, you need to do the following:

1. [Review the security considerations](#security-considerations)
2. [Confirm the prerequisites](#prerequisites)
3. [Choose an app registration path](#choose-a-registration-path):

   * [Register the apps during deployment](#deployment)
   * [Register the apps in Azure AD before deployment](#register-and-configure-the-apps-in-azure-ad)

4. [Deploy the templates](#deployment)
5. [Configure the registered apps in Azure AD](#to-configure-the-registered-apps) - Only do this if you chose to register the apps in Azure AD before deployment.
6. [Generate SAS URI for data export](#generate-sas-uri-for-data-export)
7. [Add users](#add-users-and-assign-roles)
8. [Process the data](#process-the-data)
9. Additional configuration and deployment options: [Incoming data](#incoming-data), [Other configuration options](#other-configuration-options), and [Audit logs](#audit-logs)

## Security considerations

Before deploying and configuring these templates, review the following security principles.

* Data is stored in your Azure subscription.
* Data is encrypted on disk and all access to and communication between Azure Resources and these templates are enabled and secured with the Secure Sockets Layer (SSL) certification.
* Authentication leverages Azure Active Directory.
* Authorization is set at the Azure Databricks and Azure Templates level by the Azure administrator who installs and sets up the Workplace Analytics Azure Templates.
* An Azure Template Configuration log is created during installation.

## Prerequisites

Before deploying Workplace Analytics Azure Templates, confirm or complete the following:

1. Confirm that [Workplace Analytics is set up](../setup/set-up-workplace-analytics.md) and ready to use.
2. Enable [Workplace Analytics data export](../data-access/data-access.md) for the Azure tenant.
3. Do the following for the Azure subscription that will host these templates and the data exported from Workplace Analytics:

   * Confirm you have either an **Azure Admin** or an **Azure Contributor** role to deploy these templates.
   * Get [applicable Azure AD permissions](https://docs.microsoft.com/azure/active-directory/develop/active-directory-how-applications-are-added) for yourself (or the admin doing the deployment) from your Office 365 global administrator.
   * If the Workplace Analytics team is deploying the templates, confirm that the vendor accounts are set up for the team and that the Technical Operations engineer also has the applicable Azure AD permissions to install and set up the templates.

## Choose a registration path

These templates require an Azure Active Directory (AD) application registration for the Web App service UI, the Web App service API, the Azure Analysis service, and the Azure key vault.

You can register these apps in one of the following ways:

* [Register the apps in Step 10 during deployment](#deployment) - You can also automatically register the apps during deployment through the Microsoft AppSource solution template deployment site.
* [Register and configure the apps in Azure AD](#register-and-configure-the-apps-in-azure-ad) - Alternatively, you can register the required apps in Azure AD before deployment, which enables the Microsoft identify platform to provide authentication and authorization. After registering, you must [deploy the templates](#deployment) through the template deployment site. After deployment, come back to Azure AD and [configure the registered apps](#to-configure-the-registered-apps). You can then proceed with the steps to [generate the SAS URI for data export](#generate-sas-uri-for-data-export), [add users](#add-users-and-assign-roles), and [process the data](#process-the-data).

## Register and configure the apps in Azure AD

You can register the required apps in the Azure portal to get the Microsoft identify platform to authenticate and authorize them, which is required for deployment.

Registering the apps before deployment enables Azure Active Directory (Azure AD) to provide [authentication](https://docs.microsoft.com/azure/active-directory/authentication/overview-authentication).

See [Register an application with the Microsoft identity platform](https://docs.microsoft.com/graph/auth-register-app-v2) and [Register an app in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) for details.

### To register the apps and create client secrets

1. Sign in to the Azure portal with an account that has permissions to register Azure AD applications, such as an [**Azure Application developer account**](https://docs.microsoft.com/azure/active-directory/roles/custom-create#create-a-new-custom-role-to-grant-access-to-manage-app-registrations).
2. In Azure Active Directory, under **Manage**, select **App registrations**, and then select **New registration**.
3. Enter a name for the **Web App service UI** with a consistent naming convention, such as: **wpaapps + YYYYMM + role** = **App registration name**. For example: **wpaapps202011-ui**.
4. In **Supported account types**, select **Accounts in this organizational directory only** for a single tenant, and then select **Register**.
5. Select **Certificates & secrets**, and then in **Client secrets**, select **New client secret**, type a description, select when it expires, and then select **Add** to create a secret for the app service.
6. Copy and save this new **secret** to use during deployment.
7. Select **New registration** again for the **Web App service API** and enter a name for it, such as: **wpaapps202011-api**.
8. In **Supported account types**, select **Accounts in this organizational directory only** for a single tenant, and then select **Register**.
9. In **Supported account types**, select **Accounts in this organizational directory only** for a single tenant, and then select **Register**.
10. Copy and save the **Application (client) ID** for both the app service and app API service.
11. Select **Certificates & secrets**, and then in **Client secrets**, select **New client secret**, type a description, select when it expires, and then select **Add** to create a secret for the API service.
12. Copy and save this new **secret** to use during deployment.
13. Complete the [deployment steps](#deployment) and in **Step 10**, select **Authentication** and update the **Redirect URI** for each app with the Application (client) ID and secret you saved in the previous steps.

### To configure the registered apps

1. After completing the [deployment steps for the templates](#deployment), sign in to the Azure portal with an account that has permissions, and then open Azure Active Directory.
2. Select the **Web App service API** > **API permissions**, and confirm the **Microsoft Graph** > **User.Read** > **Delegated** default is listed.
3. Select **Expose an API**, and then select **Save and continue** to grant delegated permission.
4. In **Add a scope** > **Scope name**, enter **user_impersonation**.
5. In **Admin consent display name**, enter **user_impersonation** again.
6. In the descriptions, enter something like: **Allows access to the wpa app API**.
7. Confirm **Enabled** is selected, and then select **Add scope**.
8. Select **Authentication** > **Add a platform** > **Web**, and then enter the [**Redirect URI**](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-redirect-uri) for the **Web App service API**. The format will be similar to this:

     `https://wpaapps202011-api.azurewebsites.net/.auth/login/aad/callback`

9. Select the **Web App service UI** > **API permissions**, confirm the **Microsoft Graph** > **User.Read** > **Delegated** default is listed, as shown in the graphic.

    ![Azure AD API permissions](./images/aad-permissions.png)

10. Select **Add a permission** > **APIs my organization uses**, and then search for and select the **Web App service API** (for example: wpaapps202011-api).
11. Select **Delegated permissions**, select **user_impersonation**, and then select **Add permissions**.
12. Select **Authentication** > **Add a platform** > **Web**, and then enter the [**Redirect URI**](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-redirect-uri) for the **Web App service UI**. The format will be similar to this:

     `https://wpaapps202011.azurewebsites.net/`

13. In **Implicit grant**, select both **Access tokens** and **ID tokens**, and then select **Configure**.
14. Select API permissions, and then select **user_impersonation**, and then select **Grant admin consent for Microsoft** to enable API consent.
15. Then proceed with the steps to [generate the SAS URI for data export](#generate-sas-uri-for-data-export).

## Deployment

1. Get and open the Azure deployment link for the Workplace Analytics Azure Templates from the Workplace Analytics team.
2. On the **Getting Started** page, select **Next**.
3. When prompted, select the applicable Azure subscription.
4. For **Resource group**, you can select to:

   * **Create new** to create a new resource group.
   * **Use existing** to use an existing resource group and append the existing group with what's needed for this template, including any updates for any of the other templates in this group.

5. Select the applicable **Region** and then select **Next**.
6. On the **Choose SKU** page, select the SKU or Pricing Tier for one or more of the Azure Components that you'll use with the templates. You should've gotten these SKU recommendations with the deployment URL or during your team deployment meeting.
7. On the **Deployment Review** page, confirm the selections, and then select **Next**.
8. After the Azure Databricks workspace deployment is done, you are automatically signed in to Azure Databricks. If you're not, you need to sign in manually.
9. On the **Databricks Token** page, you need to [generate the Azure Databricks Token](https://docs.azuredatabricks.net/api/latest/authentication.html#generate-a-token) for the App source and then select **Next**.
10. In **Deployment Review**, do the following:

    * If you registered the apps before deployment, select **Authentication** and update the **Redirect URI** for each of the apps listed.
    * Otherwise the apps are registered automatically during this step. Review the information for the following supported Azure components that the templates might use. For example, confirm the Databricks cluster is assigned. If it's empty, no resources will be deployed for it.

      * [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis)
      * [Azure Resource Group](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-overview#resource-groups)
      * [Azure Blob storage account](https://docs.microsoft.com/azure/storage/blobs/storage-blobs-introduction)
      * [Azure Databricks](https://docs.microsoft.com/azure/azure-databricks/)
      * [Azure SQL database](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits-single-databases)
      * [Azure Analysis Services](https://docs.microsoft.com/azure/analysis-services/)
      * [Azure Web Apps (App Service)](https://docs.microsoft.com/azure/app-service/)
      * [Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-use-from-web-application)

11. Select **Next** to start the two-phase deployment, which can take up to 60 minutes to complete.
12. After the deployment is complete, open, copy, and save the deployed website link for the templates, similar to the one shown in the following graphic.

    >[!Important]
    >You must save this deployment link because you and the other users you add need the link to configure and use the templates.

    ![Azure Templates deployment](./images/deployed-website-link.png)

13. If you registered the apps before deployment, go back and [configure the registered apps in Azure AD](#to-configure-the-registered-apps). Otherwise, proceed to the next steps to [generate the SAS URI for data export](#generate-sas-uri-for-data-export).

## Generate SAS URI for data export

After deployment, you need to create a write-only SAS URI on the raw data container in the storage account created during the deployment. The SAS URI is given to the Workplace Analytics admin to configure the weekly automated data access feed that is required to drive a few of the Azure Templates.

1. Use Storage Explorer (or Storage Explorer (preview) web) application to view the raw data container in the storage account created during deployment.
2. Right-click the **rawdata** folder and select **Get Shared Access Signature**.
3. In **Shared Access Signature**, select an expiration time.
4. In **Permissions**, confirm only **Write** is selected, and then select **Create**.
5. For the URI, select **Copy** to copy the complete URI, which will be similar to the example URI in the following graphic.
6. Give the new URI that you copied in the previous step to your Workplace Analytics admin, who needs it to configure [automatic data exports](../data-access/data-access.md#to-export-data-from-workplace-analytics).

    ![Example SAS URI](./images/example-sas-uri.png)

## Add users and assign roles

As the Azure Templates Admin, you can use the Admin page to manage security, privacy settings, and other administrative processes. Before other people can use the templates, you need to add them as users and assign them one of the following roles based on the tasks they need to accomplish with the templates:

* **Azure Templates Admin**

  * Can add other users and assign roles for the templates.
  * Can share the templates website link with other users.
  * Can share the link to access the [Azure Databricks Workspace](https://docs.azuredatabricks.net/user-guide/workspace.html) with assigned Data scientists.
  * Configure specific template settings on the [Configuration](#other-configuration-options) page.
  * Access and [audit logs](#audit-logs).

* **Analyst**

  * Can access, use, and customize the analytical templates available through a Workplace Analytics Azure Templates website link.
  * Can access, use, and customize the Power BI reports and dashboards connected to the Workplace Analytics Azure Templates.

* **API User**

  * Can access and use a limited set of templates available through a Workplace Analytics Azure Templates website link.
  * Assign to allow automated processes access to data from specific scenarios.

* **Data Owner**

  * Can access, use, and customize the same analytical templates and Power BI reports and dashboards as an Analyst.
  * Owns and can access and use incoming data to create datasets.
  * Can share access to data they own with other users.
  * For the [Join Datasets Azure Template](./join-datasets.md), can share access to their joined datasets with other template users.

* **Data Scientist (beta)**

  * Can access, use, and customize the same analytical templates and Power BI reports and dashboards as an Analyst.
  * Can also access the Azure Databricks Workspace and use Python or R scripts to derive new insights.

**To add users and assign them roles:**

1. Use the website link (from the last step in Deployment) to open the Workplace Analytics Azure Templates.
2. Select **Admin** > **User Management** > **Add New User**.
3. Type the email address for the new user and select the applicable role for this user, as shown in the following graphic.

    ![Add Workplace Analytics users](./images/add-user.png)

4. In **Scenarios**, select the applicable templates for which the user needs access. Users can only access and use templates that are selected from this list.

## Process the data

After adding users, you need to process the Workplace Analytics data that you want to use with these templates:

1. In Azure Resource groups, locate the folder that the deployment just created. The new resource group name begins with **wpaappsrg** and includes the deployment date and time, as shown in the following graphic.
  
    ![Workplace Analytics Resource group](./images/resource-group-a.png)

    The new storage group contains a **rawdata** folder, as shown in the following graphic.

    ![Workplace Analytics rawdata folder](./images/rawdata-folder.png)

2. Confirm that the following .csv files are in the new **rawdata** folder:

   * **MailParticipants.csv**
   * **Mails.csv, MeetingParticipants.csv**
   * **Meetings.csv**
   * **PersonalHistorical.csv**

   If these .csv files are not already in the **rawdata** folder, you need to use the Azure Storage Explorer (or other comparable tool) to connect to the Azure storage group that currently stores your Workplace Analytics data set, and select and copy these files into that folder.

3. In the Workplace Analytics Azure Templates app, select **Admin** > **Scenario Execution**, select the **rawdata** folder, and then select **Process data**.

   ![Process Rawdata in Workplace Analytics](./images/rawdata-folder-n.png)

## Incoming data

On the **Admin** > **Incoming Data** page, you can see a list of the most recent data uploads in descending order, including the data's path, the date it was uploaded, the status, and the option to delete it. This list populates the list you can use to create new datasets with the Process Explorer Azure template. Also, use this page to easily delete data (trash can icon in far right column) that's outdated or no longer needed.

## Other configuration options

As an admin, you can configure template settings in **Admin** > **Configuration**, including:

* The minimum group size, maximum number of nodes and links in data analysis with the **Organizational Network Analysis Azure Template**.
* If the **Process Explorer Azure Template** either surfaces and uses, or does not surface or use, email subjects in blob storage datasets to help train the model for categorization.
* Set the number of days to retain data created and saved as joined datasets with the **Join Datasets Template**.

## Audit logs

As an admin, you can audit user activity in **Admin** > **Logs**. Select the **information** (i) icon in the **Message** column to see more details about a specific  activity.

## Related topics

* [Workplace Analytics Azure Templates overview](./overview.md)
* [What's new in Workplace Analytics Azure Templates](./release-notes.md)
* [Azure Templates support](support.md)
