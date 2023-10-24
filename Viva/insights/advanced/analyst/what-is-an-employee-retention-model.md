---
ms.date: 11/1/2023
title: What is an employee retention model?
description: Provides an overview of an employee retention model including terminology like attrition and turnover model.
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: abelubetk
audience: Admin
---

# What is an Employee Retention Model?

Before diving into the definitions of what an employee retention model is, it's helpful to clarify some of the terminology that is associated with the subject, such as _retention_, _attrition_, _churn_, and _turnover_.

## What is the difference between an employee retention, attrition (churn), or a turnover model?

Employee retention, attrition, and turnover are all HR metrics that measure employee movement within an organization:

- Employee retention refers to the ability of an organization to keep its employees
- Employee attrition refers to the natural reduction of the workforce through reasons such as retirement, sickness, death, or resignations
- Employee turnover measures all terminations, which includes positions that are refilled. For the purpose of comparing employee attrition and retention, we will use attrition as a synonym for turnover

The concepts are closely related. In this playbook, we are going to focus on a specific type of employee attrition: voluntary. But the general principles and approach can be adapted for the similar business objectives above.

## Types of attrition

There are two main types of attrition: **involuntary** and **voluntary**. Involuntary attrition refers to the loss of employees due to reasons beyond their control, such as layoffs, restructuring, or termination by the company. Attrition due to retirement, sickness, and death also normally fall under this category. Voluntary attrition refers to the loss of employees who leave the company voluntarily, often due to reasons such as better job opportunities, dissatisfaction with their current role or work environment, or personal reasons.

In this playbook, we will focus on **voluntary churn**, which is around employees leaving an organization due to voluntary reasons that an organization can practically intervene on. For instance, such voluntary reasons could be:

- Dissatisfaction with wellbeing
- Dissatisfaction with culture or manager style
- Dissatisfaction with pay or package
- Better opportunity elsewhere

An exit survey will usually provide a classification for whether an employee has churned due to voluntary reasons. In Viva Insights, this can be uploaded as an organizational variable. This can then be used as an outcome variable to determine whether someone has churned or not.

## Modelling attrition

To model attrition, one of the approaches would be to train a statistical model that can be used to measure the likelihood of voluntary attrition, and the importance of the factors that contribute to it.

A statistical model will be composed of an **outcome variable** and a set of **predictor variables** (sometimes referred to as dependent variable and independent variables).

For an employee attrition model, the outcome variable is typically a binary variable on whether an employee has voluntarily attritioned or not:

| HasChurned |
| ---------- |
| TRUE |
| FALSE |

Although this might alter the nature of the model, the following outcome variables may also be used:

- Employee engagement/satisfaction score, or Employer NPS
- Employee sentiment on staying, e.g. _Likelihood to stay in the organization in the next 6 months_
- Tenure

The next chapter provides details on what predictor variables, including data from Viva Insights and Glint, can be added into the model.
