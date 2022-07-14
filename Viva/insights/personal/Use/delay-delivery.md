---
title: Delay delivery plan with Viva Insights
description: Learn how to opt in and use Delay delivery with Viva Insights for suggestions on when to send email during your coworker's working hours
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-personal 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: helayne
audience: user
---

# Delay delivery plan

_**Applies to**: The Delay delivery plan is available to people who are using Microsoft Viva Insights and are enrolled in an applicable [Personal insights service plan](../overview/plans-environments.md#additional-features)._

When you're composing an email in Outlook, Delay delivery will show you suggestions for scheduling email deliveries. You might see suggestions for the following scenarios:

* When all recipients in the **To** field are outside of their working hours.
* When a recipient in the **To** field has an [automatic out-of-office reply](https://support.microsoft.com/office/send-automatic-out-of-office-replies-from-outlook-9742f476-5348-4f9f-997f-5e208513bd67) set up in Outlook.
* When you are outside of your working hours.

The delay helps minimize disruptions to recipients outside their working hours or when they’re away from work. It helps anybody who wants to maintain the flexibility to work when they want without putting the burden of their schedule on others.

You might not see suggestions in the following scenarios:

* When you’re composing an email during the 30 minutes before the recipients’ or your working hours.
* When there are more than 15 recipients in the **To** field.
* When you're sending an email to yourself.

>[!NOTE]
> Distribution lists and Microsoft 365 or Office 365 groups do *not* count as qualifying recipients for use by the delay-delivery feature.
>
> A shared mailbox in the **To** field, however, *does* count as a qualifying recipient. If a user has Full access permissions and can **Send as** or **Send on behalf of** the shared mailbox, that user counts as a qualifying sender.

With inline suggestions turned on, you can get up to two daily Delay delivery suggestions. To get more than two a day, you need to opt in to the Delay delivery plan.

You can opt in to the Delay delivery plan through Viva Insights or through the Insights Outlook add-in to get an unlimited number of inline suggestions for delaying email delivery to your coworkers. The Delay delivery plan is currently available in the Outlook desktop app for Windows. Be sure you are using Outlook for Windows 2016 version 1808 or later and build 16.0.12016.10000 or later.

## Use Delay delivery

When composing email in Outlook, you can delay delivery of an email as follows:

1. When you see a suggested delivery time while composing an email, such as **Thu, Nov 07 10:00 AM** (as shown in the graphic), select **Delay send** to confirm message delivery at that time.

   ![Delay delivery inline suggestion](../../Images/mya/use/delay-delivery.png)

2. An insight opens to show the scheduled time. You can select:

   * **Send** (within the email) to send the email at that scheduled time.
   * **Edit time** (within the insight) to change the suggested delivery time, and then select **Send** (within the email) to send the email at the new time.
   * **Cancel delay** (within the insight) to cancel the scheduled delivery time, and then select **Send** (within the email) to send the email now.

   ![Delay delivery insight options](../../Images/mya/use/delay-options.png)

3. After you send the email, it's kept in your Outlook **Sent items** folder until the scheduled delivery time, when it's automatically delivered for you.

   Before the message is sent, you can open the message and select:

   * **Send now** to ignore the scheduled delivery time and send the email now.
   * **Don't send** to stop the scheduled delivery time, which moves the email to your Outlook **Deleted items** folder.

   ![Delay delivery options after being sent](../../Images/mya/use/delay-options-2.png)

## Opt in with the dashboard

When you opt in to the Delay delivery plan, Viva Insights aligns email delivery with your coworker's working hours. You can opt in as follows:

1. Open your [dashboard](https://myanalytics.microsoft.com).
2. In **Settings** > **Protect time**, change the setting for **Delay delivery** to **On**.

   ![Turn on Delay delivery in the dashboard](../../Images/mya/use/delay-mya2.png)

## Opt in with Insights

You can also use the Outlook Insights add-in to opt in to the Delay delivery plan as follows:

1. In the Outlook Insights add-in, select **Settings** (gear icon) to open it.
2. Change the setting for **Delay delivery** to **On**.

   ![Turn on Delay delivery in the Insights add-in.](../../Images/mya/use/delay-add-in.png)

## To opt out

You can opt in or opt out of the Delay delivery plan as many times as you want. To turn it off:

* In the [dashboard](https://myanalytics.microsoft.com), select **Config Settings**, and then change the setting for **Delay delivery** to **Off**.
* Or in the Insights Outlook add-in, open **Settings** (gear icon), and then change the setting for **Delay delivery** to **Off** .

After you opt out of the Delay delivery plan, you can delay up to two email deliveries each day when the inline suggestions feature is turned on. To opt out of inline suggestions in Outlook, including delay-delivery inline suggestions, follow the steps in [Inline suggestions in Outlook](mya-notifications.md#opt-out-of-inline-suggestions).

## Video walk-through

Watch this video to take a closer look at Delay delivery experiences in Outlook.

<br><iframe src="https://player.vimeo.com/video/725822960?h=59923f2d8d" width="640" height="360" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>