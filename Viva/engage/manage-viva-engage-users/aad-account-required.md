---
title: "Microsoft Entra credentials are required for Viva Engage Enterprise sign in"
f1.keywords:
- NOCSH
ms.author: elizapo
author: ToniSFrench
manager: elizapo
ms.date: 8/23/2023
audience: Admin
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
ms.localizationpriority: medium
search.appverid:
- MET150
- MOE150
- YAE150
ms.custom: Adm_Yammer
description: "As of January 31, 2019, Viva Engage Enterprise users can no longer use legacy (Yammer) credentials. If self-service signup is enabled, users are automatically prompted to change their password."
---

# Microsoft Entra credentials are required for Viva Engage Enterprise sign-in 
 
Starting January 31, 2019, Viva Engage Enterprise users with legacy credentials (instead of a Microsoft Entra account) will be redirected to a new sign-up flow. After they complete the required steps, a Microsoft Entra account with no Office 365 licenses is automatically created for the user. This process is called self-service signup.  

- After changing their password, these users can access your Viva Engage network, and have access to all their groups and data. 
- After the Microsoft Entra account is created for a user, admins can manage the user from the Microsoft 365 admin center.  

As a Viva Engage admin, if you want to prevent users who don’t have Office 365 licenses from accessing your Viva Engage network, you can choose to enforce Office 365 licenses. For instructions, see [Enforce Office 365 identity for Viva Engage users](../configure-your-viva-engage-network/enforce-office-365-identity.md).
 
## Why is Viva Engage doing this? 

Several existing and upcoming features require both Microsoft Entra credentials and a central place to manage users for Microsoft 365 apps, Office 365 apps, and Microsoft 365 connected groups.
 
### Notify users that they're required to create a new password.  

Users must create a new password the first time they try to log in after January 31, 2019. After they create a new password and validate their email address, they 'll use their new credentials to sign in. 

Other than this requirement, the change is transparent to users. Their data is unaffected. Their groups, external networks, and content are the same as before the change.

**Identify affected users and notify them**  

To identify users you need to notify, follow the instructions in [Audit Viva Engage users](audit-users-connected-to-office-365.md) to get contact information for users not using Microsoft Entra credentials.

## FAQ 

**Q: Will this change users' experience?**

A: After January 31, 2019, the user's experience changes:
**If self-service signup is enabled**, a user with legacy credentials is asked to create a new password and validate their email address. After that, they must use their newly created Microsoft Entra credentials each time they sign in to Viva Engage. 

**If self-service signup isn't enabled**, a user with legacy credentials can't sign in after January 31 until the Microsoft 365 or Office 365 admin manually creates a Microsoft Entra account for them.

**Q: What happens if as an admin, I don’t take action by January 31, 2019?** 

A: If self-service sign-up is enabled, users are redirected to the self-service signup flow. They can create their own password, even if no action is taken. However, we recommend letting the users know in advance so they are not surprised by the change. 

If self-service signup is not enabled, users using legacy Viva Engage credentials can't log in after January 31 unless you manually create a Microsoft Entra account for them. 

**Q: Will this impact guest users?** 

A: No, this change doesn't impact guest users.

**Q. Do I have to buy an Office 365 license for each user that currently doesn't have a Microsoft Entra account?**

A. No. After January 31, 2019, you must create the Microsoft Entra account yourself. No Office 365 license is required.
