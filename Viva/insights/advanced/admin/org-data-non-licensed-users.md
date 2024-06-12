---
ROBOTS: NOINDEX, NOFOLLOW
ms.date: 06/12/2024
title: Show organizational data for nonlicensed users
description: Explains how admins can change settings in Viva Insights to show organizational data for nonlicensed users in meeting query results.
author: zachminers
ms.author: v-zachminers
ms.topic: concept-article
ms.localizationpriority: medium
ms.collection: 
- viva-insights-advanced
- essentials-manage
ms.service: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Show organizational data for nonlicensed users

When creating a meeting query, Viva Insights analysts can select meeting organizer attributes to appear in the query output. These attributes come from the organizational data you’ve uploaded to Viva Insights. By default, Viva Insights doesn't show organizational data for nonlicensed meeting organizers in meeting queries, but you can choose to do so.

### How to show organizational data for nonlicensed users 

1. Go to the **Privacy settings** page in the advanced insights app.
2. Select the box under **Show organizational data for non-licensed users**.
3. Select **Save changes**.

>[!Important]
>This option only applies to queries that analysts run in the future. When you change this setting, it won't apply to queries that analysts have already run.

### How it works

If you choose to show organizational data for nonlicensed users, meeting query results show meeting organizer attributes for nonlicensed users if their data was included in the organizational data upload. In the following table, the meeting in the second row was organized by a user whose data was included in the organizational data upload but who doesn't have a Viva Insights license.

:::image type="content" source="../images/non-licensed-table-01.png" alt-text="Screenshot that shows a user whose data was included in the org data upload but who doesn't have a Viva Insights license.":::

By default, Viva Insights doesn't show organizational data for nonlicensed meeting organizers. The following table shows what the output of the same query looks like by default.

:::image type="content" source="../images/non-licensed-table-02.png" alt-text="Screenshot that shows what the output of a query would look like for a nonlicensed user.":::

Regardless of whether you decide to show organizational data for nonlicensed employees or not:

* The meeting organizer’s PersonId is never shown in meeting query results.
* Organizational data of employees who opted out of Viva Insights is never exposed in meeting query results.
* Organizational data of employees associated with domains you’ve suppressed is never exposed in meeting query results.

**Show organizational data for non-licensed users** doesn’t affect other query types, such as person or cross-collaboration queries, and doesn’t affect metric calculations.