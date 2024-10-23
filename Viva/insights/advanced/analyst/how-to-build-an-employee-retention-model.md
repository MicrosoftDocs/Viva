---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 10/25/2024
title: How to build an employee retention model
description: Explains the process for building an employee retention model using R and Python.
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

# How to build an Employee Retention Model using R and Python

In this example, we'll use Random Forest to build our employee retention model. Random Forest is a popular and effective machine learning model for predicting employee turnover, since it can handle both categorical and continuous variables, capture non-linear relationships between variables, and provide insights into variable importance.

### 1. Read the data

First, read the data from the different data sources into a data frame. A data frame is a tabular data structure that stores the data in rows and columns.

For example, if we have a CSV file named `person_query.csv` downloaded from Viva Insights, we can read it into a data frame using the code below. In both cases of Python and R, we have loaded in the respective 'vivainsights' package, which contains specific functions for analyzing data from Viva Insights. The `import_query` function loads in the csv query and performs variable name cleaning in the process.

*Python:*

```python
import numpy as np
import pandas as pd
import matplotlib as mpl
import matplotlib.pyplot as plt
import vivainsights as vi

train = vi.import_query("input/person_query.csv") 
```

*R:*

```R
library(tidyverse)
library(vivainsights)
library(randomForest)
library(caret) # For splitting training and test datasets
library(pROC)

raw_data <- vivainsights::import_query("input/person_query.csv")
```

We can then inspect the data frame using the head, tail, info, and describe methods. These methods help us get a glimpse of the data, its structure, its summary statistics, and its missing values.

> [!NOTE]
> In R, once a package is loaded with `library(package)`, it's not necessary to prefix the function with the package name when calling it. However, if you want to use a function without loading the entire package, or if there's a naming conflict between functions from different packages, you can use `package::function()` to explicitly call the function. For clarity in this demonstration, we'll use this explicit notation to show which package each function comes from.

### 2. Clean the data

The next step is to clean the data by handling missing values, outliers, and categorical variables.

- **Missing values** are the values that aren't recorded in the data, and they can affect the performance and accuracy of the model.
- **Outliers** are the values that are far away from the normal range of the data, and they can also distort the results of the model.
- **Categorical variables** are the variables that have a finite number of discrete values, such as gender, color, or class.

#### Validating Viva Insights metrics

Missing values generally do not occur in Viva Insights metrics, although there are a few scenarios where there might be outliers and anomalous values. For instance:

  1. Collaboration metrics might be unusually low for some individuals or teams due to personal leave or national public holidays.
  2. Collaboration metrics might be unusually high or skewed for some individuals, as some licenses might have been assigned to non-ordinary mailboxes.
  3. Some mailboxes might appear to be close to inactive, as the individual might have already left the organization.
  
The **vivainsights** packages provide functions for identifying metric outliers, inactive weeks, and general population holiday weeks in the data.

*Python:*

```python
# Return a data frame removing weeks where collaboration was 1 standard deviation below the mean
train = vi.identify_holidayweeks(train, sd = 1, return_type = "cleaned_data")

# Return a data frame removing person-weeks where collaboration was 1 standard deviation below the mean
train = vi.identify_inactiveweeks(train, sd = 1, return_type = "data_cleaned")
```

*R:*

```R
clean_data <-
    raw_data %>%
    identify_holidayweeks(sd = 1, return = "cleaned_data") %>%
    identify_inactiveweeks(sd = 1, return = "data_cleaned")
```

#### Missing values

You might have missing values that come from other data sources that you import into the model, such as data on absence days or pay and benefit packages.

There are different ways to handle missing values: delete the rows or columns that have missing values; or impute the missing values with the mean, median, mode, or a constant value. The choice of the method depends on the nature and amount of the missing values, and the impact they have on the model.

*Python:*

```python
# Check for missing data
NAs = pd.concat([train.isnull().sum()], axis=1, keys 'Train'])

# Filter data frame to include only columns with at least one missing value
cols_with_missing = NAs[NAs.sum(axis=1) > 0].index

# Drop rows with missing data
train = train.dropna(subset = cols with missing)
```

*R:*

```R
# Filter data frame to include only columns with at least one missing value
cols_with_missing <- clean_data %>% select_if(~ any(is.na(.)))

clean_data <-
  clean_data %>%
  drop_na(cols with missing) # drop rows with missing values
```

