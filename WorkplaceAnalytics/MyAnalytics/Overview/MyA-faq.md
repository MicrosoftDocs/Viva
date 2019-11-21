---
# Metadata Sample
# required metadata

title: MyAnalytics FAQ
description: Frequently asked questions about MyAnalytics
author: paul9955
ms.author: v-midehm
ms.topic: article
localization_priority: once
ms.prod: mya

---

# Frequently asked questions for MyAnalytics

> [!Note]
> Productivity insights powered by MyAnalytics are becoming broadly available to all Office 365 users. [Learn more](./plans-environments.md) about the experiences that users will get in each plan.

  * [Privacy](#privacy) applies to everyone

The other sets of questions and answers are grouped by role:

   * For [MyAnalytics users](#for-myanalytics-users)
   * For [IT administrators](#for-it-administrators)

## Privacy

#### Q1. Who can see my data?

Only you can see your data. The statistics and insights that are generated from your data are for your eyes only. Your manager or system administrator cannot view your personal data.

For more details, see the [MyAnalytics privacy guide](Privacy-Guide.md).

#### Q2. How does MyAnalytics protect my data?

MyAnalytics uses data from your Office 365 mailbox, namely data about your email and your meetings plus data about your calls and chats in Teams or in Skype for Business.

MyAnalytics stores your data in your mailbox itself, and gets the same protection that your email and calendar itself gets. This means your data is protected the same way your email and calendar information is kept private and protected.

Every calculation that MyAnalytics performs is based on data that you, yourself, can get by gathering and examining metadata of your email, meetings, calls, and instant messages, such as their start and end times and their subject lines. In other words, MyAnalytics automates what would otherwise be a painstaking task; these automatic calculations provide you with transparency into your workplace collaboration habits.

MyAnalytics does not have any tracking software running on your computer.

#### Q3. What data does MyAnalytics use?

> [!Note]
> MyAnalytics processes the data as described in the [Privacy Guide](privacy-guide.md).

**MyAnalytics uses:**

 * Information from email items:

   * Metadata - which includes the email's timestamp, sender, recipients, and "read" signal
   * Statements that people have made in email body text - these statements are used to create [task cards](../use/MyA-Outlook-add-in/MyA-Add-in-To-do.md) for your use only
   * Actions of other users who receive your email - for example, whether or not they have opened your email. (This would be used only in aggregate form, to protect individual privacy.)

 * Information from calendar items:
  
   * Type (meeting or appointment)
   * Status (busy, free, out-of-office, tentative)
   * Category
   * Subject
   * Duration
   * Attendees

 * Information from Teams and from Skype for Business:

   * MyAnalytics counts audio calls, video calls, and chats that people make in Teams and in Skype for Business as collaboration activities.

 * OneDrive SharePoint data: MyAnalytics shows a count of OneDrive and SharePoint documents that you have worked on. 

 * _Used only if you have opted in_: Data derived from activities on your computer, such as applications that you've used and websites that you've visited.

**MyAnalytics does not use:**

Email and calendar data from people outside of your organization, with the following exception: MyAnalytics uses data that is present in your own Office 365 mailbox. For example, if you conduct a meeting with a person outside of your organization, the start and end times of that meeting can be found in your mailbox and therefore are visible to you. This data, therefore, can be used in computations about your collaboration history.

## For MyAnalytics users

### Data sources

#### Q1. Can data be extracted from on-premises installations of Microsoft Exchange or Skype for Business?

No. Only Exchange Online, Skype for Business Online, and Teams are used as sources of MyAnalytics data.

### Meetings

#### Q1. Does "meeting time" include time that I block out for personal work on my calendar?

If you block out your calendar for personal work by using an appointment (see [Create or schedule an appointment](https://support.office.com/article/create-or-schedule-an-appointment-be84396a-0903-4e25-b31c-1c99ce0dacf2)) or by creating a meeting with just yourself, this time does not count as meeting time and will count as focus time.

### Focus time

#### Q1. Does “focus time” exclude time that I block out for personal work on my calendar?

If you block out your calendar for personal work by using an appointment (see [Create or schedule an appointment](https://support.office.com/article/create-or-schedule-an-appointment-be84396a-0903-4e25-b31c-1c99ce0dacf2)) or by creating a meeting with just yourself, this time can count as focus time. For more details, see [Focus](../Use/focus.md). To exclude focus time, right-click the appointment and set **Show As** to **Out of Office**.

#### Q2. Can I change my settings to make time outside of work more accurate?

Yes. You can change your time zone and your working time in your [Outlook settings](https://outlook.office.com/calendar/options/calendar/view/appearance).

#### Q3. Why does my focus time seem incorrect or inaccurate?

Try the following to troubleshoot your focus-time totals:

1. Verify that your work time and time zone settings are correct. (See  [Outlook settings](https://outlook.office.com/calendar/options/calendar/view/appearance).)
2. For more details about focus time, see [Focus](../Use/focus.md).  

#### Q4. How do I tell MyAnalytics that I am on vacation?

If you plan to go on vacation (or on holiday), create an Outlook calendar event that includes the days of your vacation and set the status to **Out of Office**. MyAnalytics will count zero focus and meeting hours for you while you're away.

### Opt out

#### Q1. Can I opt out of MyAnalytics? And if I do (or if an admin opts me out), can I opt back in later?

Yes to both questions. You can opt out of access to individual parts of MyAnalytics or out of all of MyAnalytics at once. And you can opt back in again later, if you want.

See the following for details:

##### Opt out of all of MyAnalytics

 * [Opt out of MyAnalytics](../use/opt-out-of-mya.md)

##### Opt out of individual parts of MyAnalytics

 * [Opt out of the MyAnalytics dashboard](../use/dashboard-2.md#opt-out-of-the-myanalytics-dashboard)
 * [Opt out of the weekly email digest](../use/email-digest-2.md#opt-out-of-email-digests)
 * [Opt out of the Insights Outlook add-in](../use/add-in.md#opt-out-of-the-insights-outlook-add-in)
 * [Opt out of inline suggestions](../use/mya-notifications.md#opt-out-of-inline-suggestions)

#### Q2. Can I add or remove the Insights Outlook add-in?

Yes, you can. But first, what's the difference between "opt out" and "remove"? 

 * **Opt out:** If you opt out, you lose access to the feature. (But remember that you can opt back in if you change your mind. To do so, follow the steps in [Opt out of the Insights Outlook add-in](../use/add-in.md#opt-out-of-the-insights-outlook-add-in) but in step 4, set the control to **On**.) 
 * **Remove:** If you [remove the Insights Outlook add-in](#remove-the-insights-outlook-add-in), not only do you lose access to the feature, its icon is also removed from your Outlook ribbon. (Note that you can change your mind about this, as well: See [Add the Insights Outlook add-in](#add-the-insights-outlook-add-in)).  

##### Remove the Insights Outlook add-in

Follow these steps to remove the Insights add-in from your Outlook ribbon.

> [!Note] 
> This procedure also removes [inline suggestions in Outlook](../use/mya-notifications.md).

1. On the Outlook Home Ribbon, select the **Get Add-ins** icon.

    ![Get Add-ins](../../Images/mya/use/get-add-ins.png)

2. Select **My add-ins**.
3. In **Admin-managed**, select the **ellipsis** (**...**) for **Insights**, and then select **Remove**.

    ![Remove Insights](../../Images/mya/use/remove-insights.png)

##### Add the Insights Outlook add-in

Follow these steps to add the Insights add-in to your Outlook ribbon.

1. On the Outlook Home Ribbon, select the **Get Add-ins** icon.
2. Select **Admin-managed**.
3. Find **Insights**, and then select **Add**.

### Visibility and access 

#### Q2. Why can't I see the MyAnalytics dashboard?

The MyAnalytics dashboard is only available if your organization has a *qualifying plan*. Qualifying plans are listed in the table under [Availability of features](../../myanalytics/overview/plans-environments.md#availability-of-features). If an organization has no *qualifying plan*, its members can't see any of the MyAnalytics elements, including the dashboard, and MyAnalytics does not use their data. 

#### Q3. Even though I don’t have a MyAnalytics license, why can I open [MyAnalytics](https://myanalytics.microsoft.com) and turn MyAnalytics on?

Even if you don’t have a MyAnalytics license, your data contributes to the email read statistics for other users. For example, when you receive a qualifying email and read it, MyAnalytics includes that stat in the read percentage that's shown to the sender. You can change this in Settings on your MyAnalytics dashboard.

#### Q4. How can I find out what my plan is?

Some MyAnalytics feature descriptions start with _**Applies to:**_ sections that refer to Office 365 or Microsoft 365 "plans," and then point to the [Plans and environments](plans-environments.md) article. What plan do I have? 

You can identify your _plan_ (and also your _service plan_) by following these steps:

1. Open your [MyAnalytics dashboard](https://myanalytics.microsoft.com).
 
2.	In the upper-right corner, under **My account**, select **My account**: 

    ![My account](../../images/mya/overview/my-account-2.png)
 
3.	On the **My account** page, under **Subscriptions**, select **View subscriptions**:

    ![View subscriptions](../../images/mya/overview/subscriptions_85.png)
 
4.	On the **Subscriptions** page, find your plan and your service plan listed under **Licenses**:

    _In the following example, the plan is "Office 365 E1" and the MyAnalytics-related service plan is "Insights by MyAnalytics":_
   
    ![service plan: Insights by MyAnalytics](../../images/mya/overview/licenses-plans-service-plans.png)

    _In the following example, the plan is "Office 365 E5" and the MyAnalytics-related service plan is "Microsoft MyAnalytics (Full)":_
    
    ![service plan: Microsoft MyAnalytics (Full)](../../images/mya/overview/e5-plans-service-plans-446.png)

#### Q5. In what languages are the elements of MyAnalytics available?

See [MyAnalytics languages](mya-languages.md).

### Insights Outlook add-in

#### Q1. The Insights Outlook add-in displays task cards (commitments). Are they available in all languages, or just in English?

The [task cards](../use/MyA-Outlook-add-in/MyA-Add-in-To-do.md) of the Outlook add-in are available only in English.

#### Q2. Can I get email read rates for shared or secondary mailboxes?

MyAnalytics does not use data from shared or secondary mailboxes.

#### Q3. Why are read statistics not available for some of my email?

To see read statistics for an email that you sent, you must have sent it within the past 14 days to at least five recipients.

## For IT administrators

#### Q1. How do I manage the MyAnalytics experience for users?

You can manage the experience in two ways:

* Turn on or off specific MyAnalytics elements for your entire organization. For details, see [Configure access at the tenant level](../setup/configure-myanalytics.md#configure-access-at-the-tenant-level).
* Turn MyAnalytics access on or off for individual users. For details, see [Configure access at the user level](../setup/configure-myanalytics.md#configure-access-at-the-user-level).

#### Q2. Where and for how long is user data stored?

User metrics data is stored in users' mailboxes. Depending on the scenario, daily data is stored for up to 35 days and weekly data is stored for up to nine weeks. However, data about the number of collaborators is stored for up to 370 days.

#### Q3. How long before new users can access the dashboard and other MyAnalytics elements?

The dashboard is available to MyAnalytics users a few days after getting assigned a license with a MyAnalytics service plan. For more details about when new users get access to MyAnalytics, see [Access to MyAnalytics elements](./plans-environments.md#access-to-myanalytics-elements).

#### Q4. When the dashboard is activated, does it show any historical data or does it start from the day of activation?

After activation, MyAnalytics processes historical data for four weeks before the date of activation. No data before this four-week date range is shown in the dashboard. For calculating active collaborators, MyAnalytics processes historical data for the previous 12 months.

#### Q5. Will MyAnalytics work for shared mailboxes?

No, currently the MyAnalytics service plan cannot be used with shared mailboxes.

#### Q6. Can data be extracted from on-premises installations of Microsoft Exchange or Skype for Business?

No. Only Exchange Online, Skype for Business Online, and Teams are used as sources of MyAnalytics data.

#### Q7. I have not received my Skype for Business data. It seems to have gone missing. Where is it?

Skype for Business data is usually prompt. However, in rare instances, users can experience delays of from two to four days. User actions completed on a Friday might not be included in MyAnalytics computations that are executed the following Monday. In such cases, non-working time, which includes Teams data, is updated later. Similarly, certain meetings might be marked as "Late start" after a day or two, or a digest email sent on a Monday or Tuesday, might not immediately include the data. In all such cases, the metrics are updated as soon as the data is updated.

#### Q8. Which MyAnalytics features are _not_ available to users who have the "Insights by MyAnalytics" service plan?

The cards that show [Email read statistics](../use/add-in.md#email-read-statistics) are not currently available with the *Insights by MyAnalytics* service plan.

   > [!Note]
   > All MyAnalytics features are available to users who have the *MyAnalytics (Full)* service plan.

#### Q9. Why can't licensed users see one or more of the MyAnalytics elements?

* Check [Access to MyAnalytics elements](./plans-environments.md#access-to-myanalytics-elements) to see when MyAnalytics elements become available after users are assigned a license with a MyAnalytics service plan.
* Check if **EWSAllowList** is configured to allow "myanalytics" for users; see [Set-OrganizationConfig](https://docs.microsoft.com/powershell/module/exchange/organization/set-organizationconfig) for more details:

   ```Set-OrganizationConfig -EwsAllowList  @{Add="myanalytics/*"}```

#### Q10. How can I pilot MyAnalytics to a subset of users?

Turn on the “Insights by MyAnalytics” OR “MyAnalytics (Full)” service plan for the pilot users. Because these plans are enabled by default, you'll need to confirm that the plans are turned off for other users. For details on how to turn off the plans, see [Assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users).

#### Q11. How can I confirm that the Insights Outlook add-in is installed?

See [Confirm installation of the Insights Outlook add-in](../setup/verify-add-in.md) to confirm it's installed.

#### Q12. Can I ask that MyAnalytics user data be deleted and not stored?

Yes, you can delete and restrict the processing of MyAnalytics user data if required by law or when requested by a user, which supports GDPR data subject rights. For delete data instructions, see [the third obligation of GDPR Compliance](privacy-guide.md#gdpr-compliance).

   > [!Note]
   > If a person opts out of using MyAnalytics, it doesn't delete that person's MyAnalytics data.

#### Q13. Can Microsoft personnel access a person's MyAnalytics data?

The same rules apply as with Microsoft Office 365 commercial online services, Microsoft personnel do not have access to customer data in MyAnalytics. To learn more, see [Who can access your data](https://www.microsoft.com/trust-center/privacy/data-access).

#### Q14. Does the system enable administrators the ability to log or audit data activity, such as accessing, modifying, or deleting data?

No. MyAnalytics does not support auditing.

#### Q15. What browsers can I use with MyAnalytics and the Insights Outlook Add-in?

See [Browser support in Plans and environments](plans-environments.md#browser-support) for a list of web browsers that the MyAnalytics dashboard supports.

As an Outlook Add-in, the Insights Outlook Add-in requires a browser compatible with your system's platform and operating system. For details, see [Browsers used by Office Add-ins](https://docs.microsoft.com/office/dev/add-ins/concepts/browsers-used-by-office-web-add-ins).

#### Q16. How can I manage MyAnalytics experiences in Office 365 GCC?

You can enable or disable MyAnalytics experiences by following the applicable steps in [Assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users). More granular controls for each user surface will be available by the end of 2019.
