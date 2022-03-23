---

ROBOTS: NOINDEX,NOFOLLOW
title: Upgrade Workplace Analytics Azure Templates to use Synapse Analytics
description: Learn how to upgrade your current Azure Templates to use Azure Synapse Analytics instead of Databricks
author: madehmer
ms.author: v-lilyolason
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
# Upgrade to Synapse Analytics

_These templates are only available as part of a Microsoft service engagement._

>[!Important]
>As of February 2022, this product is no longer being supported.

Your current Azure Templates have been using Workplace Analytics data that's been exported and running on Azure Databricks for computations. To improve usability and reduce costs, you can upgrade from Databricks to Azure Synapse Analytics.

## Prerequisites

* **Azure admin** - Must be an admin of the Azure subscription or you cannot complete the upgrade.
* **SAS token for file download** - You should've received an email from Microsoft with the SAS token for this upgrade. If you did not receive an email with it, ask your Microsoft representative for it.
* **App Registrations access** - Confirm you can access the Azure Active Directory “App Registrations” in the Azure portal for your current Azure Templates installation for both the “UI” and the “API," including the IDs for the services being upgraded.
* **Azure Active Directory Service access** - Confirm you have access in the Azure portal, including the Tenant ID.
* **Resource Groups access** - Confirm you access in the Azure portal, including the names and Subscription IDs.
* **Azure Template service names** - Confirm you have the names of the current Azure Template services in the Azure portal, including the storage account, UI or UX app service, API app service, and the key vault names.
* **Key vault secrets access** – Confirm you can view and modify the Key vault secrets because the scripts must be able to modify some of the key vault secrets. If you don’t have access, the scripts will fail with permission errors.

## Launch Azure CloudShell

Login to the Azure Portal, and launch Azure CloudShell by clicking the link in the top navigation bar shown below

>[!Note]
>If this is your first time running Azure CloudShell, you will need to select the subscription storage before you are allowed to use CloudShell.

## Download Install scripts

1. To format the File Download SAS URL, open Notepad in Windows and copy and paste the following code:

$sasUri = "https://wpaappsprodtest1.blob.core.windows.net/tmpexternal/AztScripts_20211011.zip"

You will need to paste the SAS Token provided in part 1 after the word zip, and before the closing quotation.  For example:

$sasUri = “https://wpaappsprodtest1.blob.core.windows.net/tmpexternal/AztScripts_20211011.zip?sv=2020-08-04&ss=bfqt&srt=o&sp=rwdlacupitfx&se=2022-02-22T04:16:23Z&st=2022-02-14T20:16:23Z&spr=https&sig=K6fCajAhRpHPm%2FlTdrTdFc0fXfYHLNDKF4zvbBXYAOE%3D%22”

1. Set SAS URL in Cloud Shell
Simply paste the full command with URL and SAS Token from Notepad in the last step and paste in Cloud Shell command line and press enter.
Download the Scripts ZIP using CloudShell
Run command:
Invoke-WebRequest -Uri $sasuri -outfile ./aztScriptsCloudShell.zip
Note: If successful then no output will display. If there are errors, they will write out to console.
Unzip Scripts Archive
Run command:
Expand-Archive -LiteralPath ./aztScriptsCloudShell.zip -DestinationPath ./ -Force
Check All Folders are in place
Run command dir to list directories in the current folder, and you should see the directory AztScripts_20211011 listed if all command executed successfully:
 

Setup and Fill Out Params File
Copy Template File to Create Params File
Run the following command:
Copy-Item ./AztScripts_20211011/template-all-param.txt ./AztScripts_20211011/azt-param.txt
 This will make a copy of the file template-all-param.txt from the files you just downloaded and rename it to azt-param.txt so that you can edit that one for script usage.
Launch the Editor App to Open azt-params.txt
Click on the bracket’s icon in the Cloud Shell top bar to launch the editor app:
 
This will open a director/file list on the left-hand side of the screen, and you will need to expand the AztScripts_20211011 folder to see the files inside.  Scroll down toward the bottom of the files in AztScripts_20211011 and you should see the params file you want to edit: azt-param.txt. The file list is alphabetical.  Double-click to open the file.
Filling Out the Params File
There are several sections and fields you need to populate with your unique information before you can begin the setup.

## Sections

### sql server

