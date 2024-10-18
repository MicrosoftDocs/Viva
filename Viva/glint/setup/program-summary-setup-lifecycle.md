---
title: Use and set up a Viva Glint Employee Lifecycle program
description: Viva Glint Employee Lifecycle programs measure the employee experience during key moments in the employment journey.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: onboarding, exit surveys, cross-program intelligence
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 10/17/2024
---

# Use and set up a Viva Glint Employee Lifecycle program

Lifecycle surveys are a comprehensive approach to understanding the employee experience throughout their tenure at an organization, from onboarding to exit. They allow organizations to get a holistic understanding of the employee experience from beginning to end. They are considered "trigger events" because they use the hire or termination date to automatically send. The insights from these surveys are invaluable for organizations to address issues that may be causing turnover and to improve the overall employee experience. 

**Onboarding Surveys** are crucial for gauging new hires’ early experiences and ensuring they have the resources and support needed to succeed. They typically occur within the first few weeks of employment and may continue at intervals to track the new employee’s integration into the company. These surveys can cover aspects like the effectiveness of your orientation process, clarity of job expectations, and the supportiveness of the environment. 

**Exit Surveys** see to understand the reason that an employee voluntarily leaves your organization. They uncover the reasons behind their departure, which could range from career advancement opportunities elsewhere to dissatisfaction with the work environment. 

## Cross-program intelligence

The pimpact of Lifecycle surveys is apparent when you introduce the concept of cross-program intelligence.  Cross-program intelligence in Viva Glint allows for a comprehensive analysis of employee feedback across various programs such as Engagement, Onboarding, and Exit. This holistic approach enables organizations to identify patterns and correlations that might not be apparent when looking at individual programs in isolation. 
 
Interconnected analysis provides value by offering insights across the entire employee lifecycle. It helps HR and senior leaders understand the full impact of their programs and initiatives on employee satisfaction and retention. By examining feedback across multiple programs, organizations can pinpoint critical intervention points and make data-driven decisions to enhance the employee experience.  

## Recommended cadence for Employee Lifecycle surveys

Viva Glint recommends this cadence:

- Onboarding surveys for new hires: within the first week of employment, then again at 30 days *and* at 90 days
- Exit surveys with voluntary terminations: as soon as possible

## Distribution List setup

Before configuring an Employee Lifecycle program, visit the [Distribution Lists](/viva/glint/setup/set-up-distribution-lists) lesson to create new lists based on hire date for Onboarding surveys and on Termination date for Exit surveys.

**Steps to create an Employee Lifecycle distribution list:**

1. Select the **Configuration** symbol on the admin dashboard and then select **Distribution Lists**.
2. Select **New Distribution List**.
3. Name your new list.
4. Select **Add/Edit Employees**.
5. Select the **Attribute Rules** tile.
6. Select **I want to filter all active employees by these populations.**
7. Select **+ New Population** and find the respective attribute value from your user data, such as "Hire Date" for Onboarding or "Termination Date" for an Exit survey.
8. Set the date range for your Distribution List window.
9. Add filters if the distribution should only go to a select population.
10. If the survey should include Inactive employees (Exit surveys), be sure the **Include Inactive Employees** box is marked.
11. Select **Save Changes**.

### Tips for Employee Lifecycle programs

**Onboarding**

- Onboarding surveys Distribution List date ranges are relative to Hire Date.
- If the users should receive the survey 30 days after their hire date, ensure you set the first value to **after 30 days.** For the end value, provide enough of a window so that if someone has their hire date updated late in your user data, they still trigger the survey.
- Don't make the survey taker window too small. Delayed imports might cause people to miss being included.
- You can't use the same number of days for the beginning and end value in the Distribution List. For example: "45 days after to 45 days after" - the query would be unable to find any users.

**Exit**

- Exit survey Distribution List date ranges are relative to the Termination Date.
- Choose to have Exit Surveys go to a company email and/or a personal email.
- If using **Company Email Address**, we recommend setting the date range from *14 days before the Termination Date to 1 day after.*
- If using **Company email + Personal email**, we recommend setting the date range from *14 days before termination date to 30 days after.*

## Program Summary setup for Employee Lifecycle survey templates

Select **My Surveys** on the admin dashboard. Choose the **Onboarding** or **Exit** survey template and then in the **Program Summary** section, set up the following pages:

- [Program Setup](/viva/glint/setup/program-set-up)
  
 > [!IMPORTANT]
 > Employee Lifecycle surveys often target only a few individuals. If that's the case, reducing your confidentiality threshold helps protect their privacy.

- [Distribution](/viva/glint/setup/set-up-distribution-lists)
- [Questions](/viva/glint/setup/questions-setup)
- [Reporting](/viva/glint/setup/reporting-setup)

>[!IMPORTANT]
> The Overall Results report is recommended for viewing Employee Lifecycle surveys.
>
> Within this report, data can be set up and customized to surface useful insights. Filters are dependent on the attributes sent to Glint in your Employee Attribute File and must meet confidentiality requirements. [Read about the Overall Results report](/viva/glint/reports/overall-results).

>[!IMPORTANT]
> Understanding [how to interpret the trend graph](/viva/glint/reports/trend-graph-lifecycle-survey) is essential to gaining the best insights from Employee Lifecycle data.

>[!TIP]
> **The default** for Employee Lifecycle reports is a 90-day look-back period.

- [Communication](/viva/glint/setup/program-summary-communications)
- [Coaching](/viva/glint/setup/program-summary-coaching)

## Related resource

[Preview and filter Employee Lifecycle programs](/viva/glint/setup/preview-filter-lifecycle-programs)
