# Credit_Risk_Analysis

## Overview of Analysis

The purpose of this analysis is to employ different techniques to train and evaluate models with unbalanced classes.  Using credit card dataset from LendingClub we will oversample the data using the RandomOverSampler and SMOTE algorithms and undersample the data using the ClusterCentroids alogrithm.  Afterwards, we will use a combinational approach of over and under sampling using the SMOTEENN algorithm.

Two new machine learning models will be compared (BalancedRandomForestClassifer and EasyEmsembleClassifier) to predict credit risk.

## Results

[credit_risk_resampling.ipynb]()

[credit_risk_ensemble.ipynb]()

- RandomOverSampler
  - Accruacy score = 0.65
  - Confusion matrix [70,31],[6711,10393]
  
  ![ROS_Confusion]()!
  
  - Imbalanced classification report
  
  ![ROS_Class]()!
  
-SMOTE
  - Accruacy score = 0.66
  - Confusion matrix [64,37],[5291,11813]
  
  ![SMOTE_Confusion]()!
  
  - Imbalanced classification report
  
  ![SMOTE_Class]()!
  
-ClusterCentroids
  - Accruacy score = 0.66
  - Confusion matrix [69,32],[10075,7029]
  
  ![CC_Confusion]()!
  
  - Imbalanced classification report
  
  ![CC_Class]()!
  
-SMOTEENN
  - Accruacy score = 0.55
  - Confusion matrix [73,28],[7412,9692]
  
  ![SMOTEENN_Confusion]()!
  
  - Imbalanced classification report
  
  ![SMOTEENN_Class]()!
  
-BalancedRandomForestClassifer
  - Accruacy score
  - Confusion matrix
  
  ![Bal_Confusion]()!
  
  - Imbalanced classification report
  
  ![Bal_Class]()!
  
  - Features
-EasyEmsembleClassifier
  - Accruacy score
  - Confusion matrix
  
  ![Easy_Confusion]()!
  
  - Imbalanced classification report
  
  ![Easy_Class]()!
  

## Summary
