# Credit Risk Analysis

## Overview 
Based on data LoanStats_2019Q1.csv, various machine learning models are built to predict credit risk by evaluating strong and weak credit applications. 

The various methodologies used included:

- Oversampling the data using RandomOverSampler and SMOTE algorithms
- Undersampling the data using the ClusterCentroids algorithm
- Comparing two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier

The most suited machine learning model will then be used to help decide which applications Fast Lending should approve for loans and which one's they shouldn't. 

On the other hand, 1 represents the “good applications” or the loan applications that would be accepted.

## Results

The first model shows random oversampling on the original data. The results show a 66% accuracy score while recall (actual vs prediction) at 0.74 i.e. 74% of the time good applications were correctly identified. 

![](https://github.com/madihajaved/Credit_Risk_Analysis/blob/main/Images/1.png)

The second model is the SMOTE oversampling model which synthetically adds data points to balance minority and majority target classes. The accuracy score is 65% while recall drops to 62%.

![](https://github.com/madihajaved/Credit_Risk_Analysis/blob/main/Images/2.png)

The next one is undersampling which removes data points from the majority group to level it with the minority group. The accuracy drops further to 54% while recall for good applications is at 69% but more importantly for subpar applications, recall drops to 40%.

![](https://github.com/madihajaved/Credit_Risk_Analysis/blob/main/Images/3.png)


The SMOTEENN model combines undersampling and oversampling and has a 64% accuracy score. 

![](https://github.com/madihajaved/Credit_Risk_Analysis/blob/main/Images/4.png)


The Balanced Random Forest Classifier takes minority class and adds subsets of majority class and is  recreated for each decision tree. The accuracy increases to 79% with higher precision and recall scores as well. 

![](https://github.com/madihajaved/Credit_Risk_Analysis/blob/main/Images/5.png)

The final model used is Easy Ensemble AdaBoost Classifier. This has an advantage over Balanced Random Forest Classifier which is that each decision tree learns from the previous tree. This significantly increases accuracy score to 93% and also improves recall rates significantly. 

![](https://github.com/madihajaved/Credit_Risk_Analysis/blob/main/Images/6.png)
 

## Summary and Recommendation 
Of these six choices, the Easy Ensmble AdaBoost Classifier had the highest accuracy score and recall rates and would be the best to use. However, for credit card applications, high precision is important so perhaps testing and training for more data (beyond 1Q 2019) should increase its effectiveness. 