---
title: Review Viva Glint settings and survey programs before launch
description: To prepare for a smooth survey launch for your Microsoft Viva Glint programs, use the guidance and checklists available here to confirm that all of your platform and survey settings are correct.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: QA, quality assurance, quality check, QC, UAT, user acceptance testing
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 05/02/2024
---

# Review Viva Glint settings and survey programs before launch

To prepare for a smooth launch for your Microsoft Viva Glint survey programs, use the guidance and checklists available here to confirm that all of your platform and survey settings are correct.

## Confirm selections in General Settings

Selections that admins make in [General Settings](manage-general-settings.md) lay the groundwork for users' survey-taking and reporting experiences. Verify that your choices for important fields here appear as expected.

> [!NOTE]
> Not all General Settings fields are included here, but settings that have the biggest impact to survey takers are included.

### Company Information

- **Client Name:** The organization name here appears in surveys and email invites and reminders.
- **Client Time Zone:** This is the default time zone that Glint uses to send communications.
- **Company Privacy Policy:** Optionally, include a link to your company policy. [Learn more](add-privacy-policy.md)
- **Company Message to Survey Participants:** To include the same message for all surveys, add a message here. To customize for each survey, add in Program Setup.

### Communications

- **Send Surveys in Users' Time Zones:** Switch to Yes or No to enable or disable [sending communications in user's time zones](time-zones.md). 

### Reporting

- **Attributes for Alerts:** Select attributes to use to generation of the [Alerts Report](/viva/glint/reports/alerts-report-attrition-risk). When blank, all attributes are included.
- **Primary Hierarchy:** Select the primary hierarchy for default reporting views and sections (usually Manager Hierarchy).
- **Secondary Hierarchy:** Select the secondary hierarchy for default reporting views and sections.

### Engage Survey Details

- **Require Azure AD for links in survey emails:** Switch to Yes to require survey participants to authenticate with Entra ID to access surveys. [Learn more](understand-survey-access-methods.md).
- **Attribute-based Survey Access:** Set up an alternate survey access method for deskless workers. [Learn more](attribute-based-survey-access.md)

### Features

- **Employee Post-Survey Action Taking:** Set to Yes or No to determine if survey participants see recommended LinkedIn Learning videos on their survey Thank you page. This applies to all surveys.

### Technical Configuration

- **SFTP Setup:** Confirm that Secure File Transfer Protocol (SFTP) setup is complete if your organization imports employee data with this method. [Learn more](set-up-sftp.md).
 
### Localization

- **Comments Analytics Languages:** Select languages that should be translated to English for comment analysis.
    > [!NOTE]
    > Languages must be selected before a survey launches to successfully analyze non-English comments.
- **Default Survey Language:** Choose the default language for survey participants.
- **Supported Survey Languages:** Choose additional languages for survey participants to select.
- **Default Dashboard Language:** Choose the default language for dashboard users.
- **Supported Dashboard Languages:** Choose additional languages for dashboard users to select.

## Review survey programs


# [Recurring](#tab/recurring)

<details>

<summary>Program Setup</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Program Name    |The correct value is entered and there are no spelling errors.       |Low        |Yes        |
|Administrators|The correct User Roles are selected as program admins.   |Low|Yes|
|Default Language|The correct default language is selected.  |Medium|Yes|
|Additional Languages|Correct additional survey languages are selected. Languages available are based on Supported Survey Languages selected in General Settings  |Medium|Yes*|
|Admin Notifications To|The correct user is selected for admin notification emails for this program.    |Medium|Yes|
|Suggested Actions Available|This setting is set to Yes or No correctly to allow or disallow users to create Focus Areas based on suggestion action templates.  |High|Yes|
|Eligible for Nudges|This setting is set to Yes or No correctly to enable or disable Nudges for managers to act on survey results.   |High|Yes|
|Allow Survey Resubmission|This setting is set to Yes or No correctly to allow or disallow users to reset their own surveys and resubmit during live surveys.   |High|Yes|
|Enable Team Conversations|This setting is set to Yes or No correctly to enable or disable Team Conversations for managers to act on results with a guided, in-platform experience.  |High|Yes|
|Confidential Responses|This setting is set to Yes or No correctly. This setting can only be switched to No for Employee Lifecycle surveys.  |High|No|
|Enable Export of Raw Survey Responses|This setting is set to Yes or No correctly to allow or disallow the export of raw respondent data for this program.   |High|No|
|Company Message to Survey Participants|Any optional custom messaging to survey participants and accompanying translations are entered correctly.  |High|Yes|

