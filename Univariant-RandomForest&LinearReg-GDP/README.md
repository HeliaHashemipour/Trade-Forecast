### README univariate
This repository contains code for predicting GDP using a Random Forest model and a Linear Regression model. The predictions are made for multiple countries using historical GDP data.

** Getting Started **
- pip install -r requirements.txt

Download the historical GDP data for each country in CSV format and save them in the same directory as this notebook. The CSV files should have a column named 'Year' representing the year and a column named 'GDP' representing the Gross Domestic Product.
How the Code Works
The code reads all CSV files in the current directory that end with '_gdp_data.csv' and loads them into separate DataFrames for each country.

For each country, the code performs the following steps:

a. Preprocess the data: The 'Year' column is converted to a datetime type and set as the index. The 'GDP' column is used as the target variable, and the last 6 years' GDP values are used as the prediction target.

b. Normalize the data: The feature and target variables are normalized using Min-Max scaling.

c. Split the data: The data is split into training and testing sets.

d. Train and evaluate the Random Forest model: A Random Forest regressor with 100 estimators is trained using the training data. The model's predictions are evaluated using Mean Absolute Error (MAE) and Mean Squared Error (MSE).

e. Train and evaluate the Linear Regression model: A Linear Regression model is trained using the training data. The model's predictions are evaluated using MAE, MSE, and Mean Absolute Percentage Error (MAPE).

f. Save predictions and evaluation metrics: The predictions and evaluation metrics for both models are saved in separate CSV files.

g. Generate forecast: The Linear Regression model is used to forecast the GDP for the next 6 years, and the results are saved in a CSV file.

h. Plot predictions: Plots are generated to visualize the true GDP values and the predictions made by the Random Forest and Linear Regression models.

After processing all countries, the code calculates the average MSE for both models and prints the results.

** Note **
Ensure that the 'Year' column in the CSV files contains the year information in a valid format.

The code assumes that the 'GDP' column in the CSV files represents the target variable.

The code uses Min-Max scaling to normalize the data. If you want to try other scaling methods, modify the code accordingly.

Make sure you have the required data and appropriate CSV files in the same directory as this notebook before running the code.