<div align="center">

# 📊 Superstore Sales Dashboard

### 💰 Sales Performance • Profitability • Product Insights • Regional Analysis

<p>
<img src="https://img.shields.io/badge/Power_BI-Interactive_Report-F2C811?style=for-the-badge&logo=powerbi&logoColor=black">
<img src="https://img.shields.io/badge/Sales_Analytics-Business_Insights-4472C4?style=for-the-badge">
<img src="https://img.shields.io/badge/KPI_Reporting-Executive_Summary-6C63FF?style=for-the-badge">
<img src="https://img.shields.io/badge/Interactive-Report_Filters-16A085?style=for-the-badge">
</p>

<p>
<img src="https://img.shields.io/badge/Total_Sales-1.50M-CC0000?style=for-the-badge">
<img src="https://img.shields.io/badge/Total_Profit-178.57K-555555?style=for-the-badge">
<img src="https://img.shields.io/badge/Average_Discount-15.70%25-E67E22?style=for-the-badge">
</p>

**📥 Sales Data → 📊 Power BI Visuals → 🎛️ Interactive Filters → 📋 Order Details → 💡 Business Insights**

</div>

---

## ✨ Project Overview

The **Superstore Sales Dashboard** is an interactive Power BI project designed to analyze sales, profit, quantity, discounts, product categories, regional performance, and order-level details.

The report combines KPI cards, horizontal bar charts, slicers, and a detailed order table. The Dashboard page gives a quick overview of business performance, while the Order Details page makes it easier to inspect individual product records and compare sales, profit, quantity, and region.

> 💡 **Main Power BI File:** `Sales_dashboard.pbix`

---

## 🖼️ Dashboard Preview

### 📊 1. Sales Dashboard

![Superstore Sales Dashboard](Output%20images/Sales_Dashboard.png)

*The main page presents headline KPIs, sales by product category, profit by region, and the Top 5 sub-categories by sales.*

### 📋 2. Order Details

![Order Details](Output%20images/Order_Details.png)

*The Order Details page displays Year, Month, Category, Product Name, Sales, Profit, Quantity, and Region. The table is sorted by sales in descending order to make high-value records easier to review.*

---

## 📌 Dashboard KPIs

| KPI | Displayed Value | Description |
|---|---:|---|
| 💰 **Total Sales** | **1.50M** | Overall sales value displayed in the report |
| 📈 **Total Profit** | **178.57K** | Overall profit displayed in the report |
| 📦 **Total Quantity** | **25K** | Total quantity shown in the dashboard |
| 🎟️ **Average Discount** | **15.70%** | Average discount in the current report context |

KPI values may change when the Region or Category slicers are used.

---

## 📊 Visual Analysis

### 🛍️ Total Sales by Product Category

| Product Category | Sales |
|---|---:|
| 💻 Technology | 503K |
| 🪑 Furniture | 502K |
| 📎 Office Supplies | 492K |

**Technology** leads the displayed category comparison, with Furniture close behind.

### 🌍 Total Profit by Region

| Region | Profit |
|---|---:|
| 🌅 West | 66K |
| 🌄 East | 50K |
| ☀️ South | 38K |
| 🧭 Central | 25K |

**West** has the highest displayed regional profit, while Central has the lowest.

### 🏆 Top 5 Sub-Categories by Sales

| Rank | Sub-Category | Sales |
|---:|---|---:|
| 1 | 🪑 Chairs | 216K |
| 2 | 📱 Phones | 209K |
| 3 | 📦 Storage | 152K |
| 4 | 🪵 Tables | 144K |
| 5 | 📁 Binders | 139K |

The Top 5 visual uses a **Top N filter** and shows the filter context **Ship Mode: Standard & Second Class**. Interpret this ranking within that context.

---

## 📋 Order Details Page

The second report page provides a detailed view of individual records.

### 🧾 Fields Included

- 📅 **Year** and **Month**
- 🏷️ **Category**
- 📦 **Product Name**
- 💰 **Sum of Sales**
- 📈 **Sum of Profit**
- 🔢 **Sum of Quantity**
- 🌍 **Region**

The table uses alternating row shading and includes a total row. Sorting by sales in descending order helps users inspect higher-value records first.

