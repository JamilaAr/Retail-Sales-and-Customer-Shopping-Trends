
![Retail Sales Overview](ReadmeImage/Retail Sales Image.jpg)

# Retail-Sales-and-Customer-Shopping-Trends

My Capstone Project

## What is the reason behind choosing this project, Retail Sales and Customer Shopping Trends?

#### I chose this project to gain practical experience in analyzing real-world sales data while deepening my understanding of customer behavior, product performance, and market trends. As someone passionate about the sales field and e-commerce, I wanted to explore how businesses can optimize sales strategies, understand customer buying patterns, and drive growth in the online marketplace. This project not only allows me to apply data analysis techniques to solve business problems but also strengthens my skills in data manipulation and visualization, which are essential for a successful career in data analysis.

## Overview

- This project analyzes retail sales and customer shopping trends to identify key factors impacting sales and customer behavior. Using Pandas, the analysis explores sales data, seasonal trends, holiday promotions, and customer shopping patterns to understand periods and factors driving higher sales. It provides valuable insights into seasonal demand fluctuations and customer behavior.

The SQL analysis further investigates the relationship between discounts and profitability, focusing on how various discount levels affect sales and profit across product categories. It identifies optimal discount strategies to maximize profit while maintaining sales performance, offering insights into the effectiveness of current sales approaches.

Together, the Pandas and SQL analyses offer actionable insights for retailers to optimize promotional strategies, refine offerings, and adapt to seasonal demand shifts, aiming to enhance retail performance and increase revenue.

## Questions Addressed

### Questions for Pandas Analysis

#### 1. What are the top-performing products and categories, and how do customer demographics (age, gender, and location) influence their sales performance?
#### 2. How do sales fluctuate throughout 2023, and are there specific months, seasons, or holidays when customers shop more?
#### 3. How do promotions and discounts impact sales across different categories, and do they encourage higher spending or more frequent purchases?
#### 4. How do customer behaviors—such as purchase frequency, previous purchases, subscription status, and review ratings—impact overall sales?

### Questions for SQL Analysis

#### 5. What is the impact of the correlation between discount and profit on category profitability?
#### 6. How does the average discount affect profits in different categories?
#### 7. How do profits differ across categories by month and season?


## Data Source

