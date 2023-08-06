# README for GDP Forecasting with ARIMA Models
This code is an example of using ARIMA (AutoRegressive Integrated Moving Average) models for forecasting GDP (Gross Domestic Product) data for different countries. The data used in this code is assumed to be in CSV format, where each file contains GDP data for a specific country.

## Prerequisites
- pip install -r requirements.txt

- Ensure that you have the CSV files containing GDP data for different countries. By default, the code assumes that the CSV files are located in the same directory as the script. If they are located elsewhere, modify the csv_files_directory variable at the beginning of the script to point to the correct directory.

## Description of Code
The code starts by importing the necessary libraries.
It reads all CSV files in the specified directory that have names ending with '.csv' and stores them in separate DataFrames for each country.
It then selects a country's GDP data (e.g., Canada) from one of the CSV files and prepares the data for modeling. It sorts the data by year, sets the year as the index, and splits it into a training and validation set (70% for training, 30% for validation).
The ARIMA model is automatically selected and fitted to the training data using the auto_arima function from pmdarima.
The model is then used to forecast GDP values for the validation period.
The code calculates the Root Mean Squared Error (RMSE) between the forecasted values and the actual validation data.
The forecasted results are plotted along with the training and validation data.


> [!NOTE]
> The code repeat similar steps for different countries (e.g., Canada and Albania). You can extend it to handle multiple countries' data efficiently, possibly by writing functions or loops.
> Depending on your use case, you may want to add more error handling, data validation, or visualization options to enhance the robustness and flexibility of the code.
> Remember that the actual performance of ARIMA models may vary depending on the data, and it is essential to evaluate the models' accuracy using appropriate metrics and validation techniques for real-world applications.
