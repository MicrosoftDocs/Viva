---

ROBOTS: NOINDEX,NOFOLLOW
title: Activate Workplace Analytics licenses
description: Activate licenses for Workplace Analytics 
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Activate Workplace Analytics licenses

You can only activate additional Workplace Analytics licenses for a Microsoft 365 or an Microsoft 365 tenant with an activation code from Microsoft.

The task of activating licenses has two parts. Each part requires a different Azure Active Directory role:

* **Part 1: Add your activation code** &ndash; The person who completes the steps in this session must have the role of Azure Active Directory [Billing administrator](https://docs.microsoft.com/azure/active-directory/roles/permissions-reference#billing-administrator).

* **Part 2: Confirm the code and turn licenses on** &ndash; The person who completes the steps in this session must have the role of Azure Active Directory [License Administrator](https://docs.microsoft.com/azure/active-directory/roles/permissions-reference#license-administrator).

## To activate Workplace Analytics licenses

### Part 1: Add your activation code

* **Role**: Azure Active Directory [Billing administrator](https://docs.microsoft.com/azure/active-directory/roles/permissions-reference#billing-administrator)

1. Start your web browser, such as Microsoft Internet Explorer, Microsoft Edge, Google Chrome, or Mozilla Firefox, for **InPrivate**, **incognito**, or **Private** browsing.

2. Open a private browsing session in your web browser. Depending on which browser you are using, right-click it and then select **Start InPrivate Browsing**, **New InPrivate window**, **New incognito window**, or **New private window**.

3. Copy the activation code link, which you received from us, paste it into the URL section of the private or incognito browser window, and then press **Enter** to open the link.

   ![Promotional code link](../images/wpa/setup/promo-code.png)  

4. To add the code to your existing environment, select **Sign In** next to **Want to add this to an existing subscription?**

   ![Promotional code sign-in](../images/wpa/setup/sign-in.png)

5. On the **Sign in** page, enter your AAD [Billing administrator](https://docs.microsoft.com/azure/active-directory/roles/permissions-reference#billing-administrator) credentials for the tenant.
6. On the **Check out** page, select **Try Now** to confirm the order.
7. When you get the order receipt, save it and then select **Continue**.

### Part 2: Confirm the code and turn licenses on

* **Role** &ndash; Azure Active Directory [License Administrator](https://docs.microsoft.com/azure/active-directory/roles/permissions-reference#license-administrator)

1. Open the [Microsoft 365 admin center](https://admin.microsoft.com). 

1. To confirm that the codes were successfully added to your environment, go to **Admin Center** > **Users** > **Active Users**.

   For example,  https://portal.office.com/AdminPortal/Home#/users

2. Select a user account, and then next to **Product licenses**, select **Edit**.

   For example, the following screenshot shows 25 new licenses.

   ![Promotional licenses](../images/wpa/setup/promo-licenses.png)  

3. On the **Product licenses** page, use the slider to turn on the available licenses.

## Related topics

* [Assign licenses to the population](../setup/Assign-licenses-to-population.md)

* [Environment requirements for Workplace Analytics](../setup/environment-requirements.md)

* [About admin roles](https://docs.microsoft.com/en-us/microsoft-365/admin/add-users/about-admin-roles?view=o365-worldwide)
