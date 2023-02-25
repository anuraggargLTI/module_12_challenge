# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.  
      Credit risk poses a classification problem that’s inherently imbalanced. This is because healthy loans easily outnumber risky loans. In this Challenge, you’ll use various techniques to train and evaluate models with imbalanced classes. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers  
* Explain what financial information the data was on, and what you needed to predict.  
      Data was on all the basic questions that one has to answer to secure the loan like loan size , interest rate , amount of debt , income details etc. So it had all the basic parameters , I would further enhance the data to add age , kind of job , longevity in the job , kind of house(rental/own) data also captured  
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).  
      Variable as expected is loan status - healthy loan and high risky loan classified as class 0 and class 1 respectively  
* Describe the stages of the machine learning process you went through as part of this analysis.  
      Below are the basic steps of ML that analysis has to go through :  
      - segregating features from variables
      - get train and test data for features as well as variables  
      - have a regressional model fit on to the training data  
      - use same model to predict test data  
      - have the accuracy score , confusion matrix and classification report of test predicton and test original
      - now have an oversampling of the original data to remove the class imbalance
      - run the regression model on oversampled data 
      - run the model to predict original test data  
      - finally have the accuracy score , confusion matrix and classification report of test prediction of oversampled data with original test data

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
      Below are the methods used in the analysis:  
          - LogisticRegression()
          - RandomOverSampler()
          - balancedaccuracyscore()
          - classification_report()

         

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
    Model 1 Accuracy : 0.9520479254722232
                  pre       rec       spe        f1       geo       iba       sup

          0       1.00      0.99      0.91      1.00      0.95      0.91     18765
          1       0.85      0.91      0.99      0.88      0.95      0.90       619

        avg / total       0.99      0.99      0.91      0.99      0.95      0.91     19384


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
    Model 2 Accuracy : 0.9936781215845847
                  pre       rec       spe        f1       geo       iba       sup

          0       1.00      0.99      0.99      1.00      0.99      0.99     18765
          1       0.84      0.99      0.99      0.91      0.99      0.99       619

        avg / total       0.99      0.99      0.99      0.99      0.99      0.99     19384

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?  
  Oversampling modeling was better as evident from accuracy score and recall values shown above
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
  Its super important to predict True positive and False Negative so that '0's can be predicted . However True negative and False positive are more important to avoid '1's leakage  (especially the True Negatives)

If you do not recommend any of the models, please justify your reasoning.
