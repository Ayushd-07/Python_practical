# 📈 RELIANCE Stock Market Data Analysis

> A practical Python data analysis project focused on exploring, cleaning, visualizing, and statistically analyzing historical **RELIANCE stock market data**.

This project uses **Python, NumPy, Pandas, Matplotlib, and Seaborn** to investigate stock-price behavior, yearly and monthly trends, trading information, and relationships between important market variables.

---

## 🌟 Project Overview

The **RELIANCE Stock Market Data Analysis** project is designed as a complete exploratory data analysis workflow.

The notebook starts by loading the RELIANCE stock dataset and checking its structure. It then performs data-quality checks, prepares the date information, selects data for **2020** for detailed monthly and daily trend analysis, creates multiple visualizations, and finally studies correlations between major numerical stock variables.

The analysis covers:

- 🗂️ Dataset loading and exploration
- 🔍 Initial data inspection
- 🧹 Missing-value checking and cleaning
- 🧾 Column and data-type analysis
- 📅 Date conversion and time-based filtering
- 📈 Monthly maximum High price analysis
- 📉 Monthly minimum Low price analysis
- 💹 Open vs Close price comparison
- 📊 High vs Low price comparison
- 💰 Yearly VWAP analysis
- 🔗 Correlation analysis
- 🌡️ Correlation heatmap visualization
- 📝 Key findings and conclusion

---

## 🎯 Objectives

The main objectives of this project are:

1. Understand the structure of the RELIANCE stock dataset.
2. Inspect the dataset for missing values and duplicate records.
3. Understand the available stock-market attributes.
4. Convert the `Date` column into a proper datetime format.
5. Filter the dataset for the year **2020** for detailed trend analysis.
6. Study monthly High and Low price behavior.
7. Compare Open and Close prices over time.
8. Compare High and Low prices to understand the trading range.
9. Summarize VWAP values year by year.
10. Analyze correlations between major stock-price variables.
11. Present the results through clear and easy-to-understand visualizations.

---

## 🛠️ Technologies & Libraries

| Technology | Purpose |
|---|---|
| 🐍 **Python** | Main programming language |
| 🧮 **NumPy** | Numerical operations and data support |
| 🐼 **Pandas** | Data loading, cleaning, grouping, and analysis |
| 📊 **Matplotlib** | Data visualization |
| 🎨 **Seaborn** | Statistical and advanced visualizations |
| 📓 **Jupyter Notebook** | Interactive analysis environment |

---

## 📁 Project Structure

```text
RELIANCE-Stock-Analysis/
│
├── 📓 RELIANCE.ipynb
├── 📄 RELIANCE.csv
└── 📘 README.md
```

### File Description

- **`RELIANCE.ipynb`**  
  Main Jupyter Notebook containing the complete analysis, Python code, visualizations, and findings.

- **`RELIANCE.csv`**  
  Dataset containing historical RELIANCE stock-market records.

- **`README.md`**  
  Project documentation and usage guide.

---

## 📊 Dataset Information

The dataset contains **5,306 records** and **13 columns**.

The analyzed dataset covers the period from:

**3 January 2000 to 30 April 2021**

### Dataset Columns

| Column | Description |
|---|---|
| `Date` | Trading date |
| `Symbol` | Stock symbol |
| `Series` | Stock series/category |
| `Prev Close` | Previous trading day's closing price |
| `Open` | Opening price |
| `High` | Highest price recorded during the trading session |
| `Low` | Lowest price recorded during the trading session |
| `Last` | Last traded price |
| `Close` | Closing price |
| `VWAP` | Volume Weighted Average Price |
| `Volume` | Trading volume |
| `Trades` | Number of trades |
| `Deliverable Volume` | Deliverable trading volume |

---

# 🔍 Analysis Workflow

## 1️⃣ Import Libraries & Load Dataset

The project begins by importing the required Python libraries and loading the RELIANCE CSV dataset using Pandas.

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

