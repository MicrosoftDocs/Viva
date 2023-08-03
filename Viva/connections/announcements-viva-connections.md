---
ms.date: 07/19/2023
title: "Use announcements in Viva Connections"
ms.reviewer: 
ms.author: evanatkin
author: AtkinE
manager: pamgreen
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-connections
localization_priority: Priority
ms.collection:
  - Strat_SP_modern
  - M365-collaboration
  - m365initiative-viva-connections
  - Tier1
search.appverid:
- SPO160
- MET150
ROBOTS: NOINDEX, NOFOLLOW
description: "Use announcements in Viva Connections"
---

# Use announcements in Viva Connections

Announcements allow you to create and share time-sensitive messages in Viva Connections. You can set up, manage, and schedule announcements from your organization’s SharePoint home site.

:::image type="content" source="../media/connections/announcements-viva-connections/announcement-tablet-mobile.png" alt-text="Screenshot that shows what an announcement in Viva Connections looks like on a tablet and mobile device."lightbox="../media/connections/announcements-viva-connections/announcement-tablet-mobile.png":::

> [!NOTE]
>
> - This experience is rolling out to targeted release customers now and will become generally available by September 2023.
> - The first release of the announcement feature is only available to customers with a SharePoint home site but will become available to all Viva Connections customers in the fall.
> - The first release of the announcement feature will only be available for mobile and tablet devices.  Support for desktop devices will become available in September 2023.
> - You must have member permissions or higher to your organization’s SharePoint homes site to send and manage announcements.

## When to use announcements

:::image type="content" source="../media/connections/announcements-viva-connections/announcement-example.png" alt-text="Screenshot of an open announcement in Viva Connections mobile."lightbox="../media/connections/announcements-viva-connections/announcement-example.png":::

Announcements are the best way to communicate targeted, time-sensitive information in the Viva Connections app.

**Example Scenarios:**

- Remind employees in a specific role of an upcoming deadline.
- Share details about open enrollment benefits for full-time employees.
- Send a specific call to action for new employees.

> [!IMPORTANT]
> For emergencies such as a safety hazard, it’s recommended to use multiple modes of communication.

### Best practices for using and writing announcements

- Use announcements sparingly so that users understand their importance. Sending them too frequently can cause users to disregard the notifications.
- Be aware that delivery time increases with the size of the targeted audience. Sending an announcement to a group of 50 users may take just a few minutes but sending one to 100,000 users may take several hours.
- Announcements aren’t designed for life-threatening emergencies.
- Keep messages short with a clear call to action. Plan to link to more information for complex topics.
- Specify which audiences need to receive the announcement to ensure the highest engagement possible.
- Allow users to dismiss announcements for less-urgent topics or when there are several high-impact announcements active at the same time.

## How announcements display in Viva Connections

> [!IMPORTANT]
> Announcements are currently only viewable on tablet and mobile experiences. The ability to view announcements on desktop is planned for future releases.

**In Teams**: Users get a Teams notification alerting them of a new announcement on their device’s lock screen  when the user has enabled it.

> [!NOTE]
> Viva Connections announcement notifications being displayed in the Teams activity feed is scheduled for a future release.

:::image type="content" source="../media/connections/announcements-viva-connections/mobile-announcement-lockscreen.png" alt-text="Screenshot of an Teams notification displayed on the lock-screen of a mobile device."lightbox="../media/connections/announcements-viva-connections/mobile-announcement-lockscreen.png":::

**In Viva Connections**: Announcements display towards the top of the Viva Connections experience where more details can be viewed.

:::image type="content" source="../media/connections/announcements-viva-connections/mobile-announcement-notification.png" alt-text="Screenshot of an open announcement in the Viva Connections mobile app."lightbox="../media/connections/announcements-viva-connections/mobile-announcement-notification.png":::

## How to create an announcement

> [!NOTE]
> Announcements are currently only able to be authored from a SharePoint home site. Authoring an announcement from the Viva Connections desktop is planned for future release.

