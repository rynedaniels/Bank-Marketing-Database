# Bank Marketing Campaign Analysis
This repository contains a Python script that is exported from a Jupyter notebook, where the data is cleaned and restructured, then converted to SQL database tables for further analysis.

## Data
The data used for this analysis is from the Bank Marketing dataset, which consists of direct marketing campaigns (phone calls) of a Portuguese banking institution. The dataset has 20 input variables and one binary output variable (y), which indicates whether the client has subscribed a term deposit or not.

The data can be downloaded here. After downloading, save it to the data folder of the project with the name bank_marketing.csv.

## Data Cleaning/Reformatting
The script reads in the CSV file using pandas and splits it into three separate DataFrames: client, campaign, and economics. Each DataFrame is then cleaned and formatted as necessary.

For the client table, the education and job columns are cleaned by replacing and removing certain characters.
For the campaign table, some columns are renamed for clarity, and the campaign_outcome and previous_outcome columns are converted to binary values. The last_contact_date column is created by combining year, month, and day columns and converting the result to a datetime object.
For the economics table, some columns are renamed for clarity.
After the data is cleaned, each DataFrame is saved to a separate CSV file for future use.

## Database Design and Creation
This section of the script outlines the SQL commands necessary to create each table in the database. The commands are stored in Python multiline strings. Each string contains a CREATE TABLE command and a \copy command. The CREATE TABLE command creates the structure of each table in the database, and the \copy command imports the data from the CSV files created in the first section into the corresponding table.

Please note that the SQL commands are just written in the Python script but not executed. You need to run these commands in your preferred SQL client to create and populate the tables in the database.

## Purpose
This script is designed to provide an easy way to clean and format the bank marketing dataset and load it into a database for further analysis. With this script, you can focus on the analysis and exploration of the data, rather than the preliminary data cleaning and database setup.

Please note that this script assumes you have a working knowledge of Python and SQL. If you encounter any issues, please make sure to check your Python and SQL syntax.

If you have any questions or suggestions, feel free to reach out or make a pull request.
