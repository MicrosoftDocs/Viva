---
title: Program setup in Program Summary
description: In Program Setup you define the basics of your program, such as its name and what languages will be needed, along with confidentiality directives.
ms.author: JudithWeiner
author: JudyWeiner
manager: elizapo
audience: admin
f1.keywords: NOCSH
keywords: confidentiality setup
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 01/08/2024
---

# Program Setup in Program Summary

The Program Setup page is the first configuration page within Program Summary. It allows you to define the basics of your program.

:::image type="content" source="../../media/glint/setup/program-setup-from-program-summary.png" alt-text="Screenshot that shows the Program Setup page for configuration within the Program Summary.":::

## Set up the first section - Define the basics for your program  

1. Enter a **Program Name**.
1. Select the administrators by searching by **Role** or entering their name into the **Search** feature.
1. Select the **Default Language** from the dropdown menu.
1. The list of **Additional Languages** is open and prepopulated with languages that have been set up for your organization in **General Settings**. To remove languages, select the **X** next to the language name.
1. **Admin Notifications** To are prepopulated. Use the **Search** field to add other admins. To remove an admin, select *X* next to their name.
1. Use the **Suggested Action Available** toggle to disable or enable users to create goals.
1. Use the **Eligible for Nudges** toggle to disable or enable timely messages to managers. Refer to the [Nudges lesson for additional setup](https://www.microsoft.com).  
1. Confidential Responses are set to YES by default.  
1. Enable **Allow Survey Resubmission** so your company admin will have the ability to reset a user's survey so that they may retake or edit their submission. **NO** means that this feature is disabled and the Viva Glint admin will not be able to reset surveys for survey takers.
   > [!TIP]
   > In order for your survey takers to reacess a survey, enable your managers with **Allow Survey Resubmission** enablement by toggling this setting to **YES**.

   :::image type="content" source="../../media/glint/setup/program-setup-survey-resubmit.png" alt-text="Screenshot that shows how to enable Allow Survey Resubmission so managers can reset surveys for survey takers.":::

1. **Enable Team Conversations** is enabled by default. **NO** disables the feature for the program. For more information, see Team Conversations. 
1. When Team Conversations is enabled, **Enable Team Conversations Sharing** is enabled by default. **NO** disables managers from sharing this read-only version of Team Conversations.  
1. Select the right-facing arrow symbol to **Save and continue**.

## Set up the second section - Confidentiality

The first toggle is set to YES by default. Confidential responses promote accurate feedback.

1. **Enable Export of Raw Survey Responses** - Enabling this functionality allows admins to export unaggregated, identifiable survey responses. Disabling this function permanently disallows the ability to access or export that survey's unaggregated, identifiable responses including the ability to transfer the data to a third party. [Learn more about raw survey access](/../../viva/glint/setup/employee-raw-data-export)
1. **Company Message to Survey Participants** - Allows organizations to incorporate additional details tailored to their organization, aiming to ensure that individuals participating in surveys are well informed. Clients may wish to append information like specifying the organizational roles with access to identifiable responses or designating appropriate points of contact within the organization for inquiries or concerns related to the survey. Additionally, they may intend to provide supplementary guidelines on the proper utilization of the survey and direct respondents towards their company-specific resources for more details. This text gets added at the beginning of the survey under the title “Message from {{Client_Name}},” directly following Viva Glint’s confidentiality statement.

>[!NOTE]
>The character limit for the Company Message to Survey Participants is: 1024.

>[!TIP]
>Custom messaging previously set up within General Settings but now edited at the survey level, overrides the initial messaging - **survey level custom messaging takes precedence**.

:::image type="content" source="../../media/glint/setup/platform-setup-confidentiality-new-message.png" alt-text="Screenshot that shows the Confidentiality configuration within Program Setup.":::

### Next Step
> [!div class="nextstepaction"]
> [Distribution setup in Program Summary](../../glint/setup/distribution-program-summary.md)

