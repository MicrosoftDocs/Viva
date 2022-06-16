---
title: Inline suggestions in Outlook
description: Describes what inline suggestions are in Outlook and how they work 
author: madehmer
ms.author: loreenl
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-personal
ms.prod: Mya
manager: helayne
audience: user

---

# Inline suggestions in Outlook

Inline suggestions in Outlook are brief data and AI-driven notifications that appear in Outlook while you are either reading or composing an email or a meeting invitation.

Inline suggestions can help boost your productivity and that of your team by displaying useful suggestions, tips, and best practices around managing email and running meetings. They help inform and guide you in making effective email and meeting decisions. They can also help you reclaim focus hours and build better collaboration habits, in addition to other practical benefits. [Types of inline suggestions](#types-of-inline-suggestions) lists some of what you might see in Outlook.

>[!Note]
>Only you can see your data, see [Privacy FAQ](../overview/mya-faq.md#privacy) for details.

## How to see inline suggestions

Inline suggestions are available in the latest versions of Outlook for the web and Outlook for Windows with Microsoft 365 or Microsoft 365 licenses. To see inline suggestions in Outlook for Windows, be sure that the following is in place on your computer:

* Outlook for Windows 2016 version 1808 or greater and build 16.0.10730 or greater.
* Outlook Insights add-in version 3.0.0.0 or higher. To check the installed version of the add-in, see [Exchange admin center](/exchange/architecture/client-access/exchange-admin-center). The add-in is installed at the tenant level, after which it can take up to eight days for the upgrade to propagate to all users. If you notice that the proper add-in version isn't installed in Outlook, you can add it by following the steps in [Add the Viva Insights Outlook add-in](../overview/mya-faq.md#add-the-viva-insights-outlook-add-in).
* Actionable messages are supported and enabled; see [Actionable messages in Outlook and Microsoft 365 Groups](/outlook/actionable-messages/).

In Outlook for Windows, inline suggestions will show up while reading or composing an email or a meeting invitation. In Outlook for the web, inline suggestions only show while reading email and meetings. These suggestions are not currently available in Outlook for Mac, Outlook for iOS, and Outlook for Android.

>[!Note]
>Inline suggestions are not available on mobile devices.

## Types of inline suggestions

The following are a few of the suggestions you might see in Outlook:

* [Delay delivery](#delay-delivery)
* [Suggested outstanding tasks](#suggested-outstanding-tasks)
* [Get more time to focus](#get-more-time-to-focus)
* [Plan your time away](#plan-your-time-away)
* [Protect your focus time](#protect-your-focus-time)
* [Shorten a meeting](#shorten-a-meeting)
* [Track email open rate](#track-email-open-rate)
* [Track email](#track-email)

## Opt out of inline suggestions

1. To opt out of inline suggestions in Outlook, select the **Viva Insights** icon on the Outlook Home ribbon. Or if you are using Outlook on the web, the **Viva Insights** icon is in the **ellipsis** (...) menu when reading an email message or when sending a new message.
2. Select the **Settings** (gear) icon in the Viva Insights add-in.

   ![Viva Insights settings](../../Images/mya/use/viva-insights-settings.png)

3. In **Settings**, for **Productivity inline suggestions**, change the setting to **Off**.

### If I am opted out, can I opt back in?

Yes. If you opt yourself out, you can opt back in any time to regain access to inline suggestions.

## Providing feedback

You can provide feedback for the inline suggestion  by selecting **Feedback** in the suggestion. In the Feedback section, select the "thumbs up" or a "thumbs down" and any other applicable feedback. If you select thumbs down, you'll see less of that suggestion.

You can also select **Turn off all notifications** if you would prefer not to receive any of the inline suggestions in the future.

You can also provide general feedback on anything by selecting the **smiley face** icon at the upper-right of the Viva Insights Add-in pane.

## Delay delivery

When you're composing an email in Outlook, Delay delivery will show you suggestions for scheduling email deliveries. You might see suggestions when:

* A recipient in the **To** field has an automatic out-of-office reply set up in Outlook. This helps minimize disruptions to recipients when they're away from work.
* You are outside of your working hours. If you're working flexible hours, this helps you send email when you're working without disrupting others' quiet hours.

You might *not* see suggestions when:

* You’re composing an email during the 30 minutes before the recipients’ or your working hours.
* There are more than 15 recipients in the **To** field.
* You're sending an email to yourself.

>[!Note]
> Distribution lists and Microsoft 365 or Office 365 groups do *not* count as qualifying recipients for use by the delay-delivery feature. A shared mailbox in the **To** field, however, *does* count as a qualifying recipient. If a user has Full access permissions and can **Send as** or **Send on behalf of** the shared mailbox, that user counts as a qualifying sender.

The delay-delivery inline suggestion is available to you if you’re using the Outlook desktop app. Be sure that you have Outlook for Windows 2016 version 1808 or greater and build 16.0.12016.10000 or greater.

When the inline suggestions feature is turned on, you can delay up two email deliveries each day. To get more than two daily delayed deliveries, you can opt in to the **Delay delivery** plan either in Viva Insights or in the Outlook Insights add-in. For details, see [Delay delivery plan](delay-delivery.md).

![Inline suggestion in email](../../Images/mya/use/delay-delivery.png)

**To delay delivery**

1. When you see a suggested delivery time while composing an email, such as **Thu, Nov 07 10:00 AM**, select **Delay send** to confirm message delivery at that time.
2. An insight opens to show the scheduled time. You can select:

   * **Send** (within the email) to send the email at that scheduled time.
   * **Edit time** (within the insight) to change the suggested delivery time, and then select **Send** (within the email) to send the email at the new time.
   * **Cancel delay** (within the insight) to cancel the scheduled delivery time, and then select **Send** (within the email) to send the email now.

   ![Delay delivery inline options](../../Images/mya/use/delay-options.png)

3. After you send the email, it's kept in your Outlook **Sent items** folder until the scheduled delivery time, when it's automatically delivered for you.

   Before the message is sent, you can open the message and select:

   * **Send now** to ignore the scheduled delivery time and send the email now.
   * **Don't send** to stop the scheduled delivery time, which moves the email to your Outlook **Deleted items** folder.

   ![Delay delivery options](../../Images/mya/use/delay-options-2.png)

## Suggested outstanding tasks

When composing or reading an email or a calendar invitation, you might see a suggestion to review suggested outstanding tasks for the sender of email or calendar invitation. There are task suggestions based on your email communications with the sender in the last 14 days and can help you keep tab of tasks you promised to get done or that team members asked you to complete.

![Suggested outstanding tasks](../../Images/mya/use/sugg-out-tasks-2.png)

You can select **See my tasks** to see and follow up on the potentially outstanding task in Insights. As shown in this image, you can open the related task (RE: Kat - Anisa chat) for more details, or select **Mark as done** or **Not a task** to remove it from your task list.

![Mark tasks as done](../../Images/mya/use/mark-as-done-55.png)

## Get more time to focus

While reading a calendar invitation, you might see a suggestion to **Book time for focused work** (if you have a heavy meeting load) so that you get more time to do deep work and reclaim your calendar for work that matters most.

Select **See suggested times** to open a pane that displays all the time available to focus in the coming week, with a couple of available slots every day. With one click you can add focus time to your calendar and get ready for distraction-free deep work. You can also book all available time for focused work with one click, thus setting you up for focused work over a longer duration.

![Book focus time](../../Images/mya/use/book-focus-time.png)

## Plan your time away

When composing an email or calendar invitation in Outlook about your upcoming time away from work, you might see a suggestion similar to the following.

![Plan your time away inline suggestion](../../Images/mya/use/inline-away-2.png)

Reduce the stress of planning for time away from work with the **Plan your time away** checklist. When you see an inline suggestion about it, select **Plan** to open the checklist and do the following:

* Resolve all your meetings in one place with a custom message about your scheduled time off.
* Compose your automatic replies and notify your team about your planned time off.
* Schedule focus time to wrap up tasks before you go and to catch up on work when you get back.

![Plan your time away checklist](../../Images/mya/use/time-away-checklist.png)

For more details about how to use the checklist, see [Plan your time away](use-the-insights.md#plan-your-time-away).

## Protect your focus time

If a meeting request conflicts with an existing focus-time block, you might see a suggestion to protect your focus-time block by moving the focus time to another time or to meet at another time.

![Protect focus time](../../Images/mya/use/protect-focus-time-2.png)

Select **See other available times** to open the Insights add-in pane and display all the available time in the coming week to reschedule the meeting. By selecting a time block you can propose a new time to the meeting organizer.

![Focus time send email](../../Images/mya/use/focus-time-send-email-2-50.png)

Select **Move your focus block** to open the Insights add-in and display all the available focus-time blocks in the coming week. By selecting a time block you can move the focus block that is "in conflict" to a new time, ensuring you have some time for deep work.

![Move focus block](../../Images/mya/use/move-focus-block-50.png)

## Shorten a meeting

_**Applies to**: This suggestion is currently available only to people who are enrolled in an applicable [service plan](../overview/plans-environments.md)._

When composing a meeting invitation with a duration of one hour, you might see a suggestion to shorten the meeting by 15 minutes to build some buffer time and save attendees time.

![Shorten a meeting](../../Images/mya/use/shorten-a-meeting-2.png)

Select **Shorten meeting** to decrease the meeting time by 15 minutes. This also opens the Insights add-in, where you can see the amount of time saved by all the participants in the meeting.

![Shorten a meeting; nice work](../../Images/mya/use/shorten-meeting-nice-work-50.png)

## Track email open rate

_**Applies to**: This insight is currently available only to people who are enrolled in an applicable [service plan](../overview/plans-environments.md)._

While reading an email that you've sent, you might see an insight that highlights what percentage of the email's recipients have opened the email.

![Track email open rate](../../Images/mya/use/track-email-3.png)

Select **See more insights** to see how many people have opened or forwarded your email and the average time that they spent reading that email, plus similar information for any attachments on that email. This information can help you follow up with recipients if needed and/or tailor your communication style to get the job done.

![Email open rates](../../Images/mya/use/email-open-rates-1.png)

## Track email

_**Applies to**: This suggestion is currently available only to people who are enrolled in an applicable [service plan](../overview/plans-environments.md)._

When composing an email to more than five recipients, you might see a suggestion that reads "Insights can track the email."

Select **Track this email** to see the email open rate and more statistics about this email. This information becomes available 15 minutes after you sent the email. You can see this information by opening the sent email or by opening the Insights add-in and selecting **Track email open rates**.
