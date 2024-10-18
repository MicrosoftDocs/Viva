---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 10/25/2024
title: What metrics and queries can be accessed in Viva Insights and in Glint?
description: Provides an overview of the relevant metrics and queries needed to build an employee retention model.
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

# What metrics and queries can be accessed in Viva Insights and in Glint?

To build an employee retention model, it's recommended to draw from a large and diverse dataset that covers the relevant factors influencing employee turnover.

Viva Insights and Glint provide a rich source of data to construct an employee retention model.

## Prerequisites for building a model with Viva Insights and Glint

There are a number of prerequisites to use Viva Insights and Glint data in the employee retention model:

* Viva Insights and/or Glint must be fully set up and the Analyst is able to run queries from the Analyst Experience. Building the model requires access to the custom person query.

* The required Glint metrics are available in the person query from Viva Insights, or at least joined at the group-level.

* For best results, we recommend manual organizational data upload because it's likely to have a wider and more updated set of HR attributes to train the model.

* The aggregated and de-identified mailboxes for churned employees (in at least the last six months) should still be assigned licenses in Viva Insights in order to capture their collaboration data. The Administrator should also check the policy to ensure their collaboration data isn't deleted.

## Selecting features from Viva Insights and Glint

To build an employee retention model, it's important to identify relevant predictors that are known drivers of employee retention or engagement. Viva Insights metrics and Glint questions can be used as potential predictors, which are organized into dimensions or factors below.

One approach is to take one metric per dimension to act as a proxy measurement of that dimension. For example, using Collaboration hours as a proxy for Wellbeing. Or, you may choose to create a composite metric per dimension. The key here is to avoid collinearity, which occurs when two or more predictors are highly correlated with each other. Collinearity can lead to unstable and unreliable model coefficients, and can make it difficult to interpret the effects of individual predictors.

To address collinearity, factor analysis or principal component analysis can be used to reduce the number of repeated variables in the model. These techniques can identify underlying factors or components that explain the correlations among the predictors, and can reduce the number of predictors in the model while retaining most of the information. We also recommend you perform exploratory data analysis prior to deciding which predictor variables to include in the model. This can help to identify potential outliers, missing values, or other issues that may affect the quality of the model. Examples include:

* Correlation analysis - to identify highly correlated pairs
* Scatter plots - to flag outliers and nonlinear relationships
* Box plots - to identify missing values or measurement errors
* Histograms - to identify issues such as skewness and non-normality
* Heat maps - to flag clusters of highly correlated variables

Overall, selecting relevant predictors and addressing collinearity are important steps in building an accurate and reliable employee retention model.

## List of recommended features from Viva Insights and Glint

The following lists a number of dimensions and associated metrics and questions from Viva Insights and Glint that are relevant for training an Employee Retention Model:

### Wellbeing

**Viva Insights:**

* Collaboration hours
* Collaboration span
* Active Connected Hours
* After-hours collaboration hours
* Focus time

**Glint:**

* *How happy are you working at [company-name]?*
* *I feel well supported by [company-name] at this time*
* *I am able to successfully balance my work and personal life*

### Connection

**Viva Insights:**

* Internal network size
* Strong tie score
* Diverse tie score

**Glint:**

* *I feel a sense of belonging at [company-name]*
* *Teams at [company-name] collaborate effectively to get things done*
* *Leaders at [company-name] value different perspectives*
* *I feel satisfied with the recognition or praise I receive for my work*

### Empowerment

**Viva Insights:**

* Manager 1:1 time
* Meeting hours with manager (manager co-attendance)

**Glint:**

* *[company-name] does a good job of communicating with employees*
* *I feel empowered to make decisions regarding my work*
* *I have the resources I need to do my job well*

### Growth

**Viva Insights:**

* Skip-level meeting hours - representing skip-level exposure
* External network size

**Glint:**

* *I feel good opportunities to learn and grow at [company-name]*
* *My role is an excellent fit with my strengths*

### Purpose

**Glint:**

* *I have confidence in the leadership team*
* *I am excited about [company-name]'s future*
* *People at [company-name] live the company values*
* *The work that I do at [company-name] is meaningful to me*

### Clarity

**Glint:**

* *[company-name] continually improves the way work gets done*
* *I know what I should be focusing on right now*
* *[My manager] provides me with feedback that helps me improve my performance*

## Other metrics

Aside from Viva Insights and Glint metrics, there are other data sources that may be worth considering adding into the model. For instance:

* Number of absences
* Pay / benefits package
* Performance metrics
* Number of hours worked / shift patterns
* Viva Engage engagement metrics. For example, employees active on Viva Engage may be at lower risk of attrition

Organizational attributes, such as job functions, region, tenure, and seniority, may also have a significant impact on the likelihood of attrition. For instance, more junior employees may likely churn due to a lack of career progression or poor management, while senior employees may churn due to burnout. A comprehensive retention model should take into account these types of organizational contexts.

Other examples of organizational attributes include:

* Level designation
* Function type
* Region
* Department
* Contract type
* Remote vs. Hybrid vs. On-site

For more information on organizational attributes in Viva Insights, use [this resource](../admin/org-data-overview.md).

### Accessing the data

To train the model with the above datasets, we recommend downloading a custom Person Query from the Analyst Experience, and uploading all other data sources to Viva Insights as organizational data. This ensures that the data is available at the person-level granularity and provides greater accuracy when training the model.

The frequency of the organizational data upload is also important. The more frequent it is, the more accurately it would reflect any changes that have occurred for the individual over time.

### Next steps

Advance to the next chapter to learn how to build the model using the R and Python programming languages.

> [!div class="nextstepaction"]
> [Build the model](how-to-build-an-employee-retention-model.md)