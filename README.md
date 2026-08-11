# 🦠 COVID-19 Data Analysis

<div align="center">

## 📊 Exploratory Data Analysis of COVID-19 Cases

**Load • Clean • Explore • Analyze • Visualize • Discover**

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C?style=for-the-badge)](https://matplotlib.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Visualization-4C72B0?style=for-the-badge)](https://seaborn.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)

</div>

---

## 📌 Project Overview

**COVID-19 Data Analysis** is an exploratory data analysis project created in Python using **Pandas, NumPy, Matplotlib, and Seaborn**.

The project analyzes a COVID-19 dataset at the country and date level. It focuses on understanding confirmed cases, deaths, recoveries, active cases, country-level differences, the COVID-19 death trend in India, and relationships between numerical variables.

The complete analysis is organized in a Jupyter Notebook and follows a clear data-analysis workflow:

```text
📂 Load Dataset
      ↓
🧹 Check Data Quality
      ↓
🔎 Explore Dataset
      ↓
🌍 Analyze Countries
      ↓
📊 Compare COVID-19 Indicators
      ↓
🇮🇳 Analyze India's Death Trend
      ↓
🔗 Correlation Analysis
      ↓
📋 Create Country Summary
      ↓
🔑 Identify Key Findings
      ↓
✅ Conclusion
```

> **Project Focus:** Exploratory Data Analysis (EDA) using Python.

---

# 🎯 Objectives

The main objectives of this project are:

- 📂 Load and understand the COVID-19 dataset
- 🧹 Check missing values and data types
- 📅 Convert the date column into a proper datetime format
- 🌍 Explore the countries included in the dataset
- 🦠 Analyze confirmed COVID-19 cases by country
- 🕯️ Analyze COVID-19 deaths by country
- 💚 Compare recoveries across countries
- ⚠️ Analyze active COVID-19 cases
- 🇮🇳 Study the COVID-19 death trend in India
- 🔗 Analyze correlations between numerical variables
- 📋 Create a final country-wise summary
- 🔑 Extract key analytical findings from the dataset

---

# 🗂️ Table of Contents

- [📌 Project Overview](#-project-overview)
- [🎯 Objectives](#-objectives)
- [📂 Project Files](#-project-files)
- [🛠️ Technology Stack](#️-technology-stack)
- [📊 Dataset](#-dataset)
- [🔄 Analysis Workflow](#-analysis-workflow)
- [1️⃣ Import Libraries](#1️⃣-import-libraries)
- [2️⃣ Load Dataset](#2️⃣-load-dataset)
- [3️⃣ Dataset Structure](#3️⃣-dataset-structure)
- [4️⃣ Data Quality Check](#4️⃣-data-quality-check)
- [5️⃣ Country-Level Overview](#5️⃣-country-level-overview)
- [6️⃣ Confirmed Cases](#6️⃣-confirmed-cases-by-country)
- [7️⃣ Deaths](#7️⃣-covid-19-deaths-by-country)
- [8️⃣ India Death Trend](#8️⃣-covid-19-death-trend-in-india)
- [9️⃣ Recoveries](#9️⃣-covid-19-recoveries-by-country)
- [🔟 Correlation Analysis](#-correlation-analysis)
- [📋 Final Summary](#-final-country-wise-summary)
- [🔑 Key Findings](#-key-analysis--findings)
- [📈 Visualizations](#-visualizations)
- [▶️ How to Run](#️-how-to-run-the-project)
- [🎓 Learning Outcomes](#-learning-outcomes)
- [🔮 Future Improvements](#-future-improvements)
- [⚠️ Notes](#️-notes)
- [👨‍💻 Author](#-author)
- [📄 License](#-license)

---

# 📂 Project Files

The project is organized around the following files:

```text
📦 COVID-19-Data-Analysis
│
├── 📓 Covid-19.ipynb
│   └── Complete exploratory data analysis notebook
│
├── 📄 Covid19_dataset.csv
│   └── COVID-19 dataset used for analysis
│
└── 📖 README.md
    └── Project documentation
```

The notebook contains the complete workflow, including data loading, data-quality checks, country-level analysis, visualizations, correlation analysis, summary creation, and findings.

---

# 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| 🐍 **Python** | Main programming language |
| 🐼 **Pandas** | Data loading, cleaning, grouping, aggregation, and analysis |
| 🔢 **NumPy** | Numerical data handling |
| 📊 **Matplotlib** | Creating charts and plots |
| 🎨 **Seaborn** | Statistical visualizations |
| 📓 **Jupyter Notebook** | Interactive development and analysis |

---

# 📊 Dataset

The notebook loads the dataset using:

```python
data = pd.read_csv("Covid19_dataset.csv")
```

The dataset is analyzed using Pandas.

The notebook works with the following important fields:

| Column | Meaning |
|---|---|
| `Date` | Date of the COVID-19 record |
| `Country` | Country represented by the record |
| `Confirmed_Cases` | Recorded confirmed COVID-19 cases |
| `Deaths` | Recorded COVID-19 deaths |
| `Recovered` | Recorded recovered cases |
| `Active_Cases` | Recorded active cases |

The project uses these fields for country comparison, trend analysis, summary statistics, and correlation analysis.

---

# 🔄 Analysis Workflow

The complete notebook follows this roadmap:

```text
                 START
                   │
                   ▼
          📂 Load COVID Dataset
                   │
                   ▼
          🔎 Inspect Data Structure
                   │
                   ▼
          🧹 Check Data Quality
                   │
          ┌────────┴────────┐
          ▼                 ▼
     Missing Values      Data Types
          │                 │
          └────────┬────────┘
                   ▼
          📅 Convert Date
                   │
                   ▼
          🌍 Country Analysis
                   │
        ┌──────────┼──────────┐
        ▼          ▼          ▼
   🦠 Cases     🕯️ Deaths   💚 Recoveries
        │          │          │
        └──────────┼──────────┘
                   ▼
          🇮🇳 India Trend
                   │
                   ▼
          🔗 Correlation
                   │
                   ▼
          📋 Final Summary
                   │
                   ▼
          🔑 Key Findings
                   │
                   ▼
                 END
```

---

# 1️⃣ 📚 Import Required Libraries

The project uses four major Python libraries:

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

### Why these libraries?

### 🐼 Pandas

Pandas is used for:

- Reading the CSV file
- Working with DataFrames
- Checking data types
- Finding missing values
- Grouping records
- Calculating maximum values
- Creating the final summary

### 🔢 NumPy

NumPy is imported for numerical data handling and identifying numeric columns.

### 📊 Matplotlib

Matplotlib is used as the base visualization library.

### 🎨 Seaborn

Seaborn is used to create cleaner statistical charts such as:

- Bar plots
- Line plots
- Heatmaps

---

# 2️⃣ 📂 Load Dataset

The dataset is loaded using:

```python
data = pd.read_csv("Covid19_dataset.csv")
```

The DataFrame is then displayed:

```python
data
```

This is the first step of the analysis because all later operations are performed on the loaded DataFrame.

---

# 3️⃣ 🔎 Dataset Structure

The notebook checks the available columns using:

```python
print(list(data.columns))
```

This provides an overview of the fields available in the dataset.

Understanding the column names is important before selecting columns for analysis.

---

# 4️⃣ 🧹 Data Quality Check

Data quality is checked before performing detailed analysis.

The notebook uses:

```python
data.isna().sum()
```

This identifies the number of missing values in each column.

Checking missing values helps determine whether the dataset requires cleaning before analysis.

---

## 🔤 Data Types

The notebook checks column data types using:

```python
data.dtypes
```

This helps identify whether columns are stored as:

- Numeric values
- Text/object values
- Date-related values

---

## 📅 Convert Date Column

The `Date` column is converted into a Pandas datetime format:

```python
data["Date"] = pd.to_datetime(data["Date"])
```

After conversion, the notebook checks the data types again:

```python
data.dtypes
```

Using a proper datetime format is important for time-based analysis, including the India death trend.

---

# 5️⃣ 🌍 Country-Level Dataset Overview

The notebook identifies all unique countries:

```python
print(list(data["Country"].unique()))
```

It also calculates the total number of unique countries:

```python
data["Country"].nunique()
```

This provides an overview of the geographical coverage of the dataset.

---

## 📊 Country Record Counts

The project also uses:

```python
data["Country"].value_counts()
```

This counts how many records are available for each country.

This helps understand how frequently each country appears in the dataset.

---

# 6️⃣ 🦠 Confirmed COVID-19 Cases by Country

The notebook calculates the maximum recorded confirmed cases for each country:

```python
country_base = data.groupby("Country")["Confirmed_Cases"].max()
```

The result is then displayed:

```python
country_base
```

---

## 📊 Confirmed Cases Visualization

A Seaborn bar plot is used:

```python
plt.figure(figsize=(14,7))

sns.barplot(country_base, palette="viridis")

for i,v in enumerate(country_base.values):
    plt.text(
        i,
        v + 5000,
        str(v),
        ha="center",
        fontsize=9,
        weight="bold"
    )

plt.title(
    "Country wise total confirmed cases of COVID-19",
    weight="bold",
    fontsize=20
)

plt.tight_layout()
plt.show()
```

### What the chart shows

The chart compares the maximum recorded confirmed COVID-19 cases between countries in the dataset.

The values are displayed directly above the bars, making the comparison easier to read.

---

# 7️⃣ 🕯️ COVID-19 Deaths by Country

The notebook calculates the maximum recorded deaths for each country:

```python
country_deaths = data.groupby("Country")["Deaths"].max()
```

The result is displayed before visualization.

---

## 📊 Deaths Visualization

The project creates a bar chart using Seaborn:

```python
plt.figure(figsize=(14, 7))

sns.barplot(country_deaths, palette="viridis")

for i,v in enumerate(country_deaths.values):
    plt.text(
        i,
        v + 5,
        str(v),
        ha="center",
        weight="bold",
        fontsize=10
    )

plt.title(
    "Total COVID-19 Deaths by Country",
    weight="bold",
    fontsize=20
)

plt.xlabel("Deaths", weight="bold")
plt.ylabel("Country", weight="bold")

plt.tight_layout()
plt.show()
```

### Purpose

This visualization provides a country-level comparison of the maximum recorded COVID-19 deaths in the dataset.

---

# 8️⃣ 🇮🇳 COVID-19 Death Trend in India

The project specifically analyzes India.

The India records are selected using:

```python
india = data[data["Country"] == "India"]
```

The resulting DataFrame contains the COVID-19 records for India.

---

## 📈 India Death Trend Visualization

The notebook uses a line plot:

```python
plt.figure(figsize=(14, 6))

sns.lineplot(
    data=india,
    x="Date",
    y="Deaths",
    marker="o",
    color="crimson",
    markersize=7,
    linewidth=2.5,
    markerfacecolor="white",
    markeredgecolor="crimson",
    markeredgewidth=2
)

plt.grid(
    linestyle="--",
    linewidth=0.7,
    alpha=0.5
)

plt.title(
    "COVID-19 Deaths in India Over Time",
    weight="bold",
    fontsize=20
)

plt.xlabel("Date", weight="bold")
plt.ylabel("Total Deaths", weight="bold")

plt.show()
```

### What this analysis does

The line chart shows how the recorded death count for India changes across the dates available in the dataset.

It provides a simple time-based view of India's COVID-19 death records.

---

# 9️⃣ 💚 COVID-19 Recoveries by Country

The project calculates maximum recorded recoveries for each country:

```python
country_recovered = (
    data.groupby("Country")["Recovered"]
    .max()
    .sort_values(ascending=False)
)
```

Sorting in descending order makes it easier to compare countries from the highest recovery value to the lowest.

---

## 📊 Recovery Visualization

A horizontal bar chart is generated:

```python
plt.figure(figsize=(16, 7))

sns.barplot(
    x=country_recovered.values,
    y=country_recovered.index,
    palette="viridis"
)

for i, v in enumerate(country_recovered.values):
    plt.text(
        v + 500,
        i,
        str(v),
        va="center",
        weight="bold"
    )

plt.title(
    "Total COVID-19 Recoveries by Country",
    fontsize=20,
    weight="bold"
)

plt.xlabel("Recovered Cases", weight="bold")
plt.ylabel("Country", weight="bold")

plt.tight_layout()
plt.show()
```

### Purpose

This chart provides a visual comparison of the maximum recorded recovered cases across countries.

---

# 🔟 🔗 Correlation Analysis

Correlation analysis is used to study relationships between numerical COVID-19 variables.

First, the notebook identifies numeric columns:

```python
num_col = list(
    data.select_dtypes(include="number").columns
)
```

The numeric columns are then displayed.

---

## 🔗 Correlation Matrix

The correlation matrix is calculated using:

```python
corr = data[num_col].corr()
```

A heatmap is created:

```python
plt.figure(figsize=(12,8))

sns.heatmap(
    corr,
    annot=True,
    cmap="Greens"
)

plt.title(
    "Correlation Between COVID-19 Variables",
    fontsize=18,
    weight="bold"
)

plt.show()
```

### What correlation analysis provides

The heatmap provides a visual representation of relationships between numerical variables.

The values shown inside the heatmap help identify the strength and direction of relationships between variables in the dataset.

---

# 📋 Final Country-Wise Summary

The notebook creates a final summary table using:

```python
summary = data.groupby("Country").agg({
    "Confirmed_Cases": "max",
    "Recovered": "max",
    "Deaths": "max",
    "Active_Cases": "max"
})
```

The resulting table combines four major COVID-19 indicators:

| Indicator | Aggregation |
|---|---|
| `Confirmed_Cases` | Maximum |
| `Recovered` | Maximum |
| `Deaths` | Maximum |
| `Active_Cases` | Maximum |

This creates a compact country-wise view of the major indicators analyzed in the project.

---

# 🔑 Key Analysis & Findings

The notebook reports the following findings based on the **maximum recorded values in the dataset**:

| 🏆 Indicator | 🌍 Country | 🔢 Maximum Recorded Value |
|---|---|---:|
| 🦠 Confirmed Cases | **India** | **415,392** |
| 🕯️ Deaths | **India** | **267** |
| 💚 Recoveries | **India** | **212,262** |
| ⚠️ Active Cases | **India** | **202,863** |

---

## 🇮🇳 India Analysis

According to the notebook's analysis:

| 📊 Indicator | 🔢 Maximum Recorded Value |
|---|---:|
| 🦠 Confirmed Cases | **415,392** |
| 💚 Recovered Cases | **212,262** |
| 🕯️ Deaths | **267** |
| ⚠️ Active Cases | **202,863** |

These values are the maximum values reported by the notebook for India.

> **Important:** These findings describe the values present in the supplied dataset. They should not be interpreted as current real-world COVID-19 statistics.

---

# 📈 Visualizations Included

The notebook creates several visualizations to make the analysis easier to understand.

### 🦠 1. Confirmed Cases by Country

**Chart type:** Bar plot

Purpose:

- Compare maximum confirmed cases
- Display country-level differences
- Show values directly above bars

---

### 🕯️ 2. Deaths by Country

**Chart type:** Bar plot

Purpose:

- Compare maximum recorded deaths
- Provide a country-level visual comparison

---

### 🇮🇳 3. Deaths in India Over Time

**Chart type:** Line plot

Purpose:

- Observe the death trend across dates
- Focus specifically on India

---

### 💚 4. Recoveries by Country

**Chart type:** Horizontal bar plot

Purpose:

- Compare maximum recorded recoveries
- Display countries in descending order

---

### 🔗 5. COVID-19 Correlation Heatmap

**Chart type:** Heatmap

Purpose:

- Visualize correlations between numerical variables
- Make relationships easier to identify

---

# 🧠 Data Analysis Concepts Demonstrated

This project covers several important concepts used in beginner-to-intermediate Data Science.

## 📂 Data Loading

```python
pd.read_csv()
```

## 🔎 Data Exploration

```python
head()
dtypes
columns
value_counts()
nunique()
```

## 🧹 Data Quality

```python
isna().sum()
```

## 📅 Date Processing

```python
pd.to_datetime()
```

## 🌍 Grouping

```python
groupby()
```

## 📊 Aggregation

```python
max()
agg()
```

## 🔢 Numeric Column Selection

```python
select_dtypes(include="number")
```

## 🔗 Correlation

```python
corr()
```

## 📊 Visualization

```python
sns.barplot()
sns.lineplot()
sns.heatmap()
```

---

# 🎓 Learning Outcomes

After completing this project, the following skills can be practiced:

### 🐍 Python

- Importing libraries
- Working with variables
- DataFrame manipulation
- Selecting and filtering data
- Basic programming workflow

### 🐼 Pandas

- Reading CSV files
- Creating DataFrames
- Inspecting columns
- Checking data types
- Detecting missing values
- Converting dates
- Counting unique values
- Grouping data
- Aggregating data
- Creating summary tables

### 🔢 NumPy

- Working with numerical data
- Identifying numerical columns
- Supporting data-analysis operations

### 📊 Matplotlib

- Creating figures
- Setting figure size
- Adding titles
- Adding axis labels
- Displaying charts
- Formatting plots

### 🎨 Seaborn

- Bar plots
- Line plots
- Heatmaps
- Statistical visualization

### 📈 Data Analysis

- Exploratory Data Analysis
- Country comparison
- Trend analysis
- Correlation analysis
- Summary generation
- Finding key patterns

---

# ▶️ How to Run the Project

## 1. Install Python

Python 3.10 or newer is recommended.

Check your version:

```bash
python --version
```

---

## 2. Install Required Libraries

Run:

```bash
pip install numpy pandas matplotlib seaborn jupyter
```

---

## 3. Keep the Dataset in the Correct Location

The notebook expects:

```text
Covid19_dataset.csv
```

The CSV file should be available in the same working directory as the notebook, unless the path in the notebook is changed.

---

## 4. Start Jupyter Notebook

Run:

```bash
jupyter notebook
```

Open the notebook:

```text
Covid-19.ipynb
```

---

## 5. Run the Notebook

Run the cells from top to bottom.

Recommended order:

```text
1. Import libraries
2. Load dataset
3. Inspect columns
4. Check missing values
5. Check data types
6. Convert Date
7. Explore countries
8. Analyze confirmed cases
9. Analyze deaths
10. Analyze India
11. Analyze recoveries
12. Analyze correlation
13. Generate final summary
14. Review findings
15. Read conclusion
```

---

# 📌 Expected Project Flow

When the notebook is executed successfully, the analysis progresses through:

```text
📥 Dataset Loaded
       ↓
🔎 Dataset Inspected
       ↓
🧹 Data Quality Checked
       ↓
📅 Date Converted
       ↓
🌍 Countries Identified
       ↓
🦠 Confirmed Cases Compared
       ↓
🕯️ Deaths Compared
       ↓
🇮🇳 India Trend Analyzed
       ↓
💚 Recoveries Compared
       ↓
🔗 Correlation Calculated
       ↓
📋 Summary Generated
       ↓
🔑 Findings Presented
```

---

# 💡 Why This Project Is Useful

COVID-19 data provides a practical example for learning exploratory data analysis.

Instead of analyzing an artificial collection of numbers, the project works with records containing:

- Dates
- Countries
- Confirmed cases
- Deaths
- Recoveries
- Active cases

This allows common Data Science techniques to be practiced in a meaningful analytical context.

The project also demonstrates how raw tabular data can be converted into visual information that is easier to compare and interpret.

---

# 🔮 Future Improvements

The current notebook provides a strong foundation for further analysis.

Possible improvements include:

## 📅 Time-Series Analysis

- Confirmed cases over time
- Recoveries over time
- Active cases over time
- Country-specific time trends
- Monthly trend analysis

## 🌍 Advanced Country Comparison

- Top countries by confirmed cases
- Top countries by recoveries
- Top countries by deaths
- Active-case comparisons
- Country ranking tables

## 📊 Additional Visualizations

- Box plots
- Count plots
- Area charts
- Histograms
- Pair plots
- Stacked bar charts
- Interactive charts

## 🧮 Additional Metrics

- Recovery rate
- Death rate
- Active-case percentage
- Cases per population, if population data is available
- Country-wise growth rate

## 🖥️ Dashboard

The analysis could be converted into an interactive dashboard using:

- Streamlit
- Plotly
- Dash

Possible dashboard controls could include:

```text
Country Filter
Date Filter
Metric Selector
Chart Selector
```

## 🤖 Advanced Data Science

The project could later be extended to include:

- Time-series forecasting
- Trend prediction
- Machine learning
- Clustering countries
- Anomaly detection

These features are not part of the current notebook, but they are possible future extensions.

---

# ⚠️ Notes & Limitations

- The analysis is based only on the supplied `Covid19_dataset.csv`.
- The notebook uses **maximum recorded values** for several country-level comparisons.
- The results therefore represent the dataset's recorded maximums, not necessarily totals calculated by summing every row.
- The notebook specifically filters India for its death-trend analysis.
- The project checks missing values but does not introduce a separate missing-value imputation workflow in the current notebook.
- The correlation analysis considers the numeric columns available in the dataset.
- The findings section reflects the values produced by the current notebook.
- COVID-19 data can vary depending on source, reporting methodology, date, and revisions.

> 📌 **Data interpretation note:** This project is intended for educational exploratory analysis. It is not a source for current public-health statistics.

---

# 🧩 Project Architecture

The project can be viewed as five simple analytical layers:

```text
┌─────────────────────────────────────┐
│          📂 DATA SOURCE             │
│       Covid19_dataset.csv           │
└──────────────────┬──────────────────┘
                   ↓
┌─────────────────────────────────────┐
│          🧹 DATA PREPARATION        │
│   Missing Values • Data Types       │
│   Date Conversion                   │
└──────────────────┬──────────────────┘
                   ↓
┌─────────────────────────────────────┐
│           🔎 EXPLORATION             │
│ Countries • Records • Columns       │
└──────────────────┬──────────────────┘
                   ↓
┌─────────────────────────────────────┐
│          📊 ANALYSIS                │
│ Cases • Deaths • Recovery • Active  │
│ India Trend • Correlation           │
└──────────────────┬──────────────────┘
                   ↓
┌─────────────────────────────────────┐
│       📈 VISUALIZATION & FINDINGS   │
│ Charts • Summary • Key Findings     │
└─────────────────────────────────────┘
```

---

# 🏆 Project Highlights

### ⭐ Complete EDA Workflow

The notebook covers the major stages of a basic exploratory data-analysis project.

### ⭐ Multiple Visualizations

Different chart types are used to analyze different aspects of the dataset.

### ⭐ Country-Level Comparison

COVID-19 indicators are compared across countries.

### ⭐ India-Focused Analysis

A dedicated time-series visualization is created for India's recorded deaths.

### ⭐ Correlation Analysis

A heatmap is used to explore relationships between numerical variables.

### ⭐ Final Summary

A country-wise summary combines confirmed cases, recoveries, deaths, and active cases.

---

# 🤝 Contributing

If you want to improve this project, you can:

```text
1. Fork the repository
2. Create a new branch
3. Add your improvement
4. Run and test the notebook
5. Commit your changes
6. Push the branch
7. Create a Pull Request
```

Ideas for contributions include:

- Better visualizations
- Additional statistical analysis
- Interactive dashboard
- Improved data cleaning
- Additional country comparisons
- Time-series analysis

---

# 👨‍💻 Author

<div align="center">

## Ayush Donga

🎓 **B.Sc. IT Student**

🐍 **Python & Data Analysis Learner**

📊 **Aspiring Data Scientist**

🤖 **AI & Machine Learning Enthusiast**

### Building practical projects while learning Data Science 🚀

</div>

---

# 🙏 Acknowledgements

This project uses the Python Data Science ecosystem, including:

- 🐍 Python
- 🐼 Pandas
- 🔢 NumPy
- 📊 Matplotlib
- 🎨 Seaborn
- 📓 Jupyter Notebook

These open-source tools provide the foundation for loading, analyzing, and visualizing structured data.

---

# 📄 License

This project is created for **educational and learning purposes**.

You are free to study, modify, and extend the project according to your requirements.

If you use the project as a base for another project, keeping attribution is appreciated.

---

<div align="center">

---

## 🦠 COVID-19 Data Analysis

### 📊 Turning Data Into Insights With Python

**Load → Clean → Explore → Analyze → Visualize → Understand**

### ⭐ If you find this project useful, consider giving the repository a Star!

**Made with ❤️ using Python, Pandas, NumPy, Matplotlib, Seaborn & Jupyter**

</div>
