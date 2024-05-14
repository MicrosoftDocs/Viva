---
title: Manage General Settings in Viva Glint 
description: Global details supporting all of your programs are defined and managed in this feature.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: focus area privacy, confidentiality setup, communications setup, localization
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 05/14/2024
---

# Manage General Settings in Viva Glint 

Details defining your Microsoft Viva Glint programs are set up and viewed by selecting the **Configuration** symbol on your Viva Glint admin dashboard and then **General Settings** in the *Service Configuration* section. 

:::image type="content" source="../../media/glint/setup/general-settings-access.png" alt-text="Screenshot of how to access General Settings from the admin dashboard.":::

Use the definitions and prompts on the platform so you feel confident about the choices you make. 

>[!IMPORTANT]
> Any initial actions or subsequent changes in General Settings apply to all survey programs created in Viva Glint.

These sections require setup: 

## Company Information 

This section provides high-level information about your company. 
Also, set up what your employees see when they open an email sharing information about a Glint program.  

| Field | Definition and notes |
|-----------|-----------|
|**Client UUID**   | How Viva Glint identifies your company in our system.  |  
|**Client Name**    | *Or Doing Business As (DBA) name*.   | 
|**Client Time Zone**    | Survey and reminder emails are sent out in this time zone unless **Send surveys in users’ time zones** is checked. [More information on customer time zones.](https://go.microsoft.com/fwlink/?linkid=2255796)   | 
|**Top-Level Manager (Chief Executive Officer- CEO)**    | This employee is used to build managerial hierarchy and is the only person in your organization that doesn't report to anyone at a higher level.| 
|**Company Privacy Policy** | To replace the Microsoft Privacy Statement, add a link to your organization’s privacy policy. The privacy policy is displayed at the beginning of Glint surveys and in the Glint navigation bar.|
|**Company Message to Survey Participants**|Enter guidance specific to your organization to be displayed at the beginning of Glint surveys and applied to new programs and scheduled surveys. Character limit: 1024|

> [!IMPORTANT]
> Avoid potential conflicts between your organization's message and Viva Glint's privacy statements. The application of one of the three privacy statements to the survey is dependent upon its configuration. [**Learn more**](/../../viva/glint/setup/viva-glint-survey-privacy). The company message displayed alongside standard privacy statements should refrain from stating anything that conflicts with the privacy statement applied to the survey.  Microsoft reserves the right to delete company messages if such conflicts comes to our attention.

>[!TIP]
>Best practice is to either link to your organization's privacy policy or to customize a message. Using both your company's privacy policy and a customized message may incur conflicts.

:::image type="content" source="../../media/glint/setup/customized-privacy-policy.png" alt-text="Screenshot of the **Hello** message that employees see when a customized message around privacy is included.":::

:::image type="content" source="../../media/glint/setup/customized-and-org-privacy-policy.png" alt-text="Screenshot of the **Hello** message that employees see when only your company's privacy policy is included.":::

## Communications

| Field | Definition and notes |
|-----------|-----------|
|**Enable Email Notifications for Focus Area Comments**    | Enable for comments and user tagging.  | 
|**Hide Focus Area/Comment Text in Focus Area Emails**    | Managers may receive an email notification when someone comments on their Focus Area (goal) or a new one is cascaded to them. Enable to hide these details from these emails. Disable to allow goal title and comment text to display.    | 
|**Send Survey in Users’ Time Zones**    | Send invitations in user’s time zones on the survey start date. | 

## Reporting  

Choose attributes and hierarchies to show in reporting and select benchmark comparisons. Also indicate permissions and thresholds for viewing feedback. 

>[!NOTE]
> This section is not applicable to 360 Feedback programs. 

| Field | Definition and notes |
|-----------|-----------|
|**Attributes for Alerts**   | Narrow down alerts, if desired. If left empty, all attributes are incorporated (other than nonreportable fields and emails).   |
|**Default Benchmark**   | Your preferred default comparison statistic. If left empty, it defaults to Benchmark.|
|**Internal Benchmarks**   | Viva Glint’s three internal default benchmarks that cannot be removed. Up to ten more may be added. Choosing **Modify internal benchmarks** opens a new window with options.     |
|**External Benchmarks**|Choose the external benchmarks that you want users to be able to select from on their dashboards and in their reporting. Choosing **Modify external benchmarks** opens a new window with options.|
|**Comments Privacy: Minimum # of Responders for Search Results**   | Minimum number of responses to a survey before comments are viewable and searchable. | 
|**Comments Privacy: Minimum # of Responders for Facet/Grouping**   | Minimum number of responses to a survey before comments are available for specific groupings.  | 
|**Confidentiality Threshold**   | Numerical scores can't be displayed for respondent groups smaller than this number of respondents. The default number is five (5).  |   
|**Exclude Negative Strengths and Positive Weaknesses**   | Remove items that how negative scoring as strengths and positive scoring as weaknesses.   |   
|**Insight Minimum Group Size**   | Minimum number of responses before insights and alerts can be shown.    |  
|**Insight Minimum Score Difference**   | Minimum number of responses before showing differences in insights and alerts.     | 
|**Minimum Sample Survey Stats**   | Response rate aren't displayed for groups smaller than this set number. This rate is based on group size, not on number of responses and it must match the confidentiality threshold.      | 
|**PowerPoint Template**   | Customer chosen default template. If unset, it defaults to the Glint template.       | 
|**Broader Team Insights PowerPoint Template**   | Customer chosen default Broader Team Insights template. If unset, it defaults to the Glint template.        |  
|**Primary Hierarchy**   | The hierarchy your company identified as the first level for reporting, typically Manager. |  
|**Secondary Hierarchy**   | The hierarchy your company identified as its second level for reporting, typically Location. | 
|**Rating Questions Scale**   | The defaults survey rating questions use. Viva Glint’s best practice is to use a 5-point scale. | 
|**Suppression Threshold**   | Suppression occurs if there aren't enough respondents to meet confidentiality requirements. The Glint Suppression Threshold default is two (2) but is dependent upon the confidentiality threshold.  |  
|**Cross-Program Filtering**   | Turns on cross-program filtering within reports. Enables user roles to compare employee groups across different survey programs and cycles/   |   

## Engage Survey Details 

Choose your survey access method. [Learn more](https://go.microsoft.com/fwlink/?linkid=2238341).

| Field | Definition and notes |
|-----------|-----------|
|**Require Azure ID for links in survey emails**   | Turn this functionality on to authenticate participants for future surveys with Azure Active Directory (recommended). If you turn off this functionality, a personalized survey link is sent to participants.   | 
|**Attribute-based Survey Access**   | Participants are able to retrieve survey links by entering attributes. This process doesn't authenticate participants and is less secure than surveys requiring Azure AD authentication.   |  

## Features 

In this section:  
- Enable or disable program templates and Focus Area visibility and privacy settings. 
- Set limits for the number of survey cycles that show on a dashboard.  

| Field | Definition and notes |
|-----------|-----------|
|**Available Survey Questions and Program Templates**   |Deselect program types you won’t use to delete them from your platform. You can edit this functionality at any time.    |  
|**Community Enabled**   |Enable to permission access to the Glint community forum for this client, regardless of role-based permissions.  |  
|**Employee Post-Survey Action Taking**   |Enables employees to view free LinkedIn Learning videos upon completing a survey. A LinkedIn Learning license is not required.  |  
|**Team Conversation Enabled**   |Enables Team Conversations for recurring surveys.   |  
|**Default Focus Area Privacy**   |Choose the visibility/privacy setting for users creating a new Focus Area. More instructions around focus area privacy follow this table.  |
|**Maximum Number of Survey Cycles for Trend**   |Default is five (5) cycles. Applies only to recurring and ad-hoc surveys. This controls the number of cycles that show on the dashboard and in reporting.    |
|**Self-Serve Mode**   |When Edit and Create is selected, this choice allows users with the correct user role permissions to edit and create surveys.   | 

## Choose Focus Area privacy settings in Features

The default privacy setting within *Features* is **Public**. 

:::image type="content" source="../../media/glint/setup/general-settings-privacy-feature.png" alt-text="Screenshot of the default setting for Focus Area Privacy in General Settings." lightbox="../../media/glint/setup/general-settings-privacy-feature.png":::

There are other options, in addition to the *Public* default setting:
- Visible to Manager
- Visible to Manager and Directs - The user creating the focus area must have a manager and a direct report - who is also a manager - to use this option.
- Visible to Manager and Full Team

:::image type="content" source="../../media/glint/setup/focus-area-privacy-dropdown.png" alt-text="Screenshot of the dropdown menu for Focus Area Privacy in General Settings." lightbox="../../media/glint/setup/focus-area-privacy-dropdown.png":::

## Technical Configuration 

Make selections for your Viva Glint technical setup:
- Username and password for Single Sign On (SSO) users 
- Employee ID 

| Field | Definition and notes |
|-----------|-----------|
|**Attribute for SSO Authentication** |Configure the unique Employee ID. The email is set as the default employee ID. |
|**SFTP Setup** |Streamline your process by automatically adding your company data into the Glint platform. [Learn more](https://go.microsoft.com/fwlink/?linkid=2238339). |

## Localization 

English is the default language for all programs, but surveys and emails may be sent to employees in their preferred language. Viva Glint has 70+ language translations for standard content that can be set during the initial configuration or added later, until the survey is live.  

| Field | Definition and notes |
|-----------|-----------|
|**Comment Analytics Language**   |The list of codes for languages to include for comment analysis. Empty value signifies English only.    |
|**Default Survey Language**   |Provides the default language for surveys. If a preference isn't populated per employee, this language is shown as a default.     |
|**Supported Survey Languages**   |Lists all languages chosen by the admin to support surveys within your organization. This setting is global but can be tailored on a per-program level.     |
|**Default Dashboard Language**   |Provides the default language for dashboards. If a preference isn't supplied/selected per employee, this language is shown as a default.      |
|**Supported Dashboard Languages**   |These languages are available for your dashboard. Your users can select any available language as their static, preferred view.       |
