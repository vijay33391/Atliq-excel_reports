# 📊 Atliq Hardware Sales Performance Analysis P & L performance analysis — End-to-End Reporting Project

This repository showcases my complete end-to-end Business Intelligence project where I analyzed sales performance for **Atliq Hardware**. The project involved **data collection, cleaning, modeling, DAX measure creation, and report generation** using Excel Power Pivot and Power Query.

---

## 🎯 Project Objective

- Analyze historical sales performance (2019 - 2021) for Atliq Hardware.
- Build an integrated data model from multiple raw data sources.
- Create interactive, management-ready reports.
- Monitor YoY growth, sales targets, and identify performance gaps.
- Gain hands-on experience with Excel BI stack: Power Query, Power Pivot, DAX, Data Modeling.

---

## 🛠 Tools & Technologies Used

- **Excel Power Pivot** (Data Modeling)
- **Power Query** (Data Cleaning & ETL)
- **DAX** (Measures, KPIs & Calculations)
- **Pivot Tables** (Report Generation)
- **Data Visualization (Charts, Tables, KPIs)**

---

## 📂 Data Sources

Collected and integrated multiple datasets including:

| File Name | Description |
|-----------|-------------|
| `fact_sales_monthly.xlsx` | Monthly sales data with customer, product, and financials |
| `fact_sales_monthly_with_cost.xlsx` | Extended sales data with cost components |
| `ns_targets_2021.xlsx` | Net Sales targets for year 2021 |
| `dim_product.xlsx` | Product hierarchy master data |
| `dim_customer.xlsx` | Customer segmentation and geography |
| `dim_market.xlsx` | Market hierarchy data |
| `dim_date.xlsx` | Date dimension with calendar and fiscal year mapping |

---

## 🧹 Data Cleaning Process

Performed using Power Query:

- Standardized column names across all datasets.
- Corrected data types for numerical, categorical & date fields.
- Merged datasets to ensure referential integrity.
- Removed duplicates & handled missing values.
- Validated foreign key relationships for building data model.

---

## 🗄 Data Modeling — Star Schema Design

Built relational data model in Power Pivot using Star Schema:

- Fact Tables:
  - Sales Fact (`fact_sales_monthly`)
  - Sales + Cost Fact (`fact_sales_monthly_with_cost`)
  - Sales Targets (`ns_targets_2021`)
- Dimension Tables:
  - `dim_product` (Product hierarchy)
  - `dim_customer` (Customer details)
  - `dim_market` (Market hierarchy)
  - `dim_date` (Time dimension)

### Relationships Established:

- Product Code → Product
- Customer Code → Customer
- Date → Sales Date
- Market → Region / Subzone

*(Refer to uploaded `relationships.png` for data model diagram)*

---

## 📐 DAX Measures Created

Created multiple DAX measures to derive KPIs for reporting:

| Measure | Description |
|---------|-------------|
| **Net Sales** | `SUM(fact_sales_monthly[net_sales_amount])` |
| **YoY Growth %** | `(Net Sales CY - Net Sales PY) / Net Sales PY` |
| **Sales vs Target Diff %** | `(Actual - Target) / Target` |
| **Cost Metrics** | Calculated total cost using manufacturing and freight components |
| **Cumulative Sales** | Rolling YTD calculations |
| **Market Performance** | Sales split by Region, Subzone, Market |

These measures allow flexible slicing and dicing across dimensions.

---

## 📊 Report Generation

### 1️⃣ Net Sales Report (`Net Saels Report.pdf`)

- Customer-wise sales from 2019 to 2021.
- YoY growth calculated (`21 vs 20` growth %).
- Identified top growing customers like Amazon, Flipkart, Atliq Exclusive.

### 2️⃣ Net Sales vs Target Report (`Ns vs Target.pdf`)

- Region & Market-wise comparison of actual sales vs target for 2021.
- Calculated both absolute variance and % variance to highlight under/over performing regions.
- Key findings:
  - India, USA, South Korea driving major sales.
  - Some regions like Poland, Canada, Spain underperformed against targets.

---

## 🚀 Key Business Insights Derived

- 2021 witnessed strong YoY growth across several key customers.
- Amazon and Flipkart had >200% YoY growth.
- India remains the largest single market contributing ~161M sales.
- Overall performance against targets was slightly below expectations (-9.2% overall gap).
- Certain smaller markets showed highly volatile performance (both over and under target).

---

## 💡 My Learnings from This Project

- ✅ Mastered Power Query for professional ETL operations.
- ✅ Gained experience in building Star Schema models in Power Pivot.
- ✅ Learned advanced DAX for KPI calculations and business logic.
- ✅ Developed reusable, dynamic reporting models suitable for real-world BI applications.
- ✅ Understood how raw data flows end-to-end from raw tables → models → executive reports.

---

## 📌 Limitations & Future Scope

- Current reports are based on Excel; can be scaled into Power BI dashboards.
- Can add forecasting models for predictive sales estimation.
- Potential to integrate live data refresh for real-time reporting.
- Scope for deeper profitability and customer segmentation analysis.

---

## 📖 Author

- **Your Name**
- GitHub: [vijay vardhan](https://github.com/vijay33391)
- LinkedIn: [https://www.linkedin.com/in/p-vijaya-vardhan-03179527b/]



