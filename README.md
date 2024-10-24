# **Portfolio Projects**

This repository contains multiple data analysis projects that showcase different skills, including SQL queries, data analysis, and Python-based analysis with Jupyter notebooks. Each project focuses on a different dataset and demonstrates various techniques for extracting insights from data.

**Table of Contents**

- [Data Analyst SQL Project](https://github.com/shrasth/PortfolioProjects/blob/main/DataAnalyst_v2.sql)
- [Housing Data SQL Project](https://github.com/shrasth/PortfolioProjects/blob/main/Housing.sql)
- [Movies Correlation Project](https://github.com/shrasth/PortfolioProjects/blob/main/Movies_Correlation_Project.ipynb)

----
## 1. Data Analyst SQL Project

- **File**: [`DataAnalyst_v2.sql`](https://github.com/shrasth/PortfolioProjects/blob/main/DataAnalyst_v2.sql)
- **Description**: This project showcases SQL skills by performing complex queries to analyze a business dataset. The SQL queries included in this project demonstrate data extraction, aggregation, filtering, and sorting techniques.

### Key Queries
- **Basic Information Retrieval**: Extract raw data from tables.
- **Aggregations**: Calculate metrics such as sum, average, and count on various fields.
- **Joins**: Combine data from multiple tables to derive insights from related datasets.
- **Filtering**: Query data based on specific conditions (e.g., date ranges, user activities).

### Example Queries
```sql
-- Retrieve the total number of customers
SELECT COUNT(*) AS total_customers FROM customers;

-- Calculate total sales by region
SELECT region, SUM(sales) AS total_sales
FROM sales_table
GROUP BY region;
```
----
## 2. Housing Data SQL Project

- **File**: [`Housing.sql`](https://github.com/shrasth/PortfolioProjects/blob/main/Housing.sql)
- **Description**: This project involves analyzing housing market data using SQL. The dataset includes information on house prices, locations, sizes, and other attributes. The goal is to perform various SQL queries to understand pricing trends, house characteristics, and location-based insights.

### Key Queries
- **Data Aggregation**: Perform calculations such as average house prices and sizes.
- **Filtering**: Find properties within specific price ranges or based on location.
- **Ranking**: Identify the top properties based on key attributes like price per square foot.

### Example Queries
```sql
-- Find the top 5 most expensive houses
SELECT * 
FROM housing_table 
ORDER BY price DESC 
LIMIT 5;

-- Calculate the average price of houses by location
SELECT location, AVG(price) AS average_price
FROM housing_table
GROUP BY location;
```
----
## 3. Movies Correlation Project

- **File**: [`Movies_Correlation_Project.ipynb`](https://github.com/shrasth/PortfolioProjects/blob/main/Movies_Correlation_Project.ipynb)
- **Description**: This project uses a Python-based Jupyter notebook to analyze the correlation between various attributes in a movie dataset, including budget, revenue, runtime, and ratings. The analysis aims to identify relationships between these variables and draw insights using correlation metrics.

### Technologies Used
- **Python**: For data analysis and manipulation.
- **Pandas**: To load, clean, and manipulate the data.
- **Matplotlib/Seaborn**: To visualize correlations and data distributions.
- **Jupyter Notebook**: For interactive data analysis.

### Key Analysis
- **Correlation Calculation**: Compute and analyze the correlation matrix for different movie attributes.
- **Visualizations**: Use scatter plots, heatmaps, and bar charts to explore relationships between variables like budget, revenue, and rating.

### Example Code
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load the dataset
df = pd.read_csv('movies.csv')

# Calculate correlation matrix
correlation_matrix = df.corr()

# Visualize the correlation matrix using a heatmap
plt.figure(figsize=(10, 6))
sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm')
plt.title('Correlation Matrix for Movie Data')
plt.show()

