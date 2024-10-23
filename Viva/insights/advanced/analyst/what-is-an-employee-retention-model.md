---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 10/25/2024
title: What is an employee retention model?
description: Provides an overview of an employee retention model including terminology like attrition and turnover model.
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva-insights
search.appverid: 
- MET150 
manager: abelubetk
audience: Admin
---

# What is an Employee Retention Model?

Let's start with defining the relevant terms: *retention*, *attrition*, *churn*, and *turnover*.

These are HR metrics that measure employee movement within an organization:

- Employee retention is the ability of an organization to keep its employees.
- Employee attrition or churn is the natural reduction of the workforce through reasons like retirement, sickness, death, or resignations.
- Employee turnover measures all terminations, which includes positions that are refilled. Attrition can be considered a subset of turnover, since turnover includes all types of employee departures and replacements.

The concepts are closely related. In this playbook, we'll focus on a specific subset of employee attrition: voluntary. But the general principles and approach can be used for similar scenarios.

## Types of attrition

There are two main types of attrition: **involuntary** and **voluntary**. Involuntary attrition refers to the loss of employees due to reasons beyond their control, such as layoffs, restructuring, or termination by the company. Attrition due to retirement, sickness, and death also normally fall under this category.

Voluntary attrition refers to the loss of employees who leave the company voluntarily, due to reasons such as better job opportunities, dissatisfaction with their current role, pay, work environment, or manager, or personal reasons.

In this playbook, we'll focus on **voluntary churn**, which an organization has greater control over to reduce, through interventions such as improving working conditions, enabling greater flexibility, and increasing managerial support.

An exit survey usually identifies an employee who has churned for voluntary reasons. In Viva Insights, this can be uploaded as an organizational attribute. This can then be used as an outcome variable to determine whether someone has churned.

## How to model attrition

To model attrition, one approach would be to train a statistical model to measure the likelihood of voluntary attrition, and the importance of the factors that contribute to it.

A statistical model includes an **outcome variable** and a set of **predictor variables** (sometimes referred to as *dependent variable* and *independent variables*).

For an employee attrition model, the outcome variable is typically a binary variable on whether an employee experienced voluntary attrition:

| HasChurned |
| ---------- |
| TRUE |
| FALSE |

Although this will change the characteristics and the interpretation of the model, the following variables can also be used as the outcome variable:

- Employee engagement/satisfaction score, or Employer NPS
- Employee attitude toward staying. For example, *Likelihood to stay in the organization in the next 6 months*
- Tenure

The next chapter provides details on what predictor variables, including data from Viva Insights and Glint, can be added to the model.

> [!div class="nextstepaction"]
> [Learn the variables](employee-retention-metrics-queries.md)
