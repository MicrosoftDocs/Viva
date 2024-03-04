---
title: "Manage Viva Engage security settings"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 8/10/2023
audience: Admin
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
search.appverid: 
- MOE150
- MET150
ms.assetid: a5f747cc-1306-450e-b8e2-23f465756f1e
description: "Control how people access Viva Engage, set password policies, control who can create external networks, and enforce Microsoft 365 identity."
---

# Manage Viva Engage security settings

Control how people access Viva Engage: set password policies, control external network access and information, and enforce Microsoft 365 identity.
  
## Allow access to Viva Engage only from the office or VPN (logical firewalls)

1. In the Viva Engage admin center, go to **Content and Security** \> **Security Settings**.

2. In the **IP Range** section, specify the IP ranges of your corporate network or other trusted networks.

3. Select whether to allow sign-in to users outside the specified ranges.

    Typically, users using mobile clients will be outside of the authorized IP range (unless the mobile client is using Wi-Fi on a trusted network). To allow access from mobile clients, select **Allow login**. This restricts web sign-ins outside of your trusted IP range, but allows mobile client logins from outside the IP range. If you select **Deny login**, users outside of the trusted IP range will be unable to access Viva Engage through clients.

## Set password policies

1. In the Viva Engage admin center, go to **Content and Security** \> **Security Settings**.

2. In the **Password Policies** section, specify the password length and complexity requirements, and when passwords need to be changed.

    If you change any password settings and select **Save**, users whose passwords don't meet these requirements are prompted to change their passwords upon their next sign-in. If you select **Force All Users to Change their Passwords Immediately** all users must change their passwords the next time they sign in, regardless of any password requirement changes.

    > [!NOTE]
    > External networks do not have the ability to configure password policies. This prevents users from being faced with multiple password strength requirement policies if they participate in External Networks. Users must comply with the password strength policies of their home network.
  
## Configure security settings for all external networks

1. In Microsoft 365, go to **Admin** \> **Viva Engage** \ **External Networks**. Or, in Viva Engage, select your home network settings icon, and go to **Network Admin** \> **External Networks**.

2. Select **External Networks**.
  
3. Select ways to limit access to all external networks:

   - **Require admin approval for users to join other companies' external networks:** When you select this box, users must request approval before they join external networks created by other organizations.

   - **Disable Related External Networks directory:** The Related Networks directory is a list of external networks to which one or more of your users belong. Selecting this box removes this directory from the External Network page.

   - **Disable our External Networks directory:** The Our External Networks directory lists all external networks attached to your Viva Engage network. Select this if you want to prevent users from viewing (and requesting to join) external networks.
  
## Prevent intellectual property from being shared with external participants and on external networks

1. In the Viva Engage admin center, go to **Content and Security** \> **Security Settings**.

2. In the **External Messaging** section, select the option that makes sense for your organization.

## Enforce Microsoft 365 (formerly Office 365) identity in Viva Engage

1. In the Viva Engage admin center, go to **Content and Security** \> **Security Settings**.

2. In the **Office 365 Identity Enforcement** section, select **Enforce Office 365 identity in Viva Engage**.

    For information about this setting, see [Enforce Microsoft 365 identity for Viva Engage users](../configure-your-viva-engage-network/enforce-office-365-identity.md)

## Learn the status of Microsoft 365 Connected Groups

1. In the Yammer admin center, go to **Content and Security** \> **Security Settings**.

2. Look in the **Office 365 or Microsoft 365 Connected Viva Engage Groups** section to see the status for your connected groups.
