---
title: "Add Viva Engage domains to your Office 365 tenant"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: pamgreen
ms.date: 06/28/2023
audience: Admin
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid: 
- MOE150
- MET150
description: "Learn what happens when you add a domain to your Office 365 tenant associated with a Yammer Basic network."
---

# Add Yammer basic domains to your Office 365 tenant

Beginning December 2019, we're changing what happens when you add a domain associated with a basic (free) Yammer network to your Office 365 tenant. Multiple primary networks are no longer supported.

We recommend that you consolidate previously migrated basic networks into a single primary network for your tenant. Doing so moves Viva Engage into a supported state for your tenant.

If you add an external domain with a Yammer Basic network (“Basic network”) to your Office 365 tenant, we must *disassociate* the domain from the basic network in order to *associate* that domain with the primary network for your O365 tenant. **The basic network is then queued for deletion.**

Below is a set of actions we immediately take after you add a domain. Also, there’s a set of steps you can take to preserve the data from the network before we delete it.

**Microsoft will**:

- Remove all users—from the network formerly associated with the added domain—so they can access the primary network for your Office 365 tenant if permitted to do so based on your Yammer licensing.

  
    :::image type="content" source="../../media/kb/Yammer-network-settings.PNG" alt-text="Screenshot of the Yammer network settings.":::

- Enable the network formerly associated with the added domain to allow for data export.

- Add all Global Admins from your Office 365 tenant as guests with Verified Admin privileges in the network formerly associated with the added domain.

- Disable the network formerly associated with the added domain 30 days from the date you added the domain to your Office 365 tenant.

- Queue the network formerly associated with the added domain for deletion in an additional 30 days. The network will be deleted, including all the data that was in the network formerly associated with the added domain.

**To preserve data from the network formerly associated with your domain**:

1. Select Settings :::image type="icon" source="../../media/9704ce70-56ce-43f7-96c6-f253b0413d40.png" border="false"::: in the home Yammer network of your Office 365 tenant.

2. Choose the network formerly associated with your domain from the list of available networks.

3. Export the data for the network formerly associated with your domain. For instructions, see [Export data from Yammer Enterprise](../manage-security-and-compliance/export-viva-engage-enterprise-data.md). None of the data from your Yammer Basic Network are migrated to your Yammer Enterprise network for your Office 365 tenant.

>[!NOTE]
> If you do not want to access or download content from the network formerly associated with the added domain, you don’t need to do anything. **The network formerly associated with the added domain—including all data in such a network—will be automatically deleted.**

## Additional information

- To learn what to do when a domain associated with a Basic Yammer network is added to your Office 365 tenant, see [Manage Yammer domains in Office 365](manage-viva-engage-domains.md).

## Related articles

[Network migration - Consolidate multiple Yammer networks](consolidate-multiple-viva-engage-networks.md)