As you're preparing the data, check the values in `cols_with_missing` so that you're not dropping the missing values inadvertently. If the data is missing due to non-random reasons (Missing Not At Random, or MNAR), i.e. that is due to a systematic reason, then this might bias the results of the model. In general, only filter out missing data in variables you're confident are Missing Completely At Random (MCAR), since the complete randomness means filtering will not introduce bias into the training dataset.  

For other scenarios, we can choose to handle missing data by imputation. The following code fills the missing values of a given column ('colName') by mean values. You can also replace it by median values, mode values or a constant value depending on the scenario and the column of the data set.

*Python:*

```python
train['colName'] = train['colName'].fillna(train['colName'].mean())
```

*R:*

```R
clean_data $colName[is.na(clean_data $colName)] <- mean(clean_data $colName, na.rm = TRUE)
```

#### Creating dummy variables

Depending on the implementation of the random forest algorithm, you will probably need to handle any predictor variables in your model that are categorical. In Python’s **scikit-learn**, the CART algorithm is used and therefore cannot accept categorical variables as-is. The **randomForest** package in R handles this automatically, but can be computationally expensive for high cardinality categorical predictors.  

One way to do this is to achieve dummy variables for each category, in a process that is known as **one-hot encoding**. One-hot encoding is a way of transforming categorical data into numerical data for machine learning purposes. It creates a new column for each possible category and assigns a value of 1 or 0 to indicate whether the original data belongs to that category or not.

*Python:*

```python
# hot encode columns which can be categorised into discreet features values
list_cat_col = ['ColA', 'ColB', 'ColC'] # list of column names which are categorical columns

for col in list_cat_col:
    for_dummy = train[col]
    train = pd.concat([train, pd.get_dummies(for_dummy, prefix=col)], axis=1)
```

Although one-hot encoding isn't necessary when using the **randomForest** R package, the same approach is shown here to demonstrate the logic.  

*R:*

```R
# Hot encode columns which can be categorized into discrete feature values
list_cat_col <- c("ColA", "ColB", "ColC") # List of column names which are categorical columns


df_with_dum_vars <-
  list_cat_col %>%
  purrr::map(function(x){
    
    # unique row id is necessary
    # create unique column names for dummy variables
    df <- data.frame(id = seq(1, length(clean_data[[x]])),
                     category = paste0(x, "_", clean_data[[x]]))
    
    df_wide <-
      pivot_wider(
        df,
        names_from = category,
        values_from = category,
        values_fn = length,
        values_fill = 0
      ) %>%
      select(-id) # Remove id
    
  }) %>%
  bind_cols()

clean_data <- cbind(clean_data, df_with_dum_vars)
```
> [!NOTE]
> Despite its simplicity, the one-hot encoding approach can degrade the performance of the random forest model with high cardinality categorical variables, because it will increase the number of features of the model. Alternative solutions are to consider other techniques for encoding (e.g. target encoding, frequency encoding) or clustering the feature so that they have fewer unique values. 

### 3. Train the model

The third step is to train the random forest model on the training data. To do this, we need to split the data into training and test sets, and then fit the model on the training set. Splitting the data into training and test sets is a common practice in machine learning and predictive modeling. The purpose of this step is to evaluate the performance of the model on data it hasn't seen before, and to avoid overfitting the model to the training data.

If we were to train the model on the entire dataset, it would likely perform well on the training data, but might not generalize well to new data. This is because the model might have learned to fit the noise in the training data, rather than the underlying patterns that are present in the data.

By splitting the data into training and test sets, we can train the model on the training set and evaluate its performance on the test set. This allows us to estimate how well the model performs on new data, and to identify any issues with overfitting or underfitting the model.

> [!NOTE]
> In addition to splitting the data into training and test sets, it's also common to use techniques such as cross-validation to further evaluate the performance of the model and tune its hyperparameters. These techniques help to ensure that the model is robust and performs well on a variety of data. Cross-validation techniques aren't covered in this Playbook, but there are many resources online on how to take this further.

We can use the **scikit-learn** library to perform these tasks.

For example, if we want to split the data into 70% training and 30% test sets, and then train a random forest model with 100 trees, we can use the following code:

*Python:*

```python
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(train, labels, test_size=0.30)
```

In R, the `createDataPartition()` function from **caret** makes it easy to split the data into training and testing datasets. In the following example, the parameters are provided in this order: 1. Data frame containing the predictor variables only; 2. Data frame containing the outcome variable only; and 3. `test_size` controlling the proportion of the dataset to include in the train split.

