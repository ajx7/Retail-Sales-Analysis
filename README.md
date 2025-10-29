# 🛒 Retail Sales Analysis using Python

## 📌 Project Overview
This project explores the **Global Superstore** dataset to uncover actionable insights about sales, profit, customers, and regional performance.  

The goal is to perform **end-to-end data analysis** using Python — from cleaning and feature engineering to exploratory data analysis (EDA), statistical testing, and key insights generation.

---

## 🎯 Objectives
- Understand sales and profit distribution across categories, regions, and segments.  
- Identify **key drivers** of profitability and **loss-making products**.  
- Perform **time-series trend analysis** and **customer behavior study**.  
- Use **statistical tests** to validate observed patterns.  
- Derive **data-backed recommendations** for strategic business decisions.

---

## 🧩 Dataset Information
**Source:** [Global Superstore Dataset (Kaggle)](https://www.kaggle.com/datasets)  
**Size:** ~51,000 rows  
**Key Columns:**
- `Order ID`, `Order Date`, `Ship Date`, `Ship Mode`
- `Customer ID`, `Segment`, `Region`
- `Category`, `Sub-Category`
- `Sales`, `Profit`, `Quantity`, `Discount`

---

## ⚙️ Tools & Libraries
- **Python 3.x**
- **Jupyter Notebook**
- `pandas`, `numpy`
- `matplotlib`, `seaborn`, `plotly`
- `scipy.stats` (for statistical testing)
- `datetime`
- `pycountry`

---

## 🧱 Project Structure

```
Retail-Sales-Analysis/
│
├─ data/
│ 	├─ global_superstore.csv
│ 	├─ global_superstore_clean.csv
│ 	└─ global_superstore_capped.csv
│
├─ notebook/
│ 	└─ retail_sales_eda.ipynb
│
├─ visuals/
│ 	├─ univariate/
│   │ 	├─ numerical_plots/
│   │	│	├─ delivery_days_plot.png
│   │	│	├─ discount_plot.png
│   │	│	├─ profit_margin_plot.png
│   │	│	├─ profit_plot.png
│   │	│	├─ quantity_plot.png
│   │	│	├─ sales_plot.png
│   │	│	└─ shipping_cost_plot.png
│   │	│
│   │ 	└─ categorical_plots/
│   │		├─ category_countplot.png
│   │		├─ market_countplot.png
│   │		├─ region_countplot.png
│   │		├─ segment_countplot.png
│   │		├─ ship_mode_countplot.png
│   │		└─ sub_category_countplot.png
│   │	
│ 	├─ bivariate/
│   │	├─ category_vs_profit.png
│   │	├─ category_vs_sales.png
│   │	├─ correlation_heatmap.png
│   │	├─ discount_vs_profit.png
│   │	├─ region_vs_category.png
│   │	├─ region_vs_profit.png
│   │	├─ segment_vs_profit.png
│   │	├─ segment_vs_ship_mode.png
│   │	├─ segment_vs_sales.png
│   │	├─ region_vs_profit.png
│   │	└─ shipmode_vs_deliverydays.png
│ 	│
│ 	├─ multivariate/
│   │	├─ profitabilityByRegionCategory.png
│   │	├─ region-category-subcategory.png
│   │	├─ SalesProfitBySegmentCategory.png
│   │	├─ top10customers.png
│   │	└─ top10ProductsByLoss.png
│   │	
│ 	├─ trend_analysis/
│   │	├─ category-sales-trend.png
│   │	├─ monthlytrend.png
│   │	├─ orderstrend.png
│   │	├─ yearlytrend.png
│   │	└─ year-month-trend.png
│   │
│ 	└─ advance_analysis/
│   	├─ AOVyearly.png
│   	├─ cohort.png
│   	├─ pareto.png
│   	├─ profitability.png
│   	└─ unique_customers.png
│  
├─ LICENSE	
├─ requirements.txt
└─ README.md
```


---

## 📊 Project Workflow
### **1. Setup & Imports**
Import all required libraries and define configurations.

### **2. Data Loading & Validation**
Load dataset and perform initial exploration (shape, dtypes, missing values).

### **3. Data Cleaning & Feature Engineering**
- Convert date columns and remove extra spaces  
- Handle missing values & duplicates  
- Engineer features like `Delivery_Days`, `Month_Year`, etc.  
- Detect and cap outliers for `Sales`, `Profit`, and `Shipping_Cost`.

### **4. Exploratory Data Analysis (EDA)**
- **Univariate:** Distribution of sales, profit, discounts, categories.  
- **Bivariate:** Relationship between discount, profit, and segment.  
- **Multivariate:** Combined effect of region, category, and segment.  
- **Trend Analysis:** Monthly and yearly sales & profit patterns.  
- **Customer Cohort:** Retention and AOV per year.  
- **RFM & Pareto Analysis:** Identify high-value customers and top contributors.  
- **Geographical Insights:** Regional sales visualization.

### **5. Statistical Testing**
To validate key findings:
- **Shapiro–Wilk Test:** Check normality of sales & profit.  
- **Correlation Test:** Numeric relationships.  
- **Kruskal-Wallis Test:** Profit differences by region, category, segment.  
- **Chi-Square Test:** Association between categorical variables.  
- **Mann–Whitney U Test:** Binary group comparisons (e.g., high vs low discount).

### **6. Key Insights & Recommendations**
Summarized actionable findings based on analysis and statistics.

### **7. Conclusion**
Wrap-up of project outcomes and business takeaways.

---

## 🔍 Key Insights
- **Highest sales** observed in **West and East regions**, but **profitability** varies across sub-categories.  
- **Furniture** often shows **high sales but low profit margins** due to high shipping and discounts.  
- **Technology** drives most of the profit, especially under **Corporate and Home Office segments**.  
- Sales **peak in Q4 each year**, suggesting strong **seasonal patterns** (likely due to festive or year-end promotions).  
- **Discounts beyond 20%** drastically reduce profit margins.  
- **Top 20% customers** contribute **~80% of total sales (Pareto principle)**.  
- **No significant profit difference across regions** (statistical validation supports this).

---

## 💡 Recommendations
- **Optimize discount strategy** — cap discounts near profitable thresholds (~15–20%).  
- **Focus marketing** on **top-performing segments (Technology & Office Supplies)**.  
- **Reduce shipping costs** for bulky items (especially Furniture) via logistics partnerships.  
- **Leverage Q4 trend** — plan stock and campaigns ahead of the sales surge.  
- **Customer retention programs** for high-value customers identified in RFM analysis.  
- **Periodic data review** — continuous tracking of profitability drivers.

---

## 🧠 Conclusion
This project demonstrates a **complete retail data analytics pipeline** using Python.  
It combines **cleaning, feature engineering, visualization, statistical inference**, and **business recommendations** — bridging the gap between data and decision-making.

---

## ▶️ How to Run
1. Clone the repository 
	```bash
	git clone https://github.com/ajx7/Retail-Sales-Analysis.git
	```

2. Navigate to the project directory
	```bash
	cd Retail-Sales-Analysis
	```

3. Install dependencies
	```bash
	pip install -r requirements.txt
	```

4. Run the Jupyter Notebook
	```bash
	jupyter notebook notebooks/retail_sales_eda.ipynb
	```

---

## 📖 Dataset Source

Global Superstore Dataset (publicly available on Kaggle):
[Global Superstore Dataset – Kaggle](https://www.kaggle.com/datasets/apoorvaappz/global-super-store-dataset)

---

## ⚖️ License

This project is licensed under the MIT License — free to use with attribution.