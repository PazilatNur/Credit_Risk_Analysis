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

https://github.com/PazilatNur/Credit_Risk_Analysis/issues/1#issue-1022143178


2. SMOTE Oversampling

Balanced Accuracy Score: 0.654

Classification Report: 

This model has higher low_risk sensitivity and higher low_risk F1 score

https://github.com/PazilatNur/Credit_Risk_Analysis/issues/2#issue-1022143597



3. ClusterCentroids resampler method

Balanced Accuracy Score: 0.53

Classification Report: 

This model has fairly good high risk sensitivity of 0.67 compared to low risk sensitivity of 0.4.  Overall F1 score is only at 0.56

https://github.com/PazilatNur/Credit_Risk_Analysis/issues/3#issue-1022143753


4. Combination of Sampling

Balanced Accuracy Score: 0.654

Classification Report: 

This model has relatively lower 0.63 recall of high_risk, compared to low_risk recall rate of 0.68.

https://github.com/PazilatNur/Credit_Risk_Analysis/issues/4#issue-1022143890



## Ensemble leanrers 

5. Balanced Random Forest Classifier

Balanced Accuracy Score: 0.712

Classification Report: 

this model better has higher low_risk recall rate of 0.82, but high_risk recall rate is also slightly better compared to our oversampling methids. Overall F1 score is high at 0.9.

https://github.com/PazilatNur/Credit_Risk_Analysis/issues/5#issue-1022144016




6. Easy Ensemble Classifier

Balanced Accuracy Score: 0.717

Classification Report: 

This model has overall better low_risk sensitivity rate than high_risk sensitivity rate. But compared to previous model, this also has a better high_risk sensitivity rate with overall better F1 score.

https://github.com/PazilatNur/Credit_Risk_Analysis/issues/6#issue-1022144219




## Summar:

When it comes to predicting credit risk, we would want a significantly better HIGH_RISK sensitivity than low_risk sensitity to make sure we would filter out as many high_risk applicant as possible. Given this goal, none of our model is good enough to predict high_risk applicants. 

However, If we looking to pick one model to utilize out of the 6 models, then it should be BalancedRandomForestClassifier. This model has much higher low_risk sensitivity rate of 0.82 with high F1 score of 0.9. We can be fairly confident in approving credit for low_risk applicants. 










