<div align="center">

# 📊 Sales Analytics & Performance Dashboard

### 📈 Excel-Based Sales Analysis • Customer Insights • Scenario Planning • Regression

<p>
<img src="https://img.shields.io/badge/Microsoft_Excel-Analytics-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white">
<img src="https://img.shields.io/badge/Sales_Data-250_Transactions-4472C4?style=for-the-badge">
<img src="https://img.shields.io/badge/Pivot_Tables-Business_Analysis-6C63FF?style=for-the-badge">
<img src="https://img.shields.io/badge/Dashboard-KPI_Reporting-FF6B35?style=for-the-badge">
</p>

<p>
<img src="https://img.shields.io/badge/XLOOKUP-Customer_Analysis-16A085?style=for-the-badge">
<img src="https://img.shields.io/badge/Scenario_Manager-What--If_Analysis-8E44AD?style=for-the-badge">
<img src="https://img.shields.io/badge/Linear_Regression-Predictive_Analysis-E67E22?style=for-the-badge">
</p>

<br>

**📥 Sales Data → 🧮 Analysis → 🔄 Pivot Tables → 🎯 Scenarios → 📈 Regression → 📊 Dashboard**

</div>

---

## ✨ Project Overview

**Sales Analytics & Performance Dashboard** is a practical Microsoft Excel project created to analyze sales transactions, customer behavior, product performance, payment methods, regions, and customer segments.

The workbook combines **formula-based analysis, customer ranking, product analysis, What-If Scenario Manager, Goal Seek, Linear Regression, PivotTables, and an interactive-style dashboard** into one complete Excel project.

| 🧩 Module | 📌 Purpose |
|---|---|
| 📋 **Data** | Stores transaction, customer, product, payment, region, and sales information |
| 🧮 **Analysis** | Calculates KPIs, customer revenue, purchase frequency, top customers, and products |
| 🎯 **Scenario Summary** | Compares different growth assumptions and projected revenue |
| 📈 **Linear Regression** | Analyzes the relationship between a selected variable and revenue |
| 🔄 **Pivot Table** | Summarizes sales by product, region, customer segment, payment method, and category |
| 📊 **Dashboard** | Presents key sales KPIs and top-product information |

> 💡 **Main Excel File:** `Final_Project.xlsx`

The project is useful for **Excel data-analysis practice, business reporting, practical assignments, dashboard creation, What-If Analysis, PivotTables, and beginner-level predictive analysis**. 🚀

---

# 🗂️ Workbook Structure

```text
📦 Final_Project.xlsx
│
├── 📋 Data
│   └── Sales Transaction Dataset
│
├── 🧮 Analysis
│   └── Customer, Product & KPI Analysis
│
├── 🎯 Scenario Summary
│   └── Growth Scenario Comparison
│
├── 📈 Linear Regression
│   └── Regression Statistics & ANOVA
│
├── 🔄 Pivot Table
│   └── Multi-Dimensional Sales Analysis
│
└── 📊 Dashboard
    └── Sales Performance Overview
```

---

# 📋 Data Sheet

The `Data` sheet contains the main transaction dataset used throughout the project.

The workbook contains **250 sales transactions**.

### 📌 Main Columns

| Column | Purpose |
|---|---|
| `Transaction_ID` | Unique transaction identifier |
| `Date` | Transaction date |
| `Customer_ID` | Customer identifier |
| `Customer_Name` | Customer name |
| `Product_ID` | Product identifier |
| `Product_Name` | Product sold |
| `Category` | Product category |
| `Quantity` | Units purchased |
| `Unit_Price` | Price per unit |
| `Payment_Method` | Payment method used |
| `Region` | Customer/sales region |
| `Customer_Segment` | Basic, Premium, or Standard |
| `Customer_Since` | Customer relationship start date |
| `Total_Amount` | Calculated transaction value |
| `Customer relationship` | Customer relationship duration |
| `Timestamp` | Current timestamp |
| `Abbreviation_Customer_Name` | Customer initials |
| `Eomonth of sales` | Month-end sales date |
| `Sales Month` | Month extracted from transaction date |

### 🧮 Important Data Formulas

**Total Amount**

```excel
=data[[#This Row],[Quantity]]*data[[#This Row],[Unit_Price]]
```

Calculates transaction revenue from quantity multiplied by unit price.

**Customer Relationship**

```excel
=DATEDIF(M2,TODAY(),"Y")
```

Calculates the customer's relationship duration in years.

