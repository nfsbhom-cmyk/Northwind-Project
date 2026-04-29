📊 Case Study: Northwind Sales & Customer Analytics
🧩 1. Project Overview
This project focuses on analyzing the Northwind retail dataset, a multi-table business database containing order transactions, order details, and customer-related information.
The goal was to:
•	Clean and integrate relational data 
•	Build meaningful business KPIs 
•	Analyze sales performance, customer behavior, and shipping efficiency 
•	Create an interactive dashboard in IBM Cognos Analytics 
________________________________________
📁 2. Dataset Description
The dataset consisted of two primary relational tables:
1. Orders Table
Contains order-level information:
•	order_id 
•	customer_id 
•	order_date 
•	ship_date 
•	region 
•	postal_code 
2. Order Details Table
Contains line-item transaction data:
•	order_id 
•	product_id 
•	unit_price 
•	quantity 
________________________________________
🧹 3. Data Cleaning Process (Python)
Data cleaning was performed using Python (Pandas):
Key steps:
•	Removed duplicate records 
•	Converted date fields to datetime format 
•	Handled missing values in: 
o	ship_date → imputed using average shipping duration 
o	region & postal_code → filled with “Unknown” 
•	Created a derived column: 
o	Revenue = unit_price × quantity 
________________________________________
🔗 4. Data Integration (Merging Process)
A relational merge was performed:
•	order_details was merged with orders using order_id 
This created a unified dataset containing:
•	Order-level information 
•	Product-level transaction data 
•	Customer and regional information 
This ensured analysis could be performed at a single unified grain level (order line item level).
________________________________________
🧠 5. Feature Engineering
New analytical features were created:
•	Revenue 
•	Shipping Days = ship_date − order_date 
•	Order Month (for trend analysis) 
These features enabled time-based and performance analysis.
________________________________________
📊 6. Exploratory Data Analysis (EDA)
Key business questions answered:
💰 Revenue Analysis
•	Total revenue generated 
•	Revenue distribution across orders 
•	Top revenue-generating orders 
👥 Customer Analysis
•	Top customers by revenue contribution 
•	Customer purchase behavior 
📦 Order Behavior
•	Average Order Value (AOV) 
•	Order size distribution (items per order) 
📈 Time Analysis
•	Monthly revenue trends 
•	Seasonal fluctuations in sales 
🚚 Operational Analysis
•	Average shipping time 
•	Shipping efficiency trends 
________________________________________
🧮 7. Key KPI Definitions
✔ Total Revenue
Sum of all transaction revenue
✔ Total Orders
Count of distinct order IDs
✔ Total Customers
Count of distinct customer IDs
✔ Average Order Value (AOV)
Total Revenue ÷ Number of Orders
✔ Average Shipping Days
Average difference between ship_date and order_date
________________________________________
⚠️ 8. Data Challenges & Solutions
Issue 1: Missing ship_date
•	Solution: Imputed using:
order_date + average shipping duration
Issue 2: Missing region & postal code
•	Solution: Filled with "Unknown" to preserve dataset integrity 
Issue 3: COUNT DISTINCT issue in Cognos
•	Solution: Used correct syntax:
count(distinct order_id)
________________________________________
📊 9. IBM Cognos Dashboard
The cleaned dataset was imported into IBM Cognos Analytics to build an interactive dashboard.
Dashboard Structure:
🟦 KPI Section (Top Row)
•	Total Revenue 
•	Total Orders 
•	Total Customers 
•	Average Order Value 
📈 Revenue Trend
•	Monthly revenue line chart 
🏆 Customer Insights
•	Top 10 customers by revenue 
📦 Order Insights
•	Order size distribution 
🌍 Regional Analysis
•	Revenue by region 
🚚 Order id Insight
•	Top 10 Order id  
________________________________________
🎯 10. Key Insights
•	A small group of customers contributed a significant portion of revenue 
•	Revenue showed clear monthly fluctuations indicating seasonal demand 
•	Average order value helped identify customer spending behavior 
•	Shipping delays were measurable and could impact customer satisfaction 
________________________________________
🧠 11. Tools Used
•	Python (Pandas, Matplotlib) 
•	IBM Cognos Analytics 
•	Excel (data inspection) 
•	SQL-style thinking for joins and aggregation 
________________________________________
🏁 12. Conclusion
This project demonstrates an end-to-end data analytics workflow:
•	Data cleaning and transformation 
•	Relational data merging 
•	KPI development 
•	Business insight generation 
•	Dashboard creation 
It showcases the ability to handle structured business data and extract actionable insights for decision-making.


