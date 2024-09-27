**Credit-Score-Classification**

1.INTRODUCTION

Over a year, a global finance company has collected basic bank details and gathered a lot of credit related information. The management wants to build an intelligent system to segregate the people into credit score brackets to reduce the manual efforts. Given a person's credit related information build a machine learning model that can classify the credit score.

2.PROBLEM STATEMENT

I have been appointed as a data scientist in the company to help in following:
Given a person’s credit-related information, build a machine learning model that can classify the credit score.
The dataset contains 1 lakh records with 28 features. There is an inherent chronological order within the dataset as for each customer 8 consecutive month period data is present across 8 records.

3.INSIGHTS

- The data seems quite complex and non-linear and difficult to draw patterns as the  three credit score classes - Standard/Poor/Good are not linearly seperable while plotting them as hue in scatter plots.
- As per feature importances for decision tree are concerned, Outstanding debt and credit mix are having high correlation with credit score followed by delay from due date, Interest rate and changed credit limit. Remaining features like age, occupation lie zero in terms of relative importance to credit score.
- We've hence, retained those top 5 features/attributes for fitting our model. However, in reality, we would require SME intervention to understand important features with respect to target variable as some of features might be really impactful in combination, hence subject matter judgement is required.

4.MACHINE LEARNING MODEL

We've leveraged and fit non-linear complex models - Decision Trees & Random Forest as the three target classes are not linearly seperable and we've converged on a best random forest model with parameters {'max_depth': None, 'min_samples_leaf': 1, 'min_samples_split': 10, 'n_estimators': 100} that has the following evaluation metrics score:

('Accuracy:', 0.7725232882300945)
Precision: 0.7568671127602743
Recall: 0.7587723144809307
f1 score: 0.7577900200937324