1. There are three ways to access announcements to create a new announcement from a SharePoint home site:
    1. Select **+New** from the command bar and choose **Announcement**.
    1. Select **Announcements** from the site navigation and then **+ New announcement**.
    1. Navigate to **Settings** > **Manage Viva Connections** > **Announcements** > **+ New announcement**.

   :::image type="content" source="../media/connections/announcements-viva-connections/create-announcement-overview.png" alt-text="Screenshot of a SharePoint home site highlighting three options for starting a new announcement."lightbox="../media/connections/announcements-viva-connections/create-announcement-overview.png":::

2. Choose an icon and color that reflect the theme of the announcement.
3. Add a title and message.
4. Select an end date and time for when the announcement should no longer appear (up to two weeks from the original posting date).
5. Select up to 10 audiences to distribute the announcement to. Audiences can be Azure Active Directory groups, Microsoft 365 Groups, or Microsoft Azure Active Directory dynamic groups.

   :::image type="content" source="../media/connections/announcements-viva-connections/create-announcement-details.png" alt-text="Screenshot of the announcement details pane."lightbox="../media/connections/announcements-viva-connections/create-announcement-details.png":::

6. To add a link to more information, add a URL and label for the link under **More options**.
7. To allow users to dismiss the announcement after viewing, toggle the **Allow users to dismiss** setting on under **More options**.
8. To send the announcement later, enter a date and time under **Schedule to send later** under **More options**.

   :::image type="content" source="../media/connections/announcements-viva-connections/create-announcement-more-options.png" alt-text="Screenshot of additional options available in the announcement detail pane."lightbox="../media/connections/announcements-viva-connections/create-announcement-more-options.png":::

9. Select **Next** to review the details of your announcement.
10. If the announcement is ready to send immediately, select the **Send announcement** option.

    :::image type="content" source="../media/connections/announcements-viva-connections/announcement-review.png" alt-text="Screenshot of the announcement review pane after creating an announcement."lightbox="../media/connections/announcements-viva-connections/announcement-review.png":::

> [!NOTE]
> Once an announcement has been sent, message details and end date can still be edited.

## How to schedule an announcement to send later

1. Follow the steps to [create an announcement](#how-to-create-an-announcement) and then choose **More options**.
2. Choose a date and time under **Schedule to send later**.

   :::image type="content" source="../media/connections/announcements-viva-connections/announcement-send-later.png" alt-text="Screenshot of the Schedule to send later fields in the announcement detail pane."lightbox="../media/connections/announcements-viva-connections/announcement-send-later.png":::

   > [!NOTE]
   >
   > - The end date can be up to two weeks from the original posting date.
   > - Scheduling is only available in half-hour increments (e.g. you could schedule a post to send at 10:30 but not 10:15).

3. Select **Next** to review the details of your announcement.

   :::image type="content" source="../media/connections/announcements-viva-connections/schedule-announcement.png" alt-text="Screenshot of the announcement review pane after scheduling an announcement."lightbox="../media/connections/announcements-viva-connections/schedule-announcement.png":::

4. If the announcement is ready to be scheduled, select **Schedule announcement** and the announcement will be sent at the scheduled time.
5. The scheduled date and time can be edited anytime before the announcement has been sent.

## Save an announcement as a draft

1. Follow the steps to [create an announcement](#how-to-create-an-announcement).
2. After writing the title and message, choose the **Save as draft** button.
3. You can come back and edit the announcement later from the announcements page.

## Manage announcements from the announcements page

You can view all announcements that are active, scheduled, saved as drafts, and expired from the **Announcements** page. 

:::image type="content" source="../media/connections/announcements-viva-connections/announcements-page.png" alt-text="Screenshot of the announcements page showing the status of several announcements."lightbox="../media/connections/announcements-viva-connections/announcements-page.png":::

From here you can complete the following tasks:

### Create a new announcement

Choose **+ New announcement** and follow the steps to [create an announcement](#how-to-create-an-announcement).

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
3. If the announcement was active, users will no longer be able to view it, but it may still be accessible through a Teams notification.
