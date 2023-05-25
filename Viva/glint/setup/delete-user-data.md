---
title: Delete user data from Viva Glint
description: Admins can request that user data be immediately deleted from the Viva Glint system.
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: Deleted data, deleted employee data
ms.collection: 
 - M365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
localization_priority: high pri
ms.date: 04/28/2023
---

# Delete user data from Viva Glint

As your company’s data controller, Microsoft Viva Glint admins can submit a user data deletion request to comply with a General Data Protection Regulation (GDPR) data subject request. The deletion requests will be processed right away.

>[!NOTE]
>User data deletion in Viva Glint is an irreversible process.

## User data can be deleted from the People section on the admin dashboard

>[!IMPORTANT]
>Deleting a user from Azure Active Directory does not delete the user and their information from Viva Glint. To delete user information from Viva Glint, you must complete the instructions provided below.

1. Select People from the Employees section.
2. Use the search box to select the employee whose data should be deleted. Open that employee’s page.
3. From the Actions dropdown menu, choose Delete User.
4. A Delete User Confirmation box displays with this information:
     1. Data will be removed from Viva Glint except for essential account information associated with your organization’s Microsoft subscription.
     2. To include later, the information must be reuploaded into your company’s HRIS data.
     3. By deleting the user,
         1. Survey results from Viva Glint reports will be deleted, possibly impacting reports.
         2. The user’s data is removed from distribution list and future surveys.
         3. The user’s role definitions and their reporting permissions are removed.
     4. The display will indicate whether the user has direct reports and that the admin will have to reassign the reports later or in the next HRIS file import.
5. Go back to the People page and verify that the username does not appear in the list of All, Active or Inactive employees.
6. Return to the admin dashboard and select Activity Audit Log in the Client Settings section. The action taken should be listed first in the Event column and its status should read “Success” and the Details column “deleted.”
7. If the deleted user is a manager, verify that all reports they had been permissioned for no longer include their name. The report will now read, “Deleted User’s Team.”

>[!NOTE]
> Should a deleted user be reinstated to your organization, their data will need to be uploaded as if they are a new employee. No previous data is stored once deleted.