**Timestamp**

```excel
=NOW()
```

Returns the current date and time.

**End of Sales Month**

```excel
=EOMONTH(data[[#This Row],[Date]],0)
```

Returns the last day of the transaction month.

**Sales Month**

```excel
=MONTH(data[[#This Row],[Date]])
```

Extracts the month number from the sales date.

---

# 🧮 Analysis Sheet

The `Analysis` sheet converts the raw transaction data into useful business information.

### 📊 Main KPIs

| KPI | Result |
|---|---:|
| 💰 Total Revenue | **$229,192.47** |
| 🧾 Total Transactions | **250** |
| 📦 Total Quantity | **753** |
| 💵 Average Transaction Value | **$916.77** |
| ⬆️ Highest Transaction | **$4,499.95** |
| ⬇️ Lowest Transaction | **$59.99** |

### 🧮 KPI Formulas

**Total Revenue**

```excel
=SUM(Data!N:N)
```

**Total Transactions**

```excel
=COUNTA(data[Transaction_ID])
```

**Total Quantity**

```excel
=SUM(data[Quantity])
```

**Average Transaction Value**

```excel
=AVERAGE(data[Total_Amount])
```

**Highest Transaction**

```excel
=MAX(data[Total_Amount])
```

**Lowest Transaction**

```excel
=MIN(data[Total_Amount])
```

---

# 👥 Customer Analysis

The workbook calculates revenue and purchase frequency for individual customers.

### 💰 Customer Revenue

```excel
=SUMIF(data[Customer_Name],Analysis!D2,data[Total_Amount])
```

Calculates the total revenue generated by a customer.

### 🔢 Purchase Frequency

```excel
=COUNTIF(data[Customer_Name],Analysis!D2)
```

Counts how many transactions were made by each customer.

### 🔤 Customer Abbreviation

The workbook also creates customer initials, for example:

```text
Paul Baker       → PB
Joseph Jackson   → JJ
Kevin Scott      → KS
Kathleen Bennett → KB
Michael Brown    → MB
```

### 🏆 Top 10 Customers

The analysis sheet ranks the highest-revenue customers using ranking and lookup formulas.

| Rank | Customer | Revenue |
|---:|---|---:|
| 1 | Mark Carter | $15,659.65 |
| 2 | Edward Mitchell | $11,919.77 |
| 3 | Barbara Young | $10,649.80 |
| 4 | Patricia Moore | $9,799.73 |
| 5 | Dorothy Nelson | $8,269.79 |

The complete workbook contains a **Top 10 Customers** section.

### 🔎 Ranking & Lookup

The workbook uses functions such as:

```excel
=LARGE(E2:E51,I3)
```

and

```excel
=_xlfn.XLOOKUP(K3,$E$2:$E$51,$D$2:$D$51)
```

to identify customers associated with the highest revenue values.

---

# 🛍️ Product Analysis

The Analysis sheet also calculates the quantity sold for each product.

### 📦 Quantity Sold

```excel
=SUMIF(data[Product_Name],Analysis!N2,data[Quantity])
```

This calculates the total quantity sold for each product.

### 🏆 Top 3 Products

The workbook identifies the three products with the highest quantity sold:

| Rank | Product | Quantity Sold |
|---:|---|---:|
| 1 | Bookshelf | **102** |
| 2 | Laptop | **96** |
| 3 | Desk | **89** |

Other products analyzed include:

```text
🖥️ Monitor
🧊 Blender
🎧 Headphones
⌨️ Keyboard
🪑 Office Chair
📱 Smartphone
☕ Coffee Maker
```

---

# 🎯 What-If Analysis & Goal Seek

The workbook includes practical **Scenario Manager** and **Goal Seek** analysis.

### 📌 Current Revenue

```text
Current Total Sales → $229,192.47
```

### 🎯 Goal Seek

The Analysis sheet contains a Goal Seek target of:

```text
🎯 Target Revenue → ₹3,50,000
```

The required growth shown by the workbook is approximately:

```text
📈 Growth → 52.71%
```

with projected sales of:

```text
💰 Projected Sales → 350,000
```

> 💡 Goal Seek is used to determine the input growth required to reach a specified revenue target.

---

# 🎯 Scenario Summary

The `Scenario Summary` sheet compares four growth scenarios.

