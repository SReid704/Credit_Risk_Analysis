# Credit_Risk_Analysis

## Project Overview

Using data from LendingClub; a peer-to-peer lending company; we will use several Machine Learning Modules to predict credit risk. We will:

- Use RandomOverSampler and SMOTE algorithms to oversample data.
- Undersample data using ClusterCentroid algorithm
- Compare BalancedRandomForestClassifier and EasyEnsembleClassifier modules to reduce bias in credit risk.
- Over and undersample using SMOTEENN algorithm

By completing these procedures we will evaluate each module to see which will best fit to be used to predict credit risk.


## Results

### RandomOverSampler Model 

<img width="460" alt="image" src="https://user-images.githubusercontent.com/101374716/182257000-539a231c-9467-4333-a9e9-b76075c146c0.png">
<img width="354" alt="image" src="https://user-images.githubusercontent.com/101374716/182257036-87b50198-89ec-4efe-bedb-21e52faa330f.png">
<img width="791" alt="image" src="https://user-images.githubusercontent.com/101374716/182257086-677c2f05-3aca-4571-a0de-c1c53fa8a03f.png">

High risk precision is around 1% with 63% sensitivity. The balanced accuracy score is 62% which is low.

### SMOTE model

<img width="377" alt="image" src="https://user-images.githubusercontent.com/101374716/182257516-2ce62817-f234-486e-986d-d4a4954fcdc4.png">
<img width="373" alt="image" src="https://user-images.githubusercontent.com/101374716/182257571-81ca988d-80ba-4235-8bea-6780a69c3c8d.png">
<img width="759" alt="image" src="https://user-images.githubusercontent.com/101374716/182257603-ad22f5f1-c659-46f1-bdac-d0291a46a35e.png">

Balanced accuracy score is 64%; which is simlar to RandomOverSampler Model. The precision score are 1.00 for predicting low-risk and 0.01 for predicting high-risk. 

### ClusterCentroids Model

<img width="358" alt="image" src="https://user-images.githubusercontent.com/101374716/182257679-bddf012d-4245-416d-b0fa-83d4d6578e52.png">
<img width="358" alt="image" src="https://user-images.githubusercontent.com/101374716/182257748-2ad85261-a63f-4230-a25f-e910e9526368.png">
<img width="732" alt="image" src="https://user-images.githubusercontent.com/101374716/182257800-83640e38-1060-418e-862f-e54180f12f28.png">

Balanced accuracy score is around 64%. High risk precision is 1% with 63% sensitivity which makes a F1 of 2%.
Due to the high number of false positives, the low_risk sensitivity is only 42%.

### SMOTEENN Model

<img width="364" alt="image" src="https://user-images.githubusercontent.com/101374716/182257887-de0a3f58-9ee1-4ef0-b2a5-acbea127ccff.png">
<img width="348" alt="image" src="https://user-images.githubusercontent.com/101374716/182257933-789a1868-7b9c-4b43-8910-2bce8969dd3a.png">
<img width="791" alt="image" src="https://user-images.githubusercontent.com/101374716/182258053-a27efb4c-7bee-47ad-8cb2-9765000445af.png">

Balanced accuracy score is around 62%.
High risk is still 1% only with 68% sensitivity.
Due to the high number of false positives, the low_risk sensitivity is 57%.

### BalancedRandomForestClassifier Model

<img width="463" alt="image" src="https://user-images.githubusercontent.com/101374716/182258152-015d25d9-fae7-41dd-99d6-41dd0aeb1089.png">
<img width="454" alt="image" src="https://user-images.githubusercontent.com/101374716/182258218-87f78870-f6b1-4c1e-a406-cd50c33cca5b.png">
<img width="746" alt="image" src="https://user-images.githubusercontent.com/101374716/182258269-45143346-ccca-4ac5-b34b-31fab1c77ba0.png">

The balanced accuracy score improved to around 79%; which is getting better than the previous models
The high_risk precision is still low at 4% only with 67% sensitivity which makes a F1 of only 7%.
With the lower number of false positives, the low risk sensitivity is now 91% with 100% precision.

### EasyEnsembleClassifier Model

<img width="485" alt="image" src="https://user-images.githubusercontent.com/101374716/182258343-01c918eb-ed63-4292-ae53-0574b84cd956.png">
<img width="430" alt="image" src="https://user-images.githubusercontent.com/101374716/182258396-2ff60f93-ccec-4440-b309-8c12ba537714.png">
<img width="705" alt="image" src="https://user-images.githubusercontent.com/101374716/182258433-7700a657-0ccc-448e-b266-52397bbab483.png">

Balanced accuracy score is around 93% which is high.
High_risk is low at 7% only with 91% sensitivity.


## Summary

After completering and reviewing all the different models, the EasyEnsembleClassifier is the best choice. This should be the model that is used. The recall score has the highest coefficients for predicting both low and high risk loan status. This would be the best model due to false negatives associated with cost.
