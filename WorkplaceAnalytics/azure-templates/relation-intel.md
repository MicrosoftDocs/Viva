---

ROBOTS: NOINDEX,NOFOLLOW
title: Relationship Intelligence Power BI report 
description: Learn about the Relationship Intelligence Power BI report included in Workplace Analytics Azure Templates and how to use it
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

# Relationship Intelligence Power BI report

_These templates are only available as part of a Microsoft service engagement._

Workplace Analytics Azure Templates includes the Relationship Intelligence Power BI report. You can use this report to analyze relationships your organization has with collaborators external to the company, such as customer or partner relationships.

Workplace Analytics has a variety of measures to help you visualize and analyze formal and informal relationships within your organization, this report can help you understand how internal groups are communicating and spending their time with external collaborators.

This report requires account and contact information from a Customer Relationship Management (CRM) platform, such as Dynamics or Salesforce. This report uses CRM data to provide account-level focus and insights into relationship patterns.

## Prerequisites
  
* **CRM data** –  Accounts and Contacts exported as .csv files from your CRM, such as Dynamics or Salesforce.
* **Data access** - Access to unhashed ExternalCollaboratorIDs and unhashed Subject lines to view “topics” in collaboration activity, such as for email, meetings, instant messages, and unscheduled calls.
* Power BI desktop app installed locally for analysts
* Permissions: the Azure Templates Admin must explicitly add all users who want to view the Relationship Intelligence reports to the group or access control list for the Azure Analysis Server configured 
 
To add a new analysis
1.	In Workplace Analytics Azure Templates, select Relationship Intelligence.
2.	On the Relationship Intelligence Analysis page, select Add New Analysis at top right.
3.	In Define Analysis Settings, enter a friendly name for the analysis and select a path to the dataset.

4.	In Select the Account Mapping, select the set of account and contacts files you want to use to identify users and companies that your organization is talking with.  See Adding Account Mappings for details on how to create and upload these files for use.
5.	In Select the Grouping Attributes, select the attributes you want to analyze and have available for pivoting in the final output report.  The available attributes match up to the HR attributes included in the imported organizational data from Workplace Analytics.


6.	Select Submit. Based on the data size, it might take anywhere from a few minutes up to a few hours to successfully create the dataset.
7.	After the analysis successfully loads, click the download icon corresponding to the analysis you created and following instructions in the dialog presented. Namely:
  

•	Click “Copy” to copy the database name specific to this analysis 
•	Click “Download PBIX File” to download a PowerBI report

To view the report:
1.   Open the Power BI file saved in the previous steps.
2.  Authenticate with your corporate credentials if asked (your Azure Template admin will need to give you access to the Azure Analysis services used)
3.  On the “Home” ribbon in Power BI Desktop, choose Transform Data and then Data source Settings  
-	 

Paste the database name copied from the analysis dialog into the database field presented and click OK.  Select “Model” and OK if prompted.



To add Account Mappings
1.	In Workplace Analytics Azure Templates, select Relationship Intelligence.
2.	On the Relationship Intelligence page, select the Account Mapping tab. 
3.	Click Add New Mapping button on the top right to create a upload a new set of files 
 
4.	In the panel that shows up enter the following and click Submit to create.
o	A friendly name for the account and contacts set in the Mapping name section
o	Upload files for accounts and contacts (see note below about format).   
o	Indicate which schema or source the files were from: Microsoft Dynamics or Salesforce
Accounts and Contacts file formats
Microsoft Dynamics format – Accounts
 
Microsoft Dynamics format – Contacts
 
Salesforce Schema – Accounts
 

Salesforce Schema - Contacts
 

