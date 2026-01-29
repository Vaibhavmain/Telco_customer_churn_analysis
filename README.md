# 📊 Telco Customer Churn Analysis (Python | Pandas | Matplotlib)

## 🔹 Project Overview

This project focuses on analyzing customer churn for a telecom company using Python. The goal is to understand **why customers leave**, identify key churn drivers, and extract actionable business insights using real-world data.

This project is designed from a **recruiter and interview perspective**, emphasizing:

* Proper project structure
* Business-driven questions
* Clean data preparation
* Multiple types of visualizations
* Clear, explainable insights

---

## 🔹 Dataset

**Source:** Kaggle – Telco Customer Churn Dataset
**Rows:** 7,043 customers
**Columns:** 21 features

The dataset contains information about:

* Customer demographics
* Subscription services
* Contract and payment details
* Charges and tenure
* Churn status (target variable)

Target Variable:

* `Churn` (Yes = customer left, No = customer stayed)

---

## 🔹 Tools & Libraries Used

* **Python**
* **Pandas** – Data loading, cleaning, grouping, analysis
* **NumPy** – Numerical support
* **Matplotlib** – Data visualization

(Seaborn is intentionally NOT used to keep the project beginner-friendly and core-focused.)

---

## 🔹 Project Structure

### 1. Project Setup & Data Loading

* Imported essential libraries
* Loaded CSV file into Pandas DataFrame
* Checked dataset shape and structure
* Previewed data using `head()`
* Inspected column names and data types using `info()`

Why this matters:

> Establishes understanding of data before jumping into analysis.

---

### 2. Data Cleaning & Preparation

Key Issue Found:

* `TotalCharges` was stored as object (string) instead of numeric

Steps Performed:

* Converted `TotalCharges` to numeric using `pd.to_numeric()`
* Used `errors='coerce'` to handle invalid values
* Identified missing values created during conversion
* Removed rows with missing `TotalCharges`

Why this matters:

> Demonstrates real-world data quality handling and preprocessing.

---

### 3. Overall Churn Analysis

Business Question:

> What is the overall customer churn rate?

Analysis:

* Calculated churn counts using `value_counts()`
* Calculated churn percentage using normalized value counts

Visualization:

* Bar chart showing churn vs non-churn customers

Business Insight:

* Established baseline churn rate for further analysis

---

### 4. Contract Type vs Churn

Business Question:

> Does contract type affect customer churn?

Analysis:

* Used `pd.crosstab()` to compare Contract vs Churn
* Calculated churn percentage by contract type

Visualization:

* Bar chart showing churn rate by contract type

Key Insight:

* Month-to-month customers have significantly higher churn
* Long-term contracts (1 year, 2 year) improve retention

---

### 5. Tenure vs Churn (Customer Lifecycle)

Business Question:

> Do new customers churn more than long-term customers?

Steps:

* Created tenure groups using `pd.cut()`
* Grouped customers into lifecycle stages
* Calculated churn rate per tenure group

Visualization:

* Bar chart showing churn rate by tenure group

Key Insight:

* Highest churn occurs in first 12 months
* Churn decreases as tenure increases

Business Value:

* Highlights importance of onboarding and early engagement

---

### 6. Monthly Charges vs Churn

Business Question:

> Do higher monthly charges increase churn?

Analysis:

* Compared average MonthlyCharges by churn status

Visualization:

* Histogram comparing distribution of MonthlyCharges for:

  * Churned customers
  * Retained customers

Key Insight:

* Customers with higher monthly charges are more likely to churn
* Indicates price sensitivity and value perception issues

---

### 7. Internet Service vs Churn

Business Question:

> Does type of internet service affect churn?

Analysis:

* Cross-tabulation of InternetService vs Churn
* Calculated churn percentage per internet type

Visualization:

* Bar chart showing churn rate by internet service

Key Insight:

* Fiber optic customers show highest churn
* Suggests pricing or service quality expectations

---

### 8. Relationship Analysis (Scatter Plot)

Business Question:

> How do Monthly Charges vary with customer tenure?

Visualization:

* Scatter plot: Tenure vs Monthly Charges

* Introduces relationship analysis between numeric variables
* Shows customer value behavior over time

Business Value:

* Helps understand revenue patterns across customer lifecycle

---
 
---

## 🔹 Future Work (Planned Enhancements)

* Revenue impact of churn analysis
* High-risk customer profiling
* Simple churn segmentation
* Feature engineering
 

---
 

---
 

---

## 🔹 Author

Vaibhav Gaikwad
vaibhavgaikwad1632@gmail.com
 

---

 
