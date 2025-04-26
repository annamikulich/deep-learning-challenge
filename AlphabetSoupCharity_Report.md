## 1. Overview of the Analysis

The purpose of this analysis was to build, train, and evaluate a deep learning model that predicts whether an organization funded by Alphabet Soup will be successful or not.
We used historical data about organizations' applications to create a binary classification model based on their characteristics.

## 2. Results

** Data Preprocessing ** 
 # Target variable:
    IS_SUCCESSFUL (1 = successful, 0 = unsuccessful)
  # Feature variables:
    APPLICATION_TYPE
    AFFILIATION
    CLASSIFICATION
    USE_CASE
    ORGANIZATION
    STATUS
    INCOME_AMT
    SPECIAL_CONSIDERATIONS
    ASK_AMT
  # Variables removed:
    EIN (Employer Identification Number — not useful for prediction)
    NAME (Name of the organization — not useful for prediction)

** Compiling, Training, and Evaluating the Model ** 
  # Neurons, Layers, and Activation Functions:
    Initial models had two or three hidden layers.
    The first hidden layer had 128 neurons with relu activation.
    The second hidden layer had 64 neurons with relu activation.
    The third hidden layer (optional in some models) had 32 neurons with relu or tanh activation.
    The output layer had 1 neuron with a sigmoid activation function for binary classification.
  # Model performance:
    One of the models achieved over 75% accuracy on the test data.
  # Steps taken to increase model performance:
    Increased the number of neurons per layer.
    Added an additional hidden layer.
    Changed activation functions (tested both relu and tanh).
    Adjusted the number of epochs and batch sizes.
    Applied StandardScaler for feature scaling.
    Grouped rare categories into "Other" to reduce noise in input data.

## 3.Summary

The deep learning model successfully achieved the target accuracy of over 75%.
The optimizations, such as adjusting the neural network architecture and preprocessing the data carefully, helped improve performance.

Recommendation for future improvements:

Try using other classification models, such as a Random Forest Classifier or XGBoost, which often perform very well on tabular data.
These models can automatically handle categorical features, are less sensitive to scaling, and often achieve higher performance on structured datasets compared to deep learning models.
