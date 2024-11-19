# Retail-Sales-and-Customer-Shopping-Trends
My Capstone Project

## What is the reason behind choosing this project, Retail Sales and Customer Shopping Trends?

#### The reason for choosing this project is to gain practical experience in analyzing real-world sales data, while developing insights into customer behavior, product performance, and market trends. This project provides an opportunity to apply data analysis techniques to solve business problems, helping companies make informed decisions to drive profitability and customer satisfaction. Additionally, it strengthens my skills in data manipulation, visualization, and prediction, which are crucial for a career in data analysis.

## Overview

#### This project analyzes Retail Sales and Customer Shopping Trends to understand key factors that impact sales performance and customer behavior. By merging transaction data with customer demographics and shopping preferences, the analysis explores seasonal and holiday sales trends, popular products, and customer responses to promotions. The goal is to uncover insights that retailers can use to tailor their offerings, optimize marketing strategies, and adapt to seasonal demand patterns. Ultimately, this project provides a data-driven foundation for enhancing retail strategies, maximizing customer satisfaction, and boosting revenue.

## Key Questions
#### What are the top-performing products and categories, and how do customer demographics (age, gender, and location) influence their sales performance?
#### How do sales fluctuate throughout 2023, and are there specific months, seasons, or holidays when customers shop more?
#### How do promotions and discounts impact sales across different categories, and do they encourage higher spending or more frequent purchases?
#### How do customer behaviors—such as purchase frequency, previous purchases, subscription status, and review ratings—affect their future spending patterns?


## Data Source

#### Retail Sales and Customer Shopping Trends are taken from : [kaggle.com]( https://www.kaggle.com).
#### Reatail Sales Dataset is taken from : [kaggle.com](https://www.kaggle.com/datasets/mohammadtalib786/retail-sales-dataset/data)
#### Customer Shopping Trends is taken from : [Kaggle.com](https://www.kaggle.com/datasets/iamsouravbanerjee/customer-shopping-trends-dataset?select=shopping_trends_updated.csv)


## Data Processing and Data Transformation

1. Data Cleaning:

#### Removing duplicate entries to avoid skewed analysis.
#### Handling missing values by either imputing them with suitable replacements (e.g., mean, median, or mode) or dropping rows/columns where data was insufficient.
#### Ensuring correct data types for all columns (e.g., converting dates to datetime format and numeric columns to appropriate numerical types)...


2. Data Merging:

#### Merged the Retail Sales and Customer Shopping Trends Using an outer join on shared keys like Customer ID to ensure no customer data was lost..
#### Renaming or resolving column conflicts in cases of overlapping column names to maintain clarity.
#### Adding a new column of holiday and merging it with the merged_df based on the Date column

3. Feature Selection:

#### Selected key columns for analysis, including Sales, Quantity, Category, Age, Season and Holiday..., while dropping irrelevant columns like Size, Color, Shipping Type...from customer_df , and Age, Gender, Transaction ID... from retail_df.
#### Creating new features like Age Group and Previous Purchases Group to provide more detailed insights into customer behavior.

4. Data Transformation:

#### Grouping numerical columns like Age and Previous Purchases into meaningful bins (e.g., age groups like "18-25").
#### Adding a Holiday column to indicate whether a transaction occurred during a significant holiday.
#### Converting columns to appropriate data types, for example, the date columnmto datetime format for time-based analysis.

5. Aggregation:

#### Summarizing sales data by Category, Location, Season... to understand performance trends.
#### Aggregating customer demographics to analyze the contribution of different age groups and genders to overall sales.


## Best practices and how to run the project:

#### To run this project, first you will need:
* Git for cloning the repository. Installation instructions can be found [here](https://github.com/git-guides/install-git) 
* Jupyter Notebook for running the analysis notebook. Installation instructions can be found [here](https://docs.jupyter.org/en/latest/install/notebook-classic.html).
* and you will need to add the CSV files to your local machine.

#### Steps to Run the Project:
1. Clone the Repository to your local machine: The link is [here](https://github.com/JamilaAr/Retail-Sales-and-Customer-Shopping-Trends/tree/main)
2. Create and activate a virtual environment, and install required packages from 'requirements.txt':

- For Linux/Mac:
  
  * python3 -m venv venv
  * source venv/bin/activate
  * pip install -r requirements.txt
  
- For Git Bash(Windows):
  
  * python -m venv venv
  * source venv/Scripts/activate
  * pip install -r requirements.txt

3. Deactivate the Virtual Environment (After Use):
  
  * deactivate
      
4. Ensure that the necessary CSV data files are copied into the main project directory. This is required for the analysis notebook to function properly.

5. Run the Notebook.

## Features

#### Loading the Data: Imported two CSV data files sourced from Kaggle.com into the project for analysis.

#### Data Cleaning and Operations: Utilized Pandas to merge datasets, filter specific rows and columns, and clean the data for consistency and accuracy.

#### Data Visualization and Presentation: Used Matplotlib, Seaborn, and Tableau to create meaningful and interactive visualizations of the data.

#### Best Practices: Provided detailed instructions for running the project, including creating and using a virtual environment.

#### Data Interpretation: Included insights and interpretations of the data, documented in Markdown cells within the Jupyter Notebook.


