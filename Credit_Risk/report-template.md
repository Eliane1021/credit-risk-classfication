# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
 * The purpose of this analysis was to develop and evaluate machine learning models to predict the loan status of borrowers. Specifically, the goal was to determine whether a loan is classified as "healthy" (0) or "high-risk" (1) based on a set of financial and borrower-related features.

* Explain what financial information the data was on, and what you needed to predict.
 * The dataset includes financial information about borrowers such as: 
    Loan size，
    Interest rate
    Borrower income
    Debt-to-income ratio
    Number of accounts
    Derogatory marks
    Total debt
* The objective was to predict the loan_status variable, which represents:
    0: Healthy loans
    1: High-risk loans

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
    Using the value_counts for the target variable (loan_status):

    0: Majority class representing healthy loans.
    1: Minority class representing high-risk loans.

* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).
    Data Preprocessing:

        Separated the data into features (X) and labels (y).
        Split the data into training and testing datasets using an 80-20 split.
        Standardized the features using StandardScaler to improve model performance.

    Modeling:

        Trained a Logistic Regression model as a baseline model due to its simplicity and interpretability.
        Used the training dataset to fit the model.
        Made predictions on the test dataset.

    Evaluation:

        Evaluated the model's performance using a confusion matrix and a classification report, which provided accuracy, precision, recall, and F1-score metrics.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.
        Logistic Regression Model:
                Accuracy: 99%
                Precision:
                For Class 0 (Healthy loans): 100%
                For Class 1 (High-risk loans): 86%
        Recall:
                For Class 0: 99%
                For Class 1: 94%
                F1-Score:
                For Class 0: 100%
                For Class 1: 90%
        
        Confusion Matrix:

                True Positives (Class 1 predicted as 1): 476
                False Positives (Class 0 predicted as 1): 31
                True Negatives (Class 0 predicted as 0): 14,924
                False Negatives (Class 1 predicted as 0): 77

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
    The Logistic Regression model demonstrates high overall accuracy (99%) with strong performance in predicting healthy loans (Class 0).

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
Yes, performance critically depends on the problem's objective. In this analysis:

Importance of Predicting 1s (High-Risk Loans)
High-risk loans (1) represent borrowers likely to default.
Correctly identifying these loans is crucial for financial institutions to mitigate risks and avoid financial losses.
Metrics like recall for Class 1 are particularly important, as missing high-risk loans (false negatives) could result in approving loans that might default.
Importance of Predicting 0s (Healthy Loans)
Predicting healthy loans (0) ensures that borrowers who are low-risk are not unnecessarily denied loans.
Precision for Class 1 also matters here because false positives (predicting a healthy loan as high-risk) can lead to unfair denial of loans to low-risk borrowers, potentially damaging customer trust.

If you do not recommend any of the models, please justify your reasoning.
For balanced risk mitigation, this Logistic Regression model performs well and can be recommended.