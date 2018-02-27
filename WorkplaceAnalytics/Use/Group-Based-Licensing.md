---
# Metadata Sample
# required metadata

title: Group-based licensing for Workplace Analytics
description: This article describes how to set up group-based licensing in Workplace Analytics.
author: rodonahu
ms.author: rodonahu
ms.date: 01/19/2018
ms.topic: get-started-article
ms.prod: wpa
---

# How to manage licenses for products with prerequisites
Some Microsoft Online products that you acquire are "add-ons" - they require a prerequisite service plan to be enabled for a user, or a group, before they can be assigned. With group-based licensing, the system requires that both the prerequisite and add-on service plans be present on the group, to ensure that any users who are added to the group can received a valid service plan assignment. Let's consider the following example:

![Admin Center](~/Images/WPA/use/aad_group1.png)

Microsoft Workplace Analytics is an add-on product. It contains a single service plan with the same name and Id of WORKPLACE_ANALYTICS. This service plan can only be assigned to a user, or group, when one of the following prerequisites are also assigned:
- Exchange Online (Plan 1) (Id: EXCHANGE_S_STANDARD) or,
- Exchange Online (Plan 2) (Id: EXCHANGE_S_ENTERPRISE).

If we try to assign this product on its own to a group, the portal will return an error - clicking on the error notification shows the following details:

![Admin Center](~/Images/WPA/use/aad_group2.png)

Clicking on the details shows the following error message:
> _License operation failed. Make sure that the group has necessary services before adding or removing a dependent service. **The service Microsoft Workplace Analytics requires Exchange Online (Plan 2) to be enabled as well.**_

In order to assign this add-on license to a group, we have to ensure that the group also contains the pre-requisite service plan. We could update an existing group that already contains the full Office 365 E3 product with Exchange Online present.
It is possible to create a standalone group that contains only the minimum required products to make the add-on work - it can be used to license only the selected users for the add-on product. In this example we have assigned the following products to the same group:

- Office 365 Enterprise E3, with only the Exchange Online (Plan 2) service plan enabled
-	Microsoft Workplace Analytics

The resulting assignment is valid and was applied to the group. From now on, any users added to this group will consume 1 license of the E3 product and one license of the Workplace Analytics product. At the same time those users can be members of another group that gives them the full E3 product and they will still consume only one license for that product.

>[!Tip]
>You can create multiple groups, for each prerequisite service plan. For example, if you use both Office 365 Enterprise **E1** and Office 365 Enterprise **E3** for your users, you could create two groups to license Microsoft Workplace Analytics; one using E1 as a prerequisite and the other using E3. This will allow you to distribute the add-on to E1 and E3 users without consuming additional licenses.
