---
title: Assign user or group roles
description: How to assign roles for Advanced insights with Microsoft Viva Insights
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Assign user roles

Do the following to assign roles to users in Azure Active Directory (AD) for Microsoft Viva Insights in the advanced insights app.

1. Sign in to your tenant's [Azure Active Directory admin center](https://aad.portal.azure.com).
2. In the left navigation menu, select **Enterprise Applications**.

    ![Enterprise Applications.](../images/WpA/Use/enterprise-applications-1.png)

3. In the Application Type drop-down menu, select **All Applications** and select **Apply**.

    ![Select Apply.](../images/WpA/Use/apply-button_90.png)

4. In the search field, type "workplace analytics" and then press **Enter**.
5. In the search results, select **Workplace Analytics**.

    ![All Applications.](../images/WpA/Use/all-applications-2.png)

6. In the **Overview** section, select **Total Users**.

    ![Total users.](../images/WpA/Use/total-users-3.png)

7. In the **Users and groups** window, select **Add user**.

   ![Add user.](../images/WpA/Use/add-user-4.png)

8. Under **Add Assignment**, select **Users and groups**.
9. In the search field for **Users and Groups**, type the name of the user to assign the required permissions and then press **Enter**. The user name will appear under the search field.
10. Select the name and then select the blue **Select** button.

      ![Select user.](../images/WpA/Use/select-user-5.png)

    **Users and groups** shows that the new user is selected.

       ![Add assignment.](../images/WpA/Use/user-selected-6.png)

11. Under **Add Assignment**, select **Select Role** to choose the role you want to assign the selected user.

      ![Select a role.](../images/WpA/Use/select-role-7.png)

12. From the list that appears, select one of the following roles:

    * Analyst
    * Analyst (Limited Access)
    * Administrator
    * Program manager

    ![Select role.](../images/WpA/Use/select-role-8.png)

13. Select the **Select** button.
14. In **Add Assignment**, select **Assign** (bottom of page). After a few seconds, a message in the upper right shows a successful role assignment, such as the following that shows one role assigned to one user.

     ![Role assignment confirmation.](../images/WpA/Use/new-role-assigned-10.png)

15. (Optional) Add additional roles:

    * To add another role to the _same_ user, repeat steps 11-14.
    * To add roles to _other_ users, repeat steps 7-14.

It might take up to 24 hours for changes to be saved in the system. The user can now sign in to [the advanced insights app](https://workplaceanalytics.office.com)(if that link doesn't work, try [this link instead](https://workplaceanalytics-eu.office.com/)) with their new role and its corresponding access permissions.

## Assign roles to groups

You can also assign roles to groups, which means that you are assigning the access permissions associated with that role to the group. Any users who are assigned to that group then automatically become members of the group and receive the same permissions that are assigned to that role.

To assign users and roles to the advanced insights group, the steps are similar to those for assigning users, as described in the previous steps. In that same process, where you add a username, you can enter a group and assign it a role.

   ![Select group.](../images/WpA/Use/select-group-b.png)

If you have not yet created an Advanced insights group in Azure AD, and want to do so, see [Create a group and add members in Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).

## FAQ

**When would you assign a role to a group rather than to an individual user?**

It depends on the situation or on your company's policy, but generally speaking, the reason for choosing between one method and another is usually efficiency. In a smaller company, if a few people will be assigned Viva Insights roles, it can be convenient to assign user roles individually, especially if such roles are unlikely to change.

However, in a larger company where the number of users required for the same role is significant, such as for Program Managers, it is more efficient to assign a role to a group, and then add users to the group, because groups are easier to manage and audit.

## Related topics

* [User roles](../use/user-roles.md)
* [Environment requirements for advanced insights](/viva/insights/setup/environment-requirements?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)
* [People manager settings](manager-settings.md)
