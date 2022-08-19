---
title: Hybrid workforce experience solution
description: Learn how to create an OnsiteDays attribute to use in the Hybrid workforce experience Power BI template
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
search.appverid:
- MET150
ms.service: viva 
ms.subservice: viva-insights
ms.collection: 
- M365-analytics
- viva-insights
manager: anirudhbajaj
audience: Admin
---

# Hybrid workforce experience report Onsite days solution

What you'll learn:

> [!div class="checklist"]
>
> * How to create an **OnsiteDays** attribute, which is required to use the Hybrid workforce experience Power BI template
> * What the Hybrid workforce experience report from Microsoft Viva Insights does and how it can help your organization as it transitions to hybrid working modes

## Background

### A new hybrid workforce

Before the COVID-19 pandemic, the business world mostly worked onsite, and workplace policies and practices supported employees as they worked in the office. Once the pandemic hit, however, organizations had to quickly shift to remote and hybrid modes of working. More than two years since COVID began, many things are starting to return to the way they were before—both in our everyday lives and in business. Hybrid and remote working, though? That’s here to stay.

So, what should businesses do to prepare for a more permanent hybrid employee workforce? First, before starting any planning and strategizing, really understand how hybrid work affects their employees. That’s where the Hybrid employee experience report from Microsoft Viva Insights comes in.

### Report overview

Using data-driven insights, the Hybrid employee experience report helps leaders quickly sum up how hybrid work affects employees in different work modes (onsite, remote, or hybrid) in the following six ways:

* **Collaboration Habits**: How does hybrid work impact meeting engagement and collaboration patterns? What does meeting engagement look like for employees in different work modes?
* **Behavioral Trends**: How are behaviors evolving over time in different work modes?
* **New Hire Onboarding**: Are new hires getting the support they need from their managers?
* **Manager Connection**: How does employee work mode impact access to 1:1 time with their manager?
* **Work-Life Balance & Flex Work**: How does hybrid work impact employees’ ability to unplug? Are there specific work modes working longer hours, or embracing more flexible schedules?
* **Connectivity and Belonging**: Are people connecting in ways that boost their sense of belonging?

Then, using information from these six categories, the report provides guidance on **Why it matters**, as well as actionable insights and recommendations about how improve the overall hybrid employee experience.

### Report prerequisites

In addition to having the latest version of Power BI Desktop installed, you’ll need to upload three attributes as part of your HR data before you can start using the Hybrid workforce experience report:

* **OnsiteDays** – The number of days per week an employee works from the company’s main worksite. This attribute can be based on badge data, wireless network data, or other sources—for example, tags in the HR system showing the number of days an employee plans to work onsite. This solution helps you create an OnsiteDays attribute.
* **SupervisorIndicator** – Indicates whether someone is a manager.
* **HireDate** – The day someone was hired. This attribute enables the New hire onboarding insights.

## Solution – create an OnsiteDays attribute and use the report

As mentioned earlier, this solution helps you create an OnsiteDays attribute. This process includes three steps, which we’ll describe in detail:

1. **Prepare two source files:** <!--link to article-->
    * Event log from Azure Active Directory (AD)
    * List of office IP addresses
2. **Transform data:** Use an Excel template to determine **Onsite days**. <!--link to article-->
3. **Use the Hybrid workforce experience report:** <!--link to article--> Use Viva Insights Hybrid workforce experience template to understand your company’s hybrid work patterns and how hybrid work impacts employees differently.

> [!div class="nextstepaction"]
> [Next up: Prepare source files](hybrid-workforce-experience-intro.md)