# Data-base-AI


📊 Sales Performance Analysis

End-to-End Data Analytics Project

Analyze retail sales, discover business trends, and turn raw data into actionable insights.


Python
SQL
Pandas
Dashboard
Charts





🎯 Project Overview

This project demonstrates an end-to-end data analytics workflow using a fictional retail business dataset. It combines a relational database, SQL analysis, Python data preparation, and an interactive dashboard.



Dataset disclaimer: All records are synthetic sample data generated for this portfolio project. They do not represent a real company.



✨ What You Can Explore

📌 KPI / Analysis	🔎 Description
💰 Total Revenue	Revenue from completed orders
🧾 Completed Orders	Number of completed orders
🛒 Average Order Value	Average revenue per completed order
📦 Units Sold	Total quantity sold
🏬 Branch Performance	Revenue comparison across branches
🏆 Top Products	Best-performing products and categories
👥 Top Customers	Highest-value customers
📈 Monthly Trends	Revenue over time

🧰 Tech Stack


🐍 Python — project logic and data processing

🗄️ SQLite / SQL — relational database and analytical queries

🧹 Pandas — data cleaning and aggregation

📊 Plotly — interactive charts

🎛️ Streamlit — interactive dashboard


🗂️ Project Structure

sales_performance_analysis/
├── app.py                         # Interactive Streamlit dashboard
├── requirements.txt               # Python dependencies
├── README.md                      # Project documentation
├── data/
│   └── sales.db                   # Generated SQLite database
├── sql/
│   ├── schema.sql                 # Database tables and relationships
│   └── analysis_queries.sql       # Business analysis queries
└── src/
    ├── create_database.py         # Generates fictional sample data
    └── analysis.py                # Data loading and KPI calculations

🗄️ Database Schema

The database contains five related tables:


erDiagram
    BRANCHES ||--o{ ORDERS : receives
    CUSTOMERS ||--o{ ORDERS : places
    ORDERS ||--|{ ORDER_ITEMS : contains
    PRODUCTS ||--o{ ORDER_ITEMS : appears_in
    BRANCHES { int branch_id PK string branch_name string city }
    CUSTOMERS { int customer_id PK string customer_name string email date signup_date }
    ORDERS { int order_id PK int customer_id FK int branch_id FK date order_date string status }
    PRODUCTS { int product_id PK string product_name string category float unit_cost float list_price }
    ORDER_ITEMS { int order_item_id PK int order_id FK int product_id FK int quantity float unit_price float discount }

🔄 Project Workflow

flowchart TD
    A[🗄️ SQLite Database] --> B[🔍 SQL Queries]
    B --> C[🐍 Python and Pandas]
    C --> D[🧹 Prepare and Analyze Data]
    D --> E[📊 Plotly Visualizations]
    E --> F[🎛️ Streamlit Dashboard]
    F --> G[💡 Business Insights]

🚀 Run the Project

1. Clone the repository

git clone https://github.com/YOUR-USERNAME/Sales-Performance-Analysis.git
cd Sales-Performance-Analysis

2. Create and activate a virtual environment

python -m venv .venv

# Windows
.venv\\Scripts\\activate
# macOS / Linux
source .venv/bin/activate

3. Install dependencies

pip install -r requirements.txt

4. Generate the sample database

python src/create_database.py

5. Launch the dashboard

streamlit run app.py

Streamlit will show a local address, usually http://localhost:8501.


📊 Dashboard Features


KPI cards for revenue, completed orders, average order value, and units sold

Monthly revenue trend

Revenue by branch

Top 10 products

Revenue by category

Top customers

Filters and CSV export


🧠 Business Questions


Which months generated the highest revenue?

Which branch performs best?

Which products and categories contribute most to revenue?

Who are the highest-value customers?

What is the average order value?


🧮 Revenue Definition

Only orders with Completed status are included in the sales analysis.


Line Revenue = Quantity × Unit Price × (1 − Discount)


Average Order Value = Total Revenue ÷ Number of Completed Orders


📁 SQL Analysis

The file sql/analysis_queries.sql includes queries for overall KPIs, monthly revenue, top products, branch performance, highest-value customers, and category performance.


⚠️ Notes and Limitations


The database is generated locally by the script; it is not a real company database.

Revenue is calculated from order-item prices after discounts.

Currency is intentionally unspecified; confirm the currency before interpreting amounts.

This is a portfolio demonstration and should be validated and adapted before real business use.


👨‍💻 Author

YOUR NAME
Data Analytics | SQL | Python | Data Visualization





⭐ If you find this project useful, consider giving the repository a star!


Made with 🐍 Python, 🗄️ SQL, and 📊 curiosity.