| Scenario | Growth | Projected Revenue |
|---|---:|---:|
| 🔵 Low Growth | 5% | 240,652.09 |
| 🟢 Medium Growth | 10% | 252,111.72 |
| 🟠 High Growth | 15% | 263,571.34 |
| 🔴 Very High Growth | 20% | 275,030.96 |

### 📊 Scenario Logic

```text
5% Growth
    ↓
240,652.09

10% Growth
    ↓
252,111.72

15% Growth
    ↓
263,571.34

20% Growth
    ↓
275,030.96
```

This provides a simple way to compare how different growth assumptions affect projected revenue.

---

# 📈 Linear Regression

The `Linear Regression` sheet contains an Excel regression output with **249 observations**.

### 📊 Regression Statistics

| Metric | Value |
|---|---:|
| Multiple R | 0.4581 |
| R Square | 0.2099 |
| Adjusted R Square | 0.2067 |
| Standard Error | 921.41 |
| Observations | 249 |

### 🧪 ANOVA

| Metric | Value |
|---|---:|
| F Statistic | 65.60 |
| Significance F | 2.539 × 10⁻¹⁴ |

### 📌 Regression Coefficients

| Variable | Coefficient |
|---|---:|
| Intercept | -148.19 |
| Predictor | 353.79 |

The workbook's regression output shows a positive coefficient for the predictor variable.

The **R Square of approximately 0.210** means the model explains about **21.0% of the variation in the dependent variable** represented in the regression.

> ⚠️ Regression indicates a statistical relationship within the analyzed dataset. It should not automatically be interpreted as proof of causation.

---

# 🔄 Pivot Table Analysis

The `Pivot Table` sheet provides multiple views of the sales data.

### 🛍️ Sales by Product

| Product | Total Amount |
|---|---:|
| Coffee Maker | $3,119.61 |
| Blender | $5,219.13 |
| Headphones | $7,049.53 |
| Keyboard | $8,009.11 |
| Office Chair | $10,399.48 |
| Bookshelf | $15,298.98 |
| Monitor | $21,999.12 |
| Desk | $23,399.22 |
| Smartphone | $67,199.04 |
| Laptop | $67,499.25 |
| **Grand Total** | **$229,192.47** |

🏆 **Laptop** has the highest total amount, closely followed by **Smartphone**.

### 🌍 Sales by Region

| Region | Total Amount |
|---|---:|
| Central | $41,288.34 |
| East | $59,288.39 |
| North | $50,808.31 |
| South | $36,398.75 |
| West | $41,408.68 |
| **Grand Total** | **$229,192.47** |

🏆 **East** is the highest-revenue region in the PivotTable.

### 👥 Sales by Customer Segment

| Segment | Total Amount |
|---|---:|
| Basic | $62,177.81 |
| Premium | $84,657.12 |
| Standard | $82,357.54 |
| **Grand Total** | **$229,192.47** |

🏆 **Premium** is the highest-revenue customer segment.

### 💳 Sales by Payment Method

| Payment Method | Total Amount |
|---|---:|
| Cash | $57,427.79 |
| Credit Card | $61,447.96 |
| Debit Card | $52,118.31 |
| PayPal | $58,198.41 |
| **Grand Total** | **$229,192.47** |

🏆 **Credit Card** generates the highest transaction value among the payment methods.

---

# 📊 Category & Quantity Analysis

The PivotTable also analyzes quantity across product categories and regions.

### 📦 Total Units Sold

```text
Appliances   → 126
Electronics  → 395
Furniture    → 232
--------------------------------
Grand Total  → 753
```

🏆 **Electronics** has the highest quantity sold with **395 units**.

### 🌍 Regional Category Quantity

The workbook provides a region-by-category quantity matrix, allowing comparison of product-category volume across:

```text
📍 Central
📍 East
📍 North
📍 South
📍 West
```

This helps identify where different categories are selling the most units.

---

# 📊 Dashboard

The `Dashboard` sheet provides a visual **Sales Performance Dashboard**.

The dashboard covers the transaction period:

```text
📅 April 2024 → April 2025
```

### 🎯 Main Dashboard KPIs

```text
💰 TOTAL REVENUE
$229,192.47

🧾 TRANSACTIONS
250

📦 UNITS SOLD
753

💵 AVG ORDER VALUE
$916.77

🏆 TOP PRODUCT
Bookshelf
```

The dashboard is connected to the Analysis/PivotTable calculations so that the main figures can be presented in a compact business-reporting format.

---

# 🧠 Excel Concepts Covered

This project provides practical experience with:

