---

title: Use Insights
description: Learn how to use the options in the Insights Outlook add-in.
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: priority 
ms.prod: mya

---

# Use Insights

The following helps you get the most out of the Insights Outlook add-in:


 * [Follow up on your tasks](#follow-up-on-your-tasks)
 * [Prepare for your meetings](#prepare-for-your-meetings)
 * [Track email and document open rates](#track-email-and-document-open-rates)
 * [Catch up with your team](#catch-up-with-your-team)
 * [Plan your time away](#plan-your-time-away)

 ## Follow up on your tasks

MyAnalytics can help you follow up on requests you asked of others in email. MyAnalytics will automatically find tasks you requested of others based on your sent mails. For example:

* "Can you send me this year's latest report?"
* "Everyone, please complete your performance evaluations by the end of the week."
* "Cancel my RSVP for Carrin Patman's lunch scheduled early next week."

For one or more of these types of requests in your sent email in the last 14 days, you'll see a follow-up summary in the Outlook Insights pane.

**To follow up on a task**

1. On the Outlook **Home** ribbon, select the **Insights** icon.
2. In **Insights**, select **Follow up on your requests**.

   ![Follow-up card](../../Images/mya/use/follow-up-340.PNG)

3. In **Follow up on your requests**, you can do one or more of the following:

   * Select the email subject line from which the task was extracted to open that specific email.
   * Select **Follow up** to open the latest instance of the email.
   * Select **Mark as done** if the task is complete. Follow-ups disappear after two weeks or after you mark them as done.
   * If this task isn't a follow-up, select the **ellipsis** (**…**) at bottom right, and then select This isn't' a follow up.

   ![Follow-up card details](../../Images/mya/use/follow-up-details-340.PNG)

> [!Note]
> This option is only available in English.


## Prepare for your meetings

Meetings are vital for healthy collaboration. Better meeting practices can improve productivity, information sharing, innovation, decision-making, and team connectedness. Read more about best practices for running effective meetings in [this playbook](../use/mya-adoption/MyAnalytics-meetings-september-2018.pdf).

In **Prepare for your meetings**, you'll see a list of upcoming meetings that you have organized, where you can evaluate if a meeting is ready to go.

#### To prepare for a meeting

1. If the **Insights** pane isn't already open, select the **Insights** icon on the Outlook **Home** ribbon.

2. In the **Insights** pane, select **Prepare for your meetings**. 
 
    ![Meeting preparation card](../../Images/mya/use/meeting-prep-card.png)

    This shows information about meetings that you have organized for this week and next week (up to 10 business days in the future) and it helps you evaluate the state of those meetings. 

3. In **Prepare for your meetings**, you'll see details about each of your upcoming meetings.

    ![Meeting preparation panel](../../Images/mya/use/meeting-prep-panel.png)
 
| Option | Description | Tips |
| ------------ | ----------- | --------------- |
| Attendees    | The percentage of invitees who have accepted, and the number of invitees. Select **See details** for more information. | **Ensure that you have a quorum** before the meeting. Consider sending a reminder to attendees if you haven't heard from them. |
| Attachments  | This section shows how many attachments the invitation has, it displays their titles and their storage location (online or locally), and it lets you click to see more details. It also provides a link that you can select to open the attachment, if the attachment is stored online. |  
| Online meeting link | **Yes** or **No** indicates whether the meeting invitation includes a link for joining the meeting online. | **Be an inclusive meeting organizer**. If you have attendees who are working remotely, consider adding an online link to your meeting. To do this, select **Online meeting link** to add one.  |
| Preparation time | This section provides options to book either 15 minutes or 30 minutes of preparation time right before the meeting. This option only appears if there is an available slot. Booked time appears on your calendar and references the meeting, as "Preparation time for [meeting title]." You can also cancel the meeting-preparation time or delete it directly from your calendar. | **Be prepared**. If you need travel time or have other tasks that need to be done immediately before the meeting to prepare for it, consider booking preparation time.  |

<!-- THIS ROW WAS REMOVED FOR NOW (2 JUNE 2020) PER PRAMOD:
| Agenda    | **Yes** or **No** indicates whether the meeting invitation includes an agenda. | **Agendas** often make a meeting run smoother. If your meeting requires an agenda, select **Agenda** to see the meeting invitation, where you can add an agenda. |
-->

The following shows the **Attachments** section expanded to show more details about the attachments:

![Meeting preparation, expanded](../../Images/mya/use/meeting-prep-panel-expanded.png) 

## Track email and document open rates

_**Applies to:** MyAnalytics elements are available in varying levels to users of different Microsoft Office 365 and Microsoft 365 plans. See [MyAnalytics plans and environments](../overview/plans-environments.md) for details. Also see [How do I find my plan?](../overview/mya-faq.md#q4-how-can-i-find-out-what-my-plan-is)_

Insights can tell you how many people have opened your email and the average time they spent reading that email. In general, it informs you about email that you sent to five or more Office 365 users who are internal to your organization. (For more information about which email messages are reported about, see [Reporting details](#reporting-details).)

Insights also tells you how many email recipients opened a document that you shared in the email as a link or as an attachment (this insight works for documents that are stored in SharePoint or in OneDrive for Business).

After you send an email message, it can take up to 30 minutes before Insights informs you about it. If the email is sent from a delegated mailbox with "send on behalf" permission, the delegate can see the read statistics.

Insights shows the open rate for the sent email that is open in Outlook. It also groups open rate information for qualifying sent items into a single summary that you can select and expand to see a more detailed view.

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

MyAnalytics respects user privacy. For this reason, the Insights add-in does not show information about individual recipients, and -- when necessary to protect privacy -- it reports approximated values only.

**Open-rate value thresholds**

Within 30 minutes of when you sent qualifying email, the Insights add-in  reports the actual or an approximated open rate, as described here: 

* **Below minimum.** For open rates lower than the minimum threshold, the threshold value is reported. For example, when 20% of 10 email recipients open the email, Insights displays the open rate as "_&lt; 25%_."
* **Between thresholds.** If the actual open rate falls between the "Minimum" and "Maximum" values shown in the table, then the actual open rate is reported.
* **Above maximum.** For open rates higher than the maximum threshold, the threshold value is reported. For example, when 98% of the 25 email recipients open the email, Insights displays the open rate as "_&gt; 95%_."

   | Number of recipients | Open rate reported | 
   | ------- | ------ |
   | 5 - 10  | Minimum: 25% <br>Maximum: 75% |
   | 11 - 20 | Minimum: 10% <br>Maximum: 90% |
   | &gt; 21 | Minimum: 5%  <br>Maximum: 95% |

 For more information, see [Email read rates and document open rates](../overview/privacy-guide.md#email-read-rates-and-document-open-rates). To see who opened an email, use [Outlook's request read receipts](https://support.office.com/article/add-and-request-read-receipts-and-delivery-notifications-a34bf70a-4c2c-4461-b2a1-12e4a7a92141).

**To see read information about sent emails**

1. If the Insights pane isn't already open, select the **Insights** icon in the Outlook **Home** ribbon to open it.

   > [!Note] 
   > If you see a "Welcome!" message, select **Get started**.

2. In **Insights**, select one of the following:

   a. **In-context email open rate** - Shows read statistics for the sent email that you currently have open in Outlook. It also provides open rates for linked or attached documents that are stored in OneDrive for Business or SharePoint.  

     > [!Note] 
     > In rare cases, the document open rate can be higher than the email open rate. This can happen when recipients open the document through sources other than the email in which it was shared.   

     ![Doc open rate exceeds email open rate](../../images/mya/use/docs-exceed-emails-51.png) 

   b. **Track email open rates** - Shows read statistics for all sent emails.  

     ![Track email open rates](../../images/mya/use/step-1-track-open-rates.png)

    The option you selected (in step 2a or step 2b) shows the email subject line and a summary of the open rate, the open rate (sometimes expressed as a percentage), and the number of forwards.

    ![Email open rates](../../images/mya/use/step-2-four-emails.png)

## Catch up with your team

People managers often have hectic schedules, and it can be tough to stay in close contact with each team member. MyAnalytics brings together all the information managers need to stay caught up and respond quickly to important requests. 

As a manager, you can:

 * Schedule 1:1 time with a team member (or reschedule if a conflict comes up)
 * Act on tasks you promised to get done or that team members asked you to complete
 * Review important emails and documents from team members that you haven’t read yet

This feature is only available for MyAnalytics users who have direct reports listed in Azure Active Directory. If you are a manager but do not see this feature, contact your Office 365 administrator.

#### To catch up with your team

1. On Outlook or in Outlook on the web, [open the Insights add-in](add-in.md#open-the-insights-add-in).

2. Select **Catch up with your team**:

   ![Catch up with your team](../../images/mya/use/catch-up.png)

   The **Insights** pane shows team members with whom you can reconnect and actions you can take to do so:

   ![Team member card Debra](../../images/mya/use/connect-actions-debra-75-90.png)

#### To edit your team list

 * If you notice that your team member list is inaccurate, select **Edit team** to add or remove team members, as shown here:

   ![Update team members](../../images/mya/use/edit-team75-75-80.png)

Any changes you make apply only to your MyAnalytics experience; they do not synchronize back to Azure Active Directory.

## Plan your time away

Taking time off from work helps reduce stress and burnout and improve overall wellbeing. However, research shows that a lack of planning can reduce the benefits of taking a vacation.

The Plan your time away Insights checklist can help reduce the stress of planning for upcoming time away from work. This single tool helps you:

* Resolve all your meetings in one place with a custom message about your scheduled time off.
* Compose your autoreplies and notify your team about your planned time off.
* Schedule focus time to wrap up tasks before you go and to catch up on work when you get back.

You can plan your schedule with these options all at one time or individually as you get closer to the date. You can also come back at any time and change details before you go. Insights will track your progress and update which actions are done.

![Insights plan your time away task list](../../images/mya/use/insights-time-away.png)

**To use Plan your time away**

1. If Insights isn't shown, select the **Insights** icon on your Outlook **Home** ribbon.
2. In the **Insights** pane, select **Plan your time away** to see a checklist of planning options.

   * **Select dates** - Select **Start** and **End dates** for when you'll be out of office, and then select **Schedule**, which sets up an Out-Of-Office appointment on your calendar for the selected dates.

     > [!Tip]
     > Updating your calendar with out-of-office information is a best practice that’ll set the right expectations with coworkers who want to connect with you. 

     ![Insights update calendar](../../images/mya/use/insights-select-dates.png)

   * **Set automatic replies** - Compose and save an out-of-office reply message here. Your automatic replies will be sent during the start and end dates you selected. You can select to send the same message to people inside and outside your organization, or you can compose a different auto-reply message for those outside your organization, and then select **Save**.

     ![Insights auto-reply email](../../images/mya/use/insights-auto-reply.png)

   * **Notify collaborators** - You'll see a list of people that you collaborated with in the last four weeks. You can select to notify them through an email or meeting invitation, and then select **Compose**.

     ![Insights notify collaborators](../../images/mya/use/insights-notify.png)

   * **Resolve meetings** - You'll see a list of meetings you either organized or accepted for while you're away.

     * **Decline and cancel meetings with this message** - Edit the message that'll be sent to decline or cancel the meeting invitation.
     * **Select meetings to decline and cancel** - Select which meetings you want to decline or cancel, or use **Select all** to decline or cancel all the meetings listed. When you're done, select **Confirm**. You can also select **Open** next to a meeting to see more details about it.

     > [!Tip]
     > By using this option to quickly and easily resolve all your meetings, you're saving valuable planning time while also respecting your coworkers time.

       ![Insights resolve meetings](../../images/mya/use/insights-resolve-meetings.png)

   * **Book time to focus** - You can schedule time to focus on wrapping up work before you go, and then on catching up after you get back. Select the **plus sign** (+) next to the available **Focus time** slots, and then select **Done** to add them to your calendar.

     > [!Tip]
     > With this time scheduled, you'll know you have time to get everything done both before you go and after you get back.

     ![Insights book focus time](../../images/mya/use/insights-focus-time.png)

## Related topics

* [Insights Outlook add-in](add-in.md)
* [MyAnalytics elements](MyA-elements.md)
