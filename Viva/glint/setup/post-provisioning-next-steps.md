---
title: Add administrators to your Viva Glint instance
description: Take care of a few items of business before you begin your first Viva Glint program journey.
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: Add administrators to Viva Glint, Viva Glint sites, Viva Glint learning paths and modules, training
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high pri
ms.date: 04/21/2023
---

# Add administrators to your Viva Glint instance

As the tenant Global Admin, you're the default Microsoft Viva Glint Service Admin. This means you have ultimate control over the subscriptions in your Viva Glint product and you can access all data. Additionally - and importantly - you can assign Viva Glint Service admin roles to other users.

> [!NOTE]
> Administrators** for Viva Glint are assigned within the Viva Glint product only, not through the Microsoft Administrator Center (MAC).

## Assign Viva Glint Service admins to the Company Admin role

Choose either of the following methods:

> [!TIP]
> Viva Glint recommends no more than five (5) administrators for your Viva Glint instance.

### Option 1

Assign service admins by first providing a full employee attribute upload:

1. Use this Viva Glint guidance to finalize attributes, prepare an employee data file, set up attributes, and upload your employee data to the Viva Glint platform:
   1. [Viva Glint employee attribute fundamentals](https://go.microsoft.com/fwlink/?linkid=2230738)
   2. [Create your Employee Attribute Template in Viva Glint](https://go.microsoft.com/fwlink/?linkid=2230862)
   3. [Set up attributes in Viva Glint](https://go.microsoft.com/fwlink/?linkid=2231120)
   4. [Upload your employee attributes to Viva Glint](https://go.microsoft.com/fwlink/?linkid=2230742).
2. Assign admins to the Company Admin role in Viva Glint:
   1. From the admin dashboard, select the **Configure** symbol, then in **Employees**, choose **People**.
   2. In the **Search People** field, enter the user's first and last name or email address.
   3. Select the user when they appear as a search result.
   4. On the user's detail page, in **Users Roles**, select the **pencil symbol** to edit.
   5. In the **Customer User Role** dialog, select the **Company Admin** checkbox and then **Save**.
   6. In the **Confirm Role** dialog, select **Grant All Access**.
   7. To grant the admin access to Advanced Configuration from their user detail page, select the **pencil symbol** next to **Company Admin: Advanced Configuration Access**.
   8. In the **Advanced Configuration Access dialog** , switch the **Enable access** to ON, and then **Save**.

### Option 2

In order for you, as the Global administrator, to assign service admins without first providing an employee data upload and instead assign another admin role to the task:

1. From the admin dashboard, select the **Configure** symbol, then in **Employees**, choose **People**.
2. In the **Actions** dropdown menu, select **Add a Support User**.
3. Enter the First Name, Last Name, and Email on file in Azure AD for this user.
4. The **Company Admin User Role** will be selected by default and grants users full access to your Viva Glint account.
5. Leave the **External user** toggle set to NO.
6. Switch the **Grant user advanced configuration access** setting to Yes to allow users access to **Advanced Configuration** features.
7. Select **Add support user.**