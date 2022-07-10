# Credit_Risk_Analysis

# Overview
The purpose of this analysis is to apply machine learning techniques to evaluate six models to predict credit risk.

# Results

The data was tested oversampled using RandomOverSampler and SMOTE algorithms, and undersampled using the ClusterCentroids algorithm. The SMOTEENN algorithm was used for a combination approach of oversampling and undersampling.

Finally, the BalancedRandomForestClassifier and EasyEnsembleClassifier models were used to reduce bias in predicting credit risk.

For the print out of the imbalanced classification report, stating both scores for high_risk and low_risk applicants:

    * pre = precision score

    * rec = recall score


## Balanced accuracy, precision, and recall scores of the six machine learning models

* ## Resampling models

* Naive Random Oversampling

![imbalanced classificaton report]()

        * The balanced accuracy score is 64.13%
        * The precision score
            high-risk = 1% : low-risk = 100%
        * the recall score 
            high-risk = 60% : low-risk = 68%

* SMOTE

![imbalanced classification report]()

        * The balanced accuracy score is 63.74%
        * The precision score
            high-risk = 1% : low-risk = 100%
        * the recall score 
            high-risk = 60% : low-risk = 68%

* ClusterCentroid

![imbalanced classification report]()

        * The balanced accuracy score is 52.92%
        * The precision score
            high-risk = 1% : low-risk = 100%
        * the recall score 
            high-risk = 61% : low-risk = 45%


* ## Combination approach, over-and-undersampling

* SMOTEENIN
       
![imbalanced classification report]()

        * The balanced accuracy score is 63.76%
        * The precision score
            high-risk = 1% : low-risk = 100%
        * the recall score 
            high-risk = 70% : low-risk = 57%

* ## Ensemble classifiers

* BalancedRandomForestClassifier

![imbalanced classification report]()

        * The balanced accuracy score is 78.78%
        * The precision score
            high-risk = 4% : low-risk = 100%
        * the recall score 
            high-risk = 67% : low-risk = 91%
    
* EasyEnsembleClassifier

![imbalanced classification report]()

        * The balanced accuracy score is 92.54%
        * The precision score
            high-risk = 7% : low-risk = 100%
        * the recall score 
            high-risk = 91% : low-risk = 94%



# Summary 


