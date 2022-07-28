---
title: Introduction to Microsoft Viva Sales
description: Get to know Viva Sales
ms.date: 07/25/2022
ms.topic: article
ms.service: viva
author: sbmjais
ms.author: shjais
manager: shujoshi
---

# Introduction to Microsoft Viva Sales

> [!IMPORTANT]
> Viva Sales is currently available only for public preview customers, and only in English. The features described here are subject to change.

Microsoft Viva Sales is a seller experience application that uses Microsoft 365 and Microsoft Teams to automatically capture, access, and register data into any customer relationship management (CRM) system. It eliminates manual data entry and gives sellers more time to focus on selling. By enriching the data set with customer engagement data from Microsoft 365 and the power of AI, Viva Sales empowers sellers with sales intelligence that helps them deeply understand their customers for faster deal closure. Viva Sales is designed to help sellers boost productivity, lighten workloads, save time, and help salespeople sell more.

## License requirements

While in public preview, Viva Sales is available at no additional charge to organizations that use Microsoft 365 and Teams. You must have valid credentials for Dynamics 365 or Salesforce CRM to try out the full public preview experience. When Viva Sales is made generally available, you'll need to purchase licenses to use it.

## Region availability

The public preview is currently available globally except for a few selected countries such as Russia, France, and Canada.

## Handling data for Viva Sales 

This articles gives you an overview of how data is handled for Viva Sales. Viva Sales is built on the [Microsoft Power Platform](https://powerplatform.microsoft.com/) and data is stored in [Dataverse](/powerapps/maker/common-data-service/data-platform-intro) in addition to the CRM solution that users are connected to.

### Data retention 

Since Viva Sales data is stored in [Dataverse](/powerapps/maker/common-data-service/data-platform-intro), data retention policies differ from other M365 applications and non-dynamics CRM solutions. For example, when your M365 subscription ends, your data is retained for 90 days before it’s automatically deleted (in accordance to [Office 365 data retention policies](/microsoft-365/compliance/retention-policies)). However, if you use Viva Sales, that data isn’t automatically deleted 90 days after your subscription ends.  

### Viva Sales and Dataverse 

When Viva Sales is connected to a non-dynamics CRM solution, a default Dataverse instance is provided to your tenant. Viva Sales data is stored in the default instance in addition to creating and updating records in your CRM solution of choice.

Administrators can find the name and details of their default Dataverse instance in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/).

For existing Dynamics Sales customers, Viva Sales data is stored together with the connected Dynamics 365 Sales instance.

### Deleting user data 

If you need to delete Viva Sales data (for example, you need to delete data for a specific user) , an admin can choose to [manually delete it](/power-platform/admin/remove-user-personal-data). An admin can also decide to stop using the app and manually delete the default Dataverse instance from the [Power Platform admin center](https://admin.powerplatform.microsoft.com/).  


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

