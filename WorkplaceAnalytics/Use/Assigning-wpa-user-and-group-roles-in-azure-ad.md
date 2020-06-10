---

title: Assign Workplace Analytics user roles and groups in Azure Active Directory (AAD)
description: How to assign Workplace Analytics roles and group permissions in Azure Active Directory (AAD)
author: paul9955
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin

---

# Assign Workplace Analytics user and group roles in Azure Active Directory

To add Workplace Analytics user roles in Azure Active Directory (Azure AD):

1. Log in to your tenant's [Azure Active Directory admin center](https://aad.portal.azure.com).

2. In the left navigation menu, select **Enterprise Applications**.

    ![Enterprise Applications](../images/WpA/Use/enterprise-applications-1.png)

3. In the Application Type drop-down menu, select **All Applications** and select **Apply**.

    ![Select Apply](../images/WpA/Use/apply-button_90.png)

4. In the search field, type "workplace" and then press **Enter**.

5. In the search results, select **Workplace Analytics**.

    ![All Applications](../images/WpA/Use/all-applications-2.png)

6. In the Overview section, select **Total Users**.

    ![Total users](../images/WpA/Use/total-users-3.png)

7. In the Users and groups window, select **Add user**.

8. Under Add Assignment, select **Users and groups**.

   ![Add user](../images/WpA/Use/add-user-4.png)

9. In the search field under Users and Groups, type the name of the user to assign the required permissions and then press **Enter**. The user name will appear under the search field.

10. Select the name and then select the blue **Select** button.

      ![Select user](../images/WpA/Use/select-user-5.png)

    Users and groups confirms that the new user has been selected.

       ![Add assignment](../images/WpA/Use/user-selected-6.png)

11. Under Add Assignment, select **Select Role** to choose the role you want to assign the selected user.

      ![Select role](../images/WpA/Use/select-role-7.png)

12. From the list that appears, select one of the following roles:

    * Analyst
    * Analyst (Limited Access)
    * Administrator
    * Program manager

    ![Select role](../images/WpA/Use/select-role-8.png)

13. Select the **Select** button.

14. Finally, select the **Assign** button.

     ![Assign role](../images/WpA/Use/assign-role-9.png)

    Users and groups now displays the user's new assigned Workplace Analytics role.

       ![Role assignment confirmation](../images/WpA/Use/new-role-assigned-10.png)

Allow time for the user account to replicate. The user can now log in to [Workplace Analytics](https://workplaceanalytics.office.com) with the new role and its corresponding access permissions.

## Assign roles to groups

You can also assign roles to groups, which means that you are assigning the access permissions associated with that role to the group. Any users who are assigned to that group then automatically become members of the group and receive the same permissions that are assigned to that role.

To assign users and roles to Workplace Analytics groups, the steps are similar to those for assigning users, as previously described in steps 9 through 14. In that same process, where you add the name of a user in step 9, at the same time, you can also add a group and assign it a role. The only difference is that instead of a user name, you substitute the name of your group, then select the group and assign a role to it.

   ![Select group](../images/WpA/Use/select-group-b.png)

If you have not yet created a Workplace Analytics group in Azure AD, and want to do so, see the article on creating a group in **Related topics**.

## FAQ

**When would you assign a role to a group rather than to an individual user?**

It depends on the situation or on your company's policy, but generally speaking, the reason for choosing between one method and another is usually efficiency. In a smaller company, if a few people will be assigned Workplace Analytics roles, it can be convenient to assign user roles individually, especially if such roles are unlikely to change.

However, in a larger company where the number of users required for the same role is significant, for example, Program Managers, it is more efficient to assign a role to a group, and then add users to the group, because groups are easier to manage and audit.

## Related topics

* [User roles](../use/user-roles.md)
* [Create a group and add members in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)
* [Environment requirements for Workplace Analytics](../setup/environment-requirements.md)
