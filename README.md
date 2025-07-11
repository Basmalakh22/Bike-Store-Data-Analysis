

## Project Overview

This project builds a Data Warehouse Analytics environment using SQL Server. It focuses on loading, exploring, and analyzing sales, customer, and product data using SQL. The project demonstrates key business intelligence concepts including trend analysis, customer segmentation, and performance tracking.

## Project Structure

- Database and Schema Creation
- Data Loading (CSV Files)
- Data Exploration Queries
- Analytical Queries (Ranking, Trends, Segmentation)
- Business Reports (Customer and Product Views)

## Setup Instructions

1. Prerequisites

- Microsoft SQL Server
- SQL Server Management Studio (SSMS)
- CSV files:
  - `gold.dim_customers.csv`
  - `gold.dim_products.csv`
  - `gold.fact_sales.csv`

1. Database Setup

- Run the provided SQL script to:
  - Drop and recreate the DataWarehouseAnalytics database.
  - Create the gold schema.
  - Create dimension and fact tables.

1. Data Loading

- Use BULK INSERT to load data from the local CSV files. Update file paths as per your environment.

```sql
BULK INSERT gold.dim_customers
FROM 'C:\sql\sql-data-analytics-project\datasets\csv-files\gold.dim_customers.csv'
...
```

## Key Components

### Database

- Schemas: gold

- Tables:
  - `gold.dim_customers`
  - `gold.dim_products`
  - `gold.fact_sales`

### Analysis Areas

- Database and data exploration
- Dimension and fact analysis
- Key metrics and aggregations
- Customer and product segmentation
- Trend and time-based analysis
- Cumulative sales tracking
- Year-over-Year and Month-over-Month comparisons

### Reports

- `gold.report_customers`: Customer-level analytics report
- `gold.report_products`: Product-level performance report

## Core Analyses

### Magnitude Analysis

- Customers by country and gender
- Products by category and average cost
- Revenue by category and customer

### Ranking Analysis

- Top and bottom performing products
- Top 10 revenue-generating customers
- Customers with the fewest orders

### Time-Series Analysis

- Monthly sales and customer trends using YEAR(), MONTH(), DATETRUNC(), and FORMAT()

### Cumulative Analysis

- Running total of sales and moving average prices over time

### Performance Analysis

- Year-over-Year product performance
- Comparison to product average sales using LAG()

### Segmentation Analysis

- Customer segmentation (VIP, Regular, New) based on spending and history
- Product segmentation by cost ranges

### Part-to-Whole Analysis

- Category contribution to overall sales

## Business Reports

### Customer Report (gold.report_customers)

- Customer demographics and purchase behavior
- Customer type: VIP, Regular, New
- Lifetime value metrics: total orders, total spend, recency, average order value, and average monthly spend

### Product Report (gold.report_products)

- Product performance: total sales, total customers, product lifespan
- Product type: High-Performer, Mid-Range, Low-Performer
- Recency, average order revenue, and average monthly revenue
