---
title: Install Viva Sales
description: Learn what are the various ways to install Viva Sales
ms.date: 08/01/2022
ms.topic: article
ms.service: viva
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.subservice: viva-sales
---

# Install Viva Sales

> [!IMPORTANT]
> Viva Sales is currently available only for public preview customers, and only in English. The features described here are subject to change.

You need to be a Microsoft 365 administrator to deploy and install the Viva Sales add-in for Outlook. You need to be a Teams administrator to deploy and install Viva Sales for Teams.

You can install Viva Sales as an integrated app on multiple platforms or as an individual add-in on a single platform. Whichever method you choose, you can start from either the Microsoft 365 admin center or Microsoft AppSource to install it in Outlook and assign users. If you start from AppSource, you'll finish installation in the Microsoft 365 admin center. Either way, we recommend an administrator install it for best performance and usability. 

The add-in is enabled in Teams but not installed. You need to go to the Microsoft Teams admin center and create setup policies to install the app and assign users. If you install the Viva Sales app for Teams from AppSource, you'll install it to your personal scope only, not for your users.

> [!NOTE]
> - If your users are using Salesforce, ensure that Microsoft Power Platform is not blocked. You can check its status on the **Connected Apps OAuth Usage** page in Salesforce.
> - It can take up to 24 hours for the add-in to show up for your users.


## Minimum privileges required to use Viva Sales

### Dynamics 365

|Table  |Functionality  |Privileges  |
|---------|---------|---------|
|Tagged Record     | Mark a contact as a customer.  |  Create, Read, Write, Delete, Append, Append To       |
|CRM Connection     | Create connection to Dynamics 365 instance.   | Create, Read, Write, Delete, Append, Append To        |
|Note     | Create, update, and associate notes with the marked customer.  | Create, Read, Write, Delete, Append, Append To        |
|Contact     | Retrieve contact data in contact card and update standard fields in the contact card.  | Read, Write, Append, Append To        |
|Account     | Show a contact's related account information in the contact card and associate contact with an account.   | Read, Append, Append To     |
|Opportunity   | Read the opportunity associated with the contact and is the stake holder in the opportunity.        | Read Opportunity, Read Connection and Read Connection Role        |
|User     | Create connections in Dynamics 365.       |  Read User       |

### Salesforce


|Table  |Functionality  |Privileges  |
|---------|---------|---------|
|Contact     | Retrieve contact data in contact card and update standard fields in the contact card.    |Read, ReadAll, Update           |
|Account     | Show a contact's related account information in the contact card.         | Read, ViewAll     |
|Opportunity     | Show a contact's related opportunity information in contact card.        | Read, ViewAll       |


### See also

[Install Viva Sales from Microsoft 365 admin center](install-viva-sales-individual-add-in-admin-center.md)<br>
[Install Viva Sales from AppSource](install-viva-sales-individual-add-in-appsource.md)<br>
[Install and pin Viva Sales in Teams](install-pin-viva-sales-teams.md)