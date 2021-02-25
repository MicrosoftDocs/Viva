---
ROBOTS: NOINDEX,NOFOLLOW
title: Assign licenses for Workplace Analytics insights
description: Learn how to assign licenses through the Microsoft 365 admin center or Azure AD to people who want to use Workplace Analytics insights
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: none 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Assign licenses

*This experience is only available through private preview at this time.*

You must be able to sign in as a global Microsoft 365 admin to use the Microsoft admin center to [assign licenses to one or more individual users](#to-assign-licenses-to-individual-users) who subscribe to a Microsoft or Microsoft 365 E5 or E3 plan whose [geo location is North America](https://docs.microsoft.com/microsoft-365/enterprise/microsoft-365-multi-geo#microsoft-365-multi-geo-availability).

Alternatively, you can assign licenses as follows:

* [Assign licenses to one or more security groups](#to-assign-licenses-to-security-groups) as an Azure Active Directory global admin
* [Assign licenses with PowerShell](assign-licenses-pshell.md) as a global Microsoft 365 admin

## To assign licenses to individual users

1. In the **Microsoft admin center**, select **Active users**, and then do one of the following to assign licenses to one user or for multiple users at the same time.

   **For one user**:
   1. In **Active users**, select the user from the list.
   2. Select **Licenses and Apps**.
   3. Select the check box for **Microsoft Workplace Analytics Insights**.
   4. Select **Save changes**, as shown in the following graphic.

   ![Assign one user a license](./images/assign-one-license.png)

   **For multiple users**:
   1. In **Active users**, select the checkbox next to the users you want to assign licenses.
   2. Select the **Ellipsis** (**...**) icon next to **Reset password**, and then select **Manage product licenses**.
   3. Select **Assign more**, and then select the check box for **Microsoft Workplace Analytics Insights**.
   4. Select **Save changes**.

   ![Assign multiple users licenses](./images/assign-multiple-licenses.png)

2. These licenses are assigned right away to the selected users.

## To assign licenses to security groups

1. In **Microsoft Azure Active Directory**, select **Licenses** under **Manage**.
2. In **Overview**, select **All products**, and then select the check box for **Microsoft Workplace Analytics Insights**.

   ![Assign licenses in Azure Active Directory](./images/assign-licenses-add.png)

3. Select **Assign**, and then select **Users and groups** to open the right pane.
4. Search for one or more group names, select each group from the list to add it to the **Selected items** list, and then choose **Select**.

   ![Add one or more groups for licensing](./images/add-group-license.png)

5. Select **Assignment options** to open the right pane, confirm that both **Microsoft Workplace Analytics Insights** are set **On**, and then select **OK**.

   ![Keep both options set to On](./images/keep-options-on.png)

6. It can take a few minutes up to 24 hours for the license assignments to update to the server, which is based on your specific server settings.

> [!Note]
> If you are assigning licenses to a group that has more people than you have licenses for, the tool will assign users as listed in the group up to the number of available licenses, and then you'll see an error message about how many in the group have and do not have licenses.

## Related topics

* [Assign roles](assign-roles.md)
* [Setup overview](./setup.md)