data = pd.read_csv("RELIANCE.csv")
```

The complete dataset is then displayed for an initial overview.

---

## 2️⃣ Initial Data Exploration

The notebook checks both the first and last records using:

```python
data.head(5)
data.tail(5)
```

Missing values are also checked using:

```python
data.isna().sum()
```

This helps understand the dataset before performing further processing.

---

## 3️⃣ Data Cleaning & Validation

The project checks missing values in important columns such as:

- `Trades`
- `Deliverable Volume`

The notebook uses median-based handling for these columns.

Additional validation includes:

```python
data.info()
data.dtypes
data.duplicated().sum()
data.describe()
```

These operations provide information about:

- Number of records
- Column names
- Data types
- Missing values
- Duplicate records
- Statistical summaries

---

## 4️⃣ Date Preparation

The `Date` column is converted into datetime format:

```python
data["Date"] = pd.to_datetime(data["Date"])
```

This makes it possible to perform time-based analysis such as:

- Year-wise filtering
- Month-wise grouping
- Monthly price analysis
- Yearly VWAP calculations

For detailed trend analysis, the notebook selects records from **2020**:

```python
year_data = data[data["Date"].dt.year == 2020]
```

---

# 📈 Visualizations & Analysis

## 5️⃣ Monthly Maximum High Price

The project calculates the maximum `High` price for every month of 2020.

```python
monthly_high = (
    year_data.groupby(year_data["Date"].dt.month)["High"].max()
)
```

A line chart is then used to visualize monthly price peaks.

### What it helps show

- Monthly maximum price movement
- Periods with higher price peaks
- Changes in the upper trading range during 2020

---

## 6️⃣ Monthly Minimum Low Price

The notebook also calculates the minimum `Low` price for each month of 2020.

```python
monthly_low = (
    year_data.groupby(year_data["Date"].dt.month)["Low"].min()
)
```

A line chart is used to visualize these monthly minimum prices.

### What it helps show

- Monthly price lows
- Periods with comparatively lower market prices
- Changes in the lower trading range

---

## 7️⃣ Open vs Close Price Trend

The project compares the `Open` and `Close` prices throughout 2020.

This visualization provides a direct view of how the opening and closing prices moved over the selected period.

### Why this comparison is useful

Comparing Open and Close prices can help identify:

- Daily price movement
- Changes between opening and closing levels
- General price trends over time

---

## 8️⃣ High vs Low Price Trend

The notebook compares the daily `High` and `Low` prices for 2020.

This gives a visual representation of the trading range and helps show how wide the price movement was during different periods.

---

## 9️⃣ Yearly VWAP Analysis

The project calculates the yearly sum of the `VWAP` column:

```python
yearly_vwap = (
    data.groupby(data["Date"].dt.year)["VWAP"].sum()
)
```

A bar chart is used to compare the resulting yearly values.

### VWAP

**VWAP** stands for **Volume Weighted Average Price**.

It is a market-related measure that considers both price and trading volume. In this project, the yearly VWAP values are summarized and visualized to compare the values across the years present in the dataset.

---

# 🔗 🔟 Correlation Analysis

The notebook performs correlation analysis on the following numerical columns:

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

The correlation matrix is generated using:

```python
corr = data[num_col].corr()
```

A Seaborn heatmap is then created to make the relationships easier to interpret.

### Variables Compared

- Previous Close
- Open
- High
- Low
- Last
- Close
- VWAP

### Why Correlation Analysis?

Correlation analysis helps identify how strongly numerical variables move in relation to each other.

The heatmap provides a visual overview of these relationships and makes it easier to identify variables with stronger or weaker linear relationships.

---

# 🏆 Key Findings

According to the analysis included in the notebook, the following maximum recorded values were identified:

| 📌 Indicator | 🔢 Maximum Recorded Value |
|---|---:|
| 🚀 High Price | **₹3,298.00** |
| 📈 Open Price | **₹3,298.00** |
| 💰 Close Price | **₹3,220.85** |
| 📊 VWAP | **₹3,197.75** |
| 📦 Trading Volume | **65,230,890** |
| 🔄 Trades | **1,428,490** |
| 📦 Deliverable Volume | **34,958,880** |

The dataset contains:

- **5,306 records**
- **13 columns**
- Historical data from **3 January 2000 to 30 April 2021**

These figures summarize the key values highlighted in the notebook.

---

# 📊 Charts Included

The project includes several visualizations to make the analysis easier to understand:

### 📈 Monthly Maximum High Price
Shows the maximum High price recorded in each month of 2020.

### 📉 Monthly Minimum Low Price
Shows the minimum Low price recorded in each month of 2020.

### 💹 Open vs Close Price
Compares daily Open and Close prices during 2020.

### 📊 High vs Low Price
Shows the daily relationship between the highest and lowest prices during 2020.

### 💰 Yearly VWAP
Displays yearly aggregated VWAP values using a bar chart.

### 🔥 Correlation Heatmap
Displays correlations between major numerical price-related variables.

---

# ▶️ How to Run the Project

## Step 1: Install Python

Make sure Python is installed on your computer.

You can check your Python version with:

```bash
python --version
```

---

## Step 2: Install Required Libraries

Install the required packages using:

```bash
pip install numpy pandas matplotlib seaborn jupyter
```

---

## Step 3: Keep the Files Together

Make sure the following files are inside the same project folder:

```text
RELIANCE.ipynb
RELIANCE.csv
README.md
```

The notebook loads the dataset using:

```python
pd.read_csv("RELIANCE.csv")
```

Therefore, `RELIANCE.csv` should be available in the notebook's working directory.

---

## Step 4: Open Jupyter Notebook

Run:

```bash
jupyter notebook
```

Then open:

```text
RELIANCE.ipynb
```

---

## Step 5: Run the Notebook

Execute the cells from top to bottom.

The notebook will:

1. Import the libraries
2. Load the dataset
3. Explore the data
4. Check missing values
5. Validate the dataset
6. Convert dates
7. Filter 2020 records
8. Generate visualizations
9. Perform VWAP analysis
10. Calculate correlations
11. Display key findings

---

# 💡 Learning Outcomes

This project provides practical experience with several important data-analysis concepts.

### 🐼 Pandas

You practice:

- Reading CSV files
- Selecting columns
- Filtering rows
- Handling missing values
- Grouping data
- Working with datetime values
- Calculating descriptive statistics

### 🧮 NumPy

You use NumPy as part of the Python data-analysis environment and numerical workflow.

### 📊 Matplotlib & Seaborn

You practice:

- Line charts
- Bar charts
- Heatmaps
- Chart labels
- Legends
- Grid lines
- Figure sizing
- Visualization formatting

### 📅 Time-Series Analysis

The project demonstrates how a date column can be converted and used to:

- Filter a specific year
- Group records by month
- Analyze yearly values
- Visualize price trends

### 🔗 Statistical Analysis

The correlation section provides practical experience with understanding relationships between numerical variables.

---

# 📌 Important Notes

- This project is an **educational data-analysis project**.
- The analysis is based on the dataset loaded by the notebook.
- The 2020 charts specifically use the filtered `year_data` dataset.
- The yearly VWAP visualization uses the full dataset.
- The results and values shown in this README are based on the findings documented in the notebook.
- This project should not be treated as financial advice or as a recommendation to buy or sell any security.

---

# 🚀 Possible Future Improvements

The project can be extended further by adding:

- 📅 Interactive date-range selection
- 📈 Moving averages such as 20-day and 50-day averages
- 📊 Daily return calculations
- 📉 Volatility analysis
- 📦 Volume trend visualization
- 🕯️ Candlestick charts
- 📈 Additional technical indicators
- 🔍 More detailed monthly and yearly comparisons
- 📊 Interactive dashboards
- 🤖 Basic predictive analysis
- 📌 Automated report generation

These additions could turn the current exploratory notebook into a more advanced stock-market analytics project.

---

# 🎓 Project Purpose

This project demonstrates how Python can be used to transform raw stock-market data into meaningful information through:

**Data → Cleaning → Exploration → Analysis → Visualization → Insights**

It is especially useful for practicing the fundamentals of **Data Analysis, Pandas, NumPy, Matplotlib, Seaborn, and basic financial-data exploration**.

---

# 👨‍💻 Author

**Ayush Donga**

B.Sc. IT Student | Python & Data Analysis Learner

This project was created as part of practical learning and project-based exploration of Python data analysis.

---

## ⭐ Project Highlights

```text
📈 RELIANCE Stock Market Analysis
│
├── 🗂️ Data Loading
├── 🔍 Data Exploration
├── 🧹 Data Cleaning
├── 📅 Date & Year Analysis
├── 📈 Monthly High Analysis
├── 📉 Monthly Low Analysis
├── 💹 Open vs Close Analysis
├── 📊 High vs Low Analysis
├── 💰 Yearly VWAP Analysis
├── 🔗 Correlation Analysis
├── 🔥 Heatmap Visualization
└── 📝 Key Findings
```

---

## ⭐ If You Like This Project

If you are learning Python or Data Analysis, this project can be used as a starting point for building more advanced financial-data analysis projects.

**Made with ❤️ using Python, Pandas, NumPy, Matplotlib & Seaborn.**
