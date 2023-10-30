# deep-learning-challenge
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

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

# Report on Neural Network Model
Data Preprocessing
Target and Features
Target Variable: The target variable for the model is "IS_SUCCESSFUL," which indicates whether the funding was used effectively (1 for success, 0 for not successful).

Features: The features used for the model include several columns from the dataset, such as "APPLICATION_TYPE," "AFFILIATION," "CLASSIFICATION," "USE_CASE," "ORGANIZATION," "INCOME_AMT," "SPECIAL_CONSIDERATIONS," and "ASK_AMT."

Removed Variables
The following variables were removed from the input data as they are neither targets nor features:

"EIN" (Employer Identification Number): A unique identifier for each organization.
"NAME": The name of the organization.
"STATUS": The active status of the organization.

Compiling, Training, and Evaluating the Model
Model Architecture

Number of Input Features: Determined by the number of features after preprocessing.
First Hidden Layer: 512 neurons with ReLU activation function.
Second Hidden Layer: 256 neurons with ReLU activation function.
Output Layer: 1 neuron with sigmoid activation function for binary classification.
Provided a deep network capable of learning complex patterns in the data.

Model Performance
The initial model achieved an accuracy of approximately 0.7315 during training.
Steps to Increase Model Performance
To increase the model's performance:

Regularization: Dropout layers (dropout rate of 0.5) were added after each hidden layer to reduce overfitting.

Hyperparameter Tuning: Hyperparameter tuning was performed by adjusting the learning rate, batch size, and the number of epochs. Grid search and cross-validation were used to find the optimal hyperparameters.

Validation Set: A validation split of 20% was used during training to monitor the model's performance and apply early stopping.

Summary
The deep learning model achieved an accuracy of approximately 0.7315, which is a reasonable baseline performance, with 5 attempted iterations of optimization. However, it falls short of the target performance of higher than 75%.
