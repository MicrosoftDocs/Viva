---

ROBOTS: NOINDEX,NOFOLLOW
title: Viva Insights partner solution overview
description: An overview of how Microsoft Viva Insights works with partners to access and analyze on-premises Exchange mailbox data
author: madehmer
ms.author: helayne
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
# Viva Insights partner solution overview

Microsoft Viva Insights provides insights into communication and collaboration trends that can affect your bottom line. Viva Insights uses Microsoft 365 email and calendar metadata to create behavioral metrics about how your employees are currently spending their time and working together.

Viva Insights requires Microsoft 365 Exchange Online mailbox data. If your organization uses on-premises Exchange mailboxes, you will need to do one of the following to use Viva Insights:

* Migrate your organization's mailboxes to [Exchange Online](/Exchange/exchange-online).
* Use a partner solution that replicates your organization's on-premises Exchange mailbox data into Microsoft 365 storage mailbox data in Exchange Online. Viva Insights can then access and use the replicated mailbox data for all your organizational data analysis needs.

Your organization must comply with the system requirements and complete the setup tasks described in [Viva Insights partner solution setup](./partner-setup.md).

## Viva Insights partner solutions

* **Archive360 FastCollect** - A solution for Azure that connects on-premises data to Microsoft 365 and Azure data. This solution supports large datasets of structured, semi-structured, and unstructured data and is very extensible as a modular architecture solution. This solution requires an on-premises connector (deployed by the customer) with the data hosted on-premises and uses MAPI for cloud access. For a managed solution, Archive360 needs access to the connector. See [Archive360 FastCollect](https://www.archive360.com/products/fastcollect-for-archives/) for details.

* **Quest On Demand Migration for Email** - Offers a cloud-based service that synchronizes on-premises Exchange mailbox data with Microsoft 365 as staged mailboxes for Viva Insights to access and analyze. The data is hosted on Quest’s Azure tenant. This solution uses SaaS and an on-premises application with Exchange Web Services. See [Quest](https://www.quest.com/products/on-demand-migration-for-email/) for details.

* **TransVault WPA-SYNC** - Replicates on-premises Exchange mailbox data into Microsoft 365 for access by Viva Insights. Implemented as a managed service, it can be deployed on-premises or in Azure and features encrypted end-to-end transfers, auditing and chain-of-custody for optimal security and compliance. WPA-SYNC also has a range of options for controlling operations and ensuring scalability in large/complex environments. It uses SaaS with Exchange Web Services and requires access to the customer's domain. See [TransVault](https://www.transvault.com/solutions/microsoft-workplace-analytics-for-hybrid/) for details.
