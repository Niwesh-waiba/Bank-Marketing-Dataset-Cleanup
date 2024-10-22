# Bank Marketing Dataset Cleanup

This project focuses on subsetting, cleaning, and reformatting the `bank_marketing.csv` dataset to create three structured CSV files: `client.csv`, `campaign.csv`, and `economics.csv`. The goal is to prepare the data for further analysis and modeling.

## Tech Stack
- **Python**: The programming language used for data manipulation.
- **Pandas**: A powerful library for data analysis and manipulation.
- **NumPy**: A library for numerical operations and handling arrays.
- **CSV**: The format used for reading and writing data files.

## Project Overview
The project involves the following key tasks:
- **Data Loading**: The `bank_marketing.csv` file is read into a Pandas DataFrame.
- **Subsetting**: Three separate DataFrames are created:
  - `client`: Contains columns related to client information.
  - `campaign`: Includes details about the marketing campaign.
  - `economics`: Contains economic indicators related to the clients.
- **Data Cleaning**: 
  - Categorical variables are converted to numerical values for easier analysis.
  - "Unknown" values are replaced with `NaN` to handle missing data.
  - Date-related columns are combined into a single date column for better time-series analysis.
- **Data Saving**: The cleaned DataFrames are saved as CSV files (`client.csv`, `campaign.csv`, and `economics.csv`) without index values.

## Key Features
- Easy access to cleaned and organized data for analysis and modeling.
- Structured DataFrames facilitate further exploration and machine learning applications.
- Preprocessing ensures data quality and readiness for insights.

## Outcome
Three tidy CSV files are generated, making the dataset more accessible and enhancing usability for data analysis and machine learning tasks.

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/bank_marketing_cleanup.git
