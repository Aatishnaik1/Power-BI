📊 Project Overview
--
A comprehensive business intelligence solution built in Power BI that analyzes retail sales data for Euromart.
The dashboard provides actionable insights into sales performance, customer behavior, product trends, and regional analysis, enabling data-driven decision-making across the organization.

**Project Type**: Retail Analytics | Business Intelligence Dashboard
Tools Used: Power BI Desktop, DAX, Power Query (M)
Data Model: Star Schema with Fact and Dimension Tables

🎯 Business Objectives
--
* Track and analyze sales performance across multiple dimensions
* Identify top-performing products, customers, and regions
* Monitor key performance indicators (KPIs) in real-time
* Provide interactive visualizations for stakeholder decision-making
* Enable trend analysis and forecasting for strategic planning

🏗️ Data Model Architecture
--
The project implements a Star Schema data model for optimal performance and intuitive analysis:

Fact Table:
* Fact Sales - Core transactional data containing sales records

Dimension Tables:

* Customer Lookup - Customer demographics and information
* Product Lookup - Product catalog with categories and attributes
* Date Lookup - Time dimension for temporal analysis
* Region Lookup - Geographic hierarchy and regional information
* Parameter - Dynamic parameters for user interactions

Relationships:

* One-to-many relationships between dimension tables and fact table
* Optimized for fast query performance and intuitive analysis
