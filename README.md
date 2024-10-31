# Retail-Sales-and-Customer-Shopping-Trends

## What is the reason behind choosing this project, Retail Sales and Superstore Performance Data Analysis?

#### The reason for choosing this project is to gain practical experience in analyzing real-world sales and profit data, while developing insights into customer behavior, product performance, and market trends. This project provides an opportunity to apply data analysis techniques to solve business problems, helping companies make informed decisions to drive profitability and customer satisfaction. Additionally, it strengthens my skills in data manipulation, visualization, and prediction, which are crucial for a career in data analysis.

## Overview

#### The "Retail Sales and Superstore Performance" capstone project analyzes sales and profit performance for both retail and superstore datasets, focusing on key factors such as customer demographics, regions, product categories, and customer segments. By examining sales trends over time, the effect of discounts, and revenue patterns across segments, this analysis aims to identify opportunities for increasing profitability. The goal is to understand customer behavior and predict future sales trends based on historical data, guiding business decision

## Key Questions

#### Sales Trends and distribution
What are the sales trends over time for both the retail and superstore datasets?
Are there seasonal trends in sales for specific products or categories?

#### Performance Analysis
Which regions, product categories, and customer segments have the highest sales and profit?
Which customer segments generate the most revenue?
What is the effect of discounts on sales and profit?

#### Demographics and Customer Insights
What demographics (age, gender, location) are associated with higher sales?
What factors influence sales performance, and how can we predict future sales based on historical data?


## Data Source

- Retail Sales and Superstore Performance Dataset is taken from [kaggle.com]( https://www.kaggle.com).
- Reatail Sales Dataset is taken from :[kaggle.com](https://www.kaggle.com/datasets/mohammadtalib786/retail-sales-dataset/data)
- Superstore Dataset is taken from :[kaggle.com](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)

## Data Processing and Data Transformation

1.Data Cleaning:

-Removed duplicates and handled missing values to ensure data quality.
-Standardized column names for consistency between datasets.

2.Data Merging:

-Merged the Retail and Superstore datasets using Customer ID as the common key, combining relevant columns such as sales, profit, quantity, and region.

3.Feature Selection:

-Selected key columns for analysis, including Sales, Profit, Quantity, Discount, Region, Category, and Customer Segment, while dropping irrelevant columns like Ship Mode and Customer Name.

4.Data Transformation:

-Converted date columns (e.g., Order Date, Date) to datetime format for time-based analysis.
-Created new calculated fields, such as Total Sales or Profit Margin.

5.Aggregation:

-Aggregated data by region, category, and customer segment to analyze overall trends.


## Best practices and how to run the project:

To run this project, first you will need Git and Jupyter Notebook, and you will need to add the CSV files to your local machine.
The instructions for installing Git can be found [here](https://github.com/git-guides/install-git) and the instructions for installing Jupyter Notebook can be found [here](https://docs.jupyter.org/en/latest/install/notebook-classic.html).

Go to my repository: [Capstone Repository](https://github.com/JamilaAr/Retail-Sales-and-Superstore-Performance-Data-Analysis)

1. Clone the repository to your machine:

  git clone https://github.com/JamilaAr/Retail-Sales-and-Superstore-Performance-Data-Analysis

2. Create and activate a virtual environment, and install required packages from 'requirements.txt':

- Linux/Mac:
  
  python3 -m venv venv
  source venv/bin/activate
  pip install -r requirements.txt
  
- GitBash(Windows):
  
  python -m venv venv
  source venv/Scripts/activate
  pip install -r requirements.txt

3. Once complete, be sure to deactivate:
  
  deactivate
      

4. Ensure the data file has successfully moved to the main project directory before running the analysis notebook.

5. Run the notebook.

## Features

#### 1. Loading Read data: I read in two CSV data files from the website Kaggle.com.
#### 2. Clean and operate on the data: pandas merge and select specific rows and columns.
#### 3. Visualize and present the data: I used matplotlib, seaborn and tableau to visualize the data.
#### 4. Best Practices: Instructions for how to run the project and creating virtual environment. 
#### 5. Interpretation of the data: markdown cells in program and summary in readme.md.

## Key Findings and Visualization

#### Sales Trends Over Time:

Finding: Sales have shown an upward trend over the analyzed period for both datasets, with noticeable peaks during specific months.
Visualization: Line chart displaying monthly sales trends for both the retail and superstore datasets, highlighting significant peaks and valleys.

#### Highest Sales and Profit by Region:

Finding: Certain regions consistently outperform others in terms of sales and profit, indicating market strengths.
Visualization: Bar chart comparing total sales and profit by region, making it easy to identify high-performing areas.

#### Customer Demographics and Sales:

Finding: Specific demographics, such as gender and age groups, are associated with higher sales, suggesting targeted marketing opportunities.
Visualization: Pie chart or bar chart illustrating sales distribution by gender and age segments, showcasing which demographics generate the most revenue.

#### Effect of Discounts on Sales and Profit:

Finding: There is a strong correlation between discount levels and sales volume, but excessive discounts can negatively impact profit margins.
Visualization: Scatter plot showing the relationship between discounts offered and sales volume, with profit margins highlighted to indicate the sweet spot for discounts.

#### Revenue Generation by Customer Segment:

Finding: Certain customer segments (e.g., Corporate vs. Consumer) generate significantly more revenue than others, indicating where to focus marketing efforts.
Visualization: Stacked bar chart comparing total revenue by customer segment, allowing for easy comparison of performance across segments.

#### Factors Influencing Sales Performance:

Finding: Key factors such as product category, region, and customer demographics play a significant role in driving sales performance.
Visualization: Heatmap or bubble chart illustrating the influence of different factors on sales performance, providing a visual representation of the most impactful variables