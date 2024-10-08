---
title: Privacy protection within 360 feedback programs
description: The confidentiality statement displayed for 360 feedback participants depends on the type of feedback provider, the confidentiality threshold, and the Feedback Provider Response Information setting. 
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
ms.collection: 
- essentials-privacy
f1.keywords: NOCSH
keywords: Thresholds, suppression, response rate, suppressed data, 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: concept-article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 10/08/2024
---

# Privacy protection in 360 feedback programs

## 360 feedback programs

The confidentiality statement displayed for 360 feedback participants depends on the type of feedback provider, the selected confidentiality threshold, and the Feedback Provider Response Information setting in a 360 feedback cycle. Review this information to see the statement that displays for each user in each situation.

> [!IMPORTANT]
> Thresholds can't be lowered or raised for a program or cycle after it's launched. 

|Feedback provider  |Confidentiality threshold   |Feedback provider response information setting |Confidentiality statement|
|:----------|:-----------|:------------|:------------|
|Self     |1       |On or Off        |Your feedback is visible to you and a limited number of people that are granted permission by your organization to view your 360 report. See your organization’s Privacy Policy for more information. Learn how Viva Glint handles survey responses in [Microsoft Viva Glint Reporting and Confidentiality Rules](viva-glint-survey-privacy.md). |
|**Non-subject**: Manager, Skip-level manager, or Custom   |1               |On or Off |This survey is identifiable, which means Contoso is able to see that your survey responses came from you. Whether you responded, as well as your feedback, will be visible to _`<360 subject’s full name>`_ and people that are granted permission by your organization. See your organization’s Privacy Policy for more information.        |
|**Non-subject**: Directs, Peers, Colleagues, or Custom    |3 or more       |Off       |Your responses are confidential and reported to Contoso in aggregate groups of three or more respondents, including any write-in comments which are reported verbatim. Take care not to identify yourself in the comments. Your aggregated feedback will be visible to _`<360 subject’s full name>`_ and people that are granted permission by your organization.   |
|**Non-subject**: Directs, Peers, Colleagues, or Custom    |3 or more       |On        |Your responses are confidential and reported to Contoso in groups of three or more respondents. This report includes write-in comments, which are reported verbatim. Take care not to identify yourself in the comments. Whether you responded, and your aggregated feedback, is visible to _`<360 subject’s full name>`_ and people granted permission by your organization. |

> [!IMPORTANT]
> - "Contoso" and confidentiality thresholds in statements pull in your organization's name and threshold information.
> - The phrase "Privacy Policy" in each statement becomes a hyperlink to your organization's policy when configured in [General Settings](/viva/glint/setup/manage-general-settings).

## More resources

[Manager Quick Guide to Confidentiality](/viva/glint/setup/quick-guide-confidentiality)
[Viva Glint confidentiality thresholds](/viva/glint/setup/manage-confidentiality-thresholds)
