# MLP GDP Prediction Model

This repository contains a Jupyter Notebook that demonstrates how to use a MLP model to predict GDP (Gross Domestic Product) values for a given country. The MLP model is implemented using the TensorFlow Keras library, and the data is prepared using Pandas and scikit-learn.

## Prerequisites

1. **Python:** The code requires Python programming language to be installed on your system.
2. **Libraries:** The following Python libraries should be installed - pandas, scikit-learn, tensorflow.


## Prerequisites

- pip install -r requirements.txt


- Load Data: The code loads yearly time series GDP data from the 'merged_data.csv' file using Pandas. Make sure you have the 'merged_data.csv' file in the same directory as the notebook.

- Sort Data: The data is sorted in ascending order based on the 'Year' column using the 'sort_values' function.

Prepare MLP Input: The 'create_sequences' function is used to create input sequences and labels for each column. The window size for the MLP model is defined as 'window_length'. The function converts the data into sequences of 'window_length' time steps, where each sequence corresponds to a specific label.

- Normalize Data: The input sequences and labels are normalized using Min-Max scaling to ensure that all values are in the range [0, 1].

- Model Training
Split Data: The data is split into training and testing sets using the 'train_test_split' function from scikit-learn.

- MLP Model: A sequential model with an MLP layer and a Dense layer is created using the TensorFlow Keras library. The model is compiled with the 'mean_squared_error' loss function and 'adam' optimizer.

- MLPRegressor: Additionally, an MLPRegressor model from scikit-learn is used as a comparison for prediction.

- Train the Model: The MLP model is trained on the training data for 100 epochs with a batch size of 32. A validation split of 0.1 is used during training.

- Evaluation
Mean Squared Error: The Mean Squared Error (MSE) is calculated to evaluate the performance of the MLP model on the test data. 

- Prediction for Canada: The MLP model is used to predict GDP values for Canada. The input sequences are created for Canada's GDP data, and the MLPRegressor model is used for prediction.(MSE=0.0004)

- Visualization: The original and predicted GDP values for Canada are visualized using matplotlib.

** Additional Notes **
The code uses a fixed window size ('window_length') for the MLP model. You can experiment with different window sizes to see how it affects the model's performance.

If you want to use data for other countries, ensure that you have the corresponding GDP data in the 'merged_data.csv' file or update the code to load data from a different CSV file.

This code provides a basic implementation of MLP for GDP prediction. For real-world applications, consider further optimizations, hyperparameter tuning, and more sophisticated MLP architectures.