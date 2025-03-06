# Retail Sales Forecasting Analysis (2025 Edition)

# 📌 Business Problem  
Retail businesses face constant uncertainty about future sales, especially in seasonal or competitive markets. This project aims to analyze historical sales data to:  

- Identify sales trends and patterns.  
- Understand which products/regions drive revenue.  
- Build a basic sales forecasting model to help management predict future sales.  
- Provide business recommendations based on sales insights.  

The goal is to help the company optimize inventory, staffing, and marketing decisions for improved profitability.  

---  

## 📊 Dataset Information  
**Source:** Kaggle - Sales Transactions Dataset Weekly  
**File Name:** `Sales_Transactions_Dataset_Weekly.csv`  
**Description:** The dataset contains weekly sales transactions for different products across multiple stores, making it ideal for time series forecasting projects.  

---  

## 🔎 Project Steps & Analysis Conducted So Far  

### 1️⃣ Data Exploration (Initial Understanding)  
**Objective:**  
Before doing any analysis, we performed exploratory steps to understand the structure and quality of the data.  

#### Steps Taken:  
- Loaded the dataset.  
- Checked shape, columns, and sample rows.  
- Used `.info()` and `.describe()` for data type checks and summary statistics.  
- Verified missing values.  

#### Key Observations:  
- **811 products (SKUs)** in the dataset.  
- **52 weeks** of data (1 year).  
- Sales ranged from **0 to 63 units per week per product**.  
- **No missing values** — data quality is good.  
- Dataset has a **"long tail"** — most products have low weekly sales, with a few top sellers.  

---  

### 2️⃣ Outlier Detection & Analysis  
**Objective:**  
Outliers can distort analysis and models, so we investigated product sales to spot unusual spikes or dips.  

#### Steps Taken:  
- Calculated summary statistics (**mean, median, IQR**).  
- Created a **visualization of sales distributions**.  
- Identified products with **extremely high weekly sales (outliers)**.  
- Saved the plot for reference.  

#### Outlier Detection Approach:  
- Used **Box Plot Analysis**.  
- **Outliers** = Values outside **Q1 - 1.5*IQR** and **Q3 + 1.5*IQR**.  

#### Key Insights:  
- **Majority of SKUs** sell fewer than **20 units per week**.  
- Outliers mainly found in a **small number of high-demand products**.  
- **Clear long tail distribution** — a few bestsellers account for significant revenue, while most products have **low consistent sales**.  

#### Saved Plot:  
![Sales Outliers Plot](images/sales_outliers_plot.png)  

