# Module 12 Report Template

## Overview of the Analysis
The purpose of this analysis is to train and evaluate a model based on loan risk.

The dataset contains information about historical lending activity from a peer-to-peer lending services company. The aim is to build a model that can identify the creditworthiness of borrowers. 
The model will learn from the variables: `loan_size`, `interest_rate`, `borrower_income`, `debt_to_income`, `num_accounts`, `derogatory_marks`, `total_debt` and `loan_status`. Afterwards, it will be tested to predict the variable `loan_status`, to find out if the borrower has a healthy loan (represented as 0), or a high-risk loan (represented as 1)

* Stages of this machine learning process: 
* Data was split into Training Set and Testing Set:
    - The .csv data from the Resources folder is read into Pandas DataFrame.
    - Create a set from `loan_status(y)` and create a `features(X)` DataFrame with the remaining columns.
    - Using the command `train_test_split`, split the data into Training and Testing Sets.
    
    
    
* A `LogisticRegression` model was created:
    - Fit the model using Training Set.
    - Score the model:
        > Training Data Score: 0.9921240885954051
    - Make predicitions using the Testing Set and the trained model
    - Score the model:
        > Testing Data Score: 0.9918489475856377  
        
* A confusion matrix is generated and the classification report for the model is printed:

    

## Results

* Machine Learning Model:
  * Accuracy: The model  , Precision, and Recall scores.



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
