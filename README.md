# Pandas Practice Project  

A hands-on practice project designed to master essential Pandas skills for Data Engineering and Data Analysis.  
Includes real cleaning, transformation, grouping, merging, and feature engineering workflows.

---

## 📂 Files Included
- **Main.ipynb** – Jupyter Notebook containing all analysis  
- **pandas_practice.csv** – Main dataset with sales + weather features  
- **customers.csv** – (If used) Customer dataset for merging exercises  

---

## ▶️ How to Run

### 1. Create virtual environment
```bash
python3 -m venv venv
source venv/bin/activate
```

### 2. Install pandas
```bash
pip install pandas
```

### 3. Open the notebook
```bash
jupyter notebook
```

---

# 📘 What I Practiced in This Project

This project covers all essential beginner → intermediate Pandas operations used in real Data Engineering workflows.

---

## 🟦 1. Reading Data
- Loaded CSV files using `pd.read_csv()`
- Inspected with:
  - `df.head()`
  - `df.info()`
  - `df.describe()`

---

## 🟦 2. Filtering & Querying
Practiced selecting rows using conditions:

- Filter rows by numeric thresholds  
- Multi-column filtering  
- Boolean indexing  

Example concepts used:
```python
df[df["sales_amount"] > 50]
df[df["city"] == "Chicago"]
```

---

## 🟦 3. Handling Missing Values (Nulls)
Cleaned NaN values in:
- `temperature`
- `humidity`
- `windspeed`

Techniques used:
- Filling missing numeric values with the column mean  
- Checking NaNs with `.isna()`  
- Replacing with `.fillna()`  

---

## 🟦 4. Feature Engineering
Created new columns such as:

### ✔️ `sales_per_degree`  
```python
sales_amount / temperature
```

### ✔️ `feels_like_weather`
Categorized temperatures into:
- **Cold**
- **Warm**
- **Hot**

Using `apply` + `lambda`.

### ✔️ `is_big_purchase`
Labeled purchases:
- `"YES"` if sales_amount > 200  
- `"NO"` otherwise  

---

## 🟦 5. GroupBy Aggregations
Grouped data by:
- **city**
- **category**

Computed:
- total sales  
- average sales  
- counts  
- multiple aggregations using `.agg()`  

Example:
```python
df.groupby("category")["sales_amount"].agg(["sum", "mean", "count"])
```

---

## 🟦 6. Sorting & Ranking
Practiced sorting with:
```python
df.sort_values("temperature", ascending=False)
```

Used ranking functions to identify top rows.

---

## 🟦 7. Merging DataFrames
Joined sales data with customer data using:
- `merge()`
- `on="customer_id"`
- Inner join logic  

---

## 🟦 8. Concatenation
Split a dataframe and stacked it back using:
```python
pd.concat([df_part1, df_part2], axis=0)
```

---

## 🟦 9. Apply() for Row-Level Logic
Used `apply()` to create derived features and run conditional logic on each row.

Examples:
- Labeling purchases
- Creating temperature categories
- Computing custom metrics  

---

# 🎯 Project Outcome

By completing this project, I strengthened my skills in:

- Data cleaning  
- Data transformation  
- Feature engineering  
- Aggregations  
- Joins  
- Real-world Pandas workflows  

This notebook now serves as a **foundation for more advanced Data Engineering tasks**, including:

- ETL pipelines  
- Data validation  
- Exploratory Data Analysis (EDA)  
- Machine learning preprocessing  

