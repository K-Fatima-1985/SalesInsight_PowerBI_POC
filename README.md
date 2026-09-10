# 📊 Sales Insight Dashboard – Power BI POC

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-Learning-blue)
![Project Type](https://img.shields.io/badge/Project-POC-success)

## 📌 Project Overview

**Sales Insight Dashboard** is a Power BI Proof of Concept (POC) created to demonstrate practical skills in **data visualization, business analysis, DAX measures, filtering, and interactive dashboard design**.

The dashboard converts sales data into interactive business insights related to:

- Revenue
- Sales quantity
- Profit margin
- Revenue contribution
- Profit contribution
- Market/zone performance
- Product performance
- Customer performance
- Revenue trends over time

> **Purpose:** This project is designed as a portfolio project to demonstrate Power BI skills to recruiters and hiring managers.

---

## 🎯 Business Objective

The main objective of this dashboard is to help a business answer questions such as:

1. How is revenue changing over time?
2. Which products generate the most revenue?
3. Which customers contribute the most revenue?
4. Which markets perform best?
5. What percentage of revenue comes from each market?
6. Which markets contribute most to profit?
7. How is profit margin changing?
8. How does current revenue compare with the previous year?
9. How much sales quantity has been generated?
10. Which customers and markets require further attention?

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Microsoft Power BI** | Data modeling, DAX, dashboard development and visualization |
| **Power Query** | Data preparation and transformation |
| **DAX** | Measures and business calculations |
| **Excel / Tabular Data** | Source-data preparation, where applicable |
| **GitHub** | Project documentation and portfolio hosting |

---

## 📄 Dashboard Pages

The Power BI report contains **three main analytical pages**.

### 1. Key Insights

This page provides a high-level view of sales performance.

**Visuals include:**

- Revenue KPI
- Sales Quantity KPI
- Revenue Trend
- Top 5 Products by Revenue
- Revenue by Markets
- Top 5 Customers
- Sales Quantity by Markets
- Year/date filters

**Purpose:** Quickly understand the overall sales picture and identify major contributors.

![Key Insights](images/key-insights.png)

---

### 2. Profit Analysis

This page focuses on profitability and contribution analysis.

**Visuals include:**

- Sales Quantity KPI
- Revenue KPI
- Total Profit Margin KPI
- Revenue Trend
- Profit Contribution % by Markets
- Revenue Contribution % by Markets
- Profit % by Markets
- Top 5 Customers by Revenue
- Year/date filters

**Purpose:** Understand where revenue and profit are being generated and compare market-level performance.

![Profit Analysis](images/profit-analysis.png)

---

### 3. Performance Insights

This page focuses on performance trends and comparative analysis.

**Visuals include:**

- Revenue KPI
- Sales Quantity KPI
- Total Profit Margin KPI
- Revenue vs Previous Year
- Profit Margin %
- Revenue Contribution % by Market Zones
- Top 5 Customers by Revenue
- Year/date filters
- Profit Target filter

**Purpose:** Analyze performance trends and identify opportunities for improvement.

![Performance Insights](images/performance-insights.png)

---

## 📐 Key DAX Measures

The report uses measures such as:

- `Revenue`
- `Revenue LY`
- `Sales Qty`
- `total Profit margin`
- `profit margin %`
- `Revenue contribution %`
- `Profit margin contribution %`

These measures are used throughout the report to create KPI cards, trend analysis, contribution analysis and market/customer comparisons.

### Example DAX Pattern

A typical revenue measure can be written as:

```DAX
Revenue =
SUMX(
    Sales,
    Sales[Quantity] * Sales[Unit_Price]
)
```

> Replace the example table/column names with the actual names from your model if they are different.

---

## 🔄 Data Preparation

The project follows a typical Power BI workflow:

```text
Raw Data
   ↓
Power Query
   ↓
Data Cleaning & Transformation
   ↓
Data Model
   ↓
DAX Measures
   ↓
Interactive Visualizations
   ↓
Business Insights
```

Typical preparation activities include:

- Checking data types
- Cleaning inconsistent values
- Handling blanks/nulls
- Removing duplicates where required
- Creating/using date fields
- Preparing fields for analysis
- Creating measures for KPIs
- Building interactive filters/slicers

---

## 🧩 Data Model

The report uses business entities represented by tables/fields such as:

- Sales data
- Sales Date
- Sales Products
- Sales Customers
- Sales Markets
- Base Measures
- Profit Target

The model supports analysis across **time, products, customers and markets**.

---

## 📊 Key Analytical Techniques Demonstrated

### Data Visualization

- KPI Cards
- Line Charts
- Bar Charts
- Tables
- Slicers
- Combo Charts

### Business Analysis

- Top-N analysis
- Contribution percentage
- Year-over-year comparison
- Profitability analysis
- Market comparison
- Customer ranking
- Trend analysis

### Power BI Skills

- Power Query
- DAX measures
- Interactive filtering
- Date hierarchy
- Dashboard/page design
- Drill/filter interactions
- Business-focused storytelling

---

## 💡 Sample Business Insights

The dashboard is designed to help decision-makers identify:

- High-performing products
- High-value customers
- Strong and weak markets
- Revenue trends
- Profitability patterns
- Contribution of individual markets to total revenue/profit
- Changes in performance compared with the previous year

> Add 3–5 exact numerical findings here after reviewing your final dashboard. For example:  
> **“Market A contributed 32% of total revenue.”**  
> **“Product X was the highest-revenue product.”**

Using real figures makes the GitHub project much stronger for recruiters.

---

## 📸 Dashboard Screenshots

GitHub does not provide a Power BI-style interactive report preview directly from a `.pbix` file. Therefore, screenshots are included/recommended to show the dashboard visually.

Recommended images:

```text
images/
├── key-insights.png
├── profit-analysis.png
└── performance-insights.png
```

---

## 📁 Recommended GitHub Repository Structure

```text
Sales-Insight-PowerBI/
│
├── README.md
│
├── PowerBI/
│   └── Sales Insight Dashboard by Fatima.pbix
│
├── Screenshots/
│   ├── key-insights.png
│   ├── profit-analysis.png
│   └── performance-insights.png
│
├── Data/
│   └── sample_sales_data.xlsx
│
├── DAX/
│   └── measures.md
│
├── PowerQuery/
│   └── transformations.md
│
└── Documentation/
    └── project-summary.pdf
```

---

## 🚀 What I Learned From This Project

Through this project, I practiced:

- Building an end-to-end Power BI dashboard
- Preparing data for analysis
- Creating business-focused DAX measures
- Designing interactive reports
- Using slicers and filters
- Performing product/customer/market analysis
- Creating KPI indicators
- Comparing current and previous-year performance
- Presenting data as actionable business insights
- Documenting a Power BI project for a professional portfolio

---

## 👩‍💻 Author

**Fatima Ansari**

Aspiring **Power BI / Data Analyst**

**Core Skills:**
- Power BI
- DAX
- Power Query
- SQL
- Excel
- Data Visualization
- Data Analysis
- AI Tools

---

## 📌 Portfolio Note

This project is a **Proof of Concept (POC)** created for learning and portfolio demonstration.

The project demonstrates the ability to move from:

**Data → Transformation → Modeling → DAX → Visualization → Business Insight**

---

## ⭐ If You Find This Project Useful

Feel free to explore the repository and review the dashboard screenshots, Power BI file, calculations and documentation.
