# Titanic Dataset — Project 2
## Exploratory Data Analysis (EDA)

---

# Project Overview

This project focuses on performing Exploratory Data Analysis (EDA) on the Titanic dataset using Python and visualization libraries. The purpose of this project is to understand patterns, trends, distributions, and relationships between variables in the dataset.

The analysis helps transform raw data into meaningful insights for better understanding and future Machine Learning applications.

---

# Dataset Information

- Dataset: Titanic Dataset
- Source: Kaggle
- File Format: CSV

The dataset contains passenger information such as:

- Passenger ID
- Name
- Age
- Gender
- Passenger Class
- Fare
- Embarkation Port
- Survival Status

---

# Objectives

The main objectives of this project are:

- Perform descriptive statistical analysis
- Identify patterns and trends
- Analyze distributions
- Detect outliers
- Study relationships between variables
- Generate meaningful insights

---

# Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming Language |
| Pandas | Data Manipulation |
| NumPy | Numerical Operations |
| Matplotlib | Data Visualization |
| Seaborn | Statistical Visualization |
| Jupyter Notebook | Project Development |

---

# Libraries Used

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

---

# Exploratory Data Analysis Steps

## 1. Loading Dataset

```python
df = pd.read_csv("cleaned_titanic.csv")
```

---

## 2. Initial Inspection

```python
df.head()
df.info()
df.shape
df.columns
```

---

## 3. Descriptive Statistics

```python
df.describe()
```

Performed:

- Mean calculation
- Median calculation
- Count analysis
- Statistical summary

---

## 4. Survival Analysis

```python
sns.countplot(x="Survived", data=df)
plt.show()
```

Observation:

- Most passengers did not survive.

---

## 5. Gender Analysis

```python
sns.countplot(x="Sex", hue="Survived", data=df)
plt.show()
```

Observation:

- Female passengers had higher survival rates than males.

---

## 6. Age Distribution Analysis

```python
plt.hist(df["Age"], bins=20)
plt.show()
```

Observation:

- Most passengers were between 20–40 years old.

---

## 7. Fare Distribution Analysis

```python
plt.hist(df["Fare"], bins=30)
plt.show()
```

Observation:

- Fare values are right-skewed.

---

## 8. Outlier Detection

```python
sns.boxplot(x=df["Fare"])
plt.show()
```

Observation:

- Several outliers exist in the Fare column.

---

## 9. Passenger Class Analysis

```python
sns.countplot(x="Pclass", hue="Survived", data=df)
plt.show()
```

Observation:

- First-class passengers had better survival rates.

---

## 10. Correlation Analysis

```python
corr = df.corr(numeric_only=True)

sns.heatmap(corr, annot=True)

plt.show()
```

Observation:

- Passenger class and fare showed relationships with survival.

---

# Key Insights

- Female passengers had better survival chances.
- First-class passengers survived more often.
- Fare contains outliers.
- Most passengers belonged to the young adult age group.
- Passenger class influenced survival probability.

---

# Project Structure

```text
Titanic_Project2/
│
├── Titanic_Project2_EDA.ipynb
├── cleaned_titanic.csv
├── README.md
└── Titanic-Dataset.csv
```

---

# Key Learnings

- Exploratory Data Analysis (EDA)
- Data Visualization
- Correlation Analysis
- Outlier Detection
- Statistical Analysis
- Insight Generation
- Analytical Thinking

---

# Conclusion

EDA was successfully performed on the Titanic dataset. Various trends, distributions, and relationships were identified using statistical and visualization techniques.

The analysis provided meaningful insights and prepared the dataset for future Machine Learning applications.

---

# Future Work

This dataset can be further used for:

- Machine Learning Models
- Survival Prediction
- Classification Algorithms
- Advanced Analytics
- Predictive Modeling

---

# Author

Name: Krisha Patel

Batch: 2026

Domain: Data Analytics

---

# Thank You

DecodeLabs — Industrial Training Program