This is assigned to four data frames: 

- `x_train` - predictors, train set 

- `x_test` - predictors, test set 

- `y_train` - outcome, train set 

- `y_test` - outcome, test set 


*R:*

```R
set.seed(123) # Set seed for reproducibility

# Split the data into training and testing sets
trainIndex <- caret::createDataPartition(
y = clean_data$HasChurned, # outcome
p = 0.7, # percentage goes into training
list = FALSE # do not return result as list
)

train_df <- clean_data[trainIndex, ]
test_df <- clean_data[-trainIndex, ]

```

The next step is to fit the random forest model, which we'll use `RandomForestClassifier()` from scikit-learn for Python and `randomForest::randomForest()` for R. In both cases, we'll use the default parameters which come with the functions.

*Python:*

```python
from sklearn.ensemble import RandomForestClassifier

rf = RandomForestClassifier()

rf.fit(x_train, y_train)

RandomForestClassifier(
  bootstrap=True,
  class_weight=None,
  criterion='gini',
  max_depth=None,
  max_features='auto',
  max_leaf_nodes=None,
  min_impurity_split=1e-07,
  min_samples_leaf=1,
  min_samples_split=2,
  min_weight_fraction_leaf=0.0,
  n_estimators=10,
  n_jobs=1,
  oob_score=False,
  random_state=None,
  verbose=0,
  warm_start=False
)

y_pred = rf.predict(x_test)
```

*R:*

```R
# Build the random forest model
rf <- randomForest(
formula = perform_cat ~ .,
data = train_df,
importance = TRUE # to allow importance to be calculated afterwards
)

rf

```

AUC (area under the curve) can serve as our evaluation metric, assessing how well a binary classification model differentiates between positive and negative categories. Given that we're predicting whether an individual will leave the organisation, it qualifies as a binary classification problem. AUC is an effective method for evaluating such scenarios.

*Python:*

```python
from sklearn.metrics import roc_curve, auc

false_positive_rate, true_positive_rate, thresholds = roc_curve(y_test, y_pred)
roc_auc = auc(false_positive_rate, true_positive_rate)
roc_auc
```

*R:*

```R
# Calculate the ROC AUC score
roc <- roc(y_test, y_pred)
roc_auc <- auc(roc)
roc_auc
```

This gives the AUC value. As the AUC value trends closer towards 1, it gives accurate predictions. If it trends towards 0, the accuracy decreases.

In the next section, we'll learn how to tune the parameters of the model to make it predict accurate results.

### 4. Tune the hyperparameters of the model

The final step is to tune the parameters of the random forest model to find the optimal values of the hyperparameters that maximize the performance and accuracy of the model. Hyperparameters are the parameters that aren't learned by the model, but are set by the user before the training process.

Some of the hyperparameters of the random forest model are:

- `Number of trees or estimators`: The number of trees in the forest. A higher number of trees can improve the accuracy of the model, but it also increases the computational complexity and the risk of overfitting. Therefore, we need to find the optimal number of trees that balances the trade-off between performance and efficiency.
- `Max_depth`: The maximum depth of each tree.
- `Minimum_samples_split`: The minimum number of samples required to split a node.
- `Minimum_samples_leaf`: The minimum number of samples required for a leaf node.
- `Maximum_features`: The number of features to consider when looking for the best split.

Since the implementations of random forest in R and Python have different hyperparameters, you may only find code examples for one language and not the other for some hyperparameters.  

The table below shows which hyperparameters are available for the respective Python and R libraries:

| Hyperparameters | scikit-learn  | randomForest |
|----|----|----|
| Number of trees | n_estimators | ntree |
| Number of variables sampled at each split | / | mtry |
| Maxiumum depth | max_depth | / |
| Minimum samples split | min_samples_split | / |
| Maximum features |   |   |

The availability of these parameters might change depending on the version and the evolution of these libraries.  

We use a parameter search technique to compare different values of n_estimators and select the one that minimizes the error on the validation set.

*Python:*