> [!TIP]
> *Viva Glint standard translations become available immediately for newly added languages. Custom question translations can't be added during a live survey.

</details>

<details>

<summary>Distribution</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Distribution For This Program    |The correct Distribution Lists are selected to include users.       |High        |No*        |
|Exclude Groups|The correct Distribution lists are selected to exclude users.   |High|No|

> [!TIP]
> *Use the Send Survey option from a user’s profile to add individual users to live surveys

</details>

<details>

<summary>Schedule</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|The surveys go out every    |The survey frequency is correct (for example, every 4 months).       |Low        |Yes        |
|Send the next survey on|The survey start date is accurate.   |High|Yes|
|Schedule Preview|Upcoming survey dates are accurate based on frequency and survey start date.   |Low|Yes|
|Response Window|The number of days the survey is open for responses is correct.   |High|Yes*|

> [!TIP]
> *Use the ellipses menu on the live survey cycle and choose Manage Schedule & Invites to make changes during a live survey.

</details>


<details>

<summary>Questions</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Welcome text and translations    |Welcome text and translations are accurate.       |High        |Yes        |
|Questions|All questions are part of the survey and that the upcoming cycle number is selected for the right questions.   |High|No|
|Questions: Order|Questions are in the correct order.   |High|Yes|
|Questions: Text and translations|Customized question text and translations are accurate.   |High|No|
|Questions: Targeting|Distribution lists selected to target questions are accurate.   |High|No|
|Questions: Display Logic|Questions that should only appear based on certain responses to other questions are set up correctly.   |High|No|
|Sections and translations|Section break/header text and translations are correct.   |Medium|No|
|Thank you text and translations|Thank you text and translations are accurate.    |High|Yes|

> [!TIP]
> - Section break: User scrolls and it disappears as you take the survey. 
> - Survey section: A persistent header with questions tied to it that remains at the top of the screen as the user responds.

</details>

<details>

<summary>Reporting</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Program Roles    |Roles who should be added to the program are present and that they're granted live or phased access correctly.      |High        |Yes        |
|Reporting View |Live View or Phased Access is selected appropriately, depending on whether the role should have access to live survey data.   |Medium|Yes|
|Concierge Visibility |This setting is set to On or Off correctly to give managers a concierge experience in dashboards.   |Medium|Yes|
|Broader Team Insights |This setting is set to On or Off to allow direct reports visibility to a summary report of users' scores in this role.   |Medium|Yes|
|Team Conversations |This setting is set to On or Off correctly to allow managers to use in-platform Team Conversations.   |Medium|Yes|
|Dashboard Default |The correct report, typically Team Summary, is selected for the dashboard view.   |Medium|Yes|
|Report Template Access |Report templates are selected correctly to grant users access to specific reports.  |High|Yes|
|Question Reporting Access |Users in the role have access to the correct questions.   |Medium|Yes|
|Aggregate Indices|Question aggregates are set up and labeled correctly.   |Medium|Yes|
|Key Outcome|The correct item or aggregate is selected.   |Medium|Yes|
|Driver Impact Outcomes|The correct items or aggregates are selected.  |Medium|Yes|
|Manager Report Defaults|The correct items are selected to appear on the Manager report.   |Medium|Yes|
|PowerPoint Export Template|The correct template is selected.   |Low|Yes|
|Broader Team Insights PowerPoint Export Template|The correct template is selected.   |Low|Yes|

> [!NOTE]
> - The Team Conversations setting only appears in a Program Role when Team Conversations have been enabled in Program Setup.
> - Aggregate Indices can't be deleted after they're setup.

</details>


<details>

<summary>Communications</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Notification Timing    |The correct timeframe is selected to deliver emails.       |High        |Yes        |
|Email Settings*|The correct email types are selected to deliver emails.   |Medium|Yes|
|Configure Notifications|Survey start, reminder, and results emails follow the correct schedule.   |High|Yes**|
|Translations|Survey start, reminder, and results emails have accurate translations.   |High|Yes**|

> [!NOTE]
> - *This setting only appears when your organization has a Personal Email Optional System Attribute set up. Personal emails are recommended for contacting exiting employees.
> - **Reminder emails can be added/edited at the survey cycle level if the added reminders aren't scheduled to send for at least 24 hours. New reminders can't be added to sent the same day.

