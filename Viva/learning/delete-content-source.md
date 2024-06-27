---
title: Delete content providers
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 06/27/2024
audience: admin
ms.topic: article
ms.service: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - Tier1
  - essentials-manage
ms.localizationpriority: medium
description: Learn how to delete a content provider in Microsoft Viva Learning.
---

# Delete a content provider in Viva Learning

As an admin, you can delete a provider in Viva Learning. 

This action is done in **Manage providers** within the Viva Learning admin tab.  

When you mark a provider to be deleted, all provider data, including learner records, is immediately hidden in the Viva Learning app's user experience.

This table outlines how different learning providers schedule and delete data from their database. 
The estimated time taken for deletion also depends on the data size.  

| Learning provider    | Deletion behavior   |
|---|---|
| LMS (Cornerstone OnDemand, Saba, SuccessFactors, Workday)    | The data from database is scheduled for deletion immediately.   |
| Global Providers (Microsoft 365 Learning, Microsoft Learn, LinkedIn Learning)  | The data from database is scheduled for deletion in 72 hours.   |
| Other Third-party providers (such as Coursera and Go1)   | The data from database is scheduled for deletion in 72 hours   |
| SharePoint  | The data from database is scheduled for deletion immediately.   |
| Graph APIs   | The data from database is scheduled for deletion immediately.   |

**How does deleting a provider reflect in the Viva Learning user experience?**

The data from a deleted provider is immediately hidden in Viva Learning app user experience. This includes, but isn't limited to:
- Provider catalog
- Learner metadata, for example bookmarks
- Learning paths
- Collections
- Assignments
- Completion

Refresh the Viva Learning app in case the data is still visible.

The provider data remains visible in Microsoft 365 search until 24 hours the after provider deletion.

**Can I track the completion of a provider's data deletion from the backend?**

Admins can't currently view the stage of data deletion within the Viva Learning admin tab.

Contact the Viva Learning team to know about the data deletion stage. 

**Can I track if data deletion is complete from backend?**
Currently, there's no experience in Viva Learning admin tab to inform about the data deletion stage. Contact Viva Learning team to confirm the data deletion stage.  

**When can I reconfigure a provider?**

You can reconfigure the learning management system  and SharePoint immediately after deletion. Viva Learning starts a full sync once reconfigured.
  
> [!NOTE]
> For other learning sources, reconfiguring the provider with the same parameters before deletion is complete can bring back the old data. Contact Viva Learning team to confirm the data deletion stage.