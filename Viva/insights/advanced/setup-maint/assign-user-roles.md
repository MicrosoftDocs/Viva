---
title: Assign user roles for Viva Insights
description: Learn how to assign user roles for Viva Insights 
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---
# Assign user roles for Viva Insights

People can work with Microsoft Viva Insights only after they've been assigned a role. See [Roles in Viva Insights](../../use/user-roles.md) for details on what each role can do with Viva Insights. Refer to the following sections for information about assigning roles:

* [Assign Viva Insights roles](#assign-viva-insights-roles)
* [Assign roles to groups](#assign-roles-to-groups)
* [Verify role assignments](#verify-role-assignments)
* [Role assignment FAQ](#role-assignment-faq)

>[!Note]
>The Insights admin enables people managers access to group insights through [Manager settings](./manager-settings.md).

## Assign Viva Insights roles

*Applies to: [Microsoft 365 global admin](/microsoft-365/admin/add-users/about-admin-roles)*

To assign users to a Viva Insights role, including **Insights Administrator**, **Insights Analyst**, and **Insights Business Leader**:

1. In the Microsoft admin center, go to the [setup tab](https://admin.microsoft.com/adminportal/home#/featureexplorer) and select **Microsoft Viva**, then **Viva Insights**. You'll need to enter your credentials if you're not already signed in.
1. Under **Add-on Plan**, select the role you want to assign: **Insights Admin**, **Insights Business Leader**, or **Insights Analyst**.
:::image type="content" source="../images/assign-admin-leader-analyst.png" alt-text="Screenshot that shows the Viva Insights admin page with options in the Add-on Plan section highlighted." lightbox="../images/assign-admin-leader-analyst.png":::
1. Select **Add users** or **Add groups**. We discuss group role assignment in [Assign roles to groups](#assign-roles-to-groups).
1. Select users(s) or groups(s), then select **Add**.
:::image type="content" source="../images/assign-users1.png" alt-text="Screenshot that shows the Add users option with three names.":::

Alternatively, instead of following steps 1-4 above, you can add users from the **Role assignments** page:

1. Go to the [Role assignments page](https://go.microsoft.com/fwlink/p/?linkid=2097861) in the [Microsoft 365 admin center](https://admin.microsoft.com/AdminPortal/home). You'll need to enter your credentials if you're not already signed in.
1. Search for **Insights**, and then select the applicable Insights role to assign a user.
1. Select **Assign** > **Add**.
1. Enter the username, and then select the user from the list of suggestions. Optionally, add multiple users until you're done.
1. Select **Save**.

Within a few days of being assigned a Viva Insights role, the **Insights Administrator** and **Insights Business Leader** users get an email about available product features based on their role and service plan.

## Assign roles to groups

You can also assign roles to groups, which means you're assigning access permissions associated with that role to the group. Any people assigned to that group automatically receive the same permissions.

To assign Viva Insights roles to a group, the steps are similar to those for assigning roles to individuals, as described in [Assign Viva Insights roles](#assign-viva-insights-roles). In that process, when prompted to select a name, select a group name instead. Then, assign a role to the selected group. For more details, refer to [Manage a group in the Microsoft 365 admin center](/microsoft-365/admin/create-groups/manage-groups).

## Verify role assignments

To find out which roles are assigned for Viva Insights, go to the [setup tab](https://admin.microsoft.com/adminportal/home#/featureexplorer) in the Microsoft admin center and select **Microsoft Viva**, then **Viva Insights**. Under **Add-on Plan**, select which role you want to verify. 

Alternately, go to [Role assignments](https://go.microsoft.com/fwlink/p/?linkid=2097861) and search for "Insights" to see a person or group's assigned Insights role(s).

## Role assignment FAQ

### When do I assign a group instead of an individual a specific role?

It depends on the situation and your company's policies. However, the primary reason for choosing between one method and another is usually efficiency. In a smaller company, if you only need to assign a few people a Viva Insights role, it's more convenient to assign individual people their applicable roles, especially if their roles are unlikely to change.

However, in a larger company where the number of people required for the same role is significant, such as for program managers, it is more efficient to assign the role to a group, and then add users to the group because groups are easier to manage and audit.

### How is the people manager role assigned?

People manager isn't technically a role that can be assigned. The Insights admin can enable them access to their Group insights through [Manager settings](./manager-settings.md) within the advanced insights app.

## Related topics

* [Roles in Viva Insights](../../use/user-roles.md)
* [Manager settings](./manager-settings.md)
* [About admin roles](/microsoft-365/admin/add-users/about-admin-roles)
