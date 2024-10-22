---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 05/14/2024
title: Improve model performance
description: Provides an overview of steps that can be taken to make the employee retention model even more useful.
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

# Improve model performance

After you create and validate a random forest model to predict employee churn, there are several possible next steps you can take to improve the model's performance and make it more useful for employee retention purposes:

- Identify the most important factors that contribute to employee churn
- Predict employee churn for different segments or employee attributes
- Design interventions based on the above

## Identify the most important factors that lead to employee churn

The random forest model is a powerful machine learning technique that can predict the probability of an employee leaving the company based on various features. The model can also identify the most important features that influence the churn rate, which can help us understand the reasons behind employee turnover and design effective retention strategies.

To interpret the model, we can use the `feature_importances` attribute of the random forest classifier object in Python, or the `importance` function in R. This will return a vector of values that indicate how much each feature contributes to the prediction. The higher the value, the more important the feature is. For example, we can do:

*Python:*

```Python
# Get feature importances
feature_importances = pd.DataFrame(rf.feature_importances_, index=X.columns, columns=["importance"]).sort_values(by="importance", ascending=False)
print(feature_importances)
```

*R:*

```R
# Get feature importances
randomForest::importance(rf, type = 2)

```

This will output something like:

| Feature | Importance |
|---------------|------------|
| tenure | 0.32 |
| salary | 0.25 |
| Internal_network_size | 0.18 |
| Collaboration_hours | 0.12 |
| purpose | 0.08 |
| education | 0.05 |


>[!Note]
> In `randomForest::importance()`, `type = 2` returns the mean decrease in node impurity, whereas `type = 1` returns the mean decrease in accuracy (permutation-based).

In this example, the most important feature is tenure, followed by salary and Internal_network_size. This means that these are the factors that have the most impact on employee churn, and we should focus on improving them to increase retention.

## Predict employee churn using the model

You can also use the model to predict employee turnover for different segments or categories of employees. This requires applying the model to new data and generating predictions on the target variable. By predicting the runover rates of various groups of employees, organizations can take proactive steps to retain these employees and reduce overall churn rates.

To predict the churn risk of a group of existing employees using a trained random forest model, you first need to load the new data to predict and apply the model to make predictions on the target variable. In both Python and R, you can use the `predict` method/function of the trained random forest model to make predictions on the new data. Then, add the predictions to the new data by creating a new column and setting its values to the predictions.

*Python:*

```python
# Load the data to predict
new_data = vi.import_query("input/new_person_query.csv") 

# Make predictions on the new data
new_data['churn_risk'] = rf.predict(new_data)
```

*R:*

```R
# Load the data to predict
new_data <- vivainsights::import_query("input/person_query.csv")

# Make predictions on the new data
new_data$churn_risk <- predict(rf, newdata = new_data)
```

## Limitations and assumptions

While random forest models can be powerful tools for predicting employee churn and identifying factors that contribute to churn, there are several limitations and assumptions you should consider when using these models:

### Limitations

- The model assumes that the input features are independent of each other, which might not always be the case. For example, the satisfaction level of an employee might be influenced by their salary, which could lead to correlated features and potentially biased predictions.

- The model assumes the relationship between the input features and the target variable is linear, which might not be the case. Non-linear relationships might require more complex models or feature engineering to capture.

- The model assumes the input features are relevant to the target variable, which might not be the case. Irrelevant or noisy features can reduce the accuracy of the model and make it more difficult to interpret.

- The model assumes the training data is representative of the population of interest, which might not be the case. Biases in the training data can lead to biased predictions and inaccurate insights.

### Assumptions

- The model assumes the target variable is binary (i.e., churned or not churned), which might not be the case. In some cases, the target variable might have more than two possible values, such as low, medium, and high churn risk.

- The model assumes the input features are accurately measured and recorded, which might not be the case. Inaccurate or missing data can reduce the accuracy of the model and make it more difficult to interpret.

- The model assumes the input features are relevant to the problem of employee churn, which might not be the case. Some features might be more relevant than others, and it might be necessary to perform feature selection or engineering to identify the most important features.

- The model assumes the predictions are used for the purpose of employee retention, which might not be the case. The predictions might be used for other purposes, such as identifying employees for termination or downsizing, which could have negative consequences for employees and the organization.

### Next steps

Advance to the next chapter to learn about other scenarios for using an Employee Retention Model.

> [!div class="nextstepaction"]
> [See the scenarios](other-ways-to-use-an-employee-retention-model.md)