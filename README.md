<div align="center">

# 🚢 Titanic Dataset | Data Analysis Project

### 📊 Exploratory Data Analysis with Python

**Clean 🧹 · Explore 🔎 · Analyze 📈 · Visualize 📊 · Understand 💡**

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C?style=for-the-badge)](https://matplotlib.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Visualization-4C72B0?style=for-the-badge)](https://seaborn.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)

<br>

> **An exploratory analysis of passenger survival patterns across gender, class, age, embarkation port, and numerical passenger attributes.**

</div>

---

# 📌 Project Overview

The **Titanic Dataset | Data Analysis Project** is an exploratory data analysis project created using **Python, Pandas, NumPy, Matplotlib, and Seaborn**.

The notebook follows a structured data-analysis workflow, beginning with dataset loading and inspection and continuing through data-quality checks, descriptive statistics, passenger survival analysis, visualization, and correlation analysis.

The main purpose of this project is to understand the structure of the Titanic passenger dataset and explore how survival outcomes vary across different passenger characteristics.

### 🔍 The analysis focuses on:

- 👥 Survival by gender
- 🎟️ Survival by passenger class
- 🧳 Passenger distribution across classes
- 🎂 Age distribution by survival status
- 🍩 Overall survival proportion
- ⚓ Survival by embarkation port
- 🔗 Correlations between numerical variables
- 🧹 Missing-value and duplicate checks

> ✨ The project is implemented as a Jupyter Notebook and is suitable for practicing the fundamentals of Data Analysis and Data Visualization.

---

# 🎯 Project Goals

The notebook is designed to:

- 🧹 Inspect and prepare the Titanic dataset
- 🔎 Understand the structure and quality of the data
- 📋 Review the first and last records
- 🧬 Understand column data types
- 📊 Generate descriptive statistics
- ♻️ Check for duplicate records
- 👥 Analyze survival patterns by gender
- 🎟️ Compare survival across passenger classes
- 🎂 Explore age distribution and survival
- ⚓ Analyze survival based on embarkation port
- 🔗 Examine relationships between numerical variables
- 📈 Present findings through easy-to-read visualizations

---

# 🗂️ Table of Contents

- [📌 Project Overview](#-project-overview)
- [🎯 Project Goals](#-project-goals)
- [📂 Project Structure](#-project-structure)
- [🛠️ Technology Stack](#️-technology-stack)
- [📊 Dataset](#-dataset)
- [🔄 Analysis Workflow](#-analysis-workflow)
- [📥 Load the Dataset](#-1-load-the-dataset)
- [👀 Explore the Dataset](#-2-explore-the-dataset)
- [🧹 Data Cleaning](#-3-data-cleaning)
- [🧬 Data Types & Columns](#-4-data-types--columns)
- [📐 Descriptive Statistics](#-5-descriptive-statistics)
- [♻️ Duplicate Check](#-6-duplicate-check)
- [📈 Survival Analysis](#-7-survival-analysis)
- [👩 Survival by Gender](#-survival-by-gender)
- [🎟️ Survival by Passenger Class](#-survival-by-passenger-class)
- [🧳 Passengers per Class](#-total-passengers-per-class)
- [🎂 Age Distribution](#-age-distribution-by-survival)
- [🍩 Overall Survival](#-overall-passenger-survival)
- [⚓ Embarkation Analysis](#-survival-by-embarkation-port)
- [🔥 Correlation Analysis](#-correlation-analysis)
- [🔑 Key Findings](#-key-findings)
- [📊 Visualization Summary](#-visualization-summary)
- [🎓 Learning Outcomes](#-learning-outcomes)
- [▶️ How to Run](#️-how-to-run)
- [🔮 Future Improvements](#-future-improvements)
- [⚠️ Notes](#️-notes)
- [🤝 Contributing](#-contributing)
- [👨‍💻 Author](#-author)
- [📄 License](#-license)

---

# 📂 Project Structure

```text
📦 Titanic-Data-Analysis
│
├── 📓 Titanic.ipynb
│   └── Complete exploratory data analysis notebook
│
├── 📄 titanic_dataset.csv
│   └── Titanic passenger dataset
│
└── 📖 README.md
    └── Project documentation
```

### 📁 File Description

| File | Purpose |
|---|---|
| `Titanic.ipynb` | Main Jupyter Notebook containing the complete analysis |
| `titanic_dataset.csv` | Dataset loaded and analyzed by the notebook |
| `README.md` | Documentation for the project |

---

# 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| 🐍 **Python** | Core programming language |
| 🐼 **Pandas** | Data loading, cleaning, transformation, and analysis |
| 🔢 **NumPy** | Numerical computing support |
| 📊 **Matplotlib** | Creating and formatting visualizations |
| 🎨 **Seaborn** | Statistical plots and data visualization |
| 📓 **Jupyter Notebook** | Interactive development and analysis |

---

# 📊 Dataset

The notebook loads the dataset with:

```python
data = pd.read_csv("titanic_dataset.csv")
```

The dataset contains:

```text
👥 Records  : 891
📋 Columns  : 12
```

The notebook works with passenger information and survival-related attributes.

### Important Variables Used

| Column | Description |
|---|---|
| `Survived` | Survival outcome |
| `Sex` | Passenger gender |
| `Pclass` | Passenger class |
| `Age` | Passenger age |
| `SibSp` | Number of siblings/spouses aboard |
| `Parch` | Number of parents/children aboard |
| `Fare` | Passenger fare |
| `Embarked` | Port of embarkation |

The notebook also displays the complete list of columns using:

```python
print(list(data.columns))
```

---

# 🔄 Analysis Workflow

The project follows a simple and practical EDA pipeline:

```text
                 📄 Titanic Dataset
                         │
                         ▼
                 📥 Load CSV File
                         │
                         ▼
                  👀 Explore Data
                         │
                         ▼
                🧹 Check Missing Data
                         │
                         ▼
                🛠️ Handle Age Values
                         │
                         ▼
               🧬 Inspect Data Types
                         │
                         ▼
                📐 Descriptive Stats
                         │
                         ▼
                ♻️ Duplicate Check
                         │
                         ▼
              👥 Survival Analysis
                         │
          ┌──────────────┼──────────────┐
          ▼              ▼              ▼
       👩 Gender       🎟️ Class       🎂 Age
          │              │              │
          └──────────────┼──────────────┘
                         ▼
                  ⚓ Embarkation
                         │
                         ▼
                  🔗 Correlation
                         │
                         ▼
                   🔑 Findings
```

---

# 📥 1. Load the Dataset

The first step loads the Titanic CSV dataset into a Pandas DataFrame:

```python
data = pd.read_csv("titanic_dataset.csv")
```

The DataFrame is then displayed to provide an initial view of the dataset.

---

# 👀 2. Explore the Dataset

## 🔝 First 5 Records

The notebook uses:

```python
data.head(5)
```

This gives a quick preview of the first five passenger records.

## 🔚 Last 5 Records

The final five records are displayed with:

```python
data.tail(5)
```

These previews help verify that the dataset has loaded correctly and provide a first look at its structure.

---

# 🧹 3. Data Cleaning

The notebook checks missing values using:

```python
data.isna().sum()
```

This identifies how many missing values are present in each column.

### Why check missing values?

Missing data can affect:

- 📊 Statistical calculations
- 📈 Visualizations
- 🔎 Comparisons
- 🧮 Numerical analysis

---

## 🛠️ Handling Missing Age Values

The notebook attempts to handle missing values in the `Age` column using the median:

```python
data["Age"] = data["Age"].fillna(
    data["Age"].median(),
    inplace=True
)
```

The intended approach is median-based filling.

### Why Median?

The median is less influenced by unusually high or low values than the mean, making it a common choice when filling missing age observations.

The notebook then checks the `Age` column again:

```python
data["Age"].isna().sum()
```

> ⚠️ **Implementation note:** The notebook code uses `inplace=True` inside an assignment. In Pandas, this pattern can result in assigning `None` back to the column. This README documents the code as it appears in the notebook rather than silently changing the implementation.

---

# 🧬 4. Data Types & Columns

The notebook checks the data types of all columns:

```python
data.dtypes
```

It also displays the complete list of columns:

```python
print(list(data.columns))
```

Understanding data types is important because different variables require different types of analysis.

For example:

```text
🔢 Numerical → Age, Fare, Pclass, SibSp, Parch
🔤 Categorical → Sex, Embarked
🎯 Target → Survived
```

---

# ℹ️ Dataset Information

The notebook uses:

```python
data.info()
```

This provides a compact overview of:

- 📌 Number of records
- 📋 Number of columns
- 🔢 Data types
- ✅ Non-null values
- 💾 Memory usage

This is one of the most useful first checks when beginning an EDA project.

---

# 📐 5. Descriptive Statistics

The notebook generates statistical summaries using:

```python
data.describe()
```

This provides information such as:

- Count
- Mean
- Standard deviation
- Minimum
- 25th percentile
- Median
- 75th percentile
- Maximum

This helps understand the distribution of numerical passenger attributes.

---

# ♻️ 6. Duplicate Check

Duplicate records are checked using:

```python
data.duplicated().sum()
```

The notebook reports:

```text
Duplicate Records = 0
```

This means the duplicate check did not identify repeated complete rows in the dataset.

---

# 📈 7. Survival Analysis

The main analytical focus of the project is understanding passenger survival.

The target variable is:

```text
Survived
```

where the notebook interprets the categories as:

```text
0 → Did not survive
1 → Survived
```

The project examines survival from several perspectives:

```text
👩 Gender
🎟️ Passenger Class
🎂 Age
⚓ Embarkation Port
🍩 Overall Survival
```

---

# 👩 Survival by Gender

The notebook creates a Seaborn count plot:

```python
plt.figure(figsize=(10,8))

sns.countplot(
    data=data,
    x="Sex",
    hue="Survived",
    palette="viridis"
)

plt.title(
    "Survival by Gender",
    fontsize=18,
    fontweight="bold"
)

plt.xlabel(
    "Gender",
    fontsize=11,
    fontweight="bold"
)

plt.ylabel(
    "Count",
    fontsize=11,
    fontweight="bold"
)

plt.show()
```

### 📊 What this chart shows

The chart compares the number of survivors and non-survivors for each gender category.

### 🔑 Main observation

The notebook finds that:

> 👩 **Female passengers had a much higher survival count than male passengers** in the gender comparison.

This visualization makes the difference between survival outcomes across gender categories easy to observe.

---

# 🎟️ Survival by Passenger Class

The project compares survival across:

```text
1st Class
2nd Class
3rd Class
```

The visualization uses:

```python
sns.countplot(
    data=data,
    x="Pclass",
    hue="Survived"
)
```

### 📊 What this chart shows

The chart compares survivors and non-survivors within each passenger class.

### 🔑 Main observation

According to the notebook:

> 🎟️ **1st-class passengers showed the strongest survival outcome relative to their class size**, while 3rd class had substantially more non-survivors.

This demonstrates why passenger class is an important variable to examine when studying survival patterns.

---

# 🧳 Total Passengers per Class

The notebook calculates passenger counts by class:

```python
count_class = (
    data.groupby("Pclass")["Sex"].count()
)
```

A bar chart is then created.

### 📊 Purpose

This visualization shows how many passengers belonged to each class.

It provides useful context for interpreting the survival-by-class chart because survival counts can be influenced by the number of passengers in each class.

---

# 🎂 Age Distribution by Survival

The project examines passenger age using a histogram:

```python
plt.figure(figsize=(10,7))

sns.histplot(
    data=data,
    x="Age",
    hue="Survived",
    bins=20,
    kde=True
)

plt.title(
    "Age Distribution by Survival",
    fontsize=18,
    fontweight="bold"
)

plt.xlabel(
    "Age",
    fontsize=11,
    fontweight="bold"
)

plt.ylabel(
    "Count",
    fontsize=11,
    fontweight="bold"
)

plt.show()
```

### 🔎 What this chart explores

- Passenger age distribution
- Differences in age distributions between survival groups
- Concentration of passengers across different age ranges
- How survival categories are distributed across age

The notebook notes that survival outcomes varied across passenger ages.

---

# 🍩 Overall Passenger Survival

The overall number of passengers in each survival category is calculated with:

```python
survival_count = data["Survived"].value_counts()
```

The notebook then creates a donut-style chart.

### Visualization

```python
plt.pie(
    survival_count,
    labels=survival_count.index,
    autopct="%1.1f%%",
    startangle=90
)
```

A white circle is added to the center to create the donut appearance.

### 📊 Main Result

The notebook reports:

| Survival Status | Passengers |
|---|---:|
| 🟢 Survived | **302** |
| 🔴 Did not survive | **589** |
| 👥 Total | **891** |

This corresponds approximately to:

```text
🟢 Survived       → 33.9%
🔴 Did not survive → 66.1%
```

The chart provides a quick overall view of the survival distribution.

---

# ⚓ Survival by Embarkation Port

The notebook analyzes survival based on the passenger's embarkation port.

The chart compares:

```text
C → Cherbourg
Q → Queenstown
S → Southampton
```

The visualization uses:

```python
sns.countplot(
    data=data,
    x="Embarked",
    hue="Survived"
)
```

### 🔑 Main observation

The notebook reports:

> ⚓ **Southampton (S) was the largest embarkation group in the dataset, and its chart also shows a large number of non-survivors.**

This analysis demonstrates how a categorical variable can be compared with the survival target.

---

# 🔗 Correlation Analysis

The project selects the following numerical variables:

```python
num_col = [
    "Age",
    "Pclass",
    "SibSp",
    "Parch",
    "Fare"
]
```

These variables represent:

| Variable | Meaning |
|---|---|
| `Age` | Passenger age |
| `Pclass` | Passenger class |
| `SibSp` | Siblings/spouses aboard |
| `Parch` | Parents/children aboard |
| `Fare` | Passenger fare |

---

# 🔥 Correlation Heatmap

The correlation matrix is calculated using:

```python
data[num_col].corr()
```

The notebook visualizes the result using:

```python
sns.heatmap(
    data[num_col].corr(),
    annot=True,
    cmap="Purples",
    fmt=".2f"
)
```

### 📊 What the heatmap shows

The heatmap helps examine relationships among:

```text
Age
Pclass
SibSp
Parch
Fare
```

### 📌 How to read correlation

| Correlation | General Interpretation |
|---:|---|
| `+1` | Strong positive linear relationship |
| `0` | Little or no linear relationship |
| `-1` | Strong negative linear relationship |

> ⚠️ **Correlation does not prove causation.** It only describes the strength and direction of a linear relationship between variables.

---

# 🔑 Key Findings

The notebook summarizes the following observations:

### 👥 Dataset

- **891 passenger records**
- **12 columns**
- **0 duplicate records** reported by the notebook

### 🧹 Data Quality

- Missing values were checked.
- `Age` was identified as requiring handling.
- The notebook attempts median-based handling for missing age values.

### 🍩 Overall Survival

```text
🟢 Survived       : 302
🔴 Did not survive: 589
👥 Total          : 891
```

### 👩 Gender

Female passengers had a much higher survival count than male passengers in the gender comparison.

### 🎟️ Passenger Class

1st-class passengers showed the strongest survival outcome relative to their class size, while 3rd class had substantially more non-survivors.

### ⚓ Embarkation

Southampton (`S`) was the largest embarkation group and also showed a large number of non-survivors.

### 🎂 Age

The age-distribution visualization shows differences in survival outcomes across passenger ages.

### 🔗 Numerical Relationships

The correlation heatmap provides a visual summary of relationships among:

```text
Age
Pclass
SibSp
Parch
Fare
```

---

# 📊 Visualization Summary

| # | Visualization | Purpose |
|---:|---|---|
| 1️⃣ | 👩 Survival by Gender | Compare survival across gender |
| 2️⃣ | 🎟️ Survival by Passenger Class | Compare survival across classes |
| 3️⃣ | 🧳 Total Passengers per Class | Show passenger distribution by class |
| 4️⃣ | 🎂 Age Distribution by Survival | Explore age distribution across survival groups |
| 5️⃣ | 🍩 Overall Passenger Survival | Show overall survival proportions |
| 6️⃣ | ⚓ Survival by Embarkation Port | Compare survival across ports |
| 7️⃣ | 🔥 Correlation Heatmap | Examine numerical relationships |

---

# 🧠 Analysis Concepts Demonstrated

## 🐍 Python

- Importing libraries
- Working with variables
- Basic data-analysis workflow

## 🐼 Pandas

- `read_csv()`
- DataFrames
- `head()`
- `tail()`
- `isna()`
- `fillna()`
- `dtypes`
- `columns`
- `info()`
- `describe()`
- `duplicated()`
- `groupby()`
- `value_counts()`

## 🔢 NumPy

NumPy is imported as part of the project's numerical Data Science environment.

## 📊 Matplotlib

The project uses Matplotlib for:

- Figure creation
- Chart titles
- Axis labels
- Plot formatting
- Pie/donut visualization

## 🎨 Seaborn

Seaborn is used for:

- Count plots
- Bar plots
- Histograms
- Correlation heatmaps

## 📈 Exploratory Data Analysis

The project demonstrates:

```text
Data Loading
     ↓
Data Cleaning
     ↓
Data Exploration
     ↓
Statistical Summary
     ↓
Categorical Analysis
     ↓
Numerical Analysis
     ↓
Visualization
     ↓
Interpretation
```

---

# 💡 Why This Project Is Useful

The Titanic dataset is a practical way to learn the fundamentals of exploratory data analysis because it contains both **numerical** and **categorical** passenger information.

The project demonstrates how raw passenger records can be transformed into useful visual insights.

For example:

```text
Raw Data
   ↓
Passenger Attributes
   ↓
Survival Categories
   ↓
Grouped Analysis
   ↓
Charts
   ↓
Insights
```

This makes the project useful for practicing the basic workflow used in many real-world Data Science projects.

---

# ▶️ How to Run the Project

## 1️⃣ Install Python

Install Python 3.x on your computer.

Check the installed version:

```bash
python --version
```

---

## 2️⃣ Install Required Libraries

Run:

```bash
pip install numpy pandas matplotlib seaborn jupyter
```

---

## 3️⃣ Keep the Dataset in the Project Folder

The notebook expects:

```text
titanic_dataset.csv
```

Keep it in the same working directory as:

```text
Titanic.ipynb
```

The notebook loads it with:

```python
pd.read_csv("titanic_dataset.csv")
```

---

## 4️⃣ Start Jupyter Notebook

Run:

```bash
jupyter notebook
```

Open:

```text
Titanic.ipynb
```

---

## 5️⃣ Run the Notebook

Run the cells from top to bottom.

### Recommended order

```text
1. 📚 Import libraries
2. 📥 Load dataset
3. 👀 Preview first records
4. 🔚 Preview last records
5. 🧹 Check missing values
6. 🛠️ Handle Age values
7. 🧬 Check data types
8. 🗂️ Review columns
9. ℹ️ Check dataset information
10. 📐 Generate descriptive statistics
11. ♻️ Check duplicates
12. 👩 Analyze gender survival
13. 🎟️ Analyze passenger class
14. 🧳 Count passengers by class
15. 🎂 Analyze age distribution
16. 🍩 Analyze overall survival
17. ⚓ Analyze embarkation
18. 🔗 Select numerical variables
19. 🔥 Generate correlation heatmap
20. 🔑 Review findings
```

---

# 📌 Expected Project Flow

```text
             🚢 TITANIC DATA ANALYSIS
                       │
                       ▼
                📥 Load Dataset
                       │
                       ▼
                 🔎 Explore Data
                       │
                       ▼
                 🧹 Clean Data
                       │
                       ▼
              📊 Understand Dataset
                       │
             ┌─────────┼─────────┐
             ▼         ▼         ▼
           👩 Sex    🎟️ Class   🎂 Age
             │         │         │
             └─────────┼─────────┘
                       ▼
                   ⚓ Port
                       │
                       ▼
                 🍩 Survival
                       │
                       ▼
                🔥 Correlation
                       │
                       ▼
                 🔑 Findings
```

---

# 🎓 Learning Outcomes

After completing this project, you will have practical experience with:

### 🐼 Pandas

- Loading datasets
- Inspecting DataFrames
- Detecting missing values
- Working with columns
- Grouping records
- Counting categories
- Generating summaries

### 📊 Visualization

- Count plots
- Bar plots
- Histograms
- Pie/donut charts
- Correlation heatmaps

### 🧹 Data Cleaning

- Missing-value detection
- Missing-value handling
- Duplicate checking
- Dataset validation

### 🔗 Statistical Analysis

- Descriptive statistics
- Correlation matrices
- Numerical variable comparison

### 🧠 Data Interpretation

- Comparing categories
- Identifying patterns
- Summarizing observations
- Turning charts into analytical findings

---

# 🔮 Future Improvements

The current notebook can be extended into a more advanced Titanic analysis project.

## 📊 More Survival Analysis

Add:

- Survival rate instead of only survival count
- Survival by age group
- Survival by fare group
- Survival by family size
- Survival by title/name category

## 👨‍👩‍👧 Family Analysis

Create a new feature such as:

```text
Family Size = SibSp + Parch + 1
```

Then analyze survival based on family size.

## 💰 Fare Analysis

Explore:

- Average fare by class
- Fare distribution
- Fare vs survival
- Fare vs passenger class

## 🎂 Age Groups

Create categories such as:

```text
Child
Teenager
Adult
Senior
```

Then compare survival rates between groups.

## 🤖 Machine Learning

The cleaned dataset could be used as a foundation for:

- Logistic Regression
- Decision Trees
- Random Forest
- K-Nearest Neighbors
- Model evaluation
- Survival prediction

## 🖥️ Interactive Dashboard

The analysis could be converted into an interactive dashboard using:

```text
Streamlit
Plotly
Dash
```

Possible filters:

```text
🎟️ Passenger Class
👩 Gender
⚓ Embarkation Port
🎂 Age Range
💰 Fare Range
```

---

# ⚠️ Notes

- This project is an **educational exploratory data analysis project**.
- The analysis is based on the supplied `titanic_dataset.csv`.
- The notebook reports **891 records and 12 columns**.
- The duplicate check reports **0 duplicate records**.
- The notebook checks missing values and attempts median-based handling for `Age`.
- The visualizations use the variables and plotting logic already present in the notebook.
- The findings describe patterns in the supplied dataset and should not be interpreted as broader historical conclusions beyond the data analyzed.
- The notebook code is documented as provided, including the current `Age` assignment implementation.

---

# 🏆 Project Highlights

<div align="center">

| Area | Status |
|---|:---:|
| 📥 Dataset Loading | ✅ |
| 🔎 Data Exploration | ✅ |
| 🧹 Missing-Value Check | ✅ |
| 🧬 Data-Type Analysis | ✅ |
| 📐 Descriptive Statistics | ✅ |
| ♻️ Duplicate Check | ✅ |
| 👩 Gender Analysis | ✅ |
| 🎟️ Class Analysis | ✅ |
| 🎂 Age Analysis | ✅ |
| 🍩 Survival Analysis | ✅ |
| ⚓ Embarkation Analysis | ✅ |
| 🔥 Correlation Heatmap | ✅ |
| 🔑 Key Findings | ✅ |

</div>

---

# 🤝 Contributing

If you want to improve this project, you can:

```text
1. Fork the repository
2. Create a new branch
3. Add your analysis or improvement
4. Test the notebook
5. Commit your changes
6. Push the branch
7. Open a Pull Request
```

Possible contributions:

- 📊 New visualizations
- 🧹 Improved data cleaning
- 📈 Survival-rate analysis
- 👨‍👩‍👧 Family-size analysis
- 💰 Fare analysis
- 🤖 Machine-learning models
- 🖥️ Interactive dashboard

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

# 🚢 Titanic Dataset | Data Analysis

### **Data → Cleaning → Exploration → Visualization → Insights**

**Built with 🐍 Python · 🐼 Pandas · 🔢 NumPy · 📊 Matplotlib · 🎨 Seaborn**

### ⭐ If you found this project useful, consider giving the repository a Star!

**Made with ❤️ while learning Data Science**

</div>
