---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Workplace Analytics partner solution setup
description: How to set up an on-premises Exchange server to work with Workplace Analytics. 
author: madehmer
ms.author: madehmer
ms.date: 9/18/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa

---

Workplace Analytics requires Office 365 storage mailbox data in Exchange Online. If your organization uses on-premises Exchange for mailbox storage, you'll need to either migrate to Exchange Online or use a partner solution to connect Workplace Analytics to your organization's email and calendar metadata.

If you want to use a partner solution to connect Workplace Analytics to your on-premises Exchange mailbox data, you must meet the following system requirements and then complete the following setup steps.

### System requirements for a partner solution setup

**On-Premises Exchange configuration**

* On-premises Exchange 2007-based organizations or later
* Office 365 in hybrid mode or have completed the Office 365 Hybrid Configuration wizard​
* On-premises Active Directory synchronized with Azure Active Directory Connect (previously known as the Directory Sync or DirSync.exe tool)

**Office 365 licensing requirements**

* Exchange Online Plan 1 or 2 license
* Workplace Analytics license

**Partner solution requirements and permissions**

* An account with Exchange impersonation​ for multiple-mailbox access permissions
* Active Directory read access​
* Open ports (HTTPS) and namespaces to connect to the partner solution
* If the storage mailbox data is hosted in your domain on premises, your Workplace Analytics admin needs domain access to manage the solution end-to-end

     **Question?** *What part of the solution is hosted on the customer's domain? Is it the storage mailbox data that's stored in their domain? Solution seems too general??*

## Set up your on-premises Exchange server



## How to get help

* For personal guidance with partner solutions or help with Workplace Analytics setup and data analysis, email the Workplace Analytics Fast Track team at <wpaft@Microsoft.com>.
* For general help with Office 365, Exchange, Azure Active Directory, assigning licenses, and issues with user access and permissions, contact Microsoft Support at https://support.microsoft.com.