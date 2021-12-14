---

title: Admin tasks for My team in the Viva Insights app
description: Admin tasks for My team in the Microsoft Viva Insights app
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: m365initiative-viva-insights
ms.service: viva
ms.subservice: viva-insights
manager: scott.ruble
audience: Admin

---

# Admin tasks for My team

Before licensed users can access the premium features within the Microsoft Viva Insights apps, you or your admin needs to enable them. The Microsoft Viva Insights SKU includes the following **Assignment options** in the Microsoft Azure Active Directory:

* **Microsoft Viva Insights** - Enables access to premium features within personal and manager insights on the *updated* **My team** page in the Viva Insights in Microsoft Teams app.
* **Microsoft Viva Insights (WpA transition)** – Only relevant for users with licenses that were purchased **_before October 2021_** and are using the Workplace Analytics app. If this is the only app that is enabled, this group or individual will continue to have access to the analyst features in Workplace Analytics but will not have access to premium features for personal and manager insights on the **My team** page in the Viva Insights in Teams app.

>[!Important]
>If your organization purchased Viva Insights licenses starting **in October 2021**, all the regular and premium features are available within your employees’ personal, team lead, manager, and leader insights in the Viva Insights in Teams app. Enabling or disabling the WpA transition app option in Azure Active Directory will not change their access to Viva Insights in Teams.

If your organization purchased Workplace Analytics **before October 2021**, you might have *accidentally* assigned the Microsoft Viva Insights in Teams app to your employees, which enables them to see the premium features in Viva Insights in Teams. To confirm this possibility and to enable or disable access to the app as applicable, do the steps in the following section.

## Set up access to premium features

1. Go to [Azure portal](https://portal.azure.com/) > **Azure Active Directory**.
2. In the left navigation, select **Licenses** > **All products**.
3. Search for and select **Microsoft Viva Insights**.
4. In the left navigation, for groups, select **Licensed groups** or for individual users, select **Licensed users**.
5. At the top, select **+Assign**.
6. In **Users and groups**, select the group or individual to add, which will then show up under **Name**.
7. Select **Assignment options**, and then select **On** to enable or **Off** to disable the following:

   * **Microsoft Viva Insights** – Select to enable the Viva Insights in Teams app.
   * **Microsoft Viva Insights (WpA transition)** – This setting is only applicable to groups or individuals with managers who were assigned licenses that were purchased **before October 2021**.

    ![Azure AD license app options for Viva Insights](../images/wpa/setup/wpa-transition-app-option.png)

8. Select **Review + assign**, and then near the bottom, select **Assign** to apply the changes.
