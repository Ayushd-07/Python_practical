<div align="center">

# 📈 RELIANCE Stock Market Analysis

### Historical Stock Data Exploration & Visualization with Python

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Analysis-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C?style=for-the-badge)](https://matplotlib.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4C72B0?style=for-the-badge)](https://seaborn.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)

<br>

**Explore 📊 · Clean 🧹 · Analyze 🔎 · Visualize 📈 · Understand 💡**

</div>

---

## 📌 About the Project

**RELIANCE Stock Market Analysis** is an exploratory data analysis project built with **Python** and the core Data Science libraries **Pandas, NumPy, Matplotlib, and Seaborn**.

The project analyzes historical RELIANCE stock-market records and focuses on understanding price movement, yearly and monthly behavior, trading activity, VWAP values, and relationships between important numerical market variables.

The analysis is implemented in a Jupyter Notebook and follows a practical workflow:

```text
📂 Load Dataset
      ↓
🔎 Explore Data
      ↓
🧹 Check & Clean Data
      ↓
📅 Prepare Date Information
      ↓
📆 Filter 2020 Data
      ↓
📈 Analyze High & Low Prices
      ↓
💹 Compare Open & Close
      ↓
💰 Analyze Yearly VWAP
      ↓
🔗 Calculate Correlations
      ↓
📊 Create Visualizations
      ↓
📝 Summarize Findings
```

> 💡 **Project goal:** Practice real-world stock-data analysis using Python and turn raw historical records into clear visual insights.

---

# 🎯 Project Objectives

The project is designed to:

- 📂 Load historical RELIANCE stock data from CSV
- 🔎 Understand the structure and quality of the dataset
- 🧹 Check missing values and duplicate records
- 🧾 Inspect columns and data types
- 📅 Convert the `Date` column to datetime format
- 📆 Filter stock records for the year 2020
- 📈 Analyze monthly maximum High prices
- 📉 Analyze monthly minimum Low prices
- 💹 Compare Open and Close prices
- 📊 Compare High and Low prices
- 💰 Analyze yearly VWAP values
- 🔗 Study correlations between major price variables
- 📊 Present findings through clean visualizations

---

# 🗂️ Table of Contents

- [📌 About the Project](#-about-the-project)
- [🎯 Project Objectives](#-project-objectives)
- [📂 Project Structure](#-project-structure)
- [🛠️ Technology Stack](#️-technology-stack)
- [📊 Dataset](#-dataset)
- [🔄 Analysis Workflow](#-analysis-workflow)
- [🔎 Data Exploration](#-data-exploration)
- [🧹 Data Cleaning](#-data-cleaning)
- [📅 Date Preparation](#-date-preparation)
- [📈 Price Analysis](#-price-analysis)
- [💰 VWAP Analysis](#-vwap-analysis)
- [🔗 Correlation Analysis](#-correlation-analysis)
- [📊 Visualizations](#-visualizations)
- [🏆 Key Findings](#-key-findings)
- [🎓 Learning Outcomes](#-learning-outcomes)
- [▶️ How to Run](#️-how-to-run)
- [🔮 Future Improvements](#-future-improvements)
- [⚠️ Important Notes](#️-important-notes)
- [🤝 Contributing](#-contributing)
- [👨‍💻 Author](#-author)
- [📄 License](#-license)

---

# 📂 Project Structure

```text
📦 RELIANCE-Stock-Analysis
│
├── 📓 RELIANCE.ipynb
│   └── Complete Jupyter Notebook analysis
│
├── 📄 RELIANCE.csv
│   └── Historical RELIANCE stock dataset
│
└── 📖 README.md
    └── Project documentation
```

### 📁 File Details

| File | Purpose |
|---|---|
| `RELIANCE.ipynb` | Contains the complete Python analysis and visualizations |
| `RELIANCE.csv` | Historical stock-market dataset |
| `README.md` | Project documentation |

---

# 🛠️ Technology Stack

| Technology | Used For |
|---|---|
| 🐍 **Python** | Core programming language |
| 🐼 **Pandas** | Data loading, cleaning, grouping, and analysis |
| 🔢 **NumPy** | Numerical operations |
| 📊 **Matplotlib** | Plot creation and customization |
| 🎨 **Seaborn** | Statistical visualizations |
| 📓 **Jupyter Notebook** | Interactive analysis environment |

---

# 📊 Dataset

The dataset contains **5,306 records** and **13 columns**.

### 📅 Dataset Period

```text
Start Date : 03 January 2000
End Date   : 30 April 2021
Records    : 5,306
Columns    : 13
```

### 📋 Dataset Columns

| Column | Description |
|---|---|
| `Date` | Trading date |
| `Symbol` | Stock symbol |
| `Series` | Stock series/category |
| `Prev Close` | Previous trading day's closing price |
| `Open` | Opening price |
| `High` | Highest price during the trading session |
| `Low` | Lowest price during the trading session |
| `Last` | Last traded price |
| `Close` | Closing price |
| `VWAP` | Volume Weighted Average Price |
| `Volume` | Trading volume |
| `Trades` | Number of trades |
| `Deliverable Volume` | Deliverable trading volume |

---

# 🔄 Analysis Workflow

```text
                     ┌─────────────────┐
                     │  📄 CSV Dataset │
                     └────────┬────────┘
                              ↓
                     ┌─────────────────┐
                     │ 🔎 Data Explore │
                     └────────┬────────┘
                              ↓
                     ┌─────────────────┐
                     │ 🧹 Data Quality │
                     └────────┬────────┘
                              ↓
                     ┌─────────────────┐
                     │ 📅 Date Convert │
                     └────────┬────────┘
                              ↓
                     ┌─────────────────┐
                     │ 📆 2020 Filter  │
                     └────────┬────────┘
                              ↓
              ┌───────────────┼───────────────┐
              ↓               ↓               ↓
        📈 High/Low      💹 Open/Close    💰 VWAP
              │               │               │
              └───────────────┼───────────────┘
                              ↓
                     ┌─────────────────┐
                     │ 🔗 Correlation  │
                     └────────┬────────┘
                              ↓
                     ┌─────────────────┐
                     │ 📊 Visualize    │
                     └────────┬────────┘
                              ↓
                     ┌─────────────────┐
                     │ 🏆 Findings     │
                     └─────────────────┘
```

---

# 🔎 Data Exploration

The notebook starts by inspecting the dataset.

### First Records

```python
data.head(5)
```

### Last Records

```python
data.tail(5)
```

### Missing Values

```python
data.isna().sum()
```

### Dataset Information

```python
data.info()
```

### Data Types

```python
data.dtypes
```

### Duplicate Records

```python
data.duplicated().sum()
```

### Descriptive Statistics

```python
data.describe()
```

These checks provide an initial understanding of the dataset before performing deeper analysis.

---

# 🧹 Data Cleaning

Data quality is checked before visualization and statistical analysis.

The notebook specifically examines missing values in fields such as:

- `Trades`
- `Deliverable Volume`

Median-based handling is used for these columns where required.

The project also checks for duplicate rows and reviews the resulting DataFrame information.

### Cleaning Workflow

```text
Raw Dataset
    ↓
Check Missing Values
    ↓
Inspect Data Types
    ↓
Handle Required Missing Data
    ↓
Check Duplicates
    ↓
Review Clean Dataset
```

---

# 📅 Date Preparation

The `Date` column is converted into a proper datetime format:

```python
data["Date"] = pd.to_datetime(data["Date"])
```

This enables time-based operations such as:

- Filtering by year
- Grouping by month
- Yearly aggregation
- Time-series visualization

---

## 📆 2020 Analysis Dataset

For detailed price analysis, the notebook filters records belonging to 2020:

```python
year_data = data[data["Date"].dt.year == 2020]
```

This `year_data` DataFrame is then used for the monthly and daily price visualizations.

---

# 📈 Price Analysis

## 1️⃣ Monthly Maximum High Price

The notebook calculates the maximum `High` price for each month of 2020:

```python
monthly_high = (
    year_data.groupby(year_data["Date"].dt.month)["High"].max()
)
```

### 📊 Purpose

This analysis helps identify:

- Monthly price peaks
- Higher trading periods
- Changes in the upper price range during 2020

A line chart is used to display the monthly movement.

---

## 2️⃣ Monthly Minimum Low Price

The minimum `Low` price for each month is calculated:

```python
monthly_low = (
    year_data.groupby(year_data["Date"].dt.month)["Low"].min()
)
```

### 📉 Purpose

This helps identify:

- Monthly price lows
- Lower trading periods
- Changes in the lower price range

The results are displayed using a line chart.

---

## 3️⃣ 💹 Open vs Close Price

The notebook compares:

```text
Open
vs
Close
```

for the 2020 records.

### Why is this useful?

Comparing Open and Close prices gives a visual understanding of daily price movement and how the stock moved between the beginning and end of each trading session.

---

## 4️⃣ 📊 High vs Low Price

The project also compares:

```text
High
vs
Low
```

for the selected 2020 period.

This provides a visual representation of the daily trading range.

```text
High ────────────────┐
                     │ Trading Range
Low  ────────────────┘
```

A wider difference between High and Low indicates a larger price range during that session.

---

# 💰 VWAP Analysis

### What is VWAP?

**VWAP** stands for **Volume Weighted Average Price**.

It is a market-data measure that considers both price and trading volume.

The notebook calculates yearly VWAP values using:

```python
yearly_vwap = (
    data.groupby(data["Date"].dt.year)["VWAP"].sum()
)
```

The result is displayed using a bar chart.

### 📊 Purpose

The yearly visualization allows comparison of the VWAP values across the years represented in the dataset.

> **Note:** The notebook uses a yearly `sum()` of the `VWAP` column for this visualization. This README describes the notebook's implemented calculation rather than replacing it with a different VWAP methodology.

---

# 🔗 Correlation Analysis

The project calculates correlations between major numerical stock-price variables.

### Variables Used

```python
num_col = [
    "Prev Close",
    "Open",
    "High",
    "Low",
    "Last",
    "Close",
    "VWAP"
]
```

The correlation matrix is calculated using:

```python
corr = data[num_col].corr()
```

Then a heatmap is generated using Seaborn.

### 🔥 Correlation Heatmap

The heatmap makes it easier to identify stronger and weaker linear relationships between:

- Previous Close
- Open
- High
- Low
- Last
- Close
- VWAP

### 📌 Correlation Guide

| Value | General Meaning |
|---:|---|
| `+1` | Strong positive relationship |
| `0` | Little or no linear relationship |
| `-1` | Strong negative relationship |

> ⚠️ **Correlation does not prove causation.** It only describes the statistical relationship captured by the correlation calculation.

---

# 📊 Visualizations

The project includes several visual analyses:

| # | Visualization | Analysis |
|---:|---|---|
| 1️⃣ | 📈 Monthly High | Maximum High price by month in 2020 |
| 2️⃣ | 📉 Monthly Low | Minimum Low price by month in 2020 |
| 3️⃣ | 💹 Open vs Close | Daily Open and Close movement |
| 4️⃣ | 📊 High vs Low | Daily trading range |
| 5️⃣ | 💰 Yearly VWAP | Year-wise VWAP aggregation |
| 6️⃣ | 🔥 Correlation Heatmap | Relationships between numerical price variables |

---

# 🏆 Key Findings

The notebook highlights the following maximum recorded values:

| Indicator | Maximum Recorded Value |
|---|---:|
| 🚀 High Price | **₹3,298.00** |
| 📈 Open Price | **₹3,298.00** |
| 💰 Close Price | **₹3,220.85** |
| 📊 VWAP | **₹3,197.75** |
| 📦 Trading Volume | **65,230,890** |
| 🔄 Trades | **1,428,490** |
| 📦 Deliverable Volume | **34,958,880** |

### Dataset Summary

```text
📊 Records  : 5,306
📋 Columns  : 13
📅 Period   : 03 Jan 2000 → 30 Apr 2021
📆 Detailed : 2020 price analysis
```

These values represent the results documented in the notebook and should be interpreted within the context of the supplied dataset.

---

# 💡 What This Project Demonstrates

This project is more than a simple charting exercise. It demonstrates a practical workflow for working with historical financial data:

```text
Raw Market Data
      ↓
Data Quality Checks
      ↓
Data Preparation
      ↓
Time-Based Filtering
      ↓
Grouped Analysis
      ↓
Statistical Analysis
      ↓
Visualization
      ↓
Interpretation
```

It shows how Pandas can be used to transform a raw CSV file into a structured dataset that can be analyzed with NumPy and visualized using Matplotlib and Seaborn.

---

# 🎓 Learning Outcomes

By completing this project, you practice:

### 🐼 Pandas

- Reading CSV files
- DataFrame operations
- Selecting columns
- Filtering rows
- Handling missing values
- Grouping data
- Aggregating data
- Datetime operations
- Descriptive statistics

### 🔢 NumPy

- Numerical data handling
- Data Science workflow integration
- Numeric column processing

### 📊 Matplotlib

- Line charts
- Bar charts
- Figure customization
- Titles and labels
- Grid and legend formatting

### 🎨 Seaborn

- Statistical charts
- Heatmaps
- Visual comparison of numerical variables

### 📅 Time-Series Concepts

- Date conversion
- Year filtering
- Month grouping
- Yearly aggregation
- Price trend visualization

### 🔗 Statistical Concepts

- Correlation matrices
- Relationship analysis
- Descriptive statistics

---

# ▶️ How to Run

## 1. Install Python

Install Python 3.x.

Check the version:

```bash
python --version
```

---

## 2. Install Dependencies

```bash
pip install numpy pandas matplotlib seaborn jupyter
```

---

## 3. Prepare the Project Folder

Keep these files together:

```text
RELIANCE.ipynb
RELIANCE.csv
README.md
```

The notebook loads:

```python
pd.read_csv("RELIANCE.csv")
```

so the CSV should normally be in the notebook's working directory.

---

## 4. Start Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
RELIANCE.ipynb
```

---

## 5. Run the Notebook

Run the cells from top to bottom.

### Recommended Order

```text
1. 📚 Import Libraries
2. 📂 Load Dataset
3. 🔎 Explore Dataset
4. 🧹 Check Data Quality
5. 📅 Convert Date
6. 📆 Filter 2020
7. 📈 Analyze Monthly High
8. 📉 Analyze Monthly Low
9. 💹 Compare Open & Close
10. 📊 Compare High & Low
11. 💰 Analyze Yearly VWAP
12. 🔗 Calculate Correlation
13. 🔥 Display Heatmap
14. 🏆 Review Findings
```

---

# ⚠️ Important Notes

- This is an **educational exploratory data-analysis project**.
- The analysis is based on the supplied RELIANCE dataset.
- Detailed price charts use the records filtered for **2020**.
- The yearly VWAP chart uses the full dataset.
- The notebook's VWAP analysis uses a yearly `sum()` aggregation.
- Correlation indicates statistical association and does not establish causation.
- Historical stock-market analysis does not guarantee future performance.
- This project is **not financial advice** and should not be used alone to make investment decisions.

---

# 🚀 Future Improvements

The project can be expanded with:

### 📈 Technical Analysis

- Moving averages
- Exponential moving averages
- RSI
- MACD
- Bollinger Bands
- Daily returns
- Volatility analysis

### 📊 Advanced Visualizations

- Candlestick charts
- Volume-price charts
- Interactive charts
- Rolling-average plots
- Monthly heatmaps

### 📅 Advanced Time-Series Analysis

- Daily return trends
- Monthly return comparison
- Year-over-year performance
- Volatility by year
- Drawdown analysis

### 🤖 Machine Learning

Future versions could explore:

- Price trend prediction
- Regression models
- Time-series forecasting
- Feature engineering
- Model evaluation

### 🖥️ Dashboard

The notebook could also be converted into an interactive dashboard using:

```text
Streamlit
Plotly
Dash
```

Possible dashboard controls:

```text
📅 Date Range
📊 Price Metric
📈 Chart Type
📦 Volume
🔍 Year / Month Filter
```

---

# 🏅 Project Highlights

<div align="center">

| 📌 Area | ✅ Included |
|---|:---:|
| CSV Data Loading | ✅ |
| Data Exploration | ✅ |
| Missing Value Check | ✅ |
| Duplicate Check | ✅ |
| Date Conversion | ✅ |
| 2020 Filtering | ✅ |
| Monthly High Analysis | ✅ |
| Monthly Low Analysis | ✅ |
| Open vs Close | ✅ |
| High vs Low | ✅ |
| Yearly VWAP | ✅ |
| Correlation Matrix | ✅ |
| Heatmap | ✅ |
| Key Findings | ✅ |

</div>

---

# 🤝 Contributing

If you want to improve this project:

```text
1. Fork the repository
2. Create a new branch
3. Make your changes
4. Test the notebook
5. Commit your changes
6. Push the branch
7. Open a Pull Request
```

Ideas for contributions include:

- More financial indicators
- Better visualizations
- Interactive dashboards
- Improved data cleaning
- Advanced statistical analysis
- Machine-learning extensions

---

# 👨‍💻 Author

<div align="center">

## **Ayush Donga**

🎓 **B.Sc. IT Student**

🐍 **Python & Data Analysis Learner**

📊 **Aspiring Data Scientist**

🤖 **AI & Machine Learning Enthusiast**

<br>

> **Learning by building practical projects. 🚀**

</div>

---

# 📄 License

This project is created for **educational and learning purposes**.

You are free to study, modify, and extend the project according to your requirements.

> Please remember that this project is an educational stock-data analysis and is not financial advice.

---

<div align="center">

---

## 📈 RELIANCE Stock Market Analysis

### **Data → Analysis → Visualization → Insights**

**Built with 🐍 Python · 🐼 Pandas · 🔢 NumPy · 📊 Matplotlib · 🎨 Seaborn**

### ⭐ If you found this project useful, consider giving the repository a Star!

**Made with ❤️ while learning Data Science**

</div>
