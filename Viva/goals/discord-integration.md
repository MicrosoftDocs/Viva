---
title: Discord integration
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
localization_priority: Priority
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Learn how to align your conversations around business execution and stay updated on your OKR progress right within Discord."
---

# Discord integration

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

## About the Discord integration

Viva Goals’ integration with Discord makes it easy for you to keep track of OKR progress in real-time. You can receive notifications on OKR progress, summary updates and manage your priorities right where you collaborate. 

## Setting up: creating a connection

1. Navigate to your sidebar and select **Admin > Integrations**. 

    :::image type="content" source="../media/goals/goals-manage-discord.png" alt-text="Image of creating a connection":::

2. In the Integrations section,  navigate to the **Discord** under the Messaging Integrations section and select **Add to Discord**.  

3. After selecting **Add to Discord**you will be directed to Discord’s authentication screen. Choose the Discord server you’d like to integrate with and select **Continue**. In the screen that follows, make sure the **Manage Webhooks** checkbox is enabled and select **Authorize**. 

4. Once authorization is successfully done, you’ll be redirected to the Discord integration configuration page in Viva Goals.

## Setting up: configuring notifications 

As an admin, you can configure what events your team receives updates on in your Discord channel. These real-time updates are applicable for the following set of events: 

- **Objectives**: Added, Closed, Deleted, Modified, Reopened.

- **Check-ins**: New check-ins, Comments

To configure channel notifications on Discord,

1. Select **Add Notification** to open the new notification configuration screen.

    :::image type="content" source="../media/goals/goals-add-notification-discord.png" alt-text="Image of add notification":::

2. In the popup that appears, choose:

    - **Send To**: Select a channel to whom the notifications would be published.
    
    - **Entities**: Choose which type of OKRs the notifications belong to - the organization’s, a specific team’s or an individual’s. You can choose multiple entities.
    
    - **Events**: Select from an array of options when you’d like to publish the notification - when an objective is added, closed, deleted, modified, reopened, and for new check-ins and check-in comments.

    :::image type="content" source="../media/goals/goals-popup-select-entities-discord.png" alt-text="Image of popup select entities":::

    :::image type="content" source="../media/goals/goals-select-events-for-notifications.png" alt-text="Image of select events for notifications":::

3. Select  **Add** to save your notification settings. Your notification settings will be saved and listed. 

    :::image type="content" source="../media/goals/goals-notification-setting-listing.png" alt-text="Image of save your notification settings":::

## Setting up: editing an existing notification setting 

Select  the **Edit** icon against the notification setting you'd like to make changes to and **Save** once you've made the required changes.

:::image type="content" source="../media/goals/goals-edit-notification-settings.png" alt-text="Image of editing an existing notification settings":::

## Customizing the cadence and frequency for summary updates

In addition to the event updates, you can also receive summary updates for your organization, team, or individual OKRs. You can determine the frequency and the cadence for when the summary updates will be posted in Discord.

1. Select the **Follower**, right next to the 'Owner' in your OKR title pane.  In the pop-up that follows, select the **Discord** tab and select the Discord channel you'd like to publish the summary updates. You can also select multiple channels to publish the updates. 

    :::image type="content" source="../media/goals/goals-summary-notification.png" alt-text="Image of summary notification":::

2. Select the gear icon against each channel to set up the publishing schedule. There are two schedules — default, and a custom schedule. The default schedule will send updates every week based on the default notification schedule set for your Viva Goals instance and will be applied to all the Discord channels you've selected. 

    :::image type="content" source="../media/goals/goals-customize-notification-cadence.png" alt-text="Image of customize notification ":::

   

3. If you want this customized, select Custom schedule and choose the frequency — weekly or monthly, and the cadence — day and the time.  

4. Select **Done** to save your settings.

## Using the Discord integration 

### Summary Notifications: 

The Viva Goals OKRs bot publishes summary updates of the Viva Goals entity (Organization OKR, Team OKR, Individual OKR) in your Discord channel based on notification cadence. The summary notification captures the overall progress change and progress and status for each individual OKR. 

 :::image type="content" source="../media/goals/goals-summary-updates.png" alt-text="Image of summary updates":::

### Notifications for events: 

The Viva Goals OKRs bot also publishes real-time updates in your Discord channel for events - adding an objective, new check-ins (Refer to the list of events supported [here](https://help.ally.io/en/articles/5151043-discord-integration#h_3448c1296f))  

:::image type="content" source="../media/goals/goals-new-objective-notification.png" alt-text="Image of objective-notification":::

> [!NOTE]
> The Viva Goals OKRs bot should be added as a channel member if you would like to trigger notifications into a private channel. If you’re creating a new private channel, you will need to enable Viva Goals OKRs under roles and add the Viva Goals OKRs bot as a channel member. 

:::image type="content" source="../media/goals/add-members-to-roles.png" alt-text="Image of add members to roles":::

## Disabling the integration 

To disable the integration, head over to the Discord Configuration page, select the **Options** dropdown and select **Remove Discord Integration**. Confirm by clicking ‘Remove Discord Integration’ in the pop-up that follows through. Disabling the integration will stop all future notifications.

:::image type="content" source="../media/goals/goals-remove-discord-integration.png" alt-text="Image of remove discord integration":::