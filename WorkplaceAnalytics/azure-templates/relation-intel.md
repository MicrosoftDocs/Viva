---

ROBOTS: NOINDEX,NOFOLLOW
title: Relationship Intelligence report 
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

# Relationship Intelligence

_These templates are only available as part of a Microsoft service engagement._

Workplace Analytics Azure Templates includes the Relationship Intelligence report for Power BI. You can use this report to analyze relationships your organization has with collaborators external to the company, such as relationships with customers or partners.

Workplace Analytics has a variety of measures to help you visualize and analyze formal and informal relationships within your organization. This report can help you understand how internal groups are communicating and spending their time with external collaborators.

This report requires account and contact information from a Customer Relationship Management (CRM) platform, such as Dynamics or Salesforce. It uses CRM data to provide account-level focus and insights into relationship patterns.

The Relationship Intelligence report includes the following:

* **Relationship Overview** - Shows information about accounts, including:

  * The Account table shows an overview of related collaboration activity with accounts, such as email and meeting hours spent with them and the last date the organization engaged with them.
  * The **Relationship score** is based on the amount, frequency, and timeliness of collaboration activity with an account.
  * Page down to see a **Relationship Highlights** chart and a chart with **Distinct contacts** analysis.
  * Use the **HR Attribute Filter** to focus the chart analysis on a specific collaboration.
  * The **Group Engagement**, **Collaboration Time**, and **Meetings by Length** charts show more details about account collaboration activity.

* **Account Analysis** - Focuses in on more details about the selected account from the first page, including:

  * See visuals about the average relationship score and how the score has changed over the selected time period.
  * Use the **HR Attribute Filter** to focus your analysis on specific areas of collaboration for the visuals about collaboration.
  * The collaboration visuals on this page also show you what type of communication has occurred with contacts over time and who the top individual account contacts are that the organization has collaborated with. It also lists the top groups in the organization that have collaborated with an account.
  * The **Topics** section shows the main topics in a word cloud that collaboration activity was focused on. The topics are based on the subject lines for meetings and email. Use the **Time Range Selection** to see how the topics in the word cloud change based on what date range is selected.
  * You'll also see visuals for collaboration trends by communication type and typical meeting lengths for the selected account.

* **Individual Collaborators** - Shows more details about all the individual account contacts and all the organizational groups that have collaborated with these contacts. The tables include the relationship score, rankings, and other details about how your organization is collaborating with individual account contacts for the selected account.

![Relationship Overview report page](./images/ri-report-1.png)

## Steps to create the report

1. [Prerequisites](#prerequisites) - Confirm or complete all the prerequisites.
2. [Add an account mapping](#add-an-account-mapping) - Follow the steps to create a new account mapping file in Workplace Analytics Azure Templates.
3. [Add new analysis](#add-new-analysis) - Follow the steps to create the dataset in Workplace Analytics Azure Templates that the Power BI report uses.
4. [Load the data and view the report](#load-the-data-and-view-the-report) - Follow the steps to download the Power BI template and load the data in Power BI. You can then use Power BI to visualize the data and drill in and focus on account details.

## Prerequisites

* **CRM data** –  Accounts and contacts exported as .csv files from your CRM, such as Microsoft Dynamics or Salesforce. See [Required CRM file formats](#required-crm-file-formats) for details about what the files must include based on the type of CRM.
* **Data access** - You need access to unhashed ExternalCollaboratorIDs and unhashed Subject lines to view topics in your organization's Office 365 collaboration data, such as for email, meetings, instant messages, and unscheduled calls.
* **Power BI Desktop** - Have the latest version of Power BI Desktop installed locally. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t?activetab=pivot:overviewtab) to download and install the latest version.
* **Permissions** - The Azure Templates admin must explicitly add people who want to view the Relationship Intelligence reports to the group or access control list for the configured Azure Analysis Services.

## Add an account mapping

Before creating analysis, you need to upload the exported CRM data (.csv) data files for your customer accounts and contacts and create a mapping file in the template. See [Required file formats](#required-crm-file-formats) for details about what the files must include based on the type of CRM.

1. In Workplace Analytics Azure Templates, select **Relationship Intelligence**.
2. Select **Account Mapping** > **Add New Mapping** (at top right) to upload a new set of files for customer accounts and contacts.

    ![Add a mapping file for the report](./images/ri-account-map.png)

3. In **Name the Account mapping**, enter a friendly name for the mapping file.
4. In **Provide the accounts** and **Provide the contacts**, select **Choose File**, and then select the .csv files for accounts and contacts, which must be in the required format as described in [Required CRM file formats](#required-crm-file-formats).
5. In **Specify your CRM source**, select the CRM source for your accounts and contacts.  

### Required CRM file formats

The following are examples of what the .csv file formats for accounts and contacts must include.

#### Dynamics accounts

![File format for Dynamics accounts](./images/ri-dynamics-accounts.png)

#### Dynamics contacts

![File format for Dynamics contacts](./images/ri-dynamics-contacts.png)

#### Salesforce accounts

![File format for Salesforce accounts](./images/ri-salesforce-accounts.png)

#### Salesforce contacts

![File format for Salesforce contacts](./images/ri-salesforce-contacts.png)

## Add new analysis

After you add a mapping file for your customer accounts and contacts, do the following to create the dataset for the report.

1. In Workplace Analytics Azure Templates, select **Relationship Intelligence** > **Add New Analysis** (at top right).
2. In **Define Analysis Settings**, enter a friendly name for the analysis and select the path to the dataset.

    ![Add new analysis for the report](./images/ri-new-analysis.png)

3. In **Select Account Mapping**, select the mapping file you created in [Add an account mapping](#add-an-account-mapping).
4. In **Select the Grouping Attributes**, select two to five HR attributes to analyze and use to pivot analysis in Power BI. These are the HR attributes imported with the organizational data from Workplace Analytics.
5. Select **Submit**. Creating the dataset will take a few minutes up to a few hours based on the size of the data.
6. In **Relationship Intelligence** > **Analysis**, the analysis table includes the name, the source, the date is was submitted, who submitted it, and the following:

   * **Download** - Select to copy a link to this dataset and download the Power BI template.
   * **Parameters** - Lists details about the job parameters, such as the input path, output folder, excluded keywords, the mapping file name, the HR attributes included, and the person who created this analysis.
   * **Status** - Analysis shows a green check mark when it successfully adds it. A red X means it failed.
   * **Details** - Lists the job details including error messages (far right column) to help troubleshoot a failure.
   * **Delete** - Select to delete analysis that failed or that's no longer needed.

    ![Analysis table details](./images/ri-analysis-table.png)

    ![Download Power BI template and copy data link](./images/ri-download.png)

## Load the data and view the report

1. In **Workplace Analytics Azure Templates** > **Relationship Intelligence** > **Analysis**, when the analysis status has a green check mark, select the **Download** icon for the analysis.
2. You need to copy both the server and database information for this analysis when prompted in Power BI Desktop in **Step 6**.
3. Select **Download PBIX File** to download the Power BI template for the report.
4. Open the downloaded file in Power BI Desktop.
5. If prompted, authenticate your credentials, which the Azure Templates admin used to give you access to the Azure Analysis services.
6. In Power BI Desktop, select **Transform data** > **Data source settings** and paste the server and database name that you copied for the analysis in **Step 2** in the **Server** and **Database** fields, and then select **OK**.
7. If prompted by the Navigator, select **Model**, and then **OK**.
8. It might take a few minutes up to a few hours to load the data from the database into the report. After it loads, you can analyze report data with Power BI tools and visualizations.

## Power BI tips, troubleshooting, and FAQs

An important tip to know about this specific Power BI report is the drill through hierarchy. To select an account or an individual collaborator to analyze on the **Account Analysis** and **Individual Collaborators** pages of the report, you must right-click the account on the **Relationship Overview** page, and then select **Drill through** > **Account Analysis**. Then you can view information about that selected account on the other two pages.

![Use Drill through for Account Analysis and Individual Collaborator data](./images/ri-drill-through.png)

For details about how to share the dashboard and other Power BI tips, troubleshoot any issues, or review the most frequently asked questions, see [Power BI templates in Workplace Analytics](../tutorials/power-bi-templates.md).

For more details about how to use Power BI tools, see [Interact with visuals in reports, dashboards, and apps](https://docs.microsoft.com/power-bi/consumer/end-user-visualizations).
