# Module 12 Report Template

## Overview of the Analysis
The purpose of this analysis is to train and evaluate a model based on loan risk.

The dataset contains information about historical lending activity from a peer-to-peer lending services company. The aim is to build a model that can identify the creditworthiness of borrowers. 
The model will learn from the variables: `loan_size`, `interest_rate`, `borrower_income`, `debt_to_income`, `num_accounts`, `derogatory_marks`, `total_debt` and `loan_status`. Afterward, it will be tested to predict the variable `loan_status`, to find out if the borrower has a healthy loan (represented as 0), or a high-risk loan (represented as 1)

* Stages of this machine learning process: 
* Data was split into Training Set and Testing Set:
    - The .csv data from the Resources folder is read into Pandas DataFrame.
    - Create a set from `loan_status(y)` and create a `features(X)` DataFrame with the remaining columns.
    - Using the command `train_test_split`, split the data into Training and Testing Sets.
     
* A `LogisticRegression` model was created:
    - Fit the model using Training Set.
    - Score the model:
        > Training Data Score: 0.9921240885954051
        
    - Make predictions using the Testing Set and the Trained model
    - Score the model:
        > Testing Data Score: 0.9918489475856377  
        
* A confusion matrix is generated and the classification report for the model is printed. 

## Results

* Machine Learning Model on the Training Set:
  * Accuracy: 99%
  * Precision: 100% for Class 0, 86% for Class 1.
  * Recall: 100% for Class 0, 90% for Class 1.
![training_report](https://github.com/lmacciomaretto/credit-risk-classification/assets/126762600/3e13df47-635d-448f-b86f-5b1b6ddb901c)

* Machine Learning Model on the Test Set:
  * Accuracy: 99%
  * Precision: 100% for Class 0, 85% for Class 1.
  * Recall: 99% for Class 0, 91% for Class 1.
![testing_report](https://github.com/lmacciomaretto/credit-risk-classification/assets/126762600/dc806911-1f6e-4fce-ba10-18ba74f2a0c4)

## Summary
Looking at the 2 classification reports, seems that the model performance declined just a little bit on the test data. This is not unexpected, however, precision and recall have not changed too much. 

I would recommend this model since it is very likely to perform well on unseen data. The performance will depend on the problem we are trying to solve. For example, if the lending company prioritizes precision in predicting the Healthy-Loan customers, this model will perform very well and predict 100% of those customers correctly.

In case the lending company absolutely wants to rule out the High-risk Loan Customers, this model will still perform very well, but there could be Class-Imbalance problems since there are very few cases of these compared to Healthy Loan customers. For the latter, it might be worth undersampling the Majority Class or oversampling the Minority Class in order to improve the scores.
