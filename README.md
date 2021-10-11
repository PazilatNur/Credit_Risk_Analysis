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

<img width="739" alt="SMOTE Oversampling" src="https://user-images.githubusercontent.com/79488124/136719140-0c1e4889-7a1b-4811-8207-6e4d7a040d7b.png">


2. SMOTE Oversampling

Balanced Accuracy Score: 0.654

Classification Report: 

This model has higher low_risk sensitivity and higher low_risk F1 score

<img width="739" alt="SMOTE Oversampling" src="https://user-images.githubusercontent.com/79488124/136719340-9ab87b24-1925-463d-93c3-00faaf0d566a.png">



3. ClusterCentroids resampler method

Balanced Accuracy Score: 0.53

Classification Report: 

This model has fairly good high risk sensitivity of 0.67 compared to low risk sensitivity of 0.4.  Overall F1 score is only at 0.56

<img width="713" alt="ClusterSampling" src="https://user-images.githubusercontent.com/79488124/136719172-f3dcef2e-bd9b-40e0-96ec-937af750bbff.png">


4. Combination of Sampling

Balanced Accuracy Score: 0.654

Classification Report: 

This model has relatively lower 0.63 recall of high_risk, compared to low_risk recall rate of 0.68.

<img width="723" alt="Combination of sampling" src="https://user-images.githubusercontent.com/79488124/136719183-d8dcf7a8-bf62-4831-afec-5289f547e864.png">



## Ensemble leanrers 

5. Balanced Random Forest Classifier

Balanced Accuracy Score: 0.712

Classification Report: 

this model better has higher low_risk recall rate of 0.82, but high_risk recall rate is also slightly better compared to our oversampling methids. Overall F1 score is high at 0.9.

<img width="744" alt="Random Forest" src="https://user-images.githubusercontent.com/79488124/136719206-48a1a944-a2de-4815-ac16-8a466cd5529f.png">




6. Easy Ensemble Classifier

Balanced Accuracy Score: 0.717

Classification Report: 

This model has overall better low_risk sensitivity rate than high_risk sensitivity rate. But compared to previous model, this also has a better high_risk sensitivity rate with overall better F1 score.

<img width="821" alt="Easy Ensemble" src="https://user-images.githubusercontent.com/79488124/136719233-caef1592-27b6-4f1d-91bc-20fd25c60d97.png">




## Summar:

When it comes to predicting credit risk, we would want a significantly better HIGH_RISK sensitivity than low_risk sensitity to make sure we would filter out as many high_risk applicant as possible. Given this goal, none of our model is good enough to predict high_risk applicants. 

However, If we looking to pick one model to utilize out of the 6 models, then it should be BalancedRandomForestClassifier. This model has much higher low_risk sensitivity rate of 0.82 with high F1 score of 0.9. We can be fairly confident in approving credit for low_risk applicants. 