- Retail Sales and Customer Shopping Trends are taken from : [kaggle.com]( https://www.kaggle.com).
- Retail Sales Dataset is taken from : [kaggle.com](https://www.kaggle.com/datasets/mohammadtalib786/retail-sales-dataset/data)
- Customer Shopping Trends is taken from : [Kaggle.com](https://www.kaggle.com/datasets/iamsouravbanerjee/customer-shopping-trends-dataset?select=shopping_trends_updated.csv)

## Data Dictionary

This project analyzes a merged dataset that combines the Retail Sales and Customer Shopping Trends datasets to provide comprehensive insights into sales performance, customer behavior, and purchasing patterns. Below is a detailed description of each column, including both original features and newly derived columns used in the analysis:

### Columns in the Merged Dataset:

1. **Customer ID**: Unique identifier for each customer.
2. **Age**:Customer age for demographic insights, categorized into Age Groups (e.g., Child, Adult, Senior).
3. **Gender**: Gender of the customer (e.g., Male, Female).
4. **Product**: The name of the product purchased by the customer.
5. **Category**: The category of the product (e.g., Clothing, Footwear, Accessories, Outerwear).
6. **Location**: Geographic location of the customer (e.g., City, State, Region).
7. **Season**: The season in which the purchase was made (e.g., Spring, Summer, Fall, Winter).
8. **Review Rating**: The average rating given by customers to the product (on a scale from 1 to 5).
9. **Subscription Status**: Indicates if the customer has a subscription status (e.g., Active, Inactive).
10. **Discount Applied**: Indicates whether a discount was applied to the order (True/False).
11. **Promo Code Used**: Indicates whether a promo code was used during the purchase (True/False).
12. **Previous Purchases**: Number of purchases made by the customer prior to this one. They were categorized into groups (e.g., 0–10, 11–20, 50+).
13. **Frequency of Purchases**: How often the customer purchases (e.g., Daily, Weekly, Monthly).
14. **Date**: Date of purchase, with extracted components Year, Month, Day for time-based trend analysis.
15. **Quantity**: The quantity of items purchased in the transaction.
16. **Purchase Amount (USD)**: The discounted price for a single unit of the product.
17. **Sales**: Total sales value of the transaction, calculated as the 'Purchase Amount (USD)' * 'Quantity'.
18. **Holiday**: Indicates the specific holiday name (e.g., New Year's Day, Christmas) during which a transaction occurred, based on the purchase date in the year 2023..
22. **Discount**: The percentage or value of the discount applied to the transaction. This column helps analyze how discounts impact customer purchasing behavior and overall sales performance.(SQL-derived)
23. **Profit**: The monetary profit earned from a transaction. This column is crucial for understanding profitability trends across products, categories and season.(SQL-derived)
24. **Original_Price_per_Item**: The original price of products before discount applied.


## Data Processing and Data Transformation

1. Data Cleaning:

- Removing duplicate entries and strip whitespaces to avoid skewed analysis.
- Handling missing values by either imputing them with suitable replacements (e.g., mean, median...) or dropping rows/columns where data was insufficient.
- Ensuring correct data types for all columns (e.g., converting dates to datetime format and numeric columns to appropriate numerical types).


2. Data Merging:

- Merged the Retail Sales and Customer Shopping Trends datasets using an outer join on shared keys such as Customer ID, ensuring that no customer data was lost during the merging process.
- Resolved column conflicts and renamed overlapping columns to maintain clarity and avoid ambiguity.
- Integrated a Holiday dataset by merging it with the merged_df based on the Date column, enabling analysis of purchasing trends during holiday periods.

3. Feature Selection:

- Selected key columns for analysis, including Sales, Quantity, Category, Age, Season and Holiday..., while dropping irrelevant columns like Size, Color, Shipping Type...from customer_df , and Age, Gender, Transaction ID... from retail_df.
- Creating new features like Age Group and Previous Purchases Group to provide more detailed insights into customer behavior.
- Added Original_Price_per_Item, Profit and Discount columns during the SQL analysis phase to evaluate the impact of discounts on purchasing behavior and to assess profitability trends.

4. Data Transformation:

- Grouping Numerical Columns: Grouping numerical columns like Age and Previous Purchases into meaningful bins (e.g., age groups like "18-25"...) to make the data easier to analyze and interpret.
- Adding Contextual Features: Adding a Holiday column to indicate whether a transaction occurred during a significant holiday period, enabling the analysis of seasonal sales trends and customer behavior.
- Incorporating Profit and Discount Metrics: While Pandas analysis primarily focuses on exploring sales trends, the SQL analysis adds a complementary dimension by introducing Profit and Discount columns. These transformations enable deeper performance evaluation, such as understanding the correlation between discounts and profit and determining the impact of discounts on sales profitability.
- Converting Data Types: Ensuring columns are converted to appropriate data types, such as converting the date column to datetime format for time-based analysis and aggregations.

5. Aggregation:

- Summarizing sales data by Category, Location, Season... to understand performance trends.
- Aggregating customer demographics to analyze the contribution of different age groups and genders to overall sales.
- Using SQL aggregation functions to calculate total sales, profit, and discounts by category, season, and other factors provides a deeper understanding of profitability trends.

## Best practices and how to Replicate and run the project:

This project contains two Jupyter notebooks located in the folder[notebooks](notebooks). While they are separate files, they complement each other, and it is recommended to run them in the following order for a seamless analysis:

1. [Retail Sales and Customer Shopping Trends](Retail_Sales_and_Customer_Shopping_Trends.ipynb)
2. [Retail Sales and Trends SQL Analysis](Retail_Sales_and_Trends_SQL_Analysis.ipynb)

Additional Resources in the Repository

The repository also includes the following folders and files to support the analysis:

* [Data folder](data): Contains all the necessary .csv files and the .db file used in this project.
* [ReadmeImage](ReadmeImage): Contains an image used as an overview in the Readme.md.

### Prerequisites for Replicating the Analysis

1. Git:
* Git is required to clone the repository to your local machine. You can follow the installation instructions available at this website [here](https://github.com/git-guides/install-git) 

2. Visual Studio Code (VSC)
The analysis was conducted using Jupyter Notebook within Visual Studio Code (VSC). To get started with VSC:

- Download and install Visual Studio Code from [here](https://code.visualstudio.com/Download)
- Once installed, open VSC and ensure the Jupyter extension is installed. You can search for the Jupyter extension in the Extensions view (Ctrl+Shift+X) and install it.

3. Jupyter Notebook
After installing VSC and the Jupyter extension, you need to install Jupyter Notebook itself. Follow these steps:
* Open a terminal in VSC and install Jupyter by running the command:
         pip install notebook
* After installation, you should be able to run Jupyter notebooks inside VSC. For more detailed instructions, refer to the official documentation [here](https://docs.jupyter.org/en/latest/install/notebook-classic.html)


4. CSV Files: 
* Download the required CSV files and place them in the project folder on your local machine. These files are necessary for running the analysis notebooks.

5. SQL Database (.db file):
The .db file, which was created by converting the merged DataFrame from Pandas to SQL, is required for running the SQL analysis. You can either download this file from the repository or you can create it by running the SQL_Analysis.ipynb notebook to convert the merged Pandas DataFrame into an SQL database.

### Getting started to Replicate and Run the Project:

1. Clone the Repository:
* Clone the project repository to your local machine by using the following URL: https://github.com/JamilaAr/Retail-Sales-and-Customer-Shopping-Trends/tree/main
* Run the command below in your terminal:
git clone https://github.com/JamilaAr/Retail-Sales-and-Customer-Shopping-Trends/tree/main

2. Create and Activate a Virtual Environment:
* Set up a virtual environment and install the required packages from requirements.txt:

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
      
4. Ensure that all the necessary CSV data files are placed in the main project directory. These files are essential for the notebooks to function properly.

5. Run the Notebooks:
* Open and execute the following notebooks for analysis:

1. Retail-Sales_and_Customer_Shopping_Trends.ipynb
2. Retail_Sales_and_Trends_SQL_Analysis.ipynb

## Features

1. Data Loading:

* Imported two CSV files sourced from Kaggle.com into the project for analysis.
* Converted the merged DataFrame from Pandas into a .db file to perform SQL-based analysis and queries.

2. Data Cleaning and Transformation:

* Utilized various Pandas functions and methods such as .strip(), .drop(), .rename(), .insert(), .fillna(), .merge(), etc., to clean and manipulate the data for consistency and accuracy.

* Filtered specific rows and columns and calculated new values as needed.

* Used functions like .head(), .info(), .describe(), .isna(), .sum(), .fillna(), .sort_values(), and .mean() to explore and analyze the data.

3. Data Visualization and Presentation:

* Used Matplotlib, Seaborn, and Tableau to create clear, meaningful, and interactive visualizations to present key findings.

4. Best Practices:

* Provided detailed, step-by-step instructions for setting up and running the project, including Prerequisites and using a virtual environment...

5. Data Interpretation:

* The interpretation of the data is included in the Markdown cells.

6. SQL Analysis:

* Utilized SQLite for structured data analysis.

* Applied SQL queries for adding, filtering, grouping, and aggregating data.

* Adding new metrics such as original price per item, profit and discount to analyze their correlation and the impact of discount on profitability...

## Interpretation of the data:

- In this analysis, we observed a clear seasonal trend in retail sales, with sales peaking during the holiday season and dropping during the summer months. Additionally, a moderate positive correlation (0.54) was found between the discount rate and profit, indicating that higher discounts tend to increase profit, although other factors also contribute to profitability. This highlights the need for businesses to strategically manage discount levels to optimize profitability, especially during peak sales periods, while considering other factors like demand and seasonality.

## I will be presenting a Tableau dashboard to analyze Retail Sales and Customer Shopping Trends. This interactive visualization provides clear and dynamic insights into sales patterns, customer demographics, and regional performance. It allows users to:

* Explore sales trends for top product and categories across various age groups and genders.

* Analyze geographic sales performance, highlighting top-performing states.

* Identify seasonal patterns by examining sales trends across holidays, months, and seasons.

[Click on the link](https://public.tableau.com/views/RetailSalesandCustomerShoppingTrends/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

## Conclusion:

The Retail Sales and Customer Shopping Trends project provided valuable insights into sales performance. The analysis highlighted strong sales across product categories, locations, and customer segments, underscoring the effectiveness of current strategies. Seasonal trends and holidays significantly boosted sales, with festive periods driving higher demand and engagement.

We observed a moderate positive correlation (0.54) between profit and discount, indicating that higher discounts tend to increase profit, though other factors also influence profitability. While discounts can drive sales, it’s important to balance them to avoid diminishing profit margins. Effective discount strategies should focus on maximizing both sales and profitability.

In summary, a strategic approach combining effective sales tactics with balanced discounting can drive growth and sustain profitability in the competitive retail market.

## Acknowledgements:

#### This project was created as a capstone for the Data Analytics pathway through the Code:You program. I would like to express my deepest gratitude to my mentors for their invaluable guidance and support throughout this journey.

#### To my husband, thank you for your unwavering support and patience. My heartfelt appreciation goes to my baby, who has grown so fast during this time. Your patience inspired me to keep going, even when balancing my studies and time with you was challenging. I’m sorry for the moments I may not have been fully present.

#### I also want to acknowledge the role of AI (ChatGPT and Perplexity) as a valuable mentor in this project. It guided me through coding challenges, debugging issues, and organizing my ideas effectively. I am grateful to several online platforms like Google, Pluralsight, Codecademy, W3Schools, FreeCodeCamp, and others, which provided additional resources and insights.