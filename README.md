# credit-risk-classfication
# Instructions
The instructions for this Challenge are divided into the following subsections:

Split the Data into Training and Testing Sets

Create a Logistic Regression Model with the Original Data

Write a Credit Risk Analysis Report

# Split the Data into Training and Testing Sets
Open the starter code notebook and use it to complete the following steps:

Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.

Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.

Split the data into training and testing datasets by using train_test_split.

# Create a Logistic Regression Model with the Original Data
Use your knowledge of logistic regression to complete the following steps:

Fit a logistic regression model by using the training data (X_train and y_train).

Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.

Evaluate the model’s performance by doing the following:

Generate a confusion matrix.

Print the classification report.

Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

# Write a Credit Risk Analysis Report
Write a brief report that includes a summary and analysis of the performance of the machine learning models that you used in this homework. You should write this report as the README.md file included in your GitHub repository.

Structure your report by using the report template that Starter_Code.zip includes, ensuring that it contains the following:

An overview of the analysis: Explain the purpose of this analysis.
 The purpose of this analysis was to develop and evaluate machine learning models to predict the loan status of borrowers. Specifically, the goal was to determine whether a loan is classified as "healthy" (0) or "high-risk" (1) based on a set of financial and borrower-related features.
 
The results: Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine learning model.
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
A summary: Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.
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


