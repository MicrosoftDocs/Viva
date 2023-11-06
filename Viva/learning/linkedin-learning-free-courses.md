---
title: LinkedIn Learning
ms.author: bhaswatic
author: bhaswatic
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 11/06/2023
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - Tier1
localization_priority: high
description: See what LinkedIn Learning courses are available on Viva Learning without a premium LinkedIn subscription.
---

# LinkedIn Learning

LinkedIn Learning is enabled as a content source without any further setup in Viva Learning.
Learn more about [content sources in Viva Learning](content-sources-365-admin-center.md).

The library of [global skilling initiative (GSI) courses](https://opportunity.linkedin.com/skills-for-in-demand-jobs) from LinkedIn Learning is available in Viva Learning without requiring a LinkedIn Learning premium subscription. 

You can view the free LinkedIn courses in Viva by putting the search query `premium:false` and choosing **LinkedIn Learning** in the provider filter.

You need a LinkedIn Learning subscription for learners in your organization to access [premium LinkedIn content](https://learning.linkedin.com).

## LinkedIn Learning seamless login


Seamless login enables users to access premium LinkedIn content without repeatedly entering their credentials. 
To enable this, you can set the following configurations:

1. Go to the **Admin** tab in Viva Learning and select **Manage providers**.

2. Turn on **Seamless Login** for LinkedIn in the Manage providers pane.


![The manage providers pane with the seamless login enabled for LinkedIn Learning](../media/learning/linkedin-learning-seamless-1-enable-toggle.png)

![Seamless login menu with an outline of the following steps.](../media/learning/linkedin-learning-seamless-2.png)

3. Provide **admin consent**.

![Permission requested window that wants to sign into the LinkedIn Learning Viva Connector](../media/learning/linkedin-learning-seamless-3-permission-requested.png)

  > [!IMPORTANT]
  > The consent is provided only by specific roles in the organization. Review who can [grant tenant-wide admin consent](learn.microsoft.com/en-us/entra/identity/enterprise-apps/grant-admin-consent?pivots=portal#prerequisites) in Enterprise applications.

4. Get tenant **Azure active directory ID**: This ID is required in the following steps. Note this ID before moving to the next step. Find our how to get your [active directory ID](https://learn.microsoft.com/en-us/partner-center/find-ids-and-domain-names).

5. Input the **tenant ID** in the LinkedIn configuration page by selecting the link in the previous step.

![LinkedIn configuration page where you copy the link to Viva Learning enter your Viva Tenant](../media/learning/linkedin-learning-seamless-4-linkedin-config.png)

6. Copy the **login web URL** from the LinkedIn configuration page and paste it in Viva Learning.

7. Select **Submit** after entering the tenant ID and copying the link.

![The seamless login screen with the linked copied from LinkedIn](../media/learning/linkedin-learning-seamless-5-validate.png)

8. Select **Validate** to confirm the settings.

9. Use your organization's LinkedIn Learning credentials to log in and go through the validation process.  

10. Select **Save** to save the configurations.


## Resources

- View the [current learning offerings](https://opportunity.linkedin.com/skills-for-in-demand-jobs) on LinkedIn.

- To see if courses are available in your language, visit the list of [supported LinkedIn Learning languages](https://www.linkedin.com/help/learning/answer/a702837).

