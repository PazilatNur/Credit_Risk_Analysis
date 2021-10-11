# Credit_Risk_Analysis
## Overview;

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company to develop a machine learning to model to identify credit risk of potential/fututure applicants. This is an inherently unbalanced classification problem, hence we will test a few different machine learning calssfication models to improve our prediction of the high risk applicants. 

## Results:

In our data at a high level, we have data in the following categories:

    low_risk     68470 

    high_risk      347

### Logistic Regression

1. Random Oversampling Methods

Balanced Accuracy Score: 0.662

Classification Report:

This model has higher high_risk sensitivity of 0.7, but low_risk F1 score is much hibgher at 0.77 compared to high_risk F1 score of 0.02.




2. SMOTE Oversampling

Balanced Accuracy Score: 0.654

Classification Report: 

                  pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.63      0.68      0.02      0.65      0.43       101
   low_risk       1.00      0.68      0.63      0.81      0.65      0.43     17104

avg / total       0.99      0.68      0.63      0.80      0.65      0.43     17205




