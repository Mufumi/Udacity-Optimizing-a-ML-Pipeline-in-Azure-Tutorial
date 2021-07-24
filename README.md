# Optimizing an ML Pipeline in Azure

## Overview
This project is part of the Udacity Azure ML Nanodegree.
In this project, we build and optimize an Azure ML pipeline using the Python SDK and a provided Scikit-learn model.
This model is then compared to an Azure AutoML run.

## Summary
This dataset contains customer data that is going to be used to find the best strategies to improve for the next marketing campaign. The aim is to predict the effectiveness of the current marketing campaign.

The best performing model was a ..... 
## Scikit-learn Pipeline

**Explain the pipeline architecture, including data, hyperparameter tuning, and classification algorithm.**
Sklearn library

The data is obtained from a csv file and converted to structured data using a dataframe.
Hyperparamter tuning - data transformation -> one hot encoder
classification algorithm - Logistic regression 

**Parameter sampler and stopping policy chosen**

The random parameter sampler was chosen based on its conservative usage to computing resources. The early stopping policy chosen was the Bandit policy 
to ensure that the experiments run within specific threshold. 

## AutoML

Using AutoML, the model of choice was the XGBoost classifier which is an optimized distributed gradient boosting library designed to be highly efficient, flexible and portable. For data transformation, AutoML used the SKLearn Sparse Normalizer

## Pipeline comparison
**Compare the two models and their performance. What are the differences in accuracy? In architecture? If there was a difference, why do you think there was one?**
HyperDrive = 
Auto ML - Accuracy = 0.91563


## Future work
**What are some areas of improvement for future experiments? Why might these improvements help the model?**

## Proof of cluster clean up
**If you did not delete your compute cluster in the code, please complete this section. Otherwise, delete this section.**
**Image of cluster marked for deletion**
