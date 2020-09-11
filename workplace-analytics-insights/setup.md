---

ROBOTS: NOINDEX,NOFOLLOW
title: Set up Workplace Analytics insights
description: Steps to set up Workplace Analytics insights
author: madehmer
ms.author: v-mideh
ms.topic: conceptual
localization_priority: normal 
ms.prod: wpa

---
# Set up Workplace Analytics insights

Your Microsoft 365 global admin can activate and assign licenses to people in your organization to use Workplace Analytics insights.

This new release is currently limited to Microsoft or Office 365 E5 plan subscribers through your Microsoft service representative.

You can request access and get more information at [Microsoft Workplace Analytics](https://www.microsoft.com/microsoft-365/business/workplace-analytics). Select **Contact us** and complete the form to request access and get more information about Workplace Analytics insights.

## Activate licenses

1. Depending on which browser you are using, on the Windows taskbar or Start menu, right-click the browser application and select **Start InPrivate Browsing**, **New InPrivate window**, **New incognito window**, or **New private window**.
2. Copy the **activation code link** that Microsoft sent you for Workplace Analytics insights, paste it into the URL section of the private or incognito browser window, and then press **Enter** to open the link.

   ![Activation code link](./Images/sign-in.png)

3. In the **Welcome** screen, select **Sign in**.
4. Enter your Microsoft or Office 365 global admin credentials, and then select **Next**.
5. In **Where will you be using this**, complete the requested information, and then select **Next**.
6. In **users**, enter the number of active licenses that correspond with the **activation URL for Microsoft Workplace Analytics insights**, and then select **Next**.

   ![Enter number of users](./Images/number-users.png)

7. In **How do you want to pay**, enter applicable information for your organizational account, and then select **Place order**.
8. When prompted in the **Confirmation** page, select **assign users to your new subscription**.

   ![Successful activation](./Images/order-success.png)

## Assign licenses

You must be able to sign in as a global Microsoft 365 admin to use the Microsoft admin center to assign licenses to one or more individual users who subscribe to Microsoft or Office 365 E5 plan.

Alternatively, you can sign in as a global admin to Azure Active Directory to assign licenses for Workplace Analytics insights to one or more security groups who subscribe to a Microsoft or Office 365 E5 plan.

### To assign licenses to individual users

1. In the **Microsoft admin center**, select **Active users**, and then do one of the following to assign licenses to one user or for multiple users at the same time.

   **For one user**:
   a. In **Active users**, select the user from the list.
   b. Select **Licenses and Apps**.
   c. Select the check box for **Microsoft Workplace Analytics Insights**.
   d. Select **Save changes**, as shown in the following graphic.

   ![Assign one user a license](./Images/assign-one-license.png)

   **For multiple users**:
   a. In **Active users**, select the checkbox next to the users you want to assign licenses.
   b. Select the **ellipsis** (**...**) icon next to **Reset password**, and then select **Manage product licenses**.
   c. Select **Assign more**, and then select the check box for **Microsoft Workplace Analytics Insights**.
   d. Select **Save changes**.

   ![Assign multiple users licenses](./Images/assign-multiple-licenses.png)

2. These licenses are assigned right away to the selected users.

### To assign licenses to security groups in Azure

1. In **Microsoft Azure Active Directory**, select **Licenses** under **Manage**.
2. In **Overview**, select **All products**, and then select the check box for **Microsoft Workplace Analytics Insights**.

   ![Assign licenses in Azure Active Directory](../Images/assign-licenses-add.png)

3. Select **Assign**, and then select **Users and groups** to open the right pane.
4. Search for one or more group names, select each group from the list to add it to the **Selected items** list, and then choose **Select**.

   ![Add one or more groups for licensing](./Images/add-group-license.png)

5. Select **Assignment options** to open the right pane, confirm that both **Microsoft Workplace Analytics Insights** are set **On**, and then select **OK**.

   ![Keep both options set to On](./Images/keep-options-on.png)

6. It can take a few minutes up to 24 hours for the license assignments to update to the server, which is based on your specific server settings.

> [!Note]
> If you are assigning licenses to a group that has more people than you have licenses for, the tool will assign users as listed in the group up to the number of available licenses, and then you'll see an error message about how many in the group have licenses.

After assigning users licenses, you can send them a [Workplace Analytics insights link](https://workplaceanalytics.office.com/) to open and use it. Refer users to [Workplace Analytics insights introduction](./intro.md) to learn more about how to use it.
