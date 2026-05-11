# Amazon Sales Data Analytics Report

## Project Overview

This project analyzes the Amazon Sales Report dataset using Python libraries such as Pandas and Matplotlib. The main objective of this analysis is to understand sales trends, category performance, state-wise sales distribution, and monthly business performance.

---

# Steps Performed in Data Analytics

## 1. Import Libraries

The required libraries such as Pandas and Matplotlib were imported for data cleaning, analysis, and visualization.

```python
import pandas as pd
import matplotlib.pyplot as plt
```

---

## 2. Data Collection

The dataset was loaded from a CSV file using Pandas.

```python
df = pd.read_csv("Amazon Sale Report.csv")
```

---

## 3. Understanding the Dataset

The dataset structure, columns, data types, and missing values were checked using:

```python
df.info()
df.head()
df.shape
```

This helped in understanding the quality and structure of the dataset.

---

## 4. Data Cleaning

Several cleaning operations were performed:

* Removed unnecessary columns.
* Removed rows with missing Amount values.
* Standardized state names.
* Fixed spelling mistakes and duplicate state representations.

Example:

```python
df.dropna(subset=["Amount"], inplace=True)
```

---

## 5. Feature Engineering

New features were created from the Date column.

* Extracted Month
* Extracted Year

```python
df["new_month"] = df["Date"].dt.month
```

This made monthly analysis easier.

---

## 6. Exploratory Data Analysis (EDA)

Different analyses were performed:

### Category-wise Sales Analysis

Used groupby() to find total sales by category.

### State-wise Sales Analysis

Analyzed which states generated higher revenue.

### Monthly Sales Analysis

Checked sales trends for different months.

### Mizoram Sales Analysis

Special analysis was performed for Mizoram state and April month sales.

---

## 7. Data Visualization

Different graphs were created using Matplotlib:

* Bar Charts
* Line Charts
* Sales Trend Graphs

Example:

```python
monthly_sales.plot(kind='bar')
```

Visualizations helped in understanding sales patterns easily.

---

# Conclusion and Data Insights

## Key Findings

1. The dataset required significant cleaning because many state names were inconsistent and some records contained missing values.

2. The "Set" category generated one of the highest sales among all product categories.

3. Monthly sales analysis showed that sales varied across different months, indicating seasonal demand patterns.

4. Some states contributed much higher revenue compared to others, showing uneven sales distribution across India.

5. Mizoram had comparatively lower sales than major states, but category-wise analysis still helped identify customer preferences.

6. Data visualization made it easier to identify trends, high-performing categories, and monthly growth patterns.

7. Feature engineering using month and year extraction improved the analysis and allowed better business insights.

---

# Business Insights

* The company should focus more on high-performing categories to increase revenue.
* Low-performing states can be targeted with marketing campaigns and discounts.
* Seasonal sales trends can help in inventory planning.
* Proper data cleaning is important because incorrect state names can affect business reports.

---

# Final Result

This project successfully performed:

* Data Cleaning
* Data Transformation
* Exploratory Data Analysis
* Data Visualization
* Business Insight Generation

The analysis provided meaningful insights into Amazon sales performance and customer purchasing trends.

---

# Technologies Used

* Python
* Pandas
* Matplotlib
* Jupyter Notebook

---

# Overall Summary

The project demonstrates how raw sales data can be converted into meaningful business insights using data analytics techniques. By performing cleaning, analysis, and visualization, important trends and sales patterns were identified successfully.
