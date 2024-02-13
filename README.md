# Alphabet Soup Funding Analysis: Enhancing Funding Selection with Machine Learning

## Purpose of the Analysis

  * The primary goal of this analysis is to empower Alphabet Soup, a nonprofit foundation, with a tool that can efficiently select funding applicants likely to succeed in their ventures. By leveraging machine learning techniques, the aim is to develop a binary classifier, capable of predicting the success of ventures funded by Alphabet Soup based on various features within the provided dataset.


* Information on the dataset
  * CSV contains more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

      EIN and NAME—Identification columns
      APPLICATION_TYPE—Alphabet Soup application type
      AFFILIATION—Affiliated sector of industry
      CLASSIFICATION—Government organization classification
      USE_CASE—Use case for funding
      ORGANIZATION—Organization type
      STATUS—Active status
      INCOME_AMT—Income classification
      SPECIAL_CONSIDERATIONS—Special considerations for application
      ASK_AMT—Funding amount requested
      IS_SUCCESSFUL—Was the money used effectively
 


## Results

* Data Preprocessing
    Identification columns, including EIN and NAME, were removed as they neither serve as targets nor features. The target variable, "IS_SUCCESSFUL," was selected, and features such as APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT were considered.

* Compiling, Training, and Evaluating the Model
  A neural network model with three layers, including 111 neurons, was compiled and trained. The activation functions used were ReLU for input and hidden layers, while the sigmoid function was employed for the output layer.
  
  The first attempt resulted in an accuracy of 72.96%.

  <img width="540" alt="image" src="https://github.com/vinaya-kusuma/deep-learning-challenge/assets/81578500/68023482-a4ae-4ec2-a491-71910e76ef0a">

  <img width="445" alt="image" src="https://github.com/vinaya-kusuma/deep-learning-challenge/assets/81578500/6fc20590-471b-41e0-8ea2-d0fd7cb428c0">


* Optimization
  With retaining the NAME column in the dataset resulted in an accuracy of 78.12%

  <img width="548" alt="image" src="https://github.com/vinaya-kusuma/deep-learning-challenge/assets/81578500/f4dbe5b4-e84c-41ce-8fa2-4530dd117687">

  <img width="429" alt="image" src="https://github.com/vinaya-kusuma/deep-learning-challenge/assets/81578500/da5da9a6-140e-4b5d-bad7-9a65a71734d0">
  

  ## Overall Summary

The model, with its current architecture and dataset modifications, demonstrates promise in predicting the success of funded ventures, achieving an accuracy of 78.12%. 

## Exploring Alternative Models

Considering the complexity of the problem, a Random Forest classifier could be a suitable alternative. Random Forests excel in handling diverse feature sets, managing overfitting, and providing interpretability. This model could complement neural networks, offering a different perspective on the dataset and potentially improving prediction accuracy.

In conclusion, while the neural network shows promise, exploring alternative models and implementing continuous improvements will enhance Alphabet Soup's ability to select successful funding applicants effectively.
