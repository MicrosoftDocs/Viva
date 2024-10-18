---
title: Duplicate, delete, and disable surveys in Viva Glint
description: As your company’s data controllers, Microsoft Viva Glint Administrators can, duplicate, delete, and disable surveys.  
ms.author: Judithweiner
author: JudyWeiner
manager: mbarry
audience: admin
f1.keywords: NOCSH
keywords: 
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint 
ms.localizationpriority: high 
ms.date: 10/09/2024
---

# Duplicate, delete, and disable surveys in Viva Glint

As your company’s data controllers, Microsoft Viva Glint Administrators can duplicate, delete, and disable surveys.

:::image type="content" source="../../media/glint/setup/survey-management-menu.png" alt-text="Screenshot of the Glint Survey Programs page showing the Duplicate, Delete, and Disable menu options for a selected survey.":::

## Duplicate a survey

Survey duplication copies all survey settings and translations from the selected survey program. To duplicate a survey in Glint, follow this process:

1.  Select **Survey Programs** from your admin **Configuration** page. 
1.  Use the search box or go to the **Survey Programs** list to identify the survey that should be duplicated.
1.  Select the three dots and then from the dropdown menu, choose **Duplicate**.
1.  You're directed to the Program Summary for the copied survey program, which is automatically named "*original survey name" Copy*. For example, "Quarterly Engagement Copy."
1.  Leave the duplicated survey name as is or give it a new unique survey program name by selecting the pencil icon to edit.

## Delete survey data

Survey deletion is available for all nonactive surveys. This feature deletes every data entity directly related to the survey, including overall survey configuration, items/questions, reports, responses, etc. The action doesn't delete distribution lists or any roles related to the survey. 

> [!NOTE]
> Viva Glint admins must have [Advanced Configuration access enabled](understand-advanced-configuration.md#grant-access-to-an-existing-admin-user) to delete survey data.

> [!CAUTION]
> Survey data deletion in Glint is an irreversible process. Perform this action only when confident that the data of the survey is not required anymore. 

To delete survey data from Glint, follow this process:

1.  Select **Survey Programs** from your admin **Configuration** page. 
1.  Use the search box or navigate to the **Survey Programs** list to identify the survey that data should be deleted from. 
1.  Select the three dots and then from the dropdown menu, choose **Delete**.
1.  A **Survey Delete** confirmation box asks for confirmation and displays the following message: "This will permanently delete all data associated with this program."
1.  If you aren't sure if they should complete the action, select **No, I am not sure**, otherwise **confirm the action**. 
1.  Once the delete action is completed, return to the Survey page to verify that the survey doesn't appear in the Survey Programs list.

## Disable a survey

> [!CAUTION]
> Disabling a survey removes all survey results for survey cycles associated with the program. Don't disable a survey program unless you want to remove all cycles in that program.

To disable a survey in Glint, follow this process:

1.  Select **Survey Programs** from your admin **Configuration** page. 
1.  Use the search box or navigate to the **Survey Programs** list to identify the survey that should be disabled. 
1.  Select the three dots and then from the dropdown menu, choose **Disable**.
1.  The survey now appears in the **Disabled** category in the status menu on the **Survey Programs** page and **all survey results for the program's cycles are no longer available**.

To enable a disabled survey in Glint, follow this process:

1.  Select **Survey Programs** from your admin **Configuration** page. 
1.  Select **Disabled** in the survey status menu to view disabled surveys.
2.  Use the search box or navigate over the **Survey Programs** list to identify the survey that should be enabled. 
1.  Select the three dots and then from the dropdown menu, choose **Enable**.
2.  The survey is available to edit and launch, but all survey response data present before the survey was disabled are inaccessible.
