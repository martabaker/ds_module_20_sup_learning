# ds_module_20_sup_learning
Supervised Learning Homework

## Libraries/Languages
1. Python
2. Jupyter Notebook
3. Pandas
4. Scikit Learn
5. Standard Scaler
6. Seaborn
7. Matplotlib
8. Train-test split
8. Following Classification Models:
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

## Work Description
1. Read in a CSV of lending data using Pandas
2. Normalized the data with StandardScaler because there were some significant variation in the features
3. Ran a `train_test_split` to predict the loan status. Given a significant imbalance in the loan status (96.8% of the loan statuses were not at risk of default), stratification was used to ensure that the ratio of `0s` and `1s` was reflected in the testing and training datasets
4. Using a formula to run each classification models, 10 different models were run to determine the best model to use to predict whether or not accounts were at risk of defaulting