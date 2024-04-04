# Module 20 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).

This analysis is intended to help predict lending risk given a variety of economic indicators including borrower income, debt-income ratio, total debt and loan size. Based on these factors, model created should predict whether to approve or reject a loan application. Using the dataset provided, the target column (loan_status) was separated as y values for testing/training sets. The remaining financial information was used as x values. The datasets were split into testing and training groups by a 70/30 ratio. The X features were then scaled for use in the model. 

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    ****Accuracy score: the accuracy score is 0.99, which means that out of 19,384 total predicted observations, only 1% of those were incorrectly diagnosed.
    ****Precision score: the precision score for predicted healthy loans is 1.00, which indicates that nearly 100% of healthy predictions were accurate and under 1% of those predicted ended up being unhealthy. On the other hand, the precision score for predicted unhealthy loans is 0.85, meaning that 85% of predictions were accurate, and 15% were actually healthy loans predicted incorrectly.
    ****Recall scores: the recall score for healthy loans is 0.99, which means that out of all loans that were actually healthy, just over 1% of healthy loans were misdiagnosed. For unhealthy loans the recall score is 0.91, meaning around 9% of actually unhealthy loans were misdiagnosed as healthy ones.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

The model should be expected to predict healthy loans fairly easily - and it does so highly effectively - given the vast majority of applications fall into that category. The efficacy of the model relies more heavily on the accurate detection of unhealthy loans, which it does effectively albeit less so than healthy loans. Both of these observations are supported by strong f1-scores. Of the 18,719 predicted healthy loan applications only 56 of those (>0.01%) were incorrectly predicted which is a number a lender can be happy with. Conversely, of 665 loans predicted to be high-risk, only 102 of them (15%) were incorrectly predicted. This tradeoff in accuracy is one that should be acceptable as a lender, because while it may reject actually healthy applications marginally more frequently, the your risk of lending to unhealthy borrowers is mitigated to a greater degree. Due to the data being heavily skewed toward healthy loan outcomes, it makes sense that the model is more effective in diagnosing those cases. However, the model is still effective enough to be used for its purpose of predicting unhealthy loan applications.
