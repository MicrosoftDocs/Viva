---
ms.date: 12/14/2023
title: Add Viva Goals to Microsoft Teams
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager: Liz.Pierce
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-goals
ms.localizationpriority: high
ms.collection:  
- m365initiative-viva-goals  
- vg-integration
search.appverid:
- MET150
description: "Learn how to add Viva Goals to Microsoft Teams so you can view, manage, and share OKRs without leaving Teams."
---

# Add Viva Goals to Microsoft Teams

This article describes how to install the Viva Goals app in Microsoft Teams for yourself or your entire organization. The app helps you set up, manage, and track your team's goals from within Microsoft Teams. The final section of this article explains how to use the app in Outlook or Microsoft 365.
:::image type="content" source="../media/goals/msteams-integration/opening-screenshot.png" alt-text="Screenshot shows a view of Viva Goals in Microsoft Teams." lightbox="../media/goals/msteams-integration/opening-screenshot.png":::

## Install the Viva Goals app for yourself in Microsoft Teams

There are multiple ways to install the Viva Goals app in Teams. The easiest way is to select the ellipsis (three dots) on the left-hand navigation bar, search for Viva Goals, and then select **Add** next to the Viva Goals app in the list of search results.

:::image type="content" source="../media/goals/5/navigation-bar-ellipse-button-to-add-viva-goals-app.png" alt-text="Screenshot that shows how to search for and add the Viva Goals app from the Teams navigation bar." lightbox="../media/goals/5/navigation-bar-ellipse-button-to-add-viva-goals-app.png":::

Or, from the Viva Goals app detail page, select the **Add** button to add Viva Goals.

:::image type="content" source="../media/goals/5/add-viva-goals-from-navigation-bar.png" alt-text="Screenshot that shows how to use the Add button to add the Viva Goals app from Teams." lightbox="../media/goals/5/add-viva-goals-from-navigation-bar.png":::

Another way to add Viva Goals is to visit the Apps store, search for **Viva Goals**, and select the app.

:::image type="content" source="../media/goals/5/add-viva-goals-from-app-store.png" alt-text="Screenshot that shows how to search and add the Viva Goals app from the Teams app store." lightbox="../media/goals/5/add-viva-goals-from-app-store.png":::

On the Viva Goals app detail page, select **Add**.

:::image type="content" source="../media/goals/5/add-button-in-viva-goals-app-detail-page.png" alt-text="Screenshot that shows how to add the Viva Goals app from the Teams app store." lightbox="../media/goals/5/add-button-in-viva-goals-app-detail-page.png":::

To pin the Viva Goals app in Teams, right-click the app icon in the left navigation panel, and select **Pin**.

## Install the Viva Goals app for your organization in Microsoft Teams

Preinstalling the app will ensure that your users will be able to see their OKRs directly in Teams without having to install the app from the Teams app store. It's a great way to ensure your users stay in the flow of work, since they'll be able to reference OKRs directly in Teams chats and channels without pausing to install the app.  

We'll show you how to preinstall the app for a specific group of users. If you want to preinstall to all users on the tenant, you can make the same changes in the "Global (Org-wide default)" policy.

> [!Note]
> To do this, you need to be a Tenant Administrator with access to admin.teams.microsoft.com.

**Follow these steps to pre-install Viva Goals:**

