!Azure Ml.jpg(https://www.bing.com/images/search?view=detailV2&ccid=FohcHpr9&id=319FAE3F68B52AC79C22F1F793740FDC1A80A88C&thid=OIP.FohcHpr9YtiH1Q1rRUV_eAHaH-&mediaurl=https%3a%2f%2fms-toolsai.gallerycdn.vsassets.io%2fextensions%2fms-toolsai%2fvscode-ai%2f0.6.11%2f1589227842242%2fMicrosoft.VisualStudio.Services.Icons.Default&cdnurl=https%3a%2f%2fth.bing.com%2fth%2fid%2fR.16885c1e9afd62d887d50d6b45457f78%3frik%3djKiAGtwPdJP38Q%26pid%3dImgRaw&exph=538&expw=500&q=Azure+Ml+Workspace+Icon&simid=608030647547276239&FORM=IRPRST&ck=748A6638B594BB1EFB4F1860F6B11550&selectedIndex=0&ajaxhist=0&ajaxserp=0)

# Optimizing an ML Pipeline in Azure

## Overview
This project is part of the Udacity Azure ML Nanodegree.
In this project, we build and optimize an Azure ML pipeline using the Python SDK and a provided Scikit-learn model.
This model is then compared to an Azure AutoML run.

## Summary
This dataset contains customer data that is going to be used to find the best strategies to improve for the next marketing campaign. The aim is to predict the effectiveness of the current marketing campaign.

The best performing model was a Logistic Regression model with the hyperparameters obtained from Hyperdrive.
## Scikit-learn Pipeline

The data is obtained from a csv file and converted to structured data using a dataframe. It was then cleaned and a OneHotEncoder technique from the sklearn library was implemented to label some features of the data. Once cleaned the data was split into a training set and test set, with the Logistic Regression model chosen as the classifier. The hyperparameters for this model were the Regularization Strength and Max iterations parameters, assisting in the convergence of the model. The best performance model had a regularization strength of 0.3711 and max iterations of 1000.

**Parameter sampler and stopping policy chosen**

The random parameter sampler was chosen based on its conservative usage to computing resources. The early stopping policy chosen was the Bandit policy 
to ensure that the experiments run within specific threshold. 

## AutoML

Using AutoML, the model of choice was the XGBoost classifier which is an optimized distributed gradient boosting library designed to be highly efficient, flexible and portable. For data transformation, AutoML used the SKLearn Sparse Normalizer

## Pipeline comparison

Training the model using a script and tuning the hyperparameters using HyperDrive, resulted in an accuracy of 0.9180 after 1 minutes 44 seconds
The Auto ML model produced an accuracy of 0.91563 within 29 seconds. The HyperDirve parameter optimizer performed with a higher accuracy but required more time and demanded a lot more iterations for tuning the hyperparameters.


## Future work
For the training model, the selcted model was a Logistic Regression model which performed well considering its accuracy. Alternative classification algorithms can also be considered especially those that require less time to process. Additionally, the training data could have benefited from being encoded using the One Hot Encoder library instead of manually performing the cleaning.

## Proof of cluster clean up
Delete method was used in code but will only occur once the script run is completed
