# 🛒 Online Sales Data Analysis  

## 📌 Overview  
This project performs an **end-to-end exploratory data analysis (EDA)** on an **online sales dataset**, focusing on **data cleaning, feature engineering, and business insight generation**.  

It demonstrates skills in data preprocessing, statistical analysis, visualization, and deriving actionable insights that can support data-driven decision-making in a retail/e-commerce context.  

---

## ⚙️ Workflow  

### 🔹 1. Data Ingestion  
- Reads `Online Sales.csv` into a `pandas` DataFrame.  
- Displays dataset metadata (`shape`, `.info()`, `.describe()`).  
- **Tool:** `pandas.read_csv`.  

### 🔹 2. Missing Value Analysis  
- Visualizes missingness with **missingno** (bar, matrix, heatmap).  
- Reports columns with highest missingness (`Product Name`, `Units Sold`, `Payment Method`).  
- Provides summary with counts & percentages of missing values.  

### 🔹 3. Data Cleaning & Type Conversion  
- Cleans formatting issues: removes `$`, strips `-ERROR`, fixes `x` multipliers.  
- Converts columns (`Unit Price`, `Units Sold` → numeric; `Date` → datetime).  
- Ensures consistent datatypes across the dataset.  

### 🔹 4. Revenue Validation  
- Recalculates revenue:  
  \[
  \text{Calculated Revenue} = \text{Unit Price} \times \text{Units Sold}
  \]  
- Compares with reported `Total Revenue`, fixes mismatches.  
- Guarantees integrity of financial metrics.  

### 🔹 5. Outlier Detection & Handling  
- Uses **IQR method** and **z-scores** for `Units Sold`, `Unit Price`, `Total Revenue`.  
- Caps/flags extreme values and removes implausible records.  
- **Tools:** `pandas`, `scipy.stats`.  

### 🔹 6. Feature Engineering  
- **Time features:** `Month`, `Quarter`, `Day_of_Week`, `Is_Weekend`, `Days_Since_First`.  
- **Business segments:**  
  - Revenue Tiers: *Budget / Standard / Premium* (quantiles).  
  - Value Segments: *Top quartile customers*.  
  - Order Types: *Single vs multi-item*.  
- **Customer Personas:** Rules based on `Product Category`, `Segment`, `Region`, and `Payment Method`.  

### 🔹 7. Exploratory Visualizations & KPIs  
- **Time series:** Daily revenue, transactions, moving averages.  
- **Category/Geography:** Revenue by product category, region, average order value.  
- **Distributions:** Histograms, boxplots, correlation heatmaps, bar charts.  
- **Tools:** `matplotlib`, `seaborn`.  

### 🔹 8. Business Insights  
- Identifies **top revenue-driving categories**.  
- Detects **regional differences** in revenue & transaction patterns.  
- Shows **payment methods linked to larger orders**.  
- Reveals **seasonality & customer segments** for targeted marketing.  

---

## 📊 Tools & Libraries  
- **Python**  
- **Pandas**  
- **NumPy**  
- **Matplotlib / Seaborn**  
- **Missingno**  
- **SciPy**  
- **Jupyter Notebook**  

---

## 🚀 Outcomes  
- Built a **cleaned, validated dataset** ready for modeling or dashboards.  
- Generated **customer personas & segments** for strategic targeting.  
- Delivered **visual KPIs** (time trends, product category insights, regional performance).  
- Produced **actionable recommendations** for business growth.  

---

## 📂 Repository Structure  
```bash
📦 Data_Analysis_Project
 ┣ 📜 Data_Analysis.ipynb    # Main notebook
 ┣ 📜 Online Sales.csv        # Dataset (if included)
 ┣ 📜 README.md               # Project documentation
 ┗ 📂 images/                 # Plots & visualizations
