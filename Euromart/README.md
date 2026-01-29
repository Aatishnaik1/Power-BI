📊 Project Overview

A comprehensive business intelligence solution built in Power BI that analyzes retail sales data for Euromart. The dashboard provides actionable insights into sales performance, customer behavior, product trends, and regional analysis, enabling data-driven decision-making across the organization.
Project Type: Retail Analytics | Business Intelligence Dashboard
Tools Used: Power BI Desktop, DAX, Power Query (M)
Data Model: Star Schema with Fact and Dimension Tables

🎯 Business Objectives

Track and analyze sales performance across multiple dimensions
Identify top-performing products, customers, and regions
Monitor key performance indicators (KPIs) in real-time
Provide interactive visualizations for stakeholder decision-making
Enable trend analysis and forecasting for strategic planning


🏗️ Data Model Architecture
The project implements a Star Schema data model for optimal performance and intuitive analysis:
Fact Table:

Fact Sales - Core transactional data containing sales records

Dimension Tables:

Customer Lookup - Customer demographics and information
Product Lookup - Product catalog with categories and attributes
Date Lookup - Time dimension for temporal analysis
Region Lookup - Geographic hierarchy and regional information
Parameter - Dynamic parameters for user interactions

Relationships:

One-to-many relationships between dimension tables and fact table
Optimized for fast query performance and intuitive analysis


📈 Key Features
Sales Performance Analysis

Total revenue, quantity sold, and transaction count tracking
Sales trends over time (daily, weekly, monthly, quarterly, yearly)
Year-over-year (YoY) and month-over-month (MoM) growth analysis
Sales performance by different time periods

Customer Analytics

Customer segmentation and profiling
Top customers by revenue and purchase frequency
Customer lifetime value analysis
New vs. returning customer metrics

Product Intelligence

Best-selling products and categories
Product performance comparison
Category-wise revenue contribution
Inventory and stock analysis insights

Regional Performance

Sales distribution across regions
Regional performance benchmarking
Geographic visualization of sales data
Market penetration analysis by region

Interactive Features

Dynamic slicers for date, product, customer, and region filtering
Drill-through capabilities for detailed analysis
Cross-filtering between visualizations
Parameter-driven dynamic reporting


🔧 Technical Implementation
Data Transformation (Power Query)

Data cleaning and standardization
Handling missing values and duplicates
Creating calculated columns
Merging multiple data sources
Data type optimization

DAX Measures
Key calculated measures implemented:
dax// Total Sales
Total Sales = SUM('Fact Sales'[Sales Amount])

// Total Quantity
Total Quantity = SUM('Fact Sales'[Quantity])

// Average Order Value
Average Order Value = DIVIDE([Total Sales], COUNTROWS('Fact Sales'))

// YoY Growth %
YoY Growth % = 
DIVIDE(
    [Total Sales] - CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date Lookup'[Date])),
    CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date Lookup'[Date]))
)

// Top N Products
Top 10 Products = 
CALCULATE(
    [Total Sales],
    TOPN(10, ALL('Product Lookup'[Product Name]), [Total Sales], DESC)
)
Visualizations Used

KPI Cards - Display key metrics at a glance
Line Charts - Trend analysis over time
Bar/Column Charts - Comparative analysis
Pie/Donut Charts - Category distribution
Tables/Matrix - Detailed data views
Maps - Geographic sales distribution
Slicers - Interactive filtering
