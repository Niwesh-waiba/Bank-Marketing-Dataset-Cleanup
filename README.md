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

![Piggy bank](piggy_bank.jpg)

Personal loans are a lucrative revenue stream for banks. The typical interest rate of a two-year loan in the United Kingdom is [around 10%](https://www.experian.com/blogs/ask-experian/whats-a-good-interest-rate-for-a-personal-loan/). This might not sound like a lot, but in September 2022 alone UK consumers borrowed [around £1.5 billion](https://www.ukfinance.org.uk/system/files/2022-12/Household%20Finance%20Review%202022%20Q3-%20Final.pdf), which would mean approximately £300 million in interest generated by banks over two years!

You have been asked to work with a bank to clean the data they collected as part of a recent marketing campaign, which aimed to get customers to take out a personal loan. They plan to conduct more marketing campaigns going forward so would like you to ensure it conforms to the specific structure and data types that they specify so that they can then use the cleaned data you provide to set up a PostgreSQL database, which will store this campaign's data and allow data from future campaigns to be easily imported. 

They have supplied you with a csv file called `"bank_marketing.csv"`, which you will need to clean, reformat, and split the data, saving three final csv files. Specifically, the three files should have the names and contents as outlined below:

## `client.csv`

| column | data type | description | cleaning requirements |
|--------|-----------|-------------|-----------------------|
| `client_id` | `integer` | Client ID | N/A |
| `age` | `integer` | Client's age in years | N/A |
| `job` | `object` | Client's type of job | Change `"."` to `"_"` |
| `marital` | `object` | Client's marital status | N/A |
| `education` | `object` | Client's level of education | Change `"."` to `"_"` and `"unknown"` to `np.NaN` |
| `credit_default` | `bool` | Whether the client's credit is in default | Convert to `boolean` data type:<br> `1` if `"yes"`, otherwise `0` |
| `mortgage` | `bool` | Whether the client has an existing mortgage (housing loan) | Convert to boolean data type:<br> `1` if `"yes"`, otherwise `0` |

<br>

## `campaign.csv`

| column | data type | description | cleaning requirements |
|--------|-----------|-------------|-----------------------|
| `client_id` | `integer` | Client ID | N/A |
| `number_contacts` | `integer` | Number of contact attempts to the client in the current campaign | N/A |
| `contact_duration` | `integer` | Last contact duration in seconds | N/A |
| `previous_campaign_contacts` | `integer` | Number of contact attempts to the client in the previous campaign | N/A |
| `previous_outcome` | `bool` | Outcome of the previous campaign | Convert to boolean data type:<br> `1` if `"success"`, otherwise `0`. |
| `campaign_outcome` | `bool` | Outcome of the current campaign | Convert to boolean data type:<br> `1` if `"yes"`, otherwise `0`. |
| `last_contact_date` | `datetime` | Last date the client was contacted | Create from a combination of `day`, `month`, and a newly created `year` column (which should have a value of `2022`); <br> **Format =** `"YYYY-MM-DD"` |

<br>

## `economics.csv`

| column | data type | description | cleaning requirements |
|--------|-----------|-------------|-----------------------|
| `client_id` | `integer` | Client ID | N/A |
| `cons_price_idx` | `float` | Consumer price index (monthly indicator) | N/A |
| `euribor_three_months` | `float` | Euro Interbank Offered Rate (euribor) three-month rate (daily indicator) | N/A |



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
