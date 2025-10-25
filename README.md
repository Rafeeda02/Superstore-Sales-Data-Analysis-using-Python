# 🛒 Superstore Sales Analysis (Python Project)

## 📘 Project Overview
This project analyzes **Superstore Sales Data** using Python.  
The goal is to explore sales performance across categories, cities, and time periods to identify key insights and improve business decisions.

The project includes:
- Data cleaning and preparation  
- Exploratory data analysis (EDA)  
- Visualization of key metrics using Matplotlib & Seaborn  
- Business insights and recommendations  

---

## 🧠 Objective
- Identify **top-performing customers** and **most profitable categories**  
- Analyze **sales trends by date** and **profit correlation**  
- Find **most profitable cities**  
- Generate insights for improving business performance  

---

## 🧰 Tools & Libraries Used
- **Python**  
- **Pandas** — Data handling and cleaning  
- **NumPy** — Numerical operations  
- **Matplotlib & Seaborn** — Data visualization  
- **Datetime** — Date/time conversion and analysis  

---

## 📂 Dataset
**Dataset Name:** `Superstore.csv`  
**Rows:** 9994  
**Columns:** 21  

**Key Columns:**
- `Order Date`, `Ship Date`, `Category`, `Sub-Category`  
- `City`, `Region`, `Sales`, `Quantity`, `Discount`, `Profit`

---

## ⚙️ Data Preparation
```python
df = pd.read_csv("Superstore.csv", encoding='windows-1252')
df['Order Date'] = pd.to_datetime(df['Order Date'], format='%d-%m-%Y')
df['Ship Date'] = pd.to_datetime(df['Ship Date'], format='%d-%m-%Y')
df.set_index('Row ID', inplace=True)
df.drop_duplicates(inplace=True)
