---
title: "Add Viva Engage domains to your Office 365 tenant"
description: "Migrate domains to a supported state for your tenant."
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: dmillerdyson
ms.date: 6/28/2023
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
localization_priority: Priority
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Add Viva Engage domains to your Office 365 tenant

We recommend that you consolidate previously migrated basic (free) networks into a single primary network for your tenant in order to move Viva Engage into a supported state for your tenant.

If you add an external domain with a Basic network to your Office 365 tenant, we must *disassociate* the domain from the basic network in order to *associate* that domain with the primary network for your O365 tenant. **The basic network is then queued for deletion.**

Following is a set of actions we immediately take after you add a domain. Also, there’s a set of steps you can take to preserve the data from the network before we delete it.

**Microsoft will**:

- Remove all users from the network formerly associated with the added domain. This ensures that your users can access the primary network for your Office 365 tenant, if they're permitted to do so based on your licensing.

- Enable the network formerly associated with the added domain to allow for data export.

- Add all Global Admins from your Office 365 tenant as guests with Verified Admin privileges in the network formerly associated with the added domain.

- Disable the network formerly associated with the added domain 30 days from the date you added the domain to your Office 365 tenant.

- Queue the network formerly associated with the added domain for deletion in an additional 30 days. At that time, we will delete the network, including all the data that was in the network formerly associated with the added domain.

**To preserve data from the network formerly associated with your domain**:

1. Select **Settings** in the home network of your Office 365 tenant.

2. Choose the network formerly associated with your domain from the list of available networks.

3. Export the data for the network formerly associated with your domain. For instructions, see [Export data from Viva Engage](eac-as-manage-data.md). None of the data from your Basic Network is migrated to your Viva Engage network for your Office 365 tenant.

>[!NOTE]
> If you don't want to access or download content from the network formerly associated with the added domain, no action is required. **The network formerly associated with the added domain—-including all data in such a network—-will be automatically deleted.**


## Related articles

[Overview of Native Mode for Microsoft 365](overview-native-mode)