---
ms.date: 09/30/2024
title: Assign roles
description: Learn how to assign Insights Administrator, Insights Analyst, and Insights Business Leader roles to users in your organization
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva-insights
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---
# Assign roles

>[!Note]
>This article covers how to assign the Insights Administrator, Insights Analyst, and Insights Business Leader roles to users.
For specific information about what each role can do with Viva Insights, refer to [Roles in Viva Insights](../../use/user-roles.md).
>
>Enabling manager and leader access to insights is a different process. Insights Administrators enable this access through [Manager settings](./manager-settings.md).

>[!Important]
>Early next year, the **Business Leader** role will no longer be available. At that point, people who previously had this role won’t be able to access organizational insights. To provide employees access to organizational insights, assign them delegate access instead. [Learn more about how delegate access works](..//..//org-team-insights/delegate-access.md). 

## Assign Viva Insights roles

People can work with Microsoft Viva Insights only after the Privileged Role Administrator assigns them one of these roles: **Insights Administrator**, **Insights Analyst**, or **Insights Business Leader**.

The Microsoft 365 admin assigns roles through the Microsoft admin center, unless your organization uses Privileged Identity Management (PIM). In that case, your organization might choose to have the Privileged Role Administrator assign roles with Microsoft Entra PIM.

### Assign roles in the Microsoft admin center  

These steps must be performed by the Microsoft 365 Global Administrator.

1. Go to the [setup tab](https://admin.microsoft.com/adminportal/home#/featureexplorer) and select **Microsoft Viva**, then **Viva Insights**. You'll need to enter your credentials if you're not already signed in.
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

<a name='assign-roles-with-azure-active-directory-privileged-identity-management'></a>

### Assign roles with Microsoft Entra Privileged Identity Management

*Applies to: Privileged Role Administrator*

If your organization uses PIM, you might choose to assign roles in Microsoft Entra PIM rather than the Microsoft admin center. To learn how to assign roles through PIM, go to [Assign Microsoft Entra roles in PIM - Microsoft Entra](/azure/active-directory/privileged-identity-management/pim-how-to-add-role-to-user). 

Here are the role names to search for:

* Insights Administrator
* Insights Analyst
* Insights Business Leader

#### About assignment and user types

Assignment type (eligible or active) and assignment duration (permanent or time-bound) are up to you. If you assign a user as eligible, they’ll need to perform an action every time they want to use their role, like doing a multi-factor authentication check or requesting approval. Active assignments don’t require these actions. If you assign a time-bound duration, a user’s role access expires at the end of a specified timeframe. Permanent assignments don’t expire.

To learn more about PIM, how to approve or deny role requests, and extend and renew assignments, go to [What is Microsoft Entra Privileged Identity Management?](/azure/active-directory/privileged-identity-management/pim-configure).

Within a few days of being assigned a Viva Insights role, Insights Administrators and Insights Business Leaders users get an email about available product features based on their role and service plan.

## Assign roles to groups

### Assign roles in the Microsoft admin center

You as the Microsoft 365 global admin can also assign roles to groups, which means you're assigning access permissions associated with that role to the group. Any people assigned to that group automatically receive the same permissions.

To assign Viva Insights roles to a group, the steps are similar to those for assigning roles to individuals, as described in [Assign Viva Insights roles](#assign-viva-insights-roles). In that process, when prompted to select a name, select a group name instead. Then, assign a role to the selected group. For more details, refer to [Manage a group in the Microsoft 365 admin center](/microsoft-365/admin/create-groups/manage-groups).

<a name='assign-roles-with-azure-active-directory-privileged-identity-management'></a>

### Assign roles with Microsoft Entra Privileged Identity Management

*Applies to: Privileged Role Administrator*

Assigning roles to groups in PIM works the same way as assigning roles to groups in the Microsoft admin center. In PIM, select the group name you want to assign permissions to.

When you assign members or owners as active in PIM, they don't need to perform any activations to use their roles, and they can use all privileges assigned to their role at all times. 


### When do I assign a group instead of an individual a specific role?

It depends on the situation and your company's policies. However, the main reason for choosing between one method and another is usually efficiency. In a smaller company, if you only need to assign a few people a Viva Insights role, it's more convenient to assign individual people their applicable roles, especially if their roles are unlikely to change.
However, in a larger company where the number of people required for the same role is significant, it’s more efficient to assign the role to a group, and then add users to the group because groups are easier to manage and audit.


## Verify role assignments

To find out which roles are assigned for Viva Insights, go to the [setup tab](https://admin.microsoft.com/adminportal/home#/featureexplorer) in the Microsoft admin center and select **Microsoft Viva**, then **Viva Insights**. Under **Add-on Plan**, select which role you want to verify. 

Alternately, go to [Role assignments](https://go.microsoft.com/fwlink/p/?linkid=2097861) and search for "Insights" to see a person or group's assigned Insights role(s).

## More about assigning roles

### How many people can I assign roles to?

As many as you need to. The number of people you assign Viva Insights roles to depends on how large your organization is and how you need to manage organizational data. For example, the number of analysts you assign should be as many your organization needs to analyze data. 

### Can I assign somebody to more than one role?

Yes. It's up to your organization to choose who’s assigned which role. For example, one person can be both an Insights Administrator and an Insights Analyst. However, it's a best practice to assign the admin and analyst roles to different people to prevent any misuse of or external linking of organizational data with collaboration metrics.
In the Microsoft admin center, you can assign multiple roles to one account, but you can assign only one role at a time.

### How can I assign the manager role?

Manager isn't technically a role that can be assigned. The Insights admin can enable them access to their group insights through [Manager settings](./manager-settings.md) within the advanced insights app.

## Next steps

> [!div class="nextstepaction"]
> [Configure manager settings](./manager-settings.md)

*Applies to: Insights Administrator*
