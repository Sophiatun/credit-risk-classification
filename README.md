### credit-risk-classification

# Overview of the Analysis

The dataset, consisting of 77,536 data points, underwent a split into training and testing sets. The training set, comprised of 75,036 low-risk loan data points and 2,500 high-risk data points, served as the foundation for constructing the initial logistic regression model (Logistic Regression Model 1) utilizing the LogisticRegression module from scikit-learn. Subsequently, Logistic Regression Model 1 was applied to the testing dataset to ascertain whether a loan to the borrower in the testing set would be categorized as low- or high-risk.

To address the class imbalance in the training data, the RandomOverSampler module from imbalanced-learn was employed to resample the training set data. This ensured that the logistic regression model had an equal number of data points to draw from during training, enhancing its ability to learn from both low- and high-risk instances effectively.

# Results

# Machine Learning Model 1:

- Model 1 Accuracy: 0.952.
- Model 1 Precision: for healthy loans the precision is 1.00, for high-risk loans the precision is 0.84.
- Model 1 Recall: for healthy loans the recall score is 0.99, for high-risk loans the recall score is 0.94.

# Machine Learning Model 2:

- Model 2 Accuracy: 0.995.
- Model 2 Precision: for healthy loans the precision is 0.99, for high-risk loans the precision is 0.99.
- Model 2 Recall: for healthy loans the recall score is 0.99, for high-risk loans the recall score is 0.99.

# Summary

It seems that the logistic regression model with the oversampled data performed better when making predictions.

If the objective of the model is to assess the probability of high-risk loans, neither model achieves a precision score exceeding 90%. However, Logistic Regression Model 2 demonstrates fewer false predictions across the testing dataset compared to Logistic Regression Model 1. Consequently, considering its notably high accuracy and recall, Logistic Regression Model 2 emerges as the preferred choice for practical application.
