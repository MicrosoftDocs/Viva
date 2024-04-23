---
title: Set up Program Summary for Viva Glint Employee Lifecycle programs
description: Viva Glint Employee Lifecycle programs measure the employee experience during key moments in the employment journey.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: onboarding, exit surveys
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 02/26/2024
---

# Set up Program Summary for Viva Glint Employee Lifecycle programs

Employee Lifecycle programs measure the employee experience during key moments in the employee journey. They allow organizations to get a holistic understanding of the employee experience from beginning to end via automated survey invitations to new hires and exiting employees.

Employee Lifecycle programs are considered "trigger events" because they use the hire or termination date to automatically be sent.

## Recommended cadence for Employee Lifecycle surveys

Viva Glint recommends this cadence:

- Onboarding surveys for new hires: Within the first week of employment, then again at 30 days _and_ at 90 days
- Exit surveys with voluntary terminations: As soon as possible

## Distribution List setup for Employee Lifecycle surveys

Before configuring an Employee Lifecycle program, visit the [Distribution Lists](https://go.microsoft.com/fwlink/?linkid=2230917) lesson to create new lists based on hire date for Onboarding surveys and on Termination date for Exit surveys.

Follow these steps to create an Employee Lifecycle distribution list:

1. Begin by selecting the **configure symbol** on the admin dashboard and then select **Distribution Lists**.
2. Select **New Distribution List**.
3. Name the new list.
4. Select **Add/Edit Employees**.
5. Select the **Attribute Rules** tile.
6. Select **I want to filter all active employees by these populations.**
7. Select **+ New Population** and find the respective attribute value from your user data, such as "Hire Date" for Onboarding or "Termination Date" for an Exit survey.
8. Set the date range for your distribution list window.
9. Add additional filters if the distribution should only go to a select population.
10. If the survey should include Inactive employees (Exit surveys), be sure the "Include Inactive Employees" box is marked.
11. Select **Save Changes** and align to your respective Employee Life Cycle survey program.

### Tips

**Onboarding**

- Onboarding surveys distribution list date ranges will be relative to Hire Date.
- If the users are to receive the survey 30 days after their hire date, then ensure you set the first value to "after 30 days". For the end value, provide enough of a window so that if someone has their hire date updated late in your user data, they can still be triggered the survey.
- Don't make the window something too small as delayed imports might cause people to miss being included.
- You can't use the same number of days for the beginning and end value in the distribution list, for example: "45 days after to 45 days after." The query would be unable to find any users.

**Exit**

- Exit survey distribution list date ranges are relative to the Termination Date.
- Choose to have Exit Surveys go to a company email and/or a personal email.
- If using **Company Email Address**, we recommend setting the date range from _14 days before the Termination Date to 1 day after._
- If using **Company email + Personal email**, we recommend setting the date range from _14 days before termination date to 30 days after_.

## Populate the Program Summary pages in a survey template

Select **My Surveys** on the admin dashboard. Choose the Onboarding or Exit survey template and then in the _Program Summary_ section, set up the following pages (note the important boxes below which are specific to Employee Lifecycle surveys only):

- [Program Setup](https://go.microsoft.com/fwlink/?linkid=2238328)
  
 > [!IMPORTANT]
 > Employee Lifecycle surveys often target only a few individuals. If that's the case, reducing your confidentiality threshold helps protect their privacy.

- [Distribution](https://go.microsoft.com/fwlink/?linkid=2231414)
- [Questions](https://go.microsoft.com/fwlink/?linkid=2231414)
- [Reports](https://go.microsoft.com/fwlink/?linkid=2230977)
>[!IMPORTANT]
> The Overall Results report is recommended for viewing Employee Lifecycle surveys.
>
> Within the Viva Glint Overall Results report, data can be configured and customized to surface useful insights. Filters are dependent on the attributes sent to Viva Glint in your Employee Attribute File and must meet confidentiality requirements for results to display. [Read about the Overall Results](https://go.microsoft.com/fwlink/?linkid=2231112)report here.

>[!IMPORTANT]
> Understanding [how to interpret the trend graph](https://go.microsoft.com/fwlink/?linkid=2235307) is essential to gaining the best insight from Employee Lifecycle data.

>[!TIP]
> **The default** for Employee Lifecycle reports is a 90-day look-back period.

- [Communication](https://go.microsoft.com/fwlink/?linkid=2231342)
- [Coaching](https://go.microsoft.com/fwlink/?linkid=2231416)

## Additional resource

[Preview and filter Employee Lifecycle programs](https://go.microsoft.com/fwlink/?linkid=2231107)
