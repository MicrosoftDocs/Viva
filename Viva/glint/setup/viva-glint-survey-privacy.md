---
title: How Viva Glint protects your privacy
description: Viva Glint is constantly evolving ways to protect confidentiality to encourage high levels of survey participation and honest and helpful feedback.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
ms.collection: 
- essentials-privacy
f1.keywords: NOCSH
keywords: Thresholds, suppression, response rate, suppressed data, identifiable surveys
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: concept-article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 10/17/2024
---

# How Viva Glint protects your privacy

Data privacy and trust are key priorities for Microsoft Viva Glint. Individual privacy is a core Viva Glint value. When survey respondents feel confident that their privacy is protected, they're more likely to participate in surveys and provide honest and constructive feedback. This enables you to get the most from your Glint programs.

Glint offers two types of surveys: confidential and identifiable.

## Confidential surveys

For confidential surveys, Glint aggregates (group averages) responses before reporting results. It's easier to guess a survey taker's identity when there are just a few responses. For this reason, confidential survey responses are reported *only* when an item meets the confidentiality threshold for responses. Your organization chooses this number and it might differ for survey *items* versus *comments*. 

For a survey to be confidential, the minimum number of responses is three (3). 

## Identifiable surveys

In Identifiable surveys, survey takers' identities might be directly or indirectly available within reporting. The minimum response threshold for these surveys is *less than three*. An example of an identifiable survey could be a company's Exit survey, where viewing responses for each departing employee is necessary.

>[!IMPORTANT]
>Admins can make Glint Employee Lifecycle and Always-On surveys identifiable in **Program Setup,** in the **Confidential Responses** setting. This setup automatically updates thresholds at the survey level.

## Use your organization's statement about privacy

At the beginning of each Glint survey, survey takers are presented with a privacy statement configured by your organization. 

A privacy statement provides information about who can see survey takers' identifiable responses and under what circumstances. It specifies whether the survey is confidential or identifiable and the minimum response threshold set by your organization. It also notifies survey takers of any potential admin access to identifiable survey responses and provides links to more Microsoft privacy documentation. Your organization can include a link to its employee privacy policy or other documentation about how it handles survey data.

## Privacy statements inform access and data handling of survey responses

Even for confidential surveys, your organization's customer admin might be able to access identifiable survey responses. Access might be necessary for an organization to meet its legal obligations, such as [Data Subject Rights under GDPR](/microsoft-365/admin/security-and-compliance/gdpr-compliance?view=o365-worldwide&preserve-view=true). Your organization can opt out of this access on a survey-by-survey basis using admin controls. 

> [!IMPORTANT]
> A statement is automatically selected based on your program setup configurations.

### Confidential survey statement: surveys that *don't* support raw survey responses export

If your organization restricts the export of raw survey responses for confidential surveys, this statement is applied to surveys: 

> Your responses are confidential and reported to [Organization Name] in aggregate groups of five or more respondents. Write-in comments are reported verbatim if at least 10 people respond to a question. Take care not to identify yourself in the comments. [Microsoft Viva Glint Reporting and Confidentiality](/viva/glint/reports/confidentiality-suppression-reports) describes other ways your data might be accessed and your organization's privacy policy also has more information.

### Confidential survey statement: surveys that *do* support raw survey responses export

If your organization approves making raw survey responses available, survey takers are informed in this statement:

> Your responses are confidential and reported to [Organization Name] in aggregate groups of five or more respondents. Write-in comments are reported verbatim if at least 10 people respond to a question. Take care not to identify yourself in the comments. A limited number of people at [Organization Name] will have access to your identifiable survey ressponses. See [Microsoft Viva Glint Reporting and Confidentiality](/viva/glint/reports/confidentiality-suppression-reports), which describes other ways your data may be accessed and your organization's privacy policy.

> [!IMPORTANT]
> - ***Organization Name*** and ***confidentiality thresholds*** macros pull in your organization's name and threshold information.
> - The phrase "Privacy Policy" in each statement becomes a hyperlink to your organization's policy. This link is set up in the [General Settings](/viva/glint/setup/manage-general-settings) feature.

## Survey statement: identifiable surveys

If your organization opts to create an identifiable survey, this statement is applied:

> Note that this is an identifiable survey, which means [Organization Name] will be able to see that your survey responses came from you. See your organization's Privacy Policy for more information. Learn how Glint handles survey responses in [Microsoft Viva Glint Reporting and Confidentiality](/viva/glint/reports/confidentiality-suppression-reports).

> [!NOTE]
> Confidentiality and comments thresholds set for programs automatically becomes your program defaults.

