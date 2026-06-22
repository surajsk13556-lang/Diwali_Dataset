# 🪔 Diwali Sales Data Analysis

An Exploratory Data Analysis (EDA) project using **Python** to analyze customer purchasing behavior during the Diwali festival. The analysis focuses on uncovering trends across demographics, geography, occupations, and product categories to help businesses optimize their sales and marketing strategies[cite: 1].

---

## 📊 Project Overview

This repository contains a detailed data cleansing and exploratory data analysis workflow on a dataset containing **11,251 rows and 15 columns** of retail transactions[cite: 1]. 

### Key Objectives:
* Perform end-to-end data cleansing (handling missing values, datatype correction, column dropping)[cite: 1].
* Analyze consumer buying patterns based on **Gender**, **Age Group**, **State**, and **Occupation**[cite: 1].
* Identify the highest-performing product categories and geographic zones[cite: 1].

---

## 🛠️ Tech Stack & Environment

* **Language:** Python `3.13.9` (Packaged by Anaconda, Inc.)[cite: 1]
* **Libraries Used:**
  * **Pandas:** Data manipulation and structural analysis[cite: 1].
  * **NumPy:** Numerical computing[cite: 1].
  * **Matplotlib & Seaborn:** Data visualization and plotting[cite: 1].

---

## 🗃️ Dataset Features

The source file `Diwali Sales Data.csv` contains the following structural fields[cite: 1]:

| Column Name | Description | Status in Cleaning |
| :--- | :--- | :--- |
| `User_ID` | Unique identifier for the customer[cite: 1] | Retained[cite: 1] |
| `Cust_name` | Name of the customer[cite: 1] | Retained[cite: 1] |
| `Product_ID` | Unique identifier for the product[cite: 1] | Retained[cite: 1] |
| `Gender` | Gender of the customer (F/M)[cite: 1] | Retained[cite: 1] |
| `Age Group` | Categorical age brackets (e.g., 26-35, 0-17)[cite: 1] | Retained[cite: 1] |
| `Age` | Actual age of the customer[cite: 1] | Retained[cite: 1] |
| `Marital_Status` | Marital status indicator[cite: 1] | Renamed to `Shaadi`[cite: 1] |
| `State` | Indian State of purchase[cite: 1] | Retained[cite: 1] |
| `Zone` | Geographic Zone (Western, Central, etc.)[cite: 1] | Retained[cite: 1] |
| `Occupation` | Industry/Profession of the customer[cite: 1] | Retained[cite: 1] |
| `Product_Category` | Category of the product bought[cite: 1] | Retained[cite: 1] |
| `Orders` | Total number of orders placed[cite: 1] | Retained[cite: 1] |
| `Amount` | Total transaction value[cite: 1] | Cleaned & converted to Integer[cite: 1] |
| `Status` / `unnamed1` | Blank/Unrelated tracking columns[cite: 1] | **Dropped** during preprocessing[cite: 1] |

---

## 🧼 Data Cleaning Highlights

The following preprocessing steps were applied directly to guarantee data integrity[cite: 1]:

1. **Dropping Empty Attributes:** Removed the completely blank `Status` and `unnamed1` columns[cite: 1].
2. **Handling Missing Values:** Detected and dropped $12$ null rows found within the `Amount` field, reducing the final row count to **11,239**[cite: 1].
3. **Datatype Optimization:** Casted the `Amount` column from a `float64` to a cleaner `int64` representation[cite: 1].
4. **Column Renaming:** Demonstrated schema flexibility by mapping `Marital_Status` to `Shaadi`[cite: 1].

```python
# Quick code glance at the cleaning sequence
df.drop(columns=['Status', 'unnamed1'], inplace=True, errors='ignore')
df.dropna(inplace=True)
df['Amount'] = df['Amount'].astype('int')
```[cite: 1]

---

## 📈 Initial Insights from EDA

* **Gender Purchasing Power:** Initial count plots and descriptive groups reveal that **Female (F)** buyers significantly lead both the total order counts and the aggregate transaction `Amount` compared to male buyers[cite: 1].
* **Statistical Spread:** The average spending per transaction sits at approximately **₹9,453**, with a maximum order threshold reaching up to **₹23,952**[cite: 1].

---

## 🚀 How to Run

1. Clone this repository to your local setup.
2. Make sure you have Anaconda or standard Python installed along with dependencies:
```bash
   pip install numpy pandas matplotlib seaborn
