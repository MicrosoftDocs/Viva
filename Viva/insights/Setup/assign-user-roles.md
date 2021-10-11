---

title: Assign roles with Azure AD
description: How to assign roles for Microsoft Viva Insights in Workplace Analytics with Azure Active Directory
author: madehmer
ms.author: v-mideh
ms.topic: article
ms.localizationpriority: medium 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Assign roles with Azure AD

People can work with Microsoft Viva Insights  or Workplace Analytics only after they've been assigned a role, which can be admin, analyst, limited analyst, or program manager. See [User roles](../use/user-roles.md) for details on what each role can do with Viva Insights or Workplace Analytics. Use the following steps to assign Viva Insights or Workplace Analytics roles to individual people or to groups:

* [Assign roles to individuals](#assign-roles-to-users)
* [Assign roles to groups](#assign-roles-to-groups)
* [Verify role assignments](#verify-role-assignments)
* [Role assignment FAQ](#role-assignment-faq)

## Assign roles to users

**Owner** - Azure Active Directory [Privileged Role Administrator](/azure/active-directory/roles/permissions-reference)

1. Sign in to your tenant's [Azure Active Directory admin center](https://aad.portal.azure.com). 

2. In the left navigation menu, select **Enterprise applications**:

   ![Enterprise applications.](../images/wpa/setup/enterprise-apps.png)

3. In **Enterprise applications | All applications**, select **Application Type** > **All Applications**:

   ![Application types.](../images/wpa/setup/ent-all-apps-3.png)

4. In the search field, enter **viva**, and then press **Enter**.
5. In the search results, select **Viva Insights** or **Workplace Analytics**.  

6. In the **Viva Insights or Workplace Analytics | Overview**, under **Getting Started**, select **Assign users and groups**:

   ![Overview page.](../images/wpa/setup/wpa-overview.png)  

7. In the Viva Insights or Workplace Analytics **Users and groups**, select **Add user**:

   ![WpA users and groups.](../images/wpa/setup/wpa-users-and-groups.png)  

> [!Note] 
> In the **Users and groups** section, you'll see **None Selected**. 

8. In **Add Assignment**, select **Users and groups**:
   
   ![Select Users and groups.](../images/wpa/setup/select-users-and-groups-4.png)

9. Under **Users and groups** (on the right side of the page), identify the user to whom you want to assign a role. Start typing that person's user identifier (such as their display name or their User Principal Name) in the search field and then select their identifier in the results list. After you select the person, their identifier appears on the right under **Selected items**: 
   
   ![Selected items.](../images/wpa/setup/selected-items.png)
   
   In the **Users and groups** section, the count of selected users has changed to 1:

   ![Add Assignment + 1.](../images/wpa/setup/add-assignment-plus-1.png)

   > [!Note]
   > You can repeat this step to add one or more additional users, if you intend to assign the same role to them. 

10. In **Add Assignment**, select **Select Role** to open the **Select Role** area on the right side of the page: 

    ![Select role.](../images/wpa/setup/select-role.png)

11. Select one of the following roles:  

   * Analyst
   * Analyst (Limited Access)
   * Administrator
   * Program manager

   > [!Note]
   > The Group manager role might appear (as a disabled option) in some tenants that were provisioned earlier.  

   The role you selected appears at the bottom of the **Select Role** section:

   ![Selected role.](../images/wpa/setup/selected-role.png)

   The role also appears under **Add Assignment** in the **Select Role** section:

   ![Added role.](../images/wpa/setup/add-assignment-select-53.png)

> [!Note]
> To change the role to assign to this user, repeat **Steps 10-11** and select a different role in **Step 11**.

12. In **Add Assignment**, select **Assign** (bottom of the page):
 
   ![Assign.](../images/wpa/setup/assign-button.png)

   After a few seconds, a message in the upper right shows a successful role assignment:

   ![Assignment succeeded.](../images/wpa/setup/assignment-succeeded.png)

You have now assigned one role to one user.  

13. (Optional) You can now assign additional roles, either to the same user or to different users. 

    * **Same user, additional role** - To add another role to the same user, repeat **Steps 7-12** and in **Step 9**, be sure you select the correct user, and then select the additional role in **Steps 10-11**.

    * **Other users** - To select other users and assign roles to them, repeat **steps 7-12** and in **Step 9-11**, be sure you select the new user and the applicable role.

To check the role assignments that a user currently has, see [Verify role assignments](#verify-role-assignments).

## Assign roles to groups

You can also assign roles to groups, which means that you are assigning access permissions associated with that role to the group. Any users who are assigned to that group automatically receive the same permissions.

> [!Note]
> The groups that you can assign Viva Insights or Workplace Analytics roles are Azure Active Directory security groups. For more information about working with this kind of group, see [Manage app and resource access using Azure Active Directory groups](/azure/active-directory/fundamentals/active-directory-manage-groups). 

To assign users and roles to Viva Insights or Workplace Analytics groups, the steps are similar to those for assigning users, as previously described in steps 9 through 12 under [Assign roles to users](#assign-roles-to-users). In that process, where you name and select a user in step 9, instead name and select a group, and then assign a role to the selected group.

   ![Select group.](../images/WpA/Use/select-group-b.png)

If you have not yet created a Viva Insights or Workplace Analytics group in Azure Active Directory, and want to do so, see [Create a group and add members in Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).

## Verify role assignments

Use the following steps to see what roles have been assigned to a user.  

1. On the **Viva Insights | Users and groups** page, start typing the user identifier. As you do so, the list of users and groups filters to contain the name you're typing.  
2. Find the user in the list. In the **Role assigned** column, you can see the user’s role (or roles).

## Role assignment FAQ

**When would you assign a role to a group rather than to an individual user?**

It depends on the situation or on your company's policy, but the reason for choosing between one method and another is usually efficiency. In a smaller company, if only a few people will be assigned Viva Insights or Workplace Analytics roles, it can be convenient to assign user roles individually, especially if such roles are unlikely to change.

However, in a larger company where the number of users required for the same role is significant &mdash; for example, Program Managers &mdash; it is more efficient to assign a role to a group and then add users to the group, because groups are easier to manage and audit.

## Related topics

* [User roles](../use/user-roles.md)
* [Create a group and add members in Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)
* [Environment requirements for advanced insights](../setup/environment-requirements.md)
* [Manager settings](../use/manager-settings.md)
* [About admin roles](/microsoft-365/admin/add-users/about-admin-roles?view=o365-worldwide&preserve-view=true)
