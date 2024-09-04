## Analysis Overview

This analysis is meant to predict whether or not accounts are at risk of defaulting. The features used to predict the loan status were: 
* Loan Size
* Interest Rate
* Borrower Income
* Debt to Income Ratio
* Number of Accounts
* Derogatory Marks

The data was very imbalanced with 96.8% of accounts not being at risk of defaulting. As a result, after the data was scaled, the dataset needed to be stratified on the loan status when the `train_test_split` was run to ensure that both the training and testing data sets had accurate ratios of borrower loan statuses.

The models that were used include:
* Mathematical Models
    * Logistic Regression
    * Support Vector Machine (SVM)
    * k-Nearest Neighbor
* Tree-based Models
    * Decision Tree
    * Random Forest
    * Extra Trees
    * Ada Boost
    * Gradient Boosting
    * XGBoost
    * LightGBM

## Results

* Logistic Regression: 
    * Accuracy: 0.99
    * Precision: 0.88
    * Recall: 0.97
    * F1-Score: 0.93
    * AUC Score: 0.996
* Decision Tree: 
    * Accuracy: 0.99
    * Precision: 0.89
    * Recall: 0.79
    * F1-Score: 0.83
    * AUC Score: 0.934
* Random Forest: 
    * Accuracy: 0.99
    * Precision: 0.89
    * Recall: 0.86
    * F1-Score: 0.87
    * AUC Score: 0.996
* Support Vector Machine (SVM): 
    * Accuracy: 1.00
    * Precision: 0.89
    * Recall: 0.99
    * F1-Score: 0.94
    * AUC Score: 0.995
* k-Nearest Neighbor (kNN): 
    * Accuracy: 1.00
    * Precision: 0.89
    * Recall: 0.99
    * F1-Score: 0.94
    * AUC Score: 0.996
* Extra Trees: 
    * Accuracy: 0.99
    * Precision: 0.89
    * Recall: 0.80
    * F1-Score: 0.84
    * AUC Score: 0.961
* Ada Boost: 
    * Accuracy: 1.00
    * Precision: 0.89
    * Recall: 0.99
    * F1-Score: 0.93
    * AUC Score: 0.996
* Gradient Boosting: 
    * Accuracy: 1.00
    * Precision: 0.89
    * Recall: 0.99
    * F1-Score: 0.93
    * AUC Score: 0.995
* XGBoost: 
    * Accuracy: 1.00
    * Precision: 0.89
    * Recall: 0.99
    * F1-Score: 0.94
    * AUC Score: 0.995
* Light GBM: 
    * Accuracy: 1.00
    * Precision: 0.89
    * Recall: 0.99
    * F1-Score: 0.94
    * AUC Score: 0.996

## Summary

Looking at the models, they all perform about the same. While some of the more complex tree models (i.e. Ada Boost, XGBoost, Light GBM, etc.) have marginally higher accuracy, presicion, and recall scores than the Logistic Regression model, the difference is relatively minor. The Logistic Regression had an Area Under the Curve (AUC) score of 0.996 in addition to an accuracy of 0.99, precision of 0.88, and a recall of 0.97. With the score results, and how close the results are to the tree-models, the Logistic Regression is the best model to use. Because the Logistic Regression is a very explainable model, it should be preferred over the other models given the low risk of either Type 1 or Type 2 errors and because no other model is significantly better.

If the bank were to want to decrease the risk of a Type 1 error where they think an account is at risk of defaulting when it isn't, the best model would be one of the following models: 
* Ada Boost, 
* Gradient Boosting, 
* XGBoost, 
* Light GBM, 
* k-Nearest Neighbor, or 
* Support Vector Machine.

All of the listed models had a recall score of 0.99. However, the Logistic Regression had a recall of 0.97. So while the listed models would have a decreased risk of a Type 1 error, the difference isn't that impactful.

On the other hand, if the bank wanted to decrease the risk of a Type 2 error where they think an account is not at risk of defaulting when it is, all models perform around the same with a precision score of 0.88 or 0.89, so there is no real difference between models in that regard.

As a final recommendation, the Logistic Regression is the best model to use.
