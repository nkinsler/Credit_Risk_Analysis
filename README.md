# Credit_Risk_Analysis

## Overview of Analysis

The purpose of this analysis is to employ different techniques to train and evaluate models with unbalanced classes.  Using credit card dataset from LendingClub we will oversample the data using the RandomOverSampler and SMOTE algorithms and undersample the data using the ClusterCentroids algorithm.  Afterwards, we will use a combinational approach of over and under sampling using the SMOTEENN algorithm.

Two new machine learning models will be compared (BalancedRandomForestClassifer and EasyEmsembleClassifier) to predict credit risk.

## Results

[credit_risk_resampling.ipynb](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/credit_risk_resampling.ipynb)

[credit_risk_ensemble.ipynb](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/credit_risk_ensemble.ipynb)

### RandomOverSampler
 - Accuracy score = 0.65
 - Confusion matrix [70,31],[6711,10393]
  
 ![ROS_Confusion](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/ROS%20Confusion.png)!
  
 - Imbalanced classification report
  
 ![ROS_Class](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/ROS%20Classification.png)!
 
 - Precision = 0.01 for high risk loans and 1.00 for low risk loans.
 
 - Recall = 0.69 for high risk loans and 0.61 for low risk loans.
 
### SMOTE
 - Accuracy score = 0.66
 - Confusion matrix [64,37],[5291,11813]
  
 ![SMOTE_Confusion](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/SMOTE%20Confusion.png)!
  
 - Imbalanced classification report
  
 ![SMOTE_Class](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/SMOTE%20Class.png)!
 
 - Precision = 0.01 for high risk loans and 1.00 for low risk loans.
 
 - Recall = 0.63 for high risk loans and 0.69 for low risk loans.
  
### ClusterCentroids
 - Accuracy score = 0.66
 - Confusion matrix [69,32],[10075,7029]
  
 ![CC_Confusion](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/CC%20Confusion.png)!
  
 - Imbalanced classification report
  
 ![CC_Class](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/CC%20Classification.png)!
  
 - Precision = 0.01 for high risk loans and 1.00 for low risk loans.
 
 - Recall = 0.68 for high risk loans and 0.41 for low risk loans.
 
### SMOTEENN
 - Accuracy score = 0.55
 - Confusion matrix [73,28],[7412,9692]
  
 ![SMOTEENN_Confusion](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/SMOTEENN%20Confusion.png)!
  
 - Imbalanced classification report
  
 ![SMOTEENN_Class](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/SMOTEENN%20Class.png)!
 
 - Precision = 0.01 for high risk loans and 1.00 for low risk loans.
 
 - Recall = 0.72 for high risk loans and 0.57 for low risk loans.
 
### BalancedRandomForestClassifer
 - Accuracy score = 0.79
 - Confusion matrix [71,30],[2153,14951]
  
 ![Bal_Confusion](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/Bal%20Confusion.png)!
  
 - Imbalanced classification report
  
 ![Bal_Class](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/Bal%20Class.png)!
 
 - Precision = 0.03 for high risk loans and 1.00 for low risk loans.
 
 - Recall = 0.70 for high risk loans and 0.87 for low risk loans.
  
 - Features

 ![Features](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/Bal%20Features.png)!
  
### EasyEnsembleClassifier
 - Accuracy score = 0.93
 - Confusion matrix [93,8],[983,16121]
  
 ![Easy_Confusion](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/Easy%20Confusion.png)!
  
 - Imbalanced classification report
  
 ![Easy_Class](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/Easy%20Class.png)!
 
 - Precision = 0.09 for high risk loans and 1.00 for low risk loans.
 
 - Recall = 0.92 for high risk loans and 0.94 for low risk loans.

## Summary

Resampling was performed (as seen in the the first four parts of the Results section) using oversampling, undersampling, and a combination of both in order to determine which model would be best to utilize in predicting which loans are highest risks.  Of these methods, SMOTEENN produced the lowest accuracy at 0.55, while RandomOverSample produced an accuracy of 0.65 and SMOTE and ClusterCentroids produce accuracy of 0.66.  The last two resampling methods used ensemble classifers.  The BalanceRandomForestClassifer resulted in an accuracy score of 0.79 while the EasyEnsembleClassifier resulted in an accuracy score of 0.93.  The ensemble classifier methods produced better results in accuracy and pre, rec, and f1 scores.

The recommendation would be to use the EasyEnsembleClassifier to predict highest risk loans.  This method takes advantage of boosting to enhance the learning as shown in outcomes displayed in the classification report.  This methods has the best accuracy between the 6 methods tested at 0.93, the highest precision of the models at .09 (which is still not considered precise) for high risk loans and 1.00 for low risk scores.  This method also produced the best recall scores with 0.92 for high risk loans and 0.94 for low risk scores (which both are considered strong scores as they are very close to 1.00).

