# E-Commerce Business Analytics Dashboard

An end-to-end analytics project on the **Olist Brazilian E-Commerce Public Dataset**. I turned multiple raw CSV files into clean, analysis-ready data and built a five-page interactive Power BI report covering sales, products, customers, regions and fulfilment.

*Completed as part of the CodSoft Data Analytics Internship (Week 3).*

---

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Tools Used](#tools-used)
- [Workflow](#workflow)
- [Excel Workbook](#excel-workbook)
- [Power BI Dashboard](#power-bi-dashboard)
- [Key Findings](#key-findings)
- [Data Limitations](#data-limitations)
- [Repository Structure](#repository-structure)
- [Skills Demonstrated](#skills-demonstrated)
- [Author](#author)

---

## Overview

The goal was to study how an e-commerce business is performing by answering questions such as:

- How do sales change over time?
- Which products and categories perform best?
- How active are customers, and how many come back?
- Which states generate the most revenue?
- How do freight costs and order status affect fulfilment?

I also documented what the data **cannot** tell us, so the final report doesn't claim more than the source supports.

## Dataset

**Source:** [Brazilian E-Commerce Public Dataset by Olist (Kaggle)](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

The dataset is a set of related CSV files:

| Data area | Used for |
| --- | --- |
| Orders | Order status, purchase timestamps, links to customers |
| Order items | Item-level sales, product and seller references, item price, freight value |
| Customers | Customer identifiers and location |
| Products & category translation | Product details and readable category names |
| Payments & reviews | Payment methods/amounts and customer reviews (analysed separately) |
| Sellers & geolocation | Seller attributes and geographic reference data |

Raw files were kept untouched. All work used cleaned copies.

## Tools Used

| Tool | How I used it |
| --- | --- |
| **Microsoft Excel** | Documentation (data dictionary, cleaning log, transformations) and structured analysis |
| **Python (Pandas) in Google Colab** | Loading, inspecting, cleaning, transforming, analysing and exporting data |
| **Power BI** | Data model, DAX measures, date analysis, slicers and the interactive report |

## Workflow

1. **Reviewed** the dataset and how the files relate to each other.
2. **Documented** fields, cleaning decisions and transformations.
3. **Cleaned and prepared** the data in Google Colab and saved cleaned CSVs without touching the raw files.
4. **Built analysis outputs:** yearly, quarterly and monthly sales; product and category performance; customers; states; payments; reviews; freight.
5. **Created a sales-detail table** by combining order items with order, customer, product and category data.
6. **Designed the Power BI report** around separate business questions.

## Excel Workbook

The workbook has ten sheets so a reviewer can follow the project without reading any code.

| Sheet | Purpose |
| --- | --- |
| 01_Project_Info | Overview, objectives, tools, workflow |
| 02_Data_Dictionary | Descriptions of key fields |
| 03_Cleaning_Log | Cleaning actions and decisions |
| 04_Transformation | Transformations and derived fields |
| 05_KPI_Summary | Key performance indicators |
| 06_Sales_Trend | Time-based sales analysis |
| 07_Product_Category | Product and category performance |
| 08_Customer_Analysis | Customer activity and repeat customers |
| 09_Regional_Analysis | State-level analysis |
| 10_Insights_Recommendations | Findings, recommendations, priorities, limitations |

## Power BI Dashboard

A five-page report built on an item-level sales fact table connected to dimension tables, with DAX measures, a date table, and slicers for year, category and state.

| Page | What it shows |
| --- | --- |
| **1. Executive Overview** | Headline KPIs, monthly revenue trend, yearly revenue |
| **2. Product & Category** | Revenue and order-item volume by category, top products, average item price |
| **3. Customer & Regional** | Customer and repeat-customer metrics, revenue per customer, revenue and customers by state |
| **4. Sales & Fulfilment** | Revenue vs freight, order-status analysis, freight-heavy categories and states |
| **5. Insights & Recommendations** | Dynamic best-performing year/state/category/product, customer-type comparison, recommendations, limitations |

**DAX measures include:** total revenue, total orders, total customers, average order value, order-item count, freight metrics, repeat-customer measures, average item price and year-over-year revenue.

## Data Limitations

Being clear about what the data does not contain was a deliberate part of this project.

- **No profit or margins:** the data has item price and freight value but no product cost, so revenue is not treated as profit.
- **No discounts:** there is no reliable discount field, so no discount percentages were calculated.
- **Order items are not units:** each row is an order line, so counts are reported as line volume, not units sold.
- **Repeat customers:** the unique customer identifier was used to separate repeat behaviour from order-level customer records.
- **Payments and reviews:** kept apart from item-level sales totals, because multiple records per order could double-count revenue.
- **Regions:** analysis uses customer state, since the source has no ready-made business-region field.

## Repository Structure

> Placeholder names. Rename to match your actual folders and files.

```
├── data/
│   ├── raw/                  # original Olist CSV files (see note below)
│   └── cleaned/              # cleaned CSVs
├── excel/
│   └── Ecommerce_Analysis.xlsx
├── python/
│   └── Ecommerce_Analysis.ipynb
├── outputs/                  # KPI, trend, category, customer, state, freight summaries
├── powerbi/
│   └── Ecommerce_Dashboard.pbix
├── screenshots/
├── docs/
│   └── Project_Report.pdf
└── README.md
```

**Note on the data:** the raw dataset is large and comes from Kaggle. Check its licence and size before uploading it, or link to the source instead.

## Skills Demonstrated

- Data cleaning and preparation with Python (Pandas)
- Working with related tables, keys and data granularity
- Defining KPIs and building DAX measures
- Time-based analysis with a date table
- Interactive dashboard design with slicers and filters
- Documenting cleaning steps and data limitations

## Author

**Manoj**
CodSoft Data Analytics Intern