</details>


<details>

<summary>Coaching</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Interpretation    |The correct content is selected for the Interpretation Guide.       |Medium        |Yes        |
|Top Strengths|The correct content is selected for Top Strengths.    |Medium        |Yes        |
|Top Opportunities|The correct content is selected for Top Opportunities   |Medium        |Yes        |

> [!TIP]
> Save and continue without edits to keep default selections for Coaching content.

</details>





# [Lifecycle](#tab/lifecycle)

<details>

<summary>Program Setup</summary>

|Item   |Confirm that...  |Impact|Editable during live survey
|:----------|:-----------|:------------|:------------|
|Program Name    |The correct value is entered and there are no spelling errors.       |Low        |Yes        |
|Administrators|The correct User Roles are selected as program admins.   |Low|Yes|
|Default Language|The correct default language is selected.  |Medium|Yes|
|Additional Languages|Correct additional survey languages are selected. Languages available are based on Supported Survey Languages selected in General Settings  |Medium|Yes*|
|Suggested Actions Available|This setting is set to Yes or No correctly to allow or disallow users to create Focus Areas based on suggestion action templates.  |High|Yes|
|Response Window|The correct number of days is selected.   |High|Yes**|
|Waiting Period Between Surveys|The correct number of days is selected.   |High|Yes**|
|Allow Survey Resubmission|This setting is set to Yes or No correctly to allow or disallow users to reset their own surveys and resubmit during live surveys.   |High|Yes|
|Confidential Responses|This setting is set to Yes or No correctly. This setting can only be switched to No for Employee Lifecycle surveys.  |High|No|
|Enable Export of Raw Survey Responses|This setting is set to Yes or No correctly to allow or disallow the export of raw respondent data for this program.   |High|No|
|Company Message to Survey Participants|Any optional custom messaging to survey participants and accompanying translations are entered correctly.  |High|Yes|

> [!TIP]
> *Viva Glint standard translations become available immediately for newly added languages. Custom question translations can't be added during a live survey.

> [!NOTE]
> **Updating the Response Window and Waiting Period Between Surveys affects future surveys only.

</details>

<details>

<summary>Distribution</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Employee Attribute    |The correct date (hire or exit) is selected as a trigger date for surveys.       |High        |No        |
|Distribution For This Program    |The correct Distribution Lists are selected to include users.       |High        |No*        |
|Exclude Groups|The correct Distribution lists are selected to exclude users.   |High|No|

> [!TIP]
> *Use the Send Survey option from a user’s profile to add individual users to live surveys.

</details>



<details>

<summary>Questions</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Welcome text and translations    |Welcome text and translations are accurate.       |High        |Yes        |
|Questions|All questions are part of the survey and that the upcoming cycle number is selected for the right questions.   |High|No|
|Questions: Order|Questions are in the correct order.   |High|Yes|
|Questions: Text and translations|Customized question text and translations are accurate.   |High|No|
|Questions: Targeting|Distribution lists selected to target questions are accurate.   |High|No|
|Questions: Display Logic|Questions that should only appear based on certain responses to other questions are set up correctly.   |High|No|
|Sections and translations|Section break/header text and translations are correct.   |Medium|No|
|Thank you text and translations|Thank you text and translations are accurate.    |High|Yes|

> [!TIP]
> - Section break: User scrolls and it disappears as you take the survey. 
> - Survey section: A persistent header with questions tied to it that remains at the top of the screen as the user responds.

</details>



<details>

<summary>Reporting</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Program Roles    |Roles who should be added to the program are present and that they're granted live or phased access correctly.      |High        |Yes        |
|Dashboard Default |The correct report, typically Team Summary, is selected for the dashboard view.   |Medium|Yes|
|Report Template Access |Report templates are selected correctly to grant users access to specific reports.  |High|Yes|
|Question Reporting Access |Users in the role have access to the correct questions.   |Medium|Yes|
|Aggregate Indices|Question aggregates are set up and labeled correctly.   |Medium|Yes|
|Key Outcome|The correct item or aggregate is selected.   |Medium|Yes|
|Driver Impact Outcomes|The correct items or aggregates are selected.  |Medium|Yes|
|Manager Report Defaults|The correct items are selected to appear on the Manager report.   |Medium|Yes|
|PowerPoint Export Template|The correct template is selected.   |Low|Yes|
|Broader Team Insights PowerPoint Export Template|The correct template is selected.   |Low|Yes|

> [!NOTE]
> Aggregate Indices can't be deleted after they're setup.

</details>

<details>

<summary>Communications</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Notification Timing    |The correct timeframe is selected to deliver emails.       |High        |Yes        |
|Email Settings*|The correct email types are selected to deliver emails.   |Medium|Yes|
|Configure Notifications|Survey start, reminder, and results emails follow the correct schedule.   |High|Yes**|
|Translations|Survey start, reminder, and results emails have accurate translations.   |High|Yes**|

> [!NOTE]
> - *This setting only appears when your organization has a Personal Email Optional System Attribute set up. Personal emails are recommended for contacting exiting employees.
> - **Reminder emails can be added/edited at the survey cycle level if the added reminders aren't scheduled to send for at least 24 hours. New reminders can't be added to sent the same day.
</details>


<details>

<summary>Coaching</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Interpretation    |The correct content is selected for the Interpretation Guide.       |Medium        |Yes        |
|Top Strengths|The correct content is selected for Top Strengths.    |Medium        |Yes        |
|Top Opportunities|The correct content is selected for Top Opportunities   |Medium        |Yes        |

> [!TIP]
> Save and continue without edits to keep default selections for Coaching content.

</details>



# [Ad-Hoc](#tab/adhoc)

<details>

<summary>Program Setup</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Program Name    |The correct value is entered and there are no spelling errors.       |Low        |Yes        |
|Administrators|The correct User Roles are selected as program admins.   |Low|Yes|
|Default Language|The correct default language is selected.  |Medium|Yes|
|Additional Languages|Correct additional survey languages are selected. Languages available are based on Supported Survey Languages selected in General Settings  |Medium|Yes*|
|Admin Notifications To|The correct user is selected for admin notification emails for this program.    |Medium|Yes|
|Suggested Actions Available|This setting is set to Yes or No correctly to allow or disallow users to create Focus Areas based on suggestion action templates.  |High|Yes|
|Eligible for Nudges|This setting is set to Yes or No correctly to enable or disable Nudges for managers to act on survey results.   |High|Yes|
|Allow Survey Resubmission|This setting is set to Yes or No correctly to allow or disallow users to reset their own surveys and resubmit during live surveys.   |High|Yes|
|Confidential Responses|This setting is set to Yes or No correctly. This setting can only be switched to No for Employee Lifecycle surveys.  |High|No|
|Enable Export of Raw Survey Responses|This setting is set to Yes or No correctly to allow or disallow the export of raw respondent data for this program.   |High|No|
|Company Message to Survey Participants|Any optional custom messaging to survey participants and accompanying translations are entered correctly.  |High|Yes|

> [!TIP]
> *Viva Glint standard translations become available immediately for newly added languages. Custom question translations can't be added during a live survey.

</details>


<details>

<summary>Distribution</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Distribution For This Program    |The correct Distribution Lists are selected to include users.       |High        |No*        |
|Exclude Groups|The correct Distribution lists are selected to exclude users.   |High|No|

> [!TIP]
> *Use the Send Survey option from a user’s profile to add individual users to live surveys

</details>


<details>

<summary>Schedule</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Send the next survey on|The survey start date is accurate.   |High|Yes|
|Response Window|The number of days the survey is open for responses is correct.   |High|Yes*|

> [!TIP]
> *Use the ellipses menu on the live survey cycle and choose Manage Schedule & Invites to make changes during a live survey.

</details>


<details>

<summary>Questions</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Welcome text and translations    |Welcome text and translations are accurate.       |High        |Yes        |
|Questions|All questions are part of the survey and that the upcoming cycle number is selected for the right questions.   |High|No|
|Questions: Order|Questions are in the correct order.   |High|Yes|
|Questions: Text and translations|Customized question text and translations are accurate.   |High|No|
|Questions: Targeting|Distribution lists selected to target questions are accurate.   |High|No|
|Questions: Display Logic|Questions that should only appear based on certain responses to other questions are set up correctly.   |High|No|
|Sections and translations|Section break/header text and translations are correct.   |Medium|No|
|Thank you text and translations|Thank you text and translations are accurate.    |High|Yes|

> [!TIP]
> - Section break: User scrolls and it disappears as you take the survey. 
> - Survey section: A persistent header with questions tied to it that remains at the top of the screen as the user responds.

</details>


<details>

<summary>Reporting</summary>


|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Program Roles    |Roles who should be added to the program are present and that they're granted live or phased access correctly.      |High        |Yes        |
|Reporting View |Live View or Phased Access is selected appropriately, depending on whether the role should have access to live survey data.   |Medium|Yes|
|Concierge Visibility |This setting is set to On or Off correctly to give managers a concierge experience in dashboards.   |Medium|Yes|
|Broader Team Insights |This setting is set to On or Off to allow direct reports visibility to a summary report of users' scores in this role.   |Medium|Yes|
|Dashboard Default |The correct report, typically Team Summary, is selected for the dashboard view.   |Medium|Yes|
|Report Template Access |Report templates are selected correctly to grant users access to specific reports.  |High|Yes|
|Question Reporting Access |Users in the role have access to the correct questions.   |Medium|Yes|
|Aggregate Indices|Question aggregates are set up and labeled correctly.   |Medium|Yes|
|Key Outcome|The correct item or aggregate is selected.   |Medium|Yes|
|Driver Impact Outcomes|The correct items or aggregates are selected.  |Medium|Yes|
|Manager Report Defaults|The correct items are selected to appear on the Manager report.   |Medium|Yes|
|PowerPoint Export Template|The correct template is selected.   |Low|Yes|
|Broader Team Insights PowerPoint Export Template|The correct template is selected.   |Low|Yes|

> [!NOTE]
> Aggregate Indices can't be deleted after they're setup.



</details>


<details>

<summary>Communications</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Notification Timing    |The correct timeframe is selected to deliver emails.       |High        |Yes        |
|Email Settings*|The correct email types are selected to deliver emails.   |Medium|Yes|
|Configure Notifications|Survey start, reminder, and results emails follow the correct schedule.   |High|Yes**|
|Translations|Survey start, reminder, and results emails have accurate translations.   |High|Yes**|

> [!NOTE]
> - *This setting only appears when your organization has a Personal Email Optional System Attribute set up. Personal emails are recommended for contacting exiting employees.
> - **Reminder emails can be added/edited at the survey cycle level if the added reminders aren't scheduled to send for at least 24 hours. New reminders can't be added to sent the same day.

</details>



<details>

<summary>Coaching</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Interpretation    |The correct content is selected for the Interpretation Guide.       |Medium        |Yes        |
|Top Strengths|The correct content is selected for Top Strengths.    |Medium        |Yes        |
|Top Opportunities|The correct content is selected for Top Opportunities   |Medium        |Yes        |

> [!TIP]
> Save and continue without edits to keep default selections for Coaching content.

</details>




# [Always-On](#tab/alwayson)

<details>

<summary>Program Setup</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Program Name    |The correct value is entered and there are no spelling errors.       |Low        |Yes        |
|Administrators|The correct User Roles are selected as program admins.   |Low|Yes|
|Default Language|The correct default language is selected.  |Medium|Yes|
|Additional Languages|Correct additional survey languages are selected. Languages available are based on Supported Survey Languages selected in General Settings  |Medium|Yes*|
|Suggested Actions Available|This setting is set to Yes or No correctly to allow or disallow users to create Focus Areas based on suggestion action templates.  |High|Yes|
|Response Window|The correct number of days is selected.   |High|Yes**|
|Next Survey Available|The correct number of days is selected.   |High|Yes**|
|Confidential Responses|This setting is set to Yes or No correctly. This setting can only be switched to No for Employee Lifecycle surveys.  |High|No|
|Enable Export of Raw Survey Responses|This setting is set to Yes or No correctly to allow or disallow the export of raw respondent data for this program.   |High|No|
|Company Message to Survey Participants|Any optional custom messaging to survey participants and accompanying translations are entered correctly.  |High|Yes|

> [!TIP]
> *Viva Glint standard translations become available immediately for newly added languages. Custom question translations can't be added during a live survey.

> [!NOTE]
> **Updating the Response Window and Waiting Period Between Surveys affects future surveys only.

</details>



<details>

<summary>Distribution</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Distribution For This Program    |The correct Distribution Lists are selected to include users.       |High        |No        |
|Exclude Groups|The correct Distribution lists are selected to exclude users.   |High|No|


</details>




<details>

