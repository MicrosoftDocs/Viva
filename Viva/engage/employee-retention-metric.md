---
title: "Measure employee retention with Viva Engage"
description: "Admins and leaders can track employee retention across the organization with Viva Engage analytics."
ms.reviewer: ethli
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 09/20/2024
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: medium
ms.collection:  
- M365initiative-viva
search.appverid:
- MET150
---

# Employee retention in Viva Engage

The Viva Engage employee retention metric in the [Network Analytics](/viva/engage/analytics#network-analytics) dashboard shows the difference in the 28-day retention rates between employees who use Viva Engage and employees who don't. Since Viva Engage has no access to customer human resources data, we impute that an employee is retained if they have an active Microsoft 365 account and they're actively using that account. Find more detail about these calculations and a numerical example in the following sections.

>[!NOTE]
>Only Engage network admins and corporate communicators have access to the Network Analytics dashboard.

:::image type="content" source="../media/engage/admin/employee-retention-metric.png" alt-text="Screenshot shows visualization of the Employee retention metric." lightbox="../media/engage/admin/employee-retention-metric.png":::

## Employee groupings

We first define the employee population for which to calculate retention. To do this, we classify employees into two groups based on Viva Engage and Microsoft 365 usage behavior for an 84-day (~three month) period.  

*Active on Engage* - Employees who perform an action in Viva Engage. Actions can include viewing, writing, or reacting within any Viva Engage platform.

*Not active on Engage* - Employees who have active accounts but don’t perform an action in Viva Engage.

## Retention proxy

To measure employee retention, we must impute the date an employee left their company. We assume that an employee wasn't retained if their Microsoft 365 account was deleted, or they didn’t use a Microsoft app (such as Outlook, Teams, Word, or OneDrive) in the previous 28 days. Because the retention proxy is also dependent on inactivity for at least 28 days, we must wait an additional 28 days after the retention calculation period to verify inactivity.

## Calculation and comparison 

Finally, for each employee group (*Active on Engage* and *Not Active on Engage*), we measure the share of those who were retained in the following 28 days. In the Network Analytics dashboard, the metric shows the percentage point difference in retention rates between those *Active on Engage* and those *Not Active on Engage*.

#### Example

To further illustrate, let’s go through an example of the retention metric calculation.

|Three stages of data collection|Details|
|------|------|
|**Population collection period (84 days)**<br>Jan 1 - Mar 25|1,000 employees had active Viva Engage accounts. 800 are classified as *Active on Engage* and 200 are *Not Active on Engage*.|
|**Evaluation period (28 days)**<br>Mar 26 - Apr 22|In this period, we count how many of these accounts are deleted or had a final Microsoft 365 action.|
|**Inactivity verification period (28 days)**<br>Apr 23 - May 20|To verify that an action is an employee’s last action, we observe their behavior for the following 28 days to ensure that no additional activity occurred.|

For our example, of all the employees that were counted in the Population Collection Period, 40 *Active on Engage* employees weren't retained and 20 *Not Active on Engage* employees weren't retained.

On 5/21, the difference in retention rates for this cohort is:

 - 95% retention for *Active on Engage* employees (760/800 = 95%)

 - 90% retention for *Not Active on Engage* employees (760/800 = 90%)

In the Network Analytics dashboard, the Retention metric would show +5.0 percentage points (95% - 90%).