```python
n_estimators = [1, 2, 4, 8, 16, 32, 64, 100, 200]

train_results = []
test_results = []

for estimator in n_estimators:
   rf = RandomForestClassifier(n_estimators=estimator, n_jobs=-1)
   rf.fit(x_train, y_train)   train_pred = rf.predict(x_train)   false_positive_rate, true_positive_rate, 

thresholds = roc_curve(y_train, train_pred)
roc_auc = auc(false_positive_rate, true_positive_rate)
train_results.append(roc_auc)   
y_pred = rf.predict(x_test)   

false_positive_rate, true_positive_rate, thresholds = roc_curve(y_test, y_pred)

roc_auc = auc(false_positive_rate, true_positive_rate)

test_results.append(roc_auc) from matplotlib.legend_handler 

import HandlerLine2D
line1, = plt.plot(n_estimators, train_results, 'b', label='Train AUC')
line2, = plt.plot(n_estimators, test_results, 'r', label='Test AUC')
plt.legend(handler_map={line1: HandlerLine2D(numpoints=2)})
plt.ylabel('AUC score')

plt.xlabel('n_estimators')
plt.show()
```

*R:*

```R
# Create function to loop through hyperparameter 

tune_rf_ntree <- function(ntree){ 

  rf <- randomForest( 

    formula = perform_cat ~ ., 
    data = train_df, 
    ntree = ntree 
  ) 

  # Predicted probabilities 
  pred_probs_train <- predict(rf, type = "prob", newdata = train_df)[, 2] 
  pred_probs_test <- predict(rf, type = "prob", newdata = test_df)[, 2] 

  # Compute ROC curve 
  roc_obj_train <- pROC::roc(train_df$perform_cat, pred_probs_train) 
  roc_obj_test <- pROC::roc(test_df$perform_cat, pred_probs_test) 

  # Return results 
  data.frame( 
   ntree = ntree, 
   auc_train = roc_obj_train$auc %>% as.numeric(), 
   auc_test = roc_obj_test$auc %>% as.numeric() 
  ) 
} 

auc_ntrees <- 
  c(1, 2, 4, 8, 16, 32, 64, 100, 200) %>% 
  purrr::map(tune_rf_ntree) %>% 
  bind_rows() 

auc_ntrees 

auc_ntrees %>% 

  ggplot() + 

  geom_line(aes(x = ntree, y = auc_train, colour = "Train"), linewidth = 0.8) + 

  geom_line(aes(x = ntree, y = auc_test, colour = "Test"), linewidth = 0.8) + 

  labs( 
    title = "Effect of Number of Estimators on AUC Score for Random Forest Model", 
    y = "AUC Score", 
    x = "Number of estimators / trees" 
  ) + 

  scale_colour_manual(values = c("Train" = "red", "Test" = "blue"))
```
:::image type="content" source="../images/retention-playbook-01.png" alt-text="Tune n_estimators.":::

In the plot above we can see that as the estimators increase, it leads to overfitting. The gap between the Train AUC and Test AUC scores starts to widen as the number of estimators increases. This indicates that the model is becoming increasingly specialized to the training data, and isn't able to generalize well to the new data. Therefore, we can choose the estimators with the smallest gap to train and test AUC.

Max_depth: represents the depth of each tree in the forest. The deeper the tree, the more splits it has and it captures more information about the data. We fit each decision tree with depths ranging from 1 to 32 and plot the training and test errors.

*Python:*

```python
max_depths = np.linspace(1, 32, 32, endpoint=True)

train_results = []
test_results = []

for max_depth in max_depths:
    rf = RandomForestClassifier(max_depth=max_depth, n_jobs=-1)
    rf.fit(x_train, y_train)   
    
    train_pred = rf.predict(x_train)   
    false_positive_rate, true_positive_rate, thresholds = roc_curve(y_train, train_pred)
    
    roc_auc = auc(false_positive_rate, true_positive_rate)
    train_results.append(roc_auc)   
 
    y_pred = rf.predict(x_test)   
     
    false_positive_rate, true_positive_rate, 
 
    thresholds = roc_curve(y_test, y_pred)
    
    roc_auc = auc(false_positive_rate, true_positive_rate)
    
    test_results.append(roc_auc)
 
    from matplotlib.legend_handler import HandlerLine2D
    line1, = plt.plot(max_depths, train_results, 'b', label="Train AUC")
    line2, = plt.plot(max_depths, test_results, 'r', label="Test AUC")
    plt.legend(handler_map={line1: HandlerLine2D(numpoints=2)})
    plt.ylabel(‘AUC score’)

    plt.xlabel(‘Tree depth’)
    plt.show()
```

:::image type="content" source="../images/retention-playbook-02.png" alt-text="Tune tree depth.":::

We can see that as the depth increases it leads to overfitting of the data.

