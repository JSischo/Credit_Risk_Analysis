# Credit_Risk_Analysis

## Overview of the Analysis
> The purpose of this project was to apply machine learning to solve a real-world challenge: credit card risk.

> Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, I needed to employ different techniques to train and evaluate models with unbalanced classes. Specifically, imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

> Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, I performed oversample of the data using the RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. Then, a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Finally, I was able to compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.


## Results
### Balanced Accuracy Score and the precision and recall scores

!['Naive Oversampling'](Resources/nos_as.png)!['SMOTE Oversampling'](Resources/smoteos_as.png)
* Analysis of the results for the Vine sub-set of reviews reveals:
  * n=170 reviews.
  * There were ***65*** **"5 star"** reviews.
  * Of all the reviews, ***38.24%*** were **"5 Star"**.

![](Resources/nonvine_star_count.png)![](Resources/nonvine_star_summary.png)
* Analysis of the results for the non-Vine sub-set of reviews reveals:
  * n=37840 reviews.
  * There were ***20,612*** **"5 star"** reviews.
  * Of all the reviews, ***54.47%*** were **"5 Star"**.
### Precision and Recall scores  

## Summary

