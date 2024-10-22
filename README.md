# Bank-Marketing-Dataset-Cleanup

This project involves subsetting, cleaning, and reformatting the bank_marketing.csv dataset to create three structured CSV files: client.csv, campaign.csv, and economics.csv. The aim is to prepare the data for further analysis and modeling.

Tech Stack
Python: Programming language used for data manipulation.
Pandas: Library for data analysis and manipulation.
NumPy: Library for numerical operations.
CSV: Format for reading and writing data files.
Key Features
Data Loading: Reads the bank_marketing.csv file into a DataFrame.
Subsetting: Creates three DataFrames:
client: Contains client-related features.
campaign: Details of the marketing campaign.
economics: Economic indicators related to clients.
Data Cleaning:
Converts categorical variables to numerical values.
Replaces "unknown" values with NaN.
Combines date-related columns into a single date column.
Data Saving: Outputs the cleaned DataFrames as client.csv, campaign.csv, and economics.csv, without index values.
Outcome
Three tidy CSV files generated for easier access and enhanced usability, facilitating further data analysis and machine learning applications.

Usage
Clone the repository and run the Python script to perform the data cleaning and export the CSV files.

