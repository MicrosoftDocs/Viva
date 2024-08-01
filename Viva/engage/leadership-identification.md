---
title: "Identify leaders and manage audiences in Viva Engage"
description: "Leadership identification and audience management enable organizations to designate leaders, configure their audience and connect leaders with the entire organization."
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 11/01/2023
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---


# Identify leaders and manage audiences in Viva Engage

Leaders naturally want to share visions, updates, and perspectives to build culture, manage change, and drive engagement with the people they lead. Viva Engage empowers leaders to connect more effectively with their employees.

This process begins with identifying leaders and the audiences they want to engage.

The leadership identification and audience management settings enable organizations to designate leaders, configure their audiences, and connect leaders with the organization. These settings are a prerequisite for other leadership features of Viva Engage, which include leadership announcements, campaigns, audience analytics, and leadership corner.

## Identify leaders

Engage admins, corporate communicators, Viva Engage verified admins, and Viva Engage network admins can identify leaders in Viva Engage. Leaders can be identified individually or by importing groups of leaders.

1. In the Viva Engage Teams application, select the ellipses button from the top navigation menu to expose the admin option. Select **Admin** to go to the Viva Engage admin center.

   [![Screenshot of the entry point into the Viva Engage admin center.](/viva/media/engage/admin/admin-entrypoint.png)](/viva/media/engage/admin/admin-entrypoint.png#lightbox)

2. On the **Feature management** tab, select **Leadership identification and audiences** to go to the **Manage leaders** page. Here, search for users and groups to identify leaders.

   [![Screenshot of the Viva Engage admin center interface to manage leader identification.](/viva/media/engage/admin/leader-id-eac.png)](/viva/media/engage/admin/leader-id-eac.png#lightbox)

3. Select **Add leaders** and enter the name of the user or group you want to identify as leaders.

   [![Screenshot of the Viva Engage admin center interface for adding leaders.](/viva/media/engage/admin/add-leaders.png)](/viva/media/engage/admin/add-leaders.png#lightbox)

5. Select the user or group from the search results.

6. If you're importing a group, select **Continue** to confirm your choice. The group members and individuals you selected are then added as leaders in the **Manage leaders** list.

    > [!NOTE]
    > Subsequent changes to group memberships don't automatically update who is identified as a leader in Viva Engage. You can re-add the group to add new members, or add and remove individual leaders.

## Manage a leader's audiences

After a leader is identified, the next step is to manage the leader’s audiences. This task is for the Engage admin, Viva Engage verified admin, Viva Engage network admin, corporate communicator, and leader or leader's delegate managers.  

1. On the **Manage leaders** list, find the leader’s row and select the pencil icon next in it to edit.

    [![Screenshot of the interface to manage a leader's audiences in Viva Engage.](/viva/media/engage/admin/edit-audience.png)](/viva/media/engage/admin/edit-audience.png#lightbox)

1. The **Manage audiences** page appears, where you configure the leader’s audiences. A leader can define as their audience:

    - **The entire organization:** The leader’s posts and announcements reach all users in the Viva Engage network, excluding guests. To enable a leader to share and reach the entire organization, enable the **Entire organization** toggle.

        :::image type="content" source="/viva/media/engage/admin/manage-audiences.png" alt-text="Screenshot of the Manage audience interface in Viva Engage.":::

        > [!NOTE]
        > Leaders and delegate managers can't enable this option. Only Engage admins, Viva Engage verified admins, Viva Engage network admins, and corporate communicators can allow leaders to reach the entire organization.  

    - **One or more audiences:** An audience represents people that the leader wants to connect with most, typically those in the leader’s immediate organization. To define an audience, select the **Add new audience** button and then search to add an existing group. If you can't find a group that includes the audience members you want, create a new group and add users to it.

        > [!NOTE]
        > Each time a storyline announcement is posted, the selected audiences receive an automatic notification.

    - **Multitenant organization:** Turn on this toggle to let spoke tenants receive leadership posts and announcements from the hub tenant. This enables users in the spoke tenants to receive a blended feed of leader announcements in Leadership corner from their own leaders and selected leaders on the hub tenant. The **Enable organization** toggle must also be turned on.

        >[!NOTE]
        >This option is only present when Viva Engage is configured as a [multitenant organization](/Viva/engage/mto-setup).

1. To define a leader’s audience, add individual users or groups, such as security, distribution, or Microsoft 365 groups. When you add a group, *changes to the group’s membership, including nested members, automatically update the audience* within 24 hours.

    Customers frequently use a distribution list to communicate with an audience by email. You can add these lists to the leader’s audience in Viva Engage for continuous communication.

## Set leader delegates and delegate managers

A leader’s posts, stories, and announcements in Viva Engage can be created and managed by delegates. A *delegate* has permission to create posts and replies on behalf of another user. A *delegate manager* has the same ability to create content, configure the audience for a leader, and assign more delegates.

A leader follows these steps to configure delegates:

1. In the Viva Engage Teams application, select the ellipses button from the top navigation menu to expose the dropdown list of options. (See the image at the beginning of this article for reference.)
2. Select **Manage delegate settings**.

3. Add the name of the person that you want to assign as delegate or delegate manager.

   [![Screenshot of the delegate settings interface in Viva Engage.](/viva/media/engage/admin/delegate-settings.png)](/viva/media/engage/admin/delegate-settings.png#lightbox)

4. Choose the type of delegate:

    - A *delegate* can create posts on behalf of the user in any public or private Viva Engage community as long as both the delegate and the user have access to it.
    - A *delegate manager* can similarly create posts. A delegate manager can also configure a leader’s audiences and assign more delegates or delegate managers.
    - When a user gets a new delegate assigned to the delegate team, the user and the whole team of delegates receive an email notifying them of this action.

    - When a delegate is removed, the same audience is also notified.

5. If a delegate needs to create posts, stories, or announcements on the leader’s [storyline](/Viva/engage/eac-storyline), **enable the storyline toggle**.

Learn more about [delegate managers in Viva Engage](https://support.microsoft.com/office/enable-someone-to-post-to-viva-engage-on-your-behalf-60f879cd-43dd-44fe-bffb-1084d4f85285).

## Leadership corner

Leadership corner provides tools so that employees in your organization can learn about their leaders and build connections with them. From leadership corner, users can catch up on leaders' posts, join their communities, and attend their AMAs.  

By default, Leadership corner is turned on. But an Engage admin can disable it in the [Viva Engage admin center](/Viva/engage/eac-overview). Follow these steps to enable or disable leadership corner:

1. Select **Leadership corner** from the **Feature management tab** in the Viva Engage admin center.

   [![Screenshot of the leadership corner button for feature management in the Viva Engage admin center.](/viva/media/engage/admin/lc-admin-eac.png)](/viva/media/engage/admin/lc-admin-eac.png#lightbox)

2. Use the toggle to enable or disable leadership corner for your organization.

   [![Screenshot of the leadership corner toggle for admin.](/viva/media/engage/admin/lc-toggle.png)](/viva/media/engage/admin/lc-toggle.png#lightbox)

> [!NOTE]
> After you disable leadership corner, users no longer see the **Leaders** entry point in the top navigation of Viva Engage.

## What next

**Announcements**

Learn more about [storyline announcements](https://support.microsoft.com/topic/8db19630-ecd0-4d1e-b735-437aea62e248), which enable leaders to reach their audiences with need-to-know information across Outlook, Teams, and Microsoft Viva.

**Analytics**

Learn more about [analytics for leaders](/Viva/engage/analytics), which empower leaders to measure and improve the effectiveness of their communication and engagement and to identify opportunities to drive impact in their organization.  

## Frequently asked questions

**What license is required for a leader?**

Any user with a license to Viva Engage, Viva Engage Core, or the Viva Engage Communities and Communications service plan can be identified as a leader. Identified leaders with a license to the Viva Engage Communities and Communications service plan have access to storyline announcements, leadership corner, campaigns, and AMAs. Identified leaders who don’t have a license to the Viva Engage Communities and Communications service plan only have access to their storyline and stories.

**Why is leader identification and audience management important?**

Identify leaders and audiences to ensure that your leaders' posts reach their intended audiences. Leader identification and audience management are required for other premium features to work successfully, such as storyline announcements, leadership corner, campaigns, and analytics.

**Who can identify and set leaders?**

Verified admins, Network admins, Engage admins, and corporate communications managers with a license to the Viva Engage Communities and Communication service plan can identify leaders.

**How are leader’s audiences configured?**

Identified leaders and their delegate managers can configure leaders' audiences in the **Manage audiences** interface in the Viva Engage admin center. But for a leader to reach the entire organization, the Engage admin, Verified admin, Network admin, or corporate communications manager must configure and enable this audience. Other users aren't involved in audience configuration.  

**Is there a way to disable leadership corner?**

Yes, the Engage admin can turn off leadership corner in the feature management section of the Viva Engage admin center.

**How can I customize the company logo in leadership corner?**

Yes. Follow the instructions at this [Customize your network](/viva/engage/manage-viva-engage-groups/customize-your-network).

**What does being in a leader's audience in Viva Engage entail?**

People who are in a leader's audience can see that leader and their content in leadership corner. From the leader's perspective, when they send a storyline announcement, the leader can decide to notify their audience members via Outlook, Teams, or Viva Engage. Leaders also get to see audience analytics.

**Are audiences restricted in size or number in Viva Engage?**

A leader can add up to 40 audiences. Audiences created through Microsoft Entra groups don’t limit the number of members in an audience.

**How are members notified about new content from their assigned leader?**

The leader posting a storyline announcement gets to decide whether to notify audience members through Outlook, Teams, or Viva Engage. Even if the leader decides not to send a notification, audience members will see the leader's content in Leadership corner.

**How should leaders be selected within the organization?**

People who frequently send announcements to the entire organization or to large groups of people within the organization make good leaders. To ensure that audience members are up-to-date with communications that matter, leadership corner helps audience members quickly identify which messages from their leaders are important.

**What privileges do identified leaders have in Viva Engage?**

Identified leaders can define one or more audiences to receive their content in leadership corner. Leaders can also send storyline announcements, sponsor campaigns, and access audience analytics.

**Once leaders are designated, what changes do leaders and audiences members experience?**

In the leader directory, designated leaders appear on the All Leaders tab for the entire network and on the My leaders tab for audience members.

Audience members can find their leaders' content in leadership corner and are notified of storyline announcements, provided the leader sends a notification. Leaders have access to features such as audience analytics and sponsoring campaigns.

## See also

[Set up and manage campaigns in Viva Engage](/viva/engage/campaigns)

[Key admin roles and permissions in Viva Engage](/viva/engage/eac-key-admin-roles-permissions)

[Manage and set up storyline in Viva Engage](/Viva/engage/eac-storyline)
