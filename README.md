# credit-card-fraud-detection


## Project Intro/Objective
The purpose of this project is to predict whether the transaction is normal or fraud. 

### Methods Used
* Statistics
* Machine Learning
* Data Visualization
* Predictive Modeling

### Technologies
* Python
* Pandas,Numpy, Scikit-learn, jupyter
 

## Project Description
This is a binary classification problem, where the dataset consists of imbalanced target class. So there are 2 notebooks uploaded to repo where one of the notebooks includes predictive model results with imbalanced dataset and other with balanced dataset(using ADASYN). The aim is to correctly classify the transactions respectively. 

## Note:-
We will use ADASYN after train test split as we need to make sure there is no leakage of data which will lead to overfitting.

## Models used

- Random Forest Classifier
- Logistic Regression

## Metrics used for evaluation of models
Here we cannot completely depend on accuracy alone because its imbalanced dataset. Other metrics used are as follows

- Accuracy
- Confusion Matrix
- Precision Score
- Recall Score 
- F-beta Score

## Metric Importance
- Though we have to focus on reducing FN/recall i.e. fraud transaction being classified as normal transaction. Our majority of transactions are of normal type and we need to make sure people don't get charged for the fraud transaction. 

- So we should select a metric which will give both precision and recall equal importance which is F1 score or F-beta which beta = 1. It depends on the use case, whether to give importance to precision or recall and if we want to consider both then we can use the f-beta score with b = 1. With b = 0.5 higher weightage will be given to precision considering both recall and precision and with b = 2 higher weightage is given to recall considering both precision and recall. 

- Discussing the results with the domain expert is important as he will decide or direct on to which metric is more important(recall or precision).

If results from both the files are compared we can see in the imbalanced notebook the model is somewhat biased to predicting the majority of the class i.e. normal. In the next file we can see that the results of the best ML model are impressive where ADASYN is used to deal with the Imbalanced class.
To study more about ADASYN [click here](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.ADASYN.html)
 
