---
title: Data handling in Viva Sales 
description: Know how data is handled in Viva Sales 
ms.date: 08/01/2022
ms.topic: article
ms.service: viva
author: sbmjais
ms.author: shjais
manager: shujoshi
---


# Data handling in Viva Sales 

This article gives you an overview of how data is handled in Viva Sales.

Viva Sales is built on the [Microsoft Power Platform](https://powerplatform.microsoft.com/). Viva Sales data is stored in [Dataverse](/powerapps/maker/common-data-service/data-platform-intro) in addition to the connected CRM.

## Data retention 

Since Viva Sales data is stored in [Dataverse](/powerapps/maker/common-data-service/data-platform-intro), data retention policies differ from other Microsoft 365 applications and non-Dynamics 365 CRM solutions. For example, when your Microsoft 365 subscription ends, your data is retained for 90 days before it's automatically deleted (in accordance to [Microsoft 365 data retention policies](/microsoft-365/compliance/retention-policies)). However, if you use Viva Sales, that data isn't automatically deleted 90 days after your subscription ends.  

## Viva Sales, Dataverse, and your CRM

When Viva Sales is connected to Dynamics 365, Viva Sales data is stored with the Dynamics 365 Sales Dataverse instance.

When Viva Sales is connected to a non-Dynamics 365 CRM, a default Dataverse instance specific to Viva Sales is provided to your tenant. Viva Sales data is stored in the default instance in addition to your CRM. 

You can find the name and details of your default Dataverse instance named **msdyn_viva** in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/).

:::image type="content" source="media/ppac-admin-center.png" alt-text="Default Dataverse instance in Power Platform admin center":::

## Delete Viva Sales data 

If you need to delete Viva Sales data (for example, delete data for a specific user), you can choose to [manually delete it](/power-platform/admin/remove-user-personal-data). 

### See also

[Introduction to Microsoft Viva Sales](introduction.md)<br>
[Install Viva Sales](install-viva-sales.md)