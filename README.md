# **Credit Risk Analysis**
## **Overview**
> Since credit risk is an unbalanced classification problem, to determine how risky certain loans are we must use different techniques to train and evaluate models with unbalanced classes. In this analysis we use imbalanced-learn and scikit-learn libraries to build and evaluate models for resampling.
Using the credit card [dataset](https://github.com/annaS000/Credit_Risk_Analysis/blob/main/linear_regression_salary/resources/LoanStats_2019Q1.csv) from the lending services company, LendingClub, we used RandomOverSampler and SMOTE algorithms to oversample the data, and ClusterCentroids to undersample the data. Then, we used a combination of over- and undersampling using SMOTEENN. Next, we compared BalancedRandomForestClassifier and EasyEnsembleClassifier, two methods that reduce bias, to predict credit risk.


---
## **Code**
[credit_risk_resampling.ipynb](https://github.com/annaS000/Credit_Risk_Analysis/blob/main/linear_regression_salary/credit_risk_resampling.ipynb)

[credit_risk_ensemble.ipynb](https://github.com/annaS000/Credit_Risk_Analysis/blob/main/linear_regression_salary/credit_risk_ensemble.ipynb)


---

## **Results**

### **1. Resampling Models**
#### **Oversampling**

* ##### **Naive Random Oversampling**
    ![](https://github.com/annaS000/Credit_Risk_Analysis/blob/main/images/random_oversample.png?raw=true)
    * Accuracy: 61.6%

        High Risk: 
        * Precision: 1%
        * Recall: 61%

        Low Risk:
        * Precision: 100%
        * Recall: 68%
        

* ##### **SMOTE Oversampling**
    ![](https://github.com/annaS000/Credit_Risk_Analysis/blob/main/images/SMOTE.png?raw=true)
    * Accuracy: 62.3%

        High Risk: 
        * Precision: 1%
        * Recall: 61%
        
        Low Risk:
        * Precision: 100%
        * Recall:  64%

#### **Undersampling**

* ##### **Cluster Centroids**
    ![](https://github.com/annaS000/Credit_Risk_Analysis/blob/main/images/clusters.png?raw=true)
    * Accuracy: 62.3%

        High Risk: 
        * Precision: 1% 
        * Recall: 57%
        
        Low Risk:
        * Precision: 100%
        * Recall:  45%


### **2. SMOTEENN Algorithm**

#### **Combination (Over and Under) Sampling**

* ##### **SMOTEENN**
    ![](https://github.com/annaS000/Credit_Risk_Analysis/blob/main/images/smote_enn.png?raw=true)
    * Accuracy: 61.6%

        High Risk: 
        * Precision: 1%
        * Recall: 69%
        
        Low Risk:
        * Precision: 100%
        * Recall:  54%

### **3. Ensemble Classifiers**

* ##### **Balanced Random Forest Classifier**
    ![](https://github.com/annaS000/Credit_Risk_Analysis/blob/main/images/RFC.png?raw=true)
    * Accuracy: 78.8%

        High Risk: 
        * Precision: 4%
        * Recall: 67%
        
        Low Risk:
        * Precision: 100%
        * Recall: 91%

* ##### **Easy Ensemble Classifier**
    ![](https://github.com/annaS000/Credit_Risk_Analysis/blob/main/images/easy.png?raw=true)
    * Accuracy: 93.2%

        High Risk: 
        * Precision: 4%
        * Recall: 67%
        
        Low Risk:
        * Precision: 100%
        * Recall:  91%

---

## **Summary**

Of all the machine learning algorithms, the Balanced Random Forest Classifier and Easy Ensemble Classifier methods produced the highest level accuracy as well as having high recall percentages. I believe this is due to the reduction in bias that these methods provide. Therefore, I would recommend this model for determining credit risk. Additionally, I would not recommend the Cluster Centroids algorithm since it produced the lowest recall scores and did not have a strong accuracy score either.



