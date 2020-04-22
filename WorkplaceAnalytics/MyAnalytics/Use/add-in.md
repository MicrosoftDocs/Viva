---

title: Insights Outlook add-in
description: All the individual Outlook Add-in topics, displayed as one in MyAnalytics
author: paul9955
ms.author: madehmer
ms.topic: article
localization_priority: priority 
ms.prod: mya

---

# Insights Outlook add-in

_**Applies to:** MyAnalytics elements are available in varying levels to users of different Microsoft Office 365 and Microsoft 365 plans. See [MyAnalytics plans and environments](../overview/plans-environments.md) for details. Also see [How do I find my plan?](../overview/mya-faq.md#q4-how-can-i-find-out-what-my-plan-is)_

Did you ever miss an important email or forget a commitment you made to your co-workers? Do meetings and emails tend to take over your calendar? Do you ever wish to see reminders for 1:1 meetings with your manager, direct reports, or other top collaborators? Would you like to be notified if an upcoming meeting doesn't have a quorum?

If your answer to any of these questions is _yes_, the Outlook add-in provides actionable insights to help you stay on top of your tasks and get more done.

This add-in is an extension of your Outlook experience and works within Outlook to help you gain focus time, maintain your work relationships, plan time away from work, and improve your overall work-life balance.

> [!Note]
> Only you can see your data, see [Privacy FAQ](../overview/mya-faq.md#privacy) for details.

## What you might see

In Outlook, open the add-in by selecting the **Insights** icon in the Outlook **Home** ribbon. If you are using Outlook on the web, open an email message, select the **ellipsis** (**...**) in the top-right corner of your email message, and then select **Insights**. (For easier access in Outlook on the web, you can pin the Insights Add-in to the quick access pane. See [Pin the add-in](#pin-the-add-in) for details.)

You'll see Insights similar to the following in the right pane in Outlook:

![Insights icon](../../images/mya/overview/insights-view.png)
![Insights panel](../../images/mya/overview/insights-cards-14.png)
<!--
## Plan your time away

Studies show that 70 percent of Americans don't use their paid time off. Taking time off work helps reduce stress and burnout, and improve work-life balance and overall wellbeing.

You can use Insights to help you reduce stress by helping plan your time away on your calendar, including helping you:

* Resolve all your meetings in one place with a custom message about your scheduled time off.
* Compose your auto-reply messages and notify your team about your scheduled time off.
* Schedule focus time to wrap up tasks before you go and to catch up on work when you get back.

You can plan your schedule with these planning options all at one time or individually as you get closer to the date. You can also come back at any time and change details before you go. Insights will track your progress and update what's done or not as you plan. For example, this shows only the first task as done:

   ![Insights plan your time away task list](../../images/mya/overview/insights-plan-time-away.png)

**To plan your time away**

1. In the **Insights** pane, select **Plan your time away**.
2. In **Select dates**, select the date range for your time off, and then select **Schedule**.

   ![Insights select dates](../../images/mya/overview/insights-select-dates.png)

3. In **Set automatic replies**, compose or edit the automatic reply message that people will receive when they send you messages or invites while you're away from work. You can select to send the same message to people inside and outside your organization, or you can compose a different auto-reply message for those outside your organization, and then select **Save**.

   ![Insights auto-reply email](../../images/mya/overview/insights-auto-reply.png)

4. In **Notify collaborators**, select who you want to notify about your upcoming holiday plans, and then:

   * Select **Open new email draft** to compose the message.
   * Select **Open new meeting invitation** to add your scheduled time off on their calendars.

5. In **Resolve meetings** > **Review meetings**, you can see all the meetings that are scheduled during your time off. Any meetings that you scheduled will be canceled and any meetings you're an attendee of will be declined:

   * In **Decline and cancel meetings with this message**, edit the message that'll be sent with the meeting invitation decline or cancel message.
   * In **Select meetings to decline or cancel**, select which meetings you want to cancel or decline, and then select **Confirm**. Or you can select **Open** next to a meeting to see more details, reschedule, and resolve if differently than the others on your calendar.

    ![Insights resolve meetings](../../images/mya/overview/insights-resolve-meetings.png)

6. In **Book time to focus**, Insights will show you a what time is available on your calendar to focus on wrapping up work before you go and on catching up after you get back.

    ![Insights book focus time](../../images/mya/overview/insights-book-focus.png)
-->
<!-- Coming soon-> When you get back, Insights helps you catch up on important email and review new documents and activity that occurred while you were away:

![Insights welcome back](../../images/mya/overview/insights-welcome-back.png)
-->

## Email read statistics

_**Applies to:** MyAnalytics elements are available in varying levels to users of different Microsoft Office 365 and Microsoft 365 plans. See [MyAnalytics plans and environments](../overview/plans-environments.md) for details. Also see [How do I find my plan?](../overview/mya-faq.md#q4-how-can-i-find-out-what-my-plan-is)_

Insights can tell you how many people have opened your email and the average time they spent reading that email. In general, it informs you about email that you sent to five or more Office 365 users who are internal to your organization. (For more information about which email messages are reported about, see [Reporting details](#reporting-details).)

After you send an email message, it can take up to 30 minutes before Insights informs you about it. If the email is sent from a delegated mailbox with "send on behalf" permission, the delegate can see the read statistics.

Insights shows the open rate for the sent email that is open in Outlook. It also groups open rate information for qualifying sent items into a single summary card that you can select and expand to see a more detailed view.

### Reporting details

Insights does not display read information about every email that you send, such as in the following circumstances.

#### Requirement: qualifying messages

Read statistics are shown only for _qualifying messages_. A qualifying message is an email message that is sent to five or more qualifying recipients. A qualifying recipient is a person who is in the same company as the sender and has a cloud mailbox. Distribution lists are expanded before counting qualifying recipients.

#### Exceptions to qualifying messages

Insights does not report about email messages in the following categories:

* Email that was sent from a shared mailbox
* Email that was sent more than 14 days ago.
* Email in which the total number of recipients (the sum of all of the recipients in the To:, Cc:, and Bcc: fields) is less than five.
* Email sent to modern groups. (If users are following the modern group, they are included in the count.)

#### Open rate

The Insights add-in reports the open rate within 30 minutes of when qualifying email was sent by you, as shown in the following table. Note the following:

* For open rates lower than the minimum threshold, the threshold value is reported. For example, when 20% of 10 email recipients open the email, Insights displays the open rate as _&lt; 25%_.
* If the actual open rate falls between the "Minimum" and "Maximum" values shown in the table, then the actual open rate is reported.
* For open rates higher than the maximum threshold, the threshold value is reported. For example, when 98% of the email recipients open the email, the maximum value in the table will be _&gt; 95%_.

   | Number of recipients | Open rate reported |
   | ------- | ------ |
   | 5 - 10  | Minimum: 25% <br>Maximum: 75% |
   | 11 - 20 | Minimum: 10% <br>Maximum: 90% |
   | &gt; 21 | Minimum: 5%  <br>Maximum: 95% |

MyAnalytics respects user privacy; this is why approximated values are reported and individual recipient information is not shown. For more details, see the [Email read rates](../overview/privacy-guide.md#email-read-rates). To see who opened an email, use [Outlook's request read receipts](https://support.office.com/article/add-and-request-read-receipts-and-delivery-notifications-a34bf70a-4c2c-4461-b2a1-12e4a7a92141).

**To see read information about sent emails**

1. On the **Home** ribbon, select the **Insights** icon. If the Insights panel isn't already open, it opens now.

   > [!Note] 
   > If you see a "Welcome!" message, select **Get started**.

2. On the **Insights** panel, select one of the following two cards:

   a. **In-context email open rate**. This card provides read statistics for the sent email that you currently have open in Outlook.

     ![In-context email open rate](../../Images/mya/use/in-context-card-59.png) 

   b. The **Track email open rates** card. This card provides read statistics for all sent emails.  

     ![Track email open rates](../../Images/mya/use/step-1-track-open-rates.png)

    The panel in the card that you selected (in either step 2a. or step 2b.) states the email subject line and shows a summary of the open rate, the open rate (sometimes expressed as a percentage), and the number of forwards.

    ![Email open rates](../../Images/mya/use/step-2-four-emails.png)

<!-- REMOVED PER RISHABH 4 SEPT 2019
### Read statistics details

Note the following about the reporting of read-statistics data: 

 * **Length of availability.** Read statistics for an email are present only for a period of 14 days. (Read statistics are not computed for mails that have been sent more than 14 days ago.)
 * **Time until availability.** It usually takes 15 to 30 minutes to compute precise results for read statistics for your emails.
 * **Five-recipient limit.** An email qualifies for read statistics only if it was sent to more than five recipients in the _To_, _Cc_ and _Bcc_ fields combined. 
-->

<!--
    Based on the length of the message, Insights estimates how long a person needs to read it. It uses that number to decide whether people glanced, skimmed, or read the email, and informs you of this in a card.
 
    ![Email open rates](../../Images/mya/use/email-open-rates-2.png)

    Depending on how many people opened the email and how long they spent reading it, Insights might suggest that you follow up on your email, or it might show tips to help improve email communication.
-->

## Follow up on your tasks

MyAnalytics can help you follow up on requests you asked of others in email. MyAnalytics will automatically find tasks you requested of others based on your sent mails. For example:

* "Can you send me this year's latest report?"
* "Everyone, please complete your performance evaluations by the end of the week."
* "Cancel my RSVP for Carrin Patman's lunch scheduled early next week."

For one or more of these types of requests in your sent email in the last 14 days, you'll see a follow-up summary card in your Outlook Insights panel.

**To see your follow-up card**

1. On the Outlook **Home** ribbon, select the **Insights** icon.
2. In the **Insights** panel, you'll see the **Follow up on your requests** card.

   ![Follow-up card](../../Images/mya/use/follow-up-340.PNG)

3. Select the card to see more details and to do one or more of the following:

   * Select the email subject line from which the task was extracted to open that specific email.
   * Select **Follow up** to open the latest instance of the email.
   * Select **Mark as done** if the task is complete. Follow-ups disappear after two weeks or after you mark them as done.
   * If this task isn't a follow-up, select the **ellipsis** (**…**) at bottom right, and then select This isn't' a follow up.

   ![Follow-up card details](../../Images/mya/use/follow-up-details-340.PNG)

> [!Note]
> This card is only available in English.

## Meeting preparation

Meetings are vital for healthy collaboration. Better meeting practices can improve productivity, information sharing, innovation, decision-making, and team connectedness. Read more about best practices for running effective meetings in [this playbook](../use/mya-adoption/MyAnalytics-meetings-september-2018.pdf).

The meeting preparation card shows you a list of upcoming meetings that you have organized, and it helps you evaluate whether each meeting is ready to go. 

#### To view and use the meeting preparation card

1. On the **Home** ribbon of Outlook, select the **Insights** icon. If the **Insights** panel isn't already open, it opens now. 

2. On the **Insights** panel, locate the **Prepare for your meetings** card: 
 
    ![Meeting preparation card](../../Images/mya/use/meeting-prep-card.png)

    This card provides information about meetings that you have organized for this week and next week (up to 10 business days in the future) and it helps you evaluate the state of those meetings. 

3. Select the **Prepare for your meetings** card. This opens a panel that displays insights cards for each of your upcoming meetings: 

    ![Meeting preparation panel](../../Images/mya/use/meeting-prep-panel.png)
 
These insights cards inform you of the following:

| Card section | Notes | Recommendations |
| ------------ | ----- | --------------- |
| (Card title) | Meeting title and time of occurrence |
| Attendees    | The percentage of invitees who have accepted, and the number of invitees. Click **See details** for more information. | **Ensure that you have a quorum** before the meeting. Consider sending a reminder to attendees if you haven't heard from them. |
| Agenda       | **Yes** or **No** indicates whether the meeting invitation includes an agenda. | **Agendas** often make a meeting run smoother. If your meeting requires an agenda, select **Agenda** in the card. This opens the meeting invitation, where you can add an agenda. |
| Attachments  | This section shows how many attachments the invitation has, it displays their titles and their storage location (online or locally), and it lets you click to see more details. It also provides a link that you can select to open the attachment, if the attachment is stored online. |  
| Online meeting link | **Yes** or **No** indicates whether the meeting invitation includes a link for joining the meeting online. | **Be an inclusive meeting organizer**. If you have attendees who are working remotely, consider adding an online link to your meeting. To do this, select **Online meeting link** to add one.  |
| Preparation time | This section provides options to book either 15 minutes or 30 minutes of preparation time right before the meeting. This option only appears if there is an available slot. Booked time appears on your calendar and references the meeting, as "Preparation time for [meeting title]." You can also cancel the meeting-preparation time or delete it directly from your calendar. | **Be prepared**. If you need travel time or have other tasks that need to be done immediately before the meeting to prepare for it, consider booking preparation time.  |

_This card shows the **Attachments** section in its expanded state, which lets you see more details about the attachments:_

![Meeting preparation panel, expanded](../../Images/mya/use/meeting-prep-panel-expanded.png) 

## Catch up with your team

People managers often have hectic schedules, and it can be tough to stay in close contact with each team member. MyAnalytics brings together all the information managers need to stay caught up and respond quickly to important requests. 

As a manager, you can:

 * Schedule 1:1 time with a team member (or reschedule if a conflict comes up)
 * Act on tasks you promised to get done or that team members asked you to complete
 * Review important emails and documents from team members that you haven’t read yet

This feature is only available for MyAnalytics users who have direct reports listed in Azure Active Directory. If you are a manager but do not see this feature, contact your Office 365 administrator.

#### To use the catch up feature

1. On the **Home** ribbon of Microsoft Outlook, [open Insights](#what-you-might-see).

2. Select **Catch up with your team**:

   ![Catch up with your team](../../images/mya/use/catch-up.png)

   The **Insights** pane shows team members with whom you can reconnect and actions you can take to do so:

   ![Team member card Debra](../../images/mya/use/connect-actions-debra-75-90.png)

#### To edit your team list

 * If you notice that your team member list is inaccurate, select **Edit team** to add or remove team members, as shown here:

   ![Update team members](../../images/mya/use/edit-team75-75-80.png)

Any changes you make apply only to your MyAnalytics experience; they do not synchronize back to Azure Active Directory.

## Pin the add-in

If you're using Outlook on the web, you can pin the Insights add-in to the quick access pane for easier access.  

**To pin the add-in to the quick access pane**

1. In Outlook on the web, select the **Settings** (gear) icon to open the **Settings** panel:

    ![OWA Settings panel](../../images/mya/use/owa-settings.png) 

2. In the **Settings** panel, select **View all Outlook Settings**.

3. Be sure **Mail** is selected in the left panel, and in the center panel, select **Customize actions**:

    ![Customize actions](../../images/mya/use/customize-actions.png) 

4. In the right pane, in the **Message surface** area, select **Insights**:

    ![Message surface/Insights](../../images/mya/use/msg-surface-insights.png) 

5. In the right pane, in the **Toolbar** area, select **Insights**:

    ![Toolbar/Insights](../../images/mya/use/toolbar-surface-insights.png) 

6. Save your new settings:

    ![Save settings](../../images/mya/use/save-settings.png) 

## Privacy by design 

[!INCLUDE [Privacy by design](../includes/privacy-by-design.md)]

<!-- PER PETERB 23 JULY 2019: DO NOT PUBLISH THIS. 
IT HAS NOT YET SHIPPED EXTERNALLY. HE WILL LET US KNOW WHEN TO PUBLISH. 

## To add tasks to your focus time

1.    In Outlook, select **Insights**.

2.    In the Insights panel, select the **View outstanding tasks** card. This opens the **SUGGESTED TASKS** panel.

3.    On a card for which you want to add a task, select the ellipsis. This opens a menu with three options:

     * If you select **Book time to review**, Outlook finds new upcoming 30-minute slots in your calendar and proposes them to you. 

       Then, select the plus sign to add this task to your calendar for the displayed time period. Outlook will book this as additional focus time and mark your status during this period as "Do not disturb." In your calendar, this time is labeled "Focus time (tasks included)."

     * If you already have focus time booked, you can select **Add to focus time**. Outlook then finds existing focus time periods in your calendar and proposes them to you. 

       Select **Add** to add this task to the already scheduled focus time block on your calendar.  
     * If you select **This isn't a task**, Outlook removes the card from the **SUGGESTED TASKS** panel.

-->

## Opt out of the Insights Outlook add-in

1. Open your [dashboard](https://myanalytics.microsoft.com).
2. Select the **Settings** (gear) icon in the top right.

    ![MyAnalytics settings](../../Images/mya/use/mya-gear-settings.png)

3. Under MyAnalytics, select **Settings**.
4. For **Insights Outlook add-in**, set the control to **Off**.

    ![Slider in off position](../../Images/mya/use/add-in-opt-in-out.png)
  
5. Select **Save** to save your changes.

> [!NOTE]
> It might take up to 24 hours for your saved changes to take effect.

### If I am opted out, can I opt back in?

Yes; if you opt yourself out or if an admin opts you out, you can opt back in any time to regain access to the Insights Outlook add-in.
