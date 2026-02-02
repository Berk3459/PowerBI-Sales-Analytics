# Power BI Sales Analytics Project
## Project Overview

This project is an end-to-end Business Intelligence & Analytics solution built to demonstrate real-world data modeling, ETL, semantic modeling, advanced DAX, and dashboard design skills using SQL Server and Power BI.

The main objective is to transform raw sales-related Excel files into a clean star schema, build a robust semantic model, and generate actionable business insights for decision-makers.

## Data Architecture & Modeling
### Source Data

The project starts with 7 Excel files:

* dim_campaigns
* dim_customers
* dim_products
* dim_dates
* dim_salespersons
* dim_stores
* fact_sales

These datasets represent a typical retail sales environment including customers, products, stores, campaigns, salespersons, and transactional sales data.

### ETL Process (Extract – Transform – Load)

The ETL pipeline was designed to ensure data consistency, performance, and scalability.

**Steps**:

***Extract***: Imported Excel files into SQL Server

***Transform***: Cleaned column names and data types, Removed duplicates and invalid records,Standardized date formats,Ensured referential integrity

***Load***:Loaded data into SQL tables,Created dimension and fact tables,ETL logic ensures that Power BI consumes analytics-ready data.

## Surrogate Keys & Star Schema Design
 Why Surrogate Keys?

* Improve join performance
* Enable Slowly Changing Dimensions (future-ready)


 ***Star Schema***

The final data model follows a Star Schema design:

Fact Table: fact_sales
Dimension Tables:

* Customers
* Products
* Dates
* Stores
* Campaigns
* Salespersons


**Semantic Model (Power BI)**

The semantic model was built on top of the star schema to provide:

* Business-friendly field names
* Reusable KPI measures
* Consistent calculations across reports
* Key Principles Applied:
* Single-direction relationships (dim ➝ fact)
* Centralized measure table
* Hidden technical columns (SKs)

This layer enables self-service analytics while maintaining governance.

## DAX Measures & KPIs
### Core KPIs

* Total Revenue

* Sales Quantity

* Total Orders

* Average Basket Value

### Time Intelligence

* Month-over-Month (MoM) Growth
* Rolling 3-Month Revenue

### Advanced Analytics

* Cumulative Revenue (Running Total)

* Top-N Products, Stores, Customers

All measures were written using best-practice DAX patterns to ensure accuracy and performance.




## Business Questions Answered

This project answers key business questions such as:

* How do sales and revenue evolve over time?
* Are there seasonal patterns or trends?
* Which products and stores generate the most revenue?
* Who are the most valuable customers?
* Do campaigns significantly increase sales?
* Which salespersons perform the best?

## Tools & Technologies

* SQL Server – Data storage & modeling
* Power BI – Semantic modeling & visualization
* DAX – Advanced analytics & time intelligence
* Excel – Source data

## What This Project Demonstrates

 End-to-end BI workflow, Strong data modeling fundamentals, Advanced DAX & analytical thinking, Business-oriented dashboard design
