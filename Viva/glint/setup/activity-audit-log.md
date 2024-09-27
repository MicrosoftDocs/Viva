---
title: Viva Glint Activity Audit Log
description: Microsoft Viva Glint Company Admin users have access to the Activity Audit Log to view actions taken in the platform.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: audit log, activity log, platform activity, tasks, admin log, activity audit log
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 09/27/2024
---

# Viva Glint Activity Audit Log

Microsoft Viva Glint Company Admin users have access to the Activity Audit Log to view actions taken in the platform. The log gives details on some user activity, User Role changes, raw data exports, data imports, and error or warning information for failed data imports. The Activity Audit Log includes:

- **Date:** The date and time of when the action was performed
- **Event:** The event type
- **Type:** The type, a subfilter of Event
- **Status:** The event's status: Success or Failed
- **User:** The email address of the user or the system responsible for the event
- **Details:** A description of the event

> [!IMPORTANT]
> The Activity Audit Log keeps a rolling year of platform activity and files are downloadable for 28 days (example: data file upload error files).

## Access the Activity Audit Log

To use the Activity Audit Log as a Viva Glint admin:

1. From the admin dashboard, select the **Configuration** symbol, then in **Service Configuration**, choose **Activity Audit Log**.
2. Select an event type from the **All Events** dropdown menu (example: "Data import").
3. If needed, filter results further by selecting an option from the **All Types** dropdown menu (example: "SFTP" to focus on data sent via secure file transfer protocol).
4. If needed, use the **All Statuses** dropdown menu to filter to successful or failed events.
   
   :::image type="content" source="../../media/glint/setup/glint-activity-audit-log.png" alt-text="Screenshot of the Activity Audit Log filtered to Data import activity for SFTP imports.":::

## Event descriptions

Choose an event type based on platform activity that you need to review and the following descriptions.

| Event  | Description  |
|:----------|:-----------|
| Access disabled | A Company Admin user disabled Advanced Configuration access. |
| Access enabled | A Company Admin user enabled Advanced Configuration access. |
| Company Admin added | A user was added to the Company Admin role. |
| Company Admin login | A Company Admin user logged into Viva Glint. |
| Company Admin logout | A Company Admin user logged out of Viva Glint. |
| Company Admin removed | A user was removed from the Company Admin role. |
| Data app execution logs | Advanced Configuration Data app and Upload activity. |
| Data DSR Control set | User Data controls for survey data deletion in General Settings update activity. |
| Data Import | Employee data import activity. |
| Data export | Employee data export activity. |
| Details changes saved | Change activity in General Settings or Advanced Configuration: Details. |
| Discarding Employee IDs | User Data controls for Employee ID reuse in General Settings update activity. |
| Export Raw Survey Data | Raw response data export activity. |
| Role assigned | A user is assigned to a new role. |
| Role unassigned | A user is removed from a role. |
| Send User Data | Individual employee data and raw survey responses send activity. |
| User added | A user was added to the Support User role. |
| User Deleted | User deletion activity. |
| User role created | User Role creation activity. |
| View as user | Admins' "View As" another user activity. |

## Related resources

### Data import errors and troubleshooting:

- [Resolve file upload errors related to attributes](/viva/troubleshoot/glint/data-file-upload/fix-upload-attributes-errors?toc=%2Fviva%2Fglint%2Ftoc.json&bc=%2Fviva%2Fbreadcrumb%2Ftoc.json)
- [Resolve upload errors related to derived attributes](/viva/troubleshoot/glint/data-file-upload/fix-upload-derivation-errors?toc=%2Fviva%2Fglint%2Ftoc.json&bc=%2Fviva%2Fbreadcrumb%2Ftoc.json)
- [Resolve upload warnings related to duplicate data](/viva/troubleshoot/glint/data-file-upload/fix-upload-duplicate-data-warnings?toc=%2Fviva%2Fglint%2Ftoc.json&bc=%2Fviva%2Fbreadcrumb%2Ftoc.json)
- [Resolve upload warnings related to invalid or unexpected values](/viva/troubleshoot/glint/data-file-upload/fix-upload-invalid-unexpected-values-warnings?toc=%2Fviva%2Fglint%2Ftoc.json&bc=%2Fviva%2Fbreadcrumb%2Ftoc.json)
- [Resolve upload warnings related to manager hierarchy](/viva/troubleshoot/glint/data-file-upload/fix-upload-manager-hierarchy-warnings?toc=%2Fviva%2Fglint%2Ftoc.json&bc=%2Fviva%2Fbreadcrumb%2Ftoc.json)

### User role setup:

- [Set up User Roles](/viva/glint/setup/set-up-user-roles)

### User data management:

- [Delete user data](/viva/glint/setup/delete-user-data)
- [Raw response data](/viva/glint/setup/employee-raw-data-export)
- [Viva Glint People page](/viva/glint/setup/people-page)
- [People page import](/viva/glint/setup/upload-employee-attributes)

### Advanced Configuration and General Settings

- [Advanced Configuration overview](/viva/glint/setup/understand-advanced-configuration)
- [Data apps](/viva/glint/setup/glint-data-apps)
- [Uploads](/viva/glint/setup/advanced-config-uploads)
- [General Settings](/viva/glint/setup/manage-general-settings)
