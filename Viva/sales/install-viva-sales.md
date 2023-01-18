---
title: Install Viva Sales
description: Learn what are the various ways to install Viva Sales
ms.date: 10/28/2022
ms.topic: article
ms.service: viva
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.subservice: viva-sales
---

# Install Viva Sales

You need to be a Microsoft 365 administrator to deploy and install the Viva Sales add-in for Outlook. You need to be a Teams administrator to deploy and install Viva Sales for Teams.

You can install Viva Sales as an integrated app on multiple platforms or as an individual add-in on a single platform. Whichever method you choose, you can start from either the Microsoft 365 admin center or Microsoft AppSource to install it in Outlook and assign users. If you start from AppSource, you'll finish installation in the Microsoft 365 admin center. Either way, we recommend an administrator installs it for best performance and usability. 

The add-in is enabled in Teams but not installed. You need to go to the Microsoft Teams admin center and create setup policies to install the app and assign users. If you install the Viva Sales app for Teams from AppSource, you'll install it to your personal scope only, not for your users.

> [!NOTE]
> - If your users are using Salesforce, ensure that Microsoft Power Platform is not blocked. You can check its status on the **Connected Apps OAuth Usage** page in Salesforce.
> - It can take up to 24 hours for the add-in to show up for your users.


## Privileges required to use Viva Sales

Viva Sales applies your organization's existing CRM access controls and user permissions. Administrators must have correct permissions to customize their CRM systems, and users must have the correct permissions to view, update, and create records in their CRM systems from Viva Sales.

### Permissions required for Salesforce administrators

Salesforce administrators who need to customize Viva Sales must have the following permissions.

|Requirement type  |You must have  |
|---------|---------|
|Permission    |  User profile needs to have **Modify All Data** or **Manage Data Integrations** permission  |

### Additional privileges required for Dynamics 365 customers

#### Dynamics 365 administrators

If you are using out-of-the-box System Administrator or System Customizer security roles, Viva Sales administration privileges are added automatically. If you are using custom security roles, you must assign the following security role to Dynamics 365 administrators who need to customize Viva Sales. 

|Requirement type  |You must have  |
|---------|---------|
|Security role     | Viva Sales Administrator |

#### Dynamics 365 sellers

If you're using the out-of-the-box Salesperson or Sales Manager security roles, Viva sales privileges are added automatically. If you're using custom security roles, you must assign the following privileges to the custom security role to use Viva Sales.

|Table  |Functionality  |Privileges  |
|---------|---------|---------|
|Tagged Record     | Match and connect an external contact to a CRM contact automatically.  |  Create, Read, Write, Delete, Append, Append To       |
|CRM Connection     | Create connection to Dynamics 365 instance.   | Create, Read, Write, Delete, Append, Append To        |
|Note     | Create, update, and associate notes with the marked customer.  | Create, Read, Write, Delete, Append, Append To        |
|User     | Create connections in Dynamics 365.       |  Read User       |

## How to use Viva Sales?

After you install Viva Sales for your users, they can start using it in Outlook and Teams. For information on how to use Viva Sales, see:

- [Use Viva Sales in Outlook](https://support.microsoft.com/topic/use-viva-sales-in-outlook-ec3605f9-fdb0-4593-9c5b-b43a76c07081)
- [Use Viva Sales in Teams](https://support.microsoft.com/topic/use-viva-sales-in-teams-04286b82-bdf8-4e37-94ce-be1943b2d6ea)

### See also

[Install Viva Sales from Microsoft 365 admin center](install-viva-sales-individual-add-in-admin-center.md)<br>
[Install Viva Sales from AppSource](install-viva-sales-individual-add-in-appsource.md)<br>
[Install and pin Viva Sales in Teams](install-pin-viva-sales-teams.md)