* servers_sql_admin: This can be anything – It does not have to be unique. Use “wpaaztsqladm” if you like, or whatever you prefer
* servers_sql_admin_pwd: This must be 8 to 20 characters in length and include at least one symbol (@#$%&)

### synapse

* synapse_workspace: This can be whatever you want it to be – something on brand will likely work best because this name must be globally unique (no one else can use this name for their service).  There are some rules the name must adhere to as well:
* synapse_adlsgen: This also must be globally unique (no one else can use this name for their service), between 3 and 24 characters containing only lowercase and numbers (no capital letters, special characters, spaces)

### AAD Application registrations

The next three params will be in the API’s App Registration in Azure for your current AzT setup:
* aad_api_clientid: This is on the overview page labeled “Application (client) ID”
* aad_api_clientname: This is also on the overview page in the top left corner (it’s the name of the App Registration)
* aad_api_clientid_key: This is under “Certificates & Secrets” on the left-hand navigation, and then there will be a listing of valid (and invalid) keys, BUT you will not be able to retrieve the full key, only see the first three characters. The full key is only shown once when it is created, so your Azure Admin should be able to tell you what it is or make you a new one.

The last param in this section will be found on you UI’s App Registration in Azure for your current AzT setup:
* aad_ui_clientid: This is on the overview page labeled “Application (client) ID”

### dest storage

* storageAccounts_name: This is the name of your current storage account for your current installation of AzT (current resource group – should only be one)

### ux app service

* sites_web_name: This is the name of your current app service deployed for the UI (or UX) of your current installation of AzT

### api app service

* sites_api_name: This is the name of your current app service deployed for the API of your current installation of AzT

### General

* azure_tenantid: “Tenant ID” from the overview page of your Azure Active Directory service for your current AzT installation
* azure_subsscriptionid: “Subscription ID” from the overview page of your Resource Group for the current AzT installation
* resource_group_name: Name of your Resource Group for the current AzT installation
* azure_region: “Location” from the overview page of your Resource Group for the current AzT installation and remove the spaces and make all lowercase (e.g., “East US” will be entered as “eastus”)


### keyvault

* vaults_kv_name: This is the name of your current key vault used by your current installation of AzT

### source storage

* src_storageAccount: This is the container you downloaded the zip file from.  The value is: wpaappsprodtest1
* src_sasToken: This is the token you received in the email with this document that you pasted in the beginning of this walkthrough

### Linkage Account Details

* synapse_linkedServiceName: This can be whatever you want it to be – something on brand will likely be easier to remember
* synapse_linkedServiceAccntName: This should be the same as what you picked for synapse_linkedServiceName

>[!Note]
>Please save the azt-params.txt file after completing the edit.

## Running the Scripts
Now that you have all the correct information set in your params file, you are ready to run the scripts. First navigate into the folder using the command cd ./AztScripts_20211011 in your CloudShell:
 
Create Synapse Workspace and Spark Pool Cluster
Run command:
./2m-azuresynapseworkspaceandlinkage.ps1
This script creates a Synapse workspace with permissions, a Gen2 storage account that will be linked to Synapse, and a spark pool cluster.
Attaching the Package Requirements for Spark Pool Cluster and links Blob Storage
Run command:
./2m-azuresynapsepackage.ps1
This script adds packages to the spark pool cluster that are required to run the Synapse Pipelines.  This script utilizes the file detailing the packages to install, Requirements7.txt, to set the proper configuration and imports into the Spark Pool.
Updates the existing sql environment
Run command:
./2m-azuresynapsesql-code.ps1
This script updates the existing SQL server and includes stored procedure changes.
Importing the Integration Dataset
Run command:
./2m-azuresynapseintegrationdataset.ps1
This script reads files from a successfully completed ONA job and zips them into ONA_Results_zip. The ONA_Results_pipeline kicks in only after an ONA job has completed successfully.
Importing the Notebooks
Run command:
./2m-azuresynapsenotebookcreation-code.ps1
This script imports the notebooks from the storage account into the Synapse workspace.
Importing the Pipelines
Run command:
./2m-azuresynapsepipelinecreation.ps1
In this script, pipelines are created based on a JSON script and then imported into Synapse workspace. Pipelines are based off the kind of job being completed – e.g. Organizational Network Analysis or Relationship Intelligence.
Adding the Key Vault Secrets
Run command:
./2m-azuresynapsekeyvault.ps1
This script adds the key vault secrets for the Synapse workspace.
Adding Permissions to Storage Account
Run command:
Connect-AzureAD
Then run command:
./2m-azuresynapsepermissions.ps1
This script adds permissions to access the storage account from the Synapse Workspace.

>[!Note]
>The console will show “InvalidOperation: Expression after ‘&’” and “InvalidOperation: Connot index into null array’.  These are just warnings and can be ignored.

Deploying the UI and API
Run command:
./2e-appservice-code.ps1
This script uses Zip Deploy to install the build for the web application on the server.

Now that the transition to Synapse is complete, the API will facilitate calls only to Azure Synapse Pipelines as is consistent with the current Synapse solution.
