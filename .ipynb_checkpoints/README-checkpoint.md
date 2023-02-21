# Credit-Risk-Classification

![Image](image.png)

## Overview of the Analysis


The purpose of this analysis is to identify whether a logistic regression model can correctly classify healthy-loans and high-risk loans in a data set. Credit risk poses a classification problem that’s inherently imbalanced. Analysing the data will help us understand if logistic regression is the right tool to use in a credit risk classification.

--- 

The information was based on historical lending data from peer-to-peer lending services which included : Loan-size, interest rate, the borrowers income, debt to income, how many loans, derogatories, total debt and loan status.

For this analysis, I used the sample data provided to train and test the model and assess if it can correctly classify the loans and have an accurate predicted outcome.The loan status was used as the classification meaning healthy or high-risk loan.  All the other data was used to make the prediction.


The value count from original data contains 75036 healthy loans and 2500 high-risk loans.


## Stages of the machine learning process
I split the data into training and testing datasets which I used to fit into the model and make the prediction

The results show that the model has 95% balanced accuracy meaning for each classification, the average accuracy was 95%.

To validate the results of the model, I used a confusion matrix which analyses the results of the logistic regression model and determines the accuracy of the results.

Results from the confusion matrix indicate that using the original data, the logistic regression model was able to correctly classify 18663 as healthy loans out of the 18765 loans from the testing data set.
When it comes to high-risk loans, the model predicted 563 as high-risk out of the 619 high risk loans. 
102 healthy loans were classified as high-risk and 56 high-risk loans were classified as healthy loans. 

To improve chances of getting better classification. The data was resampled using the RandomOverSampler module. 

After fitting the original data into RandomOverSampler module,
The value count of the health-loans and high-risk loans evened out at 56271 each and balanced accuracy went up to 99%

I made a prediction with the resampled data and ran a confusion matrix to validate the results. 

## Results
The results show an improvement in predicting high-risk loans with the number of correctly predicted loans up to 615 as opposed to 563 from the original data. Only 4 high-risk loans were incorrectly identified. 
Results using resampled data show a decline in healthy loan classification with the number of correctly identified healthy-loans dropping from 18663 to 18649. 




---

## Machine Learning Model 1:
* LogisticRegression model has 95% balanced accuracy which is the average percentage of accuracy it used to predict each classification
* Precision was 100% for healthy loans and 85% for high-risk loans. This is the percentage representation of the accuracy of the model classification.
* Recall was 99% for healthy loans and 99% for high-risk loans. This is a percentage representation of how many times the model made the classification. 
  

---

## Machine Learning Model 2:
 * RandomOverSampler module has 99% balanced accuracy which is the average percentage of accuracy it used to predict each classification
 * Precision was 100% for healthy loans and 84% for high-risk loans. This is the percentage representation of the accuracy of the model classification.
* Recall was 99% for healthy loans and 99% for high-risk loans. This is a percentage representation of how many times the model made the classification. 
  

## Summary

Much as the resampled data did not make a high number of correct predictions when it came to healthy loans, It did well with the high-risk loans compared to results derived from testing the original data and I would recommend using it for predictions. 
Recognizing that no given model comes with 100% accuracy, the data provided also plays a role in how accurately the model can make the predictions. 
The RandomOverSampler module provides the best outcome from the data given the unbalanced data that had more healthy-loans than high-risk loans.
When it comes to loans, being able to identify high-risk loans with more precision is beneficial and more advantageous as this reduces the risk for both the lender and the borrower. 
