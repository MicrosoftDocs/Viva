---

ROBOTS: NOINDEX,NOFOLLOW
title: Relationship Intelligence Azure Template for Workplace Analytics 
description: Learn about the Relationship Intelligence Azure Template for Workplace Analytics and how to use it
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

# Relationship Intelligence Azure Template for Workplace Analytics

_These templates are only available as part of a Microsoft service engagement._

Workplace Analytics Azure Templates include the Relationship Intelligence template that enables you to analyze relationships your organization has with collaborators external to the company.

Workplace Analytics has a variety of measures to help you visualize and analyze formal and informal relationships within your organization, this template can help you understand how internal groups are communicating and spending their time with external collaborators.  
If you have account and contacts information from a CRM system, that can be leveraged to provide account level focus and insight into patterns.

## Prerequisites

* **CRM files** – Users should have Accounts and Contacts exported from Dynamics or Salesforce to view account data
* **Data access** - To view and categorize topics, the dataset must have exposed, unhashed data for **ExternalCollaboratorID** and **Subject lines**.
* **Power BI Desktop** - [Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t?activetab=pivot:overviewtab) installed locally for analysts.
* **Permissions** - For those who want to view the Relationship Intelligence reports, the Azure Templates admin must explicitly add them to the group or access control list for the configured Azure Analysis Server.

## To add new analysis

Use the following steps to add new analysis in Relationship Intelligence.

1. In Workplace Analytics Azure Templates, select **Relationship Intelligence**.
2. Select **Add New Analysis** (top right).
3. In **Define Analysis Settings**, enter a friendly name for the analysis and select a path to the dataset.
4. In Select the Account Mapping, select the set of account and contacts files you want to use to identify users and companies that your organization is talking with.  See Adding Account Mappings for details on how to create and upload these files for use.
5. In Select the Grouping Attributes, select the attributes you want to analyze and have available for pivoting in the final output report.  The available attributes match up to the HR attributes included in the imported organizational data from Workplace Analytics.
6. Select Submit. Based on the data size, it might take anywhere from a few minutes up to a few hours to successfully create the dataset.
7. After the analysis successfully loads, click the download icon corresponding to the analysis you created and following instructions in the dialog presented. Namely:

   * Select **Copy** to copy the database name specific to this analysis.
   * Select **Download PBIX file** to download a Power BI report.

## To view the report

1. Double click the PowerBI file saved above.
2. Authenticate with your corporate credentials if asked (your Azure Template admin will need to give you access to the Azure Analysis services used)
3.  On the “Home” ribbon in Power BI Desktop, choose Transform Data and then Data source Settings  
4. Paste the database name copied from the analysis dialog into the database field presented and select **OK**. Select **Model**, and then if prompted, select **OK**.


## To add Account Mappings

1. In Workplace Analytics Azure Templates, select Relationship Intelligence.
2. On the Relationship Intelligence page, select the Account Mapping tab. 
3. Click Add New Mapping button on the top right to create a upload a new set of files 
4. In the panel that shows up enter the following and click Submit to create.

   * A friendly name for the account and contacts set in the Mapping name section
   * Upload files for accounts and contacts (see note below about format).   
   * Indicate which schema or source the files were from: Microsoft Dynamics or Salesforce

Accounts and Contacts file formats
Microsoft Dynamics format – Accounts
 
Microsoft Dynamics format – Contacts
 
Salesforce Schema – Accounts
 

Salesforce Schema - Contacts



## Related topics

* [Workplace Analytics Azure Templates overview](./overview.md)
* [What's new in Workplace Analytics Azure Templates](./release-notes.md)
* [Deploy and configure Workplace Analytics Azure Templates](./deploy-configure.md)
