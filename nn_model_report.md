# Neural Network Model Report

## Overview

* The purpose of this analysis is to build a tool that can help nonprofit foundation Alphabet Soup select applicants for funding with the best chance of success in their ventures. This was done using the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.
* The data received from the business team is a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:
    * EIN and NAME—Identification columns
    * APPLICATION_TYPE—Alphabet Soup application type
    * AFFILIATION—Affiliated sector of industry
    * CLASSIFICATION—Government organization classification
    * USE_CASE—Use case for funding
    * ORGANIZATION—Organization type
    * STATUS—Active status
    * INCOME_AMT—Income classification
    * SPECIAL_CONSIDERATIONS—Special considerations for application
    * ASK_AMT—Funding amount requested
    * IS_SUCCESSFUL—Was the money used effectively

## Results

* Data Preprocessing
    * "IS_SUCCESFUL" serves as our target variable for the neural network model. The remaining columns in the dataset serve as the features. The EIN and NAME identification columns are neither targe nor features and were dropped from the dataset.
* Compiling, Training, and Evaluating the Model
    * The initial model included 2 hidden layers with 80 neurons in the first layer and 30 neurons in the second layer. The rectified linear unit (ReLU) activation function was used for the hidden layers and the sigmoid function was used for the output layer. We used 100 epochs to train the model. These variables were selected in an attempt to appropriately fit the model with minimal computational resources required. The model accuracy of 72.85% did not achieve target accuracy of 75%.
    * We used the following methods to optimize the model:
      1. Increased the number of CLASSIFICATION bins by decreasing the cutoff value from 1500 to 100
      2. Increased the number of hidden layers from 2 to 4
      3. Added more neurons to the hidden layers
      4. Used the Sigmoid activation function for the hidden layers (also tried tanh)
   * Despite the changes to the variables, the model accuracy was 72.86%, still below the target of at least 75%.
       
## Summary
We were unable to optimize a neural network model to achieve higher than 75% accuracy. Additional preprocessing to clarify variables and/or capture outliers is necessary to improve model performance. We might also consider a Random Forest model since Random Forests are less influenced by outliers than other algorithms.