---

## 🎛️ Filters & Interactions

The report includes two slicers:

- 🌍 **Region:** Explore performance by region.
- 🏷️ **Category:** Focus on a selected product category.

### 🔄 Cross-Filtering

To configure visual interactions in Power BI:

1. Select the **Sales by Product Category** chart.
2. Open **Format → Edit interactions**.
3. Configure the **Profit by Region** chart to cross-filter.
4. Choose the intended interaction for KPI cards, such as highlight or none.
5. Select a category bar and check whether the other visuals respond as expected.
6. Repeat the interaction check for at least two additional visual pairs.

> 💡 Test slicers and chart selections before publishing to make sure the report behaves as intended.

---

## 🎨 Design & Layout

The dashboard uses a clean, card-based layout with:

- 🔴 Red headings and category bars for strong visual emphasis
- ⬜ White cards against a light grey background
- 🔢 Large KPI values for quick scanning
- 📊 Horizontal bar charts for category and regional comparisons
- 🎛️ Slicers placed at the top for easy access
- 📋 A separate Order Details page for transaction-level review
- 🧩 Consistent spacing, rounded cards, and readable labels

A built-in professional theme can be applied from **View → Themes**. After applying a theme, check that colours and fonts remain consistent across all visuals.

---

## 💡 Key Insights

- 💰 Total sales are displayed as **1.50M**.
- 📈 Total profit is displayed as **178.57K**.
- 📦 The dashboard shows approximately **25K** in total quantity.
- 🎟️ Average discount is **15.70%**.
- 🛍️ **Technology** has the highest displayed category sales at approximately **503K**.
- 🌍 **West** leads the displayed regional profit comparison at approximately **66K**.
- 🏆 **Chairs** lead the displayed Top 5 sub-category sales chart at approximately **216K**.
- 🔎 The Order Details page supports product-level inspection of sales and profit.

*These observations reflect the values shown in the supplied screenshots. Active filters can change the displayed results.*

---

## ▶️ How to Use

### 💻 Requirements

- 🟡 **Microsoft Power BI Desktop**
- 📄 `Sales_dashboard.pbix`
- 📁 The `Output images` folder for the README screenshots

### 🚀 Steps

1. Open `Sales_dashboard.pbix` in Power BI Desktop.
2. Review the KPI cards on the Dashboard page.
3. Use the **Region** and **Category** slicers to filter the report.
4. Compare category sales and regional profit.
5. Review the Top 5 sub-categories and note the ship-mode filter context.
6. Open **Order Details** to inspect individual product records.
7. Test chart interactions and confirm that visuals respond as intended.
8. Save the report after making changes.

---

## 🎥 Dashboard Walkthrough Video

Watch the project walkthrough using the Google Drive link below.

**▶️ [Open Sales Dashboard Walkthrough Video](https://drive.google.com/drive/folders/1Ft32rP0E23pXjXehZTHOQyGM7CYn3wol)**

---

## 📁 Project Structure

```text
📦 Sales_dashboard
│
├── 📊 Sales_dashboard.pbix
├── 📄 README.md
└── 📁 Output images
    ├── Sales_Dashboard.png
    └── Order_Details.png
```

---

## 🧠 Skills Demonstrated

- 📊 Power BI report and dashboard design
- 💰 KPI cards and sales performance reporting
- 🛍️ Product category and sub-category analysis
- 🌍 Regional profit comparison
- 📋 Order-level data presentation
- 🎛️ Slicers and interactive filtering
- 🔄 Cross-filtering and visual interactions
- 🎨 Theme consistency and dashboard layout
- 💡 Communicating business insights with visuals

---

## 👨‍💻 Author

<div align="center">

### 🌟 Ayush Donga 🌟

**B.Sc IT Student | Aspiring Data Analyst & AI/ML Engineer 🤖**

`📊 Power BI` · `📈 Data Analysis` · `📗 Excel` · `🐍 Python`

**📄 Project:** `Sales_dashboard.pbix`

</div>

---

<div align="center">

### ⭐ Explore the numbers. Find the patterns. Make better decisions. 🚀

**📊 Power BI • 💰 Sales Analytics • 📋 Order Details • 🎛️ Interactive Dashboard**

</div>
