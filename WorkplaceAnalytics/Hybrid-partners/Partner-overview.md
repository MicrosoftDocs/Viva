---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,NOFOLLOW
title: Workplace Analytics partner solution overview
description: An overview of how Workplace Analytics works with partners to access and analyze on-premises Exchange mailbox data. 
author: madehmer
ms.author: madehmer
ms.date: 9/18/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---
# Workplace Analytics partner solution overview

Workplace Analytics provides rich insights into your company’s communication and collaboration trends to identify behaviors that affect your bottom line. Workplace Analytics uses Office 365 email and calendar metadata and turns it into a set of behavioral metrics that help you understand how your teams are currently spending their time and working together.

Workplace Analytics requires Office 365 Exchange Online mailbox data. If your organization uses on-premises Exchange mailboxes, you will need to do one of the following to use Workplace Analytics:

* Migrate your organization's mailboxes to [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online).
* Use a partner solution that replicates your organization's on-premises Exchange mailbox data into Office 365 storage mailbox data in Exchange Online. Workplace Analytics can then access and use the replicated mailbox data for all your organizational data analysis needs.

Your organization must comply with the system requirements and complete the setup tasks described in [Workplace Analytics partner solution setup](./partner-setup.md).

## Workplace Analytics partner solutions

* **Archive360 FastCollect** is an Azure-based solution that connects your on-premises data to Office 365 and Azure. This solution supports large data sets of structured, semi-structured, and unstructured data and is very extensible as a modular architecture solution. This solution requires an on-premises connector (deployed by the customer) with the data hosted on-premises and uses MAPI for cloud access. For a managed solution, Archive360 needs access to the connector. To learn more about this solution, see [Archive360 FastCollect](https://www.archive360.com/products/fastcollect-for-archives/).

* **Quest On Demand Migration for Email** offers a cloud-based service that synchronizes on-premises Exchange mailbox data with Office 365 as staged mailboxes for Workplace Analytics to access and analyze. The data is hosted on Quest’s Azure tenant. This solution uses SaaS and an on-premises application with Exchange Web Services. To learn more about this solution, see [Quest](https://www.quest.com/products/on-demand-migration-for-email/).

* **TransVault WPA-SYNC** replicates on-premises Exchange mailbox data into Office 365 for access by Workplace Analytics.  Implemented as a managed service, it can be deployed on-premises or in Azure and features encrypted end-to-end transfers, auditing and chain-of-custody for optimal security and compliance.  WPA-SYNC also has a range of options for controlling operations and ensuring scalability in large/complex environments.  It uses SaaS with Exchange Web Services and requires access to the customer's domain. To learn more about this solution, see [TransVault](https://www.transvault.com/solutions/microsoft-workplace-analytics-for-hybrid/).
