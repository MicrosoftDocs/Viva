---

ROBOTS: NOINDEX,NOFOLLOW
ms.date: 09/20/2018
title: Viva Insights partner solution setup
description: How to set up an on-premises Exchange server to work with Advanced insights from Microsoft Viva Insights
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: m365initiative-viva-insights 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin

---
# Viva Insights partner solution setup

Microsoft Viva Insights requires Microsoft 365 storage mailbox data in Exchange Online. If your organization uses on-premises Exchange for mailbox storage, you'll need to either migrate to Exchange Online or use a partner solution to connect Viva Insights to your organization's email and calendar metadata.

If you want to use a partner solution to connect Viva Insights to your on-premises Exchange mailbox data, you must meet the following system requirements and then complete the following setup tasks.

## System requirements for a partner solution setup

**On-Premises Exchange configuration**

* On-premises Exchange 2007-based organizations or later
* Microsoft 365 in hybrid mode or have completed the Microsoft 365 Hybrid Configuration wizard​
* On-premises Active Directory synchronized with Azure Active Directory Connect (previously known as the Directory Sync or DirSync.exe tool)

**Microsoft 365 licensing requirements**

* Exchange Online Plan 1 or 2 license
* Viva Insights license

**Partner solution requirements and permissions**

* An account with Exchange impersonation​ for multiple-mailbox access permissions
* Active Directory read access​
* Open ports (HTTPS) and namespaces to connect to the partner solution
* If the partner solution is hosted in your on-premises domain, your Viva Insights admin needs domain access to manage the solution end-to-end

## Workflow to set up the partner solution

The following table lists the necessary tasks and who's responsible for them during each phase of setting up the partner solution.

|Solution setup phase|Your tasks as the customer|Partner tasks|Microsoft tasks
|--------------------|---------------|-------------|-------------------------|
|Assess, scope, and select a partner solution|<ul><li>Select a partner solution</li><li>Sign applicable contracts</li><li>Confirm scope, including number of mailboxes and time range of data to copy</li></ul>|Provide quotes and statement of work|Provide assistance with assessment|
|Deploy the solution|Provide solution requirements, including Exchange mailbox impersonation permissions, open ports, and namespaces|<ul><li>Deploy and configure the solution​</li><li>Create [Microsoft 365 Exchange Online storage mailboxes​](#storage-mailbox-setup)</li><li>Assign licenses for mailboxes with Exchange and for Viva Insights</li><li>Disable mailbox access and email routing​</li><li>Hide the storage mailboxes from Exchange's Global Address List (GAL)</li></ul>|Provide mailbox naming convention (the primary/secondary (proxy) SMTP to use)
|Test the solution|Review pilot results|<ul><li>Copy pilot data from on-premises to Microsoft 365​​</li><li>Coordinate testing with Microsoft​​</li><li>Resolve any issues with the solution</li></ul>|Confirm the pilot data is available to Viva Insights in the advanced insights app and sign-off on the solution
|Production|<ul><li>Confirm data is available to Viva Insights in the advanced insights app</li><li>Provide scope changes, if any</li></ul>|<ul><li>Copy all scoped mailboxes​</li><li>Provide status reports to the customer and to Microsoft​</li><li>Copy any deltas, continuously or daily​</li><li>Clean up mailboxes when ready to migrate</li></ul>|Monitor production data to check it’s available to Viva Insights in the advanced insights app
|Change requests (if any)|Submit changes to mailboxes per process outlined in statement of work|Resolve any issues with the solution|Resolve any issues with Microsoft services

## Storage mailbox setup

Storage mailboxes are Microsoft 365-based mailboxes that contain synchronized data from associated on-premises Exchange Online mailboxes. You can use a PowerShell script to create and configure these mailboxes and assign required licenses, if necessary.

![Advanced insights storage mailboxes.](./images/storage-mailboxes.png)

​These storage mailboxes are different than the mailboxes that already exist in Microsoft 365. Viva Insights uses logic to map the storage mailboxes to the correct user mailboxes for data analysis. For these storage mailboxes, you'll need to:

* Confirm they're not linked to any existing mailboxes
* Confirm they're only visible to Viva Insights and your Microsoft 365 admin
* Disable the following Exchange Online mailbox parameters:
  * ActiveSyncEnabled
  * EwsAllowEntourage
  * EwsAllowMacOutlook
  * EwsAllowOutlook
  * IMAPEnabled
  * MAPIEnabled
  * POPEnabled
  * OWAEnabled
  * OWAforDevicesEnabled
  * UniversalOutlookEnabled

## How to get help

* For personal guidance with partner solutions or help with the advanced insights app setup and data analysis, email the FastTrack team at <wpaft@Microsoft.com>.
* For general help with Microsoft 365, Exchange, Azure Active Directory, assigning licenses, and issues with user access and permissions, contact [Microsoft Support](https://support.microsoft.com/contactus/).

