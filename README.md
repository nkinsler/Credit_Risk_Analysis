# Credit_Risk_Analysis

## Overview of Analysis

The purpose of this analysis is to employ different techniques to train and evaluate models with unbalanced classes.  Using credit card dataset from LendingClub we will oversample the data using the RandomOverSampler and SMOTE algorithms and undersample the data using the ClusterCentroids alogrithm.  Afterwards, we will use a combinational approach of over and under sampling using the SMOTEENN algorithm.

Two new machine learning models will be compared (BalancedRandomForestClassifer and EasyEmsembleClassifier) to predict credit risk.

## Results

[credit_risk_resampling.ipynb](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/credit_risk_resampling.ipynb)

[credit_risk_ensemble.ipynb](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/credit_risk_ensemble.ipynb)

### RandomOverSampler
 - Accruacy score = 0.65
 - Confusion matrix [70,31],[6711,10393]
  
 ![ROS_Confusion](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/ROS%20Confusion.png)!
  
 - Imbalanced classification report
  
 ![ROS_Class](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/ROS%20Classification.png)!
  
### SMOTE
 - Accruacy score = 0.66
 - Confusion matrix [64,37],[5291,11813]
  
 ![SMOTE_Confusion](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/SMOTE%20Confusion.png)!
  
 - Imbalanced classification report
  
 ![SMOTE_Class](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/SMOTE%20Class.png)!
  
### ClusterCentroids
 - Accruacy score = 0.66
 - Confusion matrix [69,32],[10075,7029]
  
 ![CC_Confusion](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/CC%20Confusion.png)!
  
 - Imbalanced classification report
  
 ![CC_Class](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/CC%20Classification.png)!
  
### SMOTEENN
 - Accruacy score = 0.55
 - Confusion matrix [73,28],[7412,9692]
  
 ![SMOTEENN_Confusion](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/SMOTE%20Confusion.png)!
  
 - Imbalanced classification report
  
 ![SMOTEENN_Class](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/SMOTEENN%20Class.png)!
  
### BalancedRandomForestClassifer
 - Accruacy score = 0.79
 - Confusion matrix [71,30],[2153,14951]
  
 ![Bal_Confusion](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/Bal%20Confusion.png)!
  
 - Imbalanced classification report
  
 ![Bal_Class](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/Bal%20Class.png)!
  
 - Features

 ![Features](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/Bal%20Features.png)!
  
### EasyEmsembleClassifier
 - Accruacy score = 0.93
 - Confusion matrix [93,8],[983,16121]
  
 ![Easy_Confusion](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/Easy%20Confusion.png)!
  
 - Imbalanced classification report
  
 ![Easy_Class](https://github.com/nkinsler/Credit_Risk_Analysis/blob/main/Resources/Easy%20Class.png)!
  

## Summary
