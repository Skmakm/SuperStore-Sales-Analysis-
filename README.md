# SuperStore-Sales-Analysis
This repository contains an in-depth analysis of the SuperStore sales dataset. The goal is to uncover insights into sales performance, customer behavior, and product profitability to provide actionable recommendations for the business.

Table of Contents
Problem Statement

Dataset Description

Data Cleaning

Data Analysis

Problem Statement
The primary objective of this analysis is to identify key drivers of sales and profit for the SuperStore. We aim to answer critical business questions such as:

What are the overall sales trends over time?

Which product categories and sub-categories are the most and least profitable?

Who are the most valuable customers and in which regions are they located?

How does ship mode affect sales and customer satisfaction?

What are the areas where the business can optimize its operations to increase profitability?

Dataset Description
The dataset used for this analysis is SuperStore_Sales_Dataset.csv. After cleaning and feature engineering, the final dataset includes the following columns:

Row ID: A unique identifier for each row.

Order ID: An identifier for each order.

Order Date: The date the order was placed.

Ship Date: The date the order was shipped.

Ship Mode: The shipping method used for the order.

Customer ID: A unique identifier for each customer.

Customer Name: The name of the customer.

Segment: The market segment the customer belongs to (e.g., Consumer, Corporate).

Country: The country where the order was placed.

City: The city where the order was placed.

State: The state where the order was placed.

Region: The geographical region.

Product ID: A unique identifier for each product.

Category: The main category of the product.

Sub-Category: The sub-category of the product.

Product Name: The name of the product.

Sales: The total sales amount for the order line.

Quantity: The number of units of the product ordered.

Profit: The profit generated from the order line.

Returns: Information on whether the product was returned.

Payment Mode: The method of payment used.

Avg Days: The number of days between the order date and ship date.

Data Cleaning
Data was imported and transformed using Power Query in Power BI.

Steps to Import Data
Navigate to Get data → More → All → Folder → Connect  

Provide the dataset folder path → Click OK  

Open Power Query editor with Transform Data 

The following DAX query was used to create a calculated column for shipping duration:
Avg Days = DATEDIFF('SuperStore_Sales'[Order Date],'SuperStore_Sales'[Ship Date],DAY)

Data Analysis
The cleaned dataset was used to build an interactive Power BI dashboard to visualize sales performance and forecast future trends.

Dashboards Included
Sales Performance Dashboard: Provides a comprehensive overview of KPIs, sales by region, segment, category, and customer preferences.

Sales Forecast Dashboard: Visualizes historical sales trends and projects future sales.

Key Insights
Geographical & Customer Insights

Regional Dominance: The West (33%) and East (29%) regions are the primary markets. This is further highlighted by state-level data, which identifies California and New York as the top two revenue-generating states.

Dominant Customer Segment: The Consumer segment is the most significant contributor to revenue, accounting for 48% of all sales.

Key Revenue-Driving Products: While Office Supplies is the largest category by sales volume, the top-performing sub-categories driving revenue are Phones, Chairs, and Binders.

Operational & Customer Preferences: Standard Class is the most utilized shipping method, while Cash on Delivery (COD) is the preferred payment method, used in 43% of transactions.

Growth Trajectory & Seasonality: A clear year-over-year growth trend in sales and profit is visible from 2019 to 2020. The sales forecast confirms this upward trend is expected to continue. The data also shows a strong seasonal pattern, with sales consistently peaking in the final quarter (October-December).
