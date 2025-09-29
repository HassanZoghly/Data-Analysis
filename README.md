# Online Sales EDA

Exploratory Data Analysis (EDA) of an **online retail transactions dataset**.  
This project performs **data cleaning, revenue validation, feature engineering, and visual analytics** to uncover actionable insights about customer behavior, product categories, and regional sales trends.

---

## 📌 Project Overview
- **Dataset:** `Online Sales.csv` (~1,155 rows × 9 columns).
- **Goal:** Ensure data quality, validate revenue calculations, engineer business features, and extract insights for decision-making.
- **Key Deliverables:** Cleaned dataset, reproducible notebook, business KPIs, and visual summaries.

---

## 🛠️ Tools & Libraries
- [pandas](https://pandas.pydata.org/) – data wrangling, time series resampling  
- [NumPy](https://numpy.org/) – numerical operations  
- [matplotlib](https://matplotlib.org/) – base plotting  
- [seaborn](https://seaborn.pydata.org/) – statistical visualizations  
- [missingno](https://github.com/ResidentMario/missingno) – missing-value diagnostics  
- [SciPy](https://scipy.org/) – z-score & outlier detection  
- [JupyterLab](https://jupyter.org/) – interactive analysis  

---

## 🔑 Workflow

1. **Data ingestion**: Load raw CSV into `pandas`.  
2. **Data quality checks**: Detect missing values (with `missingno`), inconsistent types, and corrupted tokens.  
3. **Cleaning & fixing**:  
   - Convert prices, units, and dates to proper types.  
   - Recalculate `Total Revenue` from `Unit Price × Units Sold`.  
   - Resolve outliers via IQR and z-score capping.  
4. **Feature engineering**:  
   - Time features (`Month`, `Quarter`, `Day_of_Week`, `Is_Weekend`).  
   - Revenue tiers (Budget, Standard, Premium).  
   - Personas (based on `Product Category`, `Region`, `Payment Method`).  
5. **EDA & visualization**:  
   - Time series: daily revenue trends & moving averages.  
   - Product & region analysis: revenue drivers, transaction counts.  
   - Personas & tiers: customer segmentation insights.  

---

## 📊 Key Insights
- **Data quality matters:** Raw `Total Revenue` field was inconsistent; corrected with recomputation.  
- **Top revenue drivers:** Specific product categories & regions dominate revenue share.  
- **Customer segmentation:** High-value personas identified for targeted marketing.  
- **Seasonality:** Weekend & monthly patterns affect transaction counts and revenue.  

---

## 📂 Repository Structure
