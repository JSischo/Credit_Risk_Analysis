# Credit_Risk_Analysis

## Overview of the Analysis
> The purpose of this project was to apply machine learning to solve a real-world challenge: credit card risk.

> Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, I needed to employ different techniques to train and evaluate models with unbalanced classes. Specifically, imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

> Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, I performed oversample of the data using the RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. Then, a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Finally, I was able to compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.


## Results
### Balanced Accuracy Score and the precision and recall scores

- ![](Resources/nos_as.png) 
  - ***Naive Oversampling***
- ![](Resources/smoteos_as.png)
  - ***SMOTE Oversampling***
- ![](Resources/us_as.png)
  - ***Undersampling***
- ![](Resources/combo_as.png)
  - ***Combination Sampling***
- ![](Resources/brf_as.png)
  - ***BRF Classifier***
- ![](Resources/eec_as.png)
  - ***Easy Ensemble Classifier***
#### Discussion
> The **accuracy** of a learning model is a measure of what percentage of the testing set the model predicted correctly. There does seem to be some variation in the accuracy score of the different models. In general, the Undersampling method seemed to perform the worst at only 56%, whereas the Oversampling and Combination methods seemed to perfrom slightly better at around 66-69%. When I utilized the ensemble models, Balanced Random Forest and Easy Ensemble Classifiers, the accuracy increased to 79% and 93% respectively. 

> So, it does seem that the ensemble methods ourperformed the over/under sampling models fairly signficantly with the Easy Ensemble Classified being the most accurate. 
  
### Precision and Recall scores  
- ![](Resources/nos_pr.png) 
  - ***Naive Oversampling***
- ![](Resources/smoteos_pr.png)
  - ***SMOTE Oversampling***
- ![](Resources/us_pr.png)
  - ***Undersampling***
- ![](Resources/combo_pr.png)
  - ***Combination Sampling***
- ![](Resources/brf_pr.png)
  - ***BRF Classifier***
- ![](Resources/eec_pr.png)
  - ***Easy Ensemble Classifier***
#### Discussion
> The **precision** of a model is a measure of the reliability of the model. In other words, how likely is a prediced result likely to be correct. In all the models that I utilized, none of them had a high precision for predicting high risk borrowers, ranging from .01 - .09%, with the EEC model being the highest. On the flip side, all models had excellent precision when looking at the low risk borrowers, with all of them having 100% precision. 

> The **recall** measure of a model, provides a measure of how well the model was able to accurately predict when a condition does or does not exist. So did it actually catch all of the high risk and low risk loan applicants in this case. Of extreme importance when assessing credit risk is a models ability to correctly identify the high risk applicants. We would like the measure of recall to be near 100%. For the models that I used, the over/under sampling models performed the worst in high risk recall at only between 65-67%. The BRF classifier was slightly better at 70%. The two best performing models were ther combination sampling and EEC models, measuring at 80% and 92% respectively.  

## Summary

Based on the accuracy scores of the different models, it seems that the EEC would be the model of choice given that it seemed to be able to predict at 93% whether or not a loan should be approved.

Precision and recall scores are a different animal altogether. None of the models seemed to do well in precision scores with the high risk classification. However, the precision scores for the high risk classification were very high in the combination and EEC models. When assessing these two measures, precision and recall, of machine learning models, it depends on the situation as to which score might be more important when choosing a model for your analysis. If this case, there is a high risk to a lender when then potential "miss" a high risk applicant that may eventually default on a loan. The lender will most likely want to value the recall score more thatn the precision in this case. It's better to detect everyone who might be a high risk, even if it means a certain number of low risk lenders might be included falsely in the high risk category, than to miss people who are high risk. The false positives in a highly sensitive test are accepted as a cost of doing business. Also, if the lender chooses to, since there are not many high risk applicants in this pool, they could further assess the high risk group to tease our those that maybe were falsley labeled as high risk.

**My recommendation based on this analysis would be that the ECC model is a very good model to use in this situation.**

