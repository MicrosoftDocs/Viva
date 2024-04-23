---
title: "Manage Viva Engage domains in Microsoft 365"
description: "When you add or remove verified domains in Microsoft 365, they are automatically added or removed from your Viva Engage network."
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 09/29/2023
audience: Admin
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 9d9f9ee8-7c56-4f50-81f3-aa0a8d761e14
---

# Manage Viva Engage domains in Microsoft 365

As the Microsoft 365  administrator, you manage Viva Engage domains in Microsoft 365 from the **Domains** link in the Microsoft 365 admin center. When you add or remove a domain in Microsoft 365, it's automatically added to or removed from the corresponding Viva Engage network, usually within minutes.
  
- If you just have one domain or don't have a legacy Viva Engage network prior to using Microsoft 365, once your domain is set up in Microsoft 365, your Viva Engage network is automatically created.

- If you have multiple domains but no legacy Viva Engage networks, setting up your domains in Microsoft 365 is straightforward. Users in all domains you add to Microsoft 365 can use your Viva Engage network.

- It gets a little more complicated when you have a legacy Viva Engage network associated with one or more of your domains.

## Initial setup for your primary Viva Engage domain
Once your domain is set up in Microsoft 365, your Viva Engage network is automatically created. Your Viva Engage primary domain is based on the first custom domain name added to Microsoft 365. So if your custom domain is contoso.com, you can access your Viva Engage network. If you don't have a custom domain name in Microsoft 365, your Viva Engage network is created using your .onmicrosoft.com domain.

### Add an additional domain to Viva Engage

