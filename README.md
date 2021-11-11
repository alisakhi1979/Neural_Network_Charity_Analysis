# Neural_Network_Charity_Analysis
Overview of the analysis: Explain the purpose of this analysis.

1) Purpose: 
Alphabet Soup is a donor agaency for funding projects. Due to the high volume of the applications, this organization has a challenge to predict whether an applicant for funding is successful or not. This project aims to utilize machine learning and neural networks to develop a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

2) Dataset:
From Alphabet Soup’s business team, we have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special consideration for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

3) Results:

A) Data Preprocessing:

Target Variable: "Is_Successful" column is the target variable in this analysis. it is a binary variable with 0 and 1 values.

Features in the model: All the following columns are taken into account as features for the predictive model:

APPLICATION_TYPE: Categorial feature that have been transformed with a cutoof count number at 500 to 9 categories.
AFFILIATION: Categorial feature with 6 categories
CLASSIFICATION: Categorial feature that have been transformed with a cutoof count number at 1500 to 6 categories.
USE_CASE: Categorial feature with 5 categories
ORGANIZATION: Categorial feature with 4 categories
STATUS:Categorial feature with 2 categories
INCOME_AMT: Categorial feature with 9 categories
SPECIAL_CONSIDERATIONS: Categorial feature with 2 categories

All the above variables are transformed to binary features using OneHotEncoder technique.

ASK_AMT: Contineouse variable 

Ommitted variables:
NAME: Applicant name
EIN: Applicant ID
* for optimization purposes two more variables were dropped i.e. STATUS and SPECIAL_CONSIDERATION

B) Compiling, Training, and Evaluating the Model:

First Model:
Utilized two hidden layers with 80 and 30 neourans and Rectified Linear Unit "relu" activation function. The output layer was assigne with Sigmoid function and the model run over 50 epoches.
Performance:
This model achieved accuracy at 0.7258 of testing dataset with loss of 0.5544.

C) Optimizing Model:

For optimization purposes two more variables i.e. "STATUS" and "Special Consideration" are ommitted from the data set and 3 models were developed to increase the performance.

First Attempt: adding one hidden layer and increasing neourans
Utilized three hidden layers with 100, 50 and 20 neourans and Rectified Linear Unit "relu" activation function. The output layer was assigne with Sigmoid function and the model run over 50 epoches.
Performance:
This model achieved accuracy at 0.7256 of testing dataset with loss of 0.5579.

Second Attempt: changing activation function
Utilized three hidden layers with 100, 50 and 20 neourans and Tanh activation function. The output layer was assigne with Sigmoid function and the model run over 50 epoches.
Performance:
This model achieved accuracy at 0.7258 of testing dataset with loss of 0.5575.

Third Attempt: increasing number of epoches to 100
Utilized three hidden layers with 100, 50 and 20 neourans and Tanh activation function. The output layer was assigne with Sigmoid function and the model run over 50 epoches.
Performance:
This model achieved accuracy at 0.7269 of testing dataset with loss of 0.5708.

Summary:
The predictive model using Neural Network deep learning in this project has achieved 72% accuracy. Three attempts to increase the performance of the model had a minor result in terms of increasing the accuracy rate. In this respect it is recommended to use Support Vector Machine algoihtm to evaluate whether a better result can be achieved. SVM is a binary classifier optimal for data that can be linearly seprable. The Alphabet Soup dataset is a good candidate for SVM analysis given the characterestics of the variables.  

