🪔 Diwali Sales Data Analysis
This project performs Exploratory Data Analysis (EDA) on Diwali sales data to understand customer purchasing behavior and identify patterns across different demographics and product categories.

📊 Project Overview
The Diwali Sales dataset provides a detailed look at retail transactions during the festive season. This project explores consumer buying patterns based on gender, age group, state, and occupation to help businesses optimize their sales and marketing strategies.

🗃️ Dataset Features
The dataset contains information about retail transactions, including:
User_ID / Cust_name  Gender / Age / Age Group  Marital_Status (renamed to Shaadi)  State / Zone  Occupation  Product_Category / Product_ID  Orders / Amount  


🛠️ Tools & Libraries UsedPython (version 3.13.9) 
Pandas 
NumPy  
Matplotlib 
Seaborn  
Jupyter Notebook

🧼 Data Cleaning & PreprocessingInspected dataset structure and data types. 
Removed completely blank columns (Status and unnamed1). 
Handled missing data by dropping $12$ null rows found within the Amount field.
Optimized data types by converting the Amount column from float to integer (int64).
Renamed Marital_Status to Shaadi to demonstrate schema modification.  

📈 Exploratory Data AnalysisData Inspection: Generated descriptive summary statistics to understand the overall dataset spread. 
Demographic Analysis: Used count plots to analyze transaction volumes across genders and age brackets.Financial Grouping: Evaluated total and average spending (Amount) mapped against specific target segments.  

🔑 Key Findings
Gender Purchasing Power: Female buyers significantly lead both the total order counts and the aggregate spending compared to male buyers.  
Statistical Spread: The average spending per transaction sits at approximately ₹9,453, with a maximum single-order threshold reaching up to ₹23,952.

🎯 ConclusionThis Exploratory Data Analysis provides key insights into consumer purchasing trends during Diwali. It effectively demonstrates fundamental data analytics techniques, including missing value mitigation, data type formatting, structural grouping, and data visualization.  

✍️ Author
Suraj Kumar
