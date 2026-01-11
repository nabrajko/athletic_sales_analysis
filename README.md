# Athletic Sales Analysis

A comprehensive Python data analysis project examining athletic sales data to identify top-performing regions, retailers, and sales trends with focus on women's athletic footwear.

## Project Overview

This project analyzes athletic sales data from 2020-2021 to extract actionable business insights through data aggregation, filtering, and time-series analysis using Python and Pandas.

## Dataset

- **athletic_sales_2020.csv**: Sales data for 2020
- **athletic_sales_2021.csv**: Sales data for 2021

## Setup and Data Preparation

### Combine and Clean the Data

1. Import the two CSV files (`athletic_sales_2020.csv` and `athletic_sales_2021.csv`) into DataFrames
2. Verify column names and data types are consistent across both DataFrames
3. Combine the DataFrames using an inner join
4. Reset the index for the combined DataFrame

## Analysis Tasks

### 1. Determine Which Region Sold the Most Products

- Use `groupby` or `pivot_table` to create a multi-index DataFrame with "region", "state", and "city" columns
- Rename the aggregated column to reflect the data aggregation
- Sort results in descending order to display the top five regions with the greatest number of products sold

### 2. Determine Which Region Had the Most Sales

- Create a multi-index DataFrame with "region", "state", and "city" columns
- Rename the aggregated column appropriately
- Sort in descending order to show the top five regions that generated the most sales

### 3. Determine Which Retailer Had the Most Sales

- Create a multi-index DataFrame with "retailer", "region", "state", and "city" columns
- Rename the aggregated column to reflect the data
- Sort results to display the top five retailers with their location details that generated the most sales

### 4. Determine Which Retailer Sold the Most Women's Athletic Footwear

- Filter the combined DataFrame for women's athletic footwear sales only
- Create a multi-index DataFrame with "retailer", "region", "state", and "city" columns
- Rename the aggregated column appropriately
- Sort to show the top five retailers and locations for women's athletic footwear sales

### 5. Determine the Day with the Most Women's Athletic Footwear Sales

- Create a pivot table with "invoice_date" as index and "total_sales" as values
- Rename the aggregated column
- Apply `resample` function to bin data daily
- Calculate total sales for each day
- Sort in descending order to display the top 10 days with highest sales

### 6. Determine the Week with the Most Women's Athletic Footwear Sales

- Apply `resample` to the pivot table to bin data weekly
- Calculate total sales for each week
- Sort in descending order to show the top 10 weeks with highest women's athletic footwear sales

## Technologies Used

- **Python**: Primary programming language
- **Pandas**: Data manipulation and analysis
- **Jupyter Notebook**: Interactive development environment

## Key Skills Demonstrated

- Data cleaning and preprocessing
- DataFrame manipulation and merging
- Multi-index DataFrame operations
- Time-series analysis with resampling
- Data aggregation using `groupby` and `pivot_table`
- Filtering and sorting large datasets

## Getting Started
```python
import pandas as pd

# Load the datasets
df_2020 = pd.read_csv('athletic_sales_2020.csv')
df_2021 = pd.read_csv('athletic_sales_2021.csv')

# Combine datasets
combined_df = pd.concat([df_2020, df_2021], ignore_index=True)
```

## Results

The analysis provides insights into:
- Top-performing geographic regions
- Most successful retailers
- Women's athletic footwear sales trends
- Daily and weekly sales patterns

