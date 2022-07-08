---
title: Add the Viva Goals app to Microsoft Teams
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: 
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: high
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Learn how to add Viva Goals to Microsoft Teams to easily view, manage and share OKRs across your organization, without leaving Microsoft Teams."
---

# Add the Viva Goals app to Microsoft Teams

- [Configure the Microsoft Teams integration: For regular users](#regular-user-setup)
- [Configure the Microsoft Teams integration: For admins](#admin-setup)

<h2 id="regular-user-setup">Configure the Microsoft Teams integration: For regular users</h2>

There are multiple ways to install the Viva Goals app in Teams.

The first way to add Viva Goals to Teams is for you to click the ellipsis […] button on the navigation bar on the left, search for Viva Goals and click on the Viva Goals app from the list of search results.

:::image type="content" source="../media/goals/5/navigation-bar-ellipse-button-to-add-viva-goals-app.png" alt-text="Searching and adding Viva Goals app from the Teams navigation bar." lightbox="../media/goals/5/navigation-bar-ellipse-button-to-add-viva-goals-app.png":::

From the Viva Goals app detail page, you can click the Add button to add Viva Goals.

:::image type="content" source="../media/goals/5/add-viva-goals-from-navigation-bar.png" alt-text="Adding Viva Goals app from the Teams navigation bar." lightbox="../media/goals/5/add-viva-goals-from-navigation-bar.png":::

The second way to Add Viva Goals is to visit the Apps store and once there, search for Viva Goals and click the Viva Goals app listing.

:::image type="content" source="../media/goals/5/add-viva-goals-from-app-store.png" alt-text="Searching and adding Viva Goals app from the Teams app store." lightbox="../media/goals/5/add-viva-goals-from-app-store.png":::

From the Viva Goals app detail page, click Add.

:::image type="content" source="../media/goals/5/add-button-in-viva-goals-app-detail-page.png" alt-text="Adding Viva Goals app from the MS Teams app store." lightbox="../media/goals/5/add-button-in-viva-goals-app-detail-page.png":::

Once Viva Goals have been added to Microsoft Teams, the app will guide you on the next steps based on if you already have an account with Viva Goals or not.

<h2 id="admin-setup">Configure the Microsoft Teams integration: For admins</h2>

Preinstalling the app will ensure that your users will be able to see their OKRs directly in Teams, without ever having to install the app from the Teams Store. It is a great way to ensure your users stay in the flow of work, since they will be able to reference OKRs directly in Teams chats and channels without first pausing to install the app.  

We will show how to preinstall the app for a specific group of users. If you want to preinstall to all users on the tenant, you can make the same changes in the “Global (Org-wide default)” policy. 

> Note:
> To do this, you need to be a tenant admin with access to admin.teams.microsoft.com.

**Follow these steps to successfully pre-install Viva Goals:**

1. Log in to https://admin.teams.microsoft.com/ with your user id and password.
2. Select **Teams apps** and choose **Setup policies**.

      :::image type="content" source="../media/goals/5/viva-goals-setup-policies.png" alt-text="Setup policies tab under Teams apps for pre-installing Viva Goals." lightbox="../media/goals/5/viva-goals-setup-policies.png":::

3. Under **Manage Policies**, select **Add** to create a new policy.

      :::image type="content" source="../media/goals/5/viva-goals-add-policies-button.png" alt-text="Adding the appropriate setup policy for pre-installing Viva Goals." lightbox="../media/goals/5/viva-goals-add-policies-button.png":::

4. Add a name and description for your new policy.

   :::image type="content" source="../media/goals/5/ms-teams-policy-name.png" alt-text="Naming the appropriate setup policy for pre-installing Viva Goals." lightbox="../media/goals/5/ms-teams-policy-name.png":::

5. Now to preinstall the Viva Goals app as part of this policy, under **Installed apps**, select **Add Apps** and search for the app by name
   
    :::image type="content" source="../media/goals/5/ms-teams-setup-policies-for-pre-installing-viva-goals.png" alt-text="Searching and adding the Viva Goals app for pre-installation." lightbox="../media/goals/5/ms-teams-setup-policies-for-pre-installing-viva-goals.png":::

6. Once you’ve added the app to the **Apps to add** list, confirm your selection by selecting **Add** at the bottom of the dialog box.
7. To make sure users can find the installed app, we recommend you also pin the app and the message extension. Under **Pinned apps**, select **Add app**.

      :::image type="content" source="../media/goals/5/add-pinned-apps-button.png" alt-text="Adding Viva Goals app to pinned apps." lightbox="../media/goals/5/add-pinned-apps-button.png":::

8. Search for and add the Viva Goals app. Select **Save** to confirm the changes to this policy.

      :::image type="content" source="../media/goals/5/pin-viva-goals-app.png" alt-text="Searching and pinning Viva Goals app." lightbox="../media/goals/5/pin-viva-goals-app.png":::
   
   > Note:
   > The app will be added by default at the bottom of the pinned list. You can use the drag handle on the right to adjust the relative position of the app in the list.

      :::image type="content" source="../media/goals/5/re-order-pinned-apps.png" alt-text="Reordering pinned apps in Viva Goals." lightbox="../media/goals/5/re-order-pinned-apps.png":::
   
9. If you had user pinning on, Teams will show you a notification that user preferences will be applied on top of this policy. Select **Save**.

      :::image type="content" source="../media/goals/5/user-pin-on.png" alt-text="User Pinning enabled." lightbox="../media/goals/5/user-pin-on.png":::

10. You will now see your new policy under the list in **Manage policies**. Note that the policy has still not been applied to a group of users.

      :::image type="content" source="../media/goals/5/manage-policies-tab.png" alt-text="View the policy under Manage policies." lightbox="../media/goals/5/manage-policies-tab.png":::

11. To apply the policy to a group of users, select the **Group Policy Assignment** tab and select **Add** to create a new assignment.

      :::image type="content" source="../media/goals/5/add-group-policy-button.png" alt-text="Adding Group Policy for a group of users." lightbox="../media/goals/5/add-group-policy-button.png":::

12. Policies can be applied to any Microsoft Teams Team or M365 group. Begin by selecting the group of users you want to apply the policy to.

       :::image type="content" source="../media/goals/5/policy-groups.png" alt-text="Select the groups to assign the policy." lightbox="../media/goals/5/policy-groups.png":::

13. Then, select the policy from the list and select **Apply** to confirm your selection. 

       :::image type="content" source="../media/goals/5/policy-list.png" alt-text="Select the policy from the list." lightbox="../media/goals/5/policy-list.png":::

14. Now, you will see the assignment in the list under **Group Policy Assignment**.

       :::image type="content" source="../media/goals/5/group-policies-list.png" alt-text="View the assignment under Group Policy Assignment." lightbox="../media/goals/5/group-policies-list.png":::

    > Note:
    > The policy can take some time to kick in. You can check this by going to the Activity Log and seeing if the policy application was complete.
      
      :::image type="content" source="../media/goals/5/activity-log.png" alt-text="Checking the completion of policy application in Activity log." lightbox="../media/goals/5/activity-log.png":::
      
    > Once you see the timestamp in the **Completed on** column, the policy will work for all the users in the group.

15. Now when a user who belongs to this group logs into Teams, the policy will kick in. For example, “Contoso” has “Julia Martins” as a member as we can see in the M365 admin.
      
      :::image type="content" source="../media/goals/5/member-list-julia-martins.png" alt-text="Example showing Julia Martins from the list of members." lightbox="../media/goals/5/member-list-julia-martins.png":::
      
16. When Julia logs into Teams, you can see that both the Viva Goals app and the message extension are preinstalled and pinned on the top left and at the bottom, respectively, in the Teams client.

      :::image type="content" source="../media/goals/5/pinned-viva-goals-with-message-extension.png" alt-text="Pinned Viva Goals app and Viva Goals message extension." lightbox="../media/goals/5/pinned-viva-goals-with-message-extension.png":::
      
