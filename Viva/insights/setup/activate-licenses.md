---

ROBOTS: NOINDEX,NOFOLLOW
title: Activate licenses for Viva Insights
description: Activate licenses for Microsoft Viva Insights 
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Activate Viva Insights licenses

You can only activate additional Microsoft Viva Insights licenses for a Microsoft 365 or an Microsoft 365 tenant with an activation code from Microsoft.

The task of activating licenses has two parts. Each part requires a different Azure Active Directory role:

* **Part 1: Add your activation code** - The person who completes the steps in this session must have the role of Azure Active Directory [Billing administrator](/azure/active-directory/roles/permissions-reference#billing-administrator).

* **Part 2: Confirm the code and turn licenses on** - The person who completes the steps in this session must have the role of Azure Active Directory [License Administrator](/azure/active-directory/roles/permissions-reference#license-administrator).

## To activate licenses

### Part 1: Add your activation code

* **Role**: Azure Active Directory [Billing administrator](/azure/active-directory/roles/permissions-reference#billing-administrator)

1. Start your web browser, such as Microsoft Internet Explorer, Microsoft Edge, Google Chrome, or Mozilla Firefox, for **InPrivate**, **incognito**, or **Private** browsing.
2. Open a private browsing session in your web browser. Depending on which browser you are using, right-click it and then select **Start InPrivate Browsing**, **New InPrivate window**, **New incognito window**, or **New private window**.
3. Copy the activation code link, which you received from us, paste it into the URL section of the private or incognito browser window, and then press **Enter** to open the link.

   ![Promotional code link.](../images/wpa/setup/promo-code.png)  

4. To add the code to your existing environment, select **Sign In** next to **Want to add this to an existing subscription?**

   ![Promotional code sign-in.](../images/wpa/setup/sign-in.png)

5. On the **Sign in** page, enter your AAD [Billing administrator](/azure/active-directory/roles/permissions-reference#billing-administrator) credentials for the tenant.
6. On the **Check out** page, select **Try Now** to confirm the order.
7. When you get the order receipt, save it and then select **Continue**.

### Part 2: Confirm the code and turn licenses on

* **Role**: Azure Active Directory [License Administrator](/azure/active-directory/roles/permissions-reference#license-administrator)

1. Open the [Microsoft 365 admin center](https://admin.microsoft.com).
2. To confirm that the codes were successfully added to your environment, go to **Admin Center** > **Users** > **Active Users**.

   For example,  https://portal.office.com/AdminPortal/Home#/users

3. Select a user account, and then next to **Product licenses**, select **Edit**.

   For example, the following screenshot shows 25 new licenses.

   ![Promotional licenses.](../images/wpa/setup/promo-licenses.png)  

4. On the **Product licenses** page, use the slider to turn on the available licenses.

## Related topics

* [Assign licenses to the population](../setup/Assign-licenses-to-population.md)
* [Environment requirements for advanced insights](/viva/insights/setup/environment-requirements?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)
* [About admin roles](/microsoft-365/admin/add-users/about-admin-roles?view=o365-worldwide&preserve-view=true)
