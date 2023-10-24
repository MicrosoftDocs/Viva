---
ms.date: 11/1/2023
title: Why build an employee retention model?
description: Introduction to the playbook on how to design, train, and interpret a predictive employee retention model using data from Viva Insights and Glint.
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

# Why build an Employee Retention Model?

## Introduction

This playbook provides an introduction on how to design, train, and interpret a predictive employee retention model using data from Viva Insights and Glint. This playbook includes: the principles of employee retention; the business scenarios of employee retention; and the code examples in R and Python.

Through this playbook, you can learn:

- The principles and the use cases of an employee retention model
- To combine and validate data from Viva Insights, Glint, and other sources such as employee attrition data
- To train and evaluate a random forest model that can predict employee attrition using the selected features
- To interpret and communicate the results and the insights from the model

In essence, we propose a playbook for organizations to create a bespoke machine learning model that can predict employee attrition. The prediction is intended to help organizations develop a retention model and strategy that best suits them, being mindful of constraints such as industry, organizational structure, and applicable conditions.

## Why should I care about creating an employee retention model?

The most valuable asset of a company is its people, especially when they are outstanding in what they do. Considering that hiring itself is costly and many hiring decisions tend to be wrong,[^1] [^2] retaining great employees becomes significant to business success.  

Employee attrition is the voluntary or involuntary loss of employees from an organization.[^3] It can have negative impacts on the organization's performance, productivity, morale, and profit.[^4] Therefore, it's important for organizations to understand the factors that influence employee attrition and to identify groups with higher attrition risk.

Losing an employee is costly because employees are considered appreciating assets, meaning, all things being equal, they produce more value for the company over time. How costly? Employers could spend between 30% to 400% of the employee’s annual salary to replace an employee,[^5] depending on the former employee’s level of specialization. Considering that one in three hires will leave the company within two years, this quickly adds up.[^6] Therefore, predicting employee attrition is important and more-so, having a model to help organizations determine strategies for increased employee retention is almost mandatory.  

Machine learning can be used to analyze employee data and to build models that can predict voluntary employee attrition. Such models can help organizations to take proactive measures to retain their valuable employees and to reduce the costs and consequences of employee turnover.  

Our proposed model will leverage historical employee data, performance metrics, engagement surveys, and other relevant indicators to proactively identify groups with higher risks of attrition to aid in creating a more stable, engaged, and productive workforce.

[^1]: <https://www.psychometrics.com/true-cost-employee-turnover/>
[^2]: <https://hbr.org/2019/05/your-approach-to-hiring-is-all-wrong>
[^3]: <https://www.gartner.com/en/human-resources/glossary/attrition>
[^4]: <https://builtin.com/recruiting/cost-of-turnover>
[^5]: <https://www.simplybenefits.ca/blog/employee-retention-what-is-the-true-cost-of-losing-an-employee>
[^6]: <https://www.forbes.com/sites/johnhall/2019/05/09/the-cost-of-turnover-can-kill-your-business-and-make-things-less-fun/>

<ins>References</ins>

1: <https://www.psychometrics.com/true-cost-employee-turnover>

2: <https://hbr.org/2019/05/your-approach-to-hiring-is-all-wrong>

3: <https://www.gartner.com/en/human-resources/glossary/attrition>

4: <https://builtin.com/recruiting/cost-of-turnover>

5: <https://www.simplybenefits.ca/blog/employee-retention-what-is-the-true-cost-of-losing-an-employee>

6: <https://www.forbes.com/sites/johnhall/2019/05/09/the-cost-of-turnover-can-kill-your-business-and-make-things-less-fun>

## Business outcomes

There are many potential benefits to an organization when a retention or attrition model is successfully deployed and leveraged:

1. **Financial Savings**: Beyond recruitment costs, low turnover can lead to financial savings in areas like benefits administration and retirement plans, which are more cost-effective with long-term employees. Moreover, costs associated with hiring, training, and productivity losses due to employee attrition can also be reduced.[^7] [^8] [^9] [^10]

2. **Increased Employee Engagement**: Employees who feel valued and supported are more likely to be engaged in their work. This leads to higher levels of job satisfaction and overall performance. An employee retention model can help identify the issues that cause dissatisfaction and disengagement.

3. **Enhanced Productivity**: When turnover is addressed, there’s less disruption to workflows, resulting in higher overall productivity. By maintaining a manageable level of turnover, an organization can avoid adding additional stress to current employees, thus improving productivity (e.g. reducing absences).

4. **Knowledge Retention**: Long-term employees have valuable institutional knowledge. By retaining them, organizations maintain critical expertise within the company.

5. **Innovation and Creativity**: Long-term employees are often more comfortable taking risks and suggesting innovative ideas. When they feel secure in their roles, they’re more likely to contribute creative solutions.

<ins>References</ins>

7: <https://www.forbes.com/sites/johnhall/2019/05/09/the-cost-of-turnover-can-kill-your-business-and-make-things-less-fun>

8: <https://www.simplybenefits.ca/blog/employee-retention-what-is-the-true-cost-of-losing-an-employee>

9: <https://www.terrastaffinggroup.com/resources/blog/cost-of-employee-turnover>

10: <https://www.workhuman.com/blog/the-ridiculously-high-cost-of-employee-turnover>
