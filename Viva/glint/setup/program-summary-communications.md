---
title: Communications setup in Program Summary
description: Learn how to notify employees about upcoming surveys and the windows for taking surveys and having feedback conversations.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: reminders, reminder times, additional languages, notifications, survey invite, disable survey email, disable survey invite
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 10/08/2024
---

# Communications setup in Program Summary

Notifying employees about upcoming surveys and the time frame for taking their survey is essential for improving survey participation. 

:::image type="content" source="../../media/glint/setup/program-summary-comms-intro.png" alt-text="Screenshot of where to access Communications setup from Program Summary." lightbox="../../media/glint/setup/program-summary-comms-intro.png":::

>[!NOTE]
> If you're configuring an Always-On program, skip this step.

There are two sections to set up:
- Notification Timing
- Configure Notifications

## Notification Timing

:::image type="content" source="../../media/glint/setup/program-summary-comms-notification-timing.png" alt-text="Screenshot of the Notifications Timing section in Communications setup.":::

Send survey invites and reminders between the times that you set. Your organization's default time zone is preset in [General Settings](https://go.microsoft.com/fwlink/?linkid=2230744).  

> [!IMPORTANT]
> Viva Glint can successfully process 10,000 - 15,000 surveys and email invites per hour. Factor in these processing limitations and the number of employees in your distribution list when selecting a delivery window.

## Configure Notifications

The following sections display as setup actions and each field can be edited by selecting the **pencil symbol** that displays when selecting a row.

:::image type="content" source="../../media/glint/setup/program-summary-comms-configure-notifications.png" alt-text="Screenshot of the Configure Notifications section in Communications setup.":::

>[!TIP]
>When [personal email](https://go.microsoft.com/fwlink/?linkid=2247991) is set up as an optional system attribute, use **Email Settings** to send to **Company** or **Company and personal** email.

### Editing the survey invitation

Select **Survey Start** to activate the *Survey Invitation* slider window.

Check **Send notification** to ensure that the send date is as expected.

### Disabling the survey invitation

If you want to include items in your survey invitation that cannot be supported on our platform (URLs, HTML, images, videos, etc.), toggle the **Send Notification** to **Off**. Be sure to send your own in-house survey invitation, including those items that Viva Glint can't support. 

> [!TIP]
> Always send your people a survey invite! Participation is essential for uncovering useful feedback.

:::image type="content" source="../../media/glint/setup/comms-invite-slider.png" alt-text="Screenshot of the Survey Invitation slider window for the Communications setup page.":::

### Use Reminders

Set up to three reminders during the survey window and also a final reminder.

>[!TIP]
>Send two survey reminders per program. Survey takers only receive reminders if they haven't completeled their survey. 

Use the **Pencil** symbol to open the window and then:

- Change reminder send dates, which are preset.
- Preview your reminder. At this time, the reminder message can't be edited. You can change the language and preview the message in other languages.

### Add survey reminders

The dropdown menu from the **Add survey Reminder** button lets admins add reminders. Reminders display on the Communications page with an alarm symbol in a green circle.

:::image type="content" source="../../media/glint/setup/program-summary-comms-add-reminder.png" alt-text="Screenshot of the Add Survey Reminder dropdown menu for the Communications setup page.":::

### Customize email content

Use this email [customization guidance](email-content-customization.md) to add custom text to your Glint survey emails.

## Notifications when survey results are available

The results notification email is a one-time notification to let users know that results are available to them. The email sends to users in roles with **live** reporting access 24-hours before the email to all others (including phased access). 

> [!IMPORTANT]
> For all users to receive a results notification, ensure that all roles are granted access (phased or live) in the **Reporting** section of the survey program before the survey closes. 

To set up the results notification email:

1. From the admin dashboard, go to **Configuration** and choose **Survey Programs**.
1. Select a survey and go to the **Communications** section in **Program Summary**.
1. Select the **Edit & Preview** option on the **Survey End** email.
   1. This email is turned off by default.
1. In the edit pane that appears, switch **Send notification** to **On**.
2. In the **Send** field, enter a number of days after survey end date to send the email.
   1. The default is three (3) and the maximum is 30 days.
2. Select **Save Changes** in the top right of the edit pane.

> [!IMPORTANT]
> Access must be scheduled to be live 24 hours before the results notification email is scheduled for sending.

> [!NOTE]
> To edit **Team Conversations** notifications, [follow this guidance](https://go.microsoft.com/fwlink/?linkid=2231273).

## Configure Nudges

Set up who in your organization receives [Nudges](https://go.microsoft.com/fwlink/?linkid=2231015) to promote continued action on feedback results. 

:::image type="content" source="../../media/glint/setup/program-summary-comms-nudges-button.png" alt-text="Screenshot of the Configure Nudges button on the Communications setup page.":::

Select **Configure Nudges** to open the **Nudges** setup page. Follow the in-platform guidance.

:::image type="content" source="../../media/glint/setup/program-summary-comms-nudge-configuration.png" alt-text="Screenshot of the Nudges setup page on the admin dashboard.":::

## Final saving of communication edits 

After adding or editing reminder dates, select the **right facing arrow** and then **Save and Continue.**

## Next Step

> [!div class="nextstepaction"]
> [Coaching setup in Program Summary](https://go.microsoft.com/fwlink/?linkid=2231416).