1. To add a domain to Viva Engage, add the domain in Microsoft 365 by following the directions in [Add a domain to Microsoft 365](https://support.office.com/article/6383f56d-3d09-4dcb-9b41-b5f5a5efd611). You must be a Microsoft 365 Global administrator on Microsoft 365 to perform these steps.

    For example, say you have a Microsoft 365 subscription that uses the domain contoso.com, and a corresponding Viva Engage network. If you add the domain **contosopharmaceuticals.com** to your Microsoft 365 tenant, that domain is automatically added to Viva Engage. Afterward, a new user of that domain, such as ryani@contosopharmaceuticals.com, can sign in to Viva Engage seamlessly with Microsoft 365 credentials.

2. Verify that the domain you added in Microsoft 365 has been added to Viva Engage.  
  
    1. In Viva Engage, select the Viva Engage settings icon :::image type="icon" source="../../media/9704ce70-56ce-43f7-96c6-f253b0413d40.png"::: in the left nav, and select **Network Admin**.

       :::image type="content" source="../../media/d1ec06fa-c2fb-4dcb-b21f-6dff1d20d6ad.png" alt-text="Viva Engage navigation, including Settings icon.":::
  
    1. In the **Network** section choose **Network Migration**.

       :::image type="content" source="../../media/f9ae9328-9cb2-46f7-9bce-26bcdc29b3fa.png" alt-text="Network Migration menu item for Viva Engage Admins.":::
  
    1. The **Step 1 of 3 - Check/Add Verified Domains** page shows the list of domains on the Viva Engage network.

       :::image type="content" source="../../media/cac649d6-9245-4645-8f59-fb27dffd87e8.png" alt-text="Screenshot of Step 1 of 3 - Check/Add Verified Domains before migrating a Viva Engage network.":::
  
### Remove a domain from Viva Engage

When you remove a domain from Microsoft 365, the domain is immediately removed from Viva Engage. Everyone with email addresses on the domain you removed can no longer access your Viva Engage network.

For instructions, follow the steps in [Remove a domain from Microsoft 365](https://support.office.com/article/Remove-a-domain-from-Office-365-f09696b2-8c29-4588-a08b-b333da19810c).

If you want to consolidate multiple domains into one Viva Engage network, see [Consolidate multiple Viva Engage networks](consolidate-multiple-networks.md).

## Change the network name displayed in the left navigation pane in Viva Engage
To change the displayed network name shown below, change the **name** in the Microsoft 365 Organization profile. This setting overrides the **Network Name** set in the Viva Engage Network admin. For steps, see [Change your organization's address, technical contact, and more](https://support.office.com/article/Change-your-organization-s-address-technical-contact-and-more-a36e5a52-4df2-479e-bb97-9e67b8483e10).

   :::image type="content" source="../../media/0a1125b1-74d2-4ea5-b8e4-6d52456a527e.jpg" alt-text="List of Viva Engage groups on the Viva Engage page.":::
  
### Change the Viva Engage primary domain

If you have just one domain in Microsoft 365, when the default domain changes in Microsoft 365 to a verified domain, the primary domain of the corresponding Viva Engage network is updated.

   >[!NOTE]
   >If you change the primary domain in Microsoft 365 to the .onmicrosoft.com domain, Viva Engage will not update the primary domain to the .onmicrosoft.com domain. Automatic domain updates in Viva Engage are only for non .onmicrosoft.com domains.

## Change the Viva Engage primary domain when you use a federated domain as your Microsoft 365 default domain

Contact Viva Engage support to help you do this domain setup.

## If your Viva Engage network has domains not verified on the Microsoft 365 tenant

If your Viva Engage network has domains that aren't verified on the corresponding Microsoft 365 tenant, you can't manage your domains from Microsoft 365. For example:
  
- Verified domains on the Microsoft 365 tenant: contoso.onmicrosoft.com, contoso.com, northwind.com

- Domains on the corresponding Viva Engage network: contoso.com, tailspin.com

Note that tailspin.com on the Viva Engage network is not verified on the Microsoft 365 tenant. If your network is in this situation, you can remedy the situation so that you can manage the domains from Microsoft 365 one of two ways. You can either:
  
1. Add and verify the missing domains to the Microsoft 365 tenant. In the example above, you would add tailspin.com to the Microsoft 365 tenant.

2. Remove the additional domain in Viva Engage. To remove Viva Engage domains from your network, contact the Viva Engage support team. In the example above, you would remove tailspin.com

After you take one of the actions above, the rest of the domains (contoso.onmicrosoft.com, northwind.com) will be added to Viva Engage, and from this point on, you can manage your domains across their lifecycle in Microsoft 365.
  
> [!TIP]
> To ensure that you don't miss this step, all Viva Engage verified administrators will receive an email notification if the list of domains on Viva Engage is out of sync with the list on Microsoft 365.
  
### If your Microsoft 365 tenant is associated with more than one Viva Engage network

These extra networks could be free Viva Engage Basic networks created by employees of your company. For example:
  
- Verified domains on the Microsoft 365 tenant: contoso.onmicrosoft.com, contoso.com, northwind.com

- Domain on Viva Engage network1: contoso.com

- Domain on Viva Engage network2: northwind.com

This configuration is no longer supported as of October 16, 2018. For more information, see [Consolidate multiple Viva Engage networks](consolidate-multiple-networks.md).

Beginning December 2019, if you add an [external domain with a Viva Engage Basic network](add-basic-domains-to-office-365.md) (“Basic network”) to your Microsoft 365 tenant, we must disassociate the domain from the basic network in order to associate the domain with the primary network for your Microsoft 365 tenant. The basic network is then queued for deletion.

### If you have more than one Microsoft 365 tenant associated with one Viva Engage network

This configuration is not supported. For more information, see [About Viva Engage networks and Microsoft 365 tenants](../engage-microsoft-365-groups.md).

For example:
  
- Verified domains on the Microsoft 365 tenant1: contoso.onmicrosoft.com, contoso.com

- Verified domains on the Microsoft 365 tenant2: northwind.onmicrosoft.com, northwind.com

- Domains on Viva Engage network: contoso.com, northwind.com
