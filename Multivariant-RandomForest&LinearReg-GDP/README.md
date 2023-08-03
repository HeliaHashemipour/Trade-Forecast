### README for MULTIVARIANT

This repository contains Python code to analyze and process CSV files containing GDP data for different countries. The code performs various tasks, such as merging CSV files, calculating correlation matrices, creating time series plots, and making predictions using a Linear Regression model in multivariate way.

** Requirements **
The code in this repository requires the following Python libraries to be installed:
- pip install -r requirements.txt

Run the script merge_csv_files.py. This script will read all CSV files ending with '_gdp_data.csv' from the specified directory, merge them into a single DataFrame, and save it as merged_data.csv.

After merging the CSV files, the script will calculate the correlation matrix and plot a heatmap for the top 5 correlated columns in the merged_data.csv file. The heatmap and time series plots will be displayed on the screen.

The script will also predict the GDP values for the next 6 years using a Linear Regression model. The predicted values will be saved in the final_modified1.csv file.

Additionally, the script will identify the next 5 correlated columns with the highest average correlation and plot their time series.

** Important Note **
Please ensure that you have the necessary CSV files with the correct format and column names. The script assumes that the CSV files contain GDP data for different countries with the 'Year' column as the index.