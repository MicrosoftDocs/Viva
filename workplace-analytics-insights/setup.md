---
ROBOTS: NOINDEX,NOFOLLOW
title: Set up Workplace Analytics insights
description: Steps to set up Workplace Analytics insights
author: madehmer
ms.author: v-mideh
ms.topic: conceptual
localization_priority: none
ms.prod: wpa

---
# Set up insights

*This experience is only available through private preview at this time.*

Before people in your organization can view and use Workplace Analytics insights, your Microsoft 365 global admin needs to do the following for them:

* [Activate licenses](#activate-licenses)
* [Assign licenses](#assign-licenses)
* [Assign roles](assign-roles.md)

This new release is currently limited to Microsoft or Office 365 E5 or E3 plan subscribers through their Microsoft service representative.

You can request access and get more information at [Microsoft Workplace Analytics](https://www.microsoft.com/microsoft-365/business/workplace-analytics). Select **Contact us** and complete the form to request access and get more information about Workplace Analytics insights.

## Activate licenses

1. Depending on which browser you are using, on the Windows taskbar or Start menu, right-click the browser application and select **Start InPrivate Browsing**, **New InPrivate window**, **New incognito window**, or **New private window**.
2. Copy the **activation code link** that Microsoft sent you for Workplace Analytics insights, paste it into the URL section of the private or incognito browser window, and then press **Enter** to open the link.

   ![Activation code link](./images/sign-in.png)

3. When prompted, enter your email address.
4. Sign in with your Microsoft or Office 365 global admin credentials, and then select **Next**.
5. In **Check out** > **confirm you order** > **Microsoft Workplace Analytics insights trial**, select **Try now**.
6. When prompted in **order receipt**, select **Continue**.

## Assign licenses

You must be able to sign in as a global Microsoft 365 admin to use the Microsoft admin center to [assign licenses to one or more individual users](#to-assign-licenses-to-individual-users) who subscribe to Microsoft or Office 365 E5 or E3 plan whose [geo location is North America](https://docs.microsoft.com/microsoft-365/enterprise/microsoft-365-multi-geo#microsoft-365-multi-geo-availability).

Alternatively, you can sign in as a global admin to Azure Active Directory to [assign licenses to one or more security groups](#to-assign-licenses-to-security-groups) who subscribe to a Microsoft or Office 365 E5 or E3 plan.

### To assign licenses to individual users

1. In the **Microsoft admin center**, select **Active users**, and then do one of the following to assign licenses to one user or for multiple users at the same time.

   **For one user**:
   1. In **Active users**, select the user from the list.
   2. Select **Licenses and Apps**.
   3. Select the check box for **Microsoft Workplace Analytics Insights**.
   4. Select **Save changes**, as shown in the following graphic.

   ![Assign one user a license](./images/assign-one-license.png)

   **For multiple users**:
   1. In **Active users**, select the checkbox next to the users you want to assign licenses.
   2. Select the **Ellipsis** (**...**) icon next to **Reset password**, and then select **Manage product licenses**.
   3. Select **Assign more**, and then select the check box for **Microsoft Workplace Analytics Insights**.
   4. Select **Save changes**.

   ![Assign multiple users licenses](./images/assign-multiple-licenses.png)

2. These licenses are assigned right away to the selected users.

### To assign licenses to security groups

1. In **Microsoft Azure Active Directory**, select **Licenses** under **Manage**.
2. In **Overview**, select **All products**, and then select the check box for **Microsoft Workplace Analytics Insights**.

   ![Assign licenses in Azure Active Directory](./images/assign-licenses-add.png)

3. Select **Assign**, and then select **Users and groups** to open the right pane.
4. Search for one or more group names, select each group from the list to add it to the **Selected items** list, and then choose **Select**.

   ![Add one or more groups for licensing](./images/add-group-license.png)

5. Select **Assignment options** to open the right pane, confirm that both **Microsoft Workplace Analytics Insights** are set **On**, and then select **OK**.

   ![Keep both options set to On](./images/keep-options-on.png)

6. It can take a few minutes up to 24 hours for the license assignments to update to the server, which is based on your specific server settings.

> [!Note]
> If you are assigning licenses to a group that has more people than you have licenses for, the tool will assign users as listed in the group up to the number of available licenses, and then you'll see an error message about how many in the group have and do not have licenses.

## Access to Insights

After assigning licenses, the data for insights might take up to three days to process and become available. After [assigning roles](assign-roles.md) and allowing for data processing, send your organization's leaders the link to [Insights](https://productivityinsights.office.com) to open and use them. Also, refer them to [Insights introduction](./intro.md) to learn more about how to use them.
