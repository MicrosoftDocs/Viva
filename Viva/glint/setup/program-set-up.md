---
title: Program setup in Program Summary
description: In Program Setup you define the basics of your program, such as its name and what languages are needed, along with confidentiality directives.
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
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 09/10/2024
---

# Program Setup in Program Summary

The **Program Setup** page is the first configuration page within **Program Summary**. This is where you define the basics of your program.

:::image type="content" source="../../media/glint/setup/program-setup-from-program-summary.png" alt-text="Screenshot that shows the Program Setup page for configuration within the Program Summary.":::

## Define the basics  

:::image type="content" source="../../media/glint/setup/program-summary-setup-vg.png" alt-text="Screenshot that The Basics section of Program Setup.":::

1. Enter a **Program Name**.
1. Select the adminis by searching by **Role** or entering their name into the **Search** feature.
1. Select the **Default Language** from the dropdown menu.
1. The list of **Additional Languages** is prepopulated with languages set up for your organization in **General Settings**. To remove languages, select the **X** next to the language name.
1. **Admin Notifications** These admins are notified of upcoming surveys. They are prepopulated in the General Settings feature. Use the **Search** field to find other admins to add.
1. Use the **Suggested Action Available** toggle to disable or enable users to create goals.
1. Use the **Eligible for Nudges** toggle to disable or enable timely messages to managers. Refer to the [Nudges lesson](https://www.microsoft.com).  
1. Confidential Responses are set to **YES** by default.  
1. Enable **Allow Survey Resubmission** so that participants have the ability to retake their surveys by selecting a link on the survey Thank You page. **NO** means that this feature is disabled and users can't resubmit survey responses.

>[!NOTE]
>To remove an admin, select **X** next to their name.

1. **Enable Team Conversations** is enabled by default. **NO** disables the feature for the program. For more information, see [Team Conversations](https://go.microsoft.com/fwlink/?linkid=2286203). 
1. When Team Conversations is enabled, **Enable Team Conversations Sharing** is enabled by default. **NO** disables managers from sharing this read-only version of Team Conversations.  
1. Select the right-facing arrow symbol to **Save and continue**.

## Confidentiality

:::image type="content" source="../../media/glint/setup/program-setup-confidentiality.png" alt-text="Screenshot that shows the Confidentiality setup within Program Setup.":::

**Confidential responses** is set to **Custom Confidential** by default to promote accurate feedback.

1. **Enable Export of Raw Survey Responses** - Enabling this functionality allows admins to export ungrouped, identifiable survey responses. Disabling this function permanently disallows access to or export of those responses, including the ability to transfer the data to a third party. [Learn more about raw survey access](/../../viva/glint/setup/employee-raw-data-export).
1. **Company Message to Survey Participants** - Allows organizations to add more details tailored to their organization, aiming to ensure that individuals participating in surveys are well informed. Clients may wish to append information like specifying the organizational roles with access to identifiable responses or designating appropriate points of contact within the organization for inquiries or concerns related to the survey. You can also add guidelines on the proper utilization of the survey and direct respondents towards their company-specific resources for more details. This text gets added at the beginning of the survey under the title “Message from [<Client_Name>],” directly following Glint’s confidentiality statement.

>[!NOTE]
> - Translations for the Company Message must be done manually.
> - The character limit for the Company Message to Survey Participants is 1,024.

>[!TIP]
> - Custom messaging previously set up within General Settings but edited at the survey level, overrides the initial messaging - **survey level custom messaging takes precedence**.
> - **Employee Lifecycle surveys often target only a few individuals.** For this reason, reducing your confidentiality threshold helps protect their privacy.

### Next Step
> [!div class="nextstepaction"]
> [Distribution setup in Program Summary](../../glint/setup/distribution-program-summary.md)

