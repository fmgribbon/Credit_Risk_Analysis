# Credit Risk Analysis

## Purpose 
The purpose of this study is to evaluate the performance of different machine learning models used for unbalanced classes and make recommendations on the models to predict credit risk.       
    
The outcome of credit risk prediction essentially contains an unbalanced class. In this study, to resolve class imbalance,  the  over sampling RandomOverSampler and SMOTE algorithms, under sampling Cluster Centroids algorithm and combination sampling SMOTEENN algorithm were evaluated.  The output of each sampling algorithms is used in the logistic regression model to predict credit risk.
    
Also, the ensemble classifiers Balanced Random Forest and Easy  Ensemble AdaBoost model performance are evaluated to predict credit risk. 
  

## Results
### Naive Random Oversampling

![alt tag]( https://github.com/fmgribbon/Credit_Risk_Analysis/blob/main/Resources/randomOverSample__bal_accuracy_score.PNG)
- Balance Accuracy: 65%

![alt tag]( https://github.com/fmgribbon/Credit_Risk_Analysis/blob/main/Resources/naive_random_oversample_classification_imbalance_rpt.PNG)
- Precision: High-risk – 0.01	Low-risk –  1.0
- Recall: High-risk – 0.69	Low-risk – 0.62
### SMOTE Oversampling 

![alt tag]( https://github.com/fmgribbon/Credit_Risk_Analysis/blob/main/Resources/SMOTE_bal_accuracy_score.PNG)

- Balance Accuracy: 66%

![alt tag]( https://github.com/fmgribbon/Credit_Risk_Analysis/blob/main/Resources/smote_imbalance_classification_report.PNG)

- Precision: High-risk – 0.01	Low-risk –  1.0
- Recall: High-risk – 0.63	Low-risk – 0.69
### Undersampling Cluster Centroids
![alt tag]( https://github.com/fmgribbon/Credit_Risk_Analysis/blob/main/Resources/cluster_centroids_bal_accuracy_score.PNG)
- Balance Accuracy: 54%

![alt tag]( https://github.com/fmgribbon/Credit_Risk_Analysis/blob/main/Resources/cluster_centroids_imbalance_classification_report.PNG)

- Precision: High-risk – 0.01	Low-risk –  1.0
- Recall: High-risk – 0.69	Low-risk – 0.39

### Combination (Over and Under) Sampling SMOTEENN
![alt tag]( https://github.com/fmgribbon/Credit_Risk_Analysis/blob/main/Resources/SMOTEENN_bal_accuracy_score.PNG)

- Balance Accuracy: 65%

![alt tag]( https://github.com/fmgribbon/Credit_Risk_Analysis/blob/main/Resources/SMOTEENN_imbalance_classification_report.PNG)

- Precision: High-risk – 0.01	Low-risk –  1.0
- Recall: High-risk – 0.71	Low-risk – 0.58

### Balanced Random Forest Classification

![alt tag]( https://github.com/fmgribbon/Credit_Risk_Analysis/blob/main/Resources/b_random_forest_bal_accuracy_score.PNG)

- Balance Accuracy: 79%

![alt tag]( https://github.com/fmgribbon/Credit_Risk_Analysis/blob/main/Resources/b_random_forest_imbalance_classification_report.PNG)

- Precision: High-risk – 0.03	Low-risk –  1.0
- Recall: High-risk – 0.70	Low-risk – 0.87



### Easy Classification

![alt tag]( https://github.com/fmgribbon/Credit_Risk_Analysis/blob/main/Resources/easycl_classification_bal_accuracy_score.PNG)

- Balance Accuracy: 93%

![alt tag]( https://github.com/fmgribbon/Credit_Risk_Analysis/blob/main/Resources/easycl_imbalance_classification_report.PNG)

- Precision: High-risk – 0.09	Low-risk –  1.0
- Recall: High-risk – 0.92	Low-risk – 0.94


## Summary
### Model Performance Score 
#### Resampling Summary based on the imbalanced classification reports.

![alt tag]( https://github.com/fmgribbon/Credit_Risk_Analysis/blob/main/Resources/summary_sampling_matrices.PNG)

- SMOTE has the highest balanced accuracy score, recall and F1 average score. This model performed the better than the combined(under and over) resampling SMOTEENN algorithm.  
- Cluster Centroids has the lowest balanced accuracy score, recall and F1 average score.

- Naive Random Oversampling, SMOTE, Cluster Centroids, SMOTEENN all have the same precision average score.

#### Comparing Ensemble Learning and Logistic Regression Model using resampled data.

![alt tag]( https://github.com/fmgribbon/Credit_Risk_Analysis/blob/main/Resources/summary_ensemble_matrices.PNG)

  - The balance accuracy of both Balanced Random Classifier and Easy Ensemble Ada Booster Classifier outperformed the 4 resampling models. 
  - The Easy Ensemble Ada Booster Classifier has the highest balanced accuracy score, recall and F1 average score. This model performed the best of all the 6 models evaluated. 

Based on the results of the evaluation of the 6 models used to predict credit risk, the models could not be used to predict high-risk outcome due to low recall score. The high F1 scores of the models could be attributed to the imbalance class that exist in the dataset. Predicting Credit risk is high risk. I recommend that further study needs to be undertaken to increase the credit risk prediction accuracy.   


