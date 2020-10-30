# ML_Credit_Risk_Analysis

## Overview of the analysis: 
- This analysis attempts to use different supervised machine learning techniques to train and evaluate models on how effectively they predict the risk of a given credit card loan based on approxiamtely 80 different features about the borrower and their loan. 
- The model classifies a given loan categorically as either high-risk or low-risk. 
- Six different machine learning resampling techniques were used to train the model:
  - Naive Random Oversampling
  - SMOTE Oversampling
  - Cluster Centroids (Undersampling)
  - SMOTEENN (Combination Sampling)
  - Balanced Random Forest Classifier
  - Easy Ensemble Classifier

## Results: 
#### Note: In the tables below, 0 codes for high-risk borrowers (minority-class) and 1 codes for low-risk borrowers (majority-class)

### Naive Random Oversampling:
##### Balanced Accuracy Score: 0.669

![NROS](https://github.com/asadca4u/ML_Credit_Risk_Analysis/blob/main/Images/1.png)
- The precision score is very low for the minority class at just 1%, however the recall score is a respectable 72% for this same class. 
  - Precision is a measure of positive predictive value — that is, how reliable a positive classification is. Within the context of credit card risk, from the perspective of the lender, it would be better to classify borrowers as high-risk when they are infact low-risk than it would be to classify borrowers as low-risk when they are in fact high-risk, as there is a greater potential to lose in this latter scenario.
- The precision score for the majority class is a perfect 100%, while the recall is a respbectable 62% for this same class. 
  - This model, in theory, will classify the vast majority of low risk borrowers correctly, meaning that the bank doesn't miss out on potential clients. 

### SMOTE Oversampling:
##### Balanced Accuracy Score: 0.647
![SMOTE](https://github.com/asadca4u/ML_Credit_Risk_Analysis/blob/main/Images/2.png)
- Again, the precision score is very low for the minority class at 1%, while it is virtually perfect for the majority class at 100%. 
- The recall scores are 61% for the minority class and 68% for the majority class. 
  - The recall score is the ability of the classifier to detect all present positive samples. In this analysis, the recall score of 0.61 reveals that the model is likley to detect 61% of all borrowers who are high-risk, as high risk. Conversely, a low recall is indicative of a large number of false negatives, that is, the model classifies a borrower as being negative for high risk, when they are in fact high risk.

### Cluster Centroids (Undersampling):
##### Balanced Accuracy Score: 0.545
- this score is barely greater than an absolutely random event, model is very poor at accurately predicting credit loan risk.
![CC](https://github.com/asadca4u/ML_Credit_Risk_Analysis/blob/main/Images/3.png)
- Again, the precision score is very low for the minority class at 1%, while it is virtually perfect for the majority class at 100%. 
- The recall scores are 69% for the minority class, and a very low 40% for the majority class, indicating the very high probability of the model returning a false negative, whereby the borrower is classified as negative for being low-risk, when they are in fact low-risk borrowers. 

### SMOTEENN (Combination Sampling):
##### Balanced Accuracy Score: 0.647
![SMOTEENN](https://github.com/asadca4u/ML_Credit_Risk_Analysis/blob/main/Images/4.png)
- Again, the precision score is very low for the minority class at 1%, while it is virtually perfect for the majority class at 100%. 
- The recall scores are 72% for the minority class, and a very low 57% for the majority class.
 

### Balanced Random Forest Classifier:
##### Balanced Accuracy Score: 0.717
![BRFC](https://github.com/asadca4u/ML_Credit_Risk_Analysis/blob/main/Images/5.png)
- The precision score for the minority class is marginally higher with this model at 2%, while the majority class still has a precision score of 100%. 
- The recall score for the minority class is 61%, while it is 82% for the majority class. This is a change from the previous models, where the recall score was greater for the minority class rather than the majority class, as in this case.  

### Easy Ensemble Classifier:
##### Balanced Accuracy Score: 0.739
![EEC](https://github.com/asadca4u/ML_Credit_Risk_Analysis/blob/main/Images/6.png)
- The precision score for the minority calss is 2% in this model, while it is still 100% for the majority class. 
- The recall score for the minority class is 71%, while it is 76% for the majority class. 


## Summary: 
- The worst thing a machine learning model could do within the context of predicting credit card risk, is classifying a borrower who is in actuality high-risk, as low-risk. This would indicate to the lender that the individual is not in danger of defaulting on their loan, probably causing them to lend out a larger amount than they should and losing that amout to a borrower who was actually at high-risk of defaulting. 
- In the paradigm established above, the precision score is generally uniform across the six models, probably owing to the very unbalanced datasets between high-risk and low-risk lenders. As a result, we may examine the recall score, which is the ability of the classifier to find all the positive samples. Since we would like to avoid the generation of false negatives for the minority class (the high-risk borrowers), which are indicated by a low recall recall score. 
- The highest recall scores are 72%, shared between the Naive Random Oversampling and the SMOTEEN combination sampling models. However, the Naive Random Oversampling method has a grater accuracy score of 67%, compared to 65% in the SMOTEEN model, as well as a greater recall score for the majority class as well at 62%, compared to 57% in the SMOTEEN model. 
- Therefore, Naive Random Oversampling is the best model for our purposes. 

