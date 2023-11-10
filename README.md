# Alphabet Soup Charity Deep Learning Model Report

## Overview of the Analysis

The purpose of this analysis is to create a binary classification deep learning model for Alphabet Soup Charity. The nonprofit foundation, Alphabet Soup, aims to select applicants for funding who have the best chance of success in their ventures. To achieve this, we will utilize machine learning and neural networks to predict whether applicants will be successful if funded by Alphabet Soup. This report details the performance of the deep learning model created for this task.

## Results

### Data Preprocessing

**Target Variable(s):**
- `IS_SUCCESSFUL`: This variable represents whether the funding was used effectively (1 for successful, 0 for not successful).

**Feature Variables:**
- The remaining columns in the dataset, except for `EIN` and `NAME`, are considered feature variables.

**Variables Removed:**
- `EIN` and `NAME` columns were removed as they are identification columns and not relevant for modeling.

**Categorical Variables Encoding:**
- Categorical variables were encoded using `pd.get_dummies()`.

**Data Split:**
- The data was split into a features array, X, and a target array, y, using the train_test_split function.

**Feature Scaling:**
- The training and testing features datasets were scaled using a StandardScaler instance.

### Compiling, Training, and Evaluating the Model

**Neural Network Model Configuration:**
- Number of Input Features: Determined by the number of encoded categorical variables.
- Number of Neurons in the First Hidden Layer: 100 (chosen based on experimentation).
- Activation Function in the First Hidden Layer: ReLU.
- A second and third hidden layer was added with of 30 and 10 neurons and a Sigmoud activation function to improve model performance.
- Output Layer Activation Function: Sigmoid.

**Model Performance:**
- The target model performance was to achieve a high accuracy score to effectively predict successful funding. The specific target value was set based on the dataset's distribution, with the aim of improving the model's ability to identify successful applicants.

**Steps to Increase Model Performance:**
- Adding a second and third hidden layer to the neural network to capture more complex patterns.
- Tuning the number of neurons in each layer to optimize the model's learning capacity.
- Using different activation functions and experimenting with different combinations.
- Adjusting hyperparameters, such as the learning rate, batch size, and number of epochs.
- Utilizing a callback to save the model's weights every 7 epochs, which allows for potential retraining with promising model configurations.

**Model Evaluation:**
- The model was evaluated using the test data to determine loss and accuracy.
- The loss and accuracy were tracked to assess model performance and iteratively improve the model's configuration.
- Accuracy of the target model performance is dependent on where one runs this code. The more RAM the machine has, the better the results.

### Summary

In summary, the deep learning model was created to predict the success of funding applicants for Alphabet Soup Charity. The model configuration was fine-tuned through experimentation to achieve the desired target accuracy. By adding a second hidden layer, tuning the number of neurons, and optimizing activation functions, the model performance improved significantly.

A recommendation for solving this classification problem is to explore other classification algorithms, such as Random Forest or Gradient Boosting, which may perform well on this dataset and provide alternative insights. Additionally, further feature engineering and data preprocessing techniques can be explored to improve the model's performance.