```text
📊 SUM
🧮 SUMIF
🔢 COUNTIF
📋 COUNTA
📈 AVERAGE
⬆️ MAX
⬇️ MIN
🔎 XLOOKUP
🏆 LARGE
🔤 Text / Name Abbreviation
📅 DATEDIF
📅 EOMONTH
📅 MONTH
⏰ NOW
🔒 Structured References
🔄 Pivot Tables
🎯 Scenario Manager
🎯 Goal Seek
📈 Linear Regression
🧪 ANOVA
📊 Dashboard KPIs
```

---

# 🧪 Recommended Practice Flow

```text
📥 Understand Transaction Data
        ↓
🧮 Calculate Revenue & KPIs
        ↓
👥 Analyze Customers
        ↓
🛍️ Analyze Products
        ↓
🏆 Rank Top Customers & Products
        ↓
🔄 Build PivotTable Views
        ↓
🌍 Compare Regions
        ↓
💳 Compare Payment Methods
        ↓
🎯 Test Growth Scenarios
        ↓
🎯 Apply Goal Seek
        ↓
📈 Review Regression
        ↓
📊 Read Dashboard Insights
```

> 💡 **Best way to practice:** Change the underlying sales data, recalculate the analysis, refresh the PivotTables, and observe how the KPIs and dashboard results change.

---

# ▶️ How to Use

## 💻 Requirements

- 🟢 **Microsoft Excel**
- 📄 **`Final_Project.xlsx`**
- 📊 Basic understanding of Excel formulas and PivotTables

## 🚀 Steps

**1️⃣ Open the workbook**

Open:

```text
Final_Project.xlsx
```

**2️⃣ Start with `Data`**

Review transactions, customers, products, quantities, prices, regions, segments, and payment methods.

**3️⃣ Explore `Analysis`**

Review total revenue, transaction count, quantity, average transaction value, customer revenue, purchase frequency, and product rankings.

**4️⃣ Review `Scenario Summary`**

Compare Low, Medium, High, and Very High Growth scenarios.

**5️⃣ Explore `Linear Regression`**

Review the regression statistics, ANOVA table, coefficients, and model results.

**6️⃣ Explore `Pivot Table`**

Compare product, region, customer segment, payment method, and category performance.

**7️⃣ Open `Dashboard`**

Use the dashboard for a quick view of the main sales KPIs and top product.

---

# 📌 Quick Project Summary

| 📌 Property | 💻 Details |
|---|---|
| 📄 Workbook | `Final_Project.xlsx` |
| 📊 Sheets | 6 |
| 🧾 Transactions | 250 |
| 💰 Total Revenue | $229,192.47 |
| 📦 Total Quantity | 753 |
| 💵 Average Transaction | $916.77 |
| 👥 Customer Analysis | Included |
| 🛍️ Product Analysis | Included |
| 🔄 PivotTables | Included |
| 🎯 Goal Seek | Included |
| 🎯 Scenario Manager | Included |
| 📈 Linear Regression | Included |
| 📊 Dashboard | Included |
| 🔎 XLOOKUP | Included |
| 🏆 Top Customer Analysis | Included |
| 🥇 Top Product Analysis | Included |

---

# 🎯 Learning Outcomes

After completing this project, you will have practical experience with:

- 📋 Working with structured sales transaction data
- 🧮 Building KPI calculations with Excel formulas
- 👥 Measuring customer revenue and purchase frequency
- 🏆 Ranking high-value customers
- 🛍️ Identifying top-selling products
- 🔄 Creating and interpreting PivotTables
- 🌍 Comparing regional performance
- 💳 Analyzing payment methods
- 👥 Comparing customer segments
- 🎯 Performing What-If Scenario Analysis
- 🎯 Using Goal Seek for revenue targets
- 📈 Understanding basic regression output
- 📊 Building a business-focused dashboard
- 💡 Turning spreadsheet calculations into useful business insights

---

## 👨‍💻 Author

<div align="center">

### 🌟 Ayush Donga 🌟

**B.Sc IT Student | Aspiring AI/ML Engineer 🤖**

`📊 Excel` · `📈 Data Analysis` · `🐍 Python` · `🤖 AI/ML`

**📄 Project:** `Final_Project.xlsx`

</div>

---

<div align="center">

### ⭐ Learn the data. Analyze the numbers. Make better decisions. 🚀

**📊 Excel • 🔄 PivotTables • 🎯 What-If Analysis • 📈 Regression • 📊 Dashboards**

</div>
