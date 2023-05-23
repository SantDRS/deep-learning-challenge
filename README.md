# deep-learning-challenge

#### Name: Jose Santos
#### Date: May 23, 2023
#### Module 21 - Deep Learning Challenge

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


## Module Steps:

### 1: Data Preprocessing
* Review data for null and duplicated values

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

## 2: Compiling, Training, and Evaluating the Model

### First model:

![Screenshot 2023-05-22 at 11 02 00 PM](https://github.com/SantDRS/deep-learning-challenge/assets/43708777/e00179a4-e619-4c36-8894-77d15945a979)
![Screenshot 2023-05-22 at 11 15 46 PM](https://github.com/SantDRS/deep-learning-challenge/assets/43708777/4fe0565e-6244-4316-bad5-37804393feae)
![Screenshot 2023-05-22 at 11 16 17 PM](https://github.com/SantDRS/deep-learning-challenge/assets/43708777/b907f444-5d6e-4645-9a48-f284401e103f)
![Screenshot 2023-05-22 at 11 16 48 PM](https://github.com/SantDRS/deep-learning-challenge/assets/43708777/e1bcc711-63d4-4eca-b939-cc4f7e7536e7)
Accuracy: 0.7278134226799011

### Second model:

![Screenshot 2023-05-22 at 11 08 17 PM](https://github.com/SantDRS/deep-learning-challenge/assets/43708777/5ce45a1d-3bec-4a93-a142-ed34d792e4ce)
![Screenshot 2023-05-22 at 11 13 42 PM](https://github.com/SantDRS/deep-learning-challenge/assets/43708777/f0ae4eba-2a57-44e4-9c90-dcd33d8f1835)
![Screenshot 2023-05-22 at 11 14 15 PM](https://github.com/SantDRS/deep-learning-challenge/assets/43708777/f2675ca2-7601-42a7-9e55-828425e19080)
![Screenshot 2023-05-22 at 11 14 58 PM](https://github.com/SantDRS/deep-learning-challenge/assets/43708777/0806809f-0f2d-4753-8717-a69f0a669283)
Accuracy: 0.7303789854049683

### Third model:

![Screenshot 2023-05-22 at 11 09 09 PM](https://github.com/SantDRS/deep-learning-challenge/assets/43708777/4eff3793-b044-4e3f-bce8-c9526528a1fb)
![Screenshot 2023-05-22 at 11 10 28 PM](https://github.com/SantDRS/deep-learning-challenge/assets/43708777/985dc7c1-b546-4c1c-ab62-112e0e5ad9d3)
![Screenshot 2023-05-22 at 11 11 29 PM](https://github.com/SantDRS/deep-learning-challenge/assets/43708777/caf5a6ef-4158-4c9d-af22-bcd61b3344e8)
![Screenshot 2023-05-22 at 11 12 50 PM](https://github.com/SantDRS/deep-learning-challenge/assets/43708777/3e4d54c7-af48-446c-9597-bc44601f5358)
Accuracy: 0.7257142663002014

## Summary: 
The highest achieved prediction accuracy from model 2 was .7304 using three layers and 90, 60, 30 nodes respectively and 100 epochs. Surprisingly, model 2 outperformed my model 3 which was built off three layers and 1000, 750, 500 nodes respectively with 100 epochs. 

## Opportunity: 
I think the opportunity exists to run an automatically optimized model to achieve the minimum 75% requested accuracy. Simply changing the factors on our nn model didn't get us there.  
