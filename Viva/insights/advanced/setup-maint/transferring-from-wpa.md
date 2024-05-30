---
ms.date: 05/07/2024
title: Transferring from Workplace Analytics to the advanced insights app
description: Learn about difference in settings between Workplace Analytics and the advanced insights app
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.collection: 
- viva-insights-manager
- viva-insights-leader
ms.localizationpriority: medium 
ms.service: viva-insights
manager: anirudhbajaj
audience: Admin
---


# Transferring from Workplace Analytics to the advanced insights app

>[!Note]
>This document applies to customers who've moved from our legacy platform, Workplace Analytics, to the advanced insights app. 

Welcome to the new advanced insights app! We’re excited to have you on board.

We launched our new app to provide improved insights and data-analysis experiences. The updated platform uses new technology so that our calculations are faster and more comprehensive than before.

As you make your transition from Workplace Analytics, our legacy analyst platform, to our new advanced insights app, here are a few things about setup we want you to know:

* Roles and role assignment look different in the advanced insights app:
    * Some roles remain the same, while we’ve removed others. 
    * A Microsoft 365 admin now uses the Microsoft admin center to assign roles to their team, of the Insights Administrator using Microsoft Entra ID.
* We’ve changed the minimum group size requirement.
* We’ve made a few improvements to privacy settings.
* You'll need to add meeting and subject line exclusions through [Keyword suppression](../admin/keyword-suppression.md). Meeting and subject line exclusions set in Workplace Analytics don't transfer over to the advanced insights app.
* Licensing hasn’t changed for existing licenses. Previously licensed users will have access to the updated platform. However, to [assign new licenses](assign-licenses.md), you'll need to use Microsoft admin center. 

## Roles and role assignments

### Role types

Here’s how roles have changed between Workplace Analytics and the advanced insights app. Notice that the Analyst (Limited Access), Program Manager, and Workplace Analytics admin roles have been retired.

>[!Important]
> The new advanced insights platform recognizes users who were assigned the analyst or administrator roles on Workplace Analytics. However, it’s highly recommended to assign these users current roles through the advanced insights platform. New roles offer better security and privacy management. Learn how to assign new roles in [Assign roles](assign-user-roles.md).
>
>If your organization uses Privileged Identity Management (PIM), you’ll need to assign roles through Microsoft Entra PIM.

|                  |Workplace Analytics |Advanced insights app|
|------------------|---------|--------|
|**Analyst (Limited Access)**|X  | |
|**Insights Administrator**|X  |X|
|**Insights Analyst**|X|X
|**Insights Business Leader**|X|X
|**Program Manager**|X|
|**Workplace Analytics admin** |X|

Insights Administrators still assign roles and upload organizational data into the system, and Insights Analysts still analyze employee data (but do so through the advanced insights app). Insights Business Leaders access organization insights within the Viva Insights app in Teams and on the web.

For more information about roles in the advanced insights app—including which roles can access which features—refer to [Roles in Viva Insights](user-roles.md).

### Role assignment

In Workplace Analytics, Microsoft Entra Application Administrators would assign advanced insights roles to users in the Microsoft Entra admin center. Now, the Microsoft 365 global admin assigns all Viva Insights-related roles within the Microsoft admin center, unless your organization is using PIM.

To learn how to assign roles, refer to [Assign roles](user-roles.md).

## Minimum group size

The minimum group size is the minimum aggregation threshold in Viva Insights—that is, the minimum number of people Viva Insights considers a group. 

In Workplace Analytics, you could set this number to at least 5. In the advanced insights app, you need to set it to at least **five** on the **Privacy settings** page.

This setting affects what managers and leaders see in organization insights. To protect individual privacy, managers and leaders will only see organization insights when the number of active group members meets the minimum group size your Insights admin set. Some groups might have a group size close to the minimum. In these cases, if enough people are away from work and the number of active people dips below the minimum, we won't show organization insights for that week.

## End user opt out

On the **Privacy settings** page, admins can choose whether to turn on the  **End-user opt-out** control. When this control is on, users can choose to opt out of having their metrics—which are always de-identified—appear in person query results.

>[!Note]
>Users can always [opt out](https://support.microsoft.com/topic/ecfd76f9-52ef-4882-9235-be1f59c25967) of personal insights.

## Keyword suppression

Through the **Privacy settings** page, you can exclude sensitive keywords from query results. Learn how to exclude certain keywords in [Keyword suppression](../admin/keyword-suppression.md).
 
## Partitions

We’re working on improving partitions from the Workplace Analytics experience. This feature isn’t available quite yet, but it will be soon. To find out when we’ve released this feature, stay tuned on our [Insights Community](https://techcommunity.microsoft.com/t5/viva-insights/ct-p/VivaInsights).

## System defaults

In Workplace Analytics, admins could set the following defaults through the **System defaults** page:

* Time zone
* Working days
* Working hours
* Hourly rate
* Reclassification of external domains

In the updated advanced insights app, admins don’t need to adjust these settings manually, because Viva Insights pulls this information from different sources. The exception is reclassification of external domains—this feature isn’t available in the updated platform. 

|Default field| Source|
|-------------|---------|
Time zone| User Outlook settings
Working days| User Outlook settings
Working hours| User Outlook settings
Hourly rate| Organizational data file, if you choose to include it
Reclassification of external domains| N/A – this feature isn’t available in the advanced insights app yet, but it will soon become part of **Privacy settings**.

## Metric rules

In Workplace Analytics, you could set meeting exclusions and attendee exclusions through **Analysis settings**. In the advanced insights app, analysts can create these exclusions through [Metric rules](../analyst/metric-rules.md), and set one rule as default to apply to all future queries. Any exclusions set in Workplace Analytics don't transfer over to the advanced insights app.
