---
title: Install Viva Sales
description: Learn what are the various ways to install Viva Sales
ms.date: 10/03/2022
ms.topic: article
ms.service: viva
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.subservice: viva-sales
---

# Install Viva Sales

You need to be a Microsoft 365 administrator to deploy and install the Viva Sales add-in for Outlook. You need to be a Teams administrator to deploy and install Viva Sales for Teams.

You can install Viva Sales as an integrated app on multiple platforms or as an individual add-in on a single platform. Whichever method you choose, you can start from either the Microsoft 365 admin center or Microsoft AppSource to install it in Outlook and assign users. If you start from AppSource, you'll finish installation in the Microsoft 365 admin center. Either way, we recommend an administrator install it for best performance and usability. 

The add-in is enabled in Teams but not installed. You need to go to the Microsoft Teams admin center and create setup policies to install the app and assign users. If you install the Viva Sales app for Teams from AppSource, you'll install it to your personal scope only, not for your users.

> [!NOTE]
> - If your users are using Salesforce, ensure that Microsoft Power Platform is not blocked. You can check its status on the **Connected Apps OAuth Usage** page in Salesforce.
> - It can take up to 24 hours for the add-in to show up for your users.


## Privileges required to use Viva Sales

Viva Sales applies your organization's existing CRM access controls and user permissions. Users must have the correct permissions to view, update, and create records in their CRM systems from Viva Sales.

### Additional privileges required for Dynamics 365 customers

If you are using the out-of-the-box Salesperson and Sales Manager security roles, Viva sales privileges are added automatically. If you are using custom security roles, you must assign the following privileges to the custom security role to use Viva Sales.

|Table  |Functionality  |Privileges  |
|---------|---------|---------|
|Tagged Record     | Match and connect an external contact to a CRM contact automatically.  |  Create, Read, Write, Delete, Append, Append To       |
|CRM Connection     | Create connection to Dynamics 365 instance.   | Create, Read, Write, Delete, Append, Append To        |
|Note     | Create, update, and associate notes with the marked customer.  | Create, Read, Write, Delete, Append, Append To        |
|User     | Create connections in Dynamics 365.       |  Read User       |


### See also

[Install Viva Sales from Microsoft 365 admin center](install-viva-sales-individual-add-in-admin-center.md)<br>
[Install Viva Sales from AppSource](install-viva-sales-individual-add-in-appsource.md)<br>
[Install and pin Viva Sales in Teams](install-pin-viva-sales-teams.md)