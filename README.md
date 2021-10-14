# Credit Risk Analysis

## Analysis Overview
In this project, we use Python to build and evaluate several machine learning models to predict credit risk.
We adopted the following procedure:

* Oversample the data using the RandomOverSampler and SMOTE algorithms.
* Undersample the data using the ClusterCentroids algorithm.
* Use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm.
* Compare two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier.

We will evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk.

## Results
### RandomOverSampler model

![RandomOverSampler model1](https://user-images.githubusercontent.com/62515666/136883785-4af23c94-d2e6-456c-b0d3-5bd0e88339f8.png)

![RandomOverSampler model2](https://user-images.githubusercontent.com/62515666/136885136-94b663ad-405f-4481-84e2-3a1e4174e3ba.png)

The balanced accuracy score is 65%.
The high_risk precision is about 1% only with 62% sensitivity which makes a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 68%.

### SMOTE model

![SMOTE_model](https://user-images.githubusercontent.com/62515666/136885389-aef74468-d410-4e3b-899a-5bb90c648e35.png)
# Credit Risk Analysis

## Analysis Overview
In this project, I am using Python to build and evaluate several machine learning models to predict credit risk. Below are the procedures followed:

* Oversample the data using the RandomOverSampler and SMOTE algorithms
* Undersample the data using the ClusterCentroids algorithm
* Use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm
* Compare two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier

We will evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk.

## Results
### RandomOverSampler model

![RandomOverSampler model1](https://user-images.githubusercontent.com/62515666/136883785-4af23c94-d2e6-456c-b0d3-5bd0e88339f8.png)

![RandomOverSampler model2](https://user-images.githubusercontent.com/62515666/136885136-94b663ad-405f-4481-84e2-3a1e4174e3ba.png)

The balanced accuracy score is 65%.
The high_risk precision is about 1% only with 67% sensitivity and a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 64%.

### SMOTE model

![SMOTE_model](https://user-images.githubusercontent.com/62515666/136885389-aef74468-d410-4e3b-899a-5bb90c648e35.png)

The results are pretty similar to the previous model.
The balanced accuracy score is 62%.
The high_risk precision is about 1% only with 61% sensitivity which makes a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 64%.

### ClusterCentroids model

![ClusterCentroids_model](https://user-images.githubusercontent.com/62515666/136885607-48db2588-f7b9-436f-9017-4fe5e32cc6fa.png)

Here the balanced accuracy score is down to about 51%.
The high_risk precision is still 1% only with 59% sensitivity which makes a F1 of 1%.
Due to the high number of false positives, the low_risk sensitivity is only 43%.

### SMOTEENN model

![SMOTEENN_model](https://user-images.githubusercontent.com/62515666/136885871-cea1d4d0-d65a-4d20-abff-1fed0a2b2faf.png)

The balanced accuracy score is about 62%.
The high_risk precision is still 1% only with 71% sensitivity which makes a F1 of only 2%.
Due to the high number of false positives, the low_risk sensitivity is 54%.

### BalancedRandomForestClassifier model

![BalancedRandomForestClassifier_model](https://user-images.githubusercontent.com/62515666/136886856-ba723006-0730-4264-8a58-201e802a73a1.png)

The balanced accuracy score improved to about 78%.
The high_risk precision is still low at 4% only with 67% sensitivity which makes a F1 of only 7%.
Due to a lower number of false positives, the low_risk sensitivity is now 91% with 100% presicion.

### EasyEnsembleClassifier model

![EasyEnsembleClassifier_model](https://user-images.githubusercontent.com/62515666/136886277-8f5d9319-8870-4e8f-9ed2-b3d2a2ffe730.png)

Now, the balanced accuracy score is high to about 93%.
The high_risk precision is still low at 7% only with 91% sensitivity which makes a F1 of only 14%.
Due to a lower number of false positives, the low_risk sensitivity is now 94% with 100% presicion.

## Summary

All the models used to perform the credit risk analysis show weak precision in determining if a credit risk is high.
The Ensemble models brought a lot more improvement specially on the sensitivity of the high risk credits.
The EasyEnsembleClassifier model shows a recall of 92% so it detects almost all high risk credit. On another hand, with a low precision, a lot of low risk credits are still falsely detected as high risk which would penalize the bank's credit strategy and infer on its revenue by missing those business opportunities.
For those reasons I would not recommend the bank to use any of these models to predict credit risk.
