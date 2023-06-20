---
title: "Microsoft Viva - Feature access management"
ms.reviewer: elizapo
ms.author: elizapo
author: lizap
manager: pamgreen
ms.date: 7/01/2023
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
localization_priority: Priority
ms.custom:
ms.collection:  
- M365initiative-viva
- m365solution-overview
- highpri
- tier1
search.appverid:
- MET150
description: "Control who can access features in Microsoft Viva"
---

# Control access to features in Viva

One of the key tools you have to manage privacy and compliance across your organization is by controlling who has access to what - to resources and apps. Viva uses Microsoft 365 users and groups to enable role-based authorization - you control which roles or groups or specific users can access which Viva apps and what they can do inside those apps. For example, someone with the knowledge manager roles in Viva Topics can review and approve content, while someone with the user role consumes that content but cannot change it. 

Feature access management in Viva lets you further fine tune access by granting or restricting access to specific features within Viva apps through the use of access policies. Imagine, for example, that a local works council has restricted the use of X in an area where you have employees. Your choice is either to not use the app at all or to disable that single feature for users in that locale. Features access management lets you do this.

> [!NOTE]
> Not all features in all Viva apps support feature access management. And for those that do, restricting the use of one feature might impact the functionality of other features in the app. Be sure to check the app documentation on the specific feature to understand the implications of disabling or enabling access to a feature.

## Create an access policy for a Viva feature
Use the following PowerShell cmdlet to create an access policy for a Viva feature:

```powershell
cmdlet name and syntax
```

This example creates an access policy that restricts access to the Reflection feature in Viva Insights. It does ....

```powershell
example cmd string
```

## More resources

[Microsoft Viva Privacy](/Viva/viva-privacy)

[Microsoft Viva Security](/Viva/microsoft-viva-security)

[Viva admin roles and tasks](/viva/microsoft-viva-admin-roles)
