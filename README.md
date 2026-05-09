# FNP Sales Analysis Dashboard

![Made with Excel](https://img.shields.io/badge/Made%20with-Excel-217346?logo=microsoft-excel&logoColor=white)
![Project Type](https://img.shields.io/badge/Project-Data%20Analysis-blue)
![Dataset](https://img.shields.io/badge/Dataset-Kaggle-20BEFF?logo=kaggle&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Level](https://img.shields.io/badge/Level-Beginner--Intermediate-orange)

---

## 📌 Project Overview

**FNP (Ferns N Petals)** is one of India's leading gifting and flower delivery brands, operating across 125+ cities and catering to occasions like Diwali, Raksha Bandhan, Valentine's Day, Anniversaries, and Birthdays.

This project analyzes FNP's transactional sales data to answer 10 real business questions around revenue, product performance, customer behavior, delivery efficiency, and seasonal trends — all presented through an interactive Excel dashboard.

**Business Questions Answered:**
1. What is the total revenue generated?
2. What is the average order and delivery time?
3. How does sales performance vary month by month?
4. Which products generate the most revenue?
5. How much do customers spend on average?
6. Which are the top 5 products by revenue?
7. Which are the top 10 cities by order volume?
8. Does order quantity affect delivery time?
9. How does revenue compare across different occasions?
10. Which products are most popular per occasion?

---

## 📂 Dataset Details

> **Note:** This is a structured dummy dataset commonly used for data analysis practice, sourced from Kaggle. It simulates real-world gifting platform operations for educational purposes.

**Dataset Link:** https://www.kaggle.com/datasets/shahzarkhanlavi/ferns-and-petals-sales-dataset?select=products.csv
The dataset consists of **3 CSV files** with a total of **1,000 order records**:

### `orders.csv`
| Column | Description |
|---|---|
| Order_ID | Unique identifier for each order |
| Customer_ID | Links to the customer record |
| Product_ID | Links to the product record |
| Order_Date | Date the order was placed |
| Delivery_Date | Date the order was delivered |
| Quantity | Number of units ordered |

### `products.csv`
| Column | Description |
|---|---|
| Product_ID | Unique product identifier |
| Product_Name | Name of the gift/product |
| Category | Product category (Flowers, Soft Toys, Cakes, Colors, Plants, etc.) |
| Price (₹) | Unit price of the product |
| Occasion | Associated occasion (Anniversary, Raksha Bandhan, Diwali, etc.) |

### `customers.csv`
| Column | Description |
|---|---|
| Customer_ID | Unique customer identifier |
| Customer_Name | Name of the customer |
| City | Delivery city |
| Gender | Customer gender |
| Contact & Address | Contact details |

**Dataset Summary:**

| Metric | Value |
|---|---|
| Total Orders | 1,000 |
| Total Customers | 100 |
| Time Period | April 2023 – October 2024 |
| Total Revenue | ₹35,20,984 |
| Average Order Value (AOV) | ₹3,520.98 |
| Average Product Price | ₹1,156.11 |
| Average Delivery Time | 5.53 days |

---

## 🛠️ Tools & Techniques Used

| Tool / Feature | Purpose |
|---|---|
| Microsoft Excel | Primary tool for analysis and dashboard |
| Power Query (ETL) | Data import, cleaning, merging 3 CSV files |
| Power Pivot | Star Schema data modeling and table relationships |
| Pivot Tables | Multi-dimensional data aggregation |
| Pivot Charts | Visual representation of insights |
| Slicers & Timelines | Interactive dashboard filtering |
| Conditional Formatting | Highlighting trends and outliers |
| Calculated Columns | Revenue = Quantity × Price, Delivery Days |

---

## ⭐ Data Model — Star Schema

```
        [customers.csv]
              |
              | Customer_ID
              |
[products.csv] — Product_ID — [orders.csv] ← Fact Table
                                    |
                         (Revenue, Quantity,
                          Order Date, Delivery Date)
```

The **Orders table** acts as the central fact table, linked to Products and Customers as dimension tables. This star schema enables clean, efficient PivotTable analysis across all business questions.

---

## 📊 Dashboard Features

The dashboard is built on a single interactive sheet with:

- **KPI Cards** — Total Revenue, AOV, Average Price, Total Orders, Total Customers, Avg Delivery Time
- **Revenue by Occasion** — Bar chart comparing Anniversary, Raksha Bandhan, Diwali, Valentine's Day, etc.
- **Revenue by Category** — Colors, Soft Toys, Cakes, Plants, and more
- **Monthly Sales Trend** — Line chart showing month-wise fluctuation across 2023–2024
- **Top Products by Revenue** — Ranked list of highest-earning products
- **Top 10 Cities by Orders** — City-level order volume comparison
- **Revenue by Hour** — Peak sales time analysis
- **Slicers** — Filter by Occasion, Month, City in one click

---

## 🔍 Key Insights Discovered

- **Total Revenue: ₹35,20,984** across 1,000 orders from 100 customers
- **Anniversary and Raksha Bandhan** were the highest-revenue occasions — critical for seasonal marketing planning
- **Colors category** led revenue, followed by **Soft Toys** — Raksha Bandhan themed products performed consistently
- **Sales peaked in August** — driven by Raksha Bandhan gifting demand
- **Late morning to early afternoon** hours saw the highest order activity — useful for targeted ad campaigns
- **Average delivery time of 5.53 days** suggests room for logistics improvement
- The **top 10 cities** contributed a disproportionate share of orders — typical Pareto pattern in e-commerce

---

## 📁 Repository Structure

```
fnp-sales-analysis-excel-dashboard/
│
├── Dataset/                  # Raw CSV files (orders, products, customers)
├── Dashboard_File/           # Final Excel dashboard (.xlsx)
├── Dashboard_Screenshots/    # Screenshots of dashboard views
├── Video_Demo/               # Walkthrough video of the dashboard
└── README.md
```

---
## ▶️ How to Use

1. Clone or download this repository
2. Open the `.xlsx` file inside `Dashboard_File/` in **Microsoft Excel 2016 or later**
3. Navigate to the **Dashboard** sheet
4. Use the **Slicers** to filter by Occasion, City, or Month
5. All charts update automatically based on your selection

---

## 🎯 What I Learned

- ETL workflow using Power Query to clean and merge multiple CSV files
- Building a Star Schema data model using Power Pivot
- Designing an interactive, business-ready dashboard in Excel
- Identifying actionable business insights from transactional data
- Presenting findings clearly for non-technical stakeholders

---

## 🚀 Future Improvements

- Rebuild this analysis in **Python (Pandas + Matplotlib/Seaborn)**
- Create an interactive version using **Power BI** or **Tableau**
- Add **forecasting** using time series analysis
- Automate data refresh using Python scripts

---

## 👤 About Me

**Pramod Patil** — Final year engineering student building skills in Data Analysis and Machine Learning.

📧 pramodpatil0520@gmail.com | 🔗 www.linkedin.com/in/pramod-patil-a00309265 | 🐙 https://github.com/pramodpatil0520
Open to **fresher and internship opportunities** in Data Analytics / Data Science.
