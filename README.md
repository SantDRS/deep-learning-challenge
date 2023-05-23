# deep-learning-challenge

Name: Jose Santos
Date: May 23, 2023
Module 21 - Deep Learning Challenge

# Report on the Neural Network Model

### Deep Learning Charity Funding Outcome Predictor Project using hyper-tuned Neural Networks. 

## Overview:

This challenge takes charity funding applications for the nonprofit foundation Alphabet Soup and attempts to help select applicatnts for funding with the best opportunity for success in their ventures. 

Using machine learning, neural networks, and the features provided in the charity_data.csv dataset we attempt to reach 75% accuracy for the model. 

The dataset contains: 
* **EIN** and **NAME**—Identification columns
* **APPLICATION_TYPE**—Alphabet Soup application type
* **AFFILIATION**—Affiliated sector of industry
* **CLASSIFICATION**—Government organization classification
* **USE_CASE**—Use case for funding
* **ORGANIZATION**—Organization type
* **STATUS**—Active status
* **INCOME_AMT**—Income classification
* **SPECIAL_CONSIDERATIONS**—Special consideration for application
* **ASK_AMT**—Funding amount requested
* **IS_SUCCESSFUL**—Was the money used effectively


# Module Steps:

### 1: Data Preprocessing
* Review dataa for null and duplicated values

* **EIN** and **NAME**—Identification columns removed from the input data because they are neither targets nor features

* Cutoff point created to bin "rare" categorical variables together in a new value, `Other` for both `CLASSIFICATION` and `APPLICATION_TYPE`

* Converted categorical data to numeric with `pd.get_dummies`

* Split the preprocessed data into features and target arrays

* Split into training and tesing datasets

Target Variable: 
* **IS_SUCCESSFUL**

Feature Variables: 
* **APPLICATION_TYPE**
* **AFFILIATION**
* **CLASSIFICATION**
* **USE_CASE**
* **ORGANIZATION**
* **STATUS**
* **INCOME_AMT**
* **SPECIAL_CONSIDERATIONS**
* **ASK_AMT**

### 2: Compiling, Training, and Evaluating the Model

First model:

Second model:

Third model:


# Summary: 
The highest achieved prediction accuracy from model 2 was .7304 using three layers and 90, 60, 30 nodes respectively and 100 epochs. Surprisingly, model 2 outperformed my model 3 which was built off three layers and 1000, 750, 500 nodes respectively with 100 epochs. 

# Opportunity: 
I think the opportunity exists to run an automatically optimized model to achieve the minimum 75% requested accuracy. Simply changing the factors on our nn model didn't get us there.  