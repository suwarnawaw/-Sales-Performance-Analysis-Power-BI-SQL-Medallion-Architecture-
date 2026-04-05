# -Sales-Performance-Analysis-SQL Server source data-Microsoft Power BI with Medallion-Architecture
This project presents an end-to-end Sales Analytics solution built using SQL Server data source, Power BI with Medallion Architecture. It transforms raw transactional data into meaningful business insights through structured data layers and interactive dashboards.

The solution enables stakeholders to:

Track Sales KPIs
Analyze YoY and MoM performance
Identify top-performing brands, categories, and states
Monitor geographical sales distribution

🧱 Architecture: Medallion Data Layers

This project follows the Medallion Architecture approach for scalable and maintainable data processing:

        ┌───────────────┐
        │   Bronze      │  → Raw Data (SSMS Tables)
        └───────────────┘
                 ↓
        ┌───────────────┐
        │   Silver      │  → Cleaned & Transformed Data
        └───────────────┘
                 ↓
        ┌───────────────┐
        │   Gold        │  → Aggregated Business Layer
        └───────────────┘
                 ↓
        📊 Power BI Dashboard

🥉 Bronze Layer (Raw Data)
Source: SQL Server (SSMS)
Contains raw ingested tables such as:
Sales Transactions
Product Details
Customer/Geography Data

🔹 Characteristics:
No transformations
Historical raw data preserved
Used for traceability and auditing

🥈 Silver Layer (Cleaned & Modeled Data)
Data is cleaned, validated, and transformed using SQL

🔹 Key transformations:
Handling nulls and duplicates
Data type standardization
Joins between fact and dimension tables
Derived columns:
Sales = Price × Quantity
Profit = Sales – COGS

🔹 Output:
Structured Fact & Dimension tables
Fact_Sales
Dim_Product
Dim_Date
Dim_Geography

🥇 Gold Layer (Business Aggregates)
Optimized for reporting and analytics

🔹 Includes:
Pre-aggregated tables
KPI-ready datasets

🔹 Metrics created:
Total Sales
Total Net Profit
Total Orders
Total Quantity Sold
Avg Order Price
YoY Growth %
MoM Growth %

📊 Dashboard Features

1️⃣ Executive Summary
KPI Cards:
Total Sales: 10M
Net Profit: 6M
Quantity Sold: 50K
Orders: 450M
COGS: 4M
YoY & MoM Performance Tables
Sales Trend by Year

2️⃣ Sales Insights
Sales by Brand
Sales by Category
Monthly Sales Trend
Dynamic Measure Selector (Sales, Profit, Orders, etc.)

3️⃣ Geographic Analysis
Sales by State (Bar Chart)
US Map Visualization
Key Insight:
California and Texas are top-performing states

🛠️ Tech Stack
Layer	Technology Used
Data Source	SQL Server (SSMS)
Processing	SQL
Modeling	Star Schema
Visualization	Power BI
Architecture	Medallion (Bronze-Silver-Gold)

📌 Key Business Insights
📈 Sales dropped significantly after 2019 → potential business issue
🏆 Brand 5 and Brand 9 are top contributors
🌎 California leads in total sales
📅 Seasonal spikes observed in mid-year months

📷 Dashboard Preview
Executive Summary
https://github.com/suwarnawaw/-Sales-Performance-Analysis-Power-BI-SQL-Medallion-Architecture-/blob/main/Sales%20Performance%20Analysis%20-%20SSMS%20Source%20Data.png

Map Visualization
https://github.com/suwarnawaw/-Sales-Performance-Analysis-Power-BI-SQL-Medallion-Architecture-/blob/main/Sales%20Performance%20Analysis%20-%20SSMS%20Source%20Data1.png

💡 Key Learnings
Implemented end-to-end data pipeline design
Built scalable layered architecture
Created dynamic Power BI dashboards
Applied advanced DAX calculations
Improved storytelling using data visualization

🔮 Future Enhancements
Add real-time data pipeline (Azure / Fabric)
Implement Row-Level Security (RLS)
Integrate forecasting models
Automate refresh using pipelines

📬 Connect With Me - If you are interested in Power BI, Data Analytics, or Business Intelligence solutions, feel free to connect. suwarna.w@gmail.com https://www.linkedin.com/in/suwarnamala-wawhal

👩‍💻 Author
Suwarnamala Wawhal
Power BI Developer / Data Analytics Professional
Pune, Maharashtra - 9158587153
https://www.linkedin.com/in/suwarnamala-wawhal
