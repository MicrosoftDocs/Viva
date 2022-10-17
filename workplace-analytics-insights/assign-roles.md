---
ROBOTS: NOINDEX,NOFOLLOW
title: Assign user roles for Microsoft Viva Insights
description: Learn how to assign roles to people who want to view Microsoft Viva Insights (synonymous with Workplace Analytics insights in Microsoft 365)
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: null 
ms.service: workplace-analytics
manager: scott.ruble
audience: Admin
---

# Assign roles

After assigning licenses, you need to assign roles to the people who want to view and use Microsoft Viva Insights in Microsoft Teams. You can assign users the role of **Insights Administrator** or **Insights Business Leader** in Microsoft 365 admin center.

To assign roles:

1. Sign in as a global admin to your tenant's [Microsoft 365 admin center](https://admin.microsoft.com/adminportal).
2. In the left navigation, select **Roles**, and then select the **Azure AD** tab.
3. In the search field, enter **Viva Insights**.
4. In the search results, select a role:

   * **Insights Administrator** - Gets full access to the Viva Insights app and read access to Azure AD properties, monitors, service health, and managed service requests.
   * **Insights Business Leader** - Gets read access to the Viva Insights app reports and data.

5. Select **Assign admins**, and then select **+ Add**.
6. In the search field for **Who do you want to assign to this role**, type the first few letters of a name, and then select the name from the list. The admin center limits you to assigning 20 names at a time. However, you can repeat these steps to assign more users a role.

    ![Assign the selected role.](./images/assign-role.png)

7. Select **Save** to assign the listed users the role.

>[!Note]
>The Microsoft 365 admin center references all roles as admins even though not all roles are admins.

## Access to Viva Insights

After assigning licenses, the data for Insights might take up to a week to process and become available. After [assigning roles](assign-roles.md) and allowing for data processing, refer your organization's leaders to [Viva Insights introduction](./intro.md) to learn more about how to use them.

## Related topics

* [Set up Viva Insights](setup.md)
* [Assign admin roles to Microsoft 365 user accounts with PowerShell](/microsoft-365/enterprise/assign-roles-to-user-accounts-with-microsoft-365-powershell)
