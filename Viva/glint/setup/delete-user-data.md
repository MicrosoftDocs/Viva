---
title: Delete user data from Viva Glint
description: Admins can request that user data be immediately deleted from the Viva Glint system.
ms.author: JudithWeiner
author: JudyWeiner
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: Deleted data, deleted employee data
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 05/08/2024
---

# Delete user data from Viva Glint

As your company’s data controller, Microsoft Viva Glint admins can submit a user data deletion request to comply with a General Data Protection Regulation (GDPR) data subject request. The deletion requests are
processed right away.

> [!IMPORTANT]
> INACTIVE user data (attributes and responses) aren't automatically deleted from Viva Glint.

> [!CAUTION]
> User data deletion in Viva Glint is an irreversible process.

## User data can be deleted from the People section on the admin dashboard

1. Select **People** from the Employees section.
2. Use the search box to select the employee whose data should be deleted. Open that employee’s page.
3. From the Actions dropdown menu, choose **Delete User**.
4. A Delete User Confirmation box displays with this information:
     1. Data is removed from Viva Glint except for essential account information associated with your organization’s Microsoft subscription.
     2. To include later, the information must be reuploaded into your company’s employee data.
     3. By deleting the user:
         1. Survey results from Viva Glint reports are deleted, possibly impacting reports.
         2. The user’s data is removed from distribution lists and future surveys.
         3. The user’s role definitions and their reporting permissions are removed.
     4. The display indicates whether the user has direct reports and that the admin needs to reassign the reports later or in the next employee data import. Follow these steps to facilitate a [**retroactive user upload update**](/../../viva/glint/setup/update-glint-reporting-data) if past survey data should reflect the new manager.
5. Go back to the **People** page and verify that the user doesn't appear in the list of *All, Active or Inactive* employees.
6. Return to the admin dashboard and select **Activity Audit Log** in the Service Configuration section. The user deletion action should be listed in the Event column and its status should read "Success" and the Details column should show "deleted."
7. If the deleted user is a manager, verify that all reports their team appeared in no longer include their name. The report now reads, "Deleted User’s Team."

> [!NOTE]
> Should a deleted user be reinstated to your organization, their data needs to be uploaded as if they are a new employee. No previous data is stored once deleted.