- `min_samples_split`: The minimum number of samples needed to split an internal node, which is a node that has further branches. This parameter can range from one sample to the total number of samples. If the parameter is one sample, that means every node is split until it becomes a leaf. If the parameter is the total number of samples, that means no node is split. By increasing this parameter, we make
each tree in the forest more conservative, as it has to take into account more samples before splitting. In this analysis, we change the parameter from 10% to 100% of the samples.

*Python:*

```python
min_samples_splits = np.linspace(0.1, 1.0, 10, endpoint=True)

train_results = []
test_results = []
for min_samples_split in min_samples_splits:
   rf = RandomForestClassifier(min_samples_split=min_samples_split)
   rf.fit(x_train, y_train)   
   train_pred = rf.predict(x_train)   

   false_positive_rate, true_positive_rate, thresholds = roc_curve(y_train, train_pred)

   roc_auc = auc(false_positive_rate, true_positive_rate)
   train_results.append(roc_auc)   

   y_pred = rf.predict(x_test)   
   false_positive_rate, true_positive_rate, thresholds = roc_curve(y_test, y_pred)
   
   roc_auc = auc(false_positive_rate, true_positive_rate)
   test_results.append(roc_auc)

from matplotlib.legend_handler import HandlerLine2D

line1, = plt.plot(min_samples_splits, train_results, 'b', label="Train AUC")
line2, = plt.plot(min_samples_splits, test_results, 'r', label="Test AUC")

plt.legend(handler_map={line1: HandlerLine2D(numpoints=2)})
plt.ylabel('AUC score')
plt.xlabel('min samples split')
plt.show()
```

:::image type="content" source="../images/retention-playbook-03.png" alt-text="Tune minsamples split.":::

We can see as the min_samples_split increase, it leads to underfitting of the data.

`min_samples_leaf`: The minimum number of samples required to be at a leaf node. This parameter is similar to min_samples_split, but it describes the minimum number of samples at the leaves, the base of the tree. By increasing these values, we can reduce the complexity of the tree and prevent overfitting.

*Python:*

```python
# Define the range for min_samples_leaf

min_samples_leafs = np.linspace(0.1, 0.5, 5, endpoint=True)

# Initialize lists to store results 

train_results = []
test_results = []

# Loop over the range of min_samples_leaf 

for min_samples_leaf in min_samples_leafs:

    # Initialize the RandomForestClassifier with the current min_samples_leaf 
    rf = RandomForestClassifier(min_samples_leaf=int(min_samples_leaf * len(x_train))) 

    # Fit the model 
    rf.fit(x_train, y_train)   

    # Predict on the training set 
    train_pred = rf.predict(x_train)   

     # Calculate ROC AUC for the training set
    false_positive_rate, true_positive_rate, thresholds = roc_curve(y_train, train_pred)
    roc_auc = auc(false_positive_rate, true_positive_rate)
    train_results.append(roc_auc)

    # Predict on the test set
    y_pred = rf.predict(x_test)   

    # Calculate ROC AUC for the test set
    false_positive_rate, true_positive_rate, thresholds = roc_curve(y_test, y_pred)
    roc_auc = auc(false_positive_rate, true_positive_rate)
    test_results.append(roc_auc)

# Plot the results
line1, = plt.plot(min_samples_leafs, train_results, 'b', label="Train AUC")
line2, = plt.plot(min_samples_leafs, test_results, 'r', label="Test AUC")
plt.legend(handler_map={line1: HandlerLine2D(numpoints=2)})
plt.ylabel('AUC score')
plt.xlabel('min samples leaf')
plt.show()
```

:::image type="content" source="../images/retention-playbook-04.png" alt-text="Tune minsamples leaf.":::

As we can see, increasing the value of the parameter leads to underfitting, and both the Train AUC and Test AUC scores start to decrease or level off. This indicates that the model is becoming increasingly simple and isn't fitting the training data well. It also indicates the model isn't generalizing well to new data.

Another sign of underfitting is that the gap between the Train AUC and Test AUC scores starts to narrow as the value of the min_samples_leaf parameter increases. This indicates that the model is becoming increasingly generalized and isn't able to capture the complexity of the training data. The model also isn't able to generalize well to new data.

After putting the found best parameters from tuning, we can generate the model again to predict the values.

### Next steps

Advance to the next chapter to learn about some key steps you can take to improve the model's performance.

> [!div class="nextstepaction"]
> [Improve the model](apply-the-model.md)