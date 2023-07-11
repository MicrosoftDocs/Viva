---
title: Admin management of the General Settings feature in Viva Glint 
description: "Global details supporting all of your programs are defined and managed in this feature."
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: viva strengths and opportunities
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: high pri
ms.date: 04/28/2023
---

# Admin management of the General Settings feature in Viva Glint 

Details defining your Viva Glint programs are set up and viewed by selecting the **configuration** symbol on your Microsoft Viva Glint admin dashboard and then **General Settings** in the *Client Settings* section.  

Once you have designated your General Settings, they're valid for all your Viva Glint programs until you edit them. 

## Standard procedures for General Settings section setup 

For each setting option, you'll see a short description so you can feel confident about the choices you make. There are seven sections which require input: 

- [Company information](#set-up-the-company-information-section) 
- [Communications](#set-up-the-communications-section) 
- [Reporting](#set-up-the-reporting-section) 
- [Engage Survey Details](#set-up-the-engage-survey-details-section) 
- [Features](#set-up-the-features-section) 
- [Technical Configuration](#set-up-the-technical-configuration-section) 
- [Translations](#set-up-the-translations-section) 

>[!NOTE]
> Any changes you make in the General Settings will apply to all survey programs created in Viva Glint.

## Set up the Company Information section 

This section provides high-level information about your company. Provide your:

|**Field**| **Definition and notes**|
|-----------|-----------|
|**Client UUID**   | How Viva Glint identifies your company in our system  |  
|**Client Name**    | *Or Doing Business As (DBA) name*   | 
|**Client Time Zone**    | Survey and reminder emails are sent out in this time zone unless **Send surveys in users’ time zones is checked**.    | 
|**SharePoint Site Name**    | Data files can be dropped here or on the Viva Glint SFTP site.    | 
|**Top-Level Manager**    | This employee is used to build managerial hierarchy and is the only person in your organization that doesn't report to anyone at a higher level.| 
|**Configure.clientSettings.privacyUrl.fieldName**    | | 

## Set up the Communications section 

Set up what your employees see when they open an email sharing information about a Viva Glint program.  

Provide or edit the following: 

|**Field**| **Definition and notes**|
|-----------|-----------|
|**Email Sender Name**   | The default name displayed in emails  |  
|**Enable Email Notifications for Focus Area Comments**    | Enable for comments and user tagging  | 
|**Hide Focus Area/Comment Text in Focus Area Emails**    | Managers may receive an email notification when someone comments on their Focus Area (goal) or a new one is cascaded to them. Enable to hide these details from these emails. Disable to allow goal title and comment text to display.    | 
|**No-Reply Email Address**    | Your company’s specific no-reply email address if any     | 
|**Send Survey in Users’ Time Zones**    | Send invitations in user’s time zones on the survey start date | 

## Set up the Reporting section 

Choose attributes and hierarchies to show in reporting and select benchmark comparisons. You will also indicate permissions and thresholds for viewing feedback. 

>[!NOTE]
> This section is not applicable to 360 Feedback programs. 

Provide or edit the following: 

|**Field**| **Definition and notes**|
|-----------|-----------|
|**Attributes for Insights & Alerts**   | Narrow down alerts, if desired. If left empty, all attributes are incorporated (other than nonreportable fields and emails)   |
|**Default Comparison**   | Your preferred default comparison statistic. If left empty, it will default to Benchmark.   |
|**Benchmark Suite**   | The comparison benchmark chosen for your platform    |
|**Internal Benchmarks**   | Viva Glint’s three internal default benchmarks that cannot be removed. Up to ten more may be added     |
|**Comments Privacy: Minimum # of Responders for Search Results**   | Minimum number of responses to a survey before comments are viewable and searchable | 
|**Comments Privacy: Minimum # of Responders for Facet/Grouping**   | Minimum number of responses to a survey before comments are available for specific groupings  | 
|**Confidentiality Threshold**   | Numerical scores can't be displayed for respondent groups smaller than this number of respondents. The default number is five (5).  |   
|**Exclude Negative Strengths and Positive Weaknesses**   | Remove items that how negative scoring as strengths and positive scoring as weaknesses   |   
|**Insight Minimum Group Size**   | Minimum number of responses before insights and alerts can be shown    |  
|**Insight Minimum Score Difference**   | Minimum number of responses before showing differences in insights and alerts     | 
|**Minimum Sample Survey Stats**   | Response rate won't be displayed for groups smaller than this set number. This is based on group size, not on number of responses and it must match the confidentiality threshold.      | 
|**PowerPoint Template**   | Customer chosen default template. If unset, it defaults to the Viva Glint default template.       | 
|**Broader Team Insights PowerPoint Template**   | Customer chosen default Broader Team Insights template. If unset, it defaults to the Viva Glint default template.        |  
|**Primary Hierarchy**   | The hierarchy your company identified as the first level for reporting, typically Manager |  
|**Secondary Hierarchy**   | The hierarchy your company identified as its second level for reporting, typically Location | 
|**Rating Questions Scale**   | The defaults survey rating questions use. Viva Glint’s best practice is to use a 5-point scale | 
|**Suppression Threshold**   | Suppression occurs if there aren't enough respondents to meet confidentiality requirements. The Viva Glint Suppression Threshold default is two (2) but depends upon the confidentiality threshold.  |  
|**Cross-Program Filtering**   | Turns on cross-program filtering within reports. Enables user roles to compare employee groups across different survey programs and cycles   |   
|**Dashboard in-Product Feedback**   | An in-product feedback form available for some users |

## Set up the Engage Survey Details section 

Choose your survey access method:

|**Field**| **Definition and notes**|
|-----------|-----------|
|**Send SSO Link in Survey Emails**   | Sends an SSO link for survey users to enter the survey   | 
|**Enable Generic Survey Login page**   | Enables or disables the generic sign-in site    |  
|**Attributes for Generic Survey Login page**   | Choose the attributes employees will use to authenticate themselves for survey access     |  

## Set up the Features section 

In this section you will:  

- Enable or disable program templates and Focus Area visibility and privacy settings. 
- Set limits for the number of survey cycles that will show on a dashboard.  
- Set maximum participation numbers for programs. 
  
Edit the following: 

|**Field**| **Definition and notes**|
|-----------|-----------|
|**Available Survey Questions and Program Templates**   |Deselect any program types that you won’t be using to delete their items from your platform. You can edit this at any time.    |   
|**Team Conversation Enabled**   |Enables Team Conversations for recurring surveys   |  
|**Default Goal Privacy**   |Choose the visibility/privacy setting for users creating a new goal  |
|**Maximum Number of Pulse Cycles for Trend**   |Default is five (5) cycles. Applies only to recurring and ad-hoc surveys. This controls the number of cycles that will show on the dashboard and in reporting.    |

## Set up the Technical Configuration section 

In this section you will make selections that help determine how users access their dashboard by enabling and choosing from: 

- Username and password for SSO users 
- Employee ID 
- SFTP IP addresses 

|**Field**| **Definition and notes**|
|-----------|-----------|
|**Unique Employee ID**   |Select "View Only" to remove all users' ability to edit or set up new Viva Glint surveys, "View and Edit" to allow only edits to existing surveys, and "View and Create" to allow full survey edits and set up abilities    |
|**SFTP IP Addresses**   |Viva Glint will verify all public IP addresses that connect to your SFTP account     |

## Set up the Translations section 

English is the default language for all programs, but surveys and emails may be sent to employees in their preferred language. Viva Glint has 70+ language translations for standard content that can be set during the initial configuration or added later, until the survey is live.  

In this section: 

- Set the list of languages to include for comment analysis. 
- Enable or disable comment translation. 
- Indicate the default language for surveys. 
- Provide the additional languages you need supported within the survey. 
- Indicate the default language for your dashboard. 
- Provide the languages available for employee dashboards. 

|**Field**| **Definition and notes**|
|-----------|-----------|
|**Comment Analytics Language**   |The list of codes for languages to include for comment analysis. Empty value signifies English only.    |
|**Default Survey Language**   |Provides the default language for surveys. If a preference isn't populated per employee, this language is shown as a default.     |
|**Supported Survey Languages**   |Lists all languages chosen by the admin to support surveys within your organization. This is a global setting and can be tailored on a per-program level.     |
|**Default Dashboard Language**   |Provides the default language for dashboards. If a preference isn't supplied/selected per employee, this language is shown as a default.      |
|**Supported Dashboard Languages**   |These are the languages available for your dashboard. Your users can select any of these as their static, preferred view.       |
