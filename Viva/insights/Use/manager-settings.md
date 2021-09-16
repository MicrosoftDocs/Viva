---

title: Leader and manager settings in Viva Insights
description: Describes the leader and manager settings in Microsoft Viva Insights and how administrators can set them up and edit them for your organization
author: madehmer
ms.author: v-mideh
ms.topic: article
ms.localizationpriority: medium 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---


# Leader and manager settings

As the Microsoft Viva Insights admin, you can set up and edit **Leader & manager settings** to allow all measured people managers or a specified group of managers access to aggregate collaboration insights about their team and the ability to start plans for their team in Viva Insights. Only managers whose team meets or exceeds the **Minimum team size** setting can access Viva Insights. The size of the team counts the manager and all the employees who directly or indirectly report to that manager within the organization's reporting hierarchy.

The following are based on the latest organizational (HR) data that's been successfully uploaded and processed in Viva Insights:

* **Measured managers** - Total number of people managers who are assigned licenses in Viva Insights.
* **Managers enabled** - Total number of people managers who meet the minimum team size and have access to their team's insights and plans in Viva Insights.

**Owner** – Only Viva InsightsAdmins have full access to this page. For details, see [Assign roles to Viva Insights admins and analysts](../setup/assign-roles-to-wpa-admins.md).

![Manager settings.](../images/wpa/use/manager-settings.png)

* **Minimum team size** - You can set the minimum size of a team that a manager is allowed to view insights about and start plans for. The minimum size allowed is 10. This section also shows you how many measured managers currently have teams that are equal to or more than the minimum setting.
* **Insights and plans** - You can select to allow all licensed managers access to aggregated collaboration insights about their teams and to start and manage plans for their teams. Or you can upload a .csv file that lists the email addresses for the managers you want to give access to their team's insights and plans in Viva Insights.
<!-- REMOVING (12/4/2020) FOR NOW. REINSTATE PERHAPS IN JANUARY 2021. 
  * If you turn **Insights and plans** on, your organizational hierarchy file will also be used to power personal insights for managers in the [Insights add-in](../personal/use/add-in.md), the [MyAnalytics dashboard](../personal/use/dashboard-2.md), and other MyAnalytics surfaces. This file will complement hierarchy information from Azure AD. If a manager in your organization has team members who are listed in both Azure AD and Viva Insights, the system will default to using the Viva Insights data; otherwise it will use whichever source is available.
   
     Personal insights help managers improve their personal impact on and relationships with direct reports, and are powered exclusively by information from the manager's own Outlook mailbox. Learn more about personal insights for people managers in [Assistance for people managers](../personal/overview/privacy-guide.md#assistance-for-people-managers). -->

## Configure leader and manager settings

Only Viva Insights admins can access **Leader & manager settings**.

* Before **leaders** can access insights about their organization in the Viva Insights app in Teams, their organization's group size must meet or exceed the **Tenant minimum group size** setting.
* Before managers can access insights about their team in the Viva Insights app in Teams, they must be assigned a Viva Insights license and have a team that meets or exceeds the **Minimum team size** setting.

1. As the admin, go to **Leader & manager settings** > **Privacy** to confirm or change the setting for the **Tenant minimum group size**, which applies only to the Outcomes that leaders and managers in your organization can see in the Viva Insights app in Teams.
2. In **Manager settings**, select to change the switch **On** to allow managers with the minimum team size access to their team data in Viva Insights.
3. Select one of the following:

   * **All managers** - Allows all measured managers access.
   * **Select managers** (upload .csv) - Enables you to give specific managers access. You then need to:

      a. Create a .csv file that lists the email addresses for the select managers.

      b. Select **Upload .csv** to upload this list.

4. If you're allowing all managers access, continue to **Step 4**. If setting up access for select managers, select **Download currently enabled manual upload manager list .csv** to confirm which managers now have access. If an error occurs, such as an invalid email or an unlicensed manager, the .csv file will show the error for that manager.
5. In **Minimum team size**, you can change the minimum to a number more than 10 (which is the lowest setting allowed), which limits access to only those managers who have teams equal to or more than that number.
6. Select **Save**.

>[!Note]
>Changes to these settings will apply after one hour.

## Related topics

* [Plans](../Tutorials/solutionsv2-intro.md)
* [Settings](settings.md)
