# Credit_Risk_Analysis

# Overview
The purpose of this analysis is to apply machine learning techniques to evaluate six models to predict credit risk of loan applicants.

# Results

The data was tested oversampled using RandomOverSampler and SMOTE algorithms, and undersampled using the ClusterCentroids algorithm. The SMOTEENN algorithm was used for a combination approach of oversampling and undersampling.

Finally, the BalancedRandomForestClassifier and EasyEnsembleClassifier models were used to reduce bias in predicting credit risk.

For the print out of the imbalanced classification report, stating both scores for high_risk and low_risk applicants:

    - pre = precision score

    - rec = recall score


### Balanced accuracy, precision, and recall scores for the six machine learning models

## Resampling models

* Naive Random Oversampling

![imbalanced classificaton report](https://github.com/courtneysims/Credit_Risk_Analysis/blob/5742d0f33adc9e89ccd2946e71023de437665d2f/Resources/randomsampler_accuracy_tests.PNG)

        * The balanced accuracy score is 64.13%
        * The precision score
            high-risk = 1% : low-risk = 100%
        * The recall score 
            high-risk = 60% : low-risk = 68%

* SMOTE

![imbalanced classification report](https://github.com/courtneysims/Credit_Risk_Analysis/blob/5742d0f33adc9e89ccd2946e71023de437665d2f/Resources/SMOTE_accuracy_tests.PNG)

        * The balanced accuracy score is 63.74%
        * The precision score
            high-risk = 1% : low-risk = 100%
        * The recall score 
            high-risk = 60% : low-risk = 68%

* Cluster Centroid

![imbalanced classification report](https://github.com/courtneysims/Credit_Risk_Analysis/blob/5742d0f33adc9e89ccd2946e71023de437665d2f/Resources/cluster_accuracy_tests.PNG)

        * The balanced accuracy score is 52.93%
        * The precision score
            high-risk = 1% : low-risk = 100%
        * The recall score 
            high-risk = 61% : low-risk = 45%

 ### Combination approach, over-and-undersampling

* SMOTEENIN
       
![imbalanced classification report](https://github.com/courtneysims/Credit_Risk_Analysis/blob/5742d0f33adc9e89ccd2946e71023de437665d2f/Resources/SMOTEENIN_accuracy_tests.PNG)

        * The balanced accuracy score is 63.76%
        * The precision score
            high-risk = 1% : low-risk = 100%
        * The recall score 
            high-risk = 70% : low-risk = 57%

### Ensemble classifiers

* Balanced Random Forest

![imbalanced classification report](https://github.com/courtneysims/Credit_Risk_Analysis/blob/5742d0f33adc9e89ccd2946e71023de437665d2f/Resources/BalanceRandomForest_accuracy_tests.PNG)

        * The balanced accuracy score is 78.78%
        * The precision score
            high-risk = 4% : low-risk = 100%
        * The recall score 
            high-risk = 67% : low-risk = 91%
    
* Easy Ensemble 

![imbalanced classification report](https://github.com/courtneysims/Credit_Risk_Analysis/blob/5742d0f33adc9e89ccd2946e71023de437665d2f/Resources/easyEnsemblyClassifier_accuracy_tests.PNG)

        * The balanced accuracy score is 92.54%
        * The precision score
            high-risk = 7% : low-risk = 100%
        * the recall score 
            high-risk = 91% : low-risk = 94%
        



# Summary 

The precision score finds out what fraction of predicted positives is truly positive. For this analysis, the models had a low level of precision for detecting high risk loan applicants and a high level of precision for detecting low-risk loan applicants. This score is important when the costs of false positives is high.

Recall, or sensitivity, is a measure of the model's ability to detect the positives. Of the models, the Balance Random Forest, and easy ensemble classifer had the highest recall scores for high-risk, 67% and 91% respectively. This score is important when the cost of false negatives is high. 

Balanced accuracy is useful when the classes are imbalanced and is the mean of sensitivity and specificity ("true negative rate"). The easy ensemble model has the highest balanced accuracy score at 92.54%.


It is recommended that the Easy Ensemble Classifier model is used to evaluate credit risk of loan applicants. I believe a low precision score is not as crucial (predicted positive is true positive) as the model needs to have high sensitivity to detect possible applicants of high-risk to flag for investigation. The model's recall score is 91%, this means it has a high precentage ability to detect high-risk applicants. 
