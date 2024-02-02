---
ms.date: 02/02/2024
title: "Use announcements in Viva Connections"
ms.reviewer: 
ms.author: evanatkin
author: AtkinE
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-connections
ms.localizationpriority: high
ms.collection:
  - Strat_SP_modern
  - M365-collaboration
  - m365initiative-viva-connections
  - Tier1
search.appverid:
- SPO160
- MET150
description: "Use announcements in Viva Connections"
---

# Use announcements in Viva Connections

Announcements allow you to create and share time-sensitive messages in Viva Connections. You can set up, manage, and schedule announcements from your organization’s SharePoint home site.

:::image type="content" source="../media/connections/announcements-viva-connections/announcement-desktop-mobile.png" alt-text="Screenshot that shows what an announcement in Viva Connections looks like on a desktop and mobile device."lightbox="../media/connections/announcements-viva-connections/announcement-desktop-mobile.png":::

> [!NOTE]
>
> - Users will be required to have a Microsoft Viva suite or Viva Communications and Communities license to utilize the announcements feature. See [Microsoft Viva plans and pricing](https://www.microsoft.com/microsoft-viva/pricing) for more info.
> - You must have edit permissions or higher to your organization’s SharePoint home site or Viva Connections to author and manage announcements.
> - Announcements are unavailable in GCC, GCC High, and DoD environments. For more information, see the [list of service availability](/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/office-365-us-government#service-availability-for-each-plan).

## When to use announcements

Announcements are the best way to communicate targeted, time-sensitive information in the Viva Connections app.

**Example Scenarios:**

- Remind users in a specific role of an upcoming deadline.
- Share details about open enrollment benefits for full-time employees.
- Send a specific call to action for new employees.

> [!IMPORTANT]
>
> For emergencies such as a safety hazard, it’s recommended to use multiple modes of communication.

### Best practices for using and writing announcements

- Use announcements sparingly so that users understand their importance. Sending them too frequently can cause users to disregard the notifications.
- Be aware that delivery time increases with the size of the targeted audience. Sending an announcement to a group of 50 users might take just a few minutes but sending one to 100,000 users can take several hours.
- Announcements aren’t designed for life-threatening emergencies.
- Keep messages short with a clear call to action. Plan to link to more information for complex topics.
- Specify which audiences need to receive the announcement to ensure the highest engagement possible.
- Allow users to dismiss announcements for less-urgent topics or when there are several high-impact announcements active at the same time.

## How announcements display in Viva Connections

Announcements are viewable to users using desktop, tablet, and mobile experiences through Viva Connections.

- **In Teams**: Users get a Teams notification alerting them of a new announcement within Teams and on their mobile device’s lock screen when the user has enabled it.

:::image type="content" source="../media/connections/announcements-viva-connections/display-announcement-in-Teams-for-desktop-mobile.png" alt-text="Screenshot of a Teams notification displayed in Microsoft Teams, and on the lock-screen of a mobile device."lightbox="../media/connections/announcements-viva-connections/display-announcement-in-Teams-for-desktop-mobile.png":::

- **In Viva Connections**: Announcements display towards the top of the Viva Connections experience where more details can be viewed.

:::image type="content" source="../media/connections/announcements-viva-connections/display-announcement-in-Connections-for-desktop-mobile.png" alt-text="Screenshot of an announcement in Viva Connections desktop view and in the Viva Connections mobile app."lightbox="../media/connections/announcements-viva-connections/display-announcement-in-Connections-for-desktop-mobile.png":::

### Teams Channel announcements displaying in Viva Connections for frontline workers

Microsoft Teams Channel announcements will also display in the Viva Connections announcements banner for Frontline workers only.  Frontline managers can communicate important updates from their Teams Channel by using an @mention. Frontline workers can then select the link within the announcement in Connections to be redirected to the Teams Channel where the announcement was made.

A Teams Channel announcement is displayed in Viva Connections only if:

- The user has been assigned a Microsoft 365 F1 or F3 license;
- Channel mentions are enabled under the Teams Channel notification settings; and
- The Teams channel announcement has been tagged with an @mention  and is unread.

> [!NOTE]
>
> - Vanity domains are not supported. Contact your organization's support team for more information.
> - Additional updates to an existing Teams Channel announcement will not be displayed in Viva Connections. Users will need to follow the link from the original announcement in Viva Connections to view the Teams Channel announcement.
> - Teams Channel announcements that are deleted and then undone will show as unread.

For more information, see [Sending an announcement to a channel in Microsoft Teams](https://support.microsoft.com/office/8f244ea6-235a-4dcc-9143-9c5b801b4992).

## Accessing the announcements page

Experience owners are able to create announcements through the Viva Connections desktop experience or from their SharePoint home site using the announcements page. To access the announcement page:

- **In Viva Connections**: Experience owners can select the **ellipsis** in the upper-right of Viva Connections then select **Announcements**.The announcements page will open where users can select **+ New announcement** to begin drafting an announcement.

:::image type="content" source="../media/connections/announcements-viva-connections/viva-connections-create-announcement.png" alt-text="Screenshot showing a dropdown menu with announcements highlighted."lightbox="../media/connections/announcements-viva-connections/viva-connections-create-announcement.png":::

- **From the SharePoint home site**: The easiest way to access the announcements page is to select **Announcements** from the site navigation and then **+ New announcement**.

:::image type="content" source="../media/connections/announcements-viva-connections/SharePoint-create-announcement.png" alt-text="Screenshot showing a SharePoint nav bar with Announcements highlighted."lightbox="../media/connections/announcements-viva-connections/SharePoint-create-announcement.png":::

>[!NOTE]
>
> Users can also access the announcement page in SharePoint by:
>
> - Selecting **Settings > Manage Viva Connections > Announcements > + New announcement**.
> - Select **+ New** from the command bar and choose **Announcement**.

## Drafting your announcement

After [choosing to create a new announcement](#accessing-the-announcements-page) either from your Viva Connections experience or from the SharePoint home site, you'll be presented with the following fields for drafting your announcement.

1. Add a title and message.
2. Select up to 10 audiences to distribute the announcement to. Audiences can be Microsoft Entra groups, Microsoft 365 Groups, or Microsoft Entra dynamic groups.
3. Select an end date and time for when the announcement should no longer appear (up to two weeks from the original posting date).

   :::image type="content" source="../media/connections/announcements-viva-connections/create-announcement-details.png" alt-text="Screenshot of the announcement details pane."lightbox="../media/connections/announcements-viva-connections/create-announcement-details.png":::

4. To add a link to more information, add a URL and label for the link under **More options**.
5. To allow users to dismiss the announcement after viewing, toggle the **Allow users to dismiss** setting on under **More options**.
6. Select **Next** to review the details of your announcement.

   :::image type="content" source="../media/connections/announcements-viva-connections/create-announcement-more-options.png" alt-text="Screenshot of additional options available in the announcement detail pane."lightbox="../media/connections/announcements-viva-connections/create-announcement-more-options.png":::

7. If the announcement is ready to send immediately, select the **Send announcement** option.

    :::image type="content" source="../media/connections/announcements-viva-connections/announcement-review.png" alt-text="Screenshot of the announcement review pane after creating an announcement."lightbox="../media/connections/announcements-viva-connections/announcement-review.png":::

> [!NOTE]
> Once an announcement has been sent, message details and end date can still be edited.

## How to schedule an announcement to send later

1. Follow the steps to [access the announcement page](#accessing-the-announcements-page) and to [drafting your announcement](#drafting-your-announcement).
2. Toggle on the **Schedule to send later** option and enter a date and time:

> [!NOTE]
>
> - The end date can be up to two weeks from the original posting date.
> - Scheduling is only available in half-hour increments (e.g. you could schedule a post to send at 10:30 but not 10:15).

   :::image type="content" source="../media/connections/announcements-viva-connections/announcement-send-later.png" alt-text="Screenshot of the Schedule to send later fields in the announcement detail pane."lightbox="../media/connections/announcements-viva-connections/announcement-send-later.png":::

3. Select **Next** to review the details of your announcement.
4. If the announcement is ready to be scheduled, select **Schedule announcement** and the announcement will be sent at the scheduled time.

   :::image type="content" source="../media/connections/announcements-viva-connections/schedule-announcement.png" alt-text="Screenshot of the announcement review pane after scheduling an announcement."lightbox="../media/connections/announcements-viva-connections/schedule-announcement.png":::

5. The scheduled date and time can be edited anytime before the announcement has been sent.

## Save an announcement as a draft

1. Follow the steps to [access the announcement page](#accessing-the-announcements-page) and to [drafting your announcement](#drafting-your-announcement).
2. After writing the title and message, choose the **Save as draft** button.
3. You can come back and edit the announcement later from the announcements page.

## Manage announcements from the announcements page

You can view all announcements that are active, scheduled, saved as drafts, and expired from the **Announcements** page.

:::image type="content" source="../media/connections/announcements-viva-connections/announcements-page.png" alt-text="Screenshot of the announcements page showing the status of several announcements."lightbox="../media/connections/announcements-viva-connections/announcements-page.png":::

From the Announcements page, you can complete the following tasks:

### Create a new announcement

Choose **+ New announcement** and follow the steps to [draft your announcement](#drafting-your-announcement).

:::image type="content" source="../media/connections/announcements-viva-connections/announcement-page-new-announcement.png" alt-text="Screenshot of the new announcement button highlighted.":::

### Edit an active, scheduled, and drafted announcement

1. From the **Announcements** page, select the **edit** (pencil) icon for the announcement you want to make changes to.

   :::image type="content" source="../media/connections/announcements-viva-connections/edit-announcement.png" alt-text="Screenshot of the edit announcement icon highlighted."lightbox="../media/connections/announcements-viva-connections/edit-announcement.png":::

2. Make any desired changes in the **Announcement details** pane.
3. Choose to send or schedule drafted announcements.

### Delete an announcement

1. From your **Announcements** page, select the delete (trash can) icon for the announcement that you want to delete. Deleted announcements can’t be recovered.

   :::image type="content" source="../media/connections/announcements-viva-connections/delete-announcement.png" alt-text="Screenshot of the delete announcement icon highlighted."lightbox="../media/connections/announcements-viva-connections/delete-announcement.png":::

2. When prompted, choose **Yes, delete**.
3. If the announcement was active, users won't be able to view it, but it might still be accessible through a Teams notification.
