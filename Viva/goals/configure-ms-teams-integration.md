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

This article describes how to install, pin, and interact with Viva Goals directly inside Microsoft Teams. The Viva Goals personal app brings the ability to create objectives and key results (OKRs), check in on them, track progress, and close OKRs within Microsoft Teams.

:::image type="content" source="../media/goals/5/organization-okrs-tab.png" alt-text="Screenshot shows a sample view of Viva Goals organization OKRs in Microsoft Teams." lightbox="../media/goals/5/organization-okrs-tab.png":::

- [Configure Microsoft Teams integration: For regular users](#regular-user-setup)
- [Configure Microsoft Teams integration: For admins](#admin-setup)

<h2 id="regular-user-setup">Configure Microsoft Teams integration: For regular users</h2>

There are multiple ways to install the Viva Goals app in Teams.

The first way to add Viva Goals to Teams is for you to select the ellipsis [**…**] button on the navigation bar on the left side, search for Viva Goals, and then select the Viva Goals app from the list of search results.

:::image type="content" source="../media/goals/5/navigation-bar-ellipse-button-to-add-viva-goals-app.png" alt-text="Screenshot shows how to search for and add Viva Goals app from the Teams navigation bar." lightbox="../media/goals/5/navigation-bar-ellipse-button-to-add-viva-goals-app.png":::

From the Viva Goals app detail page, you can select the **Add** button to add Viva Goals.

:::image type="content" source="../media/goals/5/add-viva-goals-from-navigation-bar.png" alt-text="Screenshot shows how to use the "Add" button to add Viva Goals app from Teams." lightbox="../media/goals/5/add-viva-goals-from-navigation-bar.png":::

Another way to Add Viva Goals is to visit the Apps store, search for Viva Goals, and select the Viva Goals app listing.

:::image type="content" source="../media/goals/5/add-viva-goals-from-app-store.png" alt-text="Screenshot that shows how to search and add Viva Goals app from the Teams app store." lightbox="../media/goals/5/add-viva-goals-from-app-store.png":::

On the Viva Goals app detail page, select **Add**.

:::image type="content" source="../media/goals/5/add-button-in-viva-goals-app-detail-page.png" alt-text="Screenshot that shows how to add the Viva Goals app from the Microsoft Teams app store." lightbox="../media/goals/5/add-button-in-viva-goals-app-detail-page.png":::

To pin the Viva Goals app in Teams, right-click the app icon in the left navigation panel and select **Pin**.

<h2 id="admin-setup">Configure Microsoft Teams integration: For admins</h2>

Preinstalling the app will ensure that your users will be able to see their OKRs directly in Teams without ever having to install the app from the Teams Store. It's a great way to ensure your users stay in the flow of work, since they will be able to reference OKRs directly in Teams chats and channels without first pausing to install the app.  

We'll show how to preinstall the app for a specific group of users. If you want to preinstall to all users on the tenant, you can make the same changes in the "Global (Org-wide default)" policy.

> [!Note]
> To do this, you need to be a tenant admin with access to admin.teams.microsoft.com.

**Follow these steps to pre-install Viva Goals:**

1. Log in to https://admin.teams.microsoft.com/ with your user ID and password.
2. Select **Teams apps** and then choose **Setup policies**.

      :::image type="content" source="../media/goals/5/viva-goals-setup-policies.png" alt-text="Screenshot shows the setup policies tab for pre-installing Viva Goals." lightbox="../media/goals/5/viva-goals-setup-policies.png":::

3. Under **Manage Policies**, select **Add** to create a new policy.

      :::image type="content" source="../media/goals/5/viva-goals-add-policies-button.png" alt-text="Screenshot shows how to add the appropriate setup policy for pre-installing Viva Goals." lightbox="../media/goals/5/viva-goals-add-policies-button.png":::

4. Enter a name and description for your new policy.

   :::image type="content" source="../media/goals/5/ms-teams-policy-name.png" alt-text="Screenshot shows how to name the appropriate setup policy for pre-installing Viva Goals." lightbox="../media/goals/5/ms-teams-policy-name.png":::

5. To preinstall the Viva Goals app as part of this policy, under **Installed apps**, select **Add Apps** and search for the app by name.
   
    :::image type="content" source="../media/goals/5/ms-teams-setup-policies-for-pre-installing-viva-goals.png" alt-text="Screenshot shows how to search by name to add the Viva Goals app for pre-installation." lightbox="../media/goals/5/ms-teams-setup-policies-for-pre-installing-viva-goals.png":::

6. After you add the app to the **Apps to add** list, select **Add** at the bottom of the dialog box to confirm.
7. To make sure users can find the installed app, we recommend you also pin the app and the message extension. Under **Pinned apps**, select **Add app**.

      :::image type="content" source="../media/goals/5/add-pinned-apps-button.png" alt-text="Screenshot shows where to choose to add an app to "pinned apps"." lightbox="../media/goals/5/add-pinned-apps-button.png":::

8. Search for and add the Viva Goals app. Select **Save** to confirm the changes to this policy.

      :::image type="content" source="../media/goals/5/pin-viva-goals-app.png" alt-text="Screenshot  shows how to search for and pin the Viva Goals app." lightbox="../media/goals/5/pin-viva-goals-app.png":::
   
   > [!Note]
   > The app will be added by default at the bottom of the pinned list. You can use the drag handle on the right side to adjust the relative position of the app in the list.

      :::image type="content" source="../media/goals/5/re-order-pinned-apps.png" alt-text="Screenshot that shows how to reorder pinned apps in Viva Goals." lightbox="../media/goals/5/re-order-pinned-apps.png":::
   
9. If you had user pinning on, Teams will notify you that user preferences will be applied on top of this policy. Select **Save**.

      :::image type="content" source="../media/goals/5/user-pin-on.png" alt-text="Screenshot that shows User Pinning enabled." lightbox="../media/goals/5/user-pin-on.png":::

10. You'll now see your new policy under the list in **Manage policies**. Note that the policy hasn't yet been applied to a group of users.

      :::image type="content" source="../media/goals/5/manage-policies-tab.png" alt-text="Screenshot that shows the View the policy under Manage policies." lightbox="../media/goals/5/manage-policies-tab.png":::

11. To apply the policy to a group of users, select the **Group Policy Assignment** tab and then select **Add** to create a new assignment.

      :::image type="content" source="../media/goals/5/add-group-policy-button.png" alt-text="Screenshot that shows Adding Group Policy for a group of users." lightbox="../media/goals/5/add-group-policy-button.png":::

    Policies can be applied to any Microsoft Teams team or Microsoft 365 group. Begin by selecting the group of users you want to apply the policy to.

      :::image type="content" source="../media/goals/5/policy-groups.png" alt-text="Screenshot that shows how to select the groups to assign the policy." lightbox="../media/goals/5/policy-groups.png":::

13. Then, select the policy from the list and select **Apply** to confirm your selection. 

       :::image type="content" source="../media/goals/5/policy-list.png" alt-text="Screenshot that shows how to select the policy from the list." lightbox="../media/goals/5/policy-list.png":::

    Now, you'll see the assignment in the list under **Group Policy Assignment**.

       :::image type="content" source="../media/goals/5/group-policies-list.png" alt-text="Screenshot that shows how to view the assignment under Group Policy Assignment." lightbox="../media/goals/5/group-policies-list.png":::


    > [!Note]
    > The policy can take some time to kick in. You can check this by going to the Activity Log and seeing if the policy application was complete.

      
      :::image type="content" source="../media/goals/5/activity-log.png" alt-text="Screenshot that shows how to check the completion of policy application in Activity log." lightbox="../media/goals/5/activity-log.png":::
      
    > Once you see the timestamp in the **Completed on** column, the policy will work for all the users in the group.

    Now when a user who belongs to this group logs into Teams, the policy will kick in. For example, "Contoso" has "Abigail Jackson" as a member, as we can see in the M365 admin.
      
      :::image type="content" source="../media/goals/5/contoso-members-list.png" alt-text="Screenshot that shows Abigail Jackson from the list of members." lightbox="../media/goals/5/contoso-members-list.png":::
      
     When Abigail logs into Teams, you can see that both the Viva Goals app and the message extension are preinstalled and pinned on the top left and at the bottom, respectively, in the Teams client.

      :::image type="content" source="../media/goals/5/pinned-viva-goals-with-message-extension.png" alt-text="Screenshot that shows the pinned Viva Goals app and Viva Goals message extension." lightbox="../media/goals/5/pinned-viva-goals-with-message-extension.png":::
      
