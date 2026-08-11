<div align="center">

# 🌍 World Happiness Data Analysis

### 📊 Exploring Global Happiness with Python

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Analysis-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C?style=for-the-badge)](https://matplotlib.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Visualization-4C72B0?style=for-the-badge)](https://seaborn.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)

<br>

**📂 Load → 🔎 Explore → 🧹 Check → 📊 Analyze → 📈 Visualize → 💡 Understand**

</div>

---

## 📌 Project Overview

**World Happiness Data Analysis** is an Exploratory Data Analysis (EDA) project created using **Python, Pandas, NumPy, Matplotlib, and Seaborn**.

The project analyzes the **2015 World Happiness dataset** to understand how happiness scores vary between countries and regions and how happiness relates to factors such as **economy, family, health, freedom, trust, generosity, and the Dystopia Residual**.

The notebook follows a clean and practical Data Science workflow, beginning with dataset loading and data-quality checks and continuing through country comparisons, regional analysis, happiness classification, visualization, and correlation analysis.

### 🔍 Main areas explored

- 🏆 Top 10 happiest countries
- 📉 Bottom 10 happiest countries
- 🕊️ Freedom vs Happiness Score
- 🌎 Average happiness by region
- 😊 Happiness-level classification
- 🔗 Correlation between numerical indicators
- 📊 Descriptive statistics
- 🧹 Missing-value and duplicate checks

> 💡 **Project goal:** Turn a structured global happiness dataset into clear comparisons, visual patterns, and analytical insights using Python.

---

# 🎯 Objectives

The main objectives of this project are:

- 📂 Load the World Happiness dataset
- 🔎 Understand the dataset structure and columns
- 🧹 Check missing values and duplicate records
- 🧬 Inspect column data types
- 📐 Generate descriptive statistics
- 🏆 Identify the top 10 happiest countries
- 📉 Identify the bottom 10 happiest countries
- 🕊️ Explore the relationship between Freedom and Happiness Score
- 🌎 Compare average happiness across regions
- 😊 Categorize countries into High, Medium, and Low Happiness
- 🔗 Analyze correlations between numerical variables
- 📈 Present results through clear and attractive visualizations
- 💡 Summarize the most important findings from the analysis

---

# 🗂️ Table of Contents

- [📌 Project Overview](#-project-overview)
- [🎯 Objectives](#-objectives)
- [📂 Project Structure](#-project-structure)
- [🛠️ Technology Stack](#️-technology-stack)
- [📊 Dataset](#-dataset)
- [🔄 Analysis Workflow](#-analysis-workflow)
- [📥 Load the Dataset](#-1-load-the-dataset)
- [🔎 Initial Data Exploration](#-2-initial-data-exploration)
- [🧹 Data Quality Check](#-3-data-quality-check)
- [📐 Descriptive Statistics](#-4-descriptive-statistics)
- [🏆 Top 10 Happiest Countries](#-5-top-10-happiest-countries)
- [📉 Bottom 10 Happiest Countries](#-6-bottom-10-happiest-countries)
- [🕊️ Freedom vs Happiness](#-7-freedom-vs-happiness)
- [🌎 Happiness by Region](#-8-happiness-by-region)
- [😊 Happiness Classification](#-9-happiness-level-classification)
- [🔗 Correlation Analysis](#-10-correlation-analysis)
- [🔑 Key Findings](#-key-findings)
- [📊 Visualization Summary](#-visualization-summary)
- [🧠 Concepts Practiced](#-concepts-practiced)
- [▶️ How to Run](#️-how-to-run)
- [🎓 Learning Outcomes](#-learning-outcomes)
- [🔮 Future Improvements](#-future-improvements)
- [⚠️ Notes & Limitations](#️-notes--limitations)
- [🤝 Contributing](#-contributing)
- [👨‍💻 Author](#-author)
- [📄 License](#-license)

---

# 📂 Project Structure

```text
📦 World-Happiness-Data-Analysis
│
├── 📓 Happiness_dataset.ipynb
│   └── Complete exploratory data analysis notebook
│
├── 📄 2015.csv
│   └── World Happiness dataset used in the notebook
│
└── 📖 README.md
    └── Project documentation
```

### 📁 File Description

| File | Purpose |
|---|---|
| `Happiness_dataset.ipynb` | Main Jupyter Notebook containing the complete analysis |
| `2015.csv` | Dataset loaded by the notebook |
| `README.md` | Project documentation |

---

# 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| 🐍 **Python** | Core programming language |
| 🐼 **Pandas** | Data loading, grouping, transformation, and analysis |
| 🔢 **NumPy** | Numerical computing support |
| 📊 **Matplotlib** | Creating and formatting charts |
| 🎨 **Seaborn** | Statistical visualization |
| 📓 **Jupyter Notebook** | Interactive analysis environment |

---

# 📊 Dataset

The notebook loads the dataset with:

```python
df = pd.read_csv("2015.csv")
```

The dataset contains **158 countries** and **12 columns**.

### 📋 Dataset Columns

| Column | Description |
|---|---|
| `Country` | Country name |
| `Region` | Geographical region |
| `Happiness Rank` | Ranking based on Happiness Score |
| `Happiness Score` | Overall happiness score |
| `Standard Error` | Standard error associated with the happiness score |
| `Economy (GDP per Capita)` | Economic contribution indicator |
| `Family` | Family/social support indicator |
| `Health (Life Expectancy)` | Health and life-expectancy indicator |
| `Freedom` | Freedom to make life choices |
| `Trust (Government Corruption)` | Trust/corruption-related indicator |
| `Generosity` | Generosity indicator |
| `Dystopia Residual` | Dystopia Residual component |

### 📌 Dataset Summary

```text
🌍 Countries     : 158
📋 Columns       : 12
📊 Numeric Data  : 10 columns
🔤 Text Data     : Country, Region
```

The notebook confirms that all 158 records are non-null across the 12 columns.

---

# 🔄 Analysis Workflow

The complete project follows this workflow:

```text
                 📄 2015.csv
                     │
                     ▼
              📥 Load Dataset
                     │
                     ▼
              🔎 Explore Data
                     │
                     ▼
             🧹 Quality Checks
                     │
          ┌──────────┼──────────┐
          ▼          ▼          ▼
      Missing     Duplicate   Data Types
       Values       Check       Check
          │          │          │
          └──────────┼──────────┘
                     ▼
              📐 Statistics
                     │
                     ▼
        ┌────────────┼────────────┐
        ▼            ▼            ▼
   🏆 Top 10      📉 Bottom 10   🕊️ Freedom
        │            │            │
        └────────────┼────────────┘
                     ▼
               🌎 Regions
                     │
                     ▼
               😊 Classification
                     │
                     ▼
               🔗 Correlation
                     │
                     ▼
                🔑 Findings
```

---

# 📥 1. Load the Dataset

The project starts by importing the required libraries:

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

The CSV file is then loaded:

```python
df = pd.read_csv("2015.csv")
```

The DataFrame is displayed to inspect the initial dataset.

---

# 🔎 2. Initial Data Exploration

The notebook explores the dataset using several basic Pandas operations.

### First 5 Records

```python
df.head(5)
```

### Column Names

```python
print(list(df.columns))
```

These operations provide an initial understanding of the dataset structure and available variables.

---

# 🧹 3. Data Quality Check

The notebook checks for missing values:

```python
df.isna().sum()
```

The output shows:

```text
Missing values = 0
```

for every column.

### ♻️ Duplicate Check

Duplicate records are checked using:

```python
df.duplicated().sum()
```

The result is:

```text
Duplicate records = 0
```

### 🧬 Data Types

The notebook checks:

```python
df.dtypes
```

The dataset contains:

- `str` columns for `Country` and `Region`
- `int64` for `Happiness Rank`
- `float64` for the remaining numerical indicators

### ℹ️ Dataset Information

```python
df.info()
```

This confirms:

```text
158 entries
12 columns
All columns have 158 non-null values
```

---

# 📐 4. Descriptive Statistics

The notebook generates descriptive statistics using:

```python
df.describe()
```

### 📊 Happiness Score Statistics

| Statistic | Value |
|---|---:|
| Count | 158 |
| Mean | 5.375734 |
| Standard Deviation | 1.145010 |
| Minimum | 2.839000 |
| 25th Percentile | 4.526000 |
| Median | 5.232500 |
| 75th Percentile | 6.243750 |
| Maximum | 7.587000 |

This gives a statistical overview of the distribution of Happiness Scores across the 158 countries.

---

# 🏆 5. Top 10 Happiest Countries

The notebook calculates the top 10 countries using:

```python
top_10 = (
    df.groupby("Country")["Happiness Score"]
    .max()
    .sort_values(ascending=False)
    .head(10)
)
```

### 🥇 Top 10 Results

| Rank | Country | Happiness Score |
|---:|---|---:|
| 🥇 1 | Switzerland | **7.587** |
| 🥈 2 | Iceland | **7.561** |
| 🥉 3 | Denmark | **7.527** |
| 4 | Norway | **7.522** |
| 5 | Canada | **7.427** |
| 6 | Finland | **7.406** |
| 7 | Netherlands | **7.378** |
| 8 | Sweden | **7.364** |
| 9 | New Zealand | **7.286** |
| 10 | Australia | **7.284** |

### 📊 Visualization

A Seaborn bar chart is used to display the top 10 countries.

```python
sns.barplot(top_10, palette="viridis")
```

The values are also written above the bars for easier comparison.

---

# 📉 6. Bottom 10 Happiest Countries

The notebook identifies the bottom 10 countries using:

```python
bottom_10 = (
    df.groupby("Country")["Happiness Score"]
    .min()
    .sort_values()
    .head(10)
)
```

### 📉 Bottom 10 Results

| Rank | Country | Happiness Score |
|---:|---|---:|
| 1 | Togo | **2.839** |
| 2 | Burundi | **2.905** |
| 3 | Syria | **3.006** |
| 4 | Benin | **3.340** |
| 5 | Rwanda | **3.465** |
| 6 | Afghanistan | **3.575** |
| 7 | Burkina Faso | **3.587** |
| 8 | Ivory Coast | **3.655** |
| 9 | Guinea | **3.656** |
| 10 | Chad | **3.667** |

### 📊 Visualization

A horizontal Seaborn bar chart is used to make the country comparison easy to read.

---

# 🕊️ 7. Freedom vs Happiness

The notebook explores the relationship between:

```text
Freedom
      ↕
Happiness Score
```

using a scatter plot:

```python
sns.scatterplot(
    data=df,
    x="Freedom",
    y="Happiness Score",
    s=80
)
```

### 🔍 What the scatter plot shows

Each point represents a country.

The visualization allows us to observe whether countries with higher Freedom values tend to have different Happiness Scores.

### 💡 Main Observation

The notebook reports an **observable relationship between Freedom and Happiness Score**.

The correlation analysis later quantifies this relationship.

---

# 🌎 8. Happiness by Region

The notebook calculates the average Happiness Score for each region:

```python
region_happiness = (
    df.groupby("Region")["Happiness Score"]
    .mean()
    .sort_values(ascending=False)
)
```

### 🌍 Regional Results

| Region | Average Happiness Score |
|---|---:|
| 🇦🇺 Australia and New Zealand | **7.285** |
| 🇺🇸 North America | **7.273** |
| 🌍 Western Europe | **6.689619** |
| 🌎 Latin America and Caribbean | **6.144682** |
| 🌏 Eastern Asia | **5.626167** |
| 🌍 Middle East and Northern Africa | **5.406900** |
| 🌍 Central and Eastern Europe | **5.332931** |
| 🌏 Southeastern Asia | **5.317444** |
| 🌏 Southern Asia | **4.580857** |
| 🌍 Sub-Saharan Africa | **4.202800** |

### 📊 Visualization

A horizontal bar chart is used to compare average Happiness Scores across regions.

---

# 😊 9. Happiness Level Classification

The project creates a new categorical feature called:

```text
Happiness Level
```

Countries are classified using the following rules:

| Happiness Score | Category |
|---:|---|
| `>= 6` | 🟢 High Happiness |
| `>= 4 and < 6` | 🟡 Medium Happiness |
| `< 4` | 🔴 Low Happiness |

The classification function is:

```python
def happiness_level(score):
    if score >= 6:
        return "High Happiness"
    elif score >= 4:
        return "Medium Happiness"
    else:
        return "Low Happiness"
```

The new column is created using:

```python
df["Happiness Level"] = (
    df["Happiness Score"].apply(happiness_level)
)
```

---

## 📊 Happiness Classification Results

The notebook reports:

| Happiness Level | Countries |
|---|---:|
| 🟡 Medium Happiness | **93** |
| 🟢 High Happiness | **44** |
| 🔴 Low Happiness | **21** |
| **Total** | **158** |

### 🍩 Visualization

A donut-style pie chart is used to show the proportion of countries in each happiness category.

```text
🟡 Medium Happiness → 93
🟢 High Happiness   → 44
🔴 Low Happiness    → 21
```

This provides a quick overview of how the 158 countries are distributed across the three defined categories.

---

# 🔗 10. Correlation Analysis

The notebook calculates a correlation matrix for all numerical columns:

```python
corr = df.select_dtypes(include="number").corr()
```

The numerical variables include:

```text
Happiness Rank
Happiness Score
Standard Error
Economy (GDP per Capita)
Family
Health (Life Expectancy)
Freedom
Trust (Government Corruption)
Generosity
Dystopia Residual
```

---

# 🔥 Correlation Heatmap

The correlation matrix is visualized using:

```python
sns.heatmap(
    corr,
    annot=True,
    cmap="Greens"
)
```

### 📊 Important Relationships with Happiness Score

The notebook's correlation matrix shows:

| Variable | Correlation with Happiness Score |
|---|---:|
| 💰 Economy (GDP per Capita) | **0.780966** |
| 👨‍👩‍👧 Family | **0.740605** |
| ❤️ Health (Life Expectancy) | **0.724200** |
| 🕊️ Freedom | **0.568211** |
| 🌫️ Dystopia Residual | **0.530474** |
| 🏛️ Trust (Government Corruption) | **0.395199** |
| 🎁 Generosity | **0.180319** |
| 📏 Standard Error | **-0.177254** |

### 💡 Interpretation

Within this dataset, the strongest positive correlations with Happiness Score are observed for:

1. 💰 Economy
2. 👨‍👩‍👧 Family
3. ❤️ Health
4. 🕊️ Freedom

> ⚠️ **Correlation does not prove causation.** These values describe statistical relationships in the dataset and should not be interpreted as proof that one factor directly causes happiness.

---

# 📊 Visualization Summary

| # | Visualization | Purpose |
|---:|---|---|
| 1️⃣ | 🏆 Top 10 Happiest Countries | Compare highest Happiness Scores |
| 2️⃣ | 📉 Bottom 10 Happiest Countries | Compare lowest Happiness Scores |
| 3️⃣ | 🕊️ Freedom vs Happiness | Explore the relationship between Freedom and Happiness |
| 4️⃣ | 🌎 Happiness by Region | Compare regional average Happiness Scores |
| 5️⃣ | 🍩 Happiness Level | Show High/Medium/Low classification |
| 6️⃣ | 🔥 Correlation Heatmap | Analyze relationships among numerical variables |

---

# 🔑 Key Findings

## 🏆 Country-Level Findings

- 🥇 **Switzerland** has the highest Happiness Score at **7.587**.
- 🥈 **Iceland** ranks second with **7.561**.
- 🥉 **Denmark** ranks third with **7.527**.
- 📉 **Togo** has the lowest Happiness Score at **2.839**.
- Happiness Scores vary substantially across the countries included in the dataset.

---

## 🌎 Regional Findings

- 🇦🇺 **Australia and New Zealand** have the highest regional average at **7.285**.
- 🇺🇸 **North America** follows with **7.273**.
- 🌍 **Western Europe** has an average of approximately **6.69**.
- 🌍 **Sub-Saharan Africa** has the lowest regional average in this analysis at approximately **4.20**.

---

## 😊 Happiness Classification

Out of 158 countries:

```text
🟡 Medium Happiness → 93
🟢 High Happiness   → 44
🔴 Low Happiness    → 21
```

The largest group is therefore **Medium Happiness** under the classification rules used in the notebook.

---

## 🔗 Correlation Findings

The strongest positive relationships with Happiness Score in the notebook are:

```text
💰 Economy       → 0.780966
👨‍👩‍👧 Family      → 0.740605
❤️ Health        → 0.724200
🕊️ Freedom       → 0.568211
```

These relationships provide useful analytical evidence for comparing economic, social, health, and freedom-related indicators with overall Happiness Score.

---

# 🧠 Concepts Practiced

## 🐍 Python

- Importing libraries
- Functions
- Conditional statements
- Applying custom functions to DataFrame columns

## 🐼 Pandas

- `read_csv()`
- DataFrames
- `head()`
- `columns`
- `isna()`
- `duplicated()`
- `dtypes`
- `info()`
- `describe()`
- `groupby()`
- `sort_values()`
- `head()`
- `value_counts()`
- `apply()`
- `select_dtypes()`
- `corr()`

## 🔢 NumPy

NumPy is included as part of the numerical Data Science toolkit used in the project.

## 📊 Matplotlib

- Figure sizing
- Titles
- Axis labels
- Pie charts
- Chart formatting

## 🎨 Seaborn

- Bar plots
- Scatter plots
- Heatmaps
- Statistical visualization

## 📈 Exploratory Data Analysis

```text
Data Loading
     ↓
Data Quality
     ↓
Descriptive Statistics
     ↓
Country Comparison
     ↓
Regional Analysis
     ↓
Classification
     ↓
Correlation
     ↓
Visualization
     ↓
Insights
```

---

# 💡 Why This Project Is Useful

The World Happiness dataset is a useful EDA dataset because it combines:

```text
🌍 Country
🌎 Region
📊 Happiness Score
💰 Economy
👨‍👩‍👧 Family
❤️ Health
🕊️ Freedom
🏛️ Trust
🎁 Generosity
```

This allows a beginner Data Analyst to practice both **categorical analysis** and **numerical analysis** in one project.

Instead of only calculating statistics, the project converts those statistics into visual comparisons and interpretable findings.

---

# ▶️ How to Run

## 1️⃣ Install Python

Install Python 3.x.

Check your version:

```bash
python --version
```

---

## 2️⃣ Install Required Libraries

```bash
pip install numpy pandas matplotlib seaborn jupyter
```

---

## 3️⃣ Keep the Files Together

Your project folder should contain:

```text
Happiness_dataset.ipynb
2015.csv
README.md
```

The notebook loads:

```python
pd.read_csv("2015.csv")
```

Therefore, the CSV should normally be in the notebook's working directory.

---

## 4️⃣ Start Jupyter Notebook

```bash
jupyter notebook
```

Then open:

```text
Happiness_dataset.ipynb
```

---

## 5️⃣ Run the Notebook

Run the cells from top to bottom.

### Recommended order

```text
1. 📚 Import libraries
2. 📂 Load dataset
3. 🔎 Explore first records
4. 📋 Inspect columns
5. 🧹 Check missing values
6. ♻️ Check duplicates
7. 🧬 Check data types
8. ℹ️ Inspect DataFrame information
9. 📐 Generate descriptive statistics
10. 🏆 Analyze top 10 countries
11. 📉 Analyze bottom 10 countries
12. 🕊️ Analyze Freedom vs Happiness
13. 🌎 Analyze happiness by region
14. 😊 Create happiness categories
15. 🍩 Visualize happiness levels
16. 🔗 Calculate correlations
17. 🔥 Generate correlation heatmap
18. 🔑 Review findings
```

---

# 📌 Expected Project Flow

```text
                 🌍 WORLD HAPPINESS
                       │
                       ▼
                 📥 Load 2015.csv
                       │
                       ▼
                  🔎 Explore
                       │
                       ▼
                 🧹 Validate
                       │
                       ▼
              📐 Statistics
                       │
          ┌────────────┼────────────┐
          ▼            ▼            ▼
       🏆 Top 10    📉 Bottom 10   🕊️ Freedom
          │            │            │
          └────────────┼────────────┘
                       ▼
                  🌎 Regions
                       │
                       ▼
                😊 Classification
                       │
                       ▼
                 🔗 Correlation
                       │
                       ▼
                  📊 Charts
                       │
                       ▼
                  💡 Insights
```

---

# 🎓 Learning Outcomes

After completing this project, you will have practical experience with:

### 🐼 Data Analysis

- Loading CSV datasets
- Exploring DataFrames
- Checking data quality
- Generating descriptive statistics
- Grouping and aggregating records

### 📊 Visualization

- Bar charts
- Horizontal bar charts
- Scatter plots
- Donut/pie charts
- Correlation heatmaps

### 🧠 Analytical Thinking

- Ranking countries
- Comparing regions
- Creating custom categories
- Identifying relationships
- Interpreting correlation values
- Communicating findings

### 🐍 Python Skills

- Writing functions
- Using `if/elif/else`
- Applying functions to DataFrame columns
- Combining Pandas operations
- Building a complete analysis workflow

---

# 🔮 Future Improvements

The current project can be expanded into a more advanced Data Science project.

## 📊 More Visualizations

Add:

- Distribution plots
- Box plots
- Pair plots
- Country-level comparison charts
- Regional distribution charts

## 🗺️ Geographic Analysis

Create a world map showing Happiness Scores by country.

Possible tools:

```text
Plotly
GeoPandas
Folium
```

## 📈 Advanced Statistical Analysis

Explore:

- Regression analysis
- Statistical significance
- Multiple-variable relationships
- Outlier detection

## 🤖 Machine Learning

Use the dataset to experiment with:

- Linear Regression
- Random Forest
- Decision Trees
- Feature importance
- Happiness-score prediction

## 🖥️ Interactive Dashboard

Convert the notebook into a dashboard using:

```text
Streamlit
Plotly
Dash
```

Possible controls:

```text
🌎 Region Filter
🏆 Happiness Rank
📊 Happiness Score
💰 Economy
🕊️ Freedom
❤️ Health
```

---

# ⚠️ Notes & Limitations

- This project analyzes the **2015 World Happiness dataset** loaded from `2015.csv`.
- The notebook contains **158 country records and 12 columns**.
- The analysis is descriptive and exploratory.
- Correlation indicates statistical association, not causation.
- The happiness classification thresholds are custom rules defined in the notebook:
  - `>= 6` → High Happiness
  - `>= 4 and < 6` → Medium Happiness
  - `< 4` → Low Happiness
- Regional averages are calculated using the mean Happiness Score for each region.
- The findings describe the supplied dataset and should not be interpreted as current global happiness statistics.

---

# 🏆 Project Highlights

<div align="center">

| Analysis Area | Status |
|---|:---:|
| 📂 Dataset Loading | ✅ |
| 🔎 Data Exploration | ✅ |
| 🧹 Missing-Value Check | ✅ |
| ♻️ Duplicate Check | ✅ |
| 🧬 Data-Type Analysis | ✅ |
| 📐 Descriptive Statistics | ✅ |
| 🏆 Top 10 Countries | ✅ |
| 📉 Bottom 10 Countries | ✅ |
| 🕊️ Freedom Analysis | ✅ |
| 🌎 Regional Analysis | ✅ |
| 😊 Happiness Classification | ✅ |
| 🍩 Happiness Visualization | ✅ |
| 🔗 Correlation Analysis | ✅ |
| 🔥 Correlation Heatmap | ✅ |
| 🔑 Key Findings | ✅ |

</div>

---

# 🤝 Contributing

If you want to improve this project:

```text
1. Fork the repository
2. Create a new branch
3. Add your analysis or improvement
4. Test the notebook
5. Commit your changes
6. Push the branch
7. Open a Pull Request
```

Possible improvements include:

- 📊 New charts
- 🗺️ Geographic visualizations
- 📈 Statistical models
- 🤖 Machine-learning experiments
- 🖥️ Interactive dashboards
- 🧹 Improved data-processing techniques

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

---

<div align="center">

---

# 🌍 World Happiness Data Analysis

### **Data → Analysis → Visualization → Insights**

**Built with 🐍 Python · 🐼 Pandas · 🔢 NumPy · 📊 Matplotlib · 🎨 Seaborn**

### ⭐ If you found this project useful, consider giving the repository a Star!

**Made with ❤️ while learning Data Science**

</div>
