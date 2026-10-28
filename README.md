# Northwind Sales Analytics Dashboard (Power BI)

An interactive 3-page Power BI dashboard built on the Northwind sample database. It tracks sales performance, product performance, and customer/order behavior, with filters for year, quarter, country, and product category.

![Sales Overview](images/01SALESOVERVIEW.png)
![Product Analysis](images/PRODUCT%20ANALYSIS.png)
![Customers & Orders](images/CUSTOMERS%20%26%20ORDERS.png)

## Project Overview

**Goal:** Turn raw Northwind order data into a clear, interactive view of the business so a manager can quickly see what is selling, where, to whom, and how it ships.

**Tool:** Microsoft Power BI Desktop (DAX measures, data modeling, Power Query cleaning)

**Dataset:** Northwind (orders, order details, customers, products, categories, employees, shippers)

## Dashboard Pages

### 1. Sales Overview
- **KPI cards:** Total Sales, Total Orders, Units Sold, Average Order Value, Total Shipping
- **Visuals:** Sales Trend Over Time, Sales by Category, Shipping Cost by Shipper, Top 5 Products by Sales, Sales by Country, Sales by Employee, Sales by Year
- **Slicers:** Year, Country, Category

### 2. Product Analysis
- **KPI cards:** Product, Category, Total Sales, Units Sold, Average Order Value
- **Visuals:** Top 10 Products by Units Sold, Top 10 Products by Sales, Sales Mix by Category, Monthly Units Sold, Sales vs Units by Product (scatter), Product Performance Summary table
- **Slicers:** Year, Quarter, Country, Category

### 3. Customers & Orders
- **KPI cards:** Customer, Total Orders, Total Sales, Average Order Value, Total Shipping
- **Visuals:** Orders Over Time, Top 10 Countries by Sales, Orders by Shipper, Orders by Employee, Orders by Country (funnel), Top 10 Customers table
- **Slicers:** Year, Quarter, Country, Category

## Business Questions Answered

| # | Question | Where to find it |
|---|----------|------------------|
| 1 | How are total sales, orders, and average order value performing overall? | Sales Overview – KPI cards |
| 2 | How do sales change over time (monthly and yearly)? | Sales Overview – Sales Trend Over Time, Sales by Year |
| 3 | Which product categories generate the most revenue? | Sales Overview – Sales by Category; Product Analysis – Sales Mix by Category |
| 4 | Which countries generate the most sales? | Sales Overview – Sales by Country; Customers & Orders – Top 10 Countries |
| 5 | Which employees drive the most sales and orders? | Sales Overview – Sales by Employee; Customers & Orders – Orders by Employee |
| 6 | Which shippers cost the most / handle the most orders? | Sales Overview – Shipping Cost by Shipper; Customers & Orders – Orders by Shipper |
| 7 | Which products sell the most by revenue and by units? | Product Analysis – Top 10 charts |
| 8 | Do high-unit products also earn high revenue? | Product Analysis – Sales vs Units scatter |
| 9 | Who are the top customers? | Customers & Orders – Top 10 Customers |
| 10 | How do order volumes trend over time? | Customers & Orders – Orders Over Time |

## Key Insights

> Fill these in from your own dashboard, e.g.:
- Top category by sales: **\_\_\_** (\_\_% of total)
- Top country by sales: **\_\_\_**
- Best-selling product by revenue: **\_\_\_**
- Sales peaked in **\_\_\_** (month/year)
- Most expensive shipper: **\_\_\_**

## Data Preparation (Power Query)

- Imported the Northwind tables and checked data types
- Cleaned the data (removed nulls/duplicates, fixed column types and names)
- Built relationships between orders, customers, products, categories, employees, and shippers
- Created a date hierarchy (Year / Quarter / Month) from `orderDate`

## DAX Measures

Measures used in the report (see the model for exact definitions):

- `Total sales`
- `Total Orders`
- `Unit Sold`
- `Avg order`
- `Total Shipping`

## How to Open

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free, Windows)
2. Download `northwind_dashboard_kpis_fixed.pbix` from this repo
3. Open it in Power BI Desktop

## Repository Structure

```
northwind-powerbi-dashboard/
├── northwind_dashboard_kpis_fixed.pbix
├── README.md
└── images/
    ├── 01_sales_overview.png
    ├── 02_product_analysis.png
    └── 03_customers_orders.png
```

## Author

**Your Name** · [LinkedIn](https://linkedin.com/in/your-profile) · [Portfolio](https://your-portfolio-link)