1. Log in to [admin.teams.microsoft.com](https://admin.teams.microsoft.com/) with your user ID and password.
2. Select **Teams apps** and then choose **Setup policies**.

      :::image type="content" source="../media/goals/5/viva-goals-setup-policies.png" alt-text="Screenshot that shows the setup policies tab for pre-installing Viva Goals." lightbox="../media/goals/5/viva-goals-setup-policies.png":::

3. Under **Manage Policies**, select **Add** to create a new policy.

      :::image type="content" source="../media/goals/5/viva-goals-add-policies-button.png" alt-text="Screenshot that shows how to add the appropriate setup policy for pre-installing Viva Goals." lightbox="../media/goals/5/viva-goals-add-policies-button.png":::

4. Enter a name and description for your new policy.

   :::image type="content" source="../media/goals/5/ms-teams-policy-name.png" alt-text="Screenshot that shows how to name the appropriate setup policy for pre-installing Viva Goals." lightbox="../media/goals/5/ms-teams-policy-name.png":::

5. To preinstall the Viva Goals app as part of this policy, under **Installed apps**, select **Add Apps** and search for the app by name.

    :::image type="content" source="../media/goals/5/ms-teams-setup-policies-for-pre-installing-viva-goals.png" alt-text="Screenshot that shows how to search by name to add the Viva Goals app for pre-installation." lightbox="../media/goals/5/ms-teams-setup-policies-for-pre-installing-viva-goals.png":::

6. After you add the app to the **Apps to add** list, select **Add** at the bottom of the dialog to confirm.
7. To make sure users can find the installed app, we recommend that you also pin the app and the message extension. Under **Pinned apps**, select **Add app**.

      :::image type="content" source="../media/goals/5/add-pinned-apps-button.png" alt-text="Screenshot that shows where to choose to add an app to pinned apps." lightbox="../media/goals/5/add-pinned-apps-button.png":::

8. Search for and add the Viva Goals app. Select **Save** to confirm the changes to this policy.

      :::image type="content" source="../media/goals/5/pin-viva-goals-app.png" alt-text="Screenshot that shows how to search for and pin the Viva Goals app." lightbox="../media/goals/5/pin-viva-goals-app.png":::

   > [!Note]
   > The app will be added by default at the bottom of the pinned list. You can use the drag handle on the right side to adjust the position of the app in the list.

      :::image type="content" source="../media/goals/5/re-order-pinned-apps.png" alt-text="Screenshot that shows how to reorder pinned apps in Viva Goals." lightbox="../media/goals/5/re-order-pinned-apps.png":::

9. If you had user pinning turned on, Teams will notify you that user preferences will be applied on top of this policy. Select **Save**.

      :::image type="content" source="../media/goals/5/user-pin-on.png" alt-text="Screenshot that shows User Pinning enabled." lightbox="../media/goals/5/user-pin-on.png":::

10. You'll now see your new policy under the list in **Manage policies**. Note that the policy hasn't yet been applied to a group of users.

      :::image type="content" source="../media/goals/5/manage-policies-tab.png" alt-text="Screenshot that shows the View the policy under Manage policies." lightbox="../media/goals/5/manage-policies-tab.png":::

11. To apply the policy to a group of users, select the **Group Policy Assignment** tab and then select **Add** to create a new assignment.

      :::image type="content" source="../media/goals/5/add-group-policy-button.png" alt-text="Screenshot that shows Adding Group Policy for a group of users." lightbox="../media/goals/5/add-group-policy-button.png":::

    Policies can be applied to any Microsoft Teams team or Microsoft 365 group. Select the group of users you want to apply the policy to.

      :::image type="content" source="../media/goals/5/policy-groups.png" alt-text="Screenshot that shows how to select the groups to assign the policy." lightbox="../media/goals/5/policy-groups.png":::

12. Next, select the policy from the list and choose **Apply** to confirm your selection.

       :::image type="content" source="../media/goals/5/policy-list.png" alt-text="Screenshot that shows how to select the policy from the list." lightbox="../media/goals/5/policy-list.png":::

    Now, you'll see the assignment in the list under **Group Policy Assignment**.

       :::image type="content" source="../media/goals/5/group-policies-list.png" alt-text="Screenshot that shows how to view the assignment under Group Policy Assignment." lightbox="../media/goals/5/group-policies-list.png":::

    > [!Note]
    > The policy can take some time to kick in. You can check this by going to the **Activity log** and seeing if the policy application was complete.

      :::image type="content" source="../media/goals/5/activity-log.png" alt-text="Screenshot that shows how to check the completion of policy application in Activity log." lightbox="../media/goals/5/activity-log.png":::

    When you see the timestamp in the **Completed on** column, the policy will work for all the users in the group.

    Now when a user who belongs to this group signs in into Teams, the policy will kick in. For example, "Contoso" has "Abigail Jackson" as a member, as we can see in the Microsoft 365 admin center.

      :::image type="content" source="../media/goals/5/contoso-members-list.png" alt-text="Screenshot that shows Abigail Jackson in the list of members." lightbox="../media/goals/5/contoso-members-list.png":::

     When Abigail signs in into Teams, she can see that both the Viva Goals app and the message extension are preinstalled and pinned on the top left and at the bottom, respectively, in the Teams client.

      :::image type="content" source="../media/goals/5/pinned-viva-goals-with-message-extension.png" alt-text="Screenshot that shows the pinned Viva Goals app and Viva Goals message extension." lightbox="../media/goals/5/pinned-viva-goals-with-message-extension.png":::

## Install the Teams app for Viva Goals in Outlook and Microsoft 365

The Viva Goals app for Microsoft Teams is a Teams app that also works on Outlook and the Microsoft 365 app. Both link previews and the message extension will work in Outlook as well once the app is installed.

If the app is installed by a user in Microsoft Teams, it will automatically show up in Outlook and Microsoft 365. As an admin, you can also deploy these apps on Outlook and Microsoft 365 for your organization, using the Integrated Apps portal on the Microsoft 365 Admin Center. Note that deployment and management for the app is separately managed from Microsoft Teams. Microsoft Teams deployments are controlled from the Teams Admin Center, while Outlook and Microsoft 365 deployments are controlled from the Microsoft 365 Admin Center, Integrated apps section.

For information on managing the app in Outlook and Microsoft 365, see [Teams apps that work on Outlook and Microsoft 365](/microsoft-365/admin/manage/teams-apps-work-on-outlook-and-m365).
