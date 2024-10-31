# Retail-Sales-and-Customer-Shopping-Trends

## What is the reason behind choosing this project, Retail Sales and Customer Shopping Trends?

#### The reason for choosing this project is to gain practical experience in analyzing real-world sales and profit data, while developing insights into customer behavior, product performance, and market trends. This project provides an opportunity to apply data analysis techniques to solve business problems, helping companies make informed decisions to drive profitability and customer satisfaction. Additionally, it strengthens my skills in data manipulation, visualization, and prediction, which are crucial for a career in data analysis.

## Overview

#### This project analyzes Retail Sales and Customer Shopping Trends to understand key factors that impact sales performance and customer behavior. By merging transaction data with customer demographics and shopping preferences, the analysis explores seasonal and holiday sales trends, popular products, and customer responses to promotions. The goal is to uncover insights that retailers can use to tailor their offerings, optimize marketing strategies, and adapt to seasonal demand patterns. Ultimately, this project provides a data-driven foundation for enhancing retail strategies, maximizing customer satisfaction, and boosting revenue.

## Key Questions

#### What are the top-selling products and categories, and how do they perform across different seasons and customer demographics?

#### How do seasonal trends, holidays, and promotions impact sales, and are there specific times of the year when sales peak or dip?

#### Who are the top customer segments, and what are their purchasing preferences based on demographics like age, gender, and location?

#### How does pricing and discounting influence sales volume, and what is the average purchase amount for discounted vs. non-discounted items?

#### What are the trends in customer purchase frequency, loyalty, and preferred payment methods, and do these factors affect purchasing behavior?

#### How does customer satisfaction vary by product category, and are subscription models effective in retaining customers with higher purchase frequency?


## Data Source

#### Retail Sales and Customer Shopping Trends are taken from : [kaggle.com]( https://www.kaggle.com).
#### Reatail Sales Dataset is taken from : [kaggle.com](https://www.kaggle.com/datasets/mohammadtalib786/retail-sales-dataset/data)
#### Customer Shopping Trends is taken from : [Kaggle.com](https://www.kaggle.com/datasets/iamsouravbanerjee/customer-shopping-trends-dataset?select=shopping_trends_updated.csv)


## Data Processing and Data Transformation

1. Data Cleaning:

#### Removed duplicates and handled missing values to ensure data quality.
#### Standardized column names for consistency between datasets.

2. Data Merging:

#### Merged the Retail Sales and Customer Shopping Trends using Customer ID, Gender and Age as the common keys, combining relevant columns such as sales, profit, quantity, and region.

3. Feature Selection:

#### Selected key columns for analysis, including , Profit, Quantity, Discount, Region, Category, and Customer Segment, while dropping irrelevant columns like Ship Mode and Customer Name.

4. Data Transformation:

#### Converted date columns (e.g. Date) to datetime format for time-based analysis.
#### Created new calculated fields, such as Discount and Profit Margin.

5. Aggregation:

#### Aggregated data by region, category, and customer segment to analyze overall trends.


## Best practices and how to run the project:

#### To run this project, first you will need Git and Jupyter Notebook, and you will need to add the CSV files to your local machine.
#### The instructions for installing Git can be found [here](https://github.com/git-guides/install-git) and the instructions for installing Jupyter Notebook can be found [here](https://docs.jupyter.org/en/latest/install/notebook-classic.html).
#### Go to my repository: [here][Capstone Repository](https://github.com/JamilaAr/Retail-Sales-and-Superstore-Performance-Data-Analysis)

1. Clone the repository to your machine:

#### git clone https://github.com/JamilaAr/Retail-Sales-and-Superstore-Performance-Data-Analysis

2. Create and activate a virtual environment, and install required packages from 'requirements.txt':

- Linux/Mac:
  
  * python3 -m venv venv
  * source venv/bin/activate
  * pip install -r requirements.txt
  
- GitBash(Windows):
  
  * python -m venv venv
  * source venv/Scripts/activate
  * pip install -r requirements.txt

3. Once complete, be sure to deactivate:
  
  * deactivate
      
4. Ensure the data file has successfully moved to the main project directory before running the analysis notebook.

5. Run the notebook.

## Features

#### 1. Loading the data: I read in two CSV data files from the website Kaggle.com.
#### 2. Clean and operate on the data: pandas merge and select specific rows and columns.
#### 3. Visualize and present the data: I used matplotlib, seaborn and tableau to visualize the data.
#### 4. Best Practices: Instructions for how to run the project and creating virtual environment. 
#### 5. Interpretation of the data: The interpretation of the data is included in the Markdown cells.