<summary>Questions</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Welcome text and translations    |Welcome text and translations are accurate.       |High        |Yes        |
|Questions|All questions are part of the survey and that the upcoming cycle number is selected for the right questions.   |High|No|
|Questions: Order|Questions are in the correct order.   |High|Yes|
|Questions: Text and translations|Customized question text and translations are accurate.   |High|No|
|Questions: Targeting|Distribution lists selected to target questions are accurate.   |High|No|
|Questions: Display Logic|Questions that should only appear based on certain responses to other questions are set up correctly.   |High|No|
|Sections and translations|Section break/header text and translations are correct.   |Medium|No|
|Thank you text and translations|Thank you text and translations are accurate.    |High|Yes|

> [!TIP]
> - Section break: User scrolls and it disappears as you take the survey. 
> - Survey section: A persistent header with questions tied to it that remains at the top of the screen as the user responds.

</details>


<details>

<summary>Reporting</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Program Roles    |Roles who should be added to the program are present and that they're granted live or phased access correctly.      |High        |Yes        |
|Dashboard Default |The correct report, typically Team Summary, is selected for the dashboard view.   |Medium|Yes|
|Report Template Access |Report templates are selected correctly to grant users access to specific reports.  |High|Yes|
|Question Reporting Access |Users in the role have access to the correct questions.   |Medium|Yes|
|Aggregate Indices|Question aggregates are set up and labeled correctly.   |Medium|Yes|
|Key Outcome|The correct item or aggregate is selected.   |Medium|Yes|
|Driver Impact Outcomes|The correct items or aggregates are selected.  |Medium|Yes|
|Manager Report Defaults|The correct items are selected to appear on the Manager report.   |Medium|Yes|
|PowerPoint Export Template|The correct template is selected.   |Low|Yes|
|Broader Team Insights PowerPoint Export Template|The correct template is selected.   |Low|Yes|

> [!NOTE]
> Aggregate Indices can't be deleted after they're setup.

</details>



<details>

<summary>Coaching</summary>

|Item   |Confirm that...  |Impact|Editable during live survey|
|:----------|:-----------|:------------|:------------|
|Interpretation    |The correct content is selected for the Interpretation Guide.       |Medium        |Yes        |
|Top Strengths|The correct content is selected for Top Strengths.    |Medium        |Yes        |
|Top Opportunities|The correct content is selected for Top Opportunities   |Medium        |Yes        |

> [!TIP]
> Save and continue without edits to keep default selections for Coaching content.

</details>

---

## Preview data in reporting

After reviewing your survey setup and confirming that employee data is imported to Glint, use the [Generate Report Preview](preview-demo-reporting.md) option to preview how attributes and questions look in reports.

> [!IMPORTANT]
> The Generate Report Preview option is only available for Recurring and Ad-Hoc survey types.

## Launch a test survey

Launch a test survey to your project team to confirm that emails arrive and the survey-taking experience appears as expected. To set up a test survey:

> [!IMPORTANT]
> Always create a copy of your survey program to launch a test survey. Test survey programs can be deleted, but test cycles in a survey program can't be deleted.

1. From the admin dashboard, select **Configuration** and then choose **Survey Programs**.
1. On the far right of your completed survey program, select the ellipses and choose **Duplicate** from the menu that appears.
1. A new survey program appears titled **"survey name" Copy**.
1. Select the copied survey and go to **Distribution**.
   1. Select a Distribution List that includes test users in the **Distribution For This Program** field.
1. Select **Save & Continue** to go to **Schedule**.
   1. Select a date to launch your test survey in the **Send the next survey on** field.
   1. Select a number of days for the test survey to be open in the **Response Window** field.
1. Go to the **Communications** section to confirm timing and invites/reminders are selected for your test survey's **Response Window**.
1. [Approve and Enable](preview-manage-enable-engage-programs.md) your test survey.

Each test user can confirm that:  

- They receive email invites and reminders as expected. [Learn more about Glint's allowed list](allowed-list.md).
- Selected survey access methods work as expected. [Learn more](understand-survey-access-methods.md).
- The survey experience appears as expected, including: 
  - Survey intro and translations
  - Survey question order and translations
  - Survey sections and translations
  - Question [Display Logic](viva-glint-display-logic.md)
  - Question [Targeting](targeted-survey-items.md)
  - Survey thank you text and translations
  - Allow survey resubmission experience
  - Post-survey video experience

### Delete a test survey

When survey testing is complete, [delete your test survey](delete-survey-data.md) from **Survey Programs**.

## Approve and enable a survey for launch

After all testing and review is complete, [Approve and Enable](preview-manage-enable-engage-programs.md) your survey for launch.
