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
ms.date: 09/17/2024
---

# Delete user data from Viva Glint

As your company’s data controllers, Microsoft Viva Glint Administrators can submit a user data deletion request to comply with a General Data Protection Regulation (GDPR) data subject request. The deletion requests are processed right away.

> [!IMPORTANT]
> - User data deleted from Viva Glint is automatically deleted from *any* Microsoft Viva program it had been shared with.
> - Viva Glint survey responses are kept in reporting unless a Viva Glint Admin chooses to delete them.
> - INACTIVE user data (attributes and responses) aren't automatically deleted from Viva Glint.

> [!CAUTION]
> User data deletion in Viva Glint is an irreversible process.

## Data deletion control

Viva Glint Admins, as data controllers, have the authority to manage survey data in response to a Data Subject Request (DSR). They can choose to either: 

1. Erase all data related to the requester, excluding attributes and survey responses, or
2. Erase all data related to the requester, including survey responses.

This configuration is set at the platform level and applies to all requests equally and is set to exclude attribute and survey responses (option 1) by default. [Learn more](https://go.microsoft.com/fwlink/?linkid=2286286).

## Delete user data

1. Select **People** from the **Employees** section on your Glint admin dashboard.
2. Use the **search box** to select the employee whose data should be deleted. Open that employee’s page.
3. From the **Actions** dropdown menu, choose **Delete User**.
4. A Delete User Confirmation box displays with this information:
     1. Data is removed from Viva Glint except for essential account information associated with your organization’s Microsoft subscription.
     2. To include later, the information must be reuploaded into your company’s employee data.
     3. By deleting the user:
         1. Survey results are deleted, possibly impacting Viva Glint reports, if deletion control is set to off. [Learn more](https://go.microsoft.com/fwlink/?linkid=2286286).
         2. The user’s data is removed from distribution lists and future surveys.
         3. The user’s role definitions and their reporting permissions are removed.
     4. The display indicates whether the user has direct reports and that the admin needs to reassign the reports later or in the next employee data import. Follow these steps to facilitate a [**retroactive user upload update**](/../../viva/glint/setup/update-glint-reporting-data) if past survey data should reflect the new manager.
5. Return to the **People** page and verify that the user doesn't appear in the list of **All, Active or Inactive** employees.
6. Return to the admin dashboard and select **Activity Audit Log** in the **Service Configuration** section. The user deletion action should be listed in the **Event** column and its status should read "Success." The **Details** column should show "Deleted."
7. If the deleted user is a manager, verify that all reports their team appeared in no longer include their name. The report now reads, "Deleted User’s Team."

> [!IMPORTANT]
> - Viva Glint 360 feedback responses are also deleted with these requests.

> [!NOTE]
> Should a deleted user be reinstated, their data needs to be uploaded as if they are a new employee. No previous data is stored once deleted.

## Employee IDs reuse control

Viva Glint Admins, as data controllers, can reuse employee IDs and reassign them to new or rehired employees. They can choose to either: 

1. Exclude data associated with employee IDs of previously removed employees from uploads or
2. Update the already deleted records with the status provided in the HRIS file.

This configuration is set at the platform level, applies to all records equally, and is set to exclude data by default (option 1). [Learn more](https://go.microsoft.com/fwlink/?linkid=2286286